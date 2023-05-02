---
title: Arquitetura e desempenho do microsserviço de publicação na nuvem
description: Entenda como o novo microsserviço permite a publicação escalável no AEMaaCS.
source-git-commit: c67cc61938b407c3b11c5f793c6becdc9e015670
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---


# Cloud Publishing Microservice Architecture and Performance Analysis

Este artigo compartilha os insights da arquitetura e alguns números de desempenho do novo microsserviço de publicação em nuvem.

>[!NOTE]
>
> Atualmente, a publicação com base em microsserviços nos Guias AEM suporta apenas a saída PDF usando a publicação Native PDF ou por meio do DITA-OT. AEM Guias adicionarão suporte à publicação baseado em microsserviços para mais tipos de saída em versões futuras.

## Problemas com fluxos de trabalho de publicação existentes na nuvem

A Publicação DITA é um processo que consome muitos recursos, dependendo principalmente da memória do sistema e da CPU disponíveis. A necessidade desses recursos aumenta ainda mais se as editoras estiverem publicando mapas grandes com muitos tópicos ou se várias solicitações de publicação paralelas forem acionadas.

Se você não estiver usando o novo serviço, toda a publicação ocorrerá no mesmo pod do Kubernetes(k8) que também está executando o servidor de nuvem AEM. Um pod k8 típico tem um limite na quantidade de memória e CPU que pode ser usada. Se o AEM Guias os usuários estiverem publicando cargas de trabalho grandes ou paralelas, esse limite poderá ser violado rapidamente. O K8 reinicia pods que estão tentando usar mais recursos do que o limite configurado, o que pode ter um impacto sério na própria instância da nuvem de AEM.

Essa restrição de recursos foi a principal motivação para criar um serviço dedicado que pode nos permitir executar várias cargas de trabalho de publicação simultâneas e grandes na nuvem.

## Introdução à nova arquitetura

O serviço está usando soluções de nuvem de ponta como o Adobe App Builder, Eventos de E/S, IMS para criar uma oferta sem servidor. Estes serviços baseiam-se, eles próprios, nos padrões industriais amplamente aceitos, como o Kubernetes, docker.

Cada solicitação para o novo microsserviço de publicação é executada em um contêiner de docker isolado que executa apenas uma solicitação de publicação por vez. Vários novos contêineres são criados automaticamente caso novas solicitações de publicação sejam recebidas. Essa configuração de contêiner único por solicitação permite que o microsserviço forneça o melhor desempenho aos clientes sem apresentar riscos de segurança. Esses contêineres são descartados depois que a publicação terminar, liberando assim os recursos usados.

Todas essas comunicações são seguras pelo Adobe IMS usando autenticação e autorização baseadas em JWT e são executadas por HTTPS.

<img src="assets/architecture.png" alt="guia projetos" width="600">

>[!NOTE]
>
> O processo de publicação executa algumas partes dependentes de conteúdo da solicitação no próprio servidor de AEM, como a geração de lista de dependências. No entanto, as partes mais exaustivas do processo de publicação, como a execução do DITA-OT ou mecanismo nativo, foram descarregadas para o novo serviço.


## Análise de desempenho

Esta seção mostra os números de desempenho do microsserviço. Observe que a arquitetura de nuvem antiga tinha problemas com a publicação de mapas grandes ou com a execução de várias publicações simultâneas, portanto, esta seção compara os números de desempenho do microsserviço com a oferta local dos Guias AEM.

Se você estiver publicando um mapa grande no local, talvez precise ajustar os parâmetros de heap do Java ou encontrar erros de falta de memória. Na nuvem, o microsserviço já tem o perfil e o heap Java ideal e outras configurações definidas imediatamente.

### Execução de uma publicação na nuvem e no local

* Nuvem

   Se você estiver executando uma única publicação na nuvem usando o novo serviço, a publicação poderá demorar um pouco mais quando comparada à publicação única no local. Esse pequeno tempo elevado se deve à natureza distribuída da nova arquitetura de nuvem.

   <img src="assets/cloud_single_publish.png" alt="guia projetos" width="600">

* No local

   Os resultados de uma única publicação são melhores na arquitetura de nuvem antiga ou no local, pois a publicação completa está acontecendo no mesmo pod/máquina em que a AEM está sendo executada.

   <img src="assets/onprem_single_publish.png" alt="guia projetos" width="600">

### Execução de várias publicações na nuvem e no local

* Nuvem

   O Novo Microserviço de Publicação brilha nesse cenário. Como você pode ver na imagem abaixo, com o aumento nos vários trabalhos de publicação simultâneos, a nuvem pode publicá-los sem nenhum aumento significativo no tempo de publicação.

   <img src="assets/cloud_bulk_publish.png" alt="guia projetos" width="600">

* No local

   A execução da publicação simultânea no local resulta em grave degradação do desempenho. Essa queda no desempenho é mais grave se as editoras estiverem publicando ainda mais mapas simultaneamente.

   <img src="assets/onprem_bulk_publish.png" alt="guia projetos" width="600">

## Benefícios adicionais

Alguns caminhos de cada solicitação de publicação devem ser executados na instância de AEM para buscar o conteúdo de publicação correto a ser enviado ao microsserviço. A nova arquitetura em nuvem usa AEM tarefas no lugar de AEM fluxos de trabalho, como era o caso na arquitetura antiga. Essa alteração permite que os administradores do AEM Guias configurem individualmente as configurações da fila de publicação na nuvem sem afetar outras tarefas AEM ou configurações do fluxo de trabalho.

Detalhes sobre como configurar o novo microsserviço de publicação podem ser encontrados aqui: [Configurar microsserviço](configure-microservices.md)