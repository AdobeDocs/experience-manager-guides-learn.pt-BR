---
title: Manipulador de eventos do processo de conversão
description: Saiba mais sobre o manipulador de eventos do processo de conversão
source-git-commit: 8707acf3ba01b7488eea6597c434da73a901d037
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# Manipulador de eventos do processo de conversão {#id175UB30E05Z}

O Guia do AEM expõe o evento com/adobe/fmdita/conversion/complete usado para executar qualquer operação de pós-processamento após a conclusão de um processo de conversão de documentos. Esse evento é disparado sempre que um documento não DITA é migrado para o formato de arquivo DITA. Por exemplo, se você executar uma conversão do Word para o DITA ou um processo de conversão do InDesign para o DITA, esse evento será chamado após o término do processo de conversão.

É necessário criar um manipulador de eventos do AEM para ler as propriedades disponíveis nesse evento e executar processamento adicional.

Os detalhes do evento são explicados abaixo:

**Nome do evento**:

```HTTP
com/adobe/fmdita/conversion/complete 
```

**Parâmetros**:\
|Nome|Tipo|Descrição| |—|—|—| |`status`|String|O status de retorno da operação executada. As opções possíveis são: - SUCESSO: o processo de conversão foi concluído com êxito. <br> - CONCLUÍDO COM ERROS: o processo de conversão foi concluído, mas com alguns erros. <br>- FALHA: o processo de conversão falhou devido a algum erro fatal.| |`filePath`|String|Caminho absoluto do arquivo de origem \(a ser convertido\) no repositório AEM.| |`outputPath`|String|Caminho absoluto do local de destino onde os arquivos DITA convertidos serão salvos.| |`logPath`|String|Caminho absoluto do nó onde o log de conversão será salvo.|
