---
title: Vertaal in de Redacteur van het Web vormen
description: Leer hoe te om de eigenschap van de Vertaling in de Redacteur van het Web te vormen
exl-id: e25473c3-9a84-4658-87c9-6fd72bcaa2b6
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# Vertaal in de Redacteur van het Web vormen {#id21BONI0J0YR}

De redacteur van het Web verstrekt een krachtige vertaaleigenschap om uw inhoud in veelvoudige talen te vertalen.

U kunt **gebruiken beheert** lusje in de Redacteur van het Web om uw inhoud te vertalen. Dit tabblad is standaard beschikbaar.

Om **te verbergen leidt** lusje in de Redacteur van het Web, voer de volgende stappen uit:

1. Logboek in **Adobe Experience Manager** als beheerder.
1. Klik op de **verbinding van Adobe Experience Manager** bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **Profielen van de Omslag**.
1. Klik op de **Globale tegel van het Profiel**.
1. Klik op **de Configuratie van de Redacteur van XML**.
1. Klik op **uitgeven** pictogram op de bovenkant.
1. Download het bestand `ui\_config.json` . Verwijder het volgende codefragment uit het gedownloade bestand:

   ```json
   {
       "component":"tab",
       "id":"workflow",
       "title":"Manage",
       "on-click":"APP_MODE_CHANGE",
       "items":
       [
           {
               "component":"label",
               "label":"Manage"
           }
       ]
   },
   ```

1. Upload het bijgewerkte bestand ui\_config.json.

Merk op dat **leidt** filter niet meer beschikbaar is.

**Bovenliggend onderwerp:**&#x200B;[&#x200B; pas de Redacteur van het Web &#x200B;](conf-web-editor.md) aan
