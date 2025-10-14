---
title: Release-aantekeningen voor  [!DNL AEM Guides], release maart 2022
description: Maart versie van  [!DNL Adobe Experience Manager Guides]  as a Cloud Service
exl-id: 885edbb5-dfe4-4bdc-bb66-0df64addb094
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Release van maart van [!DNL Adobe Experience Manager Guides] as a Cloud Service

## Upgrade naar de release van maart

Voer de volgende stappen uit om de huidige instelling voor [!DNL Adobe Experience Manager Guides] as a Cloud Service (later *[!DNL AEM Guides]as a Cloud Service* genoemd) bij te werken:
1. Controle uit de code van Git van Cloud Servicen en schakelaar aan de tak die in de pijpleiding van Cloud Servicen wordt gevormd die aan het milieu beantwoordt u wilt bevorderen.
1. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code van de Cloud Service bij naar 2022.3.123.
1. Leg de wijzigingen vast en voer de pijplijn met Cloud Servicen uit om naar de release van maart van [!DNL AEM Guides] as a Cloud Service te upgraden.

## Compatibiliteitsmatrix

Deze sectie bevat een overzicht van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van [!DNL AEM Guides] as a Cloud Service maart 2022.

### FrameMaker en FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Niet compatibel | 2020-update 4 en hoger |
| | |


### Zuurstofaansluiting

| [!DNL AEM Guides] Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac |
| --- | --- | --- |
| 2022,3,0 | 2.4.0. | 2.4.0. |
|  |  |  |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

## Nieuwe en verbeterde functies

### Nieuw basislijndashboard

In de release van [!DNL AEM Guides] as a Cloud Service maart is de functie Basislijn geïntegreerd in de webeditor. U kunt basislijnen van de Redacteur van het Web nu tot stand brengen en hen gebruiken om onderwerpen van verschillende versies te publiceren of te vertalen.

Nota: Voor bevorderd systeem, te werk gelieve recentste **ui_config.json** voor het Profiel van de Omslag bij.

Gebruik deze functie om een basislijn met een specifieke versie van de onderwerpen tot stand te brengen beschikbaar op een specifieke datum en een tijd. Bovendien kunt u met de API-ondersteuning een basislijn maken of bijwerken met een label dat is gedefinieerd voor een versie van onderwerpen.

![&#x200B; basislijn beheert lusje &#x200B;](assets/baseline-manage.png)

U kunt de bestanden doorzoeken op bestandsnamen of op de bestandslocatie. U kunt ook de onderwerpen filteren die in het basislijnbewerkingsvenster moeten worden weergegeven en ze sorteren op basis van specifieke kolommen.

![&#x200B; basislijn beheert lusje &#x200B;](assets/baseline-filter.png)

De prestaties voor het basisproces voor het maken zijn verder verbeterd. Het proces om basislijnen tot stand te brengen is asynchroon, zodat kunt u andere dossiers in de Redacteur van het Web blijven uitgeven terwijl de basislijn wordt gecreeerd. Voor meer details, zie *basislijnen van de Redacteur van het Web* in de Gids van de Gebruiker creëren en leiden.

Opmerking: het tabblad Basislijn op het kaartdashboard is standaard verborgen. Uw beheerder kan het lusje van de Basislijn op het kaartdashboard toelaten.

### Verbeterd gedrag voor vernieuwen van webeditor

De volgende verbeteringen zijn nu beschikbaar met browser verfrist verrichting in de Redacteur van het Web:

* Nu krijgt u de ondersteuning om de browser te vernieuwen terwijl u uw
inhoud in de webeditor. Als u op het pictogram Vernieuwen van de browser klikt terwijl een of meer bestanden met
niet-opgeslagen wijzigingen worden geopend voor bewerking. U wordt gevraagd uw bestanden op te slaan of de vernieuwingsactie te annuleren.

* Zelfs bij het vernieuwen van de browser blijven de weergaven van het linkerdeelvenster en het rechterdeelvenster behouden.

* Het actieve onderwerp of de kaart DITA wordt opnieuw geopend in het inhoudsuitgevende gebied.

### Verbeteringen voor publiceren

Het publicatieproces is verder verbeterd met de release van [!DNL AEM Guides] as a Cloud Service in maart:

* De basislijnen zijn gerespecteerd voor de metagegevens van AEM site-uitvoer. U kunt de eigenschappen van een basislijnversie ook als metagegevens verwerken. Als geen basislijn wordt bepaald, dan worden de eigenschappen van de recentste versie verwerkt als meta-gegevens.

* De **Naam van het Dossier** en **DITA-OT de Argumenten van de Lijn van het Bevel** opties zijn toegevoegd voor HTML5, EPUB, en de output van de Douane vooraf instelt. U kunt nu de bestandsnaam opgeven waarmee u de uitvoer wilt opslaan. U kunt ook de aanvullende argumenten opgeven die u met DITA-OT wilt verwerken tijdens het genereren van uitvoer.

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

* Onbekwaam om voorgrond, achterstandselementen in een boekenkaart toe te voegen gebruikend de mening van de Auteur van de Redacteur van het Web. 7652
* De boomeinden van de verwijzing na het verwijderen van een onderwerp en het uitvoeren van een bewegingsverrichting. (8804)
* Er wordt een uitzondering ontvangen bij het weergeven van de inhoud na het uploaden van een element. 3638
* De fout komt voor wanneer de dossiers de waarvan ouderomslag speciale karakters in filename heeft, in Zuurstof (gebruikend **uitgeeft in Zuurstof** knoop) worden geopend. 8918
* De **plaats in Bewaarplaats** optie bepaalt en benadrukt niet de kaart DITA in de Redacteur van XML. 8796
* Filteren geeft niet de juiste resultaten wanneer meerdere kenmerken aan de inhoud in de XML-editor worden toegevoegd. 8795
* Er treedt een fout op bij het toevoegen van een gebruiker als beheerder in het mappenprofiel als de gebruiker-id numeriek is. 8908

## Bekende problemen

Adobe heeft het volgende bekende probleem geïdentificeerd in de release van [!DNL AEM Guides] as a Cloud Service maart.

* Als u labels op directe verwijzingen verwijdert, worden de labels ook van indirecte verwijzingen verwijderd.

* Kan de bijgewerkte basislijntitel niet spiegelen zonder het basislijnvenster handmatig te vernieuwen.

* De functie voor versievoorvertoning in het deelvenster Versiehistorie geeft geen voorvertoning van een geselecteerd onderwerp weer.
