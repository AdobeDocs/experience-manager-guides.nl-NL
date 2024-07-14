---
title: Knop
description: Knop
role: User, Admin
exl-id: 40e3f254-f94e-4f43-8ff5-2e6e1eb1cb6f
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# Knop

Om een knoop te tonen gebruiken wij de component, knoop.
De knopcomponent in JUI vertegenwoordigt een HTML `<button/>` .

```js title="buttonJSON.js"
const buttonJSON = {
  "component": "button",//tells the component name
  "label": "Yes, login",//tells the text for the button
  "variant": "cta",//tells the variants for the button which  provides default styles
  "on-click": "done",//tells what function to run after user clicks the button
};
```

Hierdoor wordt een knop met het label `Yes, login` gemaakt. De andere eigenschappen omvatten maar zijn niet beperkt tot variant,label,klikken.
> **_NOTA:_** `on-<events>` is de syntaxis voor het aanhalen van de bevelen in de controlemechanismen.

De weergegeven knop ziet er als volgt uit:

![ knoop ](imgs/yes_login_button.png " Knoop ")
