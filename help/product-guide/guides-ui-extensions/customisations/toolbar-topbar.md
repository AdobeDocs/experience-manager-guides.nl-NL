---
title: Onderbalk en werkbalk
description: De bovenste balk en werkbalk aanpassen
role: User, Admin
exl-id: 7065c9b8-67ac-4f6d-8124-daa547f2dc3b
source-git-commit: 4f41609368b64415993b93be27162b069e7b2e32
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# De bovenste balk en werkbalk aanpassen

Als u `topbar` en `toolbar` wilt aanpassen, gebruiken we de id&#39;s: `topbar` of `toolbar` en volgen we dezelfde weergave, controlestructuur.

Hieronder ziet u een triviaal voorbeeld van het aanpassen van de werkbalk. Hier hebben we de knop `Insert Numbered List` verwijderd en de knop `Insert Paragraph` vervangen door onze eigen component met behulp van een aangepaste on-click handler.

Voor toegang tot functies die onder `proxy` -object worden weergegeven, moeten we deze benaderen met `this.proxy.getValue` , waarmee u een waarde kunt ophalen.

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
        init: function() {
            console.log(this.proxy.getValue("canUndo"))
            this.proxy.subscribeAppEvent({
              key: "editor.preview_rendered",
              next: async function (e) {
                console.log(this.proxy.getValue("canUndo"))
              }.bind(this)
            })
        },
        INSERT_P(){
            this.next("AUTHOR_INSERT_ELEMENT",  "p" )
        }
    }
}
```
