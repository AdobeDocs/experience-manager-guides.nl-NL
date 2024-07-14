---
title: DITA-onderwerp of toewijzingsbestanden openen op hetzelfde tabblad
description: Leer hoe u DITA-onderwerp of toewijzingsbestanden op hetzelfde tabblad opent
exl-id: 81ad2e18-3ea7-4cc1-8387-d703d1038a18
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# DITA-onderwerp of toewijzingsbestanden openen op hetzelfde tabblad {#id223HI0P202H}

In sommige werkschema&#39;s, wanneer u op een verbinding van een onderwerp of een kaartdossier klikt, opent het in een nieuw lusje. Dit kan tot vele lusjes leiden die in uw browser worden geopend, die uw productiviteit kunnen beïnvloeden. U kunt dit gedrag wijzigen door een onderwerp- of kaartbestand op een nieuw tabblad te openen en dit op het huidige tabblad zelf te forceren. Hiervoor voert u de volgende configuratiewijzigingen uit:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. Selecteer de **Open Onderwerp DITA/Kaart op Zelfde Lusje** optie.

1. Klik **sparen**.


Deze instelling is van invloed op de volgende plaatsen waar u toegang kunt krijgen tot het onderwerp- of kaartbestand:

- Creeer Onderwerp DITA \(aan het eind van het werkschema, wanneer u **Open Onderwerp** knoop \ klikt)

- Creeer Kaart DITA \ (aan het eind van het werkschema, wanneer u de **Open Kaart** knoop \ klikt)

- Het lusje van onderwerpen in de DITA kaartconsole

- Het lusje van basislijnen in de DITA kaartconsole

- Het lusje van rapporten in de DITA kaartconsole


**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
