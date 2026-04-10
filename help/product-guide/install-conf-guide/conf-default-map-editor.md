---
title: De Geavanceerde Kaarteditor instellen als standaard
description: Leer hoe u de Geavanceerde Kaarteditor instelt als standaard
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# De Geavanceerde Kaarteditor instellen als standaard {#id181AI0003PN}

>[!NOTE]
>
> De Basic Map Editor, die voorheen beschikbaar was in Experience Manager Guides, is vanaf versie 4.3 en 2307 vervangen. U kunt tot de Basis Redacteur van de Kaart niet toegang hebben om kaarten te creëren en te beheren DITA.
>U wordt geadviseerd om de Geavanceerde Redacteur van de Kaart te gebruiken. De geavanceerde Kaarteditor biedt verbeterde functies en betere aanpassingsopties. Onderzoek meer over hoe te met de [ Geavanceerde Redacteur van de Kaart ](../user-guide/map-editor-advanced-map-editor.md) te werken.

Voor versies ouder dan 4.3 en 2307, komt Experience Manager Guides met de Basis Redacteur van de Kaart en een Geavanceerde Redacteur van de Kaart. De Basis Redacteur van de Kaart geeft u alle noodzakelijke eigenschappen om uw kaartdossier tot stand te brengen. De Geavanceerde Redacteur van de Kaart is veel eigenschaprijker en het is geïntegreerd binnen de Redacteur van het Web. Met de Geavanceerde Kaarteditor kunnen auteurs DITA-kaartbestanden maken en bewerken met een gebruiksvriendelijke interface.

Wanneer een nieuw kaartbestand wordt gemaakt, wordt dit standaard geopend in de Basic Map Editor. U kunt dit gedrag veranderen door het plaatsen toe te laten om de Geavanceerde Redacteur van de Kaart door gebrek te openen.

Op de volgende tabbladen vindt u instructies voor het instellen van de Geavanceerde Kaarteditor als de standaardeditor voor de kaartbestanden op basis van de Experience Manager Guides-instelling: Cloud Service of On-Premise.


>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om de Basic Map Editor in te schakelen:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | ``fmdita.hide.oldmapeditor`` | Boolean \(true/false\). Als u de Geavanceerde Redacteur van de Kaart door gebrek wilt gebruiken, dan plaats dit bezit aan waar.<br> **Standaardwaarde**: vals |

>[!NOTE]
>
> Wanneer een auteur een kaartbestand maakt en ervoor kiest dit te openen om te bewerken, wordt standaard de Basic Map Editor gestart. Als de optie Bewerken is geselecteerd voor een kaartbestand in de gebruikersinterface van Assets, wordt deze ook geopend in de basiskaarteditor.

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. Selecteer de **Basisoptie van de Redacteur van de Kaart van de Verbergen**.

   Als deze optie is geselecteerd, zien gebruikers nergens in de gebruikersinterface de koppeling Basic Map Editor. Standaard worden kaartbestanden geopend in de Geavanceerde Kaarteditor.

>[!ENDTABS]

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](customize-overview.md) aan
