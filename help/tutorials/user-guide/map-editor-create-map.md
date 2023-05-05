---
title: Criar um mapa
description: Saiba como criar um mapa
exl-id: d35ee09f-f951-4866-a2b1-e4b19f76e7a1
source-git-commit: 3bca42f0954afc2362ab24f369e698113324dbc3
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Criar um mapa {#id176FEN0D05Z}

AEM Guias fornece dois modelos de mapa prontos para uso - mapa DITA e Bookmap. Você também pode criar seus próprios modelos de mapa e compartilhá-los com seus autores para criar arquivos de mapa.

Execute as seguintes etapas para criar um arquivo de mapa:

1. Na interface do usuário do Assets, navegue até o local em que deseja criar o arquivo de mapa.

1. Clique em **Criar** \> **Mapa DITA**.

1. Na página Blueprint, selecione o tipo de modelo de mapa que deseja usar e clique em **Próximo**.

   >[!NOTE]
   >
   > A maneira como os tópicos são referenciados em um arquivo de mapa depende do modelo de mapa. Por exemplo, se você selecionar o modelo de Mapa, o tópico referenciará \(`topicref`\) são usadas para se referir a tópicos. No caso de um Bookmap, as referências de tópico são criadas usando o `chapter` no DITA.

   ![](images/map-template.png){width="650" align="left"}

1. Na página Propriedades , especifique o mapa **Título**.

1. \(Opcional\) Especifique o arquivo **Nome**.

   Se o administrador tiver configurado o nome automático do arquivo com base na configuração da UUID, você não verá a opção para especificar o nome do arquivo. Um nome de arquivo baseado em UUID é automaticamente atribuído ao arquivo.

   Se a opção de nomenclatura de arquivo estiver disponível, o nome também será sugerido automaticamente com base no Título do seu mapa. Se você quiser especificar manualmente o nome do arquivo de mapa, verifique se o nome do arquivo não contém espaços, apóstrofe ou chaves e termina com `.ditamap`.

1. Clique em **Criar**.

   A mensagem Map Created (Mapa criado) é exibida.

   Cada novo arquivo de mapa que você criar na interface do usuário do Assets **Criar** \> **Mapa DITA** ou o Editor da Web recebe uma ID de mapa exclusiva. Além disso, o novo mapa é salvo como a cópia de trabalho mais recente no DAM. Até salvar uma revisão de um mapa recém-criado, você não verá nenhum número de versão no Histórico de versões. Se você abrir o mapa para edição, as informações da versão serão mostradas no canto superior direito da guia do arquivo de mapa:

   ![](images/first-version-map-none.png){width="650" align="left"}

   As informações de versão de um mapa recém-criado são mostradas como *nenhum*. Ao salvar uma nova versão, é atribuído um número de versão como 1.0. Para obter mais informações sobre como salvar uma nova versão, consulte [Salvar como nova versão](web-editor-features.md#save-as-new-version-id209ME400GXA).

   Você pode optar por abrir o mapa para edição no editor de mapa configurado ou salvar o arquivo de mapa no repositório de AEM.

   >[!NOTE]
   >
   > Para usar o Editor de mapa avançado, acesse o arquivo de mapa no Editor da Web. Caso o administrador tenha configurado o Editor de mapa avançado como editor padrão nos arquivos de mapa, o arquivo de mapa será aberto diretamente no Editor de mapa avançado para edição. Consulte *Definir o Editor de mapa avançado como padrão* em Instalar e configurar os Guias do Adobe Experience Manager as a Cloud Service.


**Tópico principal:**[ Trabalhar com o Editor de Mapa](map-editor.md)
