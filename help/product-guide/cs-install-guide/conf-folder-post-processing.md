---
title: Bestandsnamen configureren
description: Leer hoe u naverwerking voor een naar Adobe Experience Manager Assets geüploade map kunt uitschakelen
feature: Filename Configuration
role: Admin
level: Experienced
source-git-commit: fedd04f4a261ec199f86cb38ecd57e76b9393ae5
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Nabewerking voor een map uitschakelen

Standaard worden alle geüploade elementen verwerkt met behulp van de DAM Update Asset-workflow. De Gidsen van de Experience Manager stelt een extra verwerking in werking, genoemd postprocessing, als deel van deze werkschema. Dit helpt ook bij het genereren van de UUID&#39;s

Tijdens het uploaden van uw bestanden en mappen naar de *Adobe Experience Manager Assets* kunt u ook de naverwerking en het genereren van UUID&#39;s uitschakelen.


Gebruik de instructies in [Configuratieoverschrijvingen](download-install-additional-config-override.md#) om het configuratiebestand te maken. In het configuratiedossier, verstrek de volgende (bezit) details om postprocessing op een bepaalde weg onbruikbaar te maken of de naverwerking voor een omslag te negeren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `ignored.post.processing.paths` | Tekenreekswaarde voor het instellen van een standaard NODE_OPTIONS (multivaluated-eigenschap, tekenreeksen met weggelaten pad) `/` aan het einde) <br> **Standaardwaarde**: `/content/dam/projects/translation_output` |


| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `enabled.post.processing.paths` | Tekenreekswaarde voor het instellen van een standaard NODE_OPTIONS (multivaluated-eigenschap, tekenreeksen met weggelaten pad) `/` aan het einde) <br> **Standaardwaarde**: `/content/dam` |


## Regels om nabewerking in of uit te schakelen

Standaard wordt nabewerking uitgevoerd voor elk mappad onder de map Experience Manager DAM. Configuraties worden toegepast op elke map volgens de volgende regels:

* Als het bovenliggende element wordt genegeerd voor nabewerking maar de onderliggende map is ingeschakeld, worden het onderliggende item en alle opvolgers ervan als ingeschakeld beschouwd.
* Als de ouder voor postprocessing wordt toegelaten maar het kind wordt genegeerd, dan worden het kind en al zijn opvolgers beschouwd als genegeerd.
* Als hetzelfde mappad voorkomt in configuraties met zowel ignored.post.processing.paths als enabled.post.processing.paths, wordt het genegeerd voor nabewerking.
