---
title: Vorm de op JSON-Gebaseerde afbeelding tussen een onderwerp en een malplaatje van het Fragment van de Ervaring.
description: Leer hoe te om op JSON-Gebaseerde afbeelding tussen een onderwerp en een malplaatje van het Fragment van de Ervaring te vormen.
feature: Output Generation
role: Admin
level: Experienced
exl-id: 2b59db60-61b5-4a7e-bbf1-35cab8b89323
source-git-commit: d525775afeeb89754762ff514126b1c3a3307b3f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Creeer een afbeelding tussen een onderwerp en een Fragment van de Ervaring

Adobe Experience Manager Guides verstrekt de eigenschap om een op JSON-Gebaseerde afbeelding tussen een onderwerp en een malplaatje van het Fragment van de Ervaring tot stand te brengen. U kunt deze afbeelding gebruiken om inhoud die aanwezig is in sommige of alle elementen binnen een onderwerp te publiceren naar een Ervingsfragment.

1. Om *experienceFragmentMapping.json* te downloaden, login in Adobe Experience Manager als beheerder.
1. Selecteer de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer Gidsen van de lijst van hulpmiddelen en selecteer de **Profielen van de Omslag**.
1. Selecteer de profieltegel die u wilt vormen. U kunt de toewijzing voor het globale profiel of een omslag-niveau profiel vormen. Bijvoorbeeld, selecteer de **Globale tegel van het Profiel**.
1. Selecteer het **lusje van de Configuratie van de Redacteur van XML** en selecteer **uitgeven** pictogram op de bovenkant.
1. Selecteer het **pictogram van de Download** om het {*dossier 2} ExperienceFragmentMapping.json op uw lokaal systeem te downloaden.* Vervolgens kunt u wijzigingen in het bestand aanbrengen en het bestand vervolgens uploaden.

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

Experience Manager Guides zet het volledige onderwerp in HTML om die dan aan de kerncomponenten kan worden in kaart gebracht die in het Fragment van de Ervaring worden gebruikt. De inhoud van een tag `<p>` kan bijvoorbeeld worden toegewezen om een tekstcomponent te maken in het Experience Fragment.
* `name`: geef het element HTML op. Bijvoorbeeld `<div>` , `<img>`
* `class`: geef de DITA-elementtag op die correspondeert met het HTML-element. Bijvoorbeeld: `<p>` `<image>`
* `resourceType`: geef het brontype op dat van toepassing is op de component die wordt gebruikt in Experience Fragment. `wcm/foundation/components/text` is bijvoorbeeld het resourceType voor de `text` -component wcm.
* `attributeMap`: geef aanvullende informatie aan de component, bijvoorbeeld of een tekstcomponent moet worden gerenderd als `RichText` of de `fileReference` van een afbeeldingscomponent bevat.




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



Terwijl het publiceren van de Fragmenten van de Ervaring van de Redacteur van het Web, selecteer `Template` van dropdown in **produceer de dialoogdoos van het Fragment van de Ervaring** om de afbeelding beschikbaar voor het malplaatje op het **In kaart brengende** gebied te bekijken. Als er geen aangepaste toewijzing voor een sjabloon aanwezig is, wordt de standaardtoewijzing weergegeven. U kunt de standaardafbeelding gebruiken om het hele onderwerp als een fragment van de Ervaring te publiceren.

Voor meer details, mening [&#x200B; de Fragmenten van de Ervaring van Publish &#x200B;](../user-guide/publish-experience-fragment.md).
