---
sidebar_position: 1
source-git-commit: 42052b37724f97e34ab007db4cc3d9f9524ad3a2
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 1%

---


# Botão

Para exibir um botão, usamos o componente, botão.
O componente de botão na JUI representa um html `<button/>`.

```js title="buttonJSON.js"
const buttonJSON = {
  "component": "button",//tells the component name
  "label": "Yes, login",//tells the text for the button
  "variant": "cta",//tells the variants for the button which  provides default styles
  "on-click": "done",//tells what function to run after user clicks the button
};
```

Isso produzirá um botão com um rótulo de `Yes, login`. As outras propriedades incluem, entre outras, variante, rótulo, clique.
> **_NOTA:_**  A variável `on-<events>` é a sintaxe para invocar os comandos nas controladoras.

O botão renderizado terá esta aparência:

![botão](imgs/yes_login_button.png "Botão")
