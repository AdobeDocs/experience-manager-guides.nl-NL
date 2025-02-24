---
title: Bestanden downloaden
description: Leer hoe u bestanden downloadt van de DITA-kaartconsole in AEM Guides en een DITA-kaartbestand exporteert in de AEM-opslagplaats.
exl-id: ae9eb355-d3ac-446a-958b-5f2da43f5533
feature: Content Management
role: User
source-git-commit: f3858b1694837c7a3fa7bb222ed8ff31ce7103f8
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Bestanden downloaden {#id216MC0H0BE8}

U kunt elementen downloaden, zoals DITA- en niet-DITA-bestanden. Er zijn meerdere manieren waarop u elementen kunt downloaden. Sommige methoden zijn native voor Adobe Experience Manager en andere worden ondersteund door Adobe Experience Manager Guides. Voor inheemse Adobe Experience Manager activa downloadinformatie, mening [ de activa van de Download van Adobe Experience Manager ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/download-assets-from-aem.html) in de documentatie van Adobe Experience Manager. In de volgende sectie wordt uitgelegd hoe u bestanden downloadt via de DITA-kaartconsole in Experience Manager Guides.

## Een DITA-toewijzingsbestand exporteren

Als u het DITA-kaartbestand eenmaal in de Adobe Experience Manager-opslagplaats hebt, kunt u het kaartbestand samen met de afhankelijke bestanden downloaden. Dit geeft u de flexibiliteit om het volledige kaartdossier voor off-line het uitgeven, bevestiging, overzicht, of eenvoudig het creëren van een steun te delen.

Voer de volgende stappen uit om een DITA kaartdossier samen met zijn afhankelijke dossiers te downloaden:

1. Navigeer in de gebruikersinterface van Assets naar de DITA-kaart die u wilt downloaden.

1. Selecteer de kaart DITA om het in DITA kaartconsole te openen.

1. Selecteer het **lusje van Onderwerpen** om de lijst van onderwerpen te bekijken beschikbaar in de kaart DITA.

1. In de belangrijkste toolbar, uitgezochte **Kaart van de Download**.

   Het dialoogvenster Kaart downloaden wordt geopend.

   ![](images/download-map.png){width="300" align="left"}

1. Selecteer **Download**. In het dialoogvenster Kaart downloaden kunt u de volgende opties kiezen:

   - **Basislijn van het Gebruik**: Selecteer deze optie om een lijst van Basislijnen te krijgen die voor de kaart DITA worden gecreeerd. Als u het kaartbestand en de inhoud ervan wilt downloaden op basis van een specifieke basislijn, selecteert u de basislijn in de vervolgkeuzelijst. Voor meer details over het werken met Basislijnen, mening [ Werk met Basislijn ](generate-output-use-baseline-for-publishing.md#).
   - **de Hiërarchie van het Dossier van de Afvlakking**: Selecteer deze optie om alle referenced onderwerpen en media dossiers in één enkele omslag te bewaren.
   >[!NOTE]
   >
   > U kunt het kaartbestand ook downloaden zonder een optie te selecteren. In dat geval wordt de laatste voortgezette versie van de onderwerpen waarnaar wordt verwezen en de mediabestanden gedownload.

1. Nadat u de **knoop van de Download** selecteert, wordt het verzoek van de kaartdownload een rij gevormd. U ontvangt het volgende bericht zodra de kaart kan worden gedownload.

   ![](images/download-map-prompt.png){width="550" align="left"}

   - Selecteer **Download** om het kaartdossier in.zip formaat te downloaden.

   - Selecteer **Later Download** om het kaartdossier in een recentere tijd te downloaden. U kunt de downloadkoppeling openen via het Adobe Experience Manager-meldingsvak. Selecteer het gegenereerde kaartbericht in het Postvak In als u de kaart in de ZIP-indeling wilt downloaden.

   >[!NOTE]
   >
   > Standaard blijven de gedownloade kaarten vijf dagen in het Adobe Experience Manager-berichtvenster Inbox staan.

![](images/download-map-inbox.png){width="300" align="left"}

Nadat de kaart is gedownload, kunt u de kaart selecteren en het pictogram Openen bovenaan gebruiken om het geselecteerde rapport te openen.

**Bovenliggend onderwerp:**[ beheert inhoud ](authoring.md)
