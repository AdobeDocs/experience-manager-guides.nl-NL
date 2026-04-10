---
title: Patroon UUID-bestandsnaam configureren
description: Leer hoe u het patroon van UUID-bestandsnamen configureert
feature: Migration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Patroon UUID-bestandsnaam configureren

Wanneer u inhoud importeert, is het niet nodig dat de bestandsnamen worden gebaseerd op de UUID. In een systeem dat op UUID-Gebaseerde dossiernamen gebruikt, is het verplicht dat alle dossiers worden bedoeld gebruikend hun UUIDs eerder dan hun originele dossiernamen. Als een geïmporteerd bestand geen op UUID gebaseerde bestandsnamen heeft, kunt u het systeem zo configureren dat een UUID wordt toegevoegd aan de eigenschap file. Deze UUID wordt vervolgens gebruikt om te verwijzen naar bestanden waarin UUID niet wordt gebruikt voor het benoemen van de bestanden.

## Stappen voor het configureren van het bestandspatroon UUID

Op de volgende tabbladen vindt u instructies voor het configureren van het patroon van UUID-bestandsnamen op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\) gegevens op om het patroon van de UUID-bestandsnaam te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `uuid.regex` | String specifying the regex for UID filename pattern. <br> Als een bestand het opgegeven patroon niet volgt, wordt een UUID toegevoegd aan de eigenschap van het bestand en worden alle verwijzingen naar het bestand bijgewerkt met de UUID die aan het bestand is toegewezen. <br> **Standaardwaarde**: `"^GUID-(?<id>.*)"` |

>[!TAB  Op locatie ]

Voer de volgende stappen uit om bestandsnamen te controleren op basis van een UUID-patroon en UUID toe te wijzen aan bestanden waaraan geen UUID is toegewezen:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en selecteer *com.adobe.fmdita.config.ConfigManager* bundel.

1. In het **bezit van de Patronen van Filename 0&rbrace; UUID &lbrace;, specificeer een patroon om de namen van het ingevoerde dossier te controleren.**

   Als een bestand het opgegeven patroon niet volgt, wordt een UUID toegevoegd aan de eigenschap van het bestand en worden alle verwijzingen naar het bestand bijgewerkt met de UUID die aan het bestand is toegewezen.

1. Selecteer **sparen**.

>[!ENDTABS]





