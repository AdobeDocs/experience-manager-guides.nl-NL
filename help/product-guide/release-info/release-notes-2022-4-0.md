---
title: Opmerkingen bij de release | Adobe Experience Manager Guides as a Cloud Service, release april 2022
description: Release van Adobe Experience Manager Guides as a Cloud Service in april
exl-id: c735ba24-a803-454b-8723-57dacf90061b
feature: Release Notes
role: Leader
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service in april

## Upgrade naar de release van april

Voer de volgende stappen uit om de huidige installatie van [!DNL Adobe Experience Manager Guides] as a Cloud Service (later ook wel *[!DNL AEM Guides]as a Cloud Service* genoemd) bij te werken:
1. Bekijk de Git-code van Cloud Services en schakel over naar de vertakking die is geconfigureerd in de Cloud Services-pijplijn die overeenkomt met de omgeving die u wilt upgraden.
1. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code voor Cloud Services bij naar 2022.4.133.
1. Leg de wijzigingen vast en voer de Cloud Services-pijplijn uit om naar de release van april van [!DNL AEM Guides] as a Cloud Service te upgraden.

## Compatibiliteitsmatrix

Deze sectie bevat een overzicht van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van [!DNL AEM Guides] as a Cloud Service April 2022.

### FrameMaker en FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Niet compatibel | 2020-update 4 en hoger |
| | |


### Zuurstofaansluiting

| AEM Guides Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac |
| --- | --- | --- |
| 2022,4,0 | 2.5.6. | 2.5.6. |
|  |  |  |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

## Nieuwe en verbeterde functies

Er zijn veel verbeteringen en nieuwe functies toegevoegd aan de webeditor:

### Verbeterde hoofdresolutie

Een DITA inhoudsbelangrijkste verwijzing neemt een deel van inhoud van één onderwerp in een andere op. Er wordt een toets gebruikt om de inhoud te zoeken. De belangrijkste verwijzingen verbonden aan een onderwerp DITA moeten worden opgelost. De geselecteerde hoofdmap heeft de hoogste prioriteit om toetsverwijzingen op te lossen.

![&#x200B; dialoog van gebruikersvoorkeur &#x200B;](assets/user-preferences.png)

Nu worden de belangrijkste verwijzingen opgelost op basis van de wortelkaart die in de volgende orde van prioriteit wordt geplaatst:

1. Gebruikersvoorkeuren
1. Deelvenster Kaartweergave
1. Mapprofiel

Voor meer details, zie *zeer belangrijke verwijzingen* sectie oplossen in de gids van de Gebruiker.

### Een aangepast deelvenster toevoegen in het linkerdeelvenster

Nu kunt u een aangepast deelvenster toevoegen in het linkerdeelvenster van de webeditor. U kunt een aangepast deelvenster gebruiken voor verschillende doeleinden, zoals het bieden van hulp of het testen voor een project. Als een douanepaneel is gevormd, dan verschijnt het ook in de lijst van panelen binnen de **Montages van de Redacteur**. U kunt schakelen tussen het weergeven of verbergen van het aangepaste deelvenster.

### Mogelijkheid om de documentstatus van onderwerpen in een DITA-kaart te wijzigen

Nu kunt u de documentstaat van geselecteerde onderwerpen binnen een kaart gemakkelijk veranderen DITA. U kunt de eigenschappen van geselecteerde onderwerpen in een kaart DITA van het **Meer menu van Opties** bij de bodem van het paneel van de Mening van de Kaart ook openen en uitgeven.

![&#x200B; geselecteerde onderwerpeigenschappen &#x200B;](assets/map-view-properties.png)

### Versiegegevens die worden weergegeven in de modus Voorbeeld

De Redacteur van het Web helpt u in het beheren van uw versies. Nu kunt u de versie van het actieve onderwerp of kaart DITA in de hoogste juiste hoek van het het dossierlusje van het onderwerp op de wijze van de Voorproef van een onderwerp ook zien.

![&#x200B; voorproefversie &#x200B;](assets/preview-version.png)

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

* Nieuwe labels worden niet automatisch weergegeven in het vervolgkeuzemenu Label toevoegen/verwijderen. Vernieuwen van basislijn is daarentegen vereist. 9249
* Kan de titel van de basislijn niet bewerken als een basislijn is gemaakt op basis van labelcriteria. (9171)
* Publiceren van een taak met een basislijn blijft vastzitten in de status &quot;wachten&quot; als de basislijnstatus verandert in &quot;mislukt&quot;. (9194)
* Als u labels op directe verwijzingen verwijdert, worden de labels ook van indirecte verwijzingen verwijderd. 9257
* Zoeken terwijl u typt, leidt tot ongewenste zoekverzoeken in de weergave Opslag. 9307
* Problemen treden op wanneer een trefwoord wordt gebruikt in de titel voor tab. 9318
* Basislijn mislukt bij het toevoegen van een label met spaties. 9362
* Bij uitvoer op de AEM-site wordt het glansingselement niet correct weergegeven. 8936
* De fout van de console komt bij het openen van het **lusje van de Output** in de Redacteur van het Web voor. 8715
* Foutbericht dat wordt weergegeven bij het publiceren van een handmatig recordtype via Salesforce is niet intuïtief. 8952
* De instelling Valideren met voorwaardenkenmerken wordt niet onmiddellijk geopend. De gebruiker moet het bestand opnieuw openen om de validaties te kunnen zien. 9300
* Metagegevens kunnen niet worden verwijderd als een DITA-kaart met metagegevens is gepubliceerd.  (9178)
* Het deelvenster Vertaling is zelfs zichtbaar bij het openen van de DITA-kaart in de Kaarteditor. 9053
* Aangepaste DTD die door de gebruiker is gedefinieerd, heeft geen voorrang op standaard-DITA DTD die is ingesloten in DITA-OT. (9104)
* In de functie Native PDF mislukt het uploaden in de sjablonen voor niet-DITA- en niet-afbeeldingsbestanden. 9070
* Het mechanisme van de vergunning voert twee vragen in plaats van één uit, in sommige gespecialiseerde scenario&#39;s. (9221)
* Het publiceren van de uitvoer van de AEM-site mislukt bij het gebruik van aangepaste DTD. 9243
* Met de voetnoot &#39;Bij gebruik naar referentie&#39; wordt niet naar de voetnootsectie in de AEM-site-uitvoer geschoven. 9234

## Bekende problemen

Adobe heeft het volgende bekende probleem geïdentificeerd in de release van [!DNL AEM Guides] as a Cloud Service April.

* De Redacteur van het Web meldt geen fout wanneer twee of meer basislijnen met de zelfde naam worden gecreeerd maar ruimte of gevalverschillen hebben. Bijvoorbeeld &quot;adobe&quot; en &quot;Adobe &quot; of &quot;Adobe&quot;.
* De zuurstofaansluiting loopt af en toe vast tijdens het frequent aanmelden of afmelden of schakelen tussen verschillende verificatietypen.
