---
title: Usar coleção de mapas para geração de saída
description: Saiba como usar a coleção de mapas para geração de saída
exl-id: 32e3af6c-9670-42cc-8dbe-9f99fbc60adf
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 0%

---

# Usar coleção de mapas para geração de saída {#id1723F20G0HS}

Em qualquer organização, um produto pode ter vários tipos de documentação. Como um especialista em publicação, você gostaria de controlar qual saída deseja gerar para qual documento. Além disso, deve haver uma maneira de publicar vários documentos em lote com um único clique.

Os Guias do AEM oferecem a capacidade de organizar o conteúdo para publicação usando um painel chamado Coleção de mapas. Uma Coleção de Mapas permite reunir todos os diferentes tipos de documentos em uma única unidade. Você pode escolher o tipo de saída que deseja gerar para cada documento na Coleção de mapas. Além disso, também é possível gerar saída e ver o progresso da geração de saída no painel de publicação.

A Coleção de mapas oferece uma opção para visualizar se há alguma alteração em qualquer mapa desde a última saída publicada. É possível exibir os detalhes na guia Mapas e predefinições da Coleção de mapas e, em seguida, republicar a saída, se necessário. Para obter mais informações, consulte Adição de um mapa a uma coleção de mapas.

## Criar uma coleção de mapas e adicionar mapas DITA

Para criar uma Coleção de mapas e adicionar mapas DITA à coleção, execute as seguintes etapas:

1. Na interface do usuário do Assets, clique em **Mapear coleções**.

   Se o link Mapear Coleções não estiver disponível, selecione o **Navegação** no painel esquerdo e, em seguida, clique em **Mapear coleções**.

   ![](images/access-map-collection-left-rail.png){width="350" align="left"}

1. Insira um Título para sua coleção de mapas.
1. Clique em **Criar**.

   Uma mensagem de Sucesso é exibida ao criar a coleção de mapas.

1. Clique em **Fechar** na mensagem Success (Êxito).

   O arquivo de mapa recém-criado é mostrado na página Coleções de mapas.

1. Clique na caixa cinza no bloco da coleção que deseja editar.
1. Clique em **Editar** e clique em **Adicionar mapas**.
1. Localize e adicione os mapas DITA que deseja adicionar à Coleção de mapas.

   Por padrão, todas as predefinições e localidades associadas ao mapa são adicionadas automaticamente.

1. Selecione a saída desejada ativando ou desativando o botão deslizante.
1. Clique em **Concluído**.

   Os arquivos de mapa DITA são adicionados à Coleção de mapas.

   ![](images/maps_presets_62_63.png){width="800" align="left"}

As seguintes opções de filtro e detalhes do mapa são mostrados na página de coleção:

- **Filtro:** O painel inferior mostra os seguintes filtros:
   - **Modificado**: Você pode selecionar Sim ou Não. Se você selecionar sim, somente os mapas DITA modificados serão exibidos na tabela Mapas e predefinições.
   - **Predefinição**: selecione uma predefinição para a qual deseja filtrar os arquivos de mapa. Por exemplo, se você escolher *Site AEM* predefinido, serão exibidos apenas os mapas que tiverem a *Site AEM* predefinição de saída configurada neles.
   - **Idioma**: é possível selecionar qualquer um dos códigos de idioma disponíveis e exibir apenas o idioma selecionado na tabela Mapas e predefinições.
- **Mapas e predefinições** tabela: A tabela Mapas e Predefinições apresenta informações nas seguintes colunas:
   - **Mapa**: mostra o título do arquivo de mapa DITA.
   - **Idioma**: mostra o idioma do mapa DITA.
   - **Predefinição**: mostra o tipo de predefinição de saída configurado no arquivo de mapa.
   - **Modificado**: indica se o mapa DITA foi atualizado após a última publicação. Com base nessas informações, você pode decidir se deseja republicar a saída desse mapa DITA ou não.
   - **Gerado por último**: mostra a data e a hora da última saída gerada.

## Configurar e gerar a saída usando uma coleção de mapas

Para configurar e gerar a saída usando uma Coleção de mapas, execute as seguintes etapas:

1. Abra a Coleção de mapas.
1. \(Opcional\) Siga qualquer um dos procedimentos a seguir com base em seus requisitos:
   - Aplique filtros no painel esquerdo para filtrar os mapas modificados, a predefinição de saída ou o idioma.
   - Se necessário, clique em **Editar** e altere a saída desejada ativando ou desativando o botão deslizante.
1. Siga uma das seguintes opções:

   - Para gerar a saída de mapas selecionados, selecione os arquivos de mapa e clique em **Gerar seleção**.
   - Para gerar a saída de todos os mapas DITA com suas predefinições configuradas, clique em **Gerar tudo**.

   >[!IMPORTANT]
   >
   > Se um processo de geração de saída para uma predefinição ou um mapa DITA estiver na fila ou em andamento, não será possível iniciar outra tarefa de geração de saída para a mesma predefinição ou mapa.


## Excluir uma coleção de mapas ou um mapa DITA da coleção de mapas

- Para excluir uma coleção de mapas, selecione uma coleção na página Coleção de Mapas e clique em **Excluir**.
- Para excluir um mapa DITA de uma coleção de mapas, abra a Coleção de mapas no modo Editar, selecione o arquivo de mapa DITA e clique em **Remover da coleção**.

   Isso também removerá quaisquer predefinições ou localidades associadas ao mapa DITA da Coleção de mapas.


## Cancelar uma tarefa de geração de saída de uma coleção de mapas

Semelhante à forma de cancelar uma tarefa de geração de saída do [Console de mapa DITA](generate-output-for-a-dita-map.md#id2061H100T5Z) ou o [Publicar painel](generate-output-publish-dashboard.md#), é possível cancelar uma tarefa de geração de saída a partir de uma coleção de mapas. Acesse a guia Saídas de uma Coleção de mapas, vá para a tarefa de publicação que deseja cancelar e clique no **Cancelar Este Trabalho** ícone para cancelar a tarefa de publicação.

![](images/cancel-publish-task-map-collection.png){width="800" align="left"}

**Tópico pai:**[ Geração de saída](generate-output.md)