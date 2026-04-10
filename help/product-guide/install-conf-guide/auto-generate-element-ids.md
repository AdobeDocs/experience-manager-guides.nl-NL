---
title: Element-id's automatisch genereren
description: Leer hoe u elementen-id's automatisch kunt genereren
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Element-id&#39;s automatisch genereren {#id20CIL40016I}

AEM Guides genereert een document-id voor elk nieuw document dat u maakt. Wanneer u bijvoorbeeld een DITA-kaart maakt, wordt een id als `map.ditamap_random_digits` toegewezen aan de id van de kaart. U kunt ook elementen definiëren waarop automatisch een id wordt gegenereerd en toegewezen.

AEM Guides biedt eenvoudige configuratie-instellingen waarbij u de elementen moet definiëren waarop een id automatisch wordt gegenereerd en een patroon voor de id. Standaard zijn bepaalde elementen, zoals `section` , `table` , `ul` en `ol` , geconfigureerd voor het automatisch genereren van een id. U kunt andere elementen aan deze lijst toevoegen zodat wanneer deze elementen in een document worden opgenomen, AEM Guides een id genereert en toewijst op basis van het opgegeven patroon.

Op de volgende tabbladen vindt u instructies voor het configureren van elementen voor automatisch gegenereerde id op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om automatisch gegenereerde element-id&#39;s te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.classes` | Geef een door komma&#39;s gescheiden lijst met elementen op. <br> **Standaardwaarde**: `"topic, section, table, simpletable, fig, image, ul, ol"` |

Als u een patroon voor automatisch gegenereerde id wilt configureren, maakt u een configuratiebestand met de volgende eigenschappen:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.pattern` | De standaardwaarde voor dit veld is ingesteld op `${elementName}_${id}` . De waarde `${elementName}` wordt vervangen door de naam van het element. De variabele `${id}` genereert een volgnummer voor het element. Als u bijvoorbeeld het alinea-element toewijst voor automatisch gegenereerde id&#39;s, krijgt de eerste alinea van het onderwerp of document een id zoals p\_1, de volgende alinea krijgt p\_2 enzovoort. In een ander document wordt het genereren van de id echter opnieuw gestart. Dit betekent dat id&#39;s zoals p\_1 en p\_2 in een ander document kunnen worden toegewezen aan alinea-elementen. **Standaardwaarde**: ``${elementName}_${id}`` |

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. In de *montages 0&rbrace; XmlEditorConfig, specificeer één of meerdere elementen in* Auto produceert IDs voor het gebied van de Markeringen van het Element **.**

   >[!NOTE]
   >
   > Elementlabels zijn de namen van DITA-elementen, zoals `body` , `title` , `codeblock` , enzovoort. Als u meerdere elementen wilt opgeven, scheidt u de elementnamen met een komma.

1. Op het **Patroon voor het Genereren van identiteitskaarts** gebied, specificeer een patroon om een identiteitskaart te produceren.

   De standaardwaarde voor dit veld is ingesteld op `${elementName}_${id}` . De waarde `${elementName}` wordt vervangen door de naam van het element. De variabele `${id}` genereert een volgnummer voor het element. Als u bijvoorbeeld het alinea-element toewijst voor automatisch gegenereerde id&#39;s, krijgt de eerste alinea van het onderwerp of document een id zoals p\_1, de volgende alinea krijgt p\_2 enzovoort. In een ander document wordt het genereren van de id echter opnieuw gestart. Dit betekent dat id&#39;s zoals p\_1 en p\_2 in een ander document kunnen worden toegewezen aan alinea-elementen.

   Als uw document al id&#39;s bevat in het opgegeven patroon, worden deze id&#39;s door het proces voor automatisch genereren niet aan nieuwe elementen toegewezen.

1. Klik **sparen**.

>[!ENDTABS]

**Bovenliggend onderwerp:**&#x200B;[&#x200B; pas de Redacteur van het Web &#x200B;](customize-overview.md) aan
