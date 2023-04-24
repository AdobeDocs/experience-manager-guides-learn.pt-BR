---
title: Marcação em massa do conteúdo DITA
description: Saiba como marcar conteúdo DITA em massa
source-git-commit: 528dd5d33f38c29809e7e7dafd77d860daaba8db
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---


# Marcação em massa do conteúdo DITA {#id179SG0TN05Z}

Tags permitem agrupar ou classificar conteúdo em seu repositório de conteúdo e também na saída publicada. Se você tiver aplicado tags ao seu conteúdo, poderá encontrar facilmente tópicos relacionados em um mapa DITA que podem ajudá-lo a criar conteúdo. Com a saída publicada, os usuários finais poderão localizar o conteúdo correto com mais rapidez, com tags adequadas em vigor.

AEM Guias permitem marcar o conteúdo do DITA em alguns cliques. Você pode usar o recurso de marcação em massa para aplicar várias tags em vários tópicos, um mapa DITA ou em um submapa. Ou também é possível aplicar tags em um tópico individual. A marcação é o recurso nativo do AEM, você pode encontrar mais detalhes sobre a criação e o gerenciamento de tags no [Administração de tags](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/tags.html?lang=en) na documentação AEM.

Por padrão, AEM Guias não concede acesso de leitura a nenhum usuário na pasta onde todas as tags no repositório AEM são armazenadas. Para usar tags definidas no repositório AEM, você deve solicitar ao administrador do sistema que conceda acesso à pasta onde as tags são armazenadas.

## Aplicar tags em massa

Use o recurso de marcação em massa para aplicar várias tags ao mesmo tempo. Execute as seguintes etapas para aplicar tags aos seus tópicos em um mapa DITA:

1. Na interface do usuário do Assets, navegue até o arquivo de mapa DITA e clique nele.

   O console do mapa DITA é exibido mostrando a lista de Predefinições de saída disponíveis para gerar saída.

1. Clique em **Tópicos**.

   Uma lista de tópicos disponíveis no mapa DITA é exibida. As UUIDs dos tópicos são mostradas abaixo do título do tópico.

1. Selecione os tópicos ou o submapa nos quais deseja aplicar as tags.

   ![](images/apply-tags-uuid.png)


   >[!NOTE]
   >
   > A captura de tela acima mostra um submapa selecionado e expandido. Ao selecionar o submapa, todos os tópicos no submapa também são selecionados.

1. Clique em **Aplicar tags**.

   A caixa de diálogo Selecionar tags é exibida.

1. Selecione uma ou mais tags que deseja aplicar nos tópicos selecionados.

1. Confirme sua seleção.

   As tags selecionadas são aplicadas aos tópicos e mostradas ao lado do título do tópico.

   >[!NOTE]
   >
   > Depois de adicionar tags aos seus tópicos, se você mover ou excluir um tópico, as tags desses tópicos também serão removidas. No entanto, esse tópico permanece no mapa até que você o remova.


## Aplicar tags em um tópico individual

Execute as seguintes etapas para aplicar tags a um tópico individual:

1. Na interface do usuário do Assets, navegue e selecione o arquivo de tópico no qual deseja aplicar as tags.

1. Na barra de ferramentas, clique em **Propriedades**.

   A página de propriedades do tópico é exibida.

1. Na guia Básico , clique no ícone Procurar ao lado do **Tags** campo.

1. Selecione uma ou mais tags que deseja aplicar no tópico selecionado.

1. Confirme sua seleção.

1. Clique em **Aplicar tags**.

   As tags selecionadas são aplicadas ao tópico e mostradas no campo Tags .

1. Clique em **Salvar e fechar**.


## Remover tags

De acordo com as necessidades de sua empresa, você pode alterar as informações de marcação para qualquer tópico DITA. Você pode remover facilmente todas as tags de uma só vez ou remover apenas as tags que não são válidas no tópico.

Execute as seguintes etapas para remover todas as tags de um ou mais tópicos:

1. Na interface do usuário do Assets, navegue até o arquivo de mapa DITA e clique nele.

   O console do mapa DITA é exibido mostrando a lista de Predefinições de saída disponíveis para gerar saída.

1. Clique em **Tópicos**.

   Uma lista de tópicos disponíveis no mapa DITA é exibida.

1. Selecione os tópicos dos quais deseja remover as tags.

1. Clique em **Remover Tags**.

   >[!NOTE]
   >
   > Se o ícone Excluir tags não estiver visível, verifique se você não ativou o recurso Ocultar tags .

1. Na caixa de diálogo Confirmar exclusão, clique em **OK** para remover as tags dos tópicos selecionados.


## Mostrar ou ocultar tags

Se você tiver uma lista longa de tags aplicadas aos seus tópicos, talvez seja um pouco complicado navegar. Você pode ocultar facilmente as tags no na visualização do console do mapa DITA clicando no ícone Ocultar tags . Da mesma forma, quando as tags não estão visíveis, clicar em Mostrar tags revela todas as tags.

**Tópico principal:**[ Gerenciar metadados](manage-metadata.md)

