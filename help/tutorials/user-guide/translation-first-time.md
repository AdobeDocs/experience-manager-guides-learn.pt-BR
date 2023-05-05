---
title: Práticas recomendadas para tradução de conteúdo
description: Saiba como adotar as Práticas recomendadas para tradução de conteúdo
exl-id: 4eff0f27-b3d1-4c6e-af88-bcb3f6d96990
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 1%

---

# Práticas recomendadas para tradução de conteúdo {#id1678G0S702F}

Considere o seguinte ponto para a tradução de conteúdo:

- Os nomes de pasta e arquivo devem estar em conformidade com os padrões de nomenclatura de arquivo, como: não deve haver espaços, apóstrofe, chaves, sinal de igual, caracteres especiais ou não ASCII.

- Se você traduzir o conteúdo em diferentes idiomas, deverá criar pastas correspondentes a cada idioma. Cada uma dessas pastas de idioma conterá o conteúdo correspondente a esse idioma. Por exemplo, você pode criar pastas usando o designador de idiomas como `de` para alemão, `fr` para francês e assim por diante. Ou você pode criar pastas usando designadores de idioma e região como `fr-FR` para o francês utilizado em França ou `fr-CA` para francês, conforme usado no Canadá.
- O idioma de destino também deve ter as localidades reais selecionadas de acordo com as pastas de idioma de destino em suas instâncias.
- A configuração de nuvem deve ser igual à da pasta de origem e deve haver apenas uma configuração de nuvem em uma pasta. Você pode criar várias pastas em /conf, se quiser usar vários conectores de tradução.
- Uma pasta não deve ter mais de 1000 arquivos.
- Certifique-se de que o usuário encarregado de iniciar o processo de tradução tenha permissões de Leitura, Modificação, Criação e Exclusão nas pastas de idioma de origem e de destino.
- Como a tradução do conteúdo requer a criação de um projeto de tradução, o usuário deve ter acesso para criar o projeto no AEM.
- Se você quiser usar Predefinições condicionais com seu mapa, deverá criá-las antes de iniciar o processo de tradução. Como as Predefinições condicionais também são agrupadas na versão traduzida do mapa, criar as predefinições antes de iniciar o processo de tradução garante que elas estejam disponíveis na versão traduzida.
- O processo de tradução de conteúdo deve ser iniciado no console do mapa DITA e não na interface do usuário do AEM Assets.
- O fluxo de trabalho de tradução DITA baseado em componentes não deve ser usado se você estiver traduzindo conteúdo por tradução humana. No entanto, essa opção deve ser usada para tradução automática.
- O conteúdo e a mídia globalmente usados que não exigem localização devem ser mantidos fora das cópias de idioma.
- Todo o conteúdo comum que deve ser localizado deve ser mantido em uma pasta comum na pasta do idioma.

A ilustração a seguir mostra um exemplo de uma estrutura de pastas no AEM quando você tiver usado globalmente o conteúdo e três cópias de idioma.

![](images/aem-directory_structure.png){width="800" align="left"}

## Configurar serviço de tradução

Execute as seguintes etapas para configurar o serviço de tradução humana ou de máquina a ser usado:

1. Na interface do usuário do Assets, selecione a pasta do idioma de origem.

1. Abra as propriedades da pasta e vá para **Cloud Services** guia .

1. No **Cloud Services** , configure o serviço de tradução que deseja usar.

   Você pode configurar a tradução automática ou humana.

   Certifique-se de que haja apenas uma configuração para o conector de tradução em uma pasta. Várias pastas podem ser criadas em /conf, se houver vários conectores de tradução. A pasta do idioma de origem deve ter uma configuração de nuvem selecionada antes de iniciar o processo de tradução.

   >[!NOTE]
   >
   > Consulte [Configuração da estrutura de integração de tradução](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/integration-framework.html?lang=en) na documentação AEM para obter detalhes sobre a integração com serviços de tradução de terceiros.

1. Clique em **Salvar e fechar** para salvar as propriedades atualizadas da pasta.


>[!TIP]
>
> Consulte a *Tradução* no guia de práticas recomendadas para as práticas recomendadas de tradução de conteúdo.

## Criar um novo projeto de tradução

Execute as seguintes etapas para criar um projeto de tradução:

>[!NOTE]
>
> Antes de executar as etapas nesse procedimento, verifique se você criou as pastas de idioma raiz e de destino necessárias, conforme descrito na [Práticas recomendadas para tradução de conteúdo](#id1678G0S702F).

1. Na interface do usuário do Assets, clique no arquivo de mapa DITA.

1. Clique no botão **Tradução** guia .

1. No **Idiomas de destino** selecione a localidade para a qual deseja traduzir o projeto e clique em **Concluído**.

   Um Resumo e Detalhes de tópicos e ativos associados são mostrados.

   >[!IMPORTANT]
   >
   > O **Idiomas de destino** mostrar apenas os idiomas para os quais uma pasta de idioma é criada paralelamente ao idioma de origem. Uma pasta de idioma criada em qualquer outro nível, como um nível abaixo da pasta de idioma de origem também não é exibida. Certifique-se de criar todas as pastas de idioma de destino no mesmo nível da pasta de idioma de origem.

1. Selecione os tópicos que deseja enviar para tradução.

   Também é possível usar as seguintes opções de filtragem de tópicos:

   >[!NOTE]
   >
   > Depois de aplicar o filtro necessário, clique em **Concluído** no painel Filtro para filtrar tópicos com base em sua seleção.

   - **Status da tradução**: Escolha filtrar tópicos com base em seu status de tradução. As opções disponíveis são: Sincronizado, Cópia ausente, Em andamento e Sincronizado.
   - **Pesquisar**: Insira um ou vários termos para pesquisar nos títulos dos tópicos.
   - **Tipo de origem**: Escolha filtrar tópicos com base em seus tipos de arquivo. As opções disponíveis são: Tudo, DITA, Mapa DITA, Recurso.
   - **Versão de origem modificada após**: Escolha filtrar o tópico com base em sua data e hora de modificação. Todos os tópicos modificados após a data e hora especificadas são mostrados na lista.
   - **Linha de base**: Clique em Usar linha de base e escolha uma linha de base criada no mapa. Todos os arquivos que fazem parte da Linha de base selecionada são mostrados na página Tradução . Você pode escolher os arquivos desejados na linha de base e prosseguir com o processo de tradução. Após a tradução do conteúdo, é possível exportar a Linha de base traduzida. Para obter mais detalhes sobre como exportar a linha de base traduzida, consulte [Exportar linha de base traduzida](generate-output-use-baseline-for-publishing.md#id196SE600GHS).
1. Clique em **Criar/atualizar cópias de idioma** na parte inferior do painel Filtro.

1. No **Projeto** lista, selecione **Criar um novo projeto de tradução**.

   >[!NOTE]
   >
   > Se você já tiver um projeto de tradução, poderá adicionar tópicos a esse projeto. Selecionar **Adicionar ao projeto de tradução existente** da **Projeto** e escolha um projeto na **Projeto de tradução existente** lista.

1. No campo **Título do projeto**, informe um título para o projeto.

1. Selecione o **Incluir mapa DITA** para enviar o mapa para tradução.
1. Clique em **Iniciar** para criar um novo projeto de tradução.

   Um novo projeto de tradução é criado com a versão selecionada dos tópicos. No momento, uma mensagem pop-up é exibida confirmando que o projeto de tradução foi criado. Quando todas as cópias de idioma de destino estiverem disponíveis no projeto de tradução, você receberá uma notificação na Caixa de entrada. Depois que a área de cópias de idioma de destino estiver disponível no projeto de tradução, você poderá prosseguir e iniciar o trabalho de tradução.


## Iniciar o trabalho de tradução {#id225IK030OE8}

Execute as seguintes etapas para iniciar o trabalho de tradução:

1. No **Projetos** , navegue até a pasta do projeto criada para localização.

1. Clique no projeto de localização para abrir a página de detalhes.

1. Clique na seta na **Tarefa de tradução** bloco e selecione **Iniciar** na lista para iniciar o fluxo de trabalho de tradução.

   >[!NOTE]
   >
   > Se você estiver usando o serviço de tradução Humana, será necessário exportar o conteúdo para tradução. Depois de ter o conteúdo traduzido, é necessário importá-lo de volta para o projeto de tradução.

1. Para exibir o status do trabalho de tradução, clique nas reticências na parte inferior do **Tarefa de tradução** mosaico.


Após a conclusão da tradução, o status do trabalho de tradução muda para *Pronto para revisar*. Para concluir o processo de tradução, é necessário aceitar a cópia traduzida e os metadados do ativo do bloco Tarefa de tradução no console Projeto .

>[!NOTE]
>
> Se você rejeitar a tradução de um ou mais tópicos em um trabalho de tradução, a variável **Em Andamento** o status de tradução de todos os tópicos rejeitados é revertido para o status original. O status dos tópicos referenciados é verificado e revertido de acordo com o estado de tradução mais recente. Além disso, os arquivos de tradução criados no projeto de destino não são excluídos, mesmo se a tradução for rejeitada para eles.

**Tópico principal:**[ Traduzir conteúdo](translation.md)
