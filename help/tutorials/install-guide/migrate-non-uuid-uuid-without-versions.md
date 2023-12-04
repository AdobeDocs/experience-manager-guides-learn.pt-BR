---
title: Converter conteúdo não UUID sem versões em conteúdo UUID
description: Saiba como migrar conteúdo não UUID sem versões.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# Migrar conteúdo não UUID sem versões

>[!IMPORTANT]
>
> Você pode escolher essa abordagem de migração se quiser ignorar ou não as versões de ativos.


1. Baixe e carregue ativos da instância que não é UUID para a instância UUID diretamente da interface do usuário do AEM Assets usando ferramentas de Adobe, como o aplicativo para desktop AEM.

1. Habilite o fluxo de trabalho do ativo de atualização do DAM e execute-o em todos os ativos depois de importar o conteúdo para criação de GUID.
