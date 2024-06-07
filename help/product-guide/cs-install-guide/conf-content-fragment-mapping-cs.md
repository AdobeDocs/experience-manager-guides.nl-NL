---
title: Vorm de op JSON-Gebaseerde afbeelding tussen een onderwerp en een model van het inhoudsfragment.
description: Leer hoe te om op JSON-Gebaseerde afbeelding tussen een onderwerp en een model van het inhoudsfragment te vormen.
exl-id: 438e2964-b9c7-462a-a68c-8031bd97911c
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: f8c71e18f5e2e5dbc5a2abdbb92c72fdad3bb233
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Een koppeling maken tussen een onderwerp en een inhoudsfragment

AEM Gidsen verstrekt de eigenschap om een op JSON-Gebaseerde afbeelding tussen een onderwerp en een model van het inhoudsfragment tot stand te brengen. U kunt deze toewijzing gebruiken om inhoud die in sommige of alle elementen binnen een onderwerp aanwezig is, naar een inhoudsfragment te publiceren.

1. Als u het dialoogvenster *contentFragmentMapping.json*, meldt u zich aan bij Adobe Experience Manager als beheerder.
1. Selecteer de Adobe Experience Manager-koppeling bovenaan en kies **Gereedschappen**.
1. Selecteer Hulplijnen in de lijst met gereedschappen en selecteer de optie **Mapprofielen**.
1. Selecteer de **Globaal profiel** tegel.
1. Selecteer de **XML Editor-configuratie** en selecteert u de **Bewerken** bovenaan.
1. Selecteer de **Downloaden** pictogram om het *contentFragmentMapping.json*  op uw lokale systeem. Vervolgens kunt u wijzigingen in het bestand aanbrengen en het bestand vervolgens uploaden.

1. U moet de volgende validaties uitvoeren:

   1. Het moet een JSON-bestand zijn
   2. Het moet een array bevatten met ten minste één object en elk object moet het volgende bevatten:


      `"name": string `

      `"mapping": array`

      Elk toewijzingsobject moet het volgende bevatten:

      `"modelField": string`

      `"xpath": string`

      `"outputType": string`
1. Sla het bestand op en upload het.

Voorbeeldbestand:

```
[
  {
    "mapping": [
      {
        "modelField": "title",
        "xpath": "/topic[1]/title[1]",
        "outputType": "textContent"
      },
      {
        "modelField": "shortdesc",
        "xpath": "/topic[1]/shortdesc[1]",
        "outputType": "textContent"
      },
      {
        "modelField": "topicData",
        "xpath": "/topic[1]/body[1]",
        "outputType": "outerHTML"
      }
    ],
    "name": "Full Topic"
  },
  {
    "mapping": [
      {
        "modelField": "title",
        "xpath": "/topic[1]/title[1]",
        "outputType": "textContent"
      },
      {
        "modelField": "shortdesc",
        "xpath": "/topic[1]/shortdesc[1]",
        "outputType": "textContent"
      },
      {
        "modelField": "heroImage",
        "xpath": "/topic[1]/body[1]/p[1]/image[1]",
        "outputType": "outerHTML"
      },
      {
        "modelField": "dataTable",
        "xpath": "/topic[1]/body[1]/table[1]",
        "outputType": "outerHTML"
      }
    ],
    "name": "Sample Example with XPath"
  }
]
```

U kunt het gehele onderwerp met de standaardafbeelding publiceren. Selecteer de `Full Topic` afbeelding van de vervolgkeuzelijst **Inhoudsfragment genereren** en heeft het veld &quot;topicData&quot; in het fragmentmodel van de inhoud.
