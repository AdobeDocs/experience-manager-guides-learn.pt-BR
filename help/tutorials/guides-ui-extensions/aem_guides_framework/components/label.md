---
sidebar_position: 2
source-git-commit: 0f20681fa4de859053c8d2baae0e53f347ce5859
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 2%

---


# Etiqueta

Para exibir qualquer texto ou string, usamos o componente, rótulo.
O componente de rótulo na JUI representa um html `<label/>`.

Veja abaixo um exemplo de adição de rótulo estático

```js title="staticLabel.js"
const staticLabelJSON =  {
    "component": "label", //tells the component name
    "label": "This is an example label", // the string to be displayed
}
```

Abaixo do JSON é exibida uma string dinâmica:

```js title="dynamicLabel.js"
const labelJSON =  {
    "component": "label", //tells the component name
    "label": "@name", // the variable storing the text to be displayed
},
```

O rótulo renderizado terá esta aparência:

![rótulo](./imgs/label.png "Rótulo")