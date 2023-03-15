---
title: Recurso de publicação do PDF nativo | Usar estilos personalizados em notas de rodapé
description: Saiba como aplicar estilo nos números das notas de rodapé.
source-git-commit: ef562c43f5b70d3fe425427108ad8277e1456f24
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# Usar estilos personalizados em notas de rodapé

As notas de rodapé são notas colocadas na parte inferior de uma página que comenta ou cita uma referência para uma parte designada do texto.

É possível criar um estilo para os números na chamada de nota de rodapé presente no conteúdo do tópico e o marcador de nota de rodapé presente na parte inferior da página. Por exemplo, você pode adicionar colchetes ao redor do número ou alterar sua cor. Esses estilos ajudam você a identificar facilmente as notas de rodapé no documento.

```css
...
.footnote::footnote-call { 
content: "(" counter(footnote, decimal) ")"; 
} 

.footnote::footnote-marker { 
content: "(" counter(footnote, decimal) ")"; 
} 

...
```

No exemplo fornecido, um colchete é adicionado antes e depois da chamada e do marcador da nota de rodapé:

* Adicione o prefixo &quot;(&quot; e o sufixo &quot;)&quot; usando o atributo de conteúdo no `footnote-call` estilo que adicionará os colchetes ao redor do número da nota de rodapé no conteúdo do tópico.
* Adicione o prefixo &quot;(&quot; e o sufixo &quot;)&quot; usando o atributo de conteúdo no `footnote-marker` estilo que adicionará os colchetes ao redor do número da nota de rodapé na parte inferior da página.

<img src="./assets/pdf-output-footer-numbers.png" alt="Rodapé na saída do PDF" width="500">
