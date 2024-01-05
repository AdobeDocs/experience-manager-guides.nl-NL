---
title: Widgets
description: Widgets begrijpen
source-git-commit: f9a72e44fe1a3d90180ff728189a24ea9c7b1b1a
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# Widgets

Meerdere basiscomponenten, zoals besproken in de sectie Componenten, kunnen worden gecombineerd om een widget te maken.
Widgets kan worden gebruikt om een nieuwe &quot;complexere&quot;component te maken, of structuur aan punten van een component te geven.

Laten we in het concept van een widget duiken!

We beginnen met het maken van een eenvoudige widget om een lijst met talen weer te geven.

```js title="basicWidget.js"
const widgetJSON =  {
    "component": "div", 
    "id": "widget_languages", 
    "items": [ // adding components to the widget
        {
            "component": "div",
            "items": [
                {
                    "component": "icon",
                    "icon": "info"
                },
                {
                    "component": "label",
                    "label": "List of some languages"
                }
            ]
        },
        {
            "component": "list",
            "data": "@languages"
        }
    ]
},
```

Hier, `@languages` is een array gedefinieerd in het model van `widget_languages` als: [&quot;English&quot;, &quot;French&quot;, &quot;Hindi&quot;, &quot;Spanish&quot;, &quot;Urdu&quot;]

De gerenderde basiswidget ziet er als volgt uit:

![basic_widget](imgs/basic_widget.png "Standaardwidget")
