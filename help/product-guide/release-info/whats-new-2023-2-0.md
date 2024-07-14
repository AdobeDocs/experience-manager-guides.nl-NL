---
title: Opmerkingen bij de release | Adobe Experience Manager Guides as a Cloud Service, release februari 2023
description: Release van Adobe Experience Manager Guides as a Cloud Service in februari
exl-id: 090eaf94-fe3a-47e9-9937-f84f8434550d
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---

# Nieuwe functies in februari 2023 release van Adobe Experience Manager Guides as a Cloud Service

Dit artikel behandelt de nieuwe en verbeterde eigenschappen in versie Februari 2023 van Adobe Experience Manager Guides (later genoemd als *as a Cloud Service van AEM Guides*).

Voor meer details op de verbeteringsinstructies, verenigbaarheidsmatrijs, en de kwesties die in deze versie worden bevestigd, zie het [ de nota&#39;s van de Versie ](release-notes-2023-2-0.md) artikel.


## Rapporten genereren vanuit de webeditor

AEM Guides wordt geleverd met een functie in de webeditor waarmee u de algehele volledigheid van uw technische documenten kunt controleren en rapporten voor deze documenten kunt genereren.
U kunt de onderwerpenlijst bekijken, de meta-gegevens beheren en multimedia zien die in alle verwijzingen voor de huidige kaart van wordt gebruikt
**Rapporten** lusje in de Redacteur van het Web.

**produceer de mening van de Lijst van het Onderwerp**

U kunt de Lijst van het Onderwerp produceren die gedetailleerde informatie over uw onderwerpen, zoals het verwijzingstype, documentstaat, en auteur verstrekt. U kunt CSV ook produceren om de huidige momentopname van de onderwerpen in de kaart te downloaden DITA.

**beheert meta-gegevens en verandert documentstaat**

U kunt markeringen op een individueel onderwerp toepassen of de bulketiketterende eigenschap gebruiken om veelvoudige markeringen op veelvoudige onderwerpen, een kaart DITA, of een sub-kaart toe te passen. U kunt de documentstatus van alle geselecteerde onderwerpen ook wijzigen in de volgende mogelijke algemene documentstatus.

<img src="assets/web-editor-metadata-panel.png" alt="metagegevens beheren" width="600">

**produceer het Multimedia rapport**

U kunt het multimediapport genereren dat gedetailleerde informatie bevat over de multimedia die wordt gebruikt in uw verwijzingen in de huidige kaart. U hebt de flexibiliteit om de dossiers van verschillende media te filtreren en te sorteren die in het rapport worden vermeld.
U kunt CSV ook produceren om de huidige momentopname van multimedia te downloaden die in de kaart DITA wordt gebruikt.

<img src="assets/web-editor-reports-multimedia.png" alt="multimediapport" width="600">

## Nieuwe UX voor de revisiefunctionaliteit

AEM gidsen verstrekt nu een betere UX die u helpt de onderwerpen herzien die voor overzicht worden gedeeld. In de meest recente ervaring zijn de volgende verbeteringen beschikbaar voor de revisiefunctionaliteit:

* Vernieuwde gebruikersinterface
* Het paneel van voorwaarden dat u toestaat om de inhoud volgens de beschikbare voorwaarden in het onderwerp te benadrukken
* Elke opmerking in het opmerkingenvenster is gekoppeld aan de corresponderende tekst in het huidige onderwerp. Hiermee kunt u de tekst met opmerkingen herkennen.
* De opmerkingen worden weergegeven in de volgorde van de tekst met opmerkingen in het document.
* De naam van de revisietaak wordt weergegeven in de revisiewerkstroom.
* Selecteer de routekaart voor de overzichtstaak die wordt gebruikt om alle belangrijkste verwijzingen en verklarende woordenlijsttermijnen op te lossen die in de overzichtsinhoud worden gebruikt.
* Contextuele werkbalk waarmee u tekst snel kunt markeren of doorhalen
* Menu Opties voor het bewerken of verwijderen van uw eigen opmerkingen
* Voor verouderde commentaren, hebt u toegang tot zij-aan-zij mening die u helpt de vorige versie van het onderwerp met huidige overzichtsversie vergelijken.
* Wanneer u de filters gebruikt, worden de opmerkingen in het rechtervenster gefilterd op basis van de selectie en de
Het aantal opmerkingen in het linkervenster wordt dienovereenkomstig bijgewerkt.


  <img alt="controletaak" src="assets/comment-pop-up-panel.png" width="600">



## Verbeterde vertaling

Nu hebt u gebruikersvriendelijkere verhogingen in het Dashboard van de Vertaling die u helpen uw documenten van de Redacteur van het Web gemakkelijk vertalen.

**ga het versielabel tot de doelversie** over

Met AEM Guides kunt u het label van het bronbestand aan het doelbestand doorgeven. Zo kunt u gemakkelijk de bronversie van het vertaalde bestand identificeren.

<img alt="vertaallabels" src="assets/translation-pass-source-label.png" width="600">

Als er bijvoorbeeld bronbestanden zijn waarop het versielabel Release 1.0 is toegepast, kunt u ook het bronlabel (Release 1.0) aan het vertaalde bestand doorgeven.

**de synchronisatie van de Dwingskracht voor uit synchrone activa**

Als u wijzigingen aanbrengt in sommige elementen, markeert AEM Guides deze als Uit-synchroon. U kunt de gewijzigde elementen opnieuw vertalen of de status Niet-gesynchroniseerd negeren. Als u bijvoorbeeld enkele kleine wijzigingen hebt aangebracht waarvoor geen vertaling nodig is, kunt u de status van de wijzigingen markeren als Bij synchroniseren.

<img src="assets/translation-version-diff.png" alt="vertaalbord" width="600">

**Mening Bezig vertaalprojecten voor een onderwerp of kaart**

Sommige verwijzingen op het vertaaldashboard zijn mogelijk in uitvoering. AEM Guides beschikt nu over een functie waarmee u de lijst kunt weergeven met alle vertaalprojecten in uitvoering (samen met de doeltaal) die de geselecteerde verwijzing bevatten.


## Produceer output in diverse formaten van de Redacteur van het Web

Nu kunt u de output voor uw onderwerpen of kaart DITA van de Redacteur van het Web gemakkelijk produceren. U kunt verschillende uitvoervoorinstellingen configureren, zoals AEM Site, PDF, HTML5,
JSON (een uitvoerindeling zonder kop) en aangepaste uitvoer. U kunt deze vervolgens gebruiken om de respectievelijke uitvoerbestanden te genereren.

U kunt attributen in uw onderwerpen bepalen DITA en dan de voorwaarde gebruiken vooraf ingesteld om een voorwaarde toe te passen terwijl het publiceren van de output. U kunt de het publiceren eigenschap van de Basislijn ook gebruiken om een specifieke versie van uw kaart DITA of onderwerp selectief te publiceren.


## Tekst zoeken en vervangen op kaartniveau

Met AEM Guides kunt u zoeken naar bestanden op een kaart die specifieke tekst bevatten. De gezochte tekst wordt benadrukt in de dossiers. Nu kunt u ook het gezochte woord of de gezochte uitdrukking door een ander woord of een uitdrukking binnen alle dossiers vervangen. U kunt **selecteren vervangt Al** pictogram op het recht bij de bovenkant van de lijst om alle voorkomen van de gezochte termijn in alle dossiers te vervangen.

<img src="assets/map-find-replace.png" alt="map zoeken vervangen" width="600">

## Bestanden verwijderen en dupliceren uit het deelvenster Verplaats

Nu kunt u een duplicaat of een exemplaar van een dossier van het **menu van Opties** van het geselecteerde dossier in het bewaarplaatspaneel gemakkelijk tot stand brengen. Standaard wordt het bestand gemaakt met
een achtervoegsel (zoals `filename_1.extension` ).

<img src="assets/options-menu-repo-view-file-level.png" alt="menu met bestandsopties " width="500">


## Andere verbeteringen in de webeditor

* In AEM Guides kunt u via het contextmenu enkele veelvoorkomende bewerkingen voor afbeeldingen en mediabestanden uitvoeren. Nu kunt u ook de geselecteerde afbeelding of media vinden in de opslagplaats of de voorvertoning van het bestand bekijken in de gebruikersinterface van Assets.

* De naam van het huidige mapprofiel wordt weergegeven als een label voor het pictogram Gebruikersvoorkeuren op de hoofdwerkbalk. Zo kunt u het mapprofiel identificeren waaraan u werkt.

* Wanneer u een kaart opent in de kaartweergave, wordt de titel van de huidige kaart weergegeven in het midden van de hoofdwerkbalk. Dit is handig om de gebruikers te laten weten welke kaart momenteel is geopend.


## Titel weergeven in plaats van UUID in de Zuurstofbewerker

Nu staat AEM Guides u toe om **Titel van het Gebruik in Redacteur en de optie van de Manager van Kaarten** in Montages te kiezen. Als u deze optie selecteert, wordt de titel van het bestand weergegeven op het tabblad van het bestand wanneer het wordt geopend in de Editor of DITA Maps Manager. Als u deze optie niet selecteert, wordt de UUID van het bestand weergegeven op het tabblad van het bestand.

## Op microservices gebaseerde publicaties voor AEM Guides as a Cloud Service

Met de nieuwe publicatiemicroservice kunt u grote publicatiewerklasten tegelijkertijd uitvoeren op AEM Guides as a Cloud Service en het toonaangevende Adobe I/O Runtime-serverloze platform benutten.

Voor elke publicatieaanvraag voert AEM Guides as a Cloud Service een aparte container uit die horizontaal wordt geschaald volgens de gebruikersaanvragen. Hierdoor kunt u meerdere publicatieverzoeken uitvoeren en de prestaties verbeteren.

Voor meer details, zie [ nieuwe op microservice-gebaseerde het publiceren voor AEM Guides as a Cloud Service ](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/knowledge-base/publishing/configure-microservices.md) vormen.

## Native PDF | Een aangepaste bladwijzer toevoegen in PDF-uitvoer

Nu kunt u voor eenvoudige navigatie een aangepaste bladwijzer toevoegen aan een bepaalde inhoud in de uiteindelijke PDF-uitvoer. Dit zou aan TOC worden toegevoegd die van de onderwerp of sectietitels in uw kaart DITA wordt gecreeerd.

## Native PDF | Aangepaste stijl toepassen op inhoudsopgave-items en onderwerpinhoud

AEM Guides biedt de functie om aangepaste opmaak toe te passen op de inhoudsopgave-items of een bepaald onderwerp in de PDF-uitvoer. U kunt bijvoorbeeld de kleur wijzigen van de tekst in de inhoudsopgave en de titel van het onderwerp. U kunt stijlen ook toepassen op de volledige inhoud binnen het onderwerp.


## Native PDF | De paginamarkering in de voetnootcomponent opmaken

Nu kunt u de paginamarkering opmaken in de voetnoten. U kunt bijvoorbeeld vierkante haakjes toevoegen of de kleur ervan wijzigen. Met deze stijlen kunnen gebruikers gemakkelijk de paginamarkeringen in het document herkennen.

## Native PDF | De bar van de verandering om op veranderde onderwerpen in Inhoudsopgave te wijzen

AEM Guides staat u nu toe om de veranderde onderwerpen in TOC van de output van PDF snel te identificeren.  Het toont een veranderingsbar op de linkerzijde van de veranderde onderwerpen in TOC. U kunt op het onderwerp in TOC klikken en de gedetailleerde veranderingen bekijken.

<img src="assets/change-marker-toc.png" alt="Markeerteken in inhoudsopgave wijzigen " width="500">
