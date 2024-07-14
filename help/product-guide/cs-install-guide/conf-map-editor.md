---
title: De Geavanceerde Kaarteditor instellen als standaard
description: Leer hoe u de Geavanceerde Kaarteditor instelt als standaard
exl-id: 365264ab-f990-42c1-ab79-61a40ecea42f
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# De Geavanceerde Kaarteditor instellen als standaard {#id181AI0003PN}

AEM Guides wordt geleverd met een Basic Map Editor en een Advanced Map Editor. De Basis Redacteur van de Kaart geeft u alle noodzakelijke eigenschappen om uw kaartdossier tot stand te brengen. De Geavanceerde Redacteur van de Kaart is veel eigenschaprijker en het is geïntegreerd binnen de Redacteur van het Web. Met de Geavanceerde Kaarteditor kunnen auteurs DITA-kaartbestanden maken en bewerken met een gebruiksvriendelijke interface.

Wanneer een nieuw kaartbestand wordt gemaakt, wordt dit standaard geopend in de Basic Map Editor. U kunt dit gedrag veranderen door het plaatsen toe te laten om de Geavanceerde Redacteur van de Kaart door gebrek te openen.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om de Basic Map Editor in te schakelen:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | ``fmdita.hide.oldmapeditor`` | Boolean \(true/false\). Als u de Geavanceerde Redacteur van de Kaart door gebrek wilt gebruiken, dan plaats dit bezit aan waar.<br> **Standaardwaarde**: vals |

>[!NOTE]
>
> Wanneer een auteur een kaartbestand maakt en ervoor kiest dit te openen om te bewerken, wordt standaard de Basic Map Editor gestart. Als de optie Bewerken is geselecteerd voor een kaartbestand in de gebruikersinterface van Assets, wordt deze ook geopend in de basiskaarteditor.

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
