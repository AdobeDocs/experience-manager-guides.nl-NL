---
title: Lijst
description: Lijst
role: User, Admin
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
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

ItemConfig is gewoonlijk een `widget`. Ga voor meer informatie over widgets naar [Widgets](../Widgets/basic-widget.md)

De gerenderde lijst ziet er als volgt uit:

![list](./imgs/list.png "Lijst")
