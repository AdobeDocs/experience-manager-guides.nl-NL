---
title: Geef de metagegevens door aan de uitvoer met DITA-OT
description: Leer hoe u de metagegevens aan de uitvoer kunt doorgeven met DITA-OT-publicaties in AEM Guides.
feature: Publishing, Metadata Management
role: User
hide: true
exl-id: 55d70c6d-feb0-43f7-9f18-6d1ccdd1e728
source-git-commit: ea597cd14469f21e197c700542b9be7c373aef14
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Geef de metagegevens door aan de uitvoer met DITA-OT {#id21BJ00QD0XA}

Metagegevens zijn aanvullende informatie over de uitvoer. In AEM Guides kunt u de bestaande metagegevens doorgeven of aangepaste metagegevenstags maken. U kunt metagegevens doorgeven aan AEM-, PDF-, HTML5-, EPUB- en Aangepast-uitvoerbestanden met DITA-OT-publicatie.

Voer de volgende stappen uit om de metagegevens door te geven aan de uitvoer met DITA-OT-publicatie:

1. In **Assets UI**, navigeer aan en klik op het DITA kaartdossier waarvoor u de meta-gegevens tot DITA-OT wilt overgaan.
1. Selecteer en bewerk een uitvoervoorinstelling waaraan u de metagegevensvelden wilt doorgeven. Selecteer bijvoorbeeld de uitvoervoorinstelling PDF.
1. Selecteer **DITA-OT** onder Generate &lt;output\> Gebruikend optie in geselecteerde output vooraf ingesteld.

   ![](images/custom-meta-data-output-preset.png){width="800" align="left"}

1. Selecteer in het keuzemenu Eigenschappen de metagegevens die u wilt doorgeven aan DITA-OT-publicaties.

   In het vervolgkeuzemenu Eigenschappen worden zowel de aangepaste als de standaardeigenschappen weergegeven. In de bovenstaande schermafbeelding is de auteur bijvoorbeeld de aangepaste eigenschap, terwijl `dc:description` , `dc:language` , `dc:title` en `docstate` de standaardeigenschappen zijn.

   >[!NOTE]
   >
   > Deze eigenschappen worden gekozen uit het metadataList dossier beschikbaar bij de volgende plaats:`/libs/fmdita/config/metadataList`. Standaard worden in dit bestand vier eigenschappen vermeld: `dc:description` , `dc:language` , `dc:title` en `docstate` .

   Dit bestand kan worden bedekt door: `/apps/fmdita/config/metadataList` .

   Om een douanebezit over te gaan waarvoor u reeds de waarden hebt bepaald, zie [&#x200B; Meta-gegevens van AEM van het Gebruik in output DITA-OT PDF &#x200B;](https://experienceleaguecommunities.adobe.com/t5/xml-documentation-discussions/use-aem-metadata-in-dita-ot-pdf-output/td-p/411880?profile.language=nl).

1. Van **Eigenschappen** dropdown, selecteer de vereiste douane en standaardeigenschappen. Selecteer bijvoorbeeld `author` , `dc:title` en `dc:description` . Dit is de standaard `metadata/properties` die wordt gemaakt wanneer we een bestand maken. De geselecteerde eigenschappen worden onder de dropbox weergegeven.

   ![](images/selected-metadata-properties.png){width="300" align="left"}

1. Klik **Gedaan** op de bovenkant verlaten om de veranderingen te bewaren.
1. Genereer de uitvoer.

De geselecteerde eigenschappen van metagegevens worden doorgegeven aan de uitvoer die wordt gegenereerd met DITA-OT.

**Bovenliggend onderwerp:**&#x200B;[&#x200B; Productie van de Output &#x200B;](generate-output.md)
