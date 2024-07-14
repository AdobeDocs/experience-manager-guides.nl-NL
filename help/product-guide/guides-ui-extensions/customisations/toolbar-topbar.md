---
title: Onderbalk en werkbalk
description: De bovenste balk en werkbalk aanpassen
role: User, Admin
exl-id: 7065c9b8-67ac-4f6d-8124-daa547f2dc3b
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---

# De bovenste balk en werkbalk aanpassen

Als u `topbar` en `toolbar` wilt aanpassen, gebruiken we de id&#39;s: `topbar` of `toolbar` en volgen we dezelfde weergave, controlestructuur.

Hieronder ziet u een triviaal voorbeeld van het aanpassen van de werkbalk. Hier hebben we de knop `Insert Numbered List` verwijderd en de knop `Insert Paragraph` vervangen door onze eigen component met behulp van een aangepaste on-click handler.

```js title = toolbar_customisation.js
const toolbarExtend = {
    id: "toolbar",
    view: {
        items: [
            {
                component: "div",
                target: {
                    key:"title",value: "Insert Numbered List",                    
                    viewState: VIEW_STATE.REPLACE
                }
            },
            {
                {
                    "component": "button",
                    "icon": "textParagraph",
                    "variant": "action",
                    "quiet": true,
                    "title": "Insert Paragraph",
                    "on-click": "INSERT_P"
                },

                target: {
                    key:"title",value: "Insert Paragraph",                    
                    viewState: VIEW_STATE.REPLACE
                }
            },
        ]
    },
    controller: {

        INSERT_P(){
            this.next("AUTHOR_INSERT_ELEMENT",  "p" )
        }
    }
}
```
