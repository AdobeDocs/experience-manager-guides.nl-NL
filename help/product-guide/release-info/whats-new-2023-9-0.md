---
title: Opmerkingen bij de release | Nieuwe functies in Adobe Experience Manager Guides, release september 2023
description: Leer de nieuwe en verbeterde functies in de release van Adobe Experience Manager Guides as a Cloud Service van september 2023
exl-id: d185d27f-0cbb-4ec6-ac65-cb69f7572c3f
feature: What's New
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 0%

---

# Nieuwe functies in de release van Adobe Experience Manager Guides as a Cloud Service van september 2023

Dit artikel behandelt de nieuwe en verbeterde eigenschappen in versie September 2023 van Adobe Experience Manager Guides (later die als *wordt bedoeld AEM Guides as a Cloud Service*).

Voor meer details op de verbeteringsinstructies, verenigbaarheidsmatrijs, en de kwesties die in deze versie worden bevestigd, zie [ de nota&#39;s van de Versie ](release-notes-2023-9-0.md).

## Verbind met een gegevensbron en neem de onderwerpen op

AEM Guides biedt kant-en-klare connectors die u helpen verbinding te maken met uw gegevensbronnen, waardoor AEM Guides een echte inhoudhub wordt. Dit geeft u het voordeel om u tijd en inspanning te besparen die anders aan handgegevenstoevoeging of replicatie zouden worden besteed.

Samen met de bestaande uit-van-de-doos schakelaars zoals JIRA en SQL (MySQL, PostgreSQL, SQL Server, SQLite), kan uw beheerder schakelaars voor MariaDB, H2DB, de Uitwisseling van Adobe, en de gegevensbestanden van de Elasticsearch ook vormen. Zij kunnen andere schakelaars ook toevoegen door de standaardinterfaces uit te breiden.

U kunt de gevormde schakelaars onder het **paneel van Gegevensbronnen** in de Redacteur van het Web bekijken.

<img src="assets/data-sources.png" alt="Lijst met gegevensbronnen in het deelvenster" width="300">

*Mening de verbonden gegevensbronnen.*

U kunt nu ook een onderwerp van een verbonden gegevensbron tot stand brengen. Een onderwerp kan gegevens in diverse formaten, zoals lijsten, lijsten, en paragrafen bevatten. Het staat u ook toe om een kaart DITA voor alle onderwerpen tot stand te brengen. U kunt meta-gegevens aan het onderwerp associëren wanneer het trekken uit een gegevensbron.

Voor meer details, mening [ Gegevens van het Gebruik van uw gegevensbron ](../user-guide/web-editor-content-snippet.md).

## citaten toevoegen aan uw inhoud

Bijschriften zijn verwijzingen naar de informatiebron die aan de inhoud is toegevoegd. Met uitnodigingen kunt u uw geloofwaardigheid herstellen en plagiaat voorkomen. Met uitnodigingen kunnen de lezers de bron vinden en de informatie in de tekst controleren.

In AEM Guides kunt u citaten toevoegen of citaten importeren en deze op de inhoud toepassen. U kunt deze citaten toevoegen vanuit elke bron van boeken, websites en tijdschriften.

Na het opnemen van uw citaten aan uw onderwerpen, kunt u voorproef hen in de Redacteur van het Web. U kunt inhoud met citaten ook publiceren gebruikend Eigen PDF.

![ Bevelen die in een paneel ](assets/citation-panel.png){width="300" align="left"} worden vermeld

*Mening de lijst van citaten in het paneel van Bevelingen.*

Voor meer details, voegt de mening [ toe en beheert citaties in uw inhoud ](../user-guide/web-editor-apply-citations.md).


## Publish naar een inhoudsfragment

Inhoudsfragmenten zijn afzonderlijke stukken inhoud in AEM. Het zijn gestructureerde inhoud die is gebaseerd op een inhoudsmodel. Inhoudsfragmenten zijn zuivere inhoud zonder ontwerp- of layoutgegevens. Ze kunnen onafhankelijk van de kanalen worden ontworpen en beheerd die AEM ondersteunen. De modulariteit en de herbruikbaarheid van de inhoudsfragmenten leiden tot meer flexibiliteit, consistentie, efficiëntie en eenvoudiger beheer.

AEM Guides biedt nu een manier om een onderwerp of de elementen binnen een onderwerp naar een inhoudsfragment te publiceren. U kunt een op JSON-Gebaseerde afbeelding tussen een onderwerp en een model van het inhoudsfragment tot stand brengen. Gebruik deze toewijzing om inhoud die in sommige of alle elementen binnen een onderwerp aanwezig is, naar een inhoudsfragment te publiceren.

Maak een hoofdletter van de kracht van AEM Guides en van inhoudsfragmenten en gebruik inhoudsfragmenten op elke AEM site. U kunt de details ook extraheren via API&#39;s die worden ondersteund door inhoudsfragmenten.

![ optie om inhoudsfragment ](assets/content-fragment-publish.png){width="550" align="left"} te publiceren

*Publish een onderwerp aan een inhoudsfragment.*

Voor meer details, bekijk [ Publish aan een inhoudsfragment ](../user-guide//publish-content-fragment.md).

## Verbeteringen voor revisie

AEM Guides beschikt nu over een verbeterde revisiefunctie met de volgende functies:

### Zoeken in revisieonderwerpen

Het uitvoeren van revisies is een belangrijk onderdeel van AEM Guides. Hiermee kunnen de revisoren de documenten controleren die aan hen zijn toegewezen.
U kunt nu naar een onderwerp zoeken door een deel van de tekst van de titel of het bestandspad in te voeren in de zoekbalk van de onderwerpenweergave van het revisiepaneel. U kunt ook alle onderwerpen of onderwerpen met opmerkingen weergeven. Standaard kunt u alle onderwerpen in de overzichtstaak weergeven. Voor meer details, mening [ onderwerpen van het Overzicht ](../user-guide/review-topics.md).

![ Onderzoek in een paneel van overzichtsonderwerpen ](assets/review-search-topic.png){width="800" align="left"}

*Onderzoek een overzichtsonderwerp in het overzichtspaneel.*



## Guides Extension Framework

Maak aangepaste pakketten boven op AEM Guides voor uitbreidbaarheid met AEM Guides Extension Framework. Deze pakketten zijn nuttig voor ontwikkelaars en consultants en geven ze uitbreidbaarheid aan de componenten in de Editor. Ze kunnen knoppen, dialoogvensters en dropdowns als doel hebben en aangepaste JavaScript toevoegen die eenvoudig kan samenwerken met de gebruikersinterface van AEM Guides.



## Native PDF-verbeteringen

De volgende Native PDF-verbeteringen zijn doorgevoerd in de release van september 2023 om van AEM Guides een robuuster product te maken:



### Pagina&#39;s bestellen in de PDF-uitvoer

U kunt de volgende secties in uw PDF tonen of verbergen en ook de orde schikken waarin zij in uw definitieve output van de PDF zouden moeten verschijnen:

* Inhoudsopgave
* Hoofdstuk en onderwerp
* Lijst met figuren
* Lijst met tabellen
* Index
* Verklarende woordenlijst
* Visum
* Paginalay-outs

Als u geen bepaalde sectie in de uitvoer van PDF wilt tonen, kunt u dat verbergen door de schakeloptie uit te schakelen.

Voor meer details, mening [ de Orde van de Pagina ](../native-pdf/components-pdf-template.md#page-order).

### Pagina&#39;s samenvoegen

In een native PDF-uitvoer beginnen standaard alle secties op een nieuwe pagina. Nu kunt u een sectie samenvoegen tot de vorige of volgende pagina. Hiermee wordt de sectie gepubliceerd in overeenstemming met de geselecteerde pagina in de PDF-uitvoer en is er geen pagina-einde tussen.

Voor meer details, bekijk de **eigenschapbeschrijving van 0&rbrace; pagina&#39;s van de Fusie &lbrace;in [ sectie van de Orde van de Pagina ](../native-pdf/components-pdf-template.md#page-order).**

### Een hoofdstuk vanaf de huidige pagina starten

U kunt de basisconfiguratiemontages voor de aanvang van een hoofdstuk van oneven of even pagina, de structuur van TOC, plaatsen en het formaat van de leaderlijn voor de ingangen van TOC bepalen.

Nu kunt u ook een hoofdstuk starten vanaf de huidige pagina. Als u dit wilt doen, worden alle hoofdstukken zonder pagina-einden verder gepubliceerd. Als een hoofdstuk bijvoorbeeld halverwege pagina 15 eindigt, begint het volgende hoofdstuk ook op de 15e pagina zelf.

Voor meer details, bekijk de **Algemene** lusjebeschrijving in [ Geavanceerde Montages van de PDF ](../native-pdf/components-pdf-template.md#advanced-pdf-settings-advanced-pdf-settings).

### Statische pagina&#39;s

U kunt ook aangepaste paginalay-outs maken en deze als statische pagina&#39;s publiceren in de PDF-uitvoer. Zo kunt u statische inhoud toevoegen, zoals notities of lege pagina&#39;s.

Voor meer details, bekijk de **Statische 1&rbrace; eigenschapbeschrijving van pagina&#39;s &lbrace;in [ sectie van de Volgorde van de Pagina ](../native-pdf/components-pdf-template.md#page-order).**


### Variabelen in kruisverwijzingen

U kunt variabelen gebruiken om een kruisverwijzing te definiëren. Wanneer u een variabele gebruikt, wordt de waarde ervan gekozen uit de eigenschappen.

Nu kunt u ook {figure} en {table} gebruiken.
Gebruik {figure} om een verwijzing naar het cijferaantal toe te voegen. Het selecteert het cijferaantal van de autoaantalstijlen die u voor figuur hebt bepaald.

Gebruik {table} om een kruisverwijzing naar het tabelnummer toe te voegen. Het kiest het lijstaantal van de autoaantalstijlen die u voor titel hebt bepaald.

Voor meer details, mening [ verwijzingen ](../native-pdf/components-pdf-template.md##cross-references).



### Opnieuw ontwerpen van CSS-editor

De CSS-editor is nu opnieuw ontworpen voor een betere gebruikerservaring met kiezers en stijleigenschappen.

#### Verbetering van dialoogvenster Stijl toevoegen

U kunt nu aangepaste kiezers gebruiken om complexe stijlen toe te voegen. Met het nieuwe veld Selector kunt u naast de combinatie Klasse, Tag en Pseudo-klasse ook aangepaste kiezers toevoegen. U kunt bijvoorbeeld een `table a.link` -stijl maken voor alle hyperlinks in een tabel.

![ toevoegend stijlen in de inheemse malplaatjes pdf ](assets/add-styles-native-pdf.png){width="300" align="left"}

*voeg de details voor de nieuwe stijl toe.*

#### Stijleigenschappen aanpassen

AEM Guides introduceert nu een nieuw deelvenster met eigenschappen onder de voorvertoningssectie voor stijlen. U kunt de eigenschappen van de stijlen efficiënter en sneller bewerken in het deelvenster Eigenschappen.


## Ondersteuning van meerdere onderwerpdefinities in één opsommingsdefinitie

U kunt nu een of meer onderwerpdefinities definiëren in een kaart en de opsommingsdefinities in een andere kaart en vervolgens de kaartverwijzing toevoegen. De verwijzingen naar onderwerpopsommingen worden opgelost in dezelfde kaart of in de kaart waarnaar wordt verwezen.

U kunt nu ook voorwaarden definiëren en deze toepassen op bepaalde specifieke elementen in een onderwerp.  De voorwaarden zijn alleen zichtbaar voor die specifieke elementen en niet voor alle andere elementen.

Voor meer details op de behandeling hiërarchische definities van onderwerpdefinities en opsommingen, bekijk de beschrijving van de onderwerpschemaeigenschap in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.





## Alle voorinstellingen in een kaartverzameling selecteren

U kunt niet alleen een individuele voorinstelling en alle voorinstellingen van het mapprofiel inschakelen, maar ook alle voorinstellingen voor een DITA-kaart in één keer.
![ geef een kaartinzameling ](assets/edit-map-collection-cs.png){width="800" align="left"} uit\
*selecteer alle vooraf instelt in een kaartinzameling.*

Voor meer details, mening [ de Inzameling van de Kaart van het Gebruik voor outputgeneratie ](../user-guide/generate-output-use-map-collection-output-generation.md).


## Native PDF-ondersteuning in Bulk Publish-dashboard


Met de functie AEM Guides Bulk Activation kunt u uw inhoud snel en eenvoudig activeren, van ontwerpen tot het publiceren van een exemplaar. In de kaart van de Activering van het Bulk, kunt u de Inheemse vooraf ingestelde PDF output, de AEM Plaats, PDF, HTML5, Douane, en output JSON omvatten.
Voor meer details, mening [ Bulk activering van gepubliceerde inhoud ](../user-guide/conf-bulk-activation.md).

## Verbeterd gereedschap Bulk verplaatsen

Als beheerder kunt u nu het verbeterde gereedschap Bulkverplaatsing gebruiken om mappen met een groot aantal bestanden van de ene naar de andere locatie te verplaatsen.
In het dialoogvenster Bladeren kunt u de bronmappen selecteren die u wilt verplaatsen. U kunt ook bladeren om de bestemmingsplaats te selecteren om de bronomslagen te bewegen. Selecteer ![ infopictogram ](assets/info-icon.svg) {width="25" align="left"} dichtbij een gebied om meer informatie over het te bekijken.

Voor meer details, bekijk [ dossiers van de Beweging in bulk ](../user-guide/authoring-file-management.md#move-files-bulk).


## Verbeterde voorvertoning via het contextmenu

Gebruik het contextmenu om snel een voorvertoning van het bestand weer te geven (.dita, .xml, audio, video of afbeelding) zonder het te openen. U kunt nu het formaat van het voorvertoningsvenster wijzigen. Als de inhoud een referentiekoppeling bevat, kunt u het venster selecteren en openen op een nieuw tabblad.

![ Het deelvenster Voorvertoning ](assets/quick-preview_cs.png){width="800" align="left"}

*voorproef het dossier in de ruit.*

Voor meer details op het contextmenu, zie de **Opties voor een dossier** eigenschapbeschrijving in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.


## Variabelen voor huidige datum en tijd gebruiken in de opties Doelpad, Sitenaam of Bestandsnaam

Terwijl het produceren van output in AEM Plaats of PDF, kunt u variabelen gebruiken voor het plaatsen van de **Weg van de Bestemming**, **Naam van de Plaats**, of **Naam van het Dossier** opties. U kunt nu ook de variabelen `${system_date}` en `${system_time}` gebruiken. Met deze variabelen kunt u de huidige datum en tijd aan deze opties toevoegen.

Leer hoe te [ gebruikvariabelen voor het plaatsen van de Weg van de Bestemming, de Naam van de Plaats, of de opties van de Naam van het Dossier ](../user-guide/generate-output-use-variables.md).
