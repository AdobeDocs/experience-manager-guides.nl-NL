---
title: De app aanpassen
description: De app aanpassen
role: User, Admin
exl-id: 3e454c48-2168-41a5-bbab-05c8a5b5aeb1
source-git-commit: 3615928117ce1be527dc3c6d2ec8ddd115b78b0a
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# De app aanpassen

## Functionaliteit onder extensieframework beschikbaar

We hebben een set functies en getters onder een `proxy` weergegeven die kan worden gebruikt om toegang te krijgen tot gegevens, om gebeurtenissen te configureren en te activeren. Hieronder ziet u een lijst en hoe u deze kunt openen.

```typescript
interface EventData {
  key?: string,
  keys?: string[]
  view?: any,
  next?: any,
  error?: any,
  completed?: any,
  id?: any
}

* getValue(key)
* setValue(key, value)
* subject // getter
* subscribe(opts: EventData)
* subscribeAppEvent(opts: EventData)
* subscribeAppModel(key, next)
* subscribeParentEvent(opts: EventData)
* parentEventHandlerNext(eventName: string, opts: any)
* appModelNext(eventName:string, opts) 
* appEventHandlerNext(eventName:string, opts)
* next(eventName:string, opts, eventHandler?)
* viewConfig //getter
* args //getter
```

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
    init: function () {
      this.setValue("buttonLabel", "Submit")
    },

    switchButtonLabel(){
        const buttonLabel = this.getValue("buttonLabel") === "Submit"? "Cancel" : "Submit"
        this.setValue("buttonLabel", buttonLabel)
    }
  }
```

Onder GIF ziet u de bovenstaande code in actie
![ basic_customization ](imgs/basic_customisation.gif " Basisaanpassingsknoop ")


### Configuratievoorbeeld weergeven

In dit geval gebruiken we de zoekmodusgebeurtenis `viewConfig` en activeren we een gebeurtenis om deze bij te werken

```typescript
  { 
    id: 'repository_panel', 
    controller: {
      init: function () {
        console.log('Logging view config ', this.viewConfig)
        this.next(this.viewConfig.items[1].searchModeChangedEvent, { searchMode: true })
      }
    }
  }
```

### Abonneren, voorbeeld

In dit geval voegen we een abonnement op een bestandsnaam toe aan het logbestand van de console wanneer op de optie Naam wijzigen van bestand wordt geklikt

```typescript
  { 
    id: 'repository_panel', 
    controller: {
      init: function () {
        this.subscribe({
          key: 'rename',
          next: () => { console.log('rename using extension') }
        })
      }
    }
  }
```

### Gebeurtenisvoorbeeld van de toepassing Abonneren

In dit geval is het aanmelden van het actieve document op onze console gewijzigd (tabbladen in editor-UI wijzigen)

```typescript
  { 
    id: 'repository_panel', 
    controller: {
      init: function () {
        this.subscribeAppEvent({
          key: 'app.active_document_changed',
          next: () => { console.log('Extension: active document changed') }
        })
      }
    }
  }
```

### Voorbeeld van gebeurtenissen in toepassingsmodel abonneren

Voorbeeld voor het abonneren van toepassingsmodelgebeurtenissen zoals `app.mode`

```typescript
  { 
    id: 'repository_panel', 
    controller: {
      init: function () {
        this.subscribeAppModel('app.mode',
          () => { console.log('app mode subs') }
        )
      }
    }
  }
```

### Voorbeeld van gebeurtenissen met bovenliggende controller

Hierin voegen we een abonnement op de `tabChange` -gebeurtenis toe. Dit is een gebeurtenis van `left_panel_container` controller die handelt
als bovenliggende controller voor `repository_panel`

```typescript
  { 
    id: 'repository_panel', 
    controller: {
      init: function () {
        this.subscribeParentEvent({
          key: 'tabChange',
          next: () => { console.log('tab change subs') }
        })
        this.parentEventHandlerNext('tabChange', {
          data: 'map_panel'
        )
      }
    }
  }
```

### Volgend toepassingsmodel en toepassingscontroller

Ze kunnen rechtstreeks worden geactiveerd door de juiste gebeurtenis en de bijbehorende gegevens te kennen

```typescript
  { 
    id: 'file_options', 
    controller: {
      init: function () {
        this.appModelNext('app.mode', 'author')
        this.appEventHandlerNext('app.active_document_changed', 'active doc changed')   
      }
    }
  } 
```
