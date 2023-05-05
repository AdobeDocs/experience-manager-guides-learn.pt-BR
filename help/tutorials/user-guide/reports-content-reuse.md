---
title: Relatório de reutilização de conteúdo
description: Saiba como usar o Relatório de reutilização de conteúdo
exl-id: 658ae0fd-9032-4480-b9e4-fe4fec261e72
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Relatório de reutilização de conteúdo {#id205BB900OQD}

Outro relatório útil que você pode gerar é o Relatório de reutilização de conteúdo. Este relatório calcula a porcentagem média de uso de conteúdo, o que é muito útil para gerentes de projeto e proprietários de negócios para ver a quantidade de conteúdo que está sendo reutilizado.

>[!TIP]
>
> Para garantir o funcionamento correto do Relatório de reutilização de conteúdo, é necessário ativar o fluxo de trabalho de pós-processamento. Entre em contato com o administrador do sistema para ativar workflows de pós-processamento.

Execute as seguintes etapas para visualizar o Relatório de reutilização de conteúdo:

1. Clique no link do Adobe Experience Manager na parte superior e escolha **Ferramentas**.

1. Selecionar **Guias** na lista de ferramentas.

1. Clique no botão **Relatório de reutilização de conteúdo** mosaico.

1. Clique em **Procurar** para escolher um caminho onde seus tópicos residem ou inserir o caminho manualmente.

   O relatório é gerado pela varredura do conteúdo nas pastas pai e filho.

1. Clique em **Gerar relatório** para obter o Relatório de reutilização de conteúdo.

   ![](images/content-reuse-uuid.png){width="800" align="left"}

   A página do relatório é dividida em duas partes:

   - **Resumo do relatório:**

      Lista a Reutilização média de conteúdo, que é calculada como Instâncias de reutilização de conteúdo/Contagem total de tópicos. Este relatório considera todas as referências de conteúdo direto de primeiro nível e as referências de tópico para o cálculo. As Instâncias de reutilização de conteúdo são calculadas como o total da soma dos valores no campo Número de vezes reutilizados . O tópico mais reutilizado também é listado no Resumo do relatório. Clicar no link do tópico no Tópico mais reutilizado abre a visualização do tópico.

   - **Detalhes:**

      A seção Detalhes contém as seguintes colunas:

      - **Título**: O título do tópico. Clicar no link de título do tópico abre a visualização do tópico.

      - **UUID**: O identificador universal exclusivo \(UUID\) do arquivo.

      - **Tamanho**: Tamanho dos arquivos em bytes.

      - **Status**: O estado atual do documento - Rascunho, Em revisão ou Revisado.

      - **Número de vezes reutilizadas**: Número de vezes que o tópico correspondente foi reutilizado. Isso é calculado como a soma total das entradas em Referenciado por colunas menos 1.

      - **Referenciado por**: Os tópicos nos quais o tópico correspondente foi referenciado. Aqui, somente as referências diretas \(primeiro nível\) são consideradas. Vários tópicos são separados por vírgula. A UUID do arquivo referenciado também é mencionada entre parênteses. Clicar no link de título do tópico abre a visualização do tópico.


>[!NOTE]
>
> Também é possível exportar o Relatório de reutilização de conteúdo no formato CSV. Para fazer isso, clique no link Export to CSV no canto superior esquerdo da tela e escolha um local para salvar o arquivo CSV. Em seguida, você pode abrir esse arquivo CSV em qualquer editor CSV.

**Tópico principal:**[ Relatórios](reports-intro.md)
