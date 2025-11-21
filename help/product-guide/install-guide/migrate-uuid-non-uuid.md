---
title: Migratie van niet-UUID naar UUID-inhoud
description: Leer hoe u niet-UUID naar UUID-inhoud migreert
exl-id: f8b723bf-84c0-4fe6-936e-63970fb3e417
feature: Migration
role: Admin
level: Experienced
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# Migratie van niet-UUID naar UUID-inhoud {#id226TI0U20XA}


U kunt niet-UUID-inhoud migreren naar UUID op basis van de huidige versie van Experience Manager Guides die u gebruikt.

>[!IMPORTANT]
>
> Voordat u inhoud migreert naar de UUID-server, moet u controleren of er een niet-UUID-server is geïnstalleerd waarop de compatibele AEM Guides-versie is geïnstalleerd.

## Compatibiliteitsmatrix

Gebruik de volgende matrix om het juiste migratiepad te bepalen op basis van uw huidige niet-UUID-versie. Dit zorgt voor een soepele overgang na de migratie.

| Niet-UUID-versie vereist voor migratie | UUID-versie na migratie | Ondersteund upgradepad na migratie |
|---|---|---|
| 4.3.1 niet-UUID | 4.3.2 UUID | Na het migreren naar versie 4.3.2 UUID, kunt u 4.6.0 (UUID) direct installeren. Zodra u op 4.6.0 bent, bevorder aan versie 5.1.0, en installeer dan 5.1.0 Service Pack 1. |
| 4.6.0 Service Pack 4 niet-UUID | 4.6.1 UUID | Na het migreren aan versie 4.6.1 UUID, kunt u aan 5.1.0 (UUID) direct bevorderen. Wanneer de upgrade is voltooid, installeert u versie 5.1.0 Service Pack 1. |

Raadpleeg de volgende artikelen voor gedetailleerde stappen bij het migreren van uw inhoud:

- [**4.3.1 niet-UUID naar 4.3.2 migratie van UUID-inhoud**](./migrate-non-uuid-4-3.md)
- [**4.6.0 Service Pack 4 niet-UUID aan 4.6.1 migratie van UUID-inhoud**](./migrate-non-uuid-uuid-4-6.md)



