---
title: Publicação com condições
description: Publicação com condições com o Adobe Experience Manager Guides
exl-id: ea94824a-884b-447f-9562-e6c629b8133b
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 1%

---

# Publicação com condições

A publicação condicional permite que uma fonte de conteúdo seja gravada para um ou mais públicos, produtos ou plataformas. Essas informações podem então ser publicadas dinamicamente e apenas o conteúdo especificamente necessário pode ser incluído na saída.

>[!VIDEO](https://video.tv.adobe.com/v/339041?quality=12&learn=on)

## Preparação para o exercício

Você pode baixar arquivos de amostra para o exercício aqui.

[Download de exercício](assets/exercises/publishing-with-conditions.zip)

## Marcar conteúdo com atributos condicionais

1. Abra o tópico a ser modificado.

1. Insira o texto a ser tornado condicional. Por exemplo, um ou mais parágrafos, uma tabela inteira, uma figura ou outro conteúdo.

   ![Informações de apresentação](images/presenting-info.png)

1. Selecione o conteúdo específico ao qual atribuir um atributo condicional. Por exemplo, um único parágrafo dentro da origem.

   ![Template-Choice](images/template-choice.png)

1. No painel direito, verifique se as Propriedades são exibidas.

1. Adicione um atributo para público, produto ou plataforma.

1. Atribua um valor ao atributo. As atualizações de exibição de conteúdo para mostrar marcação condicional foram aplicadas.

   ![Especificar-modelo](images/specify-template.png)

## Visualização de conteúdo condicional

1. Clique em **Visualizar**.

1. Em **Filtros**, selecione ou desmarque as condições a serem exibidas ou ocultadas.

1. Marcar ou desmarcar **Realçar texto de condições**.

   ![Pré-visualização-conteúdo-condicional](images/preview-conditional-content.png)

## Criação de uma predefinição de condição

Uma predefinição de condição é uma coleção de propriedades que definem o que deve ser incluído ou excluído, ou de outra forma marcado, durante a geração da saída.

1. No Painel do Mapa, selecione o **Predefinições de condição** guia.

1. Clique em **Criar**.

1. Selecionar **Adicionar** (ou **Adicionar tudo**).

1. Nomeie a condição.

1. Selecione um atributo, rótulo e combinação de ação.

   ![Criar-Condição-Predefinição](images/create-condition-preset.png)

1. Repita conforme necessário.

1. Clique em **Salvar**.

## Gerando saída condicional

Depois que as condições forem aplicadas ao conteúdo, ele poderá ser gerado como saída. Isso pode usar uma Predefinição de condição ou um arquivo DITAval.

## Geração de saída condicional usando uma predefinição de condição

1. Selecione o **Predefinições de saída** guia.

1. Selecione uma predefinição de saída.

1. Clique em **Editar**.

1. Em **Aplicar condição usando** selecione uma Predefinição de condição.

   ![Generate-Conditional-Output](images/generate-conditional-output.png)

1. Clique em **Concluído**.

1. Gere a predefinição de saída e revise o conteúdo.

## Gerando saída condicional usando um arquivo DITAval

O arquivo DITAval pode ser usado para publicar conteúdo condicional. Isso requer que um arquivo seja criado ou carregado e depois referenciado na publicação.

1. Selecione o **Predefinições de saída** guia.

1. Selecione uma predefinição de saída.

1. Clique em **Editar**.

1. Em Aplicar condição usando, selecione um arquivo DITAval.

   ![Generate-Using-DITAval](images/generate-using-ditaval.png)

1. Clique em **Concluído**.

1. Gere a predefinição de saída e revise o conteúdo.
