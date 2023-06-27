---
title: Abrir tópico DITA ou mapear arquivos na mesma guia
description: Saiba como Abrir um tópico DITA ou mapear arquivos na mesma guia
source-git-commit: 4f15166b1b250578f07e223b0260aacf402224be
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---


# Abrir tópico DITA ou mapear arquivos na mesma guia {#id223HH0301J3}

Em alguns workflows, ao clicar em um link de um tópico ou arquivo de mapa, ele é aberto em uma nova guia. Isso pode levar a muitas guias abertas no navegador, o que pode afetar sua produtividade. Você pode alterar esse comportamento de abrir um tópico ou arquivo de mapa em uma nova guia e forçá-lo a abrir na própria guia atual.

Use as instruções fornecidas em [Substituições de configuração](download-install-additional-config-override.md#) para criar o arquivo de configuração. No arquivo de configuração, forneça os seguintes detalhes \(propriedade\) para abrir um tópico ou mapear arquivo em uma nova guia:

| PID | Chave de propriedade | Valor da propriedade |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.openinsametab` | Booleano \(true/false\). <br> **Valor padrão**: `false` |

Essa configuração afeta os seguintes locais de onde você pode acessar o tópico ou mapear arquivos:

- Crie o tópico DITA \(no final do fluxo de trabalho, ao clicar no botão **Abrir tópico** botão\)

- Crie o Mapa DITA \(no final do fluxo de trabalho, ao clicar no botão **Abrir mapa** botão\)

- Guia Tópicos no console do mapa DITA

- Guia Linhas de Base no console de mapa DITA

- Guia Relatórios no console de mapa DITA


**Tópico pai:**[ Personalizar editor da Web](conf-web-editor.md)

