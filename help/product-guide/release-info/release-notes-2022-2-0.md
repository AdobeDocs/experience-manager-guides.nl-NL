---
title: Release-aantekeningen voor  [!DNL AEM Guides], release van februari 2022
description: De versie van februari van  [!DNL Adobe Experience Manager Guides]  as a Cloud Service
exl-id: eb7ff475-bb5b-4d32-b291-024147fbfed1
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 0%

---

# Release van februari van [!DNL Adobe Experience Manager Guides] as a Cloud Service

## Upgrade naar de release van februari

Voer de volgende stappen uit om de huidige [!DNL Adobe Experience Manager Guides] as a Cloud Service instelling (later [!DNL AEM Guides] as a Cloud Service genoemd) bij te werken:
1. Controle uit de code van Git van Cloud Servicen en schakelaar aan de tak die in de pijpleiding van Cloud Servicen wordt gevormd die aan het milieu beantwoordt u wilt bevorderen.
1. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code van de Cloud Service bij naar 202.2.114.
1. Leg de wijzigingen vast en voer de pijplijn met Cloud Servicen uit om naar de release van februari van [!DNL AEM Guides] as a Cloud Service te upgraden.

## Compatibiliteitsmatrix

Deze sectie bevat een overzicht van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van [!DNL AEM Guides] as a Cloud Service februari 2022.

### FrameMaker en FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Niet compatibel | 2020-update 4 en hoger |
| | |


### Zuurstofaansluiting

| [!DNL AEM Guides] Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac |
| --- | --- | --- |
| 2022,2,0 | 2.4.0. | 2.4.0. |
|  |  |  |


## Nieuwe en verbeterde functies

### Native PDF-publicatie

Ondersteuning voor het maken van een native PDF is ook toegevoegd in de release van [!DNL AEM Guides] as a Cloud Service in februari. Er is een nieuwe uitgeverij-engine geïntroduceerd met de volgende functies:
* Een CSS-sjabloon maken
* Andere paginasjablonen maken
* PDF-sjablonen ontwerpen die CSS en paginasjablonen bevatten
* Publish-kaart en onderwerpinhoud in de PDF-indeling

### Ondersteuning voor het pad van de kennisbasissite in op artikelen gebaseerde publicaties

[!DNL AEM Guides] as a Cloud Service biedt de op artikelen gebaseerde publicatiefunctie om incrementeel een uitvoer van een of meer onderwerpen te genereren of uw inhoud te publiceren naar een kennisgebaseplatform. Met de versie van februari, hebt u een extra optie om de de plaatsweg te kiezen van de Kennisbank waaraan het onderwerp/de kaart moet worden gepubliceerd. Nadat u het pad hebt geselecteerd, wordt de uitvoer gegenereerd op het opgegeven pad.

### Verbeteringen in de webeditor

Er zijn veel verbeteringen en nieuwe functies toegevoegd aan de webeditor:

* **Verbeterde dialoog op dossierdichte**

[!DNL AEM Guides] as a Cloud Service vraagt u om uw wijzigingen op te slaan en vergrendelde bestanden te ontgrendelen wanneer u een bestand probeert te sluiten dat is geopend in de webeditor. De herinneringen worden getoond gebaseerd op **vraagt om controle-binnen op dicht** en **vraagt om nieuwe versie op dichte** montages die door uw beheerder worden gevormd.

Op basis van de configuratie kunt u de wijzigingen opslaan en een nieuwe versie van het document maken. U kunt ook het bestand inchecken en de wijzigingen in de huidige versie opslaan.

![ Dossier dicht ](assets/file-close-save-changes-unlock.png)

Voor meer details, zie *Dossier sluiten en scenario&#39;s* in de Gids van de Gebruiker opslaan.

* Er is een vaste spatie toegevoegd aan het tekenpalet.  A **het niet breken** ruimte verhindert een automatische lijnonderbreking op een bepaald punt in een document van HTML. De Redacteur van het Web steunt een vaste ruimte voor zowel AEM Plaats als HTML5 output.

* Wanneer u een afbeelding uploadt vanuit de webeditor, wordt een bevestigingsvenster weergegeven als er al een afbeelding met dezelfde naam bestaat. U kunt beide bestanden behouden (bestaande en nieuwe bestanden) of het bestaande bestand overschrijven en alleen het nieuwe bestand opslaan.

* Als een gebruiker een bestand voor bewerkingen heeft vergrendeld, kan een beheerder de vergrendeling loslaten en het bestand inchecken. Deze functie is handig wanneer bepaalde bestanden moeten worden bewerkt, maar zijn vergrendeld door gebruikers die het bestand niet kunnen inchecken

### Kaartdashboard

Wanneer u selecteert om de kaart te downloaden DITA, wordt het verzoek een rij gevormd, en u ontvangt een bericht zodra de kaart klaar is om te downloaden. U kunt ervoor kiezen het kaartbestand direct te downloaden of later te downloaden via de koppeling in het AEM-meldingsvak.

![ download van de Kaart ](assets/download-map-prompt.png)

### Controleren

U kunt de details vermelden in het beschrijvingsveld van de revisietaak en deze worden weergegeven in de e-mail die naar de revisor wordt verzonden.

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Op artikel gebaseerde publicatie

* Publiceren op basis van artikelen publiceert geen artikelen op basis van de geselecteerde basislijn. 8771
* DITAVAL-bestanden worden niet ondersteund in publicaties op basis van artikelen. (8770)
* Kan op artikelen gebaseerde publicaties voor het Salesforce-profiel niet uitvoeren als het recordtype FAQ is en de inhoud van het artikelveld Vraag is. (8448)
* Kan op artikel gebaseerde publicaties voor Salesforce-profiel niet uitvoeren als het recordtype Handmatig is. 8447

### Webeditor

* Het slepen en neerzetten van een voorwaarde werkt niet bij DITA-onderwerpen. 8761
* Kenmerken ontbreken bij het toevoegen van een hoofdstuk aan een bladwijzer met behulp van slepen en neerzetten in de weergave Favorieten. 8746
* Als u de eigenschappen van een afbeelding (hoogte, breedte) bewerkt, treedt er een toepassingsfout op. 8722
* verbroken koppelingen worden niet weergegeven in het deelvenster Overzicht in de bronweergave. 8590
* De Redacteur van XML verwijdert nieuwe lijnmarkering in codeblock. 8522
* Glossusage wordt getoond als Nota wanneer een ingang van de Verklarende woordenlijst wordt geschreven. 8384
* xref kan zelfs op geldige locaties niet worden ingevoegd. 8354
* De elementenlijst (Alt+Enter) wordt grijs weergegeven in het thema Donkerder/Donkerst. 7913
* De lijst van kaartmalplaatjes in **creeert** optie ( ellipsis menu) van het paneel van de Bewaarplaats is niet zoals per het **Profiel van de Omslag** in de Voorkeur van de Gebruiker. 5918
* Element-id&#39;s worden niet automatisch gegenereerd voor elementen die worden toegevoegd met de functie Inhoud hergebruiken van de hoofdwerkbalk. 5826

### ASSETS UI

* Beeldbewerking werkt niet zoals verwacht op de cloudserver. 8768
* In het deelvenster Versiehistorie wordt in de huidige sectie een onjuiste tijdstempel weergegeven en deze wordt door informatie gewijzigd. 8765
* Het uploaden van DITAVAL-bestanden naar de cloudserver mislukt wanneer AEM bureaubladgereedschap wordt gebruikt. 8707
* De tweede beheerdergebruiker kan niet als eerste beheerdergebruiker aan een omslag worden toegevoegd. 8430
* Niet-unieke eigenschappen van een element worden niet gekopieerd wanneer het element wordt gekopieerd en geplakt. 8241

### Bruikbaarheid

* Als een gebruikersnaam lang is in het deelvenster Revisie van de webeditor, worden de pictogrammen die u wilt accepteren/afwijzen niet duidelijk weergegeven. 8793
* In het **Vondst en vervangt** paneel, verschijnt een ongewenst pictogram op de muiswijzer in de resultaatsectie. (8775)
* Het pictogram Aangepast wordt niet gekozen uit de eigenschap en in plaats daarvan wordt het standaardpictogram weergegeven voor de rapporten die worden gegenereerd met de knop Rapport genereren. 8573
