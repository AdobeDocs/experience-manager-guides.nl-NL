---
title: Opmerkingen bij de release | Upgradeinstructies voor de release van Adobe Experience Manager Guides 4.3.1.5
description: Leer hoe u een upgrade uitvoert naar versie 4.3.1.5 van de Adobe Experience Manager-hulplijnen
role: Leader
source-git-commit: 296bbea301df8828c00436db2b3c8b46dd235e64
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---


# Upgrade-instructies voor de 4.3.1.5-release

In dit artikel worden de upgrade-instructies en de compatibiliteitsmatrix voor de release van Adobe Experience Manager-hulplijnen in versie 4.3.1.5 besproken.


Voor de lijst met problemen die in deze release zijn opgelost, raadpleegt u [4.3.1.5. Opgeloste problemen](../release-info/fixed-issues-4-3-1-5.md).




## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van Experience Manager Guides 4.3.1.5.

### Adobe Experience Manager

**4.3.1.5 Niet-UUID**
Versie 6.5 Service Pack 18, 17, 16, 15, 14

**4.3.1.5 UUID**
Versie 6.5 Service Pack 18, 17, 16, 15, 14

Voor meer informatie bekijkt u de *Technische voorschriften* in de installatie- en configuratiehandleiding op locatie.

### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.3.1.5 (niet-UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.3 of hoger |
| 4.3.1.5 (UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.4 of hoger |
| | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.3.1.5 (niet-UUID) | 2.3-regelmatig-5 | 2.3-regelmatig-5 | 1,6 | 1,6 |
| 4.3.1.5 (UUID) | 3.2-uuid-5 | 3.2-uuid-5 | 2,3 | 2,3 |
|  |  |   |



### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package for Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |



## Upgrade naar 4.3.1.5 release van Experience Manager Guides


U kunt uw huidige versie van Hulplijnen eenvoudig upgraden naar versie 4.3.1.5. Voordat u verdergaat met het upgraden naar versie 4.3.1.5 van de Hulplijnen voor Experience Managers, moet u rekening houden met de volgende punten:


- Als u versie 4.3.1 of 4.3.1.x gebruikt, kunt u rechtstreeks upgraden naar versie 4.3.1.5.
- Als u versie 4.3.0 of 4.2 (Hotfix 4.2.1.3) gebruikt, moet u een upgrade naar versie 4.3.1 uitvoeren voordat u een upgrade naar versie 4.3.1.5 uitvoert.

- Als u versie 4.1 of 4.1.x gebruikt, moet u een upgrade naar versie 4.3.1 uitvoeren voordat u een upgrade naar versie 4.3.1.5 uitvoert.


- Als u versie 4.0 gebruikt, moet u een upgrade naar versie 4.2 uitvoeren voordat u een upgrade naar versie 4.3.x uitvoert.
- Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
- Als u een versie gebruikt die ouder is dan 3.8.5, raadpleegt u de sectie met instructies voor upgrades van Experience Manager in de productspecifieke installatiegids die beschikbaar is op [Adobe Experience Manager Guides Help PDF archief](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).



>[!NOTE]
>
>U moet AEM de dienstpak installeren alvorens de versie van de Gidsen van de Experience Manager te bevorderen.

Zie voor meer informatie [Upgradeinstructies voor de On-premise releases](../install-guide/upgrade-xml-documentation.md) van Experience Manager Guides.

