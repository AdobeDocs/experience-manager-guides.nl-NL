---
title: Standaardwaarde voor de weergave Codes configureren
description: Leer hoe te om standaardwaarde voor de Mening van Markeringen te vormen
exl-id: 3ab75101-4c23-4e45-bfcf-76c1f5b92c96
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# Standaardwaarde voor de weergave Codes configureren {#id223GN0M0NDC}

AEM Guides staat u toe om de standaardstaat voor de Mening van Markeringen in de Redacteur van het Web te vormen, die u helpt om de Mening van Markeringen voor de zitting van een nieuwe gebruiker te houden of weg door gebrek. Voer de volgende stappen uit om de standaardwaarde voor de Mening van Markeringen te vormen:

1. Download het UI-configuratiebestand door u als beheerder aan te melden bij Adobe Experience Manager.
1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **Profielen van de Omslag**.
1. Klik op de **Globale tegel van het Profiel**.
1. Selecteer het **lusje van de Configuratie van de Redacteur van XML** en klik **uitgeven** pictogram op de bovenkant.
1. In de **UI van de Redacteur van XML configuratie** sectie, klik het **3} pictogram van de Download {om het `ui_config.json` dossier op uw lokaal systeem te downloaden.**
1. Wijzig in het bestand `ui_config.json` de weergavestatus van de standaardlabels door de sectie defaultValues (zie hieronder) te wijzigen:

```
"defaultValues":
                {
                "tagsView": true
                }
```

1). Sla het bestand op en upload het.

>[!NOTE]
>
> De voorkeur van de gebruiker in de Redacteur van het Web om de Mening van Markeringen toe te laten/onbruikbaar te maken heeft belangrijkheid over deze standaardwaarde. Zo, als een gebruiker de Mening van Markeringen van de Redacteur van het Web toelaat, blijft het toegelaten zelfs over de zittingen.

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
