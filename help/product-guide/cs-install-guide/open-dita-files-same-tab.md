---
title: DITA-onderwerp of toewijzingsbestanden openen op hetzelfde tabblad
description: Leer hoe u DITA-onderwerp of toewijzingsbestanden op hetzelfde tabblad opent
exl-id: 466cbea4-c75a-488e-bde2-465cf2c184d5
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# DITA-onderwerp of toewijzingsbestanden openen op hetzelfde tabblad {#id223HH0301J3}

In sommige werkschema&#39;s, wanneer u op een verbinding van een onderwerp of een kaartdossier klikt, opent het in een nieuw lusje. Dit kan tot vele lusjes leiden die in uw browser worden geopend, die uw productiviteit kunnen beïnvloeden. U kunt dit gedrag wijzigen door een onderwerp- of kaartbestand op een nieuw tabblad te openen en dit op het huidige tabblad zelf te forceren.

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. In het configuratiedossier, verstrek de volgende \(bezit \) details om een onderwerp of kaartdossier in een nieuw lusje te openen:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.openinsametab` | Boolean \(true/false\). <br> **Standaardwaarde**: `false` |

Deze instelling is van invloed op de volgende plaatsen waar u toegang kunt krijgen tot het onderwerp- of kaartbestand:

- Creeer Onderwerp DITA \(aan het eind van het werkschema, wanneer u **Open Onderwerp** knoop \ klikt)

- Creeer Kaart DITA \ (aan het eind van het werkschema, wanneer u de **Open Kaart** knoop \ klikt)

- Het lusje van onderwerpen in de DITA kaartconsole

- Het lusje van basislijnen in de DITA kaartconsole

- Het lusje van rapporten in de DITA kaartconsole


**Bovenliggend onderwerp:**&#x200B;[&#x200B; pas de Redacteur van het Web &#x200B;](conf-web-editor.md) aan
