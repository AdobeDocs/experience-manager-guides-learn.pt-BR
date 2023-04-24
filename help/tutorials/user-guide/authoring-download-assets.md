---
title: Baixar arquivos
description: Saiba como Baixar arquivos
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# Baixar arquivos {#id216MC0H0BE8}

É possível baixar ativos, incluindo arquivos DITA e não-DITA. Há várias maneiras de baixar ativos, alguns métodos são nativos de AEM e outros são compatíveis com AEM Guias. Para obter informações sobre download de ativos nativos AEM, consulte [Baixar ativos do Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/download-assets-from-aem.html) na documentação AEM. A seção a seguir explica o mecanismo de download de arquivos por meio do console de mapa DITA nos Guias AEM.

## Exportar um arquivo de mapa DITA

Depois de ter o arquivo de mapa DITA no repositório AEM, é possível baixar o arquivo de mapa junto com seus dependentes. Isso proporciona a flexibilidade de compartilhar o arquivo de mapa completo para edição, validação, revisão ou simplesmente criar um backup offline.

Execute as seguintes etapas para baixar um arquivo de mapa DITA junto com seus arquivos dependentes:

1. Na interface do usuário do Assets, navegue até o mapa DITA que deseja baixar.

1. Clique no mapa DITA para abri-lo no console do mapa DITA.

1. Selecione o **Tópicos** para ver uma lista de tópicos disponíveis no mapa DITA.

1. Na barra de ferramentas principal, clique em **Mapa de download**.

   A caixa de diálogo Baixar mapa é exibida.

   ![](images/download-map.png){width="300" align="left"}

1. Clique em **Baixar**. Na caixa de diálogo Baixar mapa, você pode escolher as seguintes opções:

   - **Usar linha de base**: Selecione essa opção para obter uma lista de Linhas de base criadas para o mapa DITA. Para baixar o arquivo de mapa e seu conteúdo com base em uma Linha de Base específica, selecione a Linha de Base na lista suspensa. Para obter mais detalhes sobre como trabalhar com Linhas de Base, consulte [Trabalhar com linha de base](generate-output-use-baseline-for-publishing.md#).
   - **Nivelar hierarquia de arquivo**: Selecione essa opção para salvar todos os tópicos e arquivos de mídia referenciados em uma única pasta.

   >[!NOTE]
   >
   > Também é possível baixar o arquivo de mapa sem selecionar qualquer opção. Nesse caso, a última versão mantida dos tópicos e arquivos de mídia referenciados é baixada.

1. Depois de clicar no botão **Baixar** , a solicitação de download de mapa é enfileirada. Você receberá a seguinte notificação quando o mapa estiver pronto para download.

   ![](images/download-map-prompt.png){width="550" align="left"}

   - Clique em **Baixar** para baixar o arquivo de mapa no formato .zip.

   - Clique em **Baixar mais tarde** para baixar o arquivo de mapa posteriormente. O link de download pode ser acessado na Caixa de entrada da notificação de AEM. Clique na notificação de mapa gerada na Caixa de entrada para baixar o mapa no formato .zip.
   >[!NOTE]
   >
   > Por padrão, os mapas baixados permanecem por cinco dias na Caixa de entrada de notificação de AEM.

![](images/download-map-inbox.png){width="300" align="left"}

Após o download do mapa, você pode selecionar o mapa e usar o ícone Open na parte superior para abrir o relatório selecionado.

**Tópico principal:**[ Gerenciar conteúdo](authoring.md)

