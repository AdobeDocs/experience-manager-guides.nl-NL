---
sidebar_position: 2
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '44'
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