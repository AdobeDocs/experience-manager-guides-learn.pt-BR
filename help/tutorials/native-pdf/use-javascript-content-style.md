---
title: Recurso de publicação de PDF nativo | Usar JavaScript para trabalhar com conteúdo ou estilo
description: Saiba como criar folhas de estilos de uso e criar estilos para o seu conteúdo.
exl-id: 2f301f6a-0d1c-4194-84c2-0fddaef8d3ec
source-git-commit: e2349fc14143e5e49f8672ef1bfa48984df3b1c7
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Usar JavaScript para trabalhar com conteúdo ou estilo

O recurso Publicação de PDF nativo permite executar o JavaScript para manipular o conteúdo ou estilo aplicado no conteúdo antes que o PDF final seja gerado. Esse recurso oferece controle total sobre como a saída final é gerada. Por exemplo, você pode adicionar informações de avisos legais à saída PDF, que reside em outro PDF. Usando o JavaScript, você pode adicionar as informações de aviso legal depois que o PDF for criado para o conteúdo base, mas antes que o PDF final seja gerado.\
Para oferecer suporte à execução do JavaScript, o recurso Publicação de PDF nativo fornece as seguintes funções de retorno de chamada:

* `window.pdfLayout.onBeforeCreateTOC(callback)`: Essa função de retorno de chamada é executada antes que o índice seja gerado.
* `window.pdfLayout.onBeforePagination(callback)`: essa função de retorno de chamada é executada após a geração do índice, mas antes de as quebras de página serem adicionadas no PDF.
* `window.pdfLayout.onAfterPagination(callback)`: Essa função de retorno de chamada é executada após o índice e as quebras de página serem adicionadas no PDF.

>[!NOTE]
>
>Internamente, uma sequência de execução é mantida para essas funções de chamada. Primeiro, onBeforeCreateTOC é executado, seguido por onBeforePagination e, por fim, onAfterPagination é executado.

Com base no tipo de conteúdo ou na modificação de estilo que deseja executar, você pode escolher qual função de retorno de chamada usar. Por exemplo, se você deseja adicionar conteúdo, é recomendável fazer isso antes que o índice seja gerado. Da mesma forma, se você quiser fazer algumas atualizações de estilo, elas poderão ser feitas antes ou depois da paginação.

No exemplo a seguir, a posição dos títulos das figuras é alterada de para acima das imagens para abaixo das imagens. Para isso, é necessário ativar a opção de execução JavaScript na predefinição. Para fazer isso, execute as seguintes etapas:

1. Abra a predefinição para edição.
1. Vá para a **Avançado** guia.
1. Selecione o **Ativar JavaScript** opção.
1. Salve a predefinição e feche.

Em seguida, crie um arquivo JavaScript com o seguinte código e salve-o na pasta Resources do seu modelo:

```css
...
/*
* DITA only allows the figure title to be placed above images 
* This JavaScript code is used to move the figure title below the image
* */
window.addEventListener('DOMContentLoaded', function () {
    window.pdfLayout.onBeforeCreateTOC(function() {
        var titleNodes = document.querySelectorAll('.fig > .title')
        for (var i = 0; i < titleNodes.length; i++) {
            var titleNode = titleNodes[i]
            var figNode = titleNode.parentNode
            var imageNode = figNode.querySelector('.image')
            if(imageNode && imageNode.parentNode !== figNode) {
              imageNode = imageNode.parentNode
            }
            if (figNode && imageNode && imageNode.parentNode === figNode) {
                figNode.insertBefore(imageNode, titleNode)
            }
        }
    })
});
...
```

>[!NOTE]
>
>A variável `window.addEventListener('DOMContentLoaded', function ()` deve ser chamada antes que as funções de retorno de chamada sejam usadas.

Em seguida, esse script deve ser chamado de um arquivo de modelo usado para gerar a saída de PDF. Para nosso exemplo, vamos adicioná-lo no modelo de índice. Certifique-se de que o `<script>` tag é adicionada em um intervalo de tempo `<div>` dentro da tag `<body>` tag. Se você adicioná-lo na variável `<head>` ou fora da `<body>` , o script não será executado.

<img src="./assets/js-added-resources-template.png" width="500">

A saída gerada usando esse código e o modelo exibem o título da figura abaixo da imagem:

<img src="./assets/fig-title-below-image.png" width="500">
