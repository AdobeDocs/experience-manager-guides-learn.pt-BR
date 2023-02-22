---
title: Recurso de publicação do PDF nativo | Aplicar estilo personalizado em entradas de sumário e conteúdo de tópico
description: Saiba como criar folhas de estilos e criar estilos para o seu conteúdo.
source-git-commit: 09918abbdade934468dea1c55d0ca2cd60622b35
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Aplicar estilo personalizado em entradas de sumário e conteúdo de tópico

Às vezes, você pode aplicar um estilo personalizado nas entradas do sumário ou em um tópico específico. Isso pode ser feito associando um `outputclass` com o `<topicref>` no mapa DITA. Além disso, caso você queira aplicar um formato personalizado a um tópico inteiro, isso também pode ser feito estendendo a definição de estilo do atributo no CSS.

Vamos ver um exemplo de um novo tópico que você deseja enviar para revisão. Para facilitar a identificação do tópico atualizado, é necessário adicionar um `outputclass` para a `<topicref>` no mapa DITA e, em seguida, defina um estilo personalizado para o mesmo no CSS.

No exemplo a seguir, a variável *História dos voos* foi atribuído um `outputclass` com o valor de `new-topic`.

<img src="./assets/new-topic-attribute-in-map.png" width="500">

A definição de classe do `new-topic` em um CSS pode permitir definir o estilo para os seguintes itens:
* A entrada principal no TOC ou miniTOC
* O título do tópico no conteúdo principal
* O conteúdo inteiro do tópico, incluindo o título

Vamos ver como cada um desses cenários pode ser definido no CSS. Na seguinte definição de CSS da variável `new-topic` , a cor do texto foi alterada.

```css
…
.new-topic {
  color: #CC5309
}
…
```

Esta definição controla a cor do texto no sumário e o título do tópico. A saída de PDF a seguir mostra a cor diferente aplicada na entrada TOC:

<img src="./assets/pdf-output-toc-entry.jpg" width="500">

O título do tópico também é estilizado usando a mesma cor.

<img src="./assets/pdf-output-topic-title.jpg" width="500">

Se quiser que a entrada do sumário e o título do tópico tenham estilos diferentes, é possível defini-los separadamente, conforme mostrado abaixo:

```css
...
/*for styling TOC entry */
.new-topic {
  color: #CC3509
}

/* for styling topic's title */
.new-topic.title {
  color: #092ACC
}
...
```

Por fim, também é possível aplicar estilos em todo o conteúdo do tópico. Para isso, é necessário adicionar um sufixo &quot;`-content`&quot; para o nome da classe. No exemplo a seguir, uma barra de alteração foi adicionada em todo o conteúdo do tópico:

```css
...
/* for styling the topic's content */
.new-topic-content {
  -ro-change-bar-color: #A609CC;
}
...
```

Usando os atributos de estilo acima, uma barra de alteração é adicionada à esquerda da variável *História do voo* tópico, conforme mostrado abaixo:

<img src="./assets/pdf-output-topic-content.jpg" width="500">


