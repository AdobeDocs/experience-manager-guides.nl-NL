---
title: Bestandsnamen configureren
description: Leer hoe u naverwerking voor een naar Adobe Experience Manager Assets geüploade map kunt uitschakelen
feature: Filename Configuration
role: Admin
level: Experienced
exl-id: ff6e1322-9655-42aa-b353-199c70c9de49
source-git-commit: e84a00237e61275c6cd1ddd312883ac4f66b65ff
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Nabewerking voor een map uitschakelen

Standaard worden alle geüploade elementen verwerkt met behulp van de DAM Update Asset-workflow. Experience Manager Guides voert als onderdeel van deze workflow een extra verwerking uit, ook wel postprocessing genoemd. Dit helpt ook bij het genereren van de UUID&#39;s.

Terwijl het uploaden van uw dossiers en omslagen aan de *Adobe Experience Manager Assets* server, kunt u postprocessing en de generatie van UUIDs ook onbruikbaar maken.


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

>[!NOTE]
>
> Naast de genegeerde en toegelaten wegen die via de configuratie OSGi worden gevormd, wordt het post-verwerkingsgedrag ook beïnvloed door een bewaarplaats-vlakke knoop die bij `/var/dxml/postprocess/ignoredPaths` wordt gevestigd. <br> Als een map onverwacht wordt uitgesloten van naverwerking en niet wordt vermeld in de OSGi-configuratie, wordt aangeraden dit knooppunt in de repository te controleren. Als het pad daar wordt weergegeven en is ingesteld op `true` , wordt het genegeerd. Om verwerking opnieuw toe te laten, kunt u het overeenkomstige bezit manueel uit de knoop verwijderen.

## Regels om nabewerking in of uit te schakelen

Standaard wordt nabewerking uitgevoerd voor elk mappad onder de Experience Manager DAM-map. Configuraties worden toegepast op elke map volgens de volgende regels:

* Als het bovenliggende element wordt genegeerd voor nabewerking maar de onderliggende map is ingeschakeld, worden het onderliggende item en alle opvolgers ervan als ingeschakeld beschouwd.
* Als de ouder voor postprocessing wordt toegelaten maar het kind wordt genegeerd, dan worden het kind en al zijn opvolgers beschouwd als genegeerd.
* Als hetzelfde mappad voorkomt in configuraties met zowel ignored.post.processing.paths als enabled.post.processing.paths, wordt het genegeerd voor nabewerking.
