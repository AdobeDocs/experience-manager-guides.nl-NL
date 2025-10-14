---
title: Tekstgebied
description: Tekstgebied
role: User, Admin
exl-id: 4c576acc-fa6a-4c41-9b92-443ba51dc8ee
source-git-commit: 08d379acc98dac425f1c84b0ac2226b0e34f6d8b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Tekstveld en tekstgebied

Om tekst als input te nemen, gebruiken wij de componenten, het tekstgebied en het tekstgebied.
De component van het tekstgebied in JUI vertegenwoordigt HTML `<textarea/>`.

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

Hier, `on-keyup` is de syntaxis voor het aanhalen van de bevelen in de controlemechanismen.
Hierdoor wordt een textArea gemaakt waarin de gebeurtenis wordt aangeroepen wanneer op ENTER wordt gedrukt `submitName`

Het gerenderde tekstgebied ziet er als volgt uit:

![&#x200B; tekst-gebied &#x200B;](./imgs/text_area.png " Gebied van de Tekst ")
