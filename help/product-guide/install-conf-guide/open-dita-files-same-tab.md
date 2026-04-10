---
title: DITA-onderwerp of toewijzingsbestanden openen op hetzelfde tabblad
description: Leer hoe u DITA-onderwerp of toewijzingsbestanden op hetzelfde tabblad opent
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# DITA-onderwerp of toewijzingsbestanden openen op hetzelfde tabblad {#id223HI0P202H}

In sommige werkschema&#39;s, wanneer u op een verbinding van een onderwerp of een kaartdossier klikt, opent het in een nieuw lusje. Dit kan tot vele lusjes leiden die in uw browser worden geopend, die uw productiviteit kunnen beïnvloeden. U kunt dit gedrag wijzigen door een onderwerp- of kaartbestand op een nieuw tabblad te openen en dit op het huidige tabblad zelf te forceren.

Op de volgende tabbladen vindt u instructies voor het openen van het DITA-onderwerp of het kaartbestand op hetzelfde tabblad, op basis van de Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. In het configuratiedossier, verstrek de volgende \(bezit \) details om een onderwerp of kaartdossier in een nieuw lusje te openen:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.openinsametab` | Boolean \(true/false\). <br> **Standaardwaarde**: `false` |

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. Selecteer de **Open Onderwerp DITA/Kaart op Zelfde Lusje** optie.

1. Klik **sparen**.

>[!ENDTABS]

Deze instelling is van invloed op de volgende plaatsen waar u toegang kunt krijgen tot het onderwerp- of kaartbestand:

- Creeer Onderwerp DITA \(aan het eind van het werkschema, wanneer u **Open Onderwerp** knoop \ klikt)

- Creeer Kaart DITA \ (aan het eind van het werkschema, wanneer u de **Open Kaart** knoop \ klikt)

- Het lusje van onderwerpen in de DITA kaartconsole

- Het lusje van basislijnen in de DITA kaartconsole

- Het lusje van rapporten in de DITA kaartconsole

**Bovenliggend onderwerp:**&#x200B;[&#x200B; pas de Redacteur van het Web &#x200B;](customize-overview.md) aan
