---
title: Bestanden downloaden
description: Leer hoe u bestanden downloadt van de DITA-kaartconsole in AEM hulplijnen en een DITA-kaartbestand exporteert in AEM opslagplaats.
exl-id: ae9eb355-d3ac-446a-958b-5f2da43f5533
feature: Content Management
role: User
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Bestanden downloaden {#id216MC0H0BE8}

U kunt elementen downloaden, zoals DITA- en niet-DITA-bestanden. Er zijn meerdere manieren waarop u elementen kunt downloaden. Sommige methoden zijn native voor AEM en andere worden ondersteund door AEM hulplijnen. Voor downloadinformatie over native AEM middelen raadpleegt u [Middelen downloaden van Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/download-assets-from-aem.html) in AEM documentatie. In de volgende sectie wordt het mechanisme uitgelegd voor het downloaden van bestanden via de DITA-kaartconsole in AEM hulplijnen.

## Een DITA-toewijzingsbestand exporteren

Zodra u het DITA kaartdossier in de AEM bewaarplaats hebt, kunt u het kaartdossier samen met zijn gebiedsdelen downloaden. Dit geeft u de flexibiliteit om het volledige kaartdossier voor off-line het uitgeven, bevestiging, overzicht, of eenvoudig het creëren van een steun te delen.

Voer de volgende stappen uit om een DITA kaartdossier samen met zijn afhankelijke dossiers te downloaden:

1. Navigeer in de interface Middelen naar de DITA-kaart die u wilt downloaden.

1. Klik op de kaart DITA om het in DITA kaartconsole te openen.

1. Selecteer de **Onderwerpen** om een lijst van onderwerpen te zien beschikbaar in de kaart DITA.

1. Klik in de hoofdwerkbalk op **Kaart downloaden**.

   Het dialoogvenster Kaart downloaden wordt geopend.

   ![](images/download-map.png){width="300" align="left"}

1. Klikken **Downloaden**. In het dialoogvenster Kaart downloaden kunt u de volgende opties kiezen:

   - **Basislijn gebruiken**: Selecteer deze optie om een lijst met basislijnen op te halen die voor de DITA-kaart zijn gemaakt. Als u het kaartbestand en de inhoud ervan wilt downloaden op basis van een specifieke basislijn, selecteert u de basislijn in de vervolgkeuzelijst. Zie voor meer informatie over het werken met Baselines [Werken met basislijn](generate-output-use-baseline-for-publishing.md#).
   - **Bestandshiërarchie afvlakken**: Selecteer deze optie als u alle onderwerpen en mediabestanden waarnaar wordt verwezen, in één map wilt opslaan.
   >[!NOTE]
   >
   > U kunt het kaartbestand ook downloaden zonder een optie te selecteren. In dat geval wordt de laatste voortgezette versie van de onderwerpen waarnaar wordt verwezen en de mediabestanden gedownload.

1. Nadat u op de knop **Downloaden** knop, wordt de aanvraag voor het downloaden van de kaart in de wachtrij geplaatst. U ontvangt het volgende bericht zodra de kaart kan worden gedownload.

   ![](images/download-map-prompt.png){width="550" align="left"}

   - Klikken **Downloaden** om het kaartbestand in .zip-indeling te downloaden.

   - Klikken **Later downloaden** om het kaartbestand later te downloaden. De downloadkoppeling is toegankelijk via het AEM-meldingsvak. Klik op het gegenereerde kaartbericht in het Postvak In om de kaart in de ZIP-indeling te downloaden.

   >[!NOTE]
   >
   > Standaard blijven de gedownloade kaarten vijf dagen in het AEM-vak.

![](images/download-map-inbox.png){width="300" align="left"}

Nadat de kaart is gedownload, kunt u de kaart selecteren en het pictogram Openen bovenaan gebruiken om het geselecteerde rapport te openen.

**Bovenliggend onderwerp:**[ Inhoud beheren](authoring.md)
