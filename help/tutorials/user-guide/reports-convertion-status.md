---
title: Relatório de status de conversão
description: Saiba como converter relatório de status
exl-id: 41887af2-404f-41d7-b54c-ec49797200f0
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Relatório de status de conversão {#id205BBA00WZZ}

AEM Guias fornece um recurso de conversão robusto para converter documentos de vários formatos em DITA. O Relatório de status de conversão fornece uma exibição consolidada de todas as tarefas de conversão executadas pelos Guias AEM.

Execute as seguintes etapas para exibir o Relatório de status de conversão:

1. Clique no link do Adobe Experience Manager na parte superior e escolha **Ferramentas**.

1. Selecionar **Guias** na lista de ferramentas.

1. Clique no botão **Relatório de status de conversão** mosaico.

   O Relatório de status de conversão é exibido para todas as tarefas de conversão executadas no sistema.

   ![](images/conversion-status-report.png){width="800" align="left"}

1. A página do relatório é dividida em duas partes:

   - **Filtro:**

      Você pode filtrar os dados do relatório com base no Tipo de arquivo e Status de conversão. No Tipo de Arquivo, você pode optar por ver os dados do relatório para documentos do Word, HTML estruturado, XML e DocBook tipo de documentos. No Status, você pode optar por ver os dados do relatório para tarefas que foram executadas com êxito, com falha, ativas ou em fila.

      A captura de tela a seguir exibe os dados do relatório para tarefas de conversão que têm status Failed, Ative e Queued .

      ![](images/conversion-report-failed-active-queued.png){width="800" align="left"}

   - **Dados do relatório:**

      Os dados do relatório contêm as seguintes colunas:

      - **Nome do arquivo**: Nome do arquivo de origem no qual o processo de conversão foi executado. Clicar no link Nome do arquivo leva você ao local do documento de origem.

      - **Tipo de arquivo**: Tipo do documento de origem, que pode ser Word, HTML estruturado, XML e DocBook.

      - **Adicionado por**: Nome do usuário que executou a tarefa de conversão.

      - **Data de adição**: Data em que a tarefa foi executada. Clicar no link Data de adição baixa o arquivo de log.

      - **Caminho**: Caminho completo do documento de origem.

      - **Status**: Status das tarefas de conversão - Sucesso, Falha, Ativo ou Em Fila.

      - **Saída**: Caminho do documento convertido com êxito. Clicar no link Saída leva você ao local onde a saída é salva.


**Tópico principal:**[ Relatórios](reports-intro.md)
