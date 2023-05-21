---
title: Exibir o status da tarefa de geração de saída
description: Saiba como Visualizar o status da tarefa de geração de saída
exl-id: 6fdaa547-8446-4ce5-95c3-a63d9c1f27d2
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Exibir o status da tarefa de geração de saída {#viewing_output_history}

Depois de iniciar a tarefa de geração de saída para um documento FrameMaker, os Guias AEM enviam essa tarefa para a fila de geração de saída. Essa fila é atualizada em tempo real, mostrando o status de cada tarefa de geração de saída na fila.

Execute as seguintes etapas para exibir a fila de geração de saída:

1. Na interface do usuário do Assets, navegue e clique no documento FrameMaker para o qual você deseja verificar o status de geração de saída.

1. Clique em Saídas.

   ![](images/output-queued-fm.png){width="800" align="left"}

1. A página Saídas é dividida em duas partes:

   - **Saídas em fila:**

      Lista as saídas que estão aguardando para serem geradas ou que estão em processo de geração. Você também pode encontrar a configuração de geração de saída ou a predefinição usada para a tarefa na fila, o tipo, o usuário que iniciou a tarefa, o tempo desde quando a tarefa está na fila e o status atual.

   - **Saídas geradas**

      Lista as tarefas de saída concluídas. Novamente, as informações mostradas aqui são semelhantes à seção Saídas em fila, com a única diferença do tempo de geração de saída.

      Nesta lista, você pode ter tarefas que foram executadas com sucesso ou tarefas que falharam. Para as tarefas concluídas com sucesso, o processo de publicação cria um arquivo de log \(logs.txt\) que pode ser acessado clicando no link da coluna Gerado em.


**Tópico pai:**[ Gerar saída de documentos do FrameMaker](fm-output-generatation.md)
