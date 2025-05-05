---
title: Eén onderwerp PDF genereren
description: Leer hoe te om enige onderwerpgeneratie te vormen PDF
exl-id: 5b66fd3b-6450-49ce-b06e-d2d5bab37990
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Eén onderwerp PDF genereren {#id22ADC70M0XA}

Met AEM Guides kunt u de PDF van afzonderlijke onderwerpen of een volledig kaartbestand genereren. U kunt uw onderwerpen in een formaat van PDF publiceren gebruikend inheemse PDF of methode DITA-OT. Gebruik de native PDF-methode om een PDF-uitvoer met veel functies te genereren op basis van W3C CSS3 en CSS-normen voor gepagineerde media. U kunt de methode DITA-OT gebruiken om een output van PDF voor een kaart van het kaartdashboard te produceren.

>[!NOTE]
>
> Native PDF is de standaardmethode voor het genereren van een PDF in de huidige versie van AEM Guides.

Om de oude generatie van PDF via DITA-OT van de wijze van de onderwerpvoorproef toe te laten, voer de volgende stappen uit:

1. Meld u aan bij Adobe Experience Manager als beheerder en download het configuratiebestand voor de gebruikersinterface.

1. Om dit te doen, klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **Profielen van de Omslag**.
1. Klik op de **Globale tegel van het Profiel**.
1. Selecteer het **lusje van de Configuratie van de Redacteur van XML** en klik **uitgeven** pictogram op de bovenkant
1. Klik het **pictogram van de Download** om het ui \_config.json- dossier op uw lokaal systeem te downloaden. Vervolgens kunt u wijzigingen in het bestand aanbrengen en het bestand vervolgens uploaden.
1. Zoek in het `ui_config.json` -bestand naar de volgende configuratie:

   ```
   {
                           "component": "button",
                           "variant": "action",
                           "quiet": true,
                           "icon": "filePDF",
                           "title": "Download as PDF",
                           "on-click": "EDITOR_SAVE_AS_PDF"
                           }
   ```

   en vervangen door

   ```
   {
                           "component": "button",
                           "icon": "filePDF",
                           "variant": "action",
                           "quiet": true, "title": "Export as PDF",
                           "on-click": "DOWNLOAD_TOPIC_PDF",
                           "show" : ["@isPreviewMode", "@isXmlMode"]
                           }
   ```

1. Sla het bestand op en upload het.

Na het uitvoeren van de bovengenoemde stappen, als u het zelfde omslagprofiel van de Voorkeur van de Gebruiker in de Redacteur van het Web kiest, zult u dan de optie voor de generatie van PDF op de voorproefwijze van een onderwerp zien.

**Bovenliggend onderwerp:**&#x200B;[ pas de Redacteur van het Web ](conf-web-editor.md) aan
