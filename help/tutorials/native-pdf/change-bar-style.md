---
title: Recurso de publicação do PDF nativo | Trabalhar com estilos de barras de alteração personalizadas
description: Saiba como aplicar estilos em barras de alteração.
source-git-commit: b6fd82fd09c04a3deefab51b1064a3b6aea73e47
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Trabalhar com estilos de barras de alteração personalizadas

Uma barra de alteração é uma linha vertical que identifica visualmente o conteúdo novo ou revisado. AEM Guias permite mostrar uma barra de alterações à esquerda do conteúdo alterado dentro dos tópicos e também os tópicos alterados no TOC da saída do PDF.

Para obter mais detalhes sobre como mostrar a barra de alteração, consulte *Criar PDF com Barra de Alteração entre Versões Publicadas* definição em [Publicar saída do PDF](../web-editor/native-pdf-web-editor.md).

## Conteúdo alterado dentro dos tópicos

A barra de alterações é exibida à esquerda do conteúdo nos tópicos que foram inseridos, alterados ou excluídos.

Você pode modificar os estilos a seguir para mostrar o conteúdo alterado e entre eles com as barras de alteração.


>[!NOTE]
>
>Esses estilos fazem parte do `layout.css` e você pode editá-las conforme necessário.

Por exemplo, você pode usar o atributo de cor na variável `.inserted-block` estilo para definir a forma como o conteúdo inserido é exibido na saída do PDF publicada.


```css
...
.inserted-block { 
  color: #2ECC40; 
  display: inline; 
  -ro-comment-content: " "; 
  -ro-comment-style: underline; 
  -ro-comment-title: "Inserted"; 
  -ro-comment-date: attr(data-time); 
  -ro-comment-dateformat: "yyyy/dd/MM HH:mm:ss"; 
} 
...
```

Da mesma forma, é possível usar a variável `.deleted-block` estilo para definir a forma como o conteúdo excluído aparece na saída do PDF publicada.

```css
...
.deleted-block { 
  display: inline; 
  color: #FF6961; 
  text-decoration: line-through; 
  -ro-comment-content: " "; 
  -ro-comment-style: strikeout; 
  -ro-comment-title: "Deleted"; 
  -ro-comment-date: attr(data-time); 
  -ro-comment-dateformat: "yyyy/dd/MM HH:mm:ss"; 
} 
...
```

Você pode usar `.inserted-change-bar` e `.deleted-change-bar` estilo para modificar a aparência das barras de alteração exibidas à esquerda do conteúdo atualizado.

Por exemplo, você pode usar `-ro-change-bar-color` atributo em `.inserted-change-bar` estilo para mostrar a barra de alteração inserida em cor verde. Você também pode usar `-ro-change-bar-color` atributo em `.deleted-change-bar` estilo para mostrar a barra de alteração excluída em cor vermelha.

```css
...
.inserted-change-bar { 
  -ro-change-bar-color: #2ECC40; 
} 

.deleted-change-bar { 
  -ro-change-bar-color: #FF6961; 
  } 
...
```

<img src="./assets/changed-bar-content.png" alt="Conteúdo do tópico da barra alterado" width="500">

## Tópico alterado no Índice (TOC)

Você também pode adicionar uma barra de alteração à esquerda dos tópicos alterados no TOC da saída do PDF. Você pode usar `-ro-change-bar-color` no `.changed-topic` estilo para adicionar uma barra de alteração na cor de sua escolha para os tópicos atualizados na lista de sumário.

Por exemplo, é possível adicionar uma barra de alteração de cor verde.

```css
...
.changed-topic { 
 -ro-change-bar-color: #2ECC40; 
}  
...
```


Isso mostra uma barra de alteração verde em relação a todos os tópicos no sumário, onde algumas atualizações foram feitas. Você pode clicar no tópico alterado no sumário e exibir as alterações detalhadas.

<img src="./assets/changed-bar-TOC.png" alt="Índice da barra alterado" width="500">
