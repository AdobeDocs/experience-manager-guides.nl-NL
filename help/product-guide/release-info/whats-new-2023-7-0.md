---
title: Opmerkingen bij de release | Nieuwe functies in Adobe Experience Manager Guides, release juli 2023
description: Leer de nieuwe en verbeterde functies in de release van Adobe Experience Manager Guides as a Cloud Service van juli 2023
exl-id: 4b907729-4fbf-48ed-a2e1-014bd1101c73
feature: What's New
role: Leader
source-git-commit: 7d0ae0f13ab77a10beb89fcb0d8592b05c3828bd
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Nieuwe functies in juli 2023 release van Adobe Experience Manager Guides as a Cloud Service

Dit artikel behandelt de nieuwe en verbeterde eigenschappen in versie Juli 2023 van Adobe Experience Manager Guides (later die als *wordt bedoeld as a Cloud Service van AEM Guides*).

Voor meer details op de verbeteringsinstructies, verenigbaarheidsmatrijs, en de kwesties die in deze versie worden bevestigd, zie [&#x200B; de nota&#39;s van de Versie &#x200B;](release-notes-2023-7-0.md).

## Verbind met een gegevensbron en neem gegevens in uw onderwerpen op

Nu kunt u snel verbinding maken met uw gegevensbronnen via kant-en-klare connectors uit AEM Guides. Door verbinding te maken met een gegevensbron, kunt u uw informatie synchroon houden met de bron. Updates van de gegevens worden automatisch weerspiegeld, waardoor AEM Guides een echte inhoudshub wordt. Met deze functie bespaart u tijd en moeite om de gegevens handmatig toe te voegen of te kopiëren.

Nu, staat AEM Guides uw beheerder toe om de uit-van-de-doosschakelaars voor JIRA en SQL (MySQL, PostgreSQL, SQL Server, SQLite) gegevensbestanden te vormen. Zij kunnen andere schakelaars ook toevoegen door de standaardinterfaces uit te breiden.

Zodra toegevoegd, kunt u de gevormde schakelaars bekijken die onder het **paneel van Gegevensbronnen** in de Redacteur van het Web worden vermeld.

![](assets/code-snippet-generator.png){width="300" align="left"}

U kunt een inhoudsfragmentgenerator tot stand brengen om de gegevens van een verbonden gegevensbron te halen. U kunt de gegevens in uw onderwerpen dan opnemen en het uitgeven.

Zodra u een inhoudsfragmentgenerator hebt gecreeerd, kunt u het opnieuw gebruiken om de gegevens in om het even welk onderwerp op te nemen. Voor meer details, neemt de mening [&#x200B; een inhoudsfragment van uw gegevensbron &#x200B;](../user-guide/web-editor-content-snippet.md) op.



## Deelvenster Controleren om revisieprojecten en de actieve revisietaken te presenteren

Nu maakt AEM Guides uw revisies naadloos. Het biedt het deelvenster Revisies in de webeditor. In het deelvenster Revisies worden alle revisieprojecten en de actieve revisietaken weergegeven in de revisieprojecten die u maakt.

Als auteur kunt u met deze functie gemakkelijk de revisietaken openen, de opmerkingen bekijken en de opmerkingen snel in een gecentraliseerde weergave adresseren.
![](assets/active-review-task-comments.png){width="800" align="left"}
Voor meer details, bekijk de **2&rbrace; eigenschapbeschrijving van het Overzicht &lbrace;binnen de** Linkerpaneel [&#x200B; sectie.](../user-guide/web-editor-features.md#id2051EA0M0HS)


## Verbeteringen voor kaartverzameling

Met een kaartverzameling kunt u meerdere toewijzingen ordenen en in batches publiceren. Er zijn veel nieuwe verbeteringen aangebracht in de kaartverzameling:

- Nu kunt u ook native PDF-uitvoervoorinstellingen toevoegen aan een kaartverzameling en deze gebruiken om de PDF-uitvoer te genereren.
- U kunt de algemene voorinstellingen en voorinstellingen van het mapprofiel die door uw beheerder zijn gemaakt, weergeven en deze gebruiken om de PDF-uitvoer te genereren.
- U kunt nu niet alleen een individuele voorinstelling selecteren, maar u kunt ook alle voorinstellingen voor het mapprofiel voor een DITA-kaart in één keer inschakelen.
  ![](assets/edit-map-collection.png){width="800" align="left"}

Voor meer details, mening [&#x200B; de Inzameling van de Kaart van het Gebruik voor outputgeneratie &#x200B;](../user-guide/generate-output-use-map-collection-output-generation.md).

## Mogelijkheid om toegang te krijgen tot tijdelijke HTML-bestanden terwijl de native PDF-uitvoer wordt gegenereerd

Nu kunt u met AEM Guides de tijdelijke HTML-bestanden downloaden die zijn gemaakt tijdens het genereren van de eigen PDF-uitvoer. Selecteer in de instellingen van de uitvoervoorinstelling de optie om de tijdelijke bestanden te downloaden.  In AEM Guides kunt u vervolgens de tijdelijke bestanden downloaden die zijn gemaakt tijdens het genereren van de uitvoer met behulp van die voorinstelling.

Met deze functie krijgt u meer inzicht in het generatieproces dankzij toegang tot tussentijdse stijlen en lay-outs en kunt u uw CSS-stijlen naar wens corrigeren of wijzigen.

![](assets/native-pdf-advanced-settings.png){width="800" align="left"}

Voor meer details, mening [&#x200B; creeer een de uitvoervooraf ingestelde PDF &#x200B;](../web-editor/native-pdf-web-editor.md#create-output-preset).

## Op microservices gebaseerde publicaties om HTML5 en aangepaste uitvoer te genereren

Met de nieuwe publicatiemicroservice kunt u grote publicatiewerklasten tegelijkertijd uitvoeren op AEM Guides as a Cloud Service en het toonaangevende Adobe I/O Runtime-serverloze platform benutten. Nu u de microservice gebruikt, kunt u ook de HTML5 en de aangepaste uitvoer genereren.
U kunt meerdere publicatieverzoeken uitvoeren en de prestaties verbeteren om deze uitvoerindelingen te genereren.
Voor meer details, vorm de mening [&#x200B; microservice-based het publiceren voor AEM Guides as a Cloud Service &#x200B;](../knowledge-base/publishing/configure-microservices.md).

## AEM Guides-versiedetails weergeven in het venster Info

Nu samen met AEM **Ongeveer** informatie, kunt u de versiedetails van AEM Guides ook bekijken. U kunt de huidige versiedetails in de **Ongeveer** optie van de **Hulp** op de pagina van de Navigatie van AEM bekijken.

![](assets/about-aem-help.png){width="800" align="left"}
