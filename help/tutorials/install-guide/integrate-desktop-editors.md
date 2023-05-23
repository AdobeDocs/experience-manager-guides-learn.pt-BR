---
title: Integrar editores de XML baseados em desktop
description: Saiba como integrar editores XML baseados em desktop
source-git-commit: 5ac066bb8db32944abd046f64da11eeb1bdbe467
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# Integrar editores de XML baseados em desktop {#id181GB01G0HS}

Há muitos editores de XML disponíveis no mercado e você já pode estar usando um. O Adobe FrameMaker é um dos editores de XML mais eficientes, que vem com o conector AEM. Usando o conector AEM no FrameMaker, você pode se conectar facilmente com o repositório AEM, com arquivos de check-out e check-in e editar arquivos diretamente no FrameMaker. Você também pode configurar os Guias do AEM para iniciar o FrameMaker no Editor da Web. Depois que o arquivo for aberto no FrameMaker, você poderá editá-lo e verificá-lo novamente no repositório AEM.

## Habilitar edição de arquivos no FrameMaker a partir do Editor da Web

Você pode usar o FrameMaker ou qualquer outro editor DITA para criar e atualizar conteúdo DITA. No entanto, se sua organização usar o FrameMaker como editor DITA, você poderá dar aos usuários a opção de abrir documentos DITA diretamente no FrameMaker a partir do AEM.

Por padrão, os usuários não veem a variável **Abrir no FrameMaker** na barra de ferramentas do AEM. Execute as seguintes etapas para adicionar esse botão à barra de ferramentas do AEM:

1. Abra a página Configuração do console da Web do Adobe Experience Manager.

   O URL padrão para acessar a página de configuração é:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Procure por e clique no link **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** pacote.

   ![](assets/open-in-fm-toolbar.png){width="550" align="left"}

1. Selecione o **Mostrar botão Abrir no FrameMaker** opção.

1. Clique em **Salvar**.


Quando você habilita o **Mostrar botão Abrir no FrameMaker** e, em seguida, a **Abrir no FrameMaker** é exibido ao selecionar qualquer arquivo DITA no repositório AEM. Quando essa opção é *não ativado*, o **Abrir no FrameMaker** O botão é exibido somente quando você seleciona um arquivo .fm ou .book no repositório.

