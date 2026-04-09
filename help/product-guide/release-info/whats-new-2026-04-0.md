---
title: Opmerkingen bij de release | Nieuwe functies in Adobe Experience Manager Guides 2026.04.0-release
description: Meer informatie over de nieuwe en verbeterde functies in de 2026.04.0-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: ce2c9da0d9beb05a15f7cefcf9483e0c93abbf37
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---

# Nieuwe functies in de release van 2026.04.0 (april 2026)

Dit artikel behandelt de nieuwe en verbeterde functies die zijn geïntroduceerd met de release 2026.04.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor de lijst van kwesties die in deze versie worden bevestigd, mening [ Vaste kwesties in de 2026.04.0 versie ](fixed-issues-2026-04-0.md).

Leer over [ verbeteringsinstructies voor de versie 2026.04.0 ](../release-info/upgrade-instructions-2026-04-0.md).

## Introductie van producttraining en leerinhoud in Experience Manager Guides

De **Opleiding van het Product en het Leren** inhoudseigenschap in Experience Manager Guides laten trainingsteams en instructieontwerpers toe om interactieve eLearning cursussen van de interface van Experience Manager Guides direct te bouwen.

![](assets/lc-overview.png)

Met sjabloon-gedreven creatie, interactieve cursuscomponenten, en steun voor beoordelingen, kunnen de teams kwalitatief hoogwaardige opleidingsinhoud ontwikkelen die aan hun organisatorische doelstellingen wordt gericht.

>[!NOTE]
> 
> De functie Producttraining en Leerinhoud blijft standaard uitgeschakeld voor alle exemplaren van Experience Manager Guides as a Cloud Service. De beheerders kunnen deze eigenschap op het omslag-profiel niveau van **montages van Workspace** toelaten > **Algemeen**.

De belangrijkste mogelijkheden zijn:

- Gecentraliseerd beheer van leerinhoud
- Sjabloongestuurd ontwerpen
- Ondersteuning voor hergebruik van inhoud
- Vaststellen en beheren van evaluaties
- Web-based overzichtswerkschema&#39;s
- Toonaangevend vertaalbeheer
- Multi-channel publishing using out-of-the-box SCORM and PDF output formats

Voor meer details, verwijs naar [ Begonnen gids ](../learning-content/course-overview.md) en [ gids van de Configuratie ](../lc-config-guide/introduction.md).


## Verbeteringen in de Editor

De volgende Editor-verbeteringen zijn doorgevoerd in deze versie:

### Verbeteringen voor het deelvenster voor systeemvalidatie

De volgende verbeteringen zijn aangebracht in de Schematron-gebruikersinterface voor meer duidelijkheid, bruikbaarheid en validatieresultaten:

- In het deelvenster Validatie wordt een bericht met een lege status weergegeven wanneer er geen Schematron-bestand is toegevoegd. Zo krijgt u meer duidelijkheid en een betere richting voor de volgende stappen.

  ![](assets/schematron-panel.png){width="350" align="left"}
- Wanneer de veelvoudige dossiers Schematron worden toegevoegd, worden zij georganiseerd onder een geconsolideerde accordeon, die betere zichtbaarheid in de gevormde dossiers van het Schematron verstrekken.

  ![](assets/schematron-panel-error.png){width="350" align="left"}
- Op basis van het rolkenmerk dat in het Schematron-bestand is gedefinieerd, worden de validatieresultaten nu gecategoriseerd als: `Fatal`, `Error`, `Warn` of `Info` . Elke categorie bevat een zichtbare telling samen met een contextuele tooltip voor duidelijkere interpretatie.

  ![](assets/schematron-validation-errors.png){width="350" align="left"}

Voor meer details bij het gebruiken van de dossiers van Schematron in Experience Manager Guides, mening [ Steun voor de dossiers van Schematron ](../user-guide/support-schematron-file.md).

### Vertaal-exemplaren zijn nu beschikbaar in het rechterdeelvenster van de Editor-interface

Een nieuwe **Vertalingen** sectie is nu beschikbaar in het Juiste paneel onder *eigenschappen van het Dossier* in de Redacteur. Deze sectie verleent directe toegang tot alle beschikbare taalexemplaren voor de momenteel geopende activa (kaart, onderwerp, beeld, enz.). U hoeft niet meer naar de gebruikersinterface van Assets te navigeren om deze taalkopieën weer te geven of te openen.

![](assets/translations-right-panel.png){width="350" align="left"}

Voor elke taalkopie kunt u de muisaanwijzer op het bestand plaatsen om het pad in de opslagplaats te vinden of het bestand selecteren om het te openen in de Editor. Naast het openen van dossiers, kunt u vele acties ook uitvoeren gebruikend het **menu van Opties**. Enkele acties die u kunt uitvoeren zijn Bewerken, Voorvertoning, UUID kopiëren, Pad kopiëren, Toevoegen aan verzamelingen en Eigenschappen.

Voor meer details, mening [ Juiste paneel in de Redacteur ](../user-guide/web-editor-right-panel.md#file-properties).


### citaten zoeken in alle velden van het Dagboek

Nu, kunt u citaties over alle gebieden van het Dagboek, zoals *Titel*, *Titel van het Dagboek*, *Auteur*, *Jaar*, *Volume*, *Aantal*, en *Pagina&#39;s* zoeken, gebruikend **Om het even welke gebied** optie in 16} voeg citaat **dialoog toe.** De zoekopdracht retourneert de dichtstbijzijnde overeenkomende vermelding op basis van de ingevoerde tekst.

Voor meer details bij het toevoegen van citaten in Experience Manager Guides, mening [ voegt toe en beheert citaten in uw inhoud ](../user-guide/web-editor-apply-citations.md).

![](assets/add-citations.png){width="350" align="left"}



## Verbeteringen voor revisie

De volgende verbeteringen zijn beschikbaar voor de functie Revisie in deze release:

- Het toewijzen van een revisor aan een revisietaak is nu afhankelijk van een actieve projectselectie. **wijst aan** gebied op *toe leidt tot de pagina van de Taak van het Overzicht* gehandicapt blijft tot een actief project wordt geselecteerd. Nadat een project wordt geselecteerd, wordt **toewijzen aan** gebied toegelaten en maakt een lijst van slechts de gebruikers en gebruikersgroepen verbonden aan dat project. Dit zorgt ervoor dat de overzichtstaken slechts aan geldige projectleden worden toegewezen en onbedoelde selectie van de recensent verhindert.

  ![](assets/create-review-task-023.png)

- Het **toewijzen aan** gebied steunt nu typeahead onderzoek, toestaand u om van gebruikers of gebruikersgroepen snel de plaats te bepalen door tekst te typen.

Samen zorgen deze verbeteringen ervoor dat de selectie van de recensent nauwkeuriger, efficiënter en beter afgestemd is op projectspecifieke revisieworkflows.

Voor meer details, verzendt de mening [ onderwerpen voor overzicht ](../user-guide/review-send-topics-for-review.md).

## Verbeteringen voor middelenbeheer

Deze release introduceert de volgende verbeteringen voor middelenbeheer:

### Bestandshiërarchie afvlakken gebruiken om kaarten te downloaden met oorspronkelijke bestandsnamen en de bijbehorende metagegevens

Nu kunt u de optie Eén laag maken gebruiken om een kaart met de oorspronkelijke bestandsnaam te downloaden. Bovendien bevat het gedownloade pakket een `metadata.json` -bestand, waardoor de bijbehorende metagegevens gemakkelijk toegankelijk zijn en opnieuw kunnen worden gebruikt buiten Experience Manager Guides.

Voor meer details bij het downloaden van dossiers in Experience Manager Guides, mening [ de dossiers van de Download ](../user-guide/authoring-download-assets.md).

### Regex gebruiken om naverwerking in of uit te schakelen

U kunt regex nu gebruiken om naverwerking voor mappen in of uit te schakelen. Dankzij deze verbetering kunnen beheerders regels voor naverwerking definiëren die van toepassing zijn op meerdere mappen of volledige maphiërarchieën met één configuratie, in plaats van afzonderlijke mappaden op te geven.

Voor meer details, mening [ Regex van het Gebruik om postverwerking ](../cs-install-guide/conf-folder-post-processing.md#use-regex-to-enable-or-disable-post-processing) toe te laten of onbruikbaar te maken.
