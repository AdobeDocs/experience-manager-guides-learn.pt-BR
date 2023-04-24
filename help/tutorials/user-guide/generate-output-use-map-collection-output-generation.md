---
title: Usar Coleção de Mapa para geração de saída
description: Saiba como usar a coleção de mapas para geração de saída
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 0%

---


# Usar Coleção de Mapa para geração de saída {#id1723F20G0HS}

Em qualquer organização, um produto pode ter vários tipos de documentação. Como especialista em publicação, você gostaria de controlar qual saída deseja gerar para qual documento. Além disso, deve haver uma maneira de publicar vários documentos em lote com um único clique.

AEM Guias fornece a capacidade de organizar o conteúdo para publicação usando um painel chamado Coleção de mapa. Uma Coleção de mapa permite reunir todos os diferentes tipos de documentos em uma única unidade. Você pode escolher o tipo de saída que deseja gerar para cada documento na Coleção de mapa. Além disso, você também pode gerar saída e ver o progresso da geração de saída no painel de publicação.

A Coleção de mapa fornece uma opção para visualizar se há alguma alteração em qualquer mapa a partir da última saída publicada. Você pode exibir os detalhes na guia Mapas e predefinições da Coleção de mapa e, em seguida, republicar a saída, se necessário. Para obter mais informações, consulte Adicionar um mapa a uma coleção de mapa.

## Criar uma coleção de mapas e adicionar mapas DITA

Para criar uma Coleção de mapa e adicionar mapas DITA à coleção, execute as seguintes etapas:

1. Na interface do usuário do Assets, clique em **Mapear coleções**.

   Se o link Mapear coleções não estiver disponível, selecione o **Navegação** no painel à esquerda e clique em **Mapear coleções**.

   ![](images/access-map-collection-left-rail.png)

1. Insira um Título para sua coleção de mapas.
1. Clique em **Criar**.

   Uma mensagem de sucesso é exibida na criação da coleção de mapas.

1. Clique em **Fechar** na mensagem Success .

   O arquivo de mapa recém-criado é exibido na página Mapear coleções .

1. Clique na caixa cinza no bloco da coleção que você deseja editar.
1. Clique em **Editar** e, em seguida, clique em **Adicionar Mapas**.
1. Localize e adicione os mapas DITA que deseja adicionar à Coleção de mapa.

   Por padrão, todas as predefinições e localidades associadas ao mapa são adicionadas automaticamente.

1. Selecione a saída desejada ao ativar ou desativar o botão deslizante.
1. Clique em **Concluído**.

   Os arquivos de mapa DITA são adicionados à Coleção de mapa.


![](images/maps_presets_62_63.png)

As seguintes opções de filtragem e detalhes do mapa são mostrados na página de coleção:

- **Filtro:** O último painel mostra os seguintes filtros:
   - **Modificado**: Você pode selecionar Sim ou Não. Se você selecionar sim, somente os mapas DITA modificados serão mostrados na tabela Mapas e predefinições .
   - **Predefinição**: Selecione uma predefinição para a qual deseja filtrar os arquivos de mapa. Por exemplo, se você escolher *Site AEM* predefinição, então somente os mapas que têm a variável *Site AEM* predefinição de saída configurada neles.
   - **Idioma**: Você pode selecionar qualquer um dos códigos de idioma disponíveis e exibir somente o idioma selecionado na tabela Mapas e predefinições .
- **Mapas e predefinições** tabela: A tabela Mapas e predefinições apresenta informações nas seguintes colunas:
   - **Mapa**: Mostra o título do arquivo de mapa DITA.
   - **Idioma**: Mostra o idioma do mapa DITA.
   - **Predefinição**: Mostra o tipo de predefinição de saída configurado no arquivo de mapa.
   - **Modificado**: Indica se o mapa DITA foi atualizado após a última publicação. Com base nessas informações, você pode decidir se deseja republicar a saída desse mapa DITA ou não.
   - **Última Geração**: Mostra a data e a hora da última saída gerada.

## Configurar e gerar a saída usando uma Coleção de mapa

Para configurar e gerar a saída usando uma Coleção de mapa, execute as seguintes etapas:

1. Abra a Coleção de mapa.
1. \(Opcional\) Siga qualquer um dos procedimentos a seguir com base em seu requisito:
   - Aplique Filtros no painel esquerdo para filtrar os mapas modificados, a predefinição de saída ou o idioma.
   - Se necessário, clique em **Editar** e altere a saída desejada ao ativar ou desativar o botão deslizante.
1. Siga uma das seguintes opções:

   - Para gerar a saída dos mapas selecionados, selecione os arquivos de mapa e clique em **Gerar selecionados**.
   - Para gerar a saída de todos os mapas DITA com suas predefinições configuradas, clique em **Gerar tudo**.

   >[!IMPORTANT]
   >
   > Se um processo de geração de saída para uma predefinição ou mapa DITA estiver na fila ou em andamento, não será possível iniciar outra tarefa de geração de saída para a mesma predefinição ou mapa.


## Excluir uma coleção de mapas ou um mapa DITA da coleção de mapas

- Para excluir uma coleção de mapa, selecione uma coleção na página Mapear coleção e clique em **Excluir**.
- Para excluir um mapa DITA de uma coleção de mapas, abra a Coleção de mapas no modo Editar, selecione o arquivo de mapa DITA e clique em **Remover da coleção**.

   Isso também removerá predefinições ou localidades associadas ao mapa DITA da coleção de mapas.


## Cancelar uma tarefa de geração de saída de uma Coleção de Mapa

Semelhante à maneira de cancelar uma tarefa de geração de saída do [Console de mapa DITA](generate-output-for-a-dita-map.md#id2061H100T5Z) ou [Publicar painel](generate-output-publish-dashboard.md#), é possível cancelar uma tarefa de geração de saída de uma Coleção de Mapa. Acesse a guia Saídas de uma Coleção de mapa, vá para a tarefa de publicação que deseja cancelar e clique no botão **Cancelar esta Tarefa** ícone para cancelar a tarefa de publicação.

![](images/cancel-publish-task-map-collection.png)

**Tópico principal:**[ Geração de saída](generate-output.md)

