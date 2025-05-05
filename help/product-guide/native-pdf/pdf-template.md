---
title: Native PDF-sjablonen maken en aanpassen
description: Leer hoe u Native PDF-sjablonen maakt en aanpast.
exl-id: 7660da8e-8a1e-4493-b99b-9b5de9a7483f
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: a6c87e6f9a68962488e70985a0513dcb05eaa9cd
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# PDF-sjabloon {#PDF-template}

Het gebruik van een sjabloon zorgt voor consistentie in de indeling en structuur van de inhoud. Aangezien de malplaatjes vooraf worden bepaald, kunt u vermijden herwerk bij het formatteren kwesties die voor elk nieuw project of updates zich voordoen. Met sjablonen kunt u paginalay-outs ontwerpen, inhoud opmaken en verschillende instellingen toepassen om uw PDF aan te passen.

## Factory- en aangepaste PDF-sjablonen

Er zijn enkele voorbeeldfabriekssjablonen die uit de doos worden verzonden en die de ontwikkelaars kunnen gebruiken als basissjablonen om aangepaste sjablonen te maken op basis van hun organisatorische vereisten.



## Een nieuwe PDF-sjabloon maken {#create-pdf-template}

U kunt aangepaste PDF-sjablonen maken met specifieke paginalay-outs en opmaak definiëren voor pagina-indelingscomponenten (zoals inhoudsopgave, index, woordenlijst) of DITA-componenten (zoals koptekst, alinea, lijst) met behulp van opmaakmodellen.

Voer de volgende stappen uit om een nieuwe PDF-sjabloon te maken:

1. In de Redacteur van het Web, ga naar de **Output** tabel.
1. Selecteer **Malplaatjes** <img src="./assets/template.png" alt= "sjabloonpictogram" width="25"> in het linkerdeelvenster.

   <img src="assets/create-pdf-template.png" alt="PDF-sjabloon maken" width="400">

1. In het **venster van Malplaatjes**, selecteer **+** pictogram naast **Malplaatjes** en kies **Malplaatje van de PDF**.
1. In het **Nieuwe PDF Malplaatje** dialoog, selecteer een fabrieksmalplaatje dat u als basis wilt gebruiken om het douanemalplaatje tot stand te brengen. U kunt ook het zoekvak gebruiken om te zoeken naar een sjabloon.
1. Geef een titel voor de sjabloon op.

   >[!NOTE]
   >
   >  U kunt ook een miniatuur voor de sjabloon voorvertonen terwijl u een sjabloon maakt en dupliceert. Bewerk of schrap de duimnagel gebruikend [**Eigenschappen**](#properties-option) in het **menu van Opties** na het creëren van het malplaatje.

1. Klik **creëren**.

   Het nieuwe malplaatje wordt gecreeerd en in het **paneel van Malplaatjes** toegevoegd.

## Een PDF-sjabloon dupliceren {#duplicate-pdf-template}

Als u een nieuwe sjabloon wilt maken met dezelfde paginalay-outs en opmaak als die van een bestaande sjabloon, kunt u een kopie maken. Nadat een sjabloon is gedupliceerd, kunt u de componenten ervan naar wens verder aanpassen.

Voer de volgende stappen uit om een bestaande PDF-sjabloon te dupliceren:

1. In de Redacteur van het Web, ga naar de **Output** tabel.
1. Selecteer **Malplaatjes** <img src="./assets/template.svg" alt= "sjabloonpictogram" width="25"> in het linkerdeelvenster. Dit opent het **venster van Malplaatjes**.
1. Beweeg over het malplaatje dat u **wilt dupliceren en selecteren...** *het pictogram van Opties* en kiest **Dupliceren** van het contextmenu.

   Dit opent de **Dubbele PDF Malplaatje** dialoog.

   <img src="assets/duplicate-template.png" alt="PDF-sjabloon dupliceren" width="350">

   *selecteer een malplaatje om te dupliceren, de duimnagel voor te vertonen, en de titel in de **Dubbele PDF Malplaatje**&#x200B;dialoog bij te werken.*

1. Geef een titel voor de sjabloon op.

   Het **gebied van de Titel** is pre-bevolkt als exemplaar van de zelfde titel zoals het bronmalplaatje. Er verschijnt een foutbericht als de sjabloon met dezelfde titel bestaat.



1. Als u een voorkeurstitel wilt opgeven, verwijdert u de vooraf ingevulde titel en geeft u een titel op.
1. Klik **Dupliceren**.

   Een dubbel malplaatje wordt gecreeerd en onder de **Malplaatjes** toegevoegd.

## Andere bewerkingen op de sjablonen

U kunt de volgende verrichtingen op de malplaatjes van het **menu van Opties {ook uitvoeren 1}:**

<img src="assets/PDF-template-options.png" alt="PDF-sjabloon dupliceren" width="350">

### Verwijderen

Selecteer de optie Verwijderen om de geselecteerde sjabloon te verwijderen. Selecteer vervolgens Ja op de bevestigingsvraag.
Vooraf ingesteld wordt verwijderd uit de **Malplaatjes**.

### Eigenschappen{#properties-option}

Selecteer deze optie om de eigenschappen van de sjabloon weer te geven en te bewerken. U kunt een voorvertoning van de bestaande miniatuur voor de sjabloon weergeven. U kunt de miniatuur ook bewerken of verwijderen. U kunt ook de titel en beschrijving van de sjabloon wijzigen.

### Weergeven in gebruikersinterface van Assets

Selecteer deze optie om de sjabloon weer te geven in de gebruikersinterface van Assets. Aangezien het de wortelplaats van het malplaatje opent, kunt u alle middelen van het malplaatje bekijken.

Nadat u de aangepaste sjabloon hebt gemaakt, kunt u deze kiezen in de paginalay-outs in de voorinstelling voor PDF-uitvoer.

Leer hoe te om [ een output van PDF ](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/user-guide/output-gen/web-editor/native-pdf-web-editor.html?lang=en) te publiceren.

>[!NOTE]
>
>Als voor uw map een mapprofiel is geconfigureerd, worden alleen de PDF-sjablonen weergegeven die in het mapprofiel zijn geconfigureerd.

Gebaseerd op uw opstelling kan uw beheerder de malplaatjes vormen:

+++ Cloud Servicen

Voor details bij vestiging globale en omslag-vlakke profielen, de mening [ vormt malplaatjes ](../cs-install-guide/conf-folder-level.md#id1889D0IL0Y4) sectie in de Installatie en configuratiegids voor Cloud Servicen.

+++

+++ Software op locatie

Voor details bij vestiging globale en omslag-vlakke profielen, de mening [ vormt auteursmalplaatjes ](../install-guide/conf-folder-level.md#create-custom-authoring-template-id1917d0eg0hj) sectie in de On-premise gids van de Installatie en van de configuratie.

+++

## Een PDF-sjabloon aanpassen {#customize-pdf-template}

U kunt sjablonen aanpassen door de sjablooncomponenten aan te passen en stijlindelingen toe te passen aan de hand van opmaakmodellen.

Voer de volgende stappen uit om een PDF-sjabloon aan te passen:

1. In de Redacteur van het Web, ga naar de **Output** tabel.
1. Breid linkerzijbalk uit en selecteer **Malplaatjes**.

   Dit opent het **paneel van Malplaatjes**.

1. Voer een van de volgende handelingen uit om de componenten van een sjabloon weer te geven:

   * Selecteer het pictogram > naast een sjabloon of dubbelklik op de sjabloonnaam.
   * Beweeg over om het even welk malplaatje en selecteer.. (**het pictogram van Opties**) en kies **uitgeven** van het contextmenu.

   Door gebrek, opent dit het **paneel van Montages** in de malplaatjedacteur.

   <img src="assets/customize-pdf-template.png" alt="PDF-sjabloon aanpassen" width="350">

   >[!NOTE]
   >
   >  Uw beheerder kan de nieuwste sjablonen downloaden van het volgende pad en de bestaande sjablonen vervangen:
   >
   > `/libs/fmdita/pdf`

   De verschillende sjablooncomponenten die u kunt aanpassen, worden in de volgende secties gecategoriseerd:

   * Paginalay-outs: een typische PDF bevat verschillende pagina&#39;s, zoals een vooromslag of een titelpagina, inhoudsopgave, hoofdstuk, index, citaten, enzovoort. In de sectie Pagina-indelingen kunt u de vormgeving ontwerpen van verschillende pagina&#39;s waaruit de PDF zou bestaan. Voor meer details, bekijk [ Lay-outs van de Pagina ](../native-pdf/components-pdf-template.md#page-layouts).

     Naast het uiterlijk kunt u ook de rangschikking van pagina-elementen definiëren, zoals de kop-, voettekst- en inhoudsgebieden op een pagina. Om meer te weten bij het aanpassen van de lay-out van een pagina, zie [ paginalay-outs ](components-pdf-template.md#create-customize-page-layout) creëren en aanpassen.

   * Stylesheets: Met de instellingen in de sectie Stijlvoorbladen kunt u de vormgeving van de onderdelen van de paginalay-out aanpassen, zoals de inhoudsopgave, index, woordenlijst, citaten en meer. Daarnaast kunt u ook de stijlen voor de DITA-inhoud aanpassen, zoals koppen, alinea&#39;s, lijsten en meer. Om meer te weten bij het gebruiken van de stylesheets, zie [ Stylesheets van het Gebruik om PDF ](components-pdf-template.md#stylesheet-customization) aan te passen.
   * Bronnen: Sla elementbestanden op die u moet aanpassen of PDF-sjablonen moet ontwerpen. Assets zoals logo&#39;s, aangepaste lettertypen, achtergrondafbeeldingen en meer worden opgeslagen in de Bronnen.
U kunt ook bronnen gebruiken die zich op een andere locatie in de opslagplaats bevinden. U hoeft geen dubbele bronnen voor elke sjabloon te maken en u kunt deze in een gedeelde map bewaren en ze in alle Native PDF-sjablonen gebruiken.

     Meer weten bij het gebruiken van middelen, zie [ Werk met middelen ](components-pdf-template.md#work-with-resources).

   * Instellingen: configureer de uitvoerinstellingen voor het genereren van een PDF met behulp van de sjabloon. In deze sectie kunt u sjabloontoewijzing definiëren voor verschillende pagina&#39;s in een PDF, hoofdstukstartpagina, afdrukmarkeringen, citaten en meer.

   U kunt ook de volgorde bepalen waarin ze in de uiteindelijke PDF-uitvoer moeten worden weergegeven.
Voor meer informatie bij het toepassen van montages, zie [ Geavanceerde Montages van de PDF ](components-pdf-template.md#advanced-pdf-settings).


1. Als u een sjablooncomponent wilt aanpassen, dubbelklikt u op een sjablooncomponent of selecteert u het pictogram > ervoor.

   Bijvoorbeeld, klik *Lay-outs van de Pagina* tweemaal of selecteer het *>* pictogram vóór *Lay-outs van de Pagina* om de beschikbare paginalay-outs te bekijken.

   >[!NOTE]
   >
   >U kunt een duimnagel en de beschrijving voor het malplaatje ook bijwerken gebruikend [**Eigenschappen**](#properties-option) in het **menu van Opties**.

1. Zodra u de gewenste veranderingen hebt aangebracht, uitgezocht *sparen allen* (of `Ctrl+S`).
