---
title: Vraag configureren om een bestand bij sluiten in te checken
description: Leer hoe u de vraag om een bestand bij het sluiten in te checken configureert
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Vraag configureren om een bestand bij sluiten in te checken {#id222HC040PE8}

Wanneer de gebruiker probeert om een dossier te sluiten dat in de Redacteur van het Web gebruikend **dicht** knoop op het lusje van het dossier of **dicht** optie in het menu van Opties wordt geopend, verschijnt een dialoog als het dossier unsaved gegevens of een niet bewaarde versie heeft. De gebruiker wordt gevraagd het bestand te ontgrendelen als het is vergrendeld.

Op de volgende tabbladen vindt u instructies voor het standaard inchecken van een bestand bij het sluiten in de webeditor op basis van de Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om een vraag te configureren om een bestand bij het sluiten in te checken:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.checkin` | Boolean \( true/ false\).<br> **Standaardwaarde**: vals |

Wanneer deze configuratie wordt toegelaten, **ontgrendel checkbox van het Dossier** door gebrek in de dialoogdoos wordt geselecteerd.

Voor meer details, zie *Dossier sluiten en sparen scenario&#39;s* sectie in de Gebruikende gids van Adobe Experience Manager Guides as a Cloud Service.

>[!TAB  Op locatie ]

>[!NOTE]
>
>**ontgrendel checkbox van het Dossier** niet door gebrek wordt toegelaten en u moet dit van configMgr toelaten. Voer de volgende stappen uit om de optie door gebrek in de Redacteur van het Web toe te laten:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. Selecteer **vragen om controle-binnen op dichte** optie.

1. Klik **sparen**.


Wanneer deze configuratie wordt toegelaten, **ontgrendel checkbox van het Dossier** door gebrek in de dialoogdoos wordt geselecteerd.

Voor meer details, zie *Dossier sluiten en sparen scenario&#39;s* sectie in de Gebruikende gids van Adobe Experience Manager Guides as a Cloud Service.

>[!ENDTABS]

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](customize-overview.md) aan
