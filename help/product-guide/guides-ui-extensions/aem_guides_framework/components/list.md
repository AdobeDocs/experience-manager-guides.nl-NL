---
title: Lijst
description: Lijst
role: User, Admin
exl-id: 333b5e24-efba-4a51-8f68-83b5d1d7daec
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 0%

---

# Lijst

Om een lijst te tonen, gebruiken wij de componentenlijst.

```js title="list.js"
const listJSON =  {
    "component": "list", //tells the component name
    "data": "@languages", // an array of list items
},
```

Hier is taal een eenvoudige array van tekenreeksen. `languages = ["English", "Hindi", "French"]`
Voor het geval dat wij een lijst van voorwerpen willen teruggeven, kunnen wij de structuur specificeren gebruikend punt config.

```js title="list.js"
const listJSON =  {
    "component": "list", //tells the component name
    "data": "@projects", // an array of list items
    "itemConfig": { // used to define the structure of the list items.
    "component": "widget",
    "id": "checkbox_label"
    }
},
```

ItemConfig is gewoonlijk een `widget` . Meer over widgets leren ga naar [ Widgets ](../Widgets/basic-widget.md)

De gerenderde lijst ziet er als volgt uit:

![ lijst ](./imgs/list.png " Lijst ")
