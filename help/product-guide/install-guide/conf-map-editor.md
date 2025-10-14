---
title: De Geavanceerde Kaarteditor instellen als standaard
description: Leer hoe u de Geavanceerde Kaarteditor instelt als standaard
exl-id: ecc023f6-48eb-4afd-97a2-4b3cdd5a8991
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 126cecdaa481b9da1add4ba3664c26c2bc5da068
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# De Geavanceerde Kaarteditor instellen als standaard {#id181AI0003PN}

>[!NOTE]
>
> De Basic Map Editor, die voorheen beschikbaar was in Experience Manager Guides, is vanaf versie 4.3 en 2307 vervangen. U kunt tot de Basis Redacteur van de Kaart niet toegang hebben om kaarten te creëren en te beheren DITA.
>U wordt geadviseerd om de Geavanceerde Redacteur van de Kaart te gebruiken. De geavanceerde Kaarteditor biedt verbeterde functies en betere aanpassingsopties. Onderzoek meer over hoe te met de [&#x200B; Geavanceerde Redacteur van de Kaart &#x200B;](../user-guide/map-editor-advanced-map-editor.md) te werken.

Voor versies ouder dan 4.3 en 2307, komt Experience Manager Guides met de Basis Redacteur van de Kaart en een Geavanceerde Redacteur van de Kaart. De Basis Redacteur van de Kaart geeft u alle noodzakelijke eigenschappen om uw kaartdossier tot stand te brengen. De Geavanceerde Redacteur van de Kaart is veel eigenschaprijker en het is geïntegreerd binnen de Redacteur van het Web. Met de Geavanceerde Kaarteditor kunnen auteurs DITA-kaartbestanden maken en bewerken met een gebruiksvriendelijke interface.

Wanneer een nieuw kaartbestand wordt gemaakt, wordt dit standaard geopend in de Basic Map Editor. U kunt dit gedrag veranderen door het plaatsen toe te laten om de Geavanceerde Redacteur van de Kaart door gebrek te openen.

Voer de volgende stappen uit om van de Geavanceerde Redacteur van de Kaart als standaardredacteur voor de kaartdossiers te maken:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. Selecteer de **Basisoptie van de Redacteur van de Kaart van de Verbergen**.

   Als deze optie is geselecteerd, zien gebruikers nergens in de gebruikersinterface de koppeling Basic Map Editor. Standaard worden kaartbestanden geopend in de Geavanceerde Kaarteditor.
