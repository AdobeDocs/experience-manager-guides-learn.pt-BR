---
title: API REST para criar e ativar pacotes
description: Saiba mais sobre a API REST para criar e ativar pacotes
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# API REST para criar e ativar pacotes {#id198CF0260Y4}

A API REST a seguir permite criar e ativar pacotes CRX.

## Criar e ativar pacote

Um método POST que cria e ativa o pacote CRX.

**URL de solicitação**: http://*&lt;aem-guides-server>*: *&lt;port-number>*/bin/fmdita/ativate

**Parâmetros**: a consulta de solicitação consiste na cadeia de caracteres de regras JSON. O tipo de conteúdo da solicitação POST deve ser definido como `application/json; charset=UTF-8`.

**Exemplo**: os exemplos a seguir mostram a chamada da API usando o comando curl:

    &quot;
    curl -u &lt;*username*>:&lt;*password*> -H &quot;Content-Type: application/json; charset=UTF-8&quot; -k -X POST -d &quot;{[Cadeia de caracteres de regras JSON](create-ativate-package-java.md#example-create-ativate-package-id198JH0B905Z)}&quot; http://&lt;*aem-guides-server*>:&lt;*port-number*>/bin/fmdita/ativate
    &quot;
