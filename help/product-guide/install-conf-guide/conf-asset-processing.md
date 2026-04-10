---
title: Asset-verwerking voor Cloud-service configureren
description: Meer informatie over het configureren van Asset Processing for Cloud-service
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Functie voor middelenverwerking configureren

Op de volgende tabbladen vindt u instructies voor het configureren van de functie voor het verwerken van bedrijfsmiddelen op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md) om het configuratiedossier tot stand te brengen.

1. Geef in het configuratiebestand de volgende gegevens (eigenschap) op:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|---|---|
   | `com.adobe.fmdita.config.ConfigManager` | `enable.asset.processing.scheduler` | **Standaardwaarde:** &quot;waar&quot; |

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en selecteer *com.adobe.fmdita.config.ConfigManager* bundel.

1. Configureer de instelling `Enable Guides asset processing scheduled job` naar wens. De instelling wordt standaard ingeschakeld.

1. Selecteer **sparen**.

>[!ENDTABS]