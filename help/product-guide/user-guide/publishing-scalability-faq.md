---
title: Veelgestelde vragen over publicatieprestaties en schaalbaarheid in Adobe Experience Manager Guides
description: Leer meer over de veelgestelde vragen over het publiceren van prestaties en schaalbaarheid in Adobe Experience Manager Guides.
source-git-commit: d128860bdff78c100ba348b54a237b237171635f
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 0%

---

# Veelgestelde vragen

Hieronder volgt een lijst met antwoorden op veelgestelde vragen met gedetailleerde informatie over hoe Adobe Experience Manager Guides publicatieworkflows, schalingsgedrag en infrastructuurprestaties beheert. Het is bedoeld voor zakelijke gebruikers, beheerders en documentatieteams die Experience Manager Guides gebruiken voor grootschalige publicatie. In het diagram wordt de algemene workflow van Experience Manager Guides Publishing Architecture beschreven.

![](images/IO_runtime.drawio.png){align="left"}


## Hoeveel publicatieverzoeken kan Experience Manager Guides per dag uitvoeren?

Het aantal publicatieverzoeken dat Experience Manager Guides per dag kan verwerken, is afhankelijk van de grootte en het type inhoud. Volgens de configuratie maakt het systeem één publicatietaak per processorcore mogelijk. In de huidige configuratie kunnen 20 publicatietaken parallel lopen (2 pods × 10 cores elk).

Als de productieomgeving automatisch wordt geschaald, kan dit aantal toenemen tot 40 gelijktijdige publicatietaken wanneer de pods worden geschaald tot 4.

## Hoeveel het publiceren verzoeken kunnen gelijktijdig lopen alvorens zij een rij worden gevormd?

- Minimaal (standaard): 20 publicatietaken (2 pods)
- Maximaal (geschaald): 40 publicatietaken (4 pods)

Dit aantal kan variëren afhankelijk van de totale serverlading. Als er andere Sling-taken op de achtergrond worden uitgevoerd, delen ze verwerkingskernen, waardoor de gelijktijdige uitvoering mogelijk tot minder dan 20 wordt beperkt.

## Heeft het uitvoeren van meerdere publicatieverzoeken invloed op andere toepassingsfuncties, zoals het bewerken van .dita-bestanden?

Er kan enige invloed op de prestaties zijn, maar deze is over het algemeen minimaal. De meeste zware verwerking vindt plaats op de IO-runtime (de service voor het publiceren van servers), terwijl de AEM-instantie voornamelijk I/O-bewerkingen uitvoert voor het genereren van afhankelijkheid en statuspolling. Als gevolg hiervan blijft het CPU-gebruik in AEM laag en worden de ervaringen met schrijven en bewerken grotendeels ongewijzigd gelaten.

## Hoe beheert Experience Manager Guides grote bestanden en afbeeldingen, zoals SVG&#39;s of .dita-bestanden van meer dan 500 kB?

Alle grote bestanden worden gecomprimeerd en opgeslagen in de JCR (Java Content Repository). De IO-runtime haalt het volledige ZIP-pakket op voordat de publicatie wordt gestart. Zelfs bij het verwerken van meerdere grote bestanden (bijvoorbeeld 500 kB elk) heeft dit geen significante invloed op de download- of overdrachtssnelheid vanwege geoptimaliseerde verpakking en parallelle I/O-afhandeling.

## Wat wordt de uitgeversinfrastructuur en configuratie gebruikt door Experience Manager Guides?

Experience Manager Guides gebruikt containergebaseerde, serverless microservices voor het publiceren. Elke nieuwe versie van de publicatieservice wordt vrijgegeven als een Docker-afbeelding, die automatisch wordt geïmplementeerd in de Adobe-cloudomgeving. Dit ontwerp garandeert:

- Geen specifiek infrastructuuronderhoud voor klanten
- Automatisch schalen om aan de vraag naar publicaties te voldoen
- Snelle updates en minimale downtime

## Als de publicatiewachtrij of het beheersysteem vastloopt als gevolg van overbelasting, worden andere AEM-functies dan beïnvloed?

Nee, de Experience Manager Guides is gebouwd met een foutverdraagzame architectuur. Als er in de publicatiewachtrij sprake is van overbelasting, worden aanvragen automatisch opnieuw geprobeerd en worden pods automatisch geschaald om de extra belasting af te handelen. Bij een bepaalde drempelwaarde wordt de belasting vertraagd om de stabiliteit te handhaven. Andere toepassingsgebieden (ontwerp, revisie, middelenbeheer) blijven ongewijzigd.

## Is er een controlehulpmiddel of logboektoegang beschikbaar om te identificeren wanneer Experience Manager Guides onder zware lading (gelijkaardig aan Jenkins controle) is?

Nee, u hebt momenteel geen toegang tot interne controlehulpmiddelen. Voor interne teams van Adobe kan de bewaking worden uitgevoerd met:

- Splunk for log and error tracking
- Kubernetes (K8s) CLI voor het controleren van prestaties op podniveau en het schrapen gedrag

Als de prestaties achteruit gaan, moeten klanten contact opnemen met Adobe Support om een onderzoek en analyse te starten.

## Welke verwerking wordt uitgevoerd alvorens een publicatieverzoek naar de microservice te verzenden?

Als u een publicatieverzoek activeert vanaf het tabblad Voorinstellingen in de kaartconsole, worden de volgende stappen uitgevoerd:

1. Het systeem accepteert de aanvraag en valideert de basislijn en voorwaardelijke voorinstellingen.
2. AEM aggregeert alle in aanmerking komende DITA-activa en afhankelijkheden.
3. Deze elementen worden gebundeld in een ZIP-pakket.
4. De serverloze publicatieservice draait een Docker-container omhoog, downloadt de elementen, voert de publicatiebewerking uit en plaatst de gegenereerde uitvoerartefacten weer in Experience Manager Guides.

Deze workflow zorgt voor betrouwbare, geïsoleerde en schaalbare publicatie-uitvoering.

## Hoeveel tijd neemt een kaart alvorens het op de microservicecontainer begint te publiceren en wat zijn de factoren die deze tijd bepalen?

Een publicatieverzoek neemt doorgaans een paar minuten in beslag voordat het naar de microservicecontainer wordt verzonden. Deze begintijd wordt gebruikt voor afhankelijkheidsaggregatie binnen AEM.

Zodra het verzoek op de serververless het publiceren dienst wordt ontvangen, hangt de totale het publiceren tijd van af:

- Grootte van de DITA-kaart
- Aantal onderwerpen en media-elementen
- Complexiteit van voorwaardelijke inhoud en opmaakregels

Grotere of complexere kaarten kunnen proportioneel langer duren om te publiceren.

## Kan Experience Manager Guides prioriteit geven aan publicatieverzoeken in de wachtrij (in plaats van First-come, First-Serve)?

Momenteel worden alle publicatietaken op gelijke wijze behandeld en een FCFS-model (First-come, First-Serve) gevolgd. Er is momenteel geen prioriteitsmechanisme beschikbaar.

Nochtans, in toekomstige versies, zou de prioriteringslogica (bijvoorbeeld, die op baangrootte of bedrijfsbelang wordt gebaseerd) als deel van rij optimaliseringsverhogingen kunnen worden geïntroduceerd.

## Hoe verwerkt Experience Manager Guides automatisch schalen voor het publiceren van aanvragen?

Experience Manager Guides-publicatie-infrastructuur ondersteunt automatisch schalen op basis van belasting. Bij publicatie neemt de vraag toe:

- Extra pods (containers) worden automatisch gecentreerd.
- Elke pod kan meerdere publicatietaken tegelijk verwerken.
- Als het laden eenmaal is verminderd, worden de pods verkleind om de kosten en prestaties te optimaliseren.

Dit verzekert hoge beschikbaarheid, verenigbare prestaties, en minimale rijtijd tijdens pieklading.

## Wat gebeurt er als een publicatietaak mislukt of uitvalt?

Als een publicatieverzoek mislukt als gevolg van een tijdelijk probleem (bijvoorbeeld netwerkonderbreking, time-out voor service):

- het wordt automatisch opnieuw geprobeerd gebaseerd op retry logica die in de het publiceren dienst wordt gevormd.
- logboeken en foutberichten worden in de achtergrond vastgelegd voor diagnostische doeleinden.
- u kunt de status van een fout weergeven en de publicatie handmatig opnieuw proberen via de kaartconsole, indien nodig.

## Kunt u de voortgang van een publicatietaak controleren of volgen?

Ja, Experience Manager Guides biedt realtime taakstatusupdates op het tabblad Voorinstellingen van de kaartconsole, waaronder:

- Begintijd en voltooiingstijd van taak
- Huidig werkgebied (resultaten comprimeren, verzenden, publiceren of uploaden)
- Foutmeldingen (indien aanwezig)

Dit helpt u baanvooruitgang begrijpen en potentiële vertragingen identificeren.

## Welke beste praktijken kunnen publicatieprestaties in Experience Manager Guides verbeteren?

Volg de volgende aanbevolen procedures om een optimale publicatiesnelheid te garanderen:

- Overbodige grote afbeeldingsbestanden of onderwerpen zonder referenties vermijden
- Basislijnen gebruiken om het bereik van publicatie te beperken
- Houd DITA kaarthiërarchieën handelbaar en goed georganiseerd
- Overmatig publiceren plannen tijdens niet-piekuren
- Voorwaardelijke filters effectief gebruiken om de verwerkingsbelasting te verminderen




