---
title: Opmerkingen bij de release | Upgradeinstructies voor Adobe Experience Manager Guides 4.3.1.5 -release
description: Leer hoe u een upgrade uitvoert naar 4.3.1.5 release van Adobe Experience Manager Guides
role: Leader
exl-id: 856970ef-9f50-4452-b589-ba1f5ee73322
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Upgradeinstructies voor de release van 4.3.1.5

In dit artikel worden de upgrade-instructies en de compatibiliteitsmatrix voor de release van 4.3.1.5 Adobe Experience Manager Guides besproken.


Voor de lijst van kwesties die in deze versie zijn bevestigd, mening [&#x200B; Vaste kwesties in de 4.3.1.5 versie &#x200B;](../release-info/fixed-issues-4-3-1-5.md).




## Compatibiliteitsmatrix

Deze sectie bevat een overzicht van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van Experience Manager Guides 4.3.1.5 .

### Adobe Experience Manager

**4.3.1.5Niet-UUID**
Versie 6.5 Service Pack 18, 17, 16, 15, 14

**4.3.1.5UUID**
Versie 6.5 Service Pack 18, 17, 16, 15, 14

Voor meer details, bekijk de *Technische vereisten* sectie in de Gids van de Installatie en van de Configuratie op locatie.

### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.3.1.5 (Niet-UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.3 of hoger |
| 4.3.1.5 (UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.4 of hoger |
| | | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.3.1.5 (Niet-UUID) | 2.3-regelmatig-5 | 2.3-regelmatig-5 | 1,6 | 1,6 |
| 4.3.1.5 (UUID) | 3.2-uuid-5 | 3.2-uuid-5 | 2,3 | 2,3 |
|  |  |   | | |



### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package voor Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |



## Upgrade naar 4.3.1.5 release van Experience Manager Guides


U kunt uw huidige versie van Hulplijnen eenvoudig upgraden naar versie 4.3.1.5 . Voordat u verdergaat met de upgrade naar versie 4.3.1.5 van Experience Manager Guides, moet u rekening houden met de volgende punten:


- Als u versie 4.3.1 of 4.3.1.x gebruikt, kunt u rechtstreeks een upgrade uitvoeren naar versie 4.3.1.5 .
- Als u versie 4.3.0 of 4.2 (Hotfix 4.2.1.3 ) gebruikt, moet u een upgrade naar versie 4.3.1 uitvoeren voordat u een upgrade naar versie 4.3.1.5 uitvoert.

- Als u versie 4.1 of 4.1.x gebruikt, moet u een upgrade naar versie 4.3.1 uitvoeren voordat u een upgrade naar versie 4.3.1.5 uitvoert.


- Als u versie 4.0 gebruikt, moet u een upgrade naar versie 4.2 uitvoeren voordat u een upgrade naar versie 4.3.x uitvoert.
- Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
- Als u op een versie voorafgaand aan 3.8.5 bent, verwijs naar de sectie van Experience Manager Guides van de Verbetering in de product-specifieke installatiegids beschikbaar op [&#x200B; Adobe Experience Manager Guides Help het archief van PDF &#x200B;](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).



>[!NOTE]
>
>U moet AEM Service Pack installeren voordat u de Experience Manager Guides-versie kunt upgraden.

Voor details, mening [&#x200B; de instructies van de Verbetering voor de On-premise versies &#x200B;](../install-guide/upgrade-xml-documentation.md) van Experience Manager Guides.
