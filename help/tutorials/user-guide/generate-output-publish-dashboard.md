---
title: Gerenciar tarefas de publicação usando o painel Publicar
description: Saiba como Gerenciar tarefas de publicação usando o Painel de publicação
source-git-commit: 8b6294425c6e60d1c5b37d98e99114014a104ee6
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---


# Gerenciar tarefas de publicação usando o painel Publicar {#id205CC08305Z}

Quando você tem um grande conjunto de tarefas de publicação em execução no sistema, torna-se praticamente impossível verificar cada mapa DITA individualmente para monitorar sua tarefa de publicação. AEM Guias fornece aos administradores e editores uma visualização unificada de todas as tarefas de publicação em execução no sistema. Uma lista de todas as tarefas de publicação ativas está disponível no Painel de publicação.

O painel Publicar fornece uma visão geral completa de todas as tarefas de publicação em execução no sistema.

![](images/publish-dashboard.png)

O Painel de publicação contém os seguintes detalhes:

- **Título do mapa** - O título de um arquivo de mapa que está sendo publicado ou que está na fila de publicação.

- **Nome do arquivo** - O nome do arquivo do mapa DITA.

- **Predefinição de saída** - Nome da predefinição de saída usada para gerar a saída.

- **Iniciado por** - Nome de usuário do usuário que iniciou a tarefa de publicação.

- **Iniciado em** - Data e hora em que a tarefa de publicação foi iniciada.

- **Tempo Decorrido** - Tempo desde a execução da tarefa de publicação no sistema.

- **Ícone Excluir** - Cancelar ou encerrar uma tarefa de publicação.

O painel esquerdo no Painel de publicação fornece as seguintes opções de filtragem:

- **Predefinição de saída** - Selecione uma ou mais predefinições de saída para as quais deseja ver as tarefas de publicação ativas no momento. Na captura de tela a seguir, as tarefas de publicação são filtradas para mostrar apenas as tarefas que usam a predefinição de saída do Site de AEM:

![](images/publish-dashboard-preset-filter.png)

- **Iniciado por** - Selecione um nome de usuário na lista para mostrar as tarefas de publicação iniciadas pelo usuário selecionado.

- **Mapa** - Selecione um arquivo de mapa na lista para mostrar as tarefas de publicação em execução para o mapa selecionado.

## Acessar o painel de publicação {#id205CC100DY4}

Execute as seguintes etapas para acessar o Painel de publicação:

>[!NOTE]
>
> Somente um Administrador ou Editor pode acessar o Painel de publicação.

1. Clique no link do Adobe Experience Manager na parte superior e escolha **Ferramentas**.

1. Selecionar **Guias** na lista de ferramentas.

1. Clique no botão **Publicar painel** mosaico.

   O painel Publicar é aberto com uma lista de todas as tarefas de publicação ativas no sistema.

   Se você clicar no link Nome do arquivo , o console do mapa DITA do mapa selecionado será exibido.

   ![](images/publish-dashboard-click-filename-link.png)


>[!NOTE]
>
> Também é possível acessar o Painel de publicação na guia Saídas ao gerar a saída do painel de mapa. Para obter mais detalhes, consulte [Exibir o status da tarefa de geração de saída](generate-output-for-a-dita-map.md#viewing_output_history).

## Cancelar uma tarefa de publicação

Execute as etapas a seguir para cancelar uma tarefa de geração de saída no Painel de publicação:

1. [Acessar o painel de publicação](#id205CC100DY4).

1. Na lista de tarefas de publicação ativas, clique no ícone excluir de uma tarefa que deseja cancelar.

   ![](images/publish-dashboard-cancel-task.png)

1. Clique em **Sim** no prompt Confirmar mensagem de cancelamento.

   O comando cancel é aceito e o cancelamento é tentado enquanto a tarefa permanecer ativa. Depois que a tarefa for concluída com êxito, ela será removida da lista de tarefas ativas no momento. O status da tarefa também é atualizado no console do mapa DITA como Cancelado. Na captura de tela a seguir, a variável *HTML5* tarefa é cancelada no painel Publicar e seu status também é alterado no console do mapa DITA.

   ![](images/cancelled-output-task.png)


**Tópico principal:**[ Geração de saída](generate-output.md)

