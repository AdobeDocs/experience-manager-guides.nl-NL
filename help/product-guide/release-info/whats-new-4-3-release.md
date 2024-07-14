---
title: Opmerkingen bij de release | Nieuwe functies in Adobe Experience Manager Guides 4.3.0-release
description: Leer de nieuwe en verbeterde functies in de 4.3.0-versies van Adobe Experience Manager Guides
exl-id: 36decbf0-ec9d-43e2-99b7-85b0f9a87bc1
feature: What's New
role: Leader
source-git-commit: 5a444e88b0adba7fa3d498437df39b729b10b5eb
workflow-type: tm+mt
source-wordcount: '2655'
ht-degree: 0%

---

# Nieuwe functies in de release 4.3.0 van Adobe Experience Manager Guides (juli 2023)

Dit artikel behandelt de nieuwe en verbeterde eigenschappen in versie 4.3.0 van Adobe Experience Manager Guides (later die als *wordt bedoeld AEM Guides*).

Voor meer details op de verbeteringsinstructies, verenigbaarheidsmatrijs, en de kwesties die in deze versie worden bevestigd, zie [ de nota&#39;s van de Versie ](./release-notes-4-3.md).


## Verbind met een gegevensbron en neem gegevens in uw onderwerpen op

Nu kunt u snel verbinding maken met uw gegevensbronnen via kant-en-klare connectors uit AEM Guides. Door verbinding te maken met een gegevensbron, kunt u uw informatie synchroon houden met de bron. Updates van de gegevens worden automatisch weerspiegeld, waardoor AEM Guides een echte inhoudshub wordt. Met deze functie bespaart u tijd en moeite om de gegevens handmatig toe te voegen of te kopiëren.

AEM Guides staat uw beheerder toe om de uit-van-de-doosschakelaars voor JIRA en SQL (MySQL, PostgreSQL, SQL Server, SQLite) gegevensbestanden te vormen. Zij kunnen andere schakelaars ook toevoegen door de standaardinterfaces uit te breiden.
Zodra toegevoegd, kunt u de gevormde schakelaars bekijken die onder het paneel van Gegevensbronnen in de Redacteur van het Web worden vermeld.

<img src="assets/data-sources.png" alt="Lijst met gegevensbronnen in het deelvenster" width="300">

Maak een inhoudsfragment om de gegevens van een verbonden gegevensbron op te halen. U kunt de gegevens in uw onderwerpen dan opnemen en het uitgeven. Zodra u een generator van het inhoudsfragment hebt gecreeerd, kunt u het opnieuw gebruiken om de gegevens in om het even welk onderwerp op te nemen.

Nu kunt u een onderwerp van een verbonden gegevensbron ook tot stand brengen. Een onderwerp kan gegevens in diverse formaten, zoals lijsten, lijsten, en paragrafen bevatten. Het staat u ook toe om een kaart DITA voor alle onderwerpen tot stand te brengen. U kunt meta-gegevens aan het onderwerp associëren wanneer het trekken uit een gegevensbron.

Voor meer details, mening [ Gegevens van het Gebruik van uw gegevensbron ](../user-guide/web-editor-content-snippet.md).

## citaten toevoegen aan uw inhoud

Bijschriften zijn verwijzingen naar de informatiebron die aan de inhoud is toegevoegd. Met uitnodigingen kunt u uw geloofwaardigheid herstellen en plagiaat voorkomen. Met uitnodigingen kunnen de lezers de bron vinden en de informatie in de tekst controleren.

In AEM Guides kunt u citaten toevoegen of citaten importeren en deze op de inhoud toepassen. U kunt deze citaten toevoegen vanuit elke bron van boeken, websites en tijdschriften.

Na het opnemen van uw citaten aan uw onderwerpen, kunt u voorproef hen in de Redacteur van het Web. U kunt inhoud met citaten ook publiceren gebruikend Eigen PDF.

![ Bevelen die in een paneel ](assets/citation-panel.png){width="300" align="left"} worden vermeld


Voor meer details, voegt de mening [ toe en beheert citaties in uw inhoud ](../user-guide/web-editor-apply-citations.md).

## Publish naar een inhoudsfragment

Inhoudsfragmenten zijn afzonderlijke stukken inhoud in AEM. Het zijn gestructureerde inhoud die is gebaseerd op een inhoudsmodel. Inhoudsfragmenten zijn zuivere inhoud zonder ontwerp- of layoutgegevens. Ze kunnen onafhankelijk van de kanalen worden ontworpen en beheerd die AEM ondersteunen. De modulariteit en de herbruikbaarheid van de inhoudsfragmenten leiden tot meer flexibiliteit, consistentie, efficiëntie en eenvoudiger beheer.

AEM Guides biedt nu een manier om een onderwerp of de elementen binnen een onderwerp naar een inhoudsfragment te publiceren. U kunt een op JSON-Gebaseerde afbeelding tussen een onderwerp en een model van het inhoudsfragment tot stand brengen. Gebruik deze toewijzing om inhoud die in sommige of alle elementen binnen een onderwerp aanwezig is, naar een inhoudsfragment te publiceren.

Maak een hoofdletter van de kracht van AEM Guides en van inhoudsfragmenten en gebruik inhoudsfragmenten op elke AEM site. U kunt de details ook extraheren via API&#39;s die worden ondersteund door inhoudsfragmenten.

![ optie om inhoudsfragment ](assets/content-fragment-publish.png){width="550" align="left"} te publiceren


## Verbeteringen voor revisie

AEM Guides beschikt nu over een verbeterde revisiefunctie met de volgende functies:

### Deelvenster Controleren om revisieprojecten en de actieve revisietaken te presenteren

Nu maakt AEM Guides uw revisies naadloos. Het biedt het deelvenster Revisies in de webeditor. In het deelvenster Revisies worden alle revisieprojecten en de actieve revisietaken weergegeven in de revisieprojecten die u maakt.

Als auteur kunt u met deze functie gemakkelijk de revisietaken openen, de opmerkingen bekijken en de opmerkingen snel in een gecentraliseerde weergave adresseren.
![](assets/active-review-task-comments.png){width="800" align="left"}
Voor meer details, bekijk de **2} eigenschapbeschrijving van het Overzicht {binnen de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.**

### Zoeken in revisieonderwerpen

Het uitvoeren van revisies is een belangrijk onderdeel van AEM Guides. Hiermee kunnen de revisoren de documenten controleren die aan hen zijn toegewezen.
U kunt nu naar een onderwerp zoeken door een deel van de tekst van de titel of het bestandspad in te voeren in de zoekbalk van de onderwerpenweergave van het revisiepaneel. U kunt ook alle onderwerpen of onderwerpen met opmerkingen weergeven. Standaard kunt u alle onderwerpen in de overzichtstaak weergeven.


![ Onderzoek in een paneel van overzichtsonderwerpen ](assets/review-search-topic.png){width="800" align="left"}

Voor meer details, mening [ onderwerpen van het Overzicht ](../user-guide/review-topics.md).

## Guides Extension Framework

Maak aangepaste pakketten boven op AEM Guides voor uitbreidbaarheid met AEM Guides Extension Framework. Deze pakketten zijn nuttig voor ontwikkelaars en consultants en geven ze uitbreidbaarheid aan de componenten in de Editor. Ze kunnen knoppen, dialoogvensters en dropdowns als doel hebben en aangepaste JavaScript toevoegen die eenvoudig kan samenwerken met de gebruikersinterface van AEM Guides.



## Native PDF-verbeteringen

De volgende Native PDF-verbeteringen zijn doorgevoerd in de 4.3.0-release om AEM Guides een robuuster product te maken:

### Ondersteuning voor taalvariabelen

AEM Guides ondersteunt taalvariabelen. U kunt taalvariabelen gebruiken om een gelokaliseerde versie van de uit-van-de-doos etiketten zoals Nota, Voorzichtigheid, en Waarschuwing of statische tekst in de output van PDF te bepalen.
U kunt de taalvariabelen of de gelokaliseerde versie van de etiketten aan de aangewezen secties in uw output van PDF en in de outputmalplaatjes toevoegen.

#### Taalvariabelen in de PDF-uitvoer

U kunt de taalvariabelen gebruiken om gelokaliseerde etiketten voor elementen zoals Nota, Voorzichtigheid, en Waarschuwing te bepalen. U kunt de waarde voor deze variabelen bijwerken in een of meer talen en vervolgens wordt de gelokaliseerde waarde automatisch gekozen in de uitvoer van PDF.
U kunt bijvoorbeeld het label Notitie op de volgende manieren in uw PDF-uitvoer presenteren:

* Engels: Opmerking
* Frans: Opmerking
* Duits: Hinweis

#### Taalvariabelen in de uitvoersjablonen

Als u de PDF-uitvoer in verschillende talen wilt maken, moet u verschillende PDF-sjablonen maken die gelokaliseerde tekst voor elke taal bevatten. Nu met de eigenschap van taalvariabelen, moet u het malplaatje slechts eenmaal tot stand brengen. Vervolgens kunt u voor elke statische tekst die u wilt lokaliseren, overeenkomstige taalvariabelen maken en deze gebruiken in uw sjabloon.
U kunt taalvariabelen maken voor langere tekst, zoals een hele zin of zelfs een alinea. U kunt ook stijlen toepassen en markeringen voor HTML gebruiken om deze taalvariabelen op te maken.

Voor meer details, mening [ Steun voor taalvariabelen ](../native-pdf/native-pdf-language-variables.md).

### Een watermerk toevoegen aan de PDF-uitvoer voor conceptdocumenten

Nu kunt u een watermerk toevoegen aan de PDF-uitvoer van het document dat nog niet is goedgekeurd. Dit watermerk wordt niet weergegeven als u de PDF voor het document genereert in de documentstatus &#39;Goedgekeurd&#39;. U kunt bijvoorbeeld een watermerk Concept toevoegen voor uw PDF-uitvoer.

Voor meer details, voegt de mening [ een watermerk aan de output van de PDF voor ontwerpdocumenten ](../native-pdf/use-javascript-content-style.md#watermark-draft-document) toe.

### Mogelijkheid om AEM metagegevens te gebruiken in PDF-lay-outs

Metagegevens zijn de beschrijving of definitie van de inhoud. Deze metagegevens worden opgeslagen in de DITA-bronkaartinhoud.

Nu kunt u in AEM Guides ook de eigenschappen van metagegevens van uw elementen selecteren en deze toevoegen aan de pagina-indeling. Vervolgens kiest AEM Guides deze metagegevenseigenschappen van uw elementen en publiceert het deze in uw PDF-uitvoer.


![ voeg meta-gegevens voor inheemse pdf ](assets/native-pdf-metadata-asset.png){width="300" align="left"} toe

>[!NOTE]
>
> AEM Guides ondersteunt ook de eigenschappen van metagegevens voor uw DITA-kaarten.

Voor meer details, mening [ voegt gebieden en meta-gegevens ](../native-pdf/design-page-layout.md#add-fields-metadata) toe.


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

In een native PDF-uitvoer beginnen standaard alle secties op een nieuwe pagina. Nu kunt u een sectie samenvoegen tot de vorige of volgende pagina. Hierdoor wordt de sectie gepubliceerd in overeenstemming met de geselecteerde pagina in de PDF-uitvoer en is er geen pagina-einde tussen de pagina&#39;s.

Voor meer details, bekijk de de eigenschapbeschrijving van de pagina&#39;s van de Fusie in [ sectie van de Orde van de Pagina ](../native-pdf/components-pdf-template.md#page-order).

### Statische pagina&#39;s

U kunt ook aangepaste paginalay-outs maken en deze als statische pagina&#39;s publiceren in de PDF-uitvoer. Zo kunt u statische inhoud toevoegen, zoals notities of lege pagina&#39;s.

Voor meer details, bekijk de Statische beschrijving van de paginageigenschap in [ sectie van de Volgorde van de Pagina ](../native-pdf/components-pdf-template.md#page-order).


### Variabelen in kruisverwijzingen

U kunt variabelen gebruiken om een kruisverwijzing te definiëren. Wanneer u een variabele gebruikt, wordt de waarde ervan gekozen uit de eigenschappen.

Nu kunt u ook {figure} en {table} gebruiken.
Gebruik {figure} om een verwijzing naar het cijferaantal toe te voegen. Het selecteert het cijferaantal van de autoaantalstijlen die u voor figuur hebt bepaald.

Gebruik {table} om een kruisverwijzing naar het tabelnummer toe te voegen. Het kiest het lijstaantal van de autoaantalstijlen die u voor titel hebt bepaald.

Voor meer details, mening [ verwijzingen ](../native-pdf/components-pdf-template.md##cross-references).

### Een hoofdstuk vanaf de huidige pagina starten

U kunt de basisconfiguratiemontages voor de aanvang van een hoofdstuk van oneven of even pagina, de structuur van TOC, plaatsen en het formaat van de leaderlijn voor de ingangen van TOC bepalen.

Nu kunt u ook een hoofdstuk starten vanaf de huidige pagina. Als u dit wilt doen, worden alle hoofdstukken zonder pagina-einden verder gepubliceerd. Als een hoofdstuk bijvoorbeeld halverwege pagina 15 eindigt, begint het volgende hoofdstuk ook op de 15e pagina zelf.


### Mogelijkheid om toegang te krijgen tot tijdelijke HTML-bestanden terwijl de native PDF-uitvoer wordt gegenereerd

Nu kunt u met AEM Guides de tijdelijke HTML-bestanden downloaden die zijn gemaakt tijdens het genereren van de native PDF-uitvoer. Selecteer in de instellingen van de uitvoervoorinstelling de optie om de tijdelijke bestanden te downloaden.  In AEM Guides kunt u vervolgens de tijdelijke bestanden downloaden die zijn gemaakt tijdens het genereren van de uitvoer met behulp van die voorinstelling.

Met deze functie krijgt u meer inzicht in het generatieproces dankzij toegang tot tussentijdse stijlen en lay-outs en kunt u uw CSS-stijlen naar wens corrigeren of wijzigen.

![ de geavanceerde montagesdialoog van inheems pdf ](assets/native-pdf-advanced-settings.png){width="800" align="left"}

Voor meer details, leidt de mening [ tot een PDF output vooraf ingesteld ](../web-editor/native-pdf-web-editor.md#create-output-preset).


### Opnieuw ontwerpen van CSS-editor

De CSS-editor is nu opnieuw ontworpen voor een betere gebruikerservaring met kiezers en stijleigenschappen.

#### Verbetering van dialoogvenster Stijl toevoegen

U kunt nu aangepaste kiezers gebruiken om complexe stijlen toe te voegen. Met het nieuwe veld Selector kunt u naast de combinatie Klasse, Tag en Pseudo-klasse ook aangepaste kiezers toevoegen. U kunt bijvoorbeeld een `table a.link` -stijl maken voor alle hyperlinks in een tabel.

![ toevoegend stijlen in de inheemse malplaatjes pdf ](assets/add-styles-native-pdf.png){width="300" align="left"}

#### Stijleigenschappen aanpassen

AEM Guides introduceert nu een nieuw deelvenster met eigenschappen onder de voorvertoningssectie voor stijlen. U kunt de eigenschappen van de stijlen efficiënter en sneller bewerken in het deelvenster Eigenschappen.


## Bestanden hernoemen en verplaatsen in de weergave Opslagplaats

U kunt nu ook de naam van een bestand wijzigen of een bestand uit het deelvenster Opslagruimte verplaatsen. Deze functie is handig en helpt uw bestanden eenvoudig te beheren vanuit het deelvenster Opslag. U kunt een dossier selecteren en het anders noemen of bewegen gebruikend het **menu van Opties** voor het geselecteerde dossier. AEM Guides geeft een succesbericht weer wanneer u een bestand verplaatst of hernoemt.

![ optiemenu van een dossier ](assets/rename-move-assets.png){width="550" align="left"}

Voor meer details op het menu van Opties van een dossier, bekijk de **eigenschapbeschrijving van de mening van de Bewaarplaats** in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

## Verbroken rapport van Verbindingen in de Redacteur van het Web

AEM Guides staat u toe om de algemene volledigheid van uw technische documenten te controleren en rapporten van de Redacteur van het Web te produceren. Nu biedt AEM Guides in juni 2023 de functie om verbroken koppelingen weer te geven en te herstellen. Dit is een handig rapport waarmee u verbroken koppelingen kunt beheren. U kunt de verbroken verbindingen gemakkelijk bekijken aanwezig in uw kaart DITA en hen ook bevestigen.
![ gebroken verbindingsrapport ](assets/broken-link-report.png){width="800" align="left"}

Als u een koppeling hebt hersteld, wordt deze niet weergegeven onder de lijst met verbroken koppelingen.

Voor meer details, zie [ Mening en moeilijke situatie gebroken verbindingen ](../user-guide/reports-web-editor.md#report-broken-links).

## Verbeteringen aan schema

### Gebruik rapportinstructies om te controleren op regels in Schematron

AEM Guides steunt nu ook de verklaringen in het verslag met de Schematron. Een rapportverklaring produceert een bericht wanneer een testverklaring aan waar evalueert. Als u bijvoorbeeld wilt dat de korte beschrijving uit maximaal 150 tekens bestaat, kunt u een rapportinstructie definiëren om de onderwerpen te controleren waarvoor de korte beschrijving uit meer dan 150 tekens bestaat.

Voor meer details, mening [ het Gebruik bevestigt en rapporteert verklaringen om regels ](../user-guide/support-schematron-file.md#schematron-assert-report) te controleren.

### Regex-expressies gebruiken

U kunt Regex-expressies ook gebruiken om een regel met de functie match() te definiëren en vervolgens validatie uit te voeren met het Schematron-bestand.

Voor meer details, mening [ de uitdrukkingen van Regex van het Gebruik ](../user-guide/support-schematron-file.md#schematron-assert-report).


### abstracte patronen definiëren

AEM Guides ondersteunt ook abstracte patronen in Schematron. U kunt generische abstracte patronen definiëren en deze abstracte patronen opnieuw gebruiken. Abstracte patronen kunnen uw Schematron-schema vereenvoudigen en u helpen uw validatielogica te beheren en bij te werken.


Voor meer details, bepaalt de mening [ abstracte patronen ](../user-guide/support-schematron-file.md#schematron-abstract-patterns).

## Ondersteuning voor XLIFF-indeling in vertaling

AEM Guides biedt ook ondersteuning voor de XLIFF-indeling (XML Localization Interchange File Format) bij het vertalen. Nu kunt u ook verkiezen om **een nieuw XLIFF vertaalproject** tot stand te brengen om de inhoud van XML in het formaat om te zetten XLIFF. AEM Guides ondersteunt XLIFF versie 1.2.

Met deze indeling kunt u de inhoud exporteren naar de industriestandaard XLIFF-indeling en deze indeling vervolgens aan de vertaalbureaus aanbieden. Voor meer details, leidt de mening [ tot een vertaalproject ](../user-guide/translate-documents-web-editor.md#create-translation-project).

![ types van vertaalprojecten ](assets/translation-project-types.png){width="350" align="left"}


## Verbeteringen voor kaartverzameling

Met een kaartverzameling kunt u meerdere toewijzingen ordenen en in batches publiceren. Er zijn veel nieuwe verbeteringen aangebracht in de kaartverzameling:

* Nu kunt u native voorinstellingen voor PDF-uitvoer toevoegen aan een kaartverzameling en deze gebruiken om de PDF-uitvoer te genereren.
* U kunt de algemene voorinstellingen en voorinstellingen van het mapprofiel die door de beheerder zijn gemaakt, weergeven en deze gebruiken om de PDF-uitvoer te genereren.
* U kunt nu niet alleen een individuele voorinstelling selecteren, maar u kunt ook alle voorinstellingen voor het mapprofiel voor een DITA-kaart in één keer inschakelen.
  ![ geef een kaartinzameling ](assets/edit-map-collection.png){width="800" align="left"} uit

Voor meer details, mening [ de Inzameling van de Kaart van het Gebruik voor outputgeneratie ](../user-guide/generate-output-use-map-collection-output-generation.md).

## Native PDF-ondersteuning in Bulk Publish-dashboard


Met de functie AEM Guides Bulk Activation kunt u uw inhoud snel en eenvoudig activeren, van ontwerpen tot het publiceren van een exemplaar. In de kaart van de Activering van het Bulk, kunt u de Inheemse vooraf ingestelde PDF output, de AEM Plaats, PDF, HTML5, Douane, en output JSON omvatten.
Voor meer details, mening [ Bulk activering van gepubliceerde inhoud ](../user-guide/conf-bulk-activation.md).

## Verbeterd gereedschap Bulk verplaatsen

Als beheerder kunt u nu het verbeterde gereedschap Bulkverplaatsing gebruiken om mappen met een groot aantal bestanden van de ene naar de andere locatie te verplaatsen.
In het dialoogvenster Bladeren kunt u de bronmappen selecteren die u wilt verplaatsen. U kunt ook bladeren om de bestemmingsplaats te selecteren om de bronomslagen te bewegen. Selecteer ![ infopictogram ](assets/info-icon.svg) {width="25" align="left"} dichtbij een gebied om meer informatie over het te bekijken.

Voor meer details, bekijk [ dossiers van de Beweging in bulk ](../user-guide/authoring-file-management.md#move-files-bulk).

## Verbeterd deelvenster Favorieten

Met AEM Guides kunt u een verzameling of favoriete lijst met bestanden en mappen maken en deze gemakkelijk gebruiken. Nu **het menu van Opties** is ook beschikbaar in het **Favorieten** paneel. U kunt de geselecteerde inzameling anders noemen of het van het **menu van Opties** schrappen. U kunt **selecteren verfrist** optie om een nieuwe lijst van dossiers of omslagen van de bewaarplaats te krijgen. U kunt de inhoud van de map ook weergeven in de gebruikersinterface van Assets.

![ het favoriete paneel ](assets/favorites-options.png){width="650" align="left"}

>[!NOTE]
>
> U kunt de lijst ook verfrissen gebruikend **verfrissen** pictogram op de bovenkant.

Voor meer details op het **menu van Opties** van een inzameling van Favorieten, bekijk de **3} eigenschapbeschrijving van Favorieten {in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.**

## Overschakelen naar het systeemthema

U kunt nu ook het apparaatthema gebruiken. Gebruikend de **Voorkeur van de Gebruiker**, kunt u AEM Guides vormen om tussen lichte en donkere thema&#39;s automatisch te schakelen die op het thema van uw apparaat worden gebaseerd.

![ gebruikersvoorkeur ](assets/device-theme-user-preferences.png){width="550" align="left"}

Voor meer details, bekijk de **eigenschapbeschrijving van de Voorkeur van de Gebruiker 1} in de [ Belangrijkste toolbar ](../user-guide/web-editor-features.md#id2051EA0G05Z) sectie.**
