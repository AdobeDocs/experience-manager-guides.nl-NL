---
title: Eén onderwerp voor PDF-generatie configureren
description: Leer hoe te om enige onderwerpPDF te vormen generatie
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Eén onderwerp voor PDF-generatie configureren voor Cloud Service

Met de AEM Guides kunt u de PDF van afzonderlijke onderwerpen of een volledig kaartbestand genereren. U kunt uw onderwerpen in PDF-indeling publiceren met behulp van de native PDF- of DITA-OT-methode. Gebruik de native PDF-methode om een veelzijdige PDF-uitvoer te genereren op basis van W3C CSS3 en CSS-normen voor gepagineerde media. U kunt de methode DITA-OT gebruiken om een uitvoer van PDF voor een kaart van het kaartdashboard te produceren.

>[!NOTE]
>
> Native PDF is de standaardmethode voor het genereren van een PDF in de huidige versie van AEM Guides.

Voer de volgende stappen uit om de oude PDF-generatie via de DITA-OT vanuit de modus voor onderwerpvoorvertoning in te schakelen:

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

**Bovenliggend onderwerp:**&#x200B;[&#x200B; pas de Redacteur van het Web &#x200B;](customize-overview.md) aan
