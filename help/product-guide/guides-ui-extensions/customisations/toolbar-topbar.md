---
title: Onderbalk en werkbalk
description: De bovenste balk en werkbalk aanpassen
role: User, Admin
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---


# De bovenste balk en werkbalk aanpassen

Als u het dialoogvenster `topbar` en `toolbar`, gebruiken we de id&#39;s: `topbar` of `toolbar`en volgt dezelfde weergave, de controlestructuur.

Hieronder ziet u een triviaal voorbeeld van het aanpassen van de werkbalk. Hier hebben we de `Insert Numbered List` en vervangt de `Insert Paragraph` knoop met onze eigen component die een aangepaste on-click manager gebruiken.

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
