---
title: Element-id's automatisch genereren
description: Leer hoe u elementen-id's automatisch kunt genereren
exl-id: 8d09ab89-4be5-49f1-9831-9f01c92dc472
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Element-id&#39;s automatisch genereren {#id20CIL40016I}

AEM Guides genereert een document-id voor elk nieuw document dat u maakt. Wanneer u bijvoorbeeld een DITA-kaart maakt, wordt een id als `map.ditamap_random_digits` toegewezen aan de id van de kaart. U kunt ook elementen definiëren waarop automatisch een id wordt gegenereerd en toegewezen.

AEM Guides biedt eenvoudige configuratie-instellingen waarbij u de elementen moet definiëren waarop een id automatisch wordt gegenereerd en een patroon voor de id. Standaard zijn bepaalde elementen, zoals `section` , `table` , `ul` en `ol` , geconfigureerd voor het automatisch genereren van een id. U kunt andere elementen aan deze lijst toevoegen zodat wanneer deze elementen in een document worden opgenomen, AEM Guides een id genereert en toewijst op basis van het opgegeven patroon

Voer de volgende stappen uit om elementen te configureren voor automatisch gegenereerde id:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. In de *montages 0&rbrace; XmlEditorConfig, specificeer één of meerdere elementen in **Auto produceert IDs voor het gebied van de Markeringen van het Element**.*

   >[!NOTE]
   >
   > Elementlabels zijn de namen van DITA-elementen, zoals `body` , `title` , `codeblock` , enzovoort. Als u meerdere elementen wilt opgeven, scheidt u de elementnamen met een komma.

1. Op het **Patroon voor het Genereren van identiteitskaarts** gebied, specificeer een patroon om een identiteitskaart te produceren.

   De standaardwaarde voor dit veld is ingesteld op `${elementName}_${id}` . De waarde `${elementName}` wordt vervangen door de naam van het element. De variabele `${id}` genereert een volgnummer voor het element. Als u bijvoorbeeld het alinea-element toewijst voor automatisch gegenereerde id&#39;s, krijgt de eerste alinea van het onderwerp of document een id zoals p\_1, de volgende alinea krijgt p\_2 enzovoort. In een ander document wordt het genereren van de id echter opnieuw gestart. Dit betekent dat id&#39;s zoals p\_1 en p\_2 in een ander document kunnen worden toegewezen aan alinea-elementen.

   Als uw document al id&#39;s bevat in het opgegeven patroon, worden deze id&#39;s door het proces voor automatisch genereren niet aan nieuwe elementen toegewezen.

1. Klik **sparen**.


**Bovenliggend onderwerp:**&#x200B;[ pas de Redacteur van het Web ](conf-web-editor.md) aan
