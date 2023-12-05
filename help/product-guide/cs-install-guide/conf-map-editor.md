---
title: De Geavanceerde Kaarteditor instellen als standaard
description: Leer hoe u de Geavanceerde Kaarteditor instelt als standaard
exl-id: 365264ab-f990-42c1-ab79-61a40ecea42f
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# De Geavanceerde Kaarteditor instellen als standaard {#id181AI0003PN}

AEM Hulplijnen worden geleverd met een Basic Map Editor en een Advanced Map Editor. De Basis Redacteur van de Kaart geeft u alle noodzakelijke eigenschappen om uw kaartdossier tot stand te brengen. De Geavanceerde Redacteur van de Kaart is veel eigenschaprijker en het is geïntegreerd binnen de Redacteur van het Web. Met de Geavanceerde Kaarteditor kunnen auteurs DITA-kaartbestanden maken en bewerken met een gebruiksvriendelijke interface.

Wanneer een nieuw kaartbestand wordt gemaakt, wordt dit standaard geopend in de Basic Map Editor. U kunt dit gedrag veranderen door het plaatsen toe te laten om de Geavanceerde Redacteur van de Kaart door gebrek te openen.

Gebruik de instructies die worden gegeven in [Configuratieoverschrijvingen](download-install-additional-config-override.md#) om het configuratiebestand te maken. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om de Basic Map Editor in te schakelen:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | ``fmdita.hide.oldmapeditor`` | Boolean \(true/false\). Als u de Geavanceerde Redacteur van de Kaart door gebrek wilt gebruiken, dan plaats dit bezit aan waar.<br> **Standaardwaarde**: false |

>[!NOTE]
>
> Wanneer een auteur een kaartbestand maakt en ervoor kiest dit te openen om te bewerken, wordt standaard de Basic Map Editor gestart. Wanneer de optie Bewerken is geselecteerd voor een kaartbestand in de interface Elementen, wordt deze ook geopend in de basiskaarteditor.

**Bovenliggend onderwerp:**[ Webeditor aanpassen](conf-web-editor.md)
