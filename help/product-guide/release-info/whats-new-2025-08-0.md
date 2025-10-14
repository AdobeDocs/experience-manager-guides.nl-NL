---
title: Opmerkingen bij de release | Nieuwe functies in de Adobe Experience Manager Guides 2025.08.0-release
description: Meer informatie over de nieuwe en verbeterde functies in de 2025.08.0-release van Adobe Experience Manager Guides
role: Leader
exl-id: c3461d0a-6394-4275-9d54-b2b1545d7c18
source-git-commit: 1a44af3522060ebc531393d4d01b1cd00eb02c10
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# Nieuwe functies in de release van 2025.08.0 (augustus 2025)

Dit artikel behandelt de nieuwe en verbeterde functies die zijn geïntroduceerd met de release 2025.08.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor de lijst van kwesties die in deze versie worden bevestigd, mening [&#x200B; Vaste kwesties in de versie 2025.08.0 &#x200B;](fixed-issues-2025-08-0.md).

Leer over [&#x200B; verbeteringsinstructies voor de versie 2025.08.0 &#x200B;](../release-info/upgrade-instructions-2025-08-0.md).


## Verbeterde revisieworkflow

Met deze release is de revisieworkflow aanzienlijk verbeterd en is de communicatie tussen auteurs en revisoren verbeterd. Belangrijke updates zijn:

- Workflows voor taakbeheer met meldingen die kunnen worden uitgevoerd
- Mogelijkheid om gebruikers te voorzien van tags om onmiddellijk aandacht te vragen
- Toegang tot project- en taakdetails vanuit het deelvenster Review voor gebruiksgemak

Met deze verbeteringen kunnen gebruikers nu verwachten:

- Efficiënte en tijdige revisiecycli
- Minder handmatige inspanningen tijdens feedbackuitwisseling

Voor meer details, bekijk [&#x200B; Inleiding aan overzicht &#x200B;](../user-guide/review.md)

## Configureerbare AI Assistant-handelingen in de Editor-instellingen

De recentste update introduceert verbeterde configuratie voor **Authoring snelle acties** in AI Medewerker, die Beheerders machtigt om het auteursmilieu volgens specifieke werkschema&#39;s en voorkeur aan te passen.

Zodra de **AI Medewerker** knevel wordt toegelaten, kunnen de Beheerders kiezen welke snelle acties onder het **Authoring** lusje zichtbaar zijn, die auteursinteractie helpen stroomlijnen. Deze zichtbaarheidsinstellingen gelden specifiek voor elk mapprofiel.

Leer meer over [&#x200B; AI medewerker in de montages van de Redacteur &#x200B;](../cs-install-guide/workspace-settings.md#general) in Experience Manager Guides.

![](assets/authoring-quick-actions.png){width="350" align="left"}


## Verbeterde ervaring voor het maken en gebruiken van DITAVAL-bestanden

Deze update introduceert verschillende verbeteringen die het maken, beheren en toepassen van DITAVAL-bestanden vereenvoudigen, waardoor u betere controle hebt over voorwaardelijke inhoud en stijlen voor verschillende uitvoerbestanden.

De belangrijkste hooglichten zijn:

- **Verbeterde het vlaggen steun in het ontwerpen van DITAVAL dossiers:** Experience Manager Guides brengt nieuwe mogelijkheden voor het aanpassen van de inhoud het publiceren door verbeterde het vlaggen steun in DITAVAL dossiers. U kunt nu begin- en eindmarkeringen toepassen rond specifieke inhoud, waaronder afbeeldingen, en secties met een vlag verrijken met opmaakopties zoals vet, cursief en meer. Om voorwaarde te behandelen overlapt, kan het **conflict van de Stijl** worden gevormd, dat het plaatsen van een standaardachtergrond en tekstkleur omvat, die duidelijkheid en consistentie in de output verzekeren. Deze markeringen worden volledig ondersteund in de native PDF-generatie en de resulterende uitvoer weerspiegelt op nauwkeurige en uitgebreide wijze alle toegepaste opmaakelementen.
Voor meer details, mening [&#x200B; Gebruik de DITAVAL Redacteur &#x200B;](../user-guide/ditaval-editor.md).

  ![](assets/ditaval-flag-style-new.png){width="350" align="left"}

- **veelvoudige DITAVAL dossiersteun voor Inheemse PDF:** voor Inheemse PDF, nu kunnen de veelvoudige DITAVAL dossiers worden toegevoegd, elk getoond als geëtiketteerde ingang voor gemakkelijke identificatie en verwijdering, die grotere flexibiliteit en controle over voorwaardelijke inhoud in de output van PDF verstrekken

  Bovendien verbetert deze update het maken van voorinstellingen voor uitvoer door bewerkbare DITAVAL-velden in verschillende indelingen in te schakelen, zodat gebruikers handmatig DITAVAL-paden kunnen opgeven.

  Voor meer details, begrijpt de mening [&#x200B; de output vooraf instelt &#x200B;](../user-guide/generate-output-understand-presets.md) in Experience Manager Guides.

## Verbeterde logboekfiltering voor uitvoergeneratie

Deze versie brengt in verbeteringen UI aan het logboekfiltrerend vermogen van de outputgeneratie. U kunt de logboeken van de outputgeneratie nu beter voor alle vier verschillende niveaus filtreren; **Info**, **waarschuwen**, **Fout** (met inbegrip van zowel fouten als uitzonderingen), en **Fataal**; met betere en intuïtieve kleur-gecodeerde indicatoren die analyse en scherpte zichtbaarheid over de logboekstroom vereenvoudigen. Dankzij deze verbetering kunt u efficiënter door logbestanden navigeren en de kritieke problemen nauwkeurig opsporen.

Voor meer details, mening [&#x200B; Basis het oplossen van problemen &#x200B;](../user-guide/generate-output-basic-troubleshooting.md).

![](./assets/log-file-new.png){align="left"}


## Tijdelijke bestanden voor gepubliceerde uitvoer bevatten nu auteur- en publicatie-URL&#39;s in een nieuw configuratiebestand

De meest recente publicatieverbeteringen aan Experience Manager Guides voegen nu een nieuw `system_config.xml` -bestand toe aan de tijdelijke bestanden die worden gegenereerd tijdens het publiceren van HTML-, PDF- en JSON-uitvoerbestanden met behulp van DITA-OT en Native PDF-uitvoer. Dit dossier is automatisch inbegrepen in de het publiceren baan en ook toegankelijk door tijdelijke dossiers wanneer u **laat behouden tijdelijke dossiers** optie voor vooraf instelt en de output produceren.

Het bestand `system_config.xml` bevat AEM-instantiedetails, zoals de URL van de auteur, de lokale URL en de URL voor publiceren, die een duidelijkere context bieden en de traceerbaarheid van de gedownloade URL&#39;s verbeteren.

Voor meer details, begrijpt de mening [&#x200B; de output vooraf instelt &#x200B;](../user-guide/generate-output-understand-presets.md).

## Ondersteuning voor variabele uitvoerpaden voor het genereren van uitvoer

Deze update introduceert een dynamische `output path` configuratie voor uitvoervoorinstellingen zoals Native PDF, DITA-OT PDF, JSON, HTML5 en Aangepast. In plaats van een vast pad te gebruiken, kunnen gebruikers de uitvoerlocatie nu definiëren met de variabele `${base_output_path}` tijdens de installatie, wat meer flexibiliteit biedt. Het vorige standaardpad `/content/dam/fmdita-outputs` is niet langer verplicht.

Alle uitvoerpaden die zijn gekoppeld aan de algemene voorinstellingen van het mapprofiel worden automatisch gemigreerd om de nieuwe variabele van het basisuitvoerpad te gebruiken. Voor aangepaste omslagprofielen, echter, is de migratie niet automatisch; u wordt geadviseerd om het team van het Succes van de Klant voor hulp te contacteren.

Voor meer details, begrijpt de mening [&#x200B; de output vooraf instelt &#x200B;](../user-guide/generate-output-understand-presets.md).

## UI-verbeteringen op de werkbalk van de Editor en gebruikersvoorkeuren

Met deze versie zijn de montages binnen de **voorkeur van de Gebruiker** op de Homepage voor Algemene en de lusjes van de Verschijning re-gestructureerd. Het omvat het anders noemen van het etiket **Openende voorkeur voor Kaarten** en het bewegen van de Vaste spaties knevel aan de toolbar van de Redacteur.

Bovendien, in de toolbar van de Redacteur worden sommige snel-toegangsknevels voor het toelaten van of het onbruikbaar maken van de Veranderingen van het Spoor, de Markeringen, en de niet-BreakSpaties nu gegroepeerd onder **toon** optie binnen dropdown van het Menu voor betere bruikbaarheid.

Voor meer details, mening [&#x200B; Toolbar in de Redacteur &#x200B;](../user-guide/web-editor-toolbar.md#menu-dropdown).
