---
title: Opmerkingen bij de release | Adobe Experience Manager Guides 4.1-release
description: Laatste release van Adobe Experience Manager Guides
exl-id: c70b3bbc-3332-4626-bc30-641034f8fd06
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '3644'
ht-degree: 0%

---

# 4.1.x-release van Adobe Experience Manager Guides

Deze versienota&#39;s behandelt de verbeteringsinstructies, de nieuwe eigenschappen, en de verhogingen in versie 4.1.x van Adobe Experience Manager Guides (later die als *wordt bedoeld AEM Guides*).

## Upgrade naar de nieuwste versie

U kunt uw huidige versie van AEM Guides eenvoudig upgraden naar versie 4.1.3. Voordat u verdergaat met de upgrade naar versie 4.1.3 van AEM Guides, moet u rekening houden met de volgende punten:
* Als u versie 4.1 of 4.1.x gebruikt, kunt u rechtstreeks upgraden naar versie 4.1.3.
* Als u versie 4.0.x gebruikt, moet u een upgrade naar versie 4.1 of 4.1.x uitvoeren voordat u een upgrade naar versie 4.1.3 uitvoert.
* Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0.x uitvoeren voordat u een upgrade naar versie 4.1 uitvoert.
* Als u een versie hebt die ouder is dan 3.8.5, raadpleegt u de upgradesectie in de productspecifieke installatiegids.

Voor details, zie [ instructies van de Verbetering ](assets/Adobe-Experience-Manager-Guides-Upgrade-Instructions-EN.pdf).

## 4.1.3. | Opmerkingen bij de release

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides 4.1.3-release.

### ADOBE EXPERIENCE MANAGER

**niet-UUID**
Versie 6.5 Service Pack 13, 12, 11 of 10

**UUID**
Versie 6.5 Service Pack 13, 12, 11 of 10

Raadpleeg de sectie Technische vereisten in de handleiding voor het installeren en configureren van Adobe Experience Manager Guides voor meer informatie.


### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2020 | FMPS 2019 | Fm 2020 | Fm 2019 |
| --- | --- | --- | --- | --- |
| 4.1.3 (niet-UUID) | 2020.2 of hoger* | 2019 | 2020.3 of hoger | 2019.8 (laatste update) |
| 4.1.3 (UUID) | 2020.2 of hoger* | Niet compatibel | 2020.4 of hoger | Niet compatibel |
| | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.1.3 (niet-UUID) | 2,0 | 2,0 | 1,6 | 1,6 |
| 4.1.3 (UUID) | 2,7 | 2,7 | 2,3 | 2,3 |
|  |  |   |


## Opgeloste problemen

De gecorrigeerde bug wordt hieronder weergegeven:

* De webeditor laadt regelmatig een lege pagina. 10678


## 4.1.2. | Opmerkingen bij de release

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides 4.1.2-release.

### ADOBE EXPERIENCE MANAGER

**niet-UUID**
Versie 6.5 Service Pack 13, 12, 11 of 10

**UUID**
Versie 6.5 Service Pack 13, 12, 11 of 10

Raadpleeg de sectie Technische vereisten in de handleiding voor het installeren en configureren van Adobe Experience Manager Guides voor meer informatie.


### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2020 | FMPS 2019 | Fm 2020 | Fm 2019 |
| --- | --- | --- | --- | --- |
| 4.1.2 (niet-UUID) | 2020.2 of hoger* | 2019 | 2020.3 of hoger | 2019.8 (laatste update) |
| 4.1.2 (UUID) | 2020.2 of hoger* | Niet compatibel | 2020.4 of hoger | Niet compatibel |
| | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.1.2 (niet-UUID) | 2,0 | 2,0 | 1,6 | 1,6 |
| 4.1.2 (UUID) | 2,7 | 2,7 | 2,3 | 2,3 |
|  |  |   |


## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

* Bij het selecteren van alle mapprofielen wordt een onzichtbaar mapprofiel (dat onjuist is) weergegeven. 10393
* Bij het maken van de basislijn wordt niet de nieuwste versie gekozen, wanneer de tijdzone van de gebruiker afwijkt van de tijdzone van de server. (10336)
* Met de sneltoets Control+F wordt de zoekmodus van de browser in de Assets-console niet geopend na de installatie van AEM Guides 4.1. (10339)
* Fout bij maken basislijn voor onderwerp met verwijzing naar een map. 10383
* Op het tabblad Uitvoervoorinstellingen wordt periodiek een leeg scherm weergegeven en in sommige gevallen worden niet-bewerkbare voorinstellingen weergegeven. 10390
* Keyspace-beheer leidt tot uitzonderingen en fouten. (10449)

### Bekende problemen met tijdelijke oplossing

* Basislijn die tijdens het omzetten is geëxporteerd, wordt niet geladen op het tabblad basislijn van de editor.

  **Oplossing**: Gebruik het basislijnlusje van DITA kaartdashboard.

## 4,1 | Opmerkingen bij de release

Deze versienota&#39;s behandelt de verbeteringsinstructies, de nieuwe eigenschappen, en de verhogingen in versie 4.1.x van Adobe Experience Manager Guides (later die als *wordt bedoeld AEM Guides*).

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides 4.1-release.

### ADOBE EXPERIENCE MANAGER

**niet-UUID**
Versie 6.5 Service Pack 13, 12, 10 of 11

**UUID**
Versie 6.5 Service Pack 13, 12, 10 of 11

Raadpleeg de sectie Technische vereisten in de handleiding voor het installeren en configureren van Adobe Experience Manager Guides voor meer informatie.




### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2020 | FMPS 2019 | Fm 2020 | Fm 2019 |
| --- | --- | --- | --- | --- |
| 4.1 (Niet-UUID) | 2020.2 of hoger* | 2019 | 2020.3 of hoger | 2019.8 (laatste update) |
| 4.1 (UUID) | 2020.2 of hoger* | Niet compatibel | 2020.4 of hoger | Niet compatibel |
| | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.1 (Niet-UUID) | 2,0 | 2,0 | 1,6 | 1,6 |
| 4.1 (UUID) | 2,7 | 2,7 | 2,3 | 2,3 |
|  |  |  |


## Nieuwe en verbeterde functies

AEM Guides biedt veel verbeteringen en nieuwe functies in de 4.1-release:

### Native PDF-publicatie

Ondersteuning voor het maken van een native PDF is ook toegevoegd aan de 4.1-release van AEM Guides. Er is een nieuwe uitgeverij-engine geïntroduceerd met de volgende functies:
* Een CSS-sjabloon maken
* Andere paginasjablonen maken
* PDF-sjablonen ontwerpen die CSS en paginasjablonen bevatten
* Publish-kaart en onderwerpinhoud in de PDF-indeling

### Ondersteuning voor het pad van de kennisbasissite in op artikelen gebaseerde publicaties

AEM Guides biedt de op artikelen gebaseerde publicatiefunctie om incrementeel een uitvoer van een of meer onderwerpen te genereren of uw inhoud te publiceren naar een Knowledgebase-platform. Met versie 4.1, hebt u een extra optie om de de plaatsweg te kiezen van de Kennisbank waaraan het onderwerp/de kaart moet worden gepubliceerd. Nadat u het pad hebt geselecteerd, wordt de uitvoer gegenereerd op het opgegeven pad.

### Verbeterde webeditor

* **Verbeterde zeer belangrijke resolutie**

Een DITA inhoudsbelangrijkste verwijzing neemt een deel van inhoud van één onderwerp in een andere op. Er wordt een toets gebruikt om de inhoud te zoeken. De belangrijkste verwijzingen verbonden aan een onderwerp DITA moeten worden opgelost. De geselecteerde hoofdmap heeft de hoogste prioriteit om toetsverwijzingen op te lossen.

![ dialoog van gebruikersvoorkeur ](assets/user-preferences.png)

Nu worden de belangrijkste verwijzingen opgelost op basis van de wortelkaart die in de volgende orde van prioriteit wordt geplaatst:

1. Gebruikersvoorkeuren
1. Deelvenster Kaartweergave
1. Mapprofiel

Voor meer details, zie *zeer belangrijke verwijzingen* sectie oplossen in de Gebruikende gids van Adobe Experience Manager Guides.

* **voeg een douanepaneel in het linkerpaneel toe**

Nu kunt u een aangepast deelvenster toevoegen in het linkerdeelvenster van de webeditor. U kunt een aangepast deelvenster gebruiken voor verschillende doeleinden, zoals het bieden van hulp of het testen voor een project. Als een douanepaneel is gevormd, dan verschijnt het ook in de lijst van panelen binnen de **Montages van de Redacteur**. U kunt schakelen tussen het weergeven of verbergen van het aangepaste deelvenster.

* **Mogelijkheid om de documentstaat van onderwerpen in een kaart te veranderen DITA**

Nu kunt u de documentstaat van geselecteerde onderwerpen binnen een kaart gemakkelijk veranderen DITA. U kunt de eigenschappen van geselecteerde onderwerpen in een kaart DITA van het **Meer menu van Opties** bij de bodem van het paneel van de Mening van de Kaart ook openen en uitgeven.

![ geselecteerde onderwerpeigenschappen ](assets/map-view-properties.png)

* **informatie van de Versie die op de wijze van de Voorproef wordt getoond**

De Redacteur van het Web helpt u in het beheren van uw versies. Nu kunt u de versie van het actieve onderwerp of kaart DITA in de hoogste juiste hoek van het het dossierlusje van het onderwerp op de wijze van de Voorproef van een onderwerp ook zien.

![ voorproefversie ](assets/preview-version.png)


* **Verbeterde Redacteur van het Web verfrist gedrag**

De volgende verbeteringen zijn nu beschikbaar met browser verfrist verrichting in de Redacteur van het Web:

* Nu krijgt u de ondersteuning om de browser te vernieuwen terwijl u uw
inhoud in de webeditor. Als u op het pictogram Vernieuwen van de browser klikt terwijl een of meer bestanden met
niet-opgeslagen wijzigingen worden geopend voor bewerking. U wordt gevraagd uw bestanden op te slaan of de vernieuwingsactie te annuleren.

* Zelfs bij het vernieuwen van de browser blijven de weergaven van het linkerdeelvenster en het rechterdeelvenster behouden.

* Het actieve onderwerp of de kaart DITA wordt opnieuw geopend in het inhoudsuitgevende gebied.

* **creeer kaarten die op aangepaste malplaatjes** worden gebaseerd

Nu krijgt u de krachtige eigenschap om aangepaste kaartmalplaatjes tot stand te brengen. U kunt hen gebruiken om kaarten DITA samen met de onderwerpmalplaatjes en kaartmalplaatjes tot stand te brengen die in het kaartmalplaatje van verwijzingen worden voorzien.

![ dita malplaatjes ](assets/dita-templates.png)

U kunt naar andere kaartmalplaatjes en onderwerpmalplaatjes van het aangepaste kaartmalplaatje ook verwijzen. De genoemde kaartmalplaatjes kunnen naar diverse kaartmalplaatjes, onderwerpmalplaatjes, onderwerpen, kaarten, beelden, video&#39;s, en andere activa verwijzen.

![ creeer bewerkingsmalplaatjes ](assets/create-dita-template.png)

Het aangepaste kaartsjabloon kan u zeer gemakkelijk helpen de kaartsjablonen en de volledige doorverwezen omslagstructuur te herhalen. Deze aangepaste sjablonen zijn vooral handig voor het maken en opnieuw maken van meerdere kaarten met recursieve structuren en verwijzingen.

* **de steun van Schematron**
&quot;Schematron&quot; verwijst naar een op regels gebaseerde validatietaal die wordt gebruikt om tests voor een XML-bestand te definiëren. Met behulp van een Schematron-bestand kunt u bepaalde regels definiëren en deze vervolgens valideren voor een DITA-onderwerp of een kaart. De redacteur van het Web steunt dossiers Schematron. U kunt de Schematron dossiers invoeren en hen ook uitgeven in de Redacteur van het Web. De steun van het Schematron in de Redacteur van het Web helpt u in het bevestigen van de dossiers tegen een reeks regels en het handhaven van consistentie en correctheid over de onderwerpen.

![ bevestigt schema ](assets/schematron-validate.png)

* **Verbeterde dialoog op dossierdichte**

AEM Guides vraagt u om uw wijzigingen op te slaan en vergrendelde bestanden te ontgrendelen wanneer u een bestand probeert te sluiten dat is geopend in de webeditor. De herinneringen worden getoond gebaseerd op **vraagt om controle-binnen op dicht** en **vraagt om nieuwe versie op dichte** montages die door uw beheerder worden gevormd.

Op basis van de configuratie kunt u de wijzigingen opslaan en een nieuwe versie van het document maken. U kunt ook het bestand inchecken en de wijzigingen in de huidige versie opslaan.

![ Dossier dicht ](assets/file-close-save-changes-unlock.png)

Voor meer details, zie *Dossier sluiten en sparen scenario&#39;s* sectie in de Gebruikende gids van Adobe Experience Manager Guides.* De **eigenschap van het Trefwoord van het Tussenvoegsel** is verbeterd. U kunt nu gemakkelijker een trefwoord vinden dat moet worden ingevoegd omdat de trefwoorden in alfabetische volgorde worden weergegeven. U kunt ook naar trefwoorden zoeken door een zoektekenreeks in het vak Zoeken te typen.

![ neem sleutelwoord ](assets/insert-keyword.png) op

* **Steun voor de documenten van de Prijsverhoging**
Markering is een eenvoudige opmaaktaal waarmee u opmaakelementen kunt toevoegen aan gewone tekstdocumenten. De Redacteur van het Web staat u toe om de documenten van de Prijsverhoging (.md) samen met uw documenten te gebruiken DITA. U kunt een document van de Prijsverhoging in de Redacteur van het Web gemakkelijk ontwerpen en voorproef en het ook toevoegen in uw kaartdossier door DITA kaartredacteur.  Voor meer details, zie *documenten van de Prijsverlaging van de Auteur van het Web* sectie in het Gebruiken van de gids van Adobe Experience Manager Guides.

![ steun prijsdown ](assets/create-markdown-dita-topic.png)

* **Mogelijkheid om een standaardmarkeringsmening te vormen**
Als een gebruiker de Mening van Markeringen van de Redacteur van het Web toelaat, blijft het toegelaten zelfs over de zittingen.  Dit betekent dat u de mening van Markeringen niet moet toelaten om tot het later toegang te hebben. Uw beheerder kan de standaardstaat voor de Mening van Markeringen in de Redacteur van het Web vormen. De standaardwaarde voor de Mening van Markeringen voor de zitting van een nieuwe gebruiker wordt bepaald door het bezit tagsView in het ui_config.json- dossier.

* In de weergavebestanden voor opslagplaatsen worden nu batches geladen. Alle bestanden in de hoofdmap of `/content/dam folder` worden weergegeven. Maar vanaf het volgende niveau of de secundaire map worden 75 bestanden tegelijk geladen. Het laden van deze batch is efficiënt en u hebt sneller toegang tot de bestanden dan tot het laden van alle bestanden in een map.

![ lading meer dossiers ](assets/load-more-files.png)

### Nieuw basislijndashboard

AEM Guides 4.1 release biedt de functie Basislijn die in de webeditor is geïntegreerd. U kunt basislijnen van de Redacteur van het Web nu tot stand brengen en hen gebruiken om onderwerpen van verschillende versies te publiceren of te vertalen.

**Nota**: Voor promotiesysteem, te werk gelieve recentste **ui_config.json** voor het Profiel van de Omslag bij.

Gebruik deze functie om een basislijn met een specifieke versie van de onderwerpen tot stand te brengen beschikbaar op een specifieke datum en een tijd. Bovendien kunt u met de API-ondersteuning een basislijn maken of bijwerken met een label dat is gedefinieerd voor een versie van onderwerpen.

![ basislijn beheert lusje ](assets/baseline-manage.png)

U kunt de bestanden doorzoeken op bestandsnamen of op de bestandslocatie. U kunt ook de onderwerpen filteren die in het basislijnbewerkingsvenster moeten worden weergegeven en ze sorteren op basis van specifieke kolommen.

![ basislijn beheert lusje ](assets/baseline-filter.png)

De prestaties voor het basisproces voor het maken zijn verder verbeterd. Het proces om basislijnen tot stand te brengen is asynchroon, zodat kunt u andere dossiers in de Redacteur van het Web blijven uitgeven terwijl de basislijn wordt gecreeerd. Voor meer details, zie *basislijnen van de Redacteur van het Web* tot stand brengen en beheren in de Gebruikende gids van Adobe Experience Manager Guides.

Opmerking: het tabblad Basislijn op het kaartdashboard is standaard verborgen. Uw beheerder kan het lusje van de Basislijn op het kaartdashboard toelaten.

* De basislijnparameter in de API&#39;s die u wilt downloaden, gebruikt nu de titel van de basislijn om de versie van de inhoud op te halen.

### Verbeterd vertaalproces

* **Mogelijkheid om een scoping vertaalproject** tot stand te brengen
Als u slechts het werkingsgebied voor een te vertalen project moet tot stand brengen, kunt u **selecteren creeert een nieuw scoping vertaalproject**. Hierdoor worden de kopieën niet voor vertaling verzonden en blijft de oorspronkelijke vertaalstatus van de bestanden behouden.

![ scoping vertaalproject ](assets/scoping-translation-project.png)

* De **Talen** lijst toont de taalomslagen samen met hun taalcodes. Bijvoorbeeld Frans (fr) en Duits (de).

![ taal vertaalde vertaling ](assets/translation-languages.png)

Voor meer details op vertaling, zie *documenten van de sectie van de Redacteur van het Web* in het Gebruiken van de gids van Adobe Experience Manager Guides vertalen.


### Verbeterde publicatie

* U kunt tot het **dashboard van Publish** van het lusje van Output ook toegang hebben terwijl u output van het kaartdashboard produceert. In het Publish-dashboard vindt u een lijst met alle actieve publicatietaken.

![ een rij gevormde output ](assets/queued-output.png)

* Via het kaartdashboard kunt u meerdere DITAVAL-bestanden selecteren om geconditioneerde inhoud te genereren. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. U kunt de muisaanwijzer ook boven de bestandsnaam plaatsen om het pad te zien in de AEM opslagplaats waar het bestand is opgeslagen.

* De basislijnen zijn gerespecteerd voor de metagegevens van AEM site-uitvoer. U kunt de eigenschappen van een basislijnversie ook als metagegevens verwerken. Als geen basislijn wordt bepaald, dan worden de eigenschappen van de recentste versie verwerkt als meta-gegevens.

* De **Naam van het Dossier** en **DITA-OT de Argumenten van de Lijn van het Bevel** opties zijn toegevoegd voor HTML5, EPUB, en de output van de Douane vooraf instelt. U kunt nu de bestandsnaam opgeven waarmee u de uitvoer wilt opslaan. U kunt ook de aanvullende argumenten opgeven die u met DITA-OT wilt verwerken tijdens het genereren van uitvoer.

### Kaartdashboard

Wanneer u selecteert om de kaart te downloaden DITA, wordt het verzoek een rij gevormd, en u ontvangt een bericht zodra de kaart klaar is om te downloaden. U kunt ervoor kiezen het kaartbestand direct te downloaden of later te downloaden via de koppeling in het AEM-meldingsvak.

![ download van de Kaart ](assets/download-map-prompt.png)

### Andere functies

* AEM Guides ondersteunt nu Oxygen XML Author versie 24.1.
* De basislijnparameter in de API&#39;s die u wilt downloaden, gebruikt nu de titel van de basislijn om de versie van de inhoud op te halen.

### Verouderde functie

AEM Guides biedt geen ondersteuning meer voor het genereren van de DITA-uitvoerindeling voor FrameMaker-documenten. Deze optie DITA is ook verwijderd uit de uitvoervoorinstellingen van het kaartdashboard.

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

* Ontwerpondersteuning is niet beschikbaar als alternatief voor bestandspaden die verwijzen naar publicatie. 8076
* Met DITA toevoegen op pakket voorkomt u dat elementen door DAM worden gedupliceerd. 8417
* Nadat een document van Oxygen naar AEM is ingecheckt, wordt Japanse inhoud in het document vervangen door vraagtekens (????). (9124)
* Uitgecheckte bestanden vernieuwen werkt niet aan registratie met webverificatie in Oxygen. (9179)
* Het bestand wordt niet uitgecheckt wanneer het wordt geopend in zuurstof. (9192)
* Nadat een document van Oxygen naar AEM is ingecheckt, wordt Japanse inhoud in het document vervangen door vraagtekens (????). 9276
* Webverificatie werkt niet in oxygen. 9296
* Herladen mislukt in zuurstof wanneer het bestand of de bestanden al in AEM op dezelfde locatie aanwezig zijn. 9328
* Optie is niet beschikbaar als u inhoud tussen AEM en het lokale systeem wilt synchroniseren. 9439
* Identiteitskaart wordt niet automatisch geproduceerd voor element dat gebruikend **wordt toegevoegd herbruikbare inhoud** dialoog van secundaire hulpmiddelbar Tussenvoegsel. 5826
* Er wordt geen bevestigingsvenster weergegeven wanneer u via de editor een afbeelding met dezelfde naam als een bestaand bestand uploadt. (6011)
* Een vaste spatie die niet beschikbaar is in het tekenpalet. 7523
* De elementenlijst (Alt+Enter) wordt grijs weergegeven in het thema Donkerder/Donkerst. 7913
* Versie wordt niet bijgewerkt bij het opslaan van de revisie van een onderwerp op de werkbalk van het kaartvenster. (8228)
* xref kan zelfs op geldige locaties niet worden ingevoegd. 8354
* De bewerking &#39;getversionlabels&#39; heeft beperkingen en levert geen verwachte prestaties. 8513
* Problemen treden op met het bevestigingsvenster wanneer een vergrendeld of bewerkt bestand wordt gesloten dat momenteel niet in de editor is geopend. 8692
* Er treedt een fout op bij het toevoegen van een gebruiker als beheerder in het mappenprofiel als de gebruiker-id numeriek is. 8908
* Het deelvenster Vertaling is zelfs zichtbaar bij het openen van de DITA-kaart in de Kaarteditor. 9053
* Taalcode wordt niet weergegeven met de taal in het deelvenster Vertaling. (9108)
* De tabbladen Vertaling en Basislijn zijn enige tijd zichtbaar op het dashboard van Kaart. (9146)
* Wanneer de vertaling is voltooid, wordt een extra versie gemaakt voor het vertaalde element. 9310
* Goedgekeurde vertaling kan niet worden geïntegreerd in de doeltaal wanneer de doeltaalcode vijf tekens bevat, zoals `fr_ca` . 9357
* Vertaalde inhoud wordt verbroken wanneer de gemaakte doeltaalcode wordt aangeduid als `fr-fr, `, `en-us` . 9527
* Bij het laden van een kaart DITA die buiten de taalomslag is, wordt een uitzondering geregistreerd bij het achtereind.9543
* Kan geen DITA-bestand maken met de aangepaste DITA-sjabloon uit de editor. 7262
* De DITA-kaart gaat verloren bij het publiceren van een UUID DITA-kaart via FMPS. 7278
* AEM Guides kopieert de niet-unieke eigenschappen van een element niet wanneer een element wordt gekopieerd en geplakt. 8241
* De bestandsnaam van de DITA-kaart wordt bij het maken niet omgezet in kleine letters. 8383
* De beschrijving van de controletaak wordt niet weergegeven in het e-mailbericht dat wordt verzonden wanneer een nieuwe controletaak wordt toegewezen. 8507
* Map-API downloaden | Tijdelijke mappen die niet worden opgeschoond in geval van fouten in het downloadproces. 8523
* `columnpreview.jsp` is afhankelijk van SP.  8543
* Uitvoertaken met de status &quot;Wachten&quot; of &quot;Uitvoeren&quot; worden niet opgeschoond in het Publish-dashboard.  8569
* Standaardpictogram gekozen bij het produceren van een rapport gebruikend de Generate knoop, zelfs wanneer het pictogrambezit wordt bepaald. 8573
* Problemen treden op tijdens het revisieproces tijdens het upgraden van 3.8.X naar 4.0. (8788)
* Als een gebruikersnaam lang is in het deelvenster Revisie van de webeditor, worden de pictogrammen die u wilt accepteren/afwijzen niet duidelijk weergegeven. 8793
* De boomeinden van de verwijzing na het verwijderen van een onderwerp en het uitvoeren van een bewegingsverrichting. (8804)
* Aangepaste DTD die door de gebruiker is gedefinieerd, heeft geen voorrang op standaard-DITA DTD die is ingesloten in DITA-OT. (9104)
* De positie van markering is onjuist in de weergave Naast elkaar. 9305
* Met de voetnoot &#39;Bij gebruik naar referentie&#39; wordt niet naar de voetnootsectie in AEM site-uitvoer geschoven. 9061
* De volgorde van voetnoten is onjuist in de uitvoer AEM Site. 9327
* Nieuw gemaakte DITA-elementen worden altijd uitgecheckt door een andere gebruiker. 9387
* Fout wordt altijd geregistreerd op de verwezenlijking van nieuwe inhoud. (9388)
* In het derde scherm van het proces voor het maken van revisietaken wordt de lijst met woordenlijsten niet weergegeven. 4558
* Onjuiste UUID-referenties toegewezen bij het uploaden van meerdere bestanden van de FrameMaker/Zuurstofconnector. 8269
* E-mailmelding wordt niet verzonden wanneer een revisietaak opnieuw wordt toegewezen in het Postvak IN. 8376
* De tweede beheerdergebruiker kan niet als eerste beheerdergebruiker aan een omslag worden toegevoegd. 8430
* **pas de dialoog van Etiketten** op het lusje van de Basislijn toe toont geen etiketten in dropdown. 8455
* Bij het gebruiken van basislijnpubliceren met beeld als conref in het onderwerp, wordt het beeld niet gepubliceerd in de output. 8564
* De functie Uitvoer leegmaken mislukt als er een groot aantal knooppunten in de uitvoergeschiedenis aanwezig zijn. 8568
* In het deelvenster Versiehistorie wordt in de huidige sectie een onjuiste tijdstempel weergegeven en deze wordt door informatie gewijzigd. 8765
* Basislijn niet bijgewerkt op basis van het gedefinieerde label. 8799
* De fout komt voor wanneer de dossiers de waarvan ouderomslag speciale karakters in filename heeft, in Zuurstof (gebruikend **uitgeeft in Zuurstof** knoop) worden geopend. 8918
* Uploaden van bestanden van Oxygen naar AEM mislukt. (9157)
* Kaart downloaden met basislijn werkt niet als de inhoud naar een andere map wordt verplaatst. (9331)
* Zuurstof controleert een onjuiste versie van een onderwerp nadat een versie in AEM terugkeert. (9411)
* Als u in het deelvenster Opslagplaats zoekt en in het dialoogvenster Bladeren op onderwerp bladert, wordt het scherm geblokkeerd wanneer de inhoud groot is. 9432
* Als het plaatsen **Nieuwe Versie voor Geüploade Dossier** creeert is, wordt een nieuwe versie gecreeerd bij het terugkeren en het bewaren op om het even welke bevroren knoop. 9473
* Onjuiste tijdstempelverschillen worden weergegeven in de gebruikersinterface van Assets bij het terugkeren van een bestandsversie. 9480
* Bestanden worden automatisch uitgecheckt wanneer u terugkeert naar een willekeurige versie. 9482
* Het vergrendelingspictogram wordt weergegeven in de dataweergave, zelfs als het bestand is ingecheckt in de editor.  5756
* Onbekwaam om voorgrond, achterstandselementen in een boekenkaart toe te voegen gebruikend de mening van de Auteur van de Redacteur van het Web. 7652
* De modus Voorbeeld ondersteunt het kenmerk voor voorwaardelijke verwerking van `deliveryTarget` niet in DITA. 7685
* Wanneer u een woordenlijst opent in de XML-editor, AEM u een bestand op om het op te slaan, zelfs als het niet is gewijzigd. 8105
* Het dialoogvenster Referenties invoegen wordt geopend wanneer u subjectref aan een kaart toevoegt met behulp van de gebruikersinterface. 8212
* Het deelvenster Inhoud opnieuw gebruiken crasht bij het zoeken naar speciale tekens `[` of `*` .8279
* Bij het ontwerpen van Glossentry, toont de Redacteur van het Web de inhoud als Nota. 8384
* De Redacteur van XML verwijdert nieuwe lijn in codeblock. 8522
* Het schakelen tussen bron en auteurswijze merkt het onderwerp als vuil en vereist dat de inhoud opnieuw wordt bewaard.8524
* Kan een ontgrendeld onderwerp niet sluiten. 8545
* Er bestaat geen optie om het pad Knowledge Base te kiezen in voorinstellingen voor publiceren op basis van artikelen. 8636
* Kenmerken ontbreken bij het toevoegen van een hoofdstuk aan een bladwijzer met behulp van slepen en neerzetten in de weergave Favorieten. 8746
* Het dialoogvenster Trefwoord invoegen beschikt niet over de zoekmogelijkheden en trefwoorden worden niet in gesorteerde volgorde weergegeven. 9094
* Als u een zoekopdracht uitvoert in de XML-editor, wordt de pagina vastgezet. 9452
* Sites ontbreken in AEM voorinstellingen onder het tabblad Uitvoer. 9567
* SVG-afbeeldingen die niet correct worden weergegeven in de auteurmodi van de XML-editor. 9426
* Basislijn wordt niet geëerd tijdens het publiceren via salesforce. 8953
* De mogelijkheid om een routekaart te wissen uit de voorkeursinstellingen van de gebruiker is niet aanwezig. 8534
