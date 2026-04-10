---
title: Bestandsnamen configureren
description: Leer hoe u naverwerking voor een naar Adobe Experience Manager Assets geüploade map kunt uitschakelen
feature: Filename Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Nabewerking voor een map uitschakelen

Standaard worden alle geüploade elementen verwerkt met behulp van de DAM Update Asset-workflow. Experience Manager Guides voert als onderdeel van deze workflow een extra verwerking uit, ook wel postprocessing genoemd. Dit helpt ook bij het genereren van de UUID&#39;s

Terwijl het uploaden van uw dossiers en omslagen aan de *Adobe Experience Manager Assets* server, kunt u postprocessing en de generatie van UUIDs ook onbruikbaar maken.

Op de volgende tabbladen vindt u instructies voor het uitschakelen van naverwerking voor een map die is gebaseerd op de Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies in [&#x200B; met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. In het configuratiedossier, verstrek de volgende (bezit) details om postprocessing op een bepaalde weg onbruikbaar te maken of de naverwerking voor een omslag te negeren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `ignored.post.processing.paths` | Tekenreekswaarde voor het instellen van een willekeurige standaard NODE_OPTIONS (eigenschap met multiwaarde, tekenreeksen met een pad dat `/` aan het einde weglaat) <br> **Standaardwaarde**: `/content/dam/projects/translation_output` |
| `com.adobe.fmdita.config.ConfigManager` | `enabled.post.processing.paths` | Tekenreekswaarde voor het instellen van een willekeurige standaard NODE_OPTIONS (eigenschap met multiwaarde, tekenreeksen met een pad dat `/` aan het einde weglaat) <br> **Standaardwaarde**: `/content/dam` |

>[!TAB  Op locatie ]

Voer de volgende stappen uit om de naverwerking op een bepaald pad uit te schakelen of de naverwerking voor een map te negeren:


1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Selecteer de **Genegeerde Wegen voor de optie van de Verwerking**, om een omslag voor postverwerking te negeren.

   Tekenreekswaarde voor het instellen van een willekeurige standaard NODE_OPTIONS (eigenschap met meerwaarde, tekenreeksen met een pad dat `/` aan het einde weglaat)

   **Standaardwaarde**: `/content/dam/projects/translation_output`

   >[!NOTE]
   >
   > Deze eigenschap is standaard uitgeschakeld en het tabblad Vertalen is beschikbaar op het kaartdashboard.

1. Selecteer de **Toegelaten Wegen voor de optie van de Verwerking**, om een weg voor postverwerking toe te laten.

   Tekenreekswaarde voor het instellen van een willekeurige standaard NODE_OPTIONS (eigenschap met meerwaarde, tekenreeksen met een pad dat `/` aan het einde weglaat)

   **Standaardwaarde**: `/content/dam/`

   >[!NOTE]
   >
   > Deze eigenschap is standaard uitgeschakeld en het tabblad Vertalen is beschikbaar op het kaartdashboard.


1. Klik **sparen**.

>[!ENDTABS]

## Regels om nabewerking in of uit te schakelen

Standaard wordt nabewerking uitgevoerd voor elk mappad onder de Experience Manager DAM-map. Configuraties worden toegepast op elke map volgens de volgende regels:

* Als het bovenliggende element wordt genegeerd voor nabewerking maar de onderliggende map is ingeschakeld, worden het onderliggende item en alle opvolgers ervan als ingeschakeld beschouwd.
* Als de ouder voor postprocessing wordt toegelaten maar het kind wordt genegeerd, dan worden het kind en al zijn opvolgers beschouwd als genegeerd.
* Als hetzelfde mappad voorkomt in configuraties met zowel ignored.post.processing.paths als enabled.post.processing.paths, wordt het genegeerd voor nabewerking.

