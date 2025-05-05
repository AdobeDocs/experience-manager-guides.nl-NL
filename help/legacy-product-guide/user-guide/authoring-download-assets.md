---
title: Bestanden downloaden
description: Leer hoe u bestanden downloadt van de DITA-kaartconsole in AEM Guides en een DITA-kaartbestand exporteert in de AEM-opslagplaats.
feature: Content Management
role: User
hide: true
exl-id: b04a0abe-a029-44ac-b8f4-138d78908d44
source-git-commit: 7286c3fb36695caa08157296fd6e0de722078c2b
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Bestanden downloaden {#id216MC0H0BE8}

U kunt elementen downloaden, zoals DITA- en niet-DITA-bestanden. Er zijn meerdere manieren waarop u elementen kunt downloaden. Sommige methoden zijn native voor AEM en andere worden ondersteund door AEM Guides. Voor de inheemse informatie van de activadownload van AEM, zie [ activa van Adobe Experience Manager ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/download-assets-from-aem.html?lang=nl-NL) in de documentatie van AEM downloaden. In de volgende sectie wordt uitgelegd hoe u bestanden downloadt via de DITA-kaartconsole in AEM Guides.

## Een DITA-toewijzingsbestand exporteren

Als u het DITA-kaartbestand eenmaal in de AEM-opslagplaats hebt, kunt u het kaartbestand samen met de afhankelijke bestanden downloaden. Dit geeft u de flexibiliteit om het volledige kaartdossier voor off-line het uitgeven, bevestiging, overzicht, of eenvoudig het creëren van een steun te delen.

Voer de volgende stappen uit om een DITA kaartdossier samen met zijn afhankelijke dossiers te downloaden:

1. Navigeer in de gebruikersinterface van Assets naar de DITA-kaart die u wilt downloaden.

1. Klik op de kaart DITA om het in DITA kaartconsole te openen.

1. Selecteer het **lusje van Onderwerpen** om een lijst van onderwerpen beschikbaar in de kaart te zien DITA.

1. In de belangrijkste toolbar, klik **Kaart van de Download**.

   Het dialoogvenster Kaart downloaden wordt geopend.

   ![](images/download-map.png){width="300" align="left"}

1. Klik **Download**. In het dialoogvenster Kaart downloaden kunt u de volgende opties kiezen:

   - **Basislijn van het Gebruik**: Selecteer deze optie om een lijst van Basislijnen te krijgen die voor de kaart DITA worden gecreeerd. Als u het kaartbestand en de inhoud ervan wilt downloaden op basis van een specifieke basislijn, selecteert u de basislijn in de vervolgkeuzelijst. Voor meer details over het werken met Basislijnen, zie [ Werk met Basislijn ](generate-output-use-baseline-for-publishing.md#).
   - **de Hiërarchie van het Dossier van de Afvlakking**: Selecteer deze optie om alle referenced onderwerpen en media dossiers in één enkele omslag te bewaren.

   >[!NOTE]
   >
   > U kunt het kaartbestand ook downloaden zonder een optie te selecteren. In dat geval wordt de laatste voortgezette versie van de onderwerpen waarnaar wordt verwezen en de mediabestanden gedownload.

1. Nadat u de **knoop van de Download** klikt, wordt het verzoek van de kaartdownload een rij gevormd. U ontvangt het volgende bericht zodra de kaart kan worden gedownload.

   ![](images/download-map-prompt.png){width="550" align="left"}

   - Klik **Download** om het kaartdossier in.zip formaat te downloaden.

   - Klik **Later Download** om het kaartdossier in een recentere tijd te downloaden. U kunt de downloadkoppeling openen via het AEM-meldingsvak. Klik op het gegenereerde kaartbericht in het Postvak In om de kaart in de ZIP-indeling te downloaden.

   >[!NOTE]
   >
   > Standaard blijven de gedownloade kaarten vijf dagen in het AEM-berichtvenster Inbox staan.

![](images/download-map-inbox.png){width="300" align="left"}

Nadat de kaart is gedownload, kunt u de kaart selecteren en het pictogram Openen bovenaan gebruiken om het geselecteerde rapport te openen.

**Bovenliggend onderwerp:**&#x200B;[ beheert inhoud ](authoring.md)
