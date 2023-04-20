---
title: Adicionar estilos personalizados ao editor de guias
description: Saiba como adicionar estilos personalizados para alterar a aparência do editor de Guias.
source-git-commit: 9e7d5bb4c8f6c6ebe21bfcebdd7d2e13971b8df2
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Adicionar estilos personalizados ao editor de guias

Neste artigo, aprenderemos como adicionar estilos personalizados para alterar a aparência padrão do webeditor.

Isso envolverá as seguintes etapas:
- Adicionar os estilos personalizados por meio da Configuração do editor XML do perfil de pasta
- Escolha do respectivo perfil de pasta no webeditor e teste as alterações


## Implementar tomando um exemplo

Vamos entender isso com um exemplo em que queremos mostrar a breve descrição e título como um bloco separado com alguns aspectos de estilo no editor.

![Visualização do editor de conteúdo com estilos personalizados](../../../assets/authoring/webeditor-customstyles-preview.png)


## Implementar


### Adicionar o CSS personalizado ao perfil da pasta

Use os perfis de pasta para verificar a variável *css_layout.css* na guia &quot;Configuração do editor XML&quot; e adicione o CSS com estilos personalizados

[use este link para saber mais sobre o perfil da pasta e configurar o layout do modelo de CSS](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/videos/advanced-user-guide/editor-configuration.html?lang=en#customize-the-css-template-layout)

Use o seguinte para configurar o estilo acima em seu editor:
- Use [css_layout.css](../../../assets/authoring/webeditor-customstyles-css_layout.css) e carregue-o no perfil da pasta de sua escolha
- Instale o pacote anexado [webeditor-styles-resources.zip](../../../assets/authoring/webeditor-styles-resources.zip) usando AEM gerenciador de pacotes para instalar os recursos usados no arquivo CSS acima

```
This will install the resources at path "/content/dam/resources" which will include sub-folders "fonts" and "images"
```


### Testes

- Abrir editor da Web
- Nas preferências do usuário, escolha o perfil da pasta no qual você adicionou os estilos personalizados. Se você a adicionou ao Perfil global, provavelmente já está usando.
- Abra um tópico; você observará que a área de edição deve ter interface do usuário personalizada

```
Please note this is compatible to AEM Guides version 4.2 and AEM Guides cloud version 2303 (March)
```


## Referências

Você também pode estar interessado na sessão especializada sobre configurações do editor e personalização abordada em [Sessão de especialistas sobre o webeditor](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/knowledge-base/expert-session/webbased-authoring-jan2023.html?lang=en)