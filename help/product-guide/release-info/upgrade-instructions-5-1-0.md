---
title: Opmerkingen bij de release | Upgradeinstructies voor Adobe Experience Manager Guides 5.1.0-versie
description: Leer meer over de compatibiliteitsmatrix en hoe u een upgrade uitvoert naar de 5.1.0-versie van Adobe Experience Manager Guides.
exl-id: 4b7b6756-d260-4baf-a9cb-d99fc02f020f
source-git-commit: 6bcfed792036a51aa0c11498e4cb489199280a56
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 1%

---

# Upgrade-instructies voor de 5.1.0-release (september 2025)

Dit artikel behandelt de upgrade-instructies en de compatibiliteitsmatrix voor 5.1.0-release van Adobe Experience Manager Guides.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [&#x200B; wat in de 5.1.0 versie &#x200B;](../release-info/whats-new-5-1-0.md) nieuw is.

Voor de lijst van kwesties die in deze versie zijn bevestigd, mening [&#x200B; Vaste kwesties in de 5.1.0 versie &#x200B;](../release-info/fixed-issues-5-1-0.md).

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van Experience Manager Guides 5.1.0.

| AEM Guides | AEM-versie | Service Pack |
| --- | --- | --- |
| 5.1.0 (UUID) | 6,5 LTS | 1 |
| 5.1.0 (UUID) | 6,5 | 23, 22, 21 |

Voor meer details, bekijk de [&#x200B; Technische vereisten &#x200B;](../install-guide/download-install-technical-requirements.md) sectie in de Gids van de Installatie en van de Configuratie op locatie.

### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS | FM |
| --- | --- | --- |
| 5.1.0 (UUID) | Ondersteund | 2022 of hoger |

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 5.1.0 (UUID) | 3.8-uuid.1 | 3.8-uuid.1 | 2,3 | 2,3 |

### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package voor Cloud Service | dxml-components.all-1.3.0 | aem-site-template-dxml.all-1.0.4 |

### Nieuwe sjabloonversie voor AEM-site


| AEM Guides | AEM-versie | Versie van componenten | Site-versie |
|---|---|---| ---|
| 5.1.0 UUID | 6,5 LTS | guides-components.all-1.4.1 | aemg-docs.all-1.2.0 |
| 5.1.0 UUID | 6,5 | guides-components.all-1.4.0 | aemg-docs.all-1.2.0 |

## Upgrade naar Experience Manager Guides 5.1.0

U kunt uw huidige versie van Experience Manager Guides aan versie 5.1.0 op **AEM 6.5** of **AEM 6.5 LTS** gemakkelijk bevorderen.

>[!NOTE]
>
> Als u momenteel op AEM 6.5 werkt en van plan bent over te stappen op AEM 6.5 LTS, dient u eerst de AEM-upgrade te voltooien voordat u verdergaat met de Experience Manager Guides 5.1.0-upgrade. Voor details, mening [&#x200B; Bevorderend aan Adobe Experience Manager (AEM) 6.5 LTS &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-65-lts/content/implementing/deploying/upgrading/upgrade).

Voordat u verdergaat met de upgrade naar versie 5.1.0 van Experience Manager Guides, moet u rekening houden met de volgende punten:

- Als u versie 4.6.3, 4.6.4, 5.0.0, of 5.0.0 Service Pack 1 gebruikt, dan kunt u aan versie 5.1.0 direct bevorderen.
- Als u versie 4.6.0 en 4.6.1 gebruikt, moet u een upgrade naar versie 4.6.3 of 4.6.4 of 5.0.0 uitvoeren voordat u een upgrade naar versie 5.1.0 uitvoert.
- Als u versie 4.3.x, 4.2, 4.2.1 (Hotfix 4.2.1.3), 4.1 of 4.1.x gebruikt, moet u een upgrade naar versie 4.4 uitvoeren voordat u een upgrade naar versie 5.1.0 uitvoert.
- Als u versie 4.0 gebruikt, moet u een upgrade naar versie 4.2 uitvoeren voordat u een upgrade naar versie 4.3.x uitvoert.
- Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
- Als u op een versie voorafgaand aan 3.8.5 bent, verwijs naar de sectie van Experience Manager Guides van de Verbetering in de product-specifieke installatiegids beschikbaar op [&#x200B; Adobe Experience Manager Guides Help het archief van PDF &#x200B;](https://helpx.adobe.com/nl/xml-documentation-for-experience-manager/archive.html).

>[!NOTE]
>
>U moet AEM Service Pack installeren voordat u de Experience Manager Guides-versie kunt upgraden.

Voor details, mening [&#x200B; de instructies van de Verbetering voor de On-premise versies &#x200B;](../install-guide/upgrade-xml-documentation.md) van Experience Manager Guides.


