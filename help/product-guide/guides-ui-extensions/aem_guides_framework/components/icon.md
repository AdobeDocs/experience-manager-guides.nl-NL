---
title: Pictogram
description: Pictogram
role: User, Admin
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 0%

---

# Pictogram

Als u een pictogram wilt weergeven, gebruiken we de component, het pictogram.
De component van het tekstgebied in JUI vertegenwoordigt een HTML `<icon/>`.

Pictogrammen beschikbaar op [Spectrumpictogrammen Adobe](https://spectrum.adobe.com/page/icons/) zijn compatibel met onze app.

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

![pictogram](./imgs/info_icon.png "Pictogram")
