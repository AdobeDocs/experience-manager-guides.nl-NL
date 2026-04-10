---
title: Vraag configureren om bij het sluiten als een nieuwe versie op te slaan
description: Leer hoe te Vorm herinnering om als nieuwe versie bij dicht te bewaren
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Vraag configureren om bij het sluiten als een nieuwe versie op te slaan {#id222HBI00XXA}

Wanneer de gebruiker probeert om een dossier te sluiten dat in de Redacteur van het Web gebruikend **dicht** knoop op het lusje van het dossier of **dicht** optie in het menu van Opties wordt geopend, verschijnt een dialoog als het dossier unsaved gegevens of een niet bewaarde versie heeft. De gebruiker wordt gevraagd het bestand op te slaan als een nieuwe versie als de versie niet is opgeslagen.

Op de volgende tabbladen vindt u instructies die zijn gebaseerd op de Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om een vraag te configureren om bij het sluiten als een nieuwe versie op te slaan:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.savenewversion` | Boolean \( true/ false\). <br>  **Standaardwaarde**: waar |

Wanneer deze configuratie wordt toegelaten, **sparen als Nieuwe 1&rbrace; checkbox van de Versie &lbrace;door gebrek in de dialoogdoos wordt geselecteerd.**

Voor meer details, zie *Dossier sluiten en sparen scenario&#39;s* sectie in de Gebruikende gids van Adobe Experience Manager Guides as a Cloud Service.

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. Selecteer **vragen om nieuwe versie op dichte** optie.

1. Klik **sparen**.


**sparen als Nieuwe 1&rbrace; checkbox van de Versie &lbrace;wordt niet toegelaten door gebrek en u moet dit van configMgr toelaten.**

Wanneer deze optie wordt geselecteerd, **sparen als Nieuwe 1&rbrace; checkbox van de Versie wordt geselecteerd door gebrek in de dialoogdoos.**

Voor meer details, zie *Dossier sluiten en sparen scenario&#39;s* sectie in de Gebruikende gids van Adobe Experience Manager Guides as a Cloud Service.

>[!ENDTABS]