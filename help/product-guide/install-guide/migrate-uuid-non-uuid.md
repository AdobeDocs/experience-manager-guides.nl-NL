---
title: Migratie van niet-UUID naar UUID-inhoud
description: Leer hoe u niet-UUID naar UUID-inhoud migreert
exl-id: f8b723bf-84c0-4fe6-936e-63970fb3e417
feature: Migration
role: Admin
level: Experienced
source-git-commit: 56f1bd81e74ad9b479b2dcbcf04e1ee82e9a9041
workflow-type: tm+mt
source-wordcount: '320'
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
| 4.3.1 niet-UUID | 4.3.2 UUID | Na het migreren naar versie 4.3.2 UUID, moet u 4.6.0 (UUID) direct installeren. Zodra u op 4.6.0 bent, bevorder aan versie 5.1.0, en installeer dan 5.1.0 Service Pack 3. |
| 4.6.0 Service Pack 4 niet-UUID | 4.6.1 UUID | Na het migreren aan versie 4.6.1 UUID, moet u aan 5.1.0 (UUID) direct bevorderen. Wanneer de upgrade is voltooid, installeert u versie 5.1.0 Service Pack 3. |

## Schatting van de migratietijd

Het migratiehulpprogramma verwerkt middelen met een gemiddelde snelheid van ongeveer 50 ms per middel. De volgende tabel biedt een schatting van de migratietijd voor een systeem dat is geconfigureerd met 64 vCPU&#39;s, 128 GB RAM en opslag op SSD-basis. De geheugenvereisten kunnen toenemen voor grotere opslagruimten of assets met veel uitvoeringen of binaire bestanden met hoge resolutie.

>[!NOTE]
>
> De werkelijke migratietijd kan variëren afhankelijk van de hardwareprestaties, de opslagdoorvoer, de gelijktijdige AEM-activiteiten en de totale systeembelasting.


| **Telling van Activa** | **Ongeveer. Tijd** |
|-----------------|-------------------------|
| 10 K | ~8-9 minuten |
| 50 K | ~42 minuten |
| 100 K | ~1,4 uur |
| 250 K | ~3,5 uur |
| 500 K | ~7 uur |
| 750 K | ~10,5 uur |
| 1M | ~14 uur |
| 2 MB | ~28 uur (~1,2 dagen) |
| 3 MB | ~42 uur (~1,75 dagen) |
| 5 MB | ~69 uur (~2,9 dagen) |
| 10 MB | ~139 uur (~5,8 dagen) |


Raadpleeg de volgende artikelen voor gedetailleerde stappen bij het migreren van uw inhoud:

- [**4.3.1 niet-UUID naar 4.3.2 migratie van UUID-inhoud**](./migrate-non-uuid-4-3.md)
- [**4.6.0 Service Pack 4 niet-UUID aan 4.6.1 migratie van UUID-inhoud**](./migrate-non-uuid-uuid-4-6.md)



