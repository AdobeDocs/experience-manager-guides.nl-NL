---
title: Bestandsnamen configureren
description: Leer hoe u naverwerking voor een naar Adobe Experience Manager Assets geüploade map kunt uitschakelen
feature: Filename Configuration
role: Admin
level: Experienced
source-git-commit: 532e7c562a233619a8c4b7cbdbaef44bc73eb4b2
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---


# Nabewerking voor een map uitschakelen

Standaard worden alle geüploade elementen verwerkt met behulp van de DAM Update Asset-workflow. De Gidsen van de Experience Manager stelt een extra verwerking in werking, genoemd postprocessing, als deel van deze werkschema. Dit helpt ook bij het genereren van de UUID&#39;s

Tijdens het uploaden van uw bestanden en mappen naar de *Adobe Experience Manager Assets* kunt u ook de naverwerking en het genereren van UUID&#39;s uitschakelen.


Voer de volgende stappen uit om de naverwerking op een bepaald pad uit te schakelen of de naverwerking voor een map te negeren:


1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Zoeken naar en klikken op de knop **com.adobe.fmdita.config.ConfigManager** bundel.

1. Selecteer de **Genegeerde paden voor nabewerking** als u een map voor nabewerking wilt negeren.

   Tekenreekswaarde voor het instellen van een standaard NODE_OPTIONS (multivaluated-eigenschap, tekenreeksen met weggelaten pad) `/` aan het einde)

   **Standaardwaarde**: `/content/dam/projects/translation_output`

   >[!NOTE]
   >
   > Deze eigenschap is standaard uitgeschakeld en het tabblad Vertalen is beschikbaar op het kaartdashboard.

1. Selecteer de **Ingeschakelde paden voor nabewerking** om een pad voor nabewerking in te schakelen.

   Tekenreekswaarde voor het instellen van een standaard NODE_OPTIONS (multivaluated-eigenschap, tekenreeksen met weggelaten pad) `/` aan het einde)

   **Standaardwaarde**: `/content/dam/`

   >[!NOTE]
   >
   > Deze eigenschap is standaard uitgeschakeld en het tabblad Vertalen is beschikbaar op het kaartdashboard.


1. Klikken **Opslaan**.



## Regels om nabewerking in of uit te schakelen

Standaard wordt nabewerking uitgevoerd voor elk mappad onder de map Experience Manager DAM. Configuraties worden toegepast op elke map volgens de volgende regels:

* Als het bovenliggende element wordt genegeerd voor nabewerking maar de onderliggende map is ingeschakeld, worden het onderliggende item en alle opvolgers ervan als ingeschakeld beschouwd.
* Als de ouder voor postprocessing wordt toegelaten maar het kind wordt genegeerd, dan worden het kind en al zijn opvolgers beschouwd als genegeerd.
* Als hetzelfde mappad voorkomt in configuraties met zowel ignored.post.processing.paths als enabled.post.processing.paths, wordt het genegeerd voor nabewerking.
