---
title: De Geavanceerde Kaarteditor instellen als standaard
description: Leer hoe u de Geavanceerde Kaarteditor instelt als standaard
exl-id: 365264ab-f990-42c1-ab79-61a40ecea42f
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 126cecdaa481b9da1add4ba3664c26c2bc5da068
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# De Geavanceerde Kaarteditor instellen als standaard {#id181AI0003PN}

>[!NOTE]
>
> De Basic Map Editor, die voorheen beschikbaar was in Experience Manager Guides, is vanaf versie 4.3 en 2307 vervangen. U kunt tot de Basis Redacteur van de Kaart niet toegang hebben om kaarten te creëren en te beheren DITA.
>U wordt geadviseerd om de Geavanceerde Redacteur van de Kaart te gebruiken. De geavanceerde Kaarteditor biedt verbeterde functies en betere aanpassingsopties. Onderzoek meer over hoe te met de [ Geavanceerde Redacteur van de Kaart ](../user-guide/map-editor-advanced-map-editor.md) te werken.

Voor versies ouder dan 4.3 en 2307, komt Experience Manager Guides met de Basis Redacteur van de Kaart en een Geavanceerde Redacteur van de Kaart. De Basis Redacteur van de Kaart geeft u alle noodzakelijke eigenschappen om uw kaartdossier tot stand te brengen. De Geavanceerde Redacteur van de Kaart is veel eigenschaprijker en het is geïntegreerd binnen de Redacteur van het Web. Met de Geavanceerde Kaarteditor kunnen auteurs DITA-kaartbestanden maken en bewerken met een gebruiksvriendelijke interface.

Wanneer een nieuw kaartbestand wordt gemaakt, wordt dit standaard geopend in de Basic Map Editor. U kunt dit gedrag veranderen door het plaatsen toe te laten om de Geavanceerde Redacteur van de Kaart door gebrek te openen.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om de Basic Map Editor in te schakelen:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | ``fmdita.hide.oldmapeditor`` | Boolean \(true/false\). Als u de Geavanceerde Redacteur van de Kaart door gebrek wilt gebruiken, dan plaats dit bezit aan waar.<br> **Standaardwaarde**: vals |

>[!NOTE]
>
> Wanneer een auteur een kaartbestand maakt en ervoor kiest dit te openen om te bewerken, wordt standaard de Basic Map Editor gestart. Als de optie Bewerken is geselecteerd voor een kaartbestand in de gebruikersinterface van Assets, wordt deze ook geopend in de basiskaarteditor.

**Bovenliggend onderwerp:**&#x200B;[ pas de Redacteur van het Web ](conf-web-editor.md) aan
