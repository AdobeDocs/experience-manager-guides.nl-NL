---
title: Geef de metagegevens door aan de uitvoer met DITA-OT
description: Leer hoe u de metagegevens aan de uitvoer kunt doorgeven met DITA-OT-publicaties in AEM Guides.
exl-id: 70ca32dc-56c3-45ee-b6b9-0efb8cc79ea1
feature: Publishing, Metadata Management
role: User
source-git-commit: e1d6123991ddd8d25f76ee03befeb95f020a9834
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Geef de metagegevens door aan de uitvoer met DITA-OT {#id21BJ00QD0XA}

Metagegevens zijn aanvullende informatie over de uitvoer. In Adobe Experience Manager Guides kunt u de bestaande metagegevens doorgeven of aangepaste metagegevenstags maken. U kunt metagegevens doorgeven aan AEM-, PDF-, HTML5-, EPUB- en Aangepast-uitvoerbestanden met DITA-OT-publicatie.

Er zijn twee manieren om de meta-gegevens tot Output over te gaan gebruikend DITA-OT:

- [Kaartconsole gebruiken](#using-map-console)
- [Het dashboard Kaart gebruiken](#using-map-dashboard)

## Kaartconsole gebruiken

Voer de volgende stappen uit om de metagegevens door te geven aan de uitvoer met DITA-OT-publicatie:

1. [ open het DITA kaartdossier in kaartconsole ](./open-files-map-console.md) waarvoor u de meta-gegevens tot DITA-OT wilt overgaan.
1. Selecteer en open een uitvoervoorinstelling waaraan u de metagegevensvelden wilt doorgeven. Selecteer bijvoorbeeld de uitvoervoorinstelling PDF. Zorg ervoor dat het gebruikend **wordt gecreeerd DITA-OT** optie.
1. Van de **eigenschappen van het Dossier** dropdown selecteren de meta-gegevens die u tot DITA-OT het publiceren wilt overgaan.

   ![](images/custom-metadata-output-preset-new.png){width="800" align="left"}

   In het vervolgkeuzemenu Eigenschappen worden zowel de aangepaste als de standaardeigenschappen weergegeven. In de bovenstaande schermafbeelding `dc:description` zijn `dc:language` , `dc:title` en `docstate` bijvoorbeeld de standaardeigenschappen.

   >[!NOTE]
   >
   > Deze eigenschappen worden gekozen uit het metadataList dossier beschikbaar bij de volgende plaats:`/libs/fmdita/config/metadataList`. Standaard worden in dit bestand vier eigenschappen vermeld: `dc:description` , `dc:language` , `dc:title` en `docstate` .

   Dit bestand kan worden bedekt door: `/apps/fmdita/config/metadataList` .

   Om een douanebezit over te gaan waarvoor u reeds de waarden hebt bepaald, bekijk {de Metagegevens van AEM van het 0} Gebruik in output van DITA-OT PDF ](https://experienceleaguecommunities.adobe.com/t5/xml-documentation-discussions/use-aem-metadata-in-dita-ot-pdf-output/td-p/411880).[

1. De geselecteerde eigenschappen worden onder het vervolgkeuzemenu weergegeven.

   ![](images/metadata-added-dropdown.png){width="300" align="left"}

1. Selecteer **sparen** op het hoogste recht om de veranderingen te bewaren.
1. Selecteer **produceren output**.

De geselecteerde eigenschappen van metagegevens worden doorgegeven aan de uitvoer die wordt gegenereerd met DITA-OT.

>[!NOTE]
>
> Vanaf de release van 2502 van Experience Manager Guides is de functionaliteit voor het doorgeven van metagegevensargumenten voor hoofdmappen via de opdrachtregel DITA-OT afgekeurd. Om onderbrekingen te voorkomen, is echter een nieuwe eigenschap toegevoegd aan de `Config.Manager` om de functionaliteit in of uit te schakelen.  Voor meer details, vormt de mening [ montages van de outputgeneratie ](../cs-install-guide/conf-output-generation.md#configure-the-dita-ot-command-line-arguement-field-on-the-dita-map-dashboard).

## Het dashboard Kaart gebruiken

Als het werken op **Assets UI**, voer de volgende stappen uit om de meta-gegevens tot de output over te gaan gebruikend DITA-OT het publiceren:

1. In **Assets UI**, navigeer aan en kies het DITA kaartdossier waarvoor u de meta-gegevens tot DITA-OT wilt overgaan.
1. Selecteer en bewerk een uitvoervoorinstelling waaraan u de metagegevensvelden wilt doorgeven. Selecteer bijvoorbeeld de uitvoervoorinstelling PDF.
1. Selecteer **DITA-OT** optie in geselecteerde output vooraf ingesteld.

   ![](images/custom-meta-data-output-preset.png){width="800" align="left"}

1. Selecteer in het keuzemenu Eigenschappen de metagegevens die u wilt doorgeven aan DITA-OT-publicaties.

   In het vervolgkeuzemenu Eigenschappen worden zowel de aangepaste als de standaardeigenschappen weergegeven. In de bovenstaande schermafbeelding is de auteur bijvoorbeeld de aangepaste eigenschap, terwijl `dc:description` , `dc:language` , `dc:title` en `docstate` de standaardeigenschappen zijn.

   >[!NOTE]
   >
   > Deze eigenschappen worden gekozen uit het metadataList dossier beschikbaar bij de volgende plaats:`/libs/fmdita/config/metadataList`. Standaard worden in dit bestand vier eigenschappen vermeld: `dc:description` , `dc:language` , `dc:title` en `docstate` .

   Dit bestand kan worden bedekt door: `/apps/fmdita/config/metadataList` .

   Om een douanebezit over te gaan waarvoor u reeds de waarden hebt bepaald, bekijk {de Metagegevens van AEM van het 0} Gebruik in output van DITA-OT PDF ](https://experienceleaguecommunities.adobe.com/t5/xml-documentation-discussions/use-aem-metadata-in-dita-ot-pdf-output/td-p/411880).[

1. Van **Eigenschappen** dropdown, selecteer de vereiste douane en standaardeigenschappen. Selecteer bijvoorbeeld `author` , `dc:title` en `dc:description` . Dit is de standaard `metadata/properties` die wordt gemaakt wanneer we een bestand maken. De geselecteerde eigenschappen worden onder de dropbox weergegeven.

   ![](images/selected-metadata-properties.png){width="300" align="left"}

1. Selecteer **Gedaan** op de bovenkant verlaten om de veranderingen te bewaren.
1. Genereer de uitvoer.

De geselecteerde eigenschappen van metagegevens worden doorgegeven aan de uitvoer die wordt gegenereerd met DITA-OT.



**Bovenliggend onderwerp:**[ Productie van de Output ](generate-output.md)
