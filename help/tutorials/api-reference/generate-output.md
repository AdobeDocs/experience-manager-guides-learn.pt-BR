---
title: API baseada em Java para trabalhar com a geração de saída
description: Saiba mais sobre a API baseada em Java para trabalhar com a geração de saída
source-git-commit: fad5049962f258bbe59c7d172436d82b3d6cd68f
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---


# API baseada em Java para trabalhar com a geração de saída {#id175UB30E05Z}

A seguinte API baseada em Java permite gerar saída para um mapa DITA. Essa API está disponível no formato de um pacote. Você deve incluir esse pacote no código para usar essas APIs.

Detalhes do pacote:

- ID do grupo: **com.adobe.fmdita**

- ID do artefato: **api**

- Versão: **3.4**

- Pacote: ****com.adobe.fmdita.api.maps****

- Detalhes da classe:

  ```JAVA
  public class **PublishUtils** extends Object
  ```

  A variável **`PublishUtils`** A classe contém um método para gerar saída para uma ou mais predefinições de saída.


## Gerar saída

A variável ``generateOutput`` O método gera a saída de um arquivo de mapa DITA usando as predefinições de saída especificadas.

**Sintaxe**:

```JAVA
public static void generateOutput(Session session,
String sourcePath,
String outputName)
throws GuidesApiException
```

**Parâmetros**: |Nome|Tipo|Descrição| |—|—|—| |`session`|javax.jcr.Session|Uma sessão JCR válida.| |``sourcePath``|String|Caminho \(no repositório AEM\) do arquivo de mapa DITA para o qual a saída precisa ser gerada.| |``outputName``|String|Nome da predefinição de saída\(s\) a ser usada para gerar saída. Várias predefinições de saída podem ser especificadas usando um delimitador de barra vertical \(&quot;\|&quot;\), por exemplo `aemsite\|pdfoutput`.|

**Exceção**: Lançamentos ``javax.jcr.RepositoryException``, `java.io.IOException`, e `java.lang.Exception`.

