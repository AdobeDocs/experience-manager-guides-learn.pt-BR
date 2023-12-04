---
title: Abrir tópico DITA ou mapear arquivos na mesma guia
description: Saiba como Abrir um tópico DITA ou mapear arquivos na mesma guia
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Abrir tópico DITA ou mapear arquivos na mesma guia {#id223HI0P202H}

Em alguns workflows, ao clicar em um link de um tópico ou arquivo de mapa, ele é aberto em uma nova guia. Isso pode levar a muitas guias abertas no navegador, o que pode afetar sua produtividade. Você pode alterar esse comportamento de abrir um tópico ou arquivo de mapa em uma nova guia e forçá-lo a abrir na própria guia atual. Para fazer isso, execute as seguintes alterações de configuração:

1. Abra a página Configuração do console da Web do Adobe Experience Manager.

   O URL padrão para acessar a página de configuração é:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Procure por e clique no link **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** pacote.

1. Selecione o **Abrir tópico/mapa DITA na mesma guia** opção.

1. Clique em **Salvar**.


Essa configuração afeta os seguintes locais de onde você pode acessar o tópico ou mapear arquivos:

- Crie o tópico DITA \(no final do fluxo de trabalho, ao clicar no botão **Abrir tópico** botão\)

- Crie o Mapa DITA \(no final do fluxo de trabalho, ao clicar no botão **Abrir mapa** botão\)

- Guia Tópicos no console do mapa DITA

- Guia Linhas de Base no console de mapa DITA

- Guia Relatórios no console de mapa DITA


**Tópico pai:**[ Personalizar editor da Web](conf-web-editor.md)
