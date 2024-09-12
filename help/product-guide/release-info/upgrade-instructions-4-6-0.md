---
title: Opmerkingen bij de release | Upgradeinstructies voor Adobe Experience Manager Guides 4.6.0-release
description: Leer hoe u een upgrade uitvoert naar de 4.6.0-versie van Adobe Experience Manager Guides
role: Leader
source-git-commit: 1880d889dc9063ef05c4f856d6082d1ea03b7946
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Upgrade-instructies voor de 4.6.0-release (september 2024)

Dit artikel behandelt de upgrade-instructies en de compatibiliteitsmatrix voor de release van Adobe Experience Manager Guides 4.6.0.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de 4.6.0 versie ](../release-info/whats-new-4-6.md) nieuw is.

Voor de lijst van kwesties die in deze versie zijn bevestigd, mening [ Vaste kwesties in de 4.6.0 versie ](../release-info/fixed-issues-4-6-0.md).

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van Experience Manager Guides 4.6.0.

### Adobe Experience Manager

**4.6.0 niet-UUID**
Versie 6.5 Service Pack 21, 20, en 19

**4.6.0 UUID**
Versie 6.5 Service Pack 21, 20, en 19

Voor meer details, bekijk de [ Technische vereisten ](../install-guide/download-install-technical-requirements.md) sectie in de Gids van de Installatie en van de Configuratie op locatie.

### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2022 | FMPS 2020 | FM 2022 | FM 2020 |
| --- | --- | --- | --- | --- |
| 4.6.0 (niet-UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.3 of hoger |
| 4.6.0 (UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.4 of hoger |
| | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.6.0 (niet-UUID) | 2.8-regelmatig-10 | 2.8-regelmatig-10 | 1,6 | 1,6 |
| 4.6.0 (UUID) | 3.6-uuid.9 | 3.6-uuid.9 | 2,3 | 2,3 |
|  |  |   |

### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package voor Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

### Nieuwe sjabloonversie AEM site


| Versie van componenten | Site-versie |
|---|---|
| guides-components.all-1.0.0 | aemg-docs.all-1.0.0 |

## Upgrade naar versie 4.6.0 van Experience Manager Guides

U kunt eenvoudig uw huidige versie van Hulplijnen upgraden naar versie 4.6.0. Voordat u verdergaat met de upgrade naar versie 4.6.0 van Experience Manager Guides, moet u rekening houden met de volgende punten:

- Als u versie 4.4, 4.3.1 of 4.3.0 gebruikt, kunt u rechtstreeks upgraden naar versie 4.6.0.
- Als u versie 4.2, 4.2.1 (Hotfix 4.2.1.3), 4.1 of 4.1.x gebruikt, moet u een upgrade naar versie 4.4 uitvoeren voordat u een upgrade naar versie 4.6.0 uitvoert.
- Als u versie 4.0 gebruikt, moet u een upgrade naar versie 4.2 uitvoeren voordat u een upgrade naar versie 4.3.x uitvoert.
- Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
- Als u op een versie voorafgaand aan 3.8.5 bent, verwijs naar de sectie van Experience Manager Guides van de Verbetering in de product-specifieke installatiegids beschikbaar op [ Adobe Experience Manager Guides help PDF archive ](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).

>[!NOTE]
>
>U moet AEM servicepack installeren voordat u de Experience Manager Guides-versie kunt upgraden.

Voor details, mening [ de instructies van de Verbetering voor de On-premise versies ](../install-guide/upgrade-xml-documentation.md) van Experience Manager Guides.
