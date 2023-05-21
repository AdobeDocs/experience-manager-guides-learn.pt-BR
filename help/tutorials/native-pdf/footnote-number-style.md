---
title: Recurso de publicação de PDF nativo | Usar estilos personalizados em notas de rodapé
description: Saiba como aplicar estilo aos números em notas de rodapé.
exl-id: f1068f2f-2ace-4bdb-b5a4-46b03d4e43d6
source-git-commit: 7b48633ef2418fa7c91842a8d2c2a4177017ef58
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# Usar estilos personalizados em notas de rodapé

As notas de rodapé são notas colocadas na parte inferior de uma página que comenta ou cita uma referência para uma parte designada do texto.

É possível estilizar os números na chamada de nota de rodapé presente no conteúdo do tópico e no marcador de nota de rodapé presente na parte inferior da página. Por exemplo, você pode adicionar colchetes ao redor do número ou alterar a cor. Esses estilos ajudam a identificar facilmente as notas de rodapé no documento.

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

No exemplo em questão, um colchete é adicionado antes e depois da chamada de nota de rodapé e do marcador:

* Adicione o prefixo &quot;(&quot; e o sufixo &quot;)&quot; usando o atributo content na variável `footnote-call` estilo que adicionará os colchetes ao redor do número da nota de rodapé no conteúdo do tópico.
* Adicione o prefixo &quot;(&quot; e o sufixo &quot;)&quot; usando o atributo content na variável `footnote-marker` estilo que adicionará os colchetes ao redor do número da nota de rodapé na parte inferior da página.

<img src="./assets/pdf-output-footer-numbers.png" alt="Rodapé na saída do PDF" width="500">
