---
title: Widgets
description: Widgets begrijpen
role: User, Admin
exl-id: 96e960df-d595-4d58-8ad4-27057f857bac
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
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

Hier, is `@languages` een serie die in het model van `widget_languages` wordt bepaald als: [ &quot;Engels&quot;, &quot;Frans&quot;, &quot;Hindi&quot;, &quot;Spaans&quot;, &quot;Urdu&quot;]

De gerenderde basiswidget ziet er als volgt uit:

![ basic_widget ](imgs/basic_widget.png " Basis widget ")
