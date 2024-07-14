---
title: Bestandsnamen configureren
description: Leer hoe u naverwerking voor een naar Adobe Experience Manager Assets geüploade map kunt uitschakelen
feature: Filename Configuration
role: Admin
level: Experienced
exl-id: 42722c6f-1b1c-4a7e-89ef-a373623eb774
source-git-commit: 5d99274da8fdacbd255d426fa4913b5773ca45f8
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Nabewerking voor een map uitschakelen

Standaard worden alle geüploade elementen verwerkt met behulp van de DAM Update Asset-workflow. Experience Manager Guides voert als onderdeel van deze workflow een extra verwerking uit, ook wel postprocessing genoemd. Dit helpt ook bij het genereren van de UUID&#39;s

Terwijl het uploaden van uw dossiers en omslagen aan de *Adobe Experience Manager Assets* server, kunt u postprocessing en de generatie van UUIDs ook onbruikbaar maken.


Gebruik de instructies in [ met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. In het configuratiedossier, verstrek de volgende (bezit) details om postprocessing op een bepaalde weg onbruikbaar te maken of de naverwerking voor een omslag te negeren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `ignored.post.processing.paths` | Tekenreekswaarde voor het instellen van een standaard NODE_OPTIONS (eigenschap met multiwaarde, tekenreeksen met pad dat `/` aan het einde weglaat) <br> **Standaardwaarde**: `/content/dam/projects/translation_output` |


| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `enabled.post.processing.paths` | Tekenreekswaarde voor het instellen van een standaard NODE_OPTIONS (eigenschap met multiwaarde, tekenreeksen met pad dat `/` aan het einde weglaat) <br> **Standaardwaarde**: `/content/dam` |


## Regels om nabewerking in of uit te schakelen

Standaard wordt nabewerking uitgevoerd voor elk mappad onder de map Experience Manager DAM. Configuraties worden toegepast op elke map volgens de volgende regels:

* Als het bovenliggende element wordt genegeerd voor nabewerking maar de onderliggende map is ingeschakeld, worden het onderliggende item en alle opvolgers ervan als ingeschakeld beschouwd.
* Als de ouder voor postprocessing wordt toegelaten maar het kind wordt genegeerd, dan worden het kind en al zijn opvolgers beschouwd als genegeerd.
* Als hetzelfde mappad voorkomt in configuraties met zowel ignored.post.processing.paths als enabled.post.processing.paths, wordt het genegeerd voor nabewerking.
