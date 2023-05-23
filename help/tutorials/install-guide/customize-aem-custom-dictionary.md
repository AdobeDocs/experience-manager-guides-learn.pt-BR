---
title: Personalizar dicionário padrão do AEM
description: Saiba como personalizar o dicionário padrão do AEM
source-git-commit: 5ac066bb8db32944abd046f64da11eeb1bdbe467
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Personalizar dicionário padrão do AEM {#id209SD8000WU}

O Editor da Web pode ser configurado para usar o verificador ortográfico AEM ou o verificador ortográfico do navegador. Se optar por trabalhar com o verificador ortográfico AEM, você terá a flexibilidade de definir sua lista de palavras personalizadas. Essas palavras personalizadas são então adicionadas ao dicionário AEM e essas palavras não são sinalizadas \(como incorreto\) no Editor da Web.

Execute as seguintes etapas para criar sua lista de palavras personalizadas, que são adicionadas ao dicionário AEM:

1. Faça logon no AEM e abra o modo CRXDE Lite.

1. Navegue até o seguinte nó:

   /apps/fmdita/config

1. Crie um novo arquivo chamado user\_dictionary.txt.

1. Abra o arquivo e adicione uma lista de palavras que deseja definir no dicionário personalizado.

   A captura de tela a seguir mostra uma lista de palavras personalizadas adicionada ao arquivo user\_dictionary.txt:

   ![](assets/custom-words-list-dictionary.png){width="650" align="left"}

1. Salvar e fechar o arquivo.


Os autores precisariam reiniciar a sessão do Editor da Web para atualizar a lista de palavras personalizadas no dicionário AEM.

**Tópico pai:**[ Personalizar editor da Web](conf-web-editor.md)

