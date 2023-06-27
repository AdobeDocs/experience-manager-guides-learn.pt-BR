---
title: Configurar o prompt para salvar como uma nova versão ao fechar
description: Saiba como Configurar o prompt para salvar como uma nova versão ao fechar
source-git-commit: 4f15166b1b250578f07e223b0260aacf402224be
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---


# Configurar o prompt para salvar como uma nova versão ao fechar {#id222HBI00XXA}

Quando o usuário tenta fechar um arquivo aberto no Editor da Web usando o **Fechar** na guia do arquivo ou na guia **Fechar** no menu Opções, uma caixa de diálogo será exibida se o arquivo tiver dados não salvos ou uma versão não salva. O usuário será solicitado a salvar o arquivo como uma nova versão se a versão não for salva.

Use as instruções fornecidas em [Substituições de configuração](download-install-additional-config-override.md#) para criar o arquivo de configuração. No arquivo de configuração, forneça os seguintes detalhes \(propriedade\) para configurar um prompt para salvar como uma nova versão ao fechar:

| PID | Chave de propriedade | Valor da propriedade |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.savenewversion` | Booleano\\ ( true/ false\). <br>  **Valor padrão**: verdadeiro |

Quando essa configuração estiver ativada, a variável **Salvar como uma nova versão** é marcada por padrão na caixa de diálogo.

Para obter mais detalhes, consulte *Cenários de fechamento e salvamento de arquivos* no guia as a Cloud Service Usar guias do Adobe Experience Manager.

**Tópico pai:**[ Personalizar editor da Web](conf-web-editor.md)
