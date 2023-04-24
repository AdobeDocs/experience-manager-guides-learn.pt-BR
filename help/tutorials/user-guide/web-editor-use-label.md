---
title: Usar rótulos
description: Saiba como usar rótulos
source-git-commit: 331871308035441f047b1ed588215b586daf3d28
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---


# Usar rótulos {#id164JBG0M0T1}

AEM Guias permitem adicionar rótulos a diferentes versões de um arquivo. Você pode usar esses rótulos para especificar a versão que deseja incluir em uma linha de base para publicação. Para obter mais informações sobre o uso de rótulos para criar uma linha de base, consulte [Trabalhar com linha de base](generate-output-use-baseline-for-publishing.md#).

Por exemplo, se você deseja usar *versão 1.0* de um tópico em *versão 1.0* e *versão 1.1* do mesmo tópico em *versão 2.0*, é possível adicionar *versão 1.0* no rótulo *versão 1.0* e *versão 2.0* no rótulo *versão 1.1*.

Depois de adicionar os rótulos, você pode criar uma linha de base e especificar qual versão do tópico deve ser incluída para publicação usando essa linha de base. Para ver qual versão deve ser incluída ou excluída em uma linha de base, você pode usar a opção Histórico de versão .

## Adicionar um rótulo

Execute as seguintes etapas para adicionar um rótulo ao seu tópico:

1. Na interface do usuário do Assets, selecione um tópico
1. Clique no ícone do seletor do painel à esquerda e selecione **Histórico da versão**.
1. No Histórico de versões, clique em uma versão onde deseja adicionar um rótulo.

1. Insira um rótulo para a versão selecionada e pressione Enter. Por exemplo, *Versão 2.6*.

   >[!NOTE]
   >
   > Não é possível adicionar o mesmo rótulo às diferentes versões de um tópico. No entanto, é possível adicionar vários rótulos à mesma versão de um tópico.

   Os rótulos são exibidos no Histórico de versão do tópico selecionado. A captura de tela a seguir exibe os rótulos *Versão x.x* e *Guia do usuário* adicionado à versão realçada do tópico.


![](images/labels.png)

>[!NOTE]
>
> Usando uma linha de base, você pode adicionar um rótulo a vários tópicos. Para obter mais informações sobre como adicionar rótulos usando a linha de base, consulte [Adicionar rótulos a uma linha de base](generate-output-use-baseline-for-publishing.md#id184KD0T305Z).

## Excluir um rótulo

Execute as seguintes etapas para excluir um rótulo:

1. Na interface do usuário do Assets, selecione um tópico que tenha um rótulo adicionado a ele.
1. Clique no ícone do seletor do painel à esquerda e selecione **Histórico da versão**.

   No Histórico de versões, você verá todas as versões de um tópico e os rótulos anexados a ele. A imagem a seguir mostra um exemplo de diferentes versões de um tópico e uma versão tem rótulos adicionados a ele.

   ![](images/labels.png)

1. Clique no botão de exclusão \(**X**\) para excluir o rótulo.

   ![](images/delete-labels.png)


**Tópico principal:**[ Trabalhar com o editor da Web](web-editor.md)

