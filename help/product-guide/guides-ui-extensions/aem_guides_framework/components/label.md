---
title: Label
description: Label
role: User, Admin
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# Label

Voor het weergeven van tekst of een tekenreeks gebruiken we de component, label.
De labelcomponent in JUI vertegenwoordigt een HTML `<label/>`.

Hieronder ziet u een voorbeeld voor het toevoegen van een statisch label

```js title="staticLabel.js"
const staticLabelJSON =  {
    "component": "label", //tells the component name
    "label": "This is an example label", // the string to be displayed
}
```

Onder JSON wordt een dynamische tekenreeks weergegeven:

```js title="dynamicLabel.js"
const labelJSON =  {
    "component": "label", //tells the component name
    "label": "@name", // the variable storing the text to be displayed
},
```

Het gerenderde label ziet er als volgt uit:

![label](./imgs/label.png "Label")