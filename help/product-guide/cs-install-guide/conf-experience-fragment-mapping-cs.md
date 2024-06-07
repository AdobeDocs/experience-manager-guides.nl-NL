---
title: Vorm de op JSON-Gebaseerde afbeelding tussen een onderwerp en een malplaatje van het Fragment van de Ervaring.
description: Leer hoe te om op JSON-Gebaseerde afbeelding tussen een onderwerp en een malplaatje van het Fragment van de Ervaring te vormen.
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: f252537d15d7e8f8651dddb0ae635905705e4adf
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Creeer een afbeelding tussen een onderwerp en een Fragment van de Ervaring

De Gidsen van Adobe Experience Manager verstrekt de eigenschap om een op JSON-Gebaseerde afbeelding tussen een onderwerp en een malplaatje van het Fragment van de Ervaring tot stand te brengen. U kunt deze afbeelding gebruiken om inhoud die aanwezig is in sommige of alle elementen binnen een onderwerp te publiceren naar een Ervingsfragment.

1. Als u het dialoogvenster *experienceFragmentMapping.json*, meldt u zich aan bij Adobe Experience Manager als beheerder.
1. Selecteer de Adobe Experience Manager-koppeling bovenaan en kies **Gereedschappen**.
1. Selecteer Hulplijnen in de lijst met gereedschappen en selecteer de optie **Mapprofielen**.
1. Selecteer de profieltegel die u wilt vormen. U kunt de toewijzing voor het globale profiel of een omslag-niveau profiel vormen. Selecteer bijvoorbeeld de **Globaal profiel** tegel.
1. Selecteer de **XML Editor-configuratie** en selecteert u de **Bewerken** bovenaan.
1. Selecteer de **Downloaden** pictogram om het *experienceFragmentMapping.json*  op uw lokale systeem. Vervolgens kunt u wijzigingen in het bestand aanbrengen en het bestand vervolgens uploaden.

1. U moet de volgende validaties uitvoeren:

   1. Het moet een JSON-bestand zijn
   2. Het moet een array bevatten met ten minste één object en elk object moet het volgende bevatten:


      `"template": string `

      `"mapping": array`

      Elk toewijzingsobject moet het volgende bevatten:

      `"name": string`

      `"class": string`

      `"resourceType": string`

      `"attributeMap": array`


1. Sla het bestand op en upload het.

De Gidsen van de Experience Manager zetten het volledige onderwerp in HTML om die dan aan de kerncomponenten kunnen worden in kaart gebracht die in het Fragment van de Ervaring worden gebruikt. De inhoud van een `<p>` -tag kan worden toegewezen om een tekstcomponent te maken in het Experience Fragment.
* `name`: Geef het element HTML op. Bijvoorbeeld: `<div>`, `<img>`
* `class`: Geef de DITA-elementtag op die overeenkomt met het HTML-element. Bijvoorbeeld: `<p>` `<image>`
* `resourceType`: Geef het brontype op dat van toepassing is op de component die wordt gebruikt in Experience Fragment. Bijvoorbeeld: `wcm/foundation/components/text` is resourceType voor wcm `text` component.
* `attributeMap`: Geef aanvullende informatie op voor de component, bijvoorbeeld of een tekstcomponent moet worden gerenderd als `RichText` of bevat het `fileReference` van een afbeeldingscomponent.




Voorbeeldbestand:

```
[
  {
    "template": "default",
    "mapping": [
      {
        "name": "#element",
        "resourceType": "wcm/foundation/components/text",
        "attributeMap": [
          {
            "from": "outerHTML",
            "to": "text"
          },
          {
            "value": true,
            "to": "textIsRich"
          }
        ]
      }
    ]
  },
  {
    "template": "/conf/we-retail/settings/wcm/templates/experience-fragment-web-variation",
    "mapping": [
      {
        "name": "div",
        "class": "title",
        "resourceType": "wcm/foundation/components/text",
        "attributeMap": [
          {
            "from": "outerHTML",
            "to": "text"
          },
          {
            "value": true,
            "to": "textIsRich"
          }
        ]
      },
      {
        "name": "h1, h2, h3, h4, h5, h6",
        "resourceType": "wcm/foundation/components/text",
        "attributeMap": [
          {
            "from": "outerHTML",
            "to": "text"
          },
          {
            "value": true,
            "to": "textIsRich"
          }
        ]
      },
      {
        "name": "div",
        "class": "p",
        "resourceType": "wcm/foundation/components/text",
        "attributeMap": [
          {
            "from": "outerHTML",
            "to": "text"
          },
          {
            "value": true,
            "to": "textIsRich"
          }
        ]
      },
      {
        "name": "img",
        "class": "image",
        "resourceType": "wcm/foundation/components/image",
        "attributeMap": [
          {
            "from": "outerHTML",
            "to": "fileReference"
          }
        ]
      },
      {
        "name": "#element",
        "resourceType": "wcm/foundation/components/text",
        "attributeMap": [
          {
            "from": "outerHTML",
            "to": "text"
          },
          {
            "value": true,
            "to": "textIsRich"
          }
        ]
      }
    ]
  }
]
```



Tijdens het publiceren van de Fragmenten van de Ervaring van de Redacteur van het Web, selecteer `Template` van de vervolgkeuzelijst in de **Experience Fragment genereren** in het dialoogvenster om de toewijzing voor de sjabloon weer te geven in het dialoogvenster **Toewijzing** veld. Als er geen aangepaste toewijzing voor een sjabloon aanwezig is, wordt de standaardtoewijzing weergegeven. U kunt de standaardafbeelding gebruiken om het hele onderwerp als een fragment van de Ervaring te publiceren.

Voor meer informatie, bekijkt u [Fragmenten voor ervaring publiceren](../user-guide/publish-experience-fragment.md).

