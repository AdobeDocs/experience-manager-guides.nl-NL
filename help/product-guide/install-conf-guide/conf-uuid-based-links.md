---
title: Weergave van op UUID gebaseerde koppelingen configureren
description: Leer hoe u weergave van UUID-koppelingen kunt configureren
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Weergave van op UUID gebaseerde koppelingen configureren {#id2035G20M0QN}

Wanneer u een koppeling maakt met de optie Referentie invoegen of Inhoud hergebruik invoegen in de Editor, wordt de koppeling standaard gemaakt met de UUID van de inhoud waarnaar wordt verwezen. Het **bezit van de Verbinding** \ (in het paneel van Eigenschappen \) van de referenced inhoud kan worden gevormd om de relatieve dossierweg van de referenced inhoud of UUID te tonen. Voor Cloud Service wordt standaard de UUID van de inhoud waarnaar wordt verwezen weergegeven in het deelvenster Eigenschappen. Voor Op locatie, wordt deze vertoning gecontroleerd door **laat optie UUIDs** in `configMgr` toe. De optie is standaard ingeschakeld, wat betekent dat de UUID van de inhoud waarnaar wordt verwezen, wordt weergegeven in het deelvenster Eigenschappen.

Op de volgende tabbladen vindt u instructies voor het weergeven van het relatieve pad of de UUID van de inhoud waarnaar wordt verwezen in de Editor, op basis van uw Experience Manager Guides-instelling: Cloud Service of Op locatie.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om het relatieve pad of de UUID van de inhoud waarnaar wordt verwezen, weer te geven in de Editor.

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.uuid` | Boolean \(true/false\). Als u het relatieve pad van de gekoppelde inhoud wilt weergeven, stelt u deze eigenschap in op false. <br> **Standaardwaarde**: waar |


>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. In de *montages 0&rbrace; XmlEditorConfig,* laat **optie UUIDs toe wordt toegelaten door gebrek.** Dit impliceert dat UUID van de referenced inhoud in het **bezit van de Verbinding** in het paneel van Eigenschappen wordt getoond.

   Als u de relatieve weg van de verbonden inhoud wilt tonen, dan schrap **toelaten UIDs** optie.

1. Klik **sparen**.

>[!ENDTABS]

**Bovenliggend onderwerp:**&#x200B;[&#x200B; pas de Redacteur van het Web &#x200B;](customize-overview.md) aan
