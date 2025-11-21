---
title: Opmerkingen bij de release | Adobe Experience Manager Guides as a Cloud Service, release oktober 2022
description: Release van Adobe Experience Manager Guides as a Cloud Service in oktober
exl-id: 38638080-625c-49c3-9e54-56cc23831546
feature: Release Notes
role: Leader
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service in oktober

## Upgrade naar de release van oktober

Bevorder uw huidige die Adobe Experience Manager Guides as a Cloud Service (later als *wordt bedoeld AEM Guides as a Cloud Service*) opstelling door de volgende stappen uit te voeren:
1. Bekijk de Git-code van Cloud Services en schakel over naar de vertakking die is geconfigureerd in de Cloud Services-pijplijn die overeenkomt met de omgeving die u wilt upgraden.
1. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code voor Cloud Services bij naar 202.10.183.
1. Leg de wijzigingen vast en voer de Cloud Services-pijplijn uit om naar de release van AEM Guides as a Cloud Service in oktober te upgraden.

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides as a Cloud Service-release van oktober 2022.

### FrameMaker en FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Niet compatibel | 2020-update 4 en hoger |
| | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| AEM Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022 10,0 | 2.7.13. | 2.7.13. | 2,3 | 2,3 |
|  |  |  |  |  |


## Nieuwe en verbeterde functies

AEM Guides as a Cloud Service biedt verbeteringen en nieuwe functies in de release van oktober:


### Deelvenster Snel genereren

Nu verstrekt AEM Guides **Snel produceert** paneel dat u snel helpt de output voor vooraf instelt produceren en bekijken die voor uw kaart DITA wordt gecreeerd.

![&#x200B; snel produceert pictogram &#x200B;](assets/quick-generate-icon.png)

In **snel produceert** paneel, kunt u de lijst van alle die outputvoorinstellingen zien voor uw kaart DITA worden gecreeerd.

![&#x200B; Snel produceert paneel &#x200B;](assets/quick-generate-panel.png)

Selecteer een of meer voorinstellingen en genereer snel de uitvoer. U kunt ook snel de uitvoer weergeven die voor de voorinstellingen is gegenereerd. Er wordt een succesbericht weergegeven bij het genereren van de uitvoer. Er wordt een foutbericht weergegeven als het genereren van de uitvoer mislukt. U kunt het foutenlogboek ook bekijken om de details van de fout te zien die in het generatieproces voorkwam.


## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

* Oorspronkelijke PDF | Er treedt een fout op bij het verwijderen van brononderwerpen uit de PDF-uitvoer. (10554)
* Oorspronkelijke PDF | Lege toetsaanslagen worden weergegeven in de PDF-uitvoer. (10553)
* Oorspronkelijke PDF | `navtitle` for `topichead` wordt niet gerespecteerd. 10509
* Oorspronkelijke PDF | Ondersteuning nodig voor amd64 JDK-aroma&#39;s. 10465
* Oorspronkelijke PDF | Kan de onderwerpen frontMatrix niet verbergen in de inhoudsopgave. 10355
* Oorspronkelijke PDF | Wanneer u het paginanummer in de hoofdstuklayout opnieuw start, wordt de nummering vanaf het einde van het vorige hoofdstuk willekeurig gestart. 10154
* Chrome-browser | Het scherm wordt leeg wanneer u elementen uit de gebruikersinterface sleept en neerzet. Bijvoorbeeld bij het slepen van een voorwaarde vanuit het deelvenster Voorwaarden. 10524
* Node-eigenschappen worden verwijderd nadat een element is gekopieerd en geplakt. 10053
* Bij het klikken **dicht** gebruikers werden opnieuw gericht aan activa - de ervaring is verbeterd om gebruikers aan de homepage van AEM te nemen. 9654
