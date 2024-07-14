---
title: Label
description: Label
role: User, Admin
exl-id: aceefb08-3198-4c3a-90ec-ac1cdde28582
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# Label

Voor het weergeven van tekst of een tekenreeks gebruiken we de component, label.
De labelcomponent in JUI vertegenwoordigt een html `<label/>` .

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

![ etiket ](./imgs/label.png " Etiket ")
