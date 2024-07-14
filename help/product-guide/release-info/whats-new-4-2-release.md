---
title: Opmerkingen bij de release | Nieuwe functies in Adobe Experience Manager Guides 4.2-release
description: Leer de nieuwe en verbeterde functies in 4.2-versies van Adobe Experience Manager Guides
exl-id: 46367ccf-58ff-4889-8314-cdd5bf5d0f1d
feature: What's New
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '2423'
ht-degree: 0%

---

# Nieuwe functies in de release 4.2 van Adobe Experience Manager Guides (februari 2023)

Dit artikel behandelt de nieuwe en verbeterde eigenschappen in versie 4.2 van Adobe Experience Manager Guides (later die als *wordt bedoeld AEM Guides*).

Voor meer details op de verbeteringsinstructies, verenigbaarheidsmatrijs, en de kwesties die in deze versie worden bevestigd, zie het [ de nota&#39;s van de Versie ](release-notes-4-2.md) artikel.

## Rapporten genereren vanuit de webeditor

AEM Guides wordt geleverd met een functie in de webeditor waarmee u de algehele volledigheid van uw technische documenten kunt controleren en rapporten voor deze documenten kunt genereren.
U kunt de onderwerpenlijst bekijken en de meta-gegevens van alle verwijzingen voor de huidige kaart van
**Rapporten** lusje in de Redacteur van het Web.

**produceer de mening van de Lijst van het Onderwerp**

U kunt de Lijst van het Onderwerp produceren die gedetailleerde informatie over uw onderwerpen, zoals het verwijzingstype, documentstaat, en auteur verstrekt. U kunt CSV ook produceren om de huidige momentopname van de onderwerpen in de kaart te downloaden DITA.

**beheert meta-gegevens en verandert documentstaat**

U kunt markeringen op een individueel onderwerp toepassen of de bulketiketterende eigenschap gebruiken om veelvoudige markeringen op veelvoudige onderwerpen, een kaart DITA, of een sub-kaart toe te passen. U kunt de documentstatus van alle geselecteerde onderwerpen ook wijzigen in de volgende mogelijke algemene documentstatus.

<img src="assets/web-editor-metadata-panel.png" alt="metagegevens beheren" width="600">

## Nieuwe UX voor de revisiefunctionaliteit

AEM gidsen verstrekt nu een betere UX die u helpt de onderwerpen herzien die voor overzicht worden gedeeld. In de meest recente ervaring zijn de volgende verbeteringen beschikbaar voor de revisiefunctionaliteit:

* Vernieuwde gebruikersinterface
* Het paneel van voorwaarden dat u toestaat om de inhoud volgens de beschikbare voorwaarden in het onderwerp te benadrukken.
* Elke opmerking in het opmerkingenvenster is gekoppeld aan de corresponderende tekst in het huidige onderwerp. Hiermee kunt u de tekst met opmerkingen herkennen.
* De opmerkingen worden weergegeven in de volgorde van de tekst met opmerkingen in het document.
* De naam van de revisietaak wordt weergegeven in de revisiewerkstroom.
* Selecteer de routekaart voor de overzichtstaak die wordt gebruikt om alle belangrijkste verwijzingen en verklarende woordenlijsttermijnen op te lossen die in de overzichtsinhoud worden gebruikt.
* Contextuele werkbalk waarmee u tekst snel kunt markeren of doorhalen.
* Met het menu Opties kunt u uw eigen opmerkingen bewerken of verwijderen.
* Voor verouderde opmerkingen hebt u toegang tot de weergave Naast elkaar, zodat u de vorige versie van het onderwerp kunt vergelijken met de huidige revisieversie
* Wanneer u de filters gebruikt, worden de opmerkingen in het rechtervenster gefilterd op basis van de selectie en de
Het aantal opmerkingen in het linkervenster wordt dienovereenkomstig bijgewerkt.


<img alt="controletaak" src="assets/comment-pop-up-panel.png" width="600">


Voor meer details, verwijs naar de *onderwerpen van het Overzicht of kaarten* sectie in de Gebruikende gids van Adobe Experience Manager Guides.

## Verbeterde vertaling

Nu hebt u gebruikersvriendelijkere verhogingen in het Dashboard van de Vertaling die u helpen uw documenten van de Redacteur van het Web gemakkelijk vertalen.


**kolom van het Etiket van de Versie die aan het vertaaldashboard** wordt toegevoegd

In het vertaaldashboard, kunt u de kolom van het Etiket van de Versie ook zien. Hierdoor wordt het label voor de geselecteerde versie van het bronbestand weergegeven. Hiermee kunt u alle bestanden met een specifiek label selecteren en in één keer vertalen.

**de versieverschil van de Mening voor uit de dossiers van de Synchronisatie van het vertaaldashboard**

Nu kunt u de verschillen tussen de geselecteerde versie en de laatste vertaalde bronversie van de onderwerpen controleren. U kunt ook verkiezen om **uit de dossiers van de Synchronisatie** te vertalen die op de veranderingen worden gebaseerd die tussen de twee versies van een onderwerp worden gedaan.

<img src="assets/translation-version-diff.png" alt="vertaalbord" width="600">



**ga het versielabel tot de doelversie** over

Met AEM Guides kunt u het label van het bronbestand aan het doelbestand doorgeven. Zo kunt u gemakkelijk de bronversie van het vertaalde bestand identificeren.

<img alt="vertaallabels" src="assets/translation-pass-source-label.png" width="600">

Als er bijvoorbeeld bronbestanden zijn waarop het versielabel Release 1.0 is toegepast, kunt u ook het bronlabel (Release 1.0) aan het vertaalde bestand doorgeven.

**de synchronisatie van de Dwingskracht voor uit synchrone activa**

Als u wijzigingen aanbrengt in sommige elementen, markeert AEM Guides deze als Uit-synchroon. U kunt de gewijzigde elementen opnieuw vertalen of de status Niet-gesynchroniseerd negeren. Als u bijvoorbeeld enkele kleine wijzigingen hebt aangebracht waarvoor geen vertaling nodig is, kunt u de status van de wijzigingen markeren als Bij synchroniseren.

**Mening Bezig vertaalprojecten voor een onderwerp of kaart**

Sommige verwijzingen op het vertaaldashboard zijn mogelijk in uitvoering. AEM Guides beschikt nu over een functie waarmee u de lijst kunt weergeven met alle vertaalprojecten in uitvoering (samen met de doeltaal) die de geselecteerde verwijzing bevatten.

Voor meer details, verwijs naar *vertaalde documenten van de sectie van de Redacteur van het Web* in de Gebruikende gids van Adobe Experience Manager Guides.

## Produceer output in diverse formaten van de Redacteur van het Web

Nu kunt u de output voor uw onderwerpen of kaart DITA van de Redacteur van het Web gemakkelijk produceren. U kunt verschillende uitvoervoorinstellingen configureren, zoals AEM Site, PDF, HTML5,
JSON (een uitvoerindeling zonder kop) en aangepaste uitvoer. Gebruik deze om de respectieve output te produceren. U kunt attributen in uw onderwerpen bepalen DITA en dan de voorwaarde gebruiken vooraf ingesteld om een voorwaarde toe te passen terwijl het publiceren van de output. U kunt de het publiceren eigenschap van de Basislijn ook gebruiken om een specifieke versie van uw kaart DITA of onderwerp selectief te publiceren.

**beheer Globale en de outputpresets van het Profiel van de Omslag**

AEM Guides biedt u de functie om uitvoervoorinstellingen voor de algemene profielen en mapprofielen te maken en te beheren. Vervolgens kunt u deze uitvoervoorinstellingen eenvoudig gebruiken om uitvoer te genereren voor alle mappen die betrekking hebben op dat algemene profiel of mapprofiel.

<img alt="voorinstelling toevoegen" src="assets/add-global-output-preset.png" width="400">


Deze globale voorinstellingen verschijnen onder het **lusje van de Output** van alle verwante kaarten. U kunt ze gebruiken om de uitvoer voor alle verwante kaarten te genereren. U kunt de voorinstelling selecteren als de standaardvoorinstelling PDF om de PDF-uitvoer te genereren. U kunt ook **uitgeven**, **anders noemen**, **Dupliceren**, of **schrapt** een bestaande output vooraf ingesteld van het **menu van Opties**.

>[!NOTE]
>
>Alleen gebruikers met beheerdersrechten op mapniveau kunnen voorinstellingen voor algemene profielen en mapprofielen maken.

## Tekst zoeken en vervangen op kaartniveau

U kunt nu zoeken naar bestanden in een kaart die specifieke tekst bevatten. De gezochte tekst wordt benadrukt in de dossiers. U kunt het gezochte woord of de gezochte uitdrukking met een ander woord of een uitdrukking binnen de dossiers ook vervangen. Selecteer **vervangen enig voorvalpictogram** om het huidige voorkomen te vervangen en **vervangen allen in het pictogram van het Dossier** om alle voorkomen in het geselecteerde dossier te vervangen. U kunt **selecteren vervangt Al** pictogram om alle voorkomen van de gezochte termijn in alle dossiers te vervangen.

<img src="assets/map-find-replace.png" alt="map zoeken vervangen" width="600">


Door gebrek, worden het dossier van de optiecontrole **alvorens** te vervangen en **nieuwe versie na vervangen** geselecteerd, zodat wordt een dossier gecontroleerd alvorens u de tekst vervangt, en een nieuwe versie wordt gecreeerd nadat de tekst wordt vervangen. U kunt de tekenreeks ook doorzoeken in de indirecte verwijzingen in de DITA-kaart. Deze optie is standaard uitgeschakeld, zodat de zoekopdracht alleen op de directe referenties wordt uitgevoerd.

## Layoutweergave in de Kaarteditor


Nu kunt u de volledige lay-out van een kaart DITA in de Redacteur van de Kaart bekijken. Wanneer u een kaart opent om te bewerken, wordt de layoutweergave van de Kaarteditor geopend. In deze weergave ziet u de kaarthiërarchie in een boomstructuurweergave. U kunt de onderwerpen in een kaart ook bewerken en ordenen of structureren.

<img src="assets/layout-view-map.png" alt=" layoutweergave" width="600">

De layoutweergave bevat een aparte werkbalk waarmee u veel taken kunt uitvoeren op de onderwerpen in een kaart.
U kunt onderwerpverwijzingen, onderwerpgroep, zeer belangrijke definities in een kaart opnemen. U kunt de onderwerpen in een kaart reorganiseren door ze omhoog, omlaag, links of rechts te verplaatsen. U kunt de onderwerpen ook slepen en neerzetten om ze in een kaart te verplaatsen. De Kaarteditor verstrekt ook de pictogrammen om dossiers te sluiten of te ontgrendelen, de versiegeschiedenis te controleren, en een beheer van het versielabel te doen.


De mening van de Lay-out verstrekt ook de **Opties van de Mening** om lijnaantal te tonen of te verbergen, controledoos te tonen of te verbergen, of de dossiernaam of titel voor de onderwerpen in een kaart te tonen.
U kunt de onderwerpen ook bekijken die op de voorwaardelijke filters worden gebaseerd die op hen worden toegepast.

Naast het organiseren van onderwerpen in het kaartdossier, kunt u ook toevoegen, bewegen, kopiëren, kleven, of verwijzingen schrappen gebruikend het **menu van Opties** beschikbaar voor een element in de mening van de Lay-out.

<img src="assets/layout-inline-attributes.png" alt=" toewijzingskenmerken" width="600">


In het rechterdeelvenster worden de eigenschappen Inhoud en Kaart weergegeven in de layoutweergave van de Kaarteditor. Nu kunt u de meta-gegevensinformatie voor de onderwerpen of de kaart ook plaatsen. U kunt de Titel Nav, de Tekst van de Verbinding, Korte Beschrijving, en Sleutelwoorden voor het geselecteerde onderwerp of de kaart bepalen.

Voor meer details, zie *sectie van de mening van de Lay-out van 0} in de Gebruikende gids van Adobe Experience Manager Guides.*

## Deelvenster Snel genereren

AEM Guides beschikt nu over het deelvenster Snel genereren waarmee u snel de uitvoer kunt genereren en weergeven voor voorinstellingen die voor uw DITA-kaart zijn gemaakt.

<img src="assets/quick-generate-map-view.png" alt=" snel genereren, deelvenster" width="600">

In **snel produceert** paneel, kunt u de lijst van alle die outputvoorinstellingen zien voor uw kaart DITA worden gecreeerd. U kunt ook snel de uitvoer weergeven die voor de voorinstellingen is gegenereerd. Er wordt een geluids- of foutbericht weergegeven als de uitvoer is gegenereerd. U kunt het foutenlogboek ook bekijken dat details van de fout bevat die in het generatieproces voorkwam.

## Een dynamische basislijn maken op basis van labels

AEM Guides beschikt nu over de functie om dynamische basislijnen te maken op basis van labels. Als u een basislijn genereert, een basislijn downloadt of een vertaalproject maakt met een basislijn, worden de bestanden dynamisch gekozen op basis van de bijgewerkte labels. Deze eigenschap is handig aangezien u niet de basislijn moet wijzigen wanneer het bijwerken van de etiketten.

<img src="assets/dynamic-baseline.png" alt=" dynamische basislijn" width="400">

## Bestanden verwijderen en dupliceren uit het deelvenster Verplaats

Nu kunt u dossiers (enig dossier tegelijkertijd) van het **menu van Opties** van het geselecteerde dossier van het bewaarplaatspaneel gemakkelijk schrappen. Er wordt een bevestigingsbericht weergegeven voordat u het bestand verwijdert. Als er vanuit een ander bestand niet naar het bestand wordt verwezen, wordt het bestand verwijderd en wordt een succesbericht weergegeven.

<img src="assets/options-menu-repo-view-file-level.png" alt="menu met bestandsopties " width="500">

U kunt ook een kopie of kopie van het geselecteerde bestand maken. Standaard wordt het bestand gemaakt met
een achtervoegsel (zoals filename_1.extension).


## Andere verbeteringen in de webeditor

* In AEM Guides kunt u via het contextmenu enkele veelvoorkomende bewerkingen voor afbeeldingen en mediabestanden uitvoeren. Nu kunt u ook de geselecteerde afbeelding of media vinden in de opslagplaats of de voorvertoning van het bestand bekijken in de gebruikersinterface van Assets.

* De naam van het huidige mapprofiel wordt weergegeven als een label voor het pictogram Gebruikersvoorkeuren op de hoofdwerkbalk. Zo kunt u het mapprofiel identificeren waaraan u werkt.

* Wanneer u een kaart opent in de kaartweergave, wordt de titel van de huidige kaart weergegeven in het midden van de hoofdwerkbalk. Dit is handig om de gebruikers te laten weten welke kaart momenteel is geopend.

## Geselecteerde versies van bestanden wissen

Terwijl u inhoud maakt en onderhoudt, worden mogelijk veel versies gemaakt voor uw DITA-bestanden in uw opslagplaats. Met AEM Guides kunt u oudere versies van uw DITA-bestanden uit de opslagplaats verwijderen en schijfruimte vrijmaken.

<img src="assets/preview-purge-report.png" alt="Voorvertoning rapport leegmaken" width="500">

AEM Guides verwijdert niet de eerste versie van het bestand of een versie die in een basislijn is opgenomen, of heeft er een label op toegepast. Met Leegmaken worden zelfs geen bestanden verwijderd die deel uitmaken van een vertaling- of revisiewerkstroom. U kunt het aantal versies kiezen dat u wilt behouden en u kunt ook besluiten om de bestanden te verwijderen die ouder zijn dan het gedefinieerde aantal dagen.

Voordat u de purgeerbewerking start, kunt u een voorvertoning van het rapport bekijken van de versies die worden gewist. Vervolgens kunt u besluiten de leegmaakbewerking te starten of te annuleren.

<img src="assets/download-purge-report.png" alt="PDownload-rapport" width="500">

Zodra de leegmaakbewerking is voltooid, kunt u het rapport leegmaken controleren om de gezuiverde bestanden te zien.

## Titel weergeven in plaats van UUID in de Zuurstofbewerker

Nu staat AEM Guides u toe om **Titel van het Gebruik in Redacteur en de optie van de Manager van Kaarten** in Montages te kiezen. Als u deze optie selecteert, wordt de titel van het bestand weergegeven op het tabblad van het bestand wanneer het wordt geopend in de Editor of DITA Maps Manager. Als u deze optie niet selecteert, wordt de UUID van het bestand weergegeven op het tabblad van het bestand.

## Gebruikersinterface met metagegevens beschikbaar voor PDF-voorinstellingen

U kunt de metagegevens instellen vanuit de uitvoervoorinstelling van een DITA-kaart. U kunt de metagegevens Titel, Auteur, Onderwerp en Trefwoorden instellen. Deze metagegevens worden toegewezen aan de metagegevens in de bestandseigenschappen van de uitvoer PDF. Deze metagegevens overschrijven de metagegevens die op boekniveau zijn gedefinieerd. U kunt de metagegevens specifiek definiëren in elke uitvoervoorinstelling en deze doorgeven aan de PDF van de uitvoer.

## Native PDF | PDF met wijzigingsbalk die het verschil tussen documentversies aangeeft

Nu kunt u een PDF maken die de verschillen in inhoud tussen twee versies weergeeft met de wijzigingsbalk. U kunt de huidige versie vergelijken met een basislijn van de vorige versie of de twee geselecteerde basislijnversies vergelijken.

<img src="assets/pdf-change-version.png" alt="pdf-change-version" width="600">

Er wordt een wijzigingsbalk weergegeven in de PDF om de gewijzigde, ingevoegde of verwijderde inhoud aan te geven. U kunt ook het volgende doen:
* Ingevoegde inhoud in groene kleur en onderstreept weergeven
* De verwijderde inhoud rood weergeven en doorhalen

## Native PDF | Ondersteuning voor variabelen voor Uitvoerpad en bestandsnaam PDF

U kunt nu ook de volgende variabelen gebruiken om het uitvoerpad en het PDF-bestand te definiëren. U kunt een enkele of een combinatie van variabelen gebruiken om de volgende opties te definiëren:
* `${map_filename}`
* `${map_title}`
* `${preset_name}`
* `${language_code}`
* `${map_parentpath}` (Alleen voor uitvoerpad)
* `${path_after_langfolder}` (Alleen voor uitvoerpad)

## Native PDF | Inhoudsopgave genereren voor DITA-kaarten en de paginalay-outs opnieuw ordenen

Nu kunt u TOC in kaarten ook produceren DITA gebruikend een geavanceerde PDF het plaatsen van het malplaatje. U kunt de weergave van de verschillende paginalay-outs in- of uitschakelen en ook de positie ervan wijzigen.

## Native PDF | Een aangepaste bladwijzer toevoegen in PDF-uitvoer

Nu kunt u voor eenvoudige navigatie een aangepaste bladwijzer toevoegen aan een bepaalde inhoud in de uiteindelijke PDF-uitvoer. Dit zou aan TOC worden toegevoegd die van de onderwerp of sectietitels in uw kaart DITA wordt gecreeerd.

## Native PDF | Aangepaste stijl toepassen op inhoudsopgave-items en onderwerpinhoud

AEM Guides biedt de functie om aangepaste opmaak toe te passen op de inhoudsopgave-items of een bepaald onderwerp in de PDF-uitvoer. U kunt bijvoorbeeld de kleur wijzigen van de tekst in de inhoudsopgave en de titel van het onderwerp. U kunt stijlen ook toepassen op de volledige inhoud binnen het onderwerp.
