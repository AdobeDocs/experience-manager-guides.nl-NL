---
title: Vorm de op JSON-Gebaseerde afbeelding tussen een onderwerp en een model van het inhoudsfragment.
description: Leer hoe te om op JSON-Gebaseerde afbeelding tussen een onderwerp en een model van het inhoudsfragment te vormen.
exl-id: 438e2964-b9c7-462a-a68c-8031bd97911c
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 97d7776c81e7776d0248d6711ae5d05c46c44239
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Een koppeling maken tussen een onderwerp en een inhoudsfragment



Met Adobe Experience Manager Guides kunt u een JSON-toewijzing maken tussen een onderwerp en een inhoudsfragmentmodel. U kunt op JSON-Gebaseerde afbeelding gebruiken om inhoud die in sommige of alle elementen binnen een onderwerp aanwezig is, naar een inhoudsfragment te publiceren.

>[!NOTE]
> 
> Als u versie 4.6 of hoger gebruikt, hoeft u deze toewijzing niet te maken, kunt u de onderwerpelementen naar de velden in het fragmentmodel van de inhoud slepen.
> Leer meer over hoe te om [ inhoudsfragmenten ](../user-guide/publish-content-fragment.md) te publiceren.


1. Om *contentFragmentMapping.json* te downloaden, login in Adobe Experience Manager als beheerder.
1. Selecteer de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer Gidsen van de lijst van hulpmiddelen en selecteer de **Profielen van de Omslag**.
1. Selecteer de **Globale tegel van het Profiel**.
1. Selecteer het **lusje van de Configuratie van de Redacteur van XML** en selecteer **uitgeven** pictogram op de bovenkant.
1. Selecteer het **pictogram van de Download** om het {*dossier 2} contentFragmentMapping.json op uw lokaal systeem te downloaden.* Vervolgens kunt u wijzigingen in het bestand aanbrengen en het bestand vervolgens uploaden.

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

U kunt het gehele onderwerp met de standaardafbeelding publiceren. Selecteer de `Full Topic` afbeelding van dropdown **produceer de dialoogdoos van het Fragment van de Inhoud**, en hebben &quot;topicData&quot;gebied in het model van het inhoudsfragment.
