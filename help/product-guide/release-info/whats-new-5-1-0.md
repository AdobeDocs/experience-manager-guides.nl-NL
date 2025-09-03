---
title: Opmerkingen bij de release | Nieuwe functies in Adobe Experience Manager Guides 5.1.0-release
description: Meer informatie over de nieuwe en verbeterde functies in de 5.1.0-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: f6617b727d385d31ba66d575ee48f29e77ac716f
workflow-type: tm+mt
source-wordcount: '1398'
ht-degree: 0%

---

# Nieuwe functies in de release 5.1.0 (september 2025)

Dit artikel behandelt de nieuwe en verbeterde functies die zijn geïntroduceerd met versie 5.1.0 van Adobe Experience Manager Guides.

Voor de lijst van kwesties die in deze versie zijn bevestigd, mening [ Vaste kwesties in de 5.1.0 versie ](fixed-issues-5-1-0.md).

Leer over [ verbeteringsinstructies voor de 5.1.0 versie ](../release-info/upgrade-instructions-5-1-0.md).


## Verbeterde revisieworkflow

Met deze release is de revisieworkflow aanzienlijk verbeterd en is de communicatie tussen auteurs en revisoren verbeterd. Belangrijke updates zijn:

- Workflows voor taakbeheer met meldingen die kunnen worden uitgevoerd
- Mogelijkheid om gebruikers te voorzien van tags om onmiddellijk aandacht te vragen
- Toegang tot project- en taakdetails vanuit het deelvenster Review voor gebruiksgemak

Met deze verbeteringen kunnen gebruikers nu verwachten:

- Efficiënte en tijdige revisiecycli
- Minder handmatige inspanningen tijdens feedbackuitwisseling

Voor meer details, bekijk [ Inleiding aan overzicht ](../user-guide/review.md)

## Verbeterde ervaring voor het maken en gebruiken van DITAVAL-bestanden

Deze update introduceert verschillende verbeteringen die het maken, beheren en toepassen van DITAVAL-bestanden vereenvoudigen, waardoor u betere controle hebt over voorwaardelijke inhoud en stijlen voor verschillende uitvoerbestanden.

De belangrijkste hooglichten zijn:

- **Verbeterde het vlaggen steun in het ontwerpen van DITAVAL dossiers:** Experience Manager Guides brengt nieuwe mogelijkheden voor het aanpassen van de inhoud het publiceren door verbeterde het vlaggen steun in DITAVAL dossiers. U kunt nu begin- en eindmarkeringen toepassen rond specifieke inhoud, waaronder afbeeldingen, en secties met een vlag verrijken met opmaakopties zoals vet, cursief en meer. Om voorwaarde te behandelen overlapt, kan het **conflict van de Stijl** worden gevormd, dat het plaatsen van een standaardachtergrond en tekstkleur omvat, die duidelijkheid en consistentie in de output verzekeren. Deze markeringen worden volledig ondersteund in de native PDF-generatie en de resulterende uitvoer weerspiegelt op nauwkeurige en uitgebreide wijze alle toegepaste opmaakelementen.
Voor meer details, mening [ Gebruik de DITAVAL Redacteur ](../user-guide/ditaval-editor.md).

  ![](assets/ditaval-flag-style-new.png){width="350" align="left"}

- **veelvoudige DITAVAL dossiersteun voor Inheemse PDF:** voor Inheemse PDF, nu kunnen de veelvoudige DITAVAL dossiers worden toegevoegd, elk getoond als geëtiketteerde ingang voor gemakkelijke identificatie en verwijdering, die grotere flexibiliteit en controle over voorwaardelijke inhoud in de output van PDF verstrekken

  Bovendien verbetert deze update het maken van voorinstellingen voor uitvoer door bewerkbare DITAVAL-velden in verschillende indelingen in te schakelen, zodat gebruikers handmatig DITAVAL-paden kunnen opgeven.

  Voor meer details, begrijpt de mening [ de output vooraf instelt ](../user-guide/generate-output-understand-presets.md) in Experience Manager Guides.

## Verbeteringen voor publiceren

De volgende publicatieverbeteringen zijn doorgevoerd in het kader van de nieuwe release:

### Verbeterde logboekfiltering voor uitvoergeneratie

Deze versie brengt in verbeteringen UI aan het logboekfiltrerend vermogen van de outputgeneratie. U kunt de logboeken van de outputgeneratie nu beter voor alle vier verschillende niveaus filtreren; **Info**, **waarschuwen**, **Fout** (met inbegrip van zowel fouten als uitzonderingen), en **Fataal**; met betere en intuïtieve kleur-gecodeerde indicatoren die analyse en scherpte zichtbaarheid over de logboekstroom vereenvoudigen. Dankzij deze verbetering kunt u efficiënter door logbestanden navigeren en de kritieke problemen nauwkeurig opsporen.

Voor meer details, mening [ Basis het oplossen van problemen ](../user-guide/generate-output-basic-troubleshooting.md).

![](./assets/log-file-new.png){align="left"}


### Tijdelijke bestanden voor gepubliceerde uitvoer bevatten nu auteur- en publicatie-URL&#39;s in een nieuw configuratiebestand

De meest recente publicatieverbeteringen aan Experience Manager Guides voegen nu een nieuw `system_config.xml` -bestand toe aan de tijdelijke bestanden die worden gegenereerd tijdens het publiceren van HTML-, PDF- en JSON-uitvoerbestanden met behulp van DITA-OT en Native PDF-uitvoer. Dit dossier is automatisch inbegrepen in de het publiceren baan en ook toegankelijk door tijdelijke dossiers wanneer u **laat behouden tijdelijke dossiers** optie voor vooraf instelt en de output produceren.

Het bestand `system_config.xml` bevat AEM-instantiedetails, zoals de URL van de auteur, de lokale URL en de URL voor publiceren, die een duidelijkere context bieden en de traceerbaarheid van de gedownloade URL&#39;s verbeteren.

Voor meer details, begrijpt de mening [ de output vooraf instelt ](../user-guide/generate-output-understand-presets.md).

### Ondersteuning voor variabele uitvoerpaden voor het genereren van uitvoer

Deze update introduceert een dynamische `output path` configuratie voor uitvoervoorinstellingen zoals Native PDF, DITA-OT PDF, JSON, HTML5 en Aangepast. In plaats van een vast pad te gebruiken, kunnen gebruikers de uitvoerlocatie nu definiëren met de variabele `${base_output_path}` tijdens de installatie, wat meer flexibiliteit biedt. Het vorige standaardpad `/content/dam/fmdita-outputs` is niet langer verplicht.

Alle uitvoerpaden die zijn gekoppeld aan de algemene voorinstellingen van het mapprofiel worden automatisch gemigreerd om de nieuwe variabele van het basisuitvoerpad te gebruiken. Voor aangepaste omslagprofielen, echter, is de migratie niet automatisch; u wordt geadviseerd om het team van het Succes van de Klant voor hulp te contacteren.

Voor meer details, begrijpt de mening [ de output vooraf instelt ](../user-guide/generate-output-understand-presets.md).

### Geëxporteerde basislijn bevat nu de documentstatus

De eigenschap van de Basislijn van de Uitvoer omvat nu de **documentstaat** naast zeer belangrijke details zoals titel, dossiernaam, dossiertype, en versieaantal in de basislijnmomentopname. Deze verbetering verbetert het basislijnbeheer door een uitgebreider overzicht van de basislijn te verstrekken.

Voor meer details, leidt de mening [ basislijnen van de console van de Kaart ](../user-guide/web-editor-baseline.md#manage-baselines) tot en beheert.

### Ondersteuning voor incrementele publicatie op basislijn via kaartdashboard voor AEM Sites-uitvoer met behulp van toewijzing van oudere componenten

Het stijgende proces van de outputgeneratie is verbeterd om het publiceren specifieke versies van onderwerpen te steunen die in de geselecteerde basislijn voor de plaatsen van AEM worden bepaald gebruikend erfeniscomponentenafbeelding, die nauwkeurige propagatie van de inhoud in de output verzekeren.

Voor meer details, bekijk [ Incrementele outputgeneratie ](../user-guide/generate-output-aem-site.md).

## Verbeteringen in de Editor

De volgende verbeteringen in de Editor zijn doorgevoerd als onderdeel van de nieuwe versie:

### Verbeterde zoekervaring voor het deelvenster Herbruikbare inhoud

Experience Manager Guides introduceert een verbeterde zoekervaring in het deelvenster Herbruikbare inhoud. Bij deze update worden bij het zoeken naar trefwoorden nu alle bestanden gescand die zijn toegevoegd als herbruikbare inhoud, en niet alleen de geopende bestanden. Op deze manier kunt u de exacte positie van het trefwoord in alle gevallen vinden, ongeacht of de containers zijn geopend of samengevouwen. Wanneer u de zoekbalk wist, blijft bovendien de oorspronkelijke staat van alle containers behouden, wat een efficiëntere en gebruikersvriendelijkere zoekfunctionaliteit biedt.

Voor meer details, mening [ Herbruikbare inhoud ](../user-guide/web-editor-features.md#reusable-content).

### &#39;Format&#39;-kenmerk toegevoegd voor verwijzingskoppelingen

Adobe Experience Manager Guides voegt nu a **formaat** attributen voor verwijzingsverbindingen binnen de Redacteur toe. Dit attribuut wordt getoond in de **mening van Source** en wijst duidelijk op het dossiertype, zoals:

- Voor dossiers met a **.pdf** uitbreiding, zal het formaat aan **pdf** worden geplaatst
- Voor dossiers met a **.html** uitbreiding, zal het formaat aan **html** worden geplaatst
- Voor dossiers met a **.dita** of **&#x200B;**&#x200B;dossiers.ditamap, zal het formaat aan **dita** worden geplaatst

Bovendien, zullen de dossiers met a **.xml** uitbreiding ook hun formaat hebben dat aan **wordt geplaatst dita**. Voor bestanden zonder extensie blijft de indeling leeg. Voorts voor om het even welke verwijzingsverbindingen met een werkingsgebied dat aan **wordt geplaatst extern**, zal het formaat aan **html** ongeacht de dossieruitbreiding in de verwijzingsverbindingen worden geplaatst.

### Verbeterde opties voor kaartdownloaden in de Editor

Experience Manager Guides introduceert een nieuwe **Echte het dossiernamen van het Gebruik** optie in de **kaart van de Download** dialoog. Wanneer u nu kaartbestanden downloadt, kunt u ervoor kiezen de oorspronkelijke bestandsnamen te behouden in plaats van de standaard-UUID&#39;s, waardoor het veel eenvoudiger wordt om uw bestanden te herkennen en te beheren. Deze optie is slechts beschikbaar als u **selecteert behoud dossierhiërarchie** en gehandicapt wanneer u **kiest afvlakken dossierhiërarchie**, die u meer flexibiliteit geeft in het organiseren van uw gedownloade kaarten.

Voor meer details, mening [ dossiers van de Download ](../user-guide/authoring-download-assets.md#download-a-dita-map-file-from-the-editor).

![](assets/download-map-dialog-new.png){width="300" align="left"}

### Time-outmelding voor sessie om onbedoeld verlies van inhoud te voorkomen

Er verschijnt nu een pop-upbericht waarin u wordt gewaarschuwd wanneer uw Adobe Experience Manager-sessie verloopt en u bent afgemeld wegens inactiviteit. Dit bericht wordt geactiveerd wanneer u inhoud in Experience Manager Guides probeert te bewerken nadat de sessie is beëindigd. De functie helpt het risico op verlies van niet-opgeslagen werk te verminderen en verbetert de algehele betrouwbaarheid en vloeiendheid van de ervaring, zelfs tijdens perioden van inactiviteit.

![](assets/sign-out-prompt.png)

Leer meer over [ herinnering van de zittingsonderbreking ](../user-guide/session-timeout-prompt.md) in Experience Manager Guides.

### Verbeterde `navref` afhandeling in de Editor

De meest recente verbeteringen aan de Editor verbeteren de verwerking van `navref` -elementen in een DITA-kaart. Nu, wanneer u een `navref` element aan een kaart toevoegt, opent de **Uitgezochte weg** dialoog, toestaand u om de kaartverwijzingen gemakkelijk te kiezen om als navigatiekoppelingen in uw kaart te omvatten. Nadat de titel van de toegevoegde kaart is toegevoegd, wordt deze zowel in de ontwerpweergave als in de layoutweergave weergegeven, zodat de opgenomen navigatie tijdens het ontwerpen beter zichtbaar is.  Bovendien wordt het toegevoegde `navref` -element automatisch omgezet om de doorverwezen kaart in de Editor weer te geven.

Voor meer details, voegt de mening [ navigatieverwijzingen ](../user-guide/map-editor-other-features.md#add-navigation-references) toe.


### UI-verbeteringen op de werkbalk van de Editor en gebruikersvoorkeuren

Met deze versie zijn de montages binnen de **voorkeur van de Gebruiker** op de Homepage voor Algemene en de lusjes van de Verschijning re-gestructureerd. Het omvat het anders noemen van het etiket **Openende voorkeur voor Kaarten** en het bewegen van de Vaste spaties knevel aan de toolbar van de Redacteur.

Bovendien, in de toolbar van de Redacteur worden sommige snel-toegangsknevels voor het toelaten van of het onbruikbaar maken van de Veranderingen van het Spoor, de Markeringen, en de niet-BreakSpaties nu gegroepeerd onder **toon** optie binnen dropdown van het Menu voor betere bruikbaarheid.

Voor meer details, mening [ Toolbar in de Redacteur ](../user-guide/web-editor-toolbar.md#menu-dropdown).







