---
title: Opmerkingen bij de release | Upgradeinstructies voor Adobe Experience Manager Guides 5.0.0 Service Pack 2-release
description: Leer over de verenigbaarheidsmatrijs en hoe te aan de 5.0.0 versie Service Pack 2 van Adobe Experience Manager Guides te bevorderen.
source-git-commit: b5b4c5484593a2f7d9121da1c7bfb28dd2c36a57
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Upgradeinstructies voor de 5.0.0 Service Pack 2-release (september 2025)

Dit artikel behandelt de verbeteringsinstructies en de verenigbaarheidsmatrijs voor 5.0.0 de versie van Service Pack 2 van Adobe Experience Manager Guides.

Voor de lijst van kwesties die in deze versie zijn bevestigd, mening [ Vaste kwesties in 5.0.0 Service Pack 2 versie ](../release-info/fixed-issues-5-0-0-sp2.md).

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door Experience Manager Guides 5.0.0 Service Pack 2.

### Adobe Experience Manager

**5.0.0 Service Pack 2 UUID**

Versie 6.5 Service Pack 22, Service Pack 21, en Service Pack 20

Voor meer details, bekijk de [ Technische vereisten ](../install-guide/download-install-technical-requirements.md) sectie in de Gids van de Installatie en van de Configuratie op locatie.

### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS | FM |
| --- | --- | --- |
| 5.0.0 Service Pack 2 (UUID) | Ondersteund | 2022 of hoger |

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 5.0.0 Service Pack 2 (UUID) | 3.7-uuid.2 | 3.7-uuid.2 | 2,3 | 2,3 |

### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package voor Cloud Service | dxml-components.all-1.3.0 | aem-site-template-dxml.all-1.0.4 |

### Nieuwe sjabloonversie voor AEM-site


| Versie van componenten | Site-versie |
|---|---|
| guides-components.all-1.3.0 | aemg-docs.all-1.2.0 |


## Upgrade naar 5.0.0 Service Pack 2-release van Experience Manager Guides

U kunt uw huidige versie van Gidsen aan versie 5.0.0 Service Pack 2 gemakkelijk bevorderen. Voordat u verdergaat met de upgrade naar versie 5.0.0 Service Pack 2 van Experience Manager Guides, moet u rekening houden met de volgende punten:

- Als u versie 5.0.0 Service Pack 1 of 5.0.0 gebruikt, dan kunt u aan versie 5.0.0 Service Pack 2 direct bevorderen.
- Als u versie 5.0.0 gebruikt, dan kunt u aan 5.0.0 Service Pack 1 direct bevorderen.
- Als u versie 4.6.x gebruikt, kunt u rechtstreeks upgraden naar versie 5.0.0.
- Als u versie 4.3.x, 4.2, 4.2.1 (Hotfix 4.2.1.3), 4.1 of 4.1.x gebruikt, moet u een upgrade naar versie 4.4 uitvoeren voordat u een upgrade naar versie 5.0.0 uitvoert.
- Als u versie 4.0 gebruikt, moet u een upgrade naar versie 4.2 uitvoeren voordat u een upgrade naar versie 4.3.x uitvoert.
- Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
- Als u op een versie voorafgaand aan 3.8.5 bent, verwijs naar de sectie van Experience Manager Guides van de Verbetering in de product-specifieke installatiegids beschikbaar op [ Adobe Experience Manager Guides Help het archief van PDF ](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).

>[!NOTE]
>
>U moet AEM Service Pack installeren voordat u de Experience Manager Guides-versie kunt upgraden.

Voor details, mening [ de instructies van de Verbetering voor de On-premise versies ](../install-guide/upgrade-xml-documentation.md) van Experience Manager Guides.
