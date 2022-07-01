---
title: Excluir parágrafos dentro de um tópico da tradução
description: Como excluir parágrafos dentro de um tópico da tradução
feature: Translation
role: User
exl-id: 21e41bb4-52f3-4352-92d9-4a60f636de99
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Como excluir parágrafos dentro de um tópico da tradução

A maneira mais fácil é usar um atributo translation=no .

+ Os autores podem inserir o atributo adicional como **translation=no** sobre os parágrafos que não pretendem traduzir. O fornecedor de tradução precisa ser informado e pode fazer a configuração ao final para ignorar o texto com este atributo.
+ A tradução automática de OOTB (com conector de tradução Microsoft de avaliação) exibe o mesmo comportamento.
+ Teste com a tradução do Microsoft : se você definir **translate=no** no nível do parágrafo, não traduz o parágrafo completo. Esse atributo pode ser definido em qualquer elemento e o conteúdo dentro desse elemento não será traduzido.


Aqui estão algumas capturas de tela que explicam isso ainda mais:

**Conteúdo de origem**

![Conteúdo de origem](assets/source-content.jpg)

**Conteúdo traduzido em espanhol**

![Conteúdo traduzido em espanhol](assets/trans-content.jpg)
