---
title: Opmerkingen bij de release | Nieuwe functies in Adobe Experience Manager Guides 4.3.1-release
description: Meer informatie over de nieuwe en verbeterde functies in 4.3.1-releases van Adobe Experience Manager Guides
exl-id: 14db7453-ccc1-4709-903f-677f55c263b2
feature: What's New
role: Leader
source-git-commit: 5a444e88b0adba7fa3d498437df39b729b10b5eb
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%

---

# Nieuwe functies in de release 4.3.1 van Adobe Experience Manager Guides (oktober 2023)

Dit artikel behandelt de nieuwe en verbeterde eigenschappen in versie 4.3.1 van Adobe Experience Manager Guides (later die als *wordt bedoeld Experience Manager Guides*).

Voor meer details op de verbeteringsinstructies, verenigbaarheidsmatrijs, en de kwesties die in deze versie worden bevestigd, zie [ de nota&#39;s van de Versie ](./release-notes-4-3-1.md).

## Verbind met een gegevensbron en neem de onderwerpen op

Experience Manager Guides biedt kant-en-klare connectors die u helpen verbinding te maken met uw gegevensbronnen, waardoor Experience Manager Guides een echte inhoudhub wordt. Dit geeft u het voordeel om u tijd en inspanning te besparen die anders aan handgegevenstoevoeging of replicatie zouden worden besteed.

Samen met de bestaande uit-van-de-doos schakelaars zoals JIRA en SQL (MySQL, PostgreSQL, SQL Server, SQLite), kan uw beheerder schakelaars voor MariaDB, H2DB, de Uitwisseling van Adobe, en de gegevensbestanden van de Elasticsearch ook vormen. Zij kunnen andere schakelaars ook toevoegen door de standaardinterfaces uit te breiden.

U kunt de gevormde schakelaars onder het **paneel van Gegevensbronnen** in de Redacteur van het Web bekijken.

<img src="assets/data-sources.png" alt="Lijst met gegevensbronnen in het deelvenster" width="300">

*Mening de verbonden gegevensbronnen.*

U kunt nu ook een onderwerp van een verbonden gegevensbron tot stand brengen. Een onderwerp kan gegevens in diverse formaten, zoals lijsten, lijsten, en paragrafen bevatten. Het staat u ook toe om een kaart DITA voor alle onderwerpen tot stand te brengen. U kunt meta-gegevens aan het onderwerp associëren wanneer het trekken uit een gegevensbron.

Voor meer details, mening [ Gegevens van het Gebruik van uw gegevensbron ](../user-guide/web-editor-content-snippet.md).

## Vorm een gegevensbronschakelaar van het gebruikersinterface

Experience Manager Guides verstrekt nu ook a **Gegevensbronnen** hulpmiddel dat u uit-van-de-doosschakelaars voor gegevensbronnen helpt vormen. U kunt de schakelaars voor JIRA, SQL (MySQL, PostgreSQL, de Server van Microsoft SQL, SQLite, MariaDB, H2DB), de gegevensbestanden van de Handel van Adobe, en van de Elasticsearch gemakkelijk tot stand brengen.

U kunt ook gemakkelijk een gegevensbronaansluiting bewerken, opnieuw verbinden, dupliceren of verwijderen. Leer meer over hoe te [ gemakkelijk een gegevensbronschakelaar van het gebruikersinterface ](../install-guide/conf-data-source-connector-tools.md) vormen.

![ gegevensbronschakelaars die in het paneel van gegevensbronnen ](assets/data-sources-create-window.png){width="550" align="left"} worden vermeld

*creeer en bekijk de gegevensbronschakelaars van het paneel van gegevensbronnen.*

## Logboeken van de mening voor de onderwerpgenerator

U kunt nu ook het logbestand voor het genereren van inhoud weergeven. Met dit logbestand kunt u de waarschuwingen, fouten en uitzonderingen controleren.  Leer meer over hoe de [ opties voor een onderwerpgenerator ](../user-guide/web-editor-content-snippet.md#options-for-a-topic-generator) u gemakkelijk de onderwerpgenerators produceren en beheren.

## Ondersteuning voor snelheidsgereedschappen in de gegevensbronsjablonen

U kunt nu de snelheidshulpmiddelen gebruiken in de Experience Manager Guides-sjablonen. Met deze gereedschappen kunt u verschillende functies toepassen op de gegevens die u ophaalt van de gegevensbronnen. U kunt de sjablonen gebruiken tijdens het maken van een inhoudsfragment of onderwerp. Met deze functie bespaart u tijd en moeite om handmatig dezelfde functie toe te passen op elke gegevensset.  Het zorgt ook voor nauwkeurige resultaten.
U kunt bijvoorbeeld het gereedschap $mathTool gebruiken om wiskundige functies uit te voeren.
Leer meer over hoe te [ de hulpmiddelen van de gebruiksSnelheid in de gegevensbronmalplaatjes ](../user-guide/web-editor-content-snippet.md#use-velocity-tools).


## Native PDF-verbeteringen

De volgende Native PDF-verbeteringen zijn doorgevoerd in de release van oktober 2023:

### Het paginanummer van de eerste pagina van een lay-out opnieuw instellen

In de native PDF-uitvoer kunt u de paginanummers opnieuw starten en het nummer opgeven waaruit de nummering begint. Nu kunt u de nummering ook alleen starten voor het eerste exemplaar van een sectie.
Leer meer over hoe te [ met de paginaeigenschappen van een paginalay-out ](../native-pdf/design-page-layout.md#page-props-page-layout) werken.


### Hoofdstukken weergeven zonder automatische nummers in de inhoudsopgave

Experience Manager Guides geeft de hoofdstuknummers weer samen met de hoofdstuknamen in de inhoudsopgave. Nu kunt u verkiezen om slechts de hoofdstuknamen zonder de hoofdstukaantallen te publiceren. Bekijk meer details over hoe te om de [ geavanceerde PDF montages van een malplaatje ](../native-pdf/components-pdf-template.md#advanced-pdf-settings) te vormen.

## Een kaart downloaden vanuit de webeditor

Nu kunt u niet alleen een kaart in de kaartweergave van de Redacteur van het Web uitgeven maar ook het downloaden. U kunt de kaart downloaden met een specifieke basislijn. U kunt de hiërarchie ook afvlakken en alle bestanden en mappen in één map opslaan.

Voor meer details, verwijs naar de **eigenschapbeschrijving van de Mening van de Kaart** {binnen de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

![ optiemenu van een dossier in de mening van de bewaarplaats ](assets/options-menu-repo-view-file-level-2310.png){width="550" align="left"}

*selecteer een dossier in bewaarplaats mening en kies de optie om een actie op het dossier uit te voeren.*


## Ondersteuning van meerdere onderwerpdefinities in één opsommingsdefinitie

U kunt nu een of meer onderwerpdefinities definiëren in een kaart en de opsommingsdefinities in een andere kaart en vervolgens de kaartverwijzing toevoegen. De verwijzingen naar onderwerpopsommingen worden opgelost in dezelfde kaart of in de kaart waarnaar wordt verwezen.

U kunt nu ook voorwaarden definiëren en deze toepassen op bepaalde specifieke elementen in een onderwerp.  De voorwaarden zijn alleen zichtbaar voor die specifieke elementen en niet voor alle andere elementen.

Voor meer details op de behandeling hiërarchische definities van onderwerpdefinities en opsommingen, bekijk de beschrijving van de onderwerpschemaeigenschap in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.




## Verbeterde voorvertoning via het contextmenu

Gebruik het contextmenu om snel een voorvertoning van het bestand weer te geven (.dita, .xml, audio, video of afbeelding) zonder het te openen. U kunt nu het formaat van het voorvertoningsvenster wijzigen. Als de inhoud een referentiekoppeling bevat, kunt u het venster selecteren en openen op een nieuw tabblad.

![ Het deelvenster Voorvertoning ](assets/quick-preview_cs.png){width="800" align="left"}

*voorproef het dossier in de ruit.*

Voor meer details op het contextmenu, zie de **Opties voor een dossier** eigenschapbeschrijving in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

## Een bestand bewerken in de plug-in voor de zuurstofaansluiting

In Experience Manager Guides kunt u nu een bestand selecteren in de webeditor en het bestand vervolgens bewerken in de insteekmodule Oxygen-connector. Deze optie wordt niet ingeschakeld als onderdeel van de out-of-the-box ondersteuning.

Voor meer details, verwijs naar de **Opties voor een dossier** eigenschapbeschrijving binnen de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

## Variabelen voor huidige datum en tijd gebruiken in de opties Doelpad, Sitenaam of Bestandsnaam

Terwijl het produceren van output in AEM Plaats of PDF, kunt u variabelen gebruiken voor het plaatsen van de **Weg van de Bestemming**, **Naam van de Plaats**, of **Naam van het Dossier** opties. U kunt nu ook de variabelen `${system_date}` en `${system_time}` gebruiken. Met deze variabelen kunt u de huidige datum en tijd aan deze opties toevoegen.

Leer hoe te [ gebruikvariabelen voor het plaatsen van de Weg van de Bestemming, de Naam van de Plaats, of de opties van de Naam van het Dossier ](../user-guide/generate-output-use-variables.md).


## Sneltoetsen om de cursor in de webeditor te verplaatsen

Experience Manager Guides staat u nu ook toe om toetsenbordkortere weg te gebruiken om de curseur in de Redacteur van het Web te bewegen. Met de sneltoetsen kunt u snel één woord naar links of rechts verplaatsen. U kunt ook naar het begin of einde van de regel gaan met behulp van de sneltoetsen.

Leer meer over de [ toetsenbordkortere weg in de Redacteur van het Web ](../user-guide/web-editor-keyboard-shortcuts.md).
