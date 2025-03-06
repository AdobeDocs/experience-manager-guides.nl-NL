---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 5.0.0
description: Meer informatie over de opgeloste problemen vindt u in de 5.0.0-release van Adobe Experience Manager Guides.
source-git-commit: 5ae05935d254b03ad99221bd5f65dbb6a3580c5f
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---

# Opgeloste problemen in de 5.0.0-release (maart 2025)

In dit artikel worden de bugs beschreven die zijn gecorrigeerd in verschillende gebieden met 5.0.0 release van Adobe Experience Manager Guides.


Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de 5.0.0 versie ](whats-new-5-0-0.md) nieuw is.

Leer over [ verbeteringsinstructies voor de 5.0.0 versie ](upgrade-instructions-5-0-0.md).


## Authoring

- Bij het bijwerken van voorwaarden uit het mapprofiel gaan alle voorwaardengroepen verloren en worden de voorwaarden samengevoegd. (23526)
- Het veranderen van de waarde van kopbalrijen voor een lijst in het **eigenschappen van de Inhoud** paneel past niet de bijgewerkte waarde toe. (23213)
- Voor volgende Guides-documentstatusovergangen moet de pagina worden vernieuwd. (19421)
- Wanneer het toevoegen van onderwerpen in kaart DITA gebruikend **het elementendialoog van de verwijzing van het 0} Onderwerp {in de** Auteur **mening, worden de geselecteerde onderwerpen opgenomen in omgekeerde orde van wordt geselecteerd.** 8031
- Wanneer het schakelen tussen **Auteur** mening en **Source** mening, worden de belangrijke ruimten in `<pre>` of `<codeblock>` elementen geschrapt en het dossier wordt bewaard met deze schrapping. (1987)
- De staat van het Document die als **wordt gemerkt Gedaan** keert aan **Ontwerp** terug alvorens een nieuwe versie op te slaan, resulterend in de **Gedaan** staat die niet in enige documentversies voortduurt. (2006)
- Wanneer lijstitems buiten de paratag worden geplaatst, gaat de inhoud van het lijstitem verloren. (22764)
- Wanneer het toevoegen van onderwerpen in kaart DITA gebruikend **het elementendialoog van de verwijzing van het 0} Onderwerp {in de** Auteur **mening, worden de geselecteerde onderwerpen opgenomen in omgekeerde orde van wordt geselecteerd.** (22858)
- Wanneer het toevoegen van nieuwe onderwerpverwijzingen in kaart DITA gebruikend **het elementendialoog van de verwijzing van 0} Onderwerp {in de** mening van de Lay-out **, worden de toegevoegde verwijzingen getoond als gebroken verbindingen.** (22859)
- Wanneer u op de `<simpletable>` markering binnen een onderwerp met de rechtermuisknop klikt, **anders noemt** optie niet toont. (22860)
- Wanneer u een `xref` invoegt die op sleutels gebaseerde verwijzingen met koppelingstekst gebruikt, wordt de koppelingstekst niet weergegeven in Experience Manager Guides. (1875)
- Het slepen van en het laten vallen van een beeld binnen een onderwerp in **Auteur** mening veroorzaakt de beeldverwijzing om te breken, die tot gegevensverlies leiden. (25769)
- Wanneer het zoeken van dossiers in de bewaarplaats gebruikend **Onderzoek &amp; filter** functionaliteit, kunnen de veelvoudige dossiers niet worden geselecteerd. 25104
- Wanneer u een afbeelding uit een extern product kopieert (bijvoorbeeld MS PowerPoint) en deze in hulplijnen plakt, wordt de functionaliteit voor het uploaden van het element direct voor gebruik in het bestand verbroken. 24983
- Het slepen van a `topicref` over een andere (in **Auteur** of **mening van de Lay-out**) veroorzaakt een bevestiging voor vervanging in plaats van het nesten, en het selecteren van **Nr** op de bevestigingsdialoog veroorzaakt nog inhoud om worden vervangen, leidend tot gegevensverlies. 18602
- U kunt geen meerdere sneltoetsen toevoegen aan één gebeurtenis. U kunt ook geen argument toevoegen aan een gebeurtenis wanneer u deze activeert vanuit een sneltoets. (1906)
- Wanneer u de browser opnieuw laadt, wordt het vorige gesloten tabblad voor afbeeldingen opnieuw geopend. (19267)
- Gedeeltelijk het selecteren van tekst in een paragraaf of lijstelement en het slepen van het buiten het element veroorzaakt inhoudsverlies wanneer het schakelen tussen **Auteur** en **Source** meningen. 25790

## Publiceren

- Publiceren naar Salesforce mislukt wanneer inhoud vaste spaties bevat. (23664)
- Voor kaarten met verbroken koppelingen mislukt het publiceren van de Salesforce en wordt de voortgangsbalk voor onbepaalde tijd weergegeven. 24963
- Voor onderwerpen met fouten zoals verbroken koppelingen mislukt het publiceren van de Salesforce en wordt de voortgangsbalk voor onbepaalde tijd weergegeven. (2985)
- Het inheemse publiceren pdf ontbreekt voor **PDF/x-4** conformiteitoptie met een fout die verklaart dat **PDF/x-4 documenten een niet lege titel** vereisen. 16904
- Als plaatsaanduidingstekst wordt gebruikt, kunnen kruisverwijzingen met `<keyref>` in native PDF niet worden opgelost. (19365)
- De inheemse generatie van PDF ontbreekt voor inhoud met **segmentattributen** die aan **aan-inhoud** worden geplaatst. (21772)
- Bij het genereren van een eigen PDF-uitvoer wordt het `ditavalref` -element niet ondersteund. (16320)
- Bij het bewerken van een groot CSS-bestand in de Native PDF CSS-editor wordt een aanzienlijke vertraging waargenomen. 16915
- Bij publicatie op basis van HTML5 wordt de DITA-OT-markering generate.copy.outer automatisch toegepast. (24299)
- De verwijzing zet in relatieve verbinding zelfs om wanneer het **werkingsgebied** van verbinding aan **extern** wordt geplaatst. (23059)
- Wanneer een ICC dossier bij een intern weg beschikbaar is, kan het niet in **1} montages van de Druk voor Inheemse vooraf ingestelde PDF worden geselecteerd.** (14741)
- Wanneer meerdere publicatieverzoeken voor verschillende kaarten worden gestart met dezelfde mapprofielvoorinstelling, mislukt het publiceren. (18800)
- Voor onderwerpen met een multi-getaxeerde meta-gegevens/bezit wanneer overgegaan tot DITA OT, ontbreekt het publiceren. (19001)
- Het **geeft eigenschappen** dialoog voor een basislijn uit toont niet de eerder bewaarde criteria voor dynamische basislijn.  (23964)
- De basislijn bevat geen indirecte verwijzingen wanneer de inhoud zich in de uiteindelijke documentstatus bevindt. (19148)
- Het plaatsen **Sanitize paginanamen &amp; filenames voor AEM Sites &amp; andere outputformaten** is van toepassing op alle outputformaten. 7651
- Als een externe koppeling een UUID bevat, gaat deze na de verwerking en wordt de externe koppeling naar de UUID-koppeling omgezet, waardoor de koppeling in de webeditor en ook op de publicatiesites wordt verbroken. (22574)


## Beheer

- De titel en het pictogram van het **Forceer schrappen** dialoogvakje worden verkeerd gericht in Assets UI. (21933)
- Wanneer om het even welke JSON in het omslagprofiel voor de Configuratie van de Redacteur van XML wordt bijgewerkt, verstoort de sparen verrichting de Configuratie van de Redacteur van XML. (22414)
- Wanneer u een mapprofiel dupliceert, wordt de bijbehorende lijst met gebruikers ook gekopieerd uit het oorspronkelijke mapprofiel. (19067)
- Wanneer u grote mappen (met een groot volume DITA-inhoud tot 200.000 items) verplaatst vanuit de gebruikersinterface van Assets, treedt er een fout op. (20107)
- Het uitgeven van het **profiel van de Omslag** met verenigde shell toegelaten, leidt tot lege UI. (22212)
- Wanneer u mappen verwijdert die een groot aantal bestanden bevatten, mislukt de bewerking. 17107
- Wanneer u annuleert/de vertaalbaan schrapt of het project schrapt, toont het vertaaldashboard **Bezig** status. 18417
- Wanneer u twee versies van een onvertaald onderwerp gelijktijdig gebruikend niet erfenisvertaling verzendt en de tweede versie vóór de eerste goedkeurt, wordt het vertaalproject met de eerste versie gebroken. (2200)


## Controleren

- Wanneer het selecteren van veelvoudige onderwerpen voor overzicht in een kaart, wijst het e-mailbericht dat de recensent ontvangt erop dat alle onderwerpen in de kaart voor overzicht, eerder dan enkel de geselecteerde onderwerpen beschikbaar zijn. (23214)
- De onderwerptitel en het pictogram worden verkeerd gericht in de interface van de overzichtsverwezenlijking. (11670)


## API&#39;s

- Wanneer het creëren van a **Basislijn** gebruikend de Gidsen API door **de dienst te teweegbrengen BaslinUtlis**, komt een fout voor. (19385)

## Bekende problemen

Adobe heeft de volgende bekende problemen voor 5.0.0-release geïdentificeerd:

- In sommige gevallen werkt de vergrendelingsfunctie voor CSS-bestanden niet zoals verwacht, waardoor andere gebruikers de bestanden kunnen bewerken en opslaan, zelfs als ze door een andere gebruiker zijn vergrendeld.
- Kan de kaartconsolemening niet afsluiten wanneer Basislijn vuil is en automatisch opslaan ingeschakeld is.
- Als u vooraf ingestelde wijzigingen in de instellingen toepast, worden de voorinstellingen die al op de kaart zijn gemaakt niet weergegeven als de naam van de voorinstelling hoofdletters bevat.
- De positie van Achtergrondkleur wordt verkeerd gericht in UI van **het Comité van de Voorwaarde**.
- Wanneer u beeld als a `<keyref>` gebruikt, wordt het **Type van Verwijzing** van het beeld niet getoond in het **Multimedia rapport**.
- Wanneer u afbeeldingen als variabelen gebruikt in de PDF-sjabloon, wordt dit niet omgezet in de uitvoer.
- In **lijst van het Onderwerp** rapporten, ontbreekt het sorteren door titel voor activa met `<conref>` of `<conkeyref>` in de titel, veroorzakend deze ingangen om altijd bij de bovenkant te verschijnen.
- Als u overschakelt naar een ander mapprofiel, worden de wijzigingen in de gebruikersinterface niet meteen doorgevoerd zonder de browser te vernieuwen.
- De aanpassingen van het extensieframework die vóór hulplijnen 5.0.0 zijn gemaakt, werken mogelijk niet naar behoren.
- De volledige inhoudsopgave van de kaart wordt niet bijgewerkt wanneer onderwerpen selectief van de kaart worden gepubliceerd.
- Het publiceren van een kaart die een dossier van de Prijsverhoging met interne beeldverwijzingen bevat, ontbreekt op de servers van Vensters.
- De lijst met opsommingstekens kan niet worden geconverteerd naar de genummerde lijst in Markeringen.
- Publiceren naar de eigen AEM-site mislukt wanneer markeringsbestanden worden vermeld in een kaart.


