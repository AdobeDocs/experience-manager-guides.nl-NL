---
title: Widgets renderen
description: Hoe rendering werkt in JUI-widgets
source-git-commit: f9a72e44fe1a3d90180ff728189a24ea9c7b1b1a
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# Widgets renderen

We kunnen een widget renderen door ernaar te verwijzen met behulp van zijn `id`

De widget renderen `widget_languages` overal in de app kunnen we de eenvoudige syntaxis gebruiken:

```json
{
    "component": "widget",
    "id": "widget_languages"
}
```

Widgets kan ook worden gebruikt om complexe punten terug te geven, zeg ik de lijst van contribuanten aan elk dossier terug te geven.
Hier kan de widget worden geconstrueerd als:

```js title="fileContributorsWidget.js"
const widgetJSON =  {
    component: "div", 
    id: "file_contributors", 
    items: [ // adding components to the widget
        {
            component: "div",
            items: [
                {
                    component: "icon",
                    icon: "file"
                },
                {
                    component: "label",
                    label: "@fileName"
                }
            ]
        },
        {
            component: "list",
            data: "@contributors",
            itemConfig: {
                component: "label"
            }
        }
    ]
},
```

Nu schrijven wij de lijst als volgt om een lijst met contribuanten voor elk bestand weer te geven:

```js title="fileContributorsList.js"
const listJSON = {
    component: "list"
    data: "@files"
    itemConfig: {
        component: "widget",
        id: "file_contributors"
    }
}
```

hier `@files` is een lijst met bestandsobjecten die velden bevatten

```typescript
- fileName: string
- contributors: Array<String>
```
