---
title: Opmerkingen bij de release | Upgradeinstructies voor Adobe Experience Manager Guides 4.6.0 Service Pack 3-release
description: Leer hoe u een upgrade uitvoert naar de 4.6.0 Service Pack 3-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: 8a24d2fd50b6b6ac93b5513e7a99953fdc1735b8
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---

# Upgradeinstructies voor de 4.6.0 Service Pack 3-release (januari 2025)

Dit artikel behandelt de verbeteringsinstructies en de verenigbaarheidsmatrijs voor versie 4.6.0 Service Pack 3 van Adobe Experience Manager Guides.

Voor de lijst van kwesties die in deze versie zijn bevestigd, mening [ Vaste kwesties in 4.6.0 Service Pack 3 versie ](fixed-issues-4-6-0-sp2.md).

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door Experience Manager Guides 4.6.0 Service Pack 3.

### Adobe Experience Manager

**4.6.0 Service Pack 3 Non-UUID**
Versie 6.5 Service Pack 21, 20, en 19

**4.6.0 Service Pack 3 UUID**
Versie 6.5 Service Pack 21, 20, en 19

Voor meer details, bekijk de [ Technische vereisten ](../install-guide/download-install-technical-requirements.md) sectie in de Gids van de Installatie en van de Configuratie op locatie.

### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2022 | FMPS 2020 | FM 2022 | FM 2020 |
| --- | --- | --- | --- | --- |
| 4.6.0 Service Pack 3 (niet-UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.3 of hoger |
| 4.6.0 Service Pack 3 (UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.4 of hoger |
| | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.6.0 Service Pack 3 (niet-UUID) | 2.8-regelmatig-10 | 2.8-regelmatig-10 | 1,6 | 1,6 |
| 4.6.0 Service Pack 3 (UUID) | 3.6-uuid.9 | 3.6-uuid.9 | 2,3 | 2,3 |
|  |  |   |

### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package voor Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

### Nieuwe sjabloonversie AEM site

| Versie van componenten | Site-versie |
|---|---|
| guides-components.all-1.0.0 | aemg-docs.all-1.0.0 |

## Upgrade naar 4.6.0 Service Pack 3-release van Experience Manager Guides

U kunt uw huidige versie van Gidsen aan 4.6.0 Service Pack 3 gemakkelijk bevorderen. Voordat u verdergaat met de upgrade, moet u rekening houden met de volgende punten:

- Als u versie 4.6.0 of 4.6.0 Service Pack 1 gebruikt, dan kunt u rechtstreeks aan 4.6.0 Service Pack 3 bevorderen.
- Als u versie 4.4, 4.3.1 of 4.3.0 gebruikt, moet u een upgrade naar versie 4.6.0 uitvoeren.
- Als u versie 4.2, 4.2.1 (Hotfix 4.2.1.3), 4.1 of 4.1.x gebruikt, moet u een upgrade naar versie 4.4 uitvoeren voordat u een upgrade naar versie 4.6.0 uitvoert.
- Als u versie 4.0 gebruikt, moet u een upgrade naar versie 4.2 uitvoeren voordat u een upgrade naar versie 4.3.x uitvoert.
- Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
- Als u op een versie voorafgaand aan 3.8.5 bent, verwijs naar de sectie van Experience Manager Guides van de Verbetering in de product-specifieke installatiegids beschikbaar op [ Adobe Experience Manager Guides help PDF archive ](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).

>[!NOTE]
>
>U moet AEM servicepack installeren voordat u de Experience Manager Guides-versie kunt upgraden.

Het upgradeproces voor de 4.6.0 Service Pack 3-release volgt dezelfde stappen als de 4.6.0-release. Voor gedetailleerde instructies, mening [ de instructies van de Verbetering voor de On-premise versies ](../install-guide/upgrade-xml-documentation.md) van Experience Manager Guides.
