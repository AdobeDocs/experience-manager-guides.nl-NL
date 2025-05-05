---
title: Opmerkingen bij de release | Nieuwe functies in de Adobe Experience Manager Guides, release november 2023
description: Leer de nieuwe en verbeterde functies in de release van Adobe Experience Manager Guides as a Cloud Service van november 2023.
exl-id: 83c04e01-92f1-41b0-8866-a202f4106b51
feature: What's New
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '803'
ht-degree: 0%

---

# Nieuwe functies in de release van Adobe Experience Manager Guides as a Cloud Service van november 2023

Dit artikel behandelt de nieuwe en verbeterde eigenschappen in versie November 2023 van Adobe Experience Manager Guides (later die als *wordt bedoeld Experience Manager Guides as a Cloud Service*).

Voor meer details op de verbeteringsinstructies, verenigbaarheidsmatrijs, en de kwesties die in deze versie worden bevestigd, mening [ de nota&#39;s van de Versie ](release-notes-2023-11-0.md).

## Native PDF-verbeteringen

De volgende Native PDF-verbeteringen zijn uitgevoerd in de release van november 2023:

### PDF-sjablonen buiten de box gebruiken en dupliceren

Experience Manager Guides beschikt over out-of-the-box of factory PDF templates. Dupliceer de PDF sjablonen van de factory om de aangepaste PDF-sjablonen te maken.

U kunt nu ook een voorbeeld van de miniatuurafbeelding voor een sjabloon bekijken terwijl u een sjabloon maakt en dupliceert. U kunt deze afbeelding ook bewerken of verwijderen. Deze functie is handig voor het brandmerken of het onderscheiden van sjablonen met vergelijkbare namen.
Leer meer over het [ malplaatje van de PDF ](../native-pdf/pdf-template.md).

![ Duplicate de malplaatjedialoog van PDF ](assets/duplicate-template.png){width="550" align="left"}

*dupliceer een bestaand malplaatje van PDF.*


### De volgorde van pagina&#39;s wijzigen en meerdere pagina&#39;s per vel publiceren

Naast het publiceren van de pagina&#39;s volgens het brondocument, kunt u ook de volgorde van pagina&#39;s in PDF wijzigen terwijl u een document met meerdere pagina&#39;s publiceert.  Dit biedt u de flexibiliteit om de pagina&#39;s in verschillende volgorden, zoals alle oneven, of alle even pagina&#39;s eerst te publiceren. U kunt de pagina&#39;s ook als een boek publiceren en lezen. U kunt ook het aantal pagina&#39;s bepalen dat u op één vel papier wilt publiceren. Voor meer details, bekijk de [&#128279;](../native-pdf/components-pdf-template.md#page-organization) sectie van de Organisatie van de Pagina 0&rbrace; &lbrace;.

### Woordenlijsttermen sorteren op basis van sorteersleutels

U kunt nu ook de woordenlijsttermen sorteren op basis van de sorteertoetsen. U kunt de tag &#39;sort-as&#39; gebruiken om een sorteersleutel voor de termen in de woordenlijst te definiëren. Vervolgens kunt u de termen sorteren op sorteertoetsen in plaats van op termen. Op deze manier kunt u de termen in de woordenlijst sorteren op basis van termen die in verschillende talen worden gebruikt. U kunt ook één sorteersleutel definiëren voor een woordenlijstterm met een woordgroep of woordgroep.
Voor meer details, bekijk de [ Geavanceerde Montages van de PDF ](../native-pdf/components-pdf-template.md#advanced-pdf-settings).


### Verbeterd resourcebeheer voor Native PDF-sjablonen

Experience Manager Guides heeft nu het beheer van bronnen voor Native PDF-sjablonen verbeterd. U kunt nu bronnen, zoals afbeeldingen, CSS-bestanden en lettertypebestanden, delen en opnieuw gebruiken voor meerdere Native PDF-sjablonen. Met deze verbetering, is het beheren van de middelen voor een grote reeks malplaatjes veel eenvoudiger. U hoeft geen dubbele bronnen voor elke sjabloon te maken en u kunt deze in een gedeelde map bewaren en ze in alle Native PDF-sjablonen gebruiken.
Voor meer details, bekijk [ Malplaatje van PDF ](../native-pdf/pdf-template.md).

## Verbeteringen in de webeditor

De volgende verhogingen van de Redacteur van het Web zijn gedaan in de versie van november 2023:


### Bestanden weergeven op titel of bestandsnamen

U kunt nu de standaardmanier kiezen om de bestanden weer te geven in de webeditor. U kunt de lijst met bestanden weergeven op basis van de titels of de bestandsnamen in de verschillende deelvensters in de weergave Auteur.

![ de dialoog van de Voorkeur van de Gebruiker ](assets/user-preferences-2311.png){width="550" align="left"}

*verander de standaardmanier om de dossiers van de **2&rbrace; dialoog van de Voorkeur van de Gebruiker te bekijken.***


### Voorinstellingen voor voorwaarden beheren

U kunt voorwaardenattributen in uw onderwerpen bepalen DITA. Gebruik vervolgens de voorwaardelmerken in de voorinstelling voor voorwaarde om de inhoud in een DITA-kaart te publiceren. Met Experience Manager Guides kunt u nu ook voorinstellingen voor voorwaarden maken en beheren in de webeditor. U kunt ze ook gemakkelijk bewerken, dupliceren of verwijderen.

![ Voorinstellingen voor voorwaarde van het tabblad Beheren van de webeditor ](assets/web-editor-manage-condition-presets.png){width="550" align="left"}

Voor meer details, vooraf instelt van het menings[ Gebruik voorwaarde ](../user-guide/generate-output-use-condition-presets.md).

### Bestandstabbladen herstellen bij vernieuwen van browser

Experience Manager Guides herstelt de staat van de geopende dossierlusjes in de Redacteur van het Web wanneer u browser vernieuwt. Voor meer details, bekijk **verfrissen browser terwijl het uitgeven van de dossiers** sectie onder [ onderwerpen in de Redacteur van het Web ](../user-guide/web-editor-edit-topics.md) uitgeeft.

### Eenvoudig een element opheffen

Nu kunt u een element gemakkelijk ontkoppelen gebruikend de optie van het contextmenu van een element in de Redacteur van het Web. Hierdoor kunt u de tekst van het element gemakkelijk samenvoegen met het bovenliggende element.
Voor meer details, bekijk **Unwrap een element** sectie van de [ andere eigenschappen in de Redacteur van het Web ](../user-guide/web-editor-other-features.md).

### Sneltoetsen om de cursor te verplaatsen

Experience Manager Guides staat u nu ook toe om toetsenbordkortere weg te gebruiken om de curseur in de Redacteur van het Web te bewegen. Met de sneltoetsen kunt u snel één woord naar links of rechts verplaatsen. U kunt ook naar het begin of einde van de regel gaan met behulp van de sneltoetsen.
Nu kunt u ook sneltoetsen gebruiken om de cursor naar het begin van het volgende element of naar het einde van het vorige element te verplaatsen.
Leer meer over de [ toetsenbordkortere weg in de Redacteur van het Web ](../user-guide/web-editor-keyboard-shortcuts.md).
