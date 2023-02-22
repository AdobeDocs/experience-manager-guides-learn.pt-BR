---
title: Recurso de publicação do PDF nativo | Usar o JavaScript para trabalhar com conteúdo ou estilo
description: Saiba como criar folhas de estilos e criar estilos para o seu conteúdo.
source-git-commit: 09918abbdade934468dea1c55d0ca2cd60622b35
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---


# Use o JavaScript para trabalhar com conteúdo ou estilo

O recurso Publicação PDF nativa permite que você execute o JavaScript para manipular seu conteúdo ou estilo aplicado no conteúdo antes que a PDF final seja gerada. Esse recurso oferece controle total sobre como sua saída final é gerada. Por exemplo, você pode querer adicionar informações de aviso legal à saída do PDF, que reside em outro PDF. Usando o JavaScript, você pode adicionar as informações de aviso legal uma vez que o PDF é criado para o conteúdo básico, mas antes que o PDF final seja gerado.\
Para oferecer suporte à execução do JavaScript, o recurso Publicação nativa do PDF oferece as seguintes funções de retorno de chamada:

* `window.pdfLayout.onBeforeCreateTOC(callback)`: Essa função de retorno de chamada é executada antes da geração do TOC.
* `window.pdfLayout.onBeforePagination(callback)`: Essa função de retorno de chamada é executada após a geração do TOC, mas antes da adição de quebras de página no PDF.
* `window.pdfLayout.onAfterPagination(callback)`: Essa função de retorno de chamada é executada após o TOC e as quebras de página são adicionadas no PDF.

>[!NOTE]
>
>Internamente, uma sequência de execução é mantida para essas funções de chamada. Primeiro, onBeforeCreateTOC é executado, seguido por onBeforePagination e, por fim, o onAfterPagination é executado.

Com base no tipo de conteúdo ou modificação de estilo que deseja executar, você pode escolher qual função de retorno de chamada usar. Por exemplo, se você quiser adicionar conteúdo, é recomendável fazer isso antes que o TOC seja gerado. Da mesma forma, se você quiser fazer algumas atualizações de estilo, elas poderão ser feitas antes ou depois da paginação.

No exemplo a seguir, a posição dos títulos da figura é alterada de para acima das imagens para abaixo das imagens. Para isso, é necessário ativar a opção JavaScript execution na predefinição. Para fazer isso, execute as seguintes etapas:

1. Abra a predefinição para edição.
1. Vá para o **Avançado** guia .
1. Selecione o **Habilitar JavaScript** opção.
1. Salve a predefinição e feche.

Em seguida, crie um arquivo JavaScript com o seguinte código e salve-o na pasta Resources do seu template:

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
>O `window.addEventListener('DOMContentLoaded', function ()` deve ser chamada antes de as funções de retorno de chamada serem usadas.

Em seguida, esse script deve ser chamado de um arquivo de modelo usado para gerar a saída do PDF. Para nosso exemplo, adicionaremos no template TOC . Certifique-se de que `<script>` é adicionada dentro de um `<div>` dentro da `<body>` . Se você adicioná-lo à função `<head>` ou fora da `<body>` , o script não será executado.

<img src="./assets/js-added-resources-template.png" width="500">

A saída gerada por esse código e o modelo exibe o título da figura abaixo da imagem:

<img src="./assets/fig-title-below-image.png" width="500">
