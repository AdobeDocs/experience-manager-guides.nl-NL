---
title: DITA Assets-replicatie configureren
description: Leer hoe u replicatie van dita-middelen configureert
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 453da51a42984b912547570f2e1de70806b41171
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# Replicatie van DITA-elementen configureren

Op de volgende tabbladen vindt u instructies voor het configureren van de replicatiefunctie voor DITA-middelen op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](../install-conf-guide/download-install-config-override.md) om het configuratiedossier tot stand te brengen.

1. Geef in het configuratiebestand de volgende gegevens (eigenschap) op:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|---|---|
   | `com.adobe.fmdita.config.ConfigManager` | `publish.replicate` | **Standaardwaarde:** &quot;waar&quot; |

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en selecteer *com.adobe.fmdita.config.ConfigManager* bundel.

1. Configureer de instelling `Replicate DITA assets` naar wens. De instelling wordt standaard ingeschakeld.


   ![](assets/dita-assets-replication.png){width="350" align="left"}


1. Selecteer **sparen**.

>[!ENDTABS]
