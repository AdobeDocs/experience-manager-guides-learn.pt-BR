---
title: Editar tópicos no Editor da Web
description: Saiba como editar tópicos no Editor da Web
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---


# Editar tópicos no Editor da Web {#id2056B040VUI}

O Editor da Web vem com vários recursos de edição que permitem criar ou modificar facilmente seus arquivos de tópicos. Em geral, você executaria as seguintes etapas para editar um tópico no Editor da Web.

>[!IMPORTANT]
>
> Se você encontrar um erro de aplicativo ao trabalhar no Editor da Web, atualize a página para continuar trabalhando.

1. Para fazer alterações em seu tópico, clique dentro do limite de texto do elemento necessário e comece a fazer edições.

1. Para inserir um elemento específico, clique no final do elemento, depois do qual deseja inserir o novo elemento e clique no ícone de elemento necessário na barra de ferramentas. Também é possível usar o atalho de teclado `Alt+Enter` para invocar o **Inserir elemento** pop-up.

   Uma lista de elementos é exibida e pode ser usada no tópico. AEM Guias faz uma inserção inteligente de elementos de acordo com seu local válido no tópico.

   >[!NOTE]
   >
   > Você também pode escolher qual ícone será exibido na barra de ferramentas, configurando o `ui_config.json` arquivo localizado em - `/etc/designs/fmdita/clientlibs/xmleditor/`. Para obter mais informações sobre como personalizar recursos, entre em contato com o administrador do sistema.

1. Depois de concluir a edição do documento, clique em **Salvar**.

   >[!NOTE]
   >
   > Se você não deseja confirmar as alterações em AEM repositório, clique em **Fechar** e, em seguida, clique em **Fechar sem salvar** na caixa de diálogo Alterações não salvas.

   **Atualizar navegador ao editar os arquivos**
AEM Guias fornece o suporte para atualizar o navegador enquanto você edita o conteúdo no Editor da Web. Este recurso ajuda você a continuar a editar o conteúdo caso encontre um erro de aplicativo durante o trabalho. Se você clicar em atualizar o navegador enquanto um ou mais arquivos com alterações não salvas forem abertos para edição, você será avisado que as alterações não salvas podem ser perdidas. Você tem a opção de cancelar a operação de atualização e salvar os arquivos para preservar as alterações.

   Mesmo ao atualizar o navegador, as exibições do painel esquerdo e direito são mantidas no Editor da Web. Por exemplo, o tópico ativo no painel Repositório é aberto novamente. O painel de mapa é mantido junto com o mapa aberto anteriormente.

   O tópico ativo ou mapa DITA é reaberto na área de edição de conteúdo.

   O painel direito também é reaberto e exibe a mesma exibição de antes da atualização.

   **Indicador de cópia de trabalho**
AEM Guias fornece o indicador de cópia de trabalho que mostra se o \(cópia de trabalho\) atual do arquivo está ou não sincronizado com a versão salva. Se você tiver alterado sua cópia atual e não tiver salvo seu arquivo, uma marca \* aparecerá junto com o título na guia arquivo do tópico. Este indicador atua como um lembrete para salvar suas alterações e desaparece ao salvar seu arquivo.

   ![](images/working-copy-text-update-indicator.png){width="550" align="left"}

   AEM Guias também indica se a última cópia \(trabalho\) salva do arquivo está ou não sincronizada com a versão salva. Se você tiver algumas alterações não salvas entre a cópia de trabalho e a última versão salva, uma marca \* aparecerá junto com as informações da versão mostradas no canto superior direito da guia Arquivo do tópico. Esse indicador atua como um lembrete para salvar e criar uma versão da sua cópia \(trabalho\) atual do arquivo.

   ![](images/version-update-indicator.png){width="550" align="left"}


**Tópico principal:**[ Trabalhar com o editor da Web](web-editor.md)

