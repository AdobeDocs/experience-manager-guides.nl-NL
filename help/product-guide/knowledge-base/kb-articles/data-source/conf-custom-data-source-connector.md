---
title: Vorm een douaneschakelaar voor de gegevensbronnen
description: Leer hoe te om een douaneschakelaar voor de gegevensbronnen te vormen.
feature: Web Editor Configuration
role: Admin
level: Experienced
exl-id: ef7ab117-7541-4e89-9ba4-22254a17efc0
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 0%

---

# Aangepaste gegevensbronconnectors configureren

Experience Manager Guides staat u toe om de schakelaars aan uw vereisten aan te passen en dan hen met de verschillende gegevensbronnen te gebruiken. Om een schakelaar aan te passen, moet u de schakelaarinterface en zijn belangrijke functies uitvoeren, en dan de interface vormen. U kunt de middelen samen met de douaneschakelaars ook verstrekken.


- [Een connector aanpassen voor Experience Manager Guides](#customize-connector)
- [Implementeer de verbindingsinterface](#implement-interface)
- [Belangrijke functies](#important-functions)
- [Typen standaardschakelaarimplementaties](#default-connectors)
   - [Config-interface](#config-interface)
   - [Typen standaard configureert implementaties](#default-config-types)
   - [Concrete configuratieimplementaties](#concrete-config-implementation)
   - [Aanvullende bronnen](#resources)



## Een connector aanpassen voor Experience Manager Guides {#customize-connector}

U kunt een schakelaar voor een gegevensbron aanpassen of vormen gebruikend de vooraf bepaalde interfaces en abstracte klassen. De volledige broncode is beschikbaar in [&#x200B; https://github.com/adobe/guides-data-source-connectors/tree/main/konnect-definitions &#x200B;](https://github.com/adobe/guides-data-source-connectors/tree/main/konnect-definitions).


Verwijs naar [![&#x200B; javadoc &#x200B;](https://javadoc.io/badge2/com.adobe.aem.addon.guides/konnect-definitions/javadoc.svg) &#x200B;](https://javadoc.io/doc/com.adobe.aem.addon.guides/konnect-definitions) voor konnect-definities.

## Implementeer de verbindingsinterface {#implement-interface}

Voer de volgende stappen uit om de interface en zijn functies volgens uw vereisten uit te voeren:

1. Bepaal een gestandaardiseerde manier voor de schakelaars om met een systeem te integreren, die voor de uitvoering van vragen, bevestiging van verbindingen, en het terugwinnen van meta-gegevens toestaat.
1. Faciliteer de integratie UI door de standaardmethodes te verstrekken om malplaatjes, logo&#39;s, vragen, en andere montages te vormen.
1. Zorg ervoor dat de schakelaars behoorlijk worden bevestigd en fouten (`KonnectException`) kunnen behandelen wanneer het interactie met gegevensbronnen.

De interface fungeert als blauwdruk voor het implementeren van verschillende typen gegevensconnectors, zodat de connectors voldoen aan specifieke integratie- en operationele vereisten binnen een groter software-ecosysteem.

## Belangrijke functies {#important-functions}

Voer de volgende belangrijke functies uit:

| Methode | Verplicht | Beschrijving |
|---|---|---|
| getLogoUrl |  | <ul><li> Deze methode keert URL terug die als embleem van de schakelaar wordt gebruikt. <li> Standaard wordt een lege tekenreeks geretourneerd, die aangeeft dat er geen logo-URL is opgegeven, tenzij deze wordt overschreven. <br><b> Aanvullende opmerkingen </b> : <br> <ul><li> Als u zowel een logo-URL als een logo-klassenaam opgeeft, wordt de URL van het logo gebruikt om het logo weer te geven in de gebruikersinterface. <li> Als u de URL van het logo opgeeft via de configuratie-instellingen, wordt de URL die is ingesteld in de methodeimplementatie genegeerd. |
| validateConnection | Ja | <ul><li> Gebruik deze methode om te bevestigen of de schakelaar een verbinding aan zijn gegevensbron kan vestigen. <li> Het neemt een `ConfigDto` voorwerp als parameter, die de configuratiemontages zoals verbindingsgeloofsbrieven, en eindpunt URLs bevat. <li> De methode retourneert true als de validatie (verbindingstest) is gelukt. Dit geeft aan dat de connector verbinding kan maken met de gegevensbron. |
| uitvoeren | ja | <ul><li>Gebruik deze methode om één enkele vraag voor de schakelaar uit te voeren, interactie met een gegevensbron. <li> De schakelaars die deze verrichting steunen behandelen de vraaguitvoering, ontleden de reactie, en zetten het in een koord JSON indien nodig om. <li> Comprimeer de query die in deze methode moet worden uitgevoerd binnen een `QueryInfoDto` -object, dat details bevat zoals de querytekenreeks en parameters. <li> De methode retourneert een JSON-tekenreeks die de reactie van het uitvoeren van de query vertegenwoordigt. <br><b> Aanvullende opmerkingen </b> : <li>De implementaties van deze methode variëren afhankelijk van de specifieke schakelaar en zijn interactie met de gegevensbron. <li> Gebruik `KonnectException` om uitzonderingen of fouten af te handelen die optreden tijdens de uitvoering of verbinding met de gegevensbron. |
| executeWithLimit | ja | <ul><li> Gebruik deze methode voor hetzelfde doel als `execute()` , maar met de extra functionaliteit om een beperkende query toe te passen, meestal voor het weergeven van voorvertoningen in UI-componenten. <li> De schakelaars die deze verrichting steunen behandelen de vraaguitvoering, ontleden de reactie, en zetten het in een koord JSON indien nodig om. <li> Inkapselt de query die in deze methode moet worden uitgevoerd binnen een `QueryInfoDto` -object, vergelijkbaar met de vorige methode. <br><b> Aanvullende opmerkingen </b> : <ul><li> `QueryResultDto` is een aangepaste klasse of een object voor gegevensoverdracht dat het resultaat van de uitvoering van de query omvat, inclusief metagegevens over de query en de uitvoeringsstatus ervan. |
| getSampleQuery | | <ul><li>Deze methode retourneert een voorbeeldqueryreeks die kan worden weergegeven in de gebruikersinterface, bijvoorbeeld in het dialoogvenster waarin gebruikers query&#39;s kunnen invoegen of bewerken. <li>Door gebrek, keert het een leeg koord terug, erop wijzend dat geen steekproefvraag wordt verstrekt tenzij met voeten getreden. <br><b> Aanvullende opmerkingen </b> : <ul> <li> Als u geen steekproefvraag bepaalt, en de methode keert een leeg koord terug, wordt geen steekproefvraag getoond in de UI tussenvoegselvraagdialoog. |
| getTemplates | | <ul> <li> Deze methode keert een lijst van malplaatjes verbonden aan de schakelaar terug. <li> Standaard wordt een lege lijst geretourneerd, met de aanduiding dat er geen sjablonen worden opgegeven, tenzij deze worden overschreven. |
| getLogoClassName | | <ul> <li> Deze methode keert de klassennaam als embleem van de schakelaar terug. Standaard wordt een lege tekenreeks geretourneerd, die aangeeft dat er geen naam van een logoklasse is opgegeven, tenzij deze wordt overschreven. <br><b> Aanvullende opmerkingen </b> : <ul><li> Als u zowel een logo-URL als een logo-klassenaam opgeeft, wordt de URL van het logo gebruikt om het logo weer te geven in de gebruikersinterface. <li> Als u de naam van de logoklasse opgeeft via configuratie-instellingen, wordt de klassenaam die is ingesteld in de methodeimplementatie genegeerd. |
| enabled | ja | <ul><li> Deze methode controleert of een `connector` is ingeschakeld. <li> Door gebrek, keert de methode vals terug, betekenend dat de schakelaar niet wordt toegelaten tenzij met voeten getreden door een klasse die deze methode uitvoert. |
| getDescription | | <ul><li>Gebruik deze methode om een beschrijvende tekenreeks te retourneren die in de gebruikersinterface kan worden weergegeven. <li> Standaard wordt een lege tekenreeks geretourneerd, die aangeeft dat geen beschrijving wordt gegeven, tenzij deze wordt overschreven. |
| getAuthor | | <ul><li> Deze methode verstrekt een manier om de naam van de auteur terug te winnen die creeerde of voor de schakelaar verantwoordelijk is. <li> Het helpt typisch de schepper of het onderhoud van de schakelaar binnen een systeem of kader identificeren en erkennen. |
| getName | ja | <ul><li>Deze methode verstrekt een manier om de unieke naam terug te winnen die aan een schakelaar wordt toegewezen. <li>De teruggekeerde naam is essentieel voor het identificeren van de schakelaar binnen een context van het gebruikersinterface (UI), vooral als de de configuratiemontages van de schakelaar geen naam uitdrukkelijk specificeren. <li>Deze naam wordt gebruikt in diverse componenten UI om schakelaars op een gebruikersvriendelijke manier te tonen of te beheren. |
| getGroup | ja | <ul> <li>Deze methode verstrekt een manier om de groepsnaam terug te winnen verbonden aan een schakelaar. <li>De namen van de groep worden typisch gebruikt om schakelaars in logische groepen te organiseren of te categoriseren die op hun functionaliteit, doel, of type worden gebaseerd. <li> Dit staat voor gemakkelijker beheer en presentatie van schakelaars binnen de configuratie UI toe. |
| getDefaultTemplatePath |  | <ul><li> Deze methode keert de standaardweg voor de malplaatjes verbonden aan deze schakelaar terug. <li> Standaard wordt een lege tekenreeks geretourneerd die aangeeft dat er geen standaardpad is ingesteld, tenzij dit wordt overschreven. |
| getLogoSvg |  | <ul><li>Gebruik deze methode om de SVG-weergave van het logo van de connector te retourneren. <li> Standaard wordt een lege tekenreeks geretourneerd die aangeeft dat geen SVG-gegevens worden opgegeven, tenzij deze worden overschreven. |
| getMaxNoRowsForPreviewQuery | | <ul><li>Deze methode retourneert het maximum aantal rijen dat wordt gevraagd of weergegeven in de UI-voorvertoning. <li> Standaard wordt de waarde van DEFAULT_LIMIT_PREVIEW geretourneerd, een constante die de standaardlimiet voor voorvertoningsrijen vertegenwoordigt. |
| getConfigClass | ja | <ul><li>Deze methode verstrekt informatie over de klassen die de interface Config uitvoeren en door deze schakelaar gesteund. <li> Het staat de toepassing of het kader toe om dynamisch configuraties te ontdekken en te werken die met de schakelaar compatibel zijn. |

## Typen standaardschakelaarimplementaties {#default-connectors}

De *konnect-definities* bibliotheek schepen abstracte schakelaarimplementaties en met vooraf bepaalde functies om vragen in werking te stellen. Deze schakelaarimplementaties handelen als malplaatjes die direct kunnen worden uitgebreid en worden gebruikt zoals is. Als een aangepaste implementatie is vereist, kunnen de functies worden overschreven.

Naast het uitvoeren van de standaardschakelaars, kunt u één van de volgende standaard abstracte klassen ook uitvoeren:

- Aansluiting rust
- Bestandsconnector
- GraphQL Connector
- SQL Connector
- NoSQL Connector


Als een schakelaar in één van deze types past, breid de schakelaar tot de overeenkomstige basisklasse uit. Anders, creeer het van kras door de schakelaarinterface uit te voeren.

## Config-interface {#config-interface}

De interface `Config` wordt ontworpen om een gegevensbron met een specifieke authentificatiemethode te vormen, die u nauwkeurige controle over geeft hoe u de verbinding creeert.

De interface `Config` biedt flexibiliteit in de manier waarop verificatiedetails worden afgehandeld en geïmplementeerd. De verschillende implementaties kunnen diverse manieren aanbieden om gegevensbronnen voor authentiek te verklaren. Een schakelaar gebruikt een instantie Config om vragen tegen een gegevensbron uit te voeren en te bevestigen, die een volledige werkschema vormen.
Een connector gebruikt een `Config` -instantie om query&#39;s uit te voeren en te valideren aan de hand van een gegevensbron, waardoor een volledige workflow wordt gevormd.

Een config implementatie bepaalt hoe de authentificatie wordt behandeld om met een gegevensbron te verbinden. Dit config wordt dan gebruikt door een schakelaarimplementatie om met de gegevensbron in wisselwerking te staan, die ervoor zorgen dat de vragen correct worden uitgevoerd en bevestigd.

Over het geheel genomen is de interface van `Config` een cruciaal onderdeel van de workflow voor het maken van verbinding met gegevensbronnen, waarbij de nadruk specifiek ligt op verificatieconfiguratie.

### Typen standaard configureert implementaties {#default-config-types}

Er zijn drie soorten standaard abstracte configuratieimplementaties voor Authentificatie:

- RestConfig
- SqlConfig
- NoSqlConfig

Als een config zich op één van deze types richt, kan het de overeenkomstige basisklasse uitbreiden. Anders, kan het van kras worden gecreeerd door de interface Config uit te voeren.

### Concrete configuratieimplementaties {#concrete-config-implementation}

De *konnect-definities* bibliotheekschepen met vooraf bepaalde implementaties van de interface Config voor sommige wijd gebruikte authentificatieconfiguraties. U kunt deze configuraties direct in de schakelaar gebruiken of nieuw bepalen gebruikend de interface Config. Deze implementaties omvatten:

- Config. API-sleutelauteur
- De basis Token-Gebaseerde Config van de Auth
- Basisconfiguratie auteur
- Toekennen aan toonder configureren
- Gebruikersbenaming Wachtwoord config voor SQL
- Auth-config van verbindingstekenreeks voor NoSQL

### Aanvullende bronnen{#resources}

Met Experience Manager Guides kunt u ook aangepaste bronnen voor logo&#39;s en sjablonen en de implementatie bieden. U kunt deze bronnen in de map `resources` houden.
Om ze bruikbaar te maken door de connector is het verplicht om deze verbindingsfuncties te implementeren:


- `getLogoSvg` - Retourneert het logo SVG als een tekenreeks.

- `getTemplates` - Geeft als resultaat de lijst met sjablonen in de opgegeven indeling.
