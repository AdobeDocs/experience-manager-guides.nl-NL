---
title: Element-id's automatisch genereren
description: Leer hoe u elementen-id's automatisch kunt genereren
exl-id: a651db7f-228e-4de5-b569-3f1b4f86c418
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Element-id&#39;s automatisch genereren {#id20CIL40016I}

AEM Guides genereert een document-id voor elk nieuw document dat u maakt. Wanneer u bijvoorbeeld een DITA-kaart maakt, wordt een id als `map.ditamap_random_digits` toegewezen aan de id van de kaart. U kunt ook elementen definiëren waarop automatisch een id wordt gegenereerd en toegewezen.

AEM Guides biedt eenvoudige configuratie-instellingen waarbij u de elementen moet definiëren waarop een id automatisch wordt gegenereerd en een patroon voor de id. Standaard zijn bepaalde elementen, zoals `section` , `table` , `ul` en `ol` , geconfigureerd voor het automatisch genereren van een id. U kunt andere elementen aan deze lijst toevoegen zodat wanneer deze elementen in een document worden opgenomen, AEM Guides een id genereert en toewijst op basis van het opgegeven patroon

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om automatisch gegenereerde element-id&#39;s te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.classes` | Geef een door komma&#39;s gescheiden lijst met elementen op. <br> **Standaardwaarde**: `"topic, section, table, simpletable, fig, image, ul, ol"` |

Als u een patroon voor automatisch gegenereerde id wilt configureren, maakt u een configuratiebestand met de volgende eigenschappen:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.pattern` | De standaardwaarde voor dit veld is ingesteld op `${elementName}_${id}` . De waarde `${elementName}` wordt vervangen door de naam van het element. De variabele `${id}` genereert een volgnummer voor het element. Als u bijvoorbeeld het alinea-element toewijst voor automatisch gegenereerde id&#39;s, krijgt de eerste alinea van het onderwerp of document een id zoals p\_1, de volgende alinea krijgt p\_2 enzovoort. In een ander document wordt het genereren van de id echter opnieuw gestart. Dit betekent dat id&#39;s zoals p\_1 en p\_2 in een ander document kunnen worden toegewezen aan alinea-elementen. **Standaardwaarde**: ``${elementName}_${id}`` |

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
