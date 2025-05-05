---
title: Eenvoudige aanpassing
description: Eenvoudige aanpassing, voorbeeld
role: User, Admin
exl-id: 7f19f0b0-2a1b-4a8b-b28c-3918a1bc9096
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Eenvoudige aanpassing, voorbeeld

Laten we nu hoe we deze aanpassingen kunnen integreren in onze AEM Guides-app.

We willen deze knop bijvoorbeeld toevoegen aan een bestaande weergave van de app.
Hiervoor moeten drie fundamentele dingen worden gedaan:

1. De `id` van de weergave-JSON waaraan we onze component willen toevoegen.
2. De `target` , dat wil zeggen de locatie in de JSON waaraan we de nieuwe component willen toevoegen. `target` wordt gedefinieerd met een `key` en `value` . Het sleutelwaardepaar kan om het even welk attribuut zijn dat wordt gebruikt om de component te bepalen die in unieke identificatie van het kan helpen.
We kunnen indexen ook gebruiken om naar het doel te verwijzen.
We hebben 3 viewStates: `APPEND`, `PREPEND`, `REPLACE` .
3. De JSON van de nieuw gemaakte component en de bijbehorende methoden.

Stel dat u een knop wilt toevoegen aan de gereedschapset voor annotaties die wordt gebruikt in de revisie, waarmee het bestand in AEM wordt geopend.

```typescript
export default {
  id: 'annotation_toolbox', 
  view: {
    items: [
      {
        component: 'button',
        icon: 'linkOut',
        title: 'Open topic in Assets view',
        'on-click': 'openTopicInAEM',
        target: {
          key: 'value',
          value: 'addcomment',
          viewState: VIEW_STATE.APPEND

        },
      },
    ],
  },
  controller: {
    openTopicInAEM: function (args) {
        const topicIndex = tcx.model.getValue(tcx.model.KEYS.REVIEW_CURR_TOPIC)
        const {allTopics = {}} = tcx.model.getValue(tcx.model.KEYS.REVIEW_DATA) || {}
        tcx.appGet('util').openInAEM(allTopics[topicIndex])
    },
  },
}
```

In het bovenstaande voorbeeld hebben we:

1. de `id` van de JSON waarin we onze component willen invoegen, dat wil zeggen `annotation_toolbox`
2. het doel is de knop `addcomment` . We voegen onze knop na de knop `addcomment` toe met behulp van viewState `append` .
3. De gebeurtenis on-click van de knop in de controller wordt gedefinieerd.

De JSON voor de &quot;annotation_toolbox&quot; `.src/jsons/review_app/annotation_toolbox.json`

Voordat de annotatietoolbox werd aangepast, zag deze er als volgt uit:

![ annotation-toolbox ](imgs/annotation_toolbox.png " toolbox van de Annotatie ")

Na de aanpassing ziet de gereedschapset voor annotaties er als volgt uit:

![ aangepast-annotation-toolbox ](imgs/customised_annotation_toolbox.png " Aangepaste annotatietoolbox ")

## CSS toevoegen

Voor de consistentie bieden we de component die al is opgemaakt. Op de ingevoegde JSON worden inherente stijlen toegepast
De primaire manier om CSS te beheren is door de extraClass sleutel in de uitbreidingen.

```js
{    
    "view":{
        items:[
            {
                compoenent:"button",
                extraClass:"underline bg-red",
            }
        ]
    }
}
```

U kunt aangepaste stijlen met CSS-klassen plaatsen door een CSS-bestand toe te voegen aan clientlibs. Tijdens de bouw creëren wij ook [&#128279;](https://tailwindcss.com/docs/utility-first) output 0&rbrace; Tailwind &lbrace;voor de nutsklassen in staartwind.  De config voor hetzelfde bestand vindt u in de map `tailwind.config.js` op `./tailwind.config.js`
