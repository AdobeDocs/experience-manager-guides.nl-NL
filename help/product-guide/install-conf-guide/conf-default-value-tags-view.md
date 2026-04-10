---
title: Standaardwaarde voor de weergave Codes configureren
description: Leer hoe te om standaardwaarde voor de Mening van Markeringen te vormen
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Standaardwaarde voor de weergave Codes configureren {#id223GN0M0NDC}

AEM Guides staat u toe om de standaardstaat voor de Mening van Markeringen in de Redacteur van het Web te vormen, die u helpt om de Mening van Markeringen voor de zitting van een nieuwe gebruiker te houden of weg door gebrek. Voer de volgende stappen uit om de standaardwaarde voor de Mening van Markeringen te vormen:

1. Download het UI-configuratiebestand door u als beheerder aan te melden bij Adobe Experience Manager.
1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **Profielen van de Omslag**.
1. Klik op de **Globale tegel van het Profiel**.
1. Selecteer het **lusje van de Configuratie van de Redacteur van XML** en klik **uitgeven** pictogram op de bovenkant.
1. In de **UI van de Redacteur van XML configuratie** sectie, klik het **3} pictogram van de Download {om het** dossier op uw lokaal systeem te downloaden.`ui_config.json`
1. Wijzig in het bestand `ui_config.json` de weergavestatus van de standaardlabels door de sectie defaultValues (zie hieronder) te wijzigen:

   ```
   "defaultValues":
               {
               "tagsView": true
               }
   ```

1. Sla het bestand op en upload het.

>[!NOTE]
>
> De voorkeur van de gebruiker in de Redacteur van het Web om de Mening van Markeringen toe te laten/onbruikbaar te maken heeft belangrijkheid over deze standaardwaarde. Zo, als een gebruiker de Mening van Markeringen van de Redacteur van het Web toelaat, blijft het toegelaten zelfs over de zittingen.

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](customize-overview.md) aan
