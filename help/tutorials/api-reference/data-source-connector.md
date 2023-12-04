---
title: API REST para registrar um conector de fonte de dados
description: Saiba mais sobre a REST API para registrar um conector de fonte de dados
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# API REST para registrar um conector de fonte de dados {#id236LG0Y0CXA}

A API REST a seguir permite registrar um conector de fonte de dados.

## Registrar um conector de fonte de dados

Um método GET que registra um conector de origem de dados.

**URL de solicitação**:
`http://server:port/bin/guides/v1/konnect/config/register?path=<uploaded file path>`

**Parâmetro**: |Nome|Tipo|Obrigatório|Descrição| |—|—|—|—| |`path`|String|Sim|Uma string que aponta para um caminho no repositório AEM. Pode ser um caminho no estado `/content/dam or /var/dxml`.|

**Exemplo**:\
`http://host:4502/bin/guides/v1/konnect/config/register?path=/var/dxml/konnect/jira.json`
