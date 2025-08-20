---
title: Opmerkingen bij de release | Nieuwe functies in de Adobe Experience Manager Guides 2025.06.0-release
description: Meer informatie over de nieuwe en verbeterde functies in de 2025.06.0-release van Adobe Experience Manager Guides
role: Leader
exl-id: 48f27aa6-d870-4228-8e62-db81699a25f7
source-git-commit: d418ffb254b11430509609b91e0174690815cf73
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Nieuwe functies in de release 2025.06.0 (juni 2025)

Dit artikel behandelt de nieuwe en verbeterde functies die zijn geïntroduceerd met de release 2025.06.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor de lijst van kwesties die in deze versie worden bevestigd, mening [ Vaste kwesties in de versie 2025.06.0 ](fixed-issues-2025-06-0.md).

Leer over [ verbeteringsinstructies voor de versie 2025.06.0 ](../release-info/upgrade-instructions-2025-06-0.md).

## Time-outmelding voor sessie om onbedoeld verlies van inhoud te voorkomen

Er verschijnt nu een pop-upbericht waarin u wordt gewaarschuwd wanneer uw Adobe Experience Manager-sessie verloopt en u bent afgemeld wegens inactiviteit. Dit bericht wordt geactiveerd wanneer u inhoud in Experience Manager Guides probeert te bewerken nadat de sessie is beëindigd. De functie helpt het risico op verlies van niet-opgeslagen werk te verminderen en verbetert de algehele betrouwbaarheid en vloeiendheid van de ervaring, zelfs tijdens perioden van inactiviteit.

![](assets/sign-out-prompt.png)

Leer meer over [ herinnering van de zittingsonderbreking ](../user-guide/session-timeout-prompt.md) in Experience Manager Guides.

## Verbeterde opties voor kaartdownloaden in de Editor

Experience Manager Guides introduceert een nieuwe **Echte het dossiernamen van het Gebruik** optie in de **kaart van de Download** dialoog. Wanneer u nu kaartbestanden downloadt, kunt u ervoor kiezen de oorspronkelijke bestandsnamen te behouden in plaats van de standaard-UUID&#39;s, waardoor het veel eenvoudiger wordt om uw bestanden te herkennen en te beheren. Deze optie is slechts beschikbaar als u **selecteert behoud dossierhiërarchie** en gehandicapt wanneer u **kiest afvlakken dossierhiërarchie**, die u meer flexibiliteit geeft in het organiseren van uw gedownloade kaarten.

Voor meer details, mening [ dossiers van de Download ](../user-guide/authoring-download-assets.md#download-a-dita-map-file-from-the-editor).

![](assets/download-map-dialog-new.png){width="300" align="left"}


## Verbeterde `navref` afhandeling in de Editor

De meest recente verbeteringen aan de Editor verbeteren de verwerking van `navref` -elementen in een DITA-kaart. Nu, wanneer u een `navref` element aan een kaart toevoegt, opent de **Uitgezochte weg** dialoog, toestaand u om de kaartverwijzingen gemakkelijk te kiezen om als navigatiekoppelingen in uw kaart te omvatten. Nadat de titel van de toegevoegde kaart is toegevoegd, wordt deze zowel in de ontwerpweergave als in de layoutweergave weergegeven, zodat de opgenomen navigatie tijdens het ontwerpen beter zichtbaar is.  Bovendien wordt het toegevoegde `navref` -element automatisch omgezet om de doorverwezen kaart in de Editor weer te geven.

Voor meer details, voegt de mening [ navigatieverwijzingen ](../user-guide/map-editor-other-features.md#add-navigation-references) toe.

## Prestatieverbeteringen in AI Assistant

De release introduceert verbeteringen voor de AI Assistant-backendengine, die betere prestaties en grotere stabiliteit biedt. U kunt deze update inschakelen en doorgaan met de Help van AI Assistant:

- Werk de `chat.url` configuratie bij om op het nieuwe eindpunt URL te wijzen.
- Voeg een nieuwe omgevingsvariabele `GUIDES_AI_SITE_ID` toe in Cloud Manager.

Voor details, vormt de mening [ de Medewerker AI ](../cs-install-guide/conf-smart-suggestions.md).

