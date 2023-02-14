---
title: Recurso de publicação do PDF nativo | Aplicar estilo personalizado em entradas de sumário e conteúdo de tópico
description: Saiba como criar folhas de estilos e criar estilos para o seu conteúdo.
source-git-commit: fbb81704ea8d9d2793b066fa159b405460fa1dcf
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---


# Adicionar um marcador personalizado na saída do PDF

Geralmente, o TOC em um mapa DITA é replicado como marcadores na saída final do PDF. Esse TOC é criado a partir dos títulos do tópico ou da seção no mapa DITA. Às vezes, você pode adicionar um marcador personalizado em um conteúdo específico na saída do PDF para facilitar a navegação. Isso pode ser feito adicionando um `outputclass` no elemento e aplicando o seguinte atributo a ele:

`bookmark-level: 3`

Aqui, o `bookmark-level` é um atributo e número `3` é o valor que indica o nível na hierarquia de marcadores em que o marcador é adicionado. No exemplo a seguir, o tópico de primeiro nível &quot;Contatos&quot; tem uma tabela, &quot;Lista de contatos&quot; na qual adicionamos um `outputclass` com o valor de `custom-bookmark`.

<img src="./assets/custom-bookmark-attribute.png" width="500">

A definição de `custom-bookmark` é adicionada no arquivo CSS:

```css
…
/*Adding a custom bookmark*/
.custom-bookmark{
    bookmark-level: 2
}
…
```

Na saída do PDF, a variável *Lista de contatos* é adicionada no segundo nível da lista de favoritos do PDF, conforme mostrado abaixo:

<img src="./assets/custom-bookmark-in-pdf-output.png" width="500">
