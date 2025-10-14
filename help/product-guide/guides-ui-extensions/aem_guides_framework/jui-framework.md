---
title: Jui Framework
description: Werken met Jui Framework
role: User, Admin
exl-id: c193cf90-5916-4d8c-88f1-be5014beca1c
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Jui Framework

Voordat we gaan bekijken hoe we extensies moeten schrijven, begrijpen we de architectuur van het framework.
Dus dat we het effectief kunnen uitbreiden.

## Inleiding

JUI is een kader MVC bovenop React en de componenten van het Spectrum van de Reactie van de Adobe. JUI is JSON-gebruikersinterface. Het bestaat uit meerdere it-repositories.

JUI-Core is de kernbibliotheek met alle logica om JSON config in werkende reactiecomponenten om te zetten en het met een relevante controlemechanismeklasseninstantie te verbinden.
JUI-React-Spectrum  bibliotheek bevat omvattende widgets voor Adobe React Spectrum-componenten

## JUI Core-ontwerp

### MVC UI-ontwerp

![&#x200B; JUI MVC stroom &#x200B;](./imgs/jui-mvc-flow.png)

### Widget

- Bevat een unieke id.
- Bevat een afzonderlijk JSON-bestand voor weergave.
- Kan een eigen of gedeelde controller hebben.
- Kan bovenliggend model of nieuw model gebruiken.
- Kan interface-elementen hebben (React Components)
- Kan andere widgets hebben
- App is een widget

![&#x200B; JUI Widget &#x200B;](./imgs/jui-widget.png)

### Element

- Is een HTML/React component.
- Heeft geen model, het gebruikt het bovenliggende widgetmodel.

### Gebeurtenishandler

- Next (eventOpts)
   - Om gebeurtenis met sommige opties teweeg te brengen
- Abonneren (callback)
   - Krijg bericht dat de gebeurtenis met configuratie in brand wordt gestoken

### App/Global-model

- Next (nieuwe waarde)
   - Nieuwe waarde publiceren
- Abonneren (callback)
   - Melding van waarde wijzigen
   - Eerste keer ophalen oude waarde
- GetValue()
   - Huidige waarde ophalen

### Controller

- Deze moet worden uitgebreid van de klasse Controller
- API&#39;s
- CreateModel
   - Een afzonderlijk model voor een onderliggende widget maken
- InitEventHandler
   - Een onderliggende widget maken, aparte gebeurtenishandler
- RegisterCommands
   - Lokale gebeurtenissen, bovenliggende gebeurtenissen of toepassingsgebeurtenissen registreren
- Next (eventName, eventHandler)
   - Gebeurtenis activeren voor onderliggende widget, gebeurtenishandler voor bovenliggende widget of app-gebeurtenishandler
- Subscribe(callback, eventHandler)
- SubscribeAppModel(callback)

### Voorbeeld van toepassingsontwerp

![&#x200B; Steekproef App &#x200B;](./imgs/jui-sample-app.png)
