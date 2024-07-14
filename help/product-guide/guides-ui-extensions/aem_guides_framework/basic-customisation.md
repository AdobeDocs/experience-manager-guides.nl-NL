---
title: De app aanpassen
description: De app aanpassen
role: User, Admin
exl-id: 3e454c48-2168-41a5-bbab-05c8a5b5aeb1
source-git-commit: 4f00d6b7ad45636618bafe92e643b3e288ec2643
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# De app aanpassen

Onze app volgt een MVC-structuur (Model, View, Controller)

## Model

Het model definieert de verschillende kenmerken en slaat de waarden ervan op. De waarden van de verschillende kenmerken die in het model zijn opgeslagen, zijn via de syntaxis toegankelijk via de controller

```typescript
this.getValue('attributeName')
```

Voor aanpassing in de app worden alle nieuwe kenmerken toegevoegd onder een kaart in het model.
Om een nieuw attribuut in het model te plaatsen zullen wij de volgende syntaxis in het controlemechanisme gebruiken:

```typescript
// If a key is not already in model then it will be added to extraProps
this.setValue('key', value)
```

Om tot een attribuut toegang te hebben dat aan het model wordt toegevoegd zullen wij de volgende syntaxis gebruiken:

```typescript
const value = this.getValue("key")
```

## Weergave

De weergave definieert de gebruikersinterface van de app. We gebruiken JSON-bestanden om de weergave van onze bestanden te definiëren. Hier, bepalen wij de componenten, css (zoals die in de winningsklasse van componenten wordt gegeven) en geven de waarden terug die in het model worden opgeslagen.
In onze app wordt elke weergave gedefinieerd met behulp van een JSON. Naar de JSON&#39;s wordt verwezen met behulp van hun unieke id&#39;s, ook wel een `id` genoemd.

## Controller

De controller wordt gebruikt om gebeurtenissen af te handelen en de gegevens te verwerken. Het controlemechanisme wordt gebruikt om gegevens van de server te halen en te verzenden, is het de interface tussen wat op UI wordt getoond en op het achtereind wordt opgeslagen.

- Voor het instellen van waarden bij initialisatie gebruikt u de functie `init` .
- Om een methode toe te voegen het controlemechanisme gebruiken wij de volgende syntaxis:

```typescript
methodName: function(args){
    // functionality
}
```

`methodName` hier fungeert als de `key` om te verwijzen naar de methode in de JSON-weergave (weergave) of in andere functies

- Om een methode in het controlemechanisme te roepen gebruiken wij de syntaxis

```typescript
this.next('methodName', args)
```

## Voorbeeld

Laten we nu een eenvoudig voorbeeld gebruiken om te laten zien hoe deze drie componenten met elkaar communiceren.
Wij zullen een knoop toevoegen die zijn etiketwaarde op een klik schakelt

### Voorbeeld weergeven

Hieronder wordt de JSON gedefinieerd voor een knop met een dynamische tekst die in het model is opgeslagen onder de variabelenaam `buttonLabel` .
In dit voorbeeld wordt het label gewijzigd wanneer u op de knop klikt.

```JSON
{
    "component": "button",
    "label": "@extraProps.buttonLabel",
    "variant": "cta",
    "on-click": "switchButtonLabel",
}
```

### Modelvoorbeeld

in dit geval bevat `extraProps.buttonLabel` het label van de knop

### Voorbeeld van controller

```typescript
  controller: {
    init: function (context) {
      context.setValue("buttonLabel", "Submit")
    },

    switchButtonLabel(){
        const buttonLabel = this.getValue("buttonLabel") === "Submit"? "Cancel" : "Submit"
        this.setValue("buttonLabel", buttonLabel)
    }
  }
```

Onder GIF ziet u de bovenstaande code in actie
![ basic_customization ](imgs/basic_customisation.gif " Basisaanpassingsknoop ")
