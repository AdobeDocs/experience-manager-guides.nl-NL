---
title: Opmerkingen bij de release | Upgradeinstructies voor de release van Adobe Experience Manager Guides 4.4.0
description: Leer hoe u een upgrade uitvoert naar de versie 4.4.0 van de Adobe Experience Manager-hulplijnen
role: Leader
source-git-commit: 2209fd311ca1ad524db35633b8be22f6d303346d
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Upgrade-instructies voor de 4.4.0-release (januari 2024)

Dit artikel behandelt de upgrade-instructies en de compatibiliteitsmatrix voor de release van Adobe Experience Manager Guides met 4.4.0.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [Nieuwe functies in de release 4.4.0](../release-info/whats-new-4-4.md).

Voor de lijst met problemen die in deze release zijn opgelost, raadpleegt u [4.4.0-release. Dit probleem is nu opgelost.](../release-info/fixed-issues-4-4.md).




## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van Experience Manager Guides 4.4.0.

### Adobe Experience Manager

**4.4.0 Niet-UUID**
Versie 6.5 Service Pack 19, 18, 17

**4.4.0 UUID**
Versie 6.5 Service Pack 19, 18, 17


Voor meer informatie bekijkt u de [Technische voorschriften](../install-guide/download-install-technical-requirements.md) in de installatie- en configuratiehandleiding op locatie.

### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.4.0 (niet-UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.3 of hoger |
| 4.4.0 (UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.4 of hoger |
| | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.4.0 (niet-UUID) | 2.7-regelmatig-1 | 2.7-regelmatig-1 | 1,6 | 1,6 |
| 4.4.0 (UUID) | 3.4-uuid-1 | 3.4-uuid-1 | 2,3 | 2,3 |
|  |  |   |



### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package for Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |



## Upgrade naar versie 4.4.0 van de hulplijnen voor Experience Managers


U kunt eenvoudig uw huidige versie van Hulplijnen upgraden naar versie 4.4.0. Voordat u verdergaat met de upgrade naar versie 4.4.0 van de Experience Manager-hulplijnen, moet u rekening houden met de volgende punten:


- Als u versie 4.3.1, 4.3.0 of 4.2.1 (Hotfix 4.2.1.3) gebruikt, kunt u rechtstreeks upgraden naar versie 4.4.0.
- Als u versie 4.2, 4.1 of 4.1.x gebruikt, moet u een upgrade naar versie 4.3.1, 4.3.0 of 4.2.1 (Hotfix 4.2.1.3) uitvoeren voordat u een upgrade naar versie 4.4.0 uitvoert.
- Als u versie 4.0 gebruikt, moet u een upgrade naar versie 4.2 uitvoeren voordat u een upgrade naar versie 4.3.x uitvoert.
- Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
- Als u een versie gebruikt die ouder is dan 3.8.5, raadpleegt u de sectie met instructies voor upgrades van Experience Manager in de productspecifieke installatiegids die beschikbaar is op [Adobe Experience Manager Guides Help PDF archief](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).



>[!NOTE]
>
>U moet AEM de dienstpak installeren alvorens de versie van de Gidsen van de Experience Manager te bevorderen.

Zie voor meer informatie [Upgradeinstructies voor de On-premise releases](../install-guide/upgrade-xml-documentation.md) van Experience Manager Guides.

