---
title: Pictogram
description: Pictogram
role: User, Admin
exl-id: 5ba41c77-7329-49fc-bce5-02682261ea8e
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 0%

---

# Pictogram

Als u een pictogram wilt weergeven, gebruiken we de component, het pictogram.
De component van het tekstgebied in JUI vertegenwoordigt HTML `<icon/>`.

Pictogrammen beschikbaar bij [ de Pictogrammen van het Spectrum van de Adobe ](https://spectrum.adobe.com/page/icons/) zijn compatibel met onze app.

```js title="icon.js"
const iconJSON =  {
    "component": "icon", //tells the component name
    "icon": "info", // name of the icon to be used
    "size": "S", // size of the icon
    "title": "Information" // tooltip corresponding to the icon.
},
```

pictogrammen kunnen ook aan knoppen worden toegevoegd.

Het weergegeven pictogram ziet er als volgt uit:

![ pictogram ](./imgs/info_icon.png " Pictogram ")
