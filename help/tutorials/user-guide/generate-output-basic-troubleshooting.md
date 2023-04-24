---
title: Solução de problemas básicos
description: Saiba como solucionar problemas básicos
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---


# Solução de problemas básicos {#id1821I0Y0G0A}

Ao trabalhar com AEM Guias, você pode encontrar erros ao publicar ou abrir o documento. Esses erros podem estar no mapa DITA, no tópico ou no processo dos Guias AEM. Esta seção fornece informações sobre como acessar e analisar informações no arquivo de log de geração de saída. Além disso, se o tópico do DITA for muito grande, você poderá ver o erro de compilação do JSP. Esta seção também fornece informações sobre como resolver o erro de compilação JSP.

## Visualizar e verificar o arquivo de log {#id1822G0P0CHS}

Execute as etapas a seguir para visualizar e verificar o arquivo de log de geração de saída:

1. Depois de iniciar o processo de geração de saída, clique em **Saídas** no console do mapa DITA.

   O **Geral** da coluna **Saídas Geradas** mostra os ícones para dar uma dica visual sobre o sucesso ou a falha da geração de saída.

   ![](images/output-general-settings.png)

   Na captura de tela acima, o primeiro e o terceiro ícones mostram a geração de saída com falha. O segundo ícone mostra uma geração de saída bem-sucedida, mas com mensagens. A última é uma geração de saída bem-sucedida sem qualquer mensagem.

1. Clique no link no **Gerado em** após a conclusão da tarefa.

   O arquivo de log é aberto em uma nova guia.

   ![](images/log-file.png)

1. Aplique os seguintes filtros para realçar o texto no arquivo de log:
   - Fatal: Destaca os erros fatais no arquivo de log com cor rosa.
   - Erro: Destaca os erros no arquivo de log com cor laranja.
   - Aviso: Destaca os avisos no arquivo de log com cor violeta.
   - Informações: Destaca as mensagens de informação no arquivo de log com cor azul.
   - Exceção: Destaca as exceções no arquivo de log com cor amarela.
1. Use os botões de navegação para cima e para baixo para ir para o texto destacado no arquivo de log.

   Como alternativa, role pelo arquivo de log e verifique as mensagens.


## Copie e verifique o arquivo de log em um editor de texto

Execute as seguintes etapas para copiar e verificar o arquivo de log de geração de saída em um editor de texto:

1. Depois de iniciar o processo de geração de saída, clique em **Saídas** no console do mapa DITA.

1. Clique no link no **Gerado em** após a conclusão da tarefa.

   O arquivo de log é aberto em uma nova guia.

1. Clique em **Copiar registro** botão. O arquivo de log é copiado para a área de transferência.
1. Abra um editor de texto e cole o arquivo de log no editor.

1. Percorra o arquivo de log e verifique se há mensagens.

   As informações a seguir ajudarão você a determinar se há um erro no arquivo DITA ou no processo de Guias de AEM:

   - *Erro relacionado ao arquivo do mapa DITA*: Caso haja um erro encontrado no arquivo de mapa DITA ou em qualquer outro arquivo contido no mapa DITA, o arquivo de log conterá uma string, &quot;BUILD FAILED&quot;. Você pode verificar as informações fornecidas no arquivo de log para localizar o arquivo incorreto e corrigir o problema.

      No seguinte trecho do arquivo de log de exemplo, você pode ver o `BUILD FAILED` juntamente com o motivo do erro.

      ![](images/dita-error-in-log-file.png)

      - *Erro relacionado a guias de AEM*: O outro tipo de erro que você pode identificar no arquivo de log está relacionado ao próprio processo Guias AEM . Nesse caso, o arquivo de mapa DITA é analisado com êxito, mas o processo de geração de saída falha devido a algum erro interno nos Guias AEM. Para esse tipo de erro, você precisa buscar ajuda da equipe de suporte técnico.

         No seguinte trecho do arquivo de log de exemplo, você pode ver o `BUILD SUCCESSFUL` , seguida de outro erro técnico.

         ![](images/process-error-in-log-file.png)


## Resolver erro de compilação JSP

Se o tópico do DITA for muito grande, você poderá ver o erro de compilação do JSP \(`org.apache.sling.api.request.TooManyCallsException`\) no seu navegador. Este erro pode aparecer quando você abre um tópico para edição, revisão ou publicação.

Execute as seguintes etapas para resolver esse problema:

1. Na Navegação global, selecione Ferramentas e escolha Operações \> Console da Web.

   A página Configuração do console da Web do Adobe Experience Manager é exibida.

1. Procure por e clique no botão *Servlet principal Apache Sling* componente.

   As opções configuráveis para o Apache Sling Main Servlet são exibidas.

1. Aumente o valor da variável *Número de chamadas por solicitação* conforme seus requisitos.


**Tópico principal:**[ Geração de saída](generate-output.md)

