---
sidebar_position: 3
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---


# Tekstveld en tekstgebied

Om tekst als input te nemen, gebruiken wij de componenten, het tekstgebied en het tekstgebied.
De component van het tekstgebied in JUI vertegenwoordigt een HTML `<textarea/>`.

```js title="textArea.js"
const textAreaJSON =  {
    "component": "textarea", //tells the component name
    "id": "input_name", // can be used to give a unique identifier to a component
    "data": "@name", // the variable storing the inputted text
    "on-keyup": {
        "name": "submitName",
        "eventArgs": {
            "keys": [
            "ENTER"
            ]
        }
    },
},
```

Hier, `on-keyup` is de syntaxis voor het aanroepen van de opdrachten in de controllers.
Dit zal een textArea veroorzaken waar het drukken ENTER de gebeurtenis zal roepen `submitName`

Het gerenderde tekstgebied ziet er als volgt uit:

![tekstgebied](./imgs/text_area.png "Tekstgebied")
