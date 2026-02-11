---
title: Niet-DITA-inhoud migreren
description: Leer hoe u niet-DITA-inhoud kunt migreren
exl-id: cf437fb8-ed33-47af-aa7e-ffd8acd232da
feature: Migration
role: Admin
level: Experienced
source-git-commit: 2c20191ba998ad7da98587f1832e1fe8499d023c
workflow-type: tm+mt
source-wordcount: '2521'
ht-degree: 0%

---

# Niet-DITA-inhoud migreren {#id181AH0R02HT}

Deze sectie begeleidt u door het migratieproces om niet-DITA documenten in formaat te migreren DITA. AEM Guides biedt migratie uit de volgende bronnen:

- [Microsoft Word](#id1949B040Z5Z)

- [InDesign-documenten](#id195AD0B0K5Z)

- [XHTML](#id1949B04L0Y4)

- [Niet-gestructureerde FrameMaker-documenten](#id1949B050VUI)

- [Alle andere gestructureerde documenten](#id1949B0590YK)


## Microsoft Word-documenten migreren {#id1949B040Z5Z}

AEM Guides staat u toe om uw bestaande documenten van Word \ (`.docx` \) in DITA onderwerptypedocumenten te migreren. U moet de locatie van de invoer- en uitvoermap en andere parameters opgeven en het document wordt geconverteerd naar DITA-document. Afhankelijk van de inhoud, zou u een.dita dossier en een.ditamap- dossier kunnen hebben.

Als u een Word-document wilt converteren, moet het document een goede structuur hebben. Uw document moet bijvoorbeeld een titel hebben, gevolgd door Kop 1, Kop 2 enzovoort. Elk van de rubrieken zou wat inhoud in het moeten hebben. Als uw document niet goed gestructureerd is, werkt het proces mogelijk niet naar behoren.

Door gebrek, gebruikt AEM Guides [&#x200B; Word-aan-DITA \ (Word2DITA \) transformatiekader &#x200B;](http://www.dita4publishers.org/docs/repo/org.dita4publishers.word2dita/word2dita/word2dita-intro.html). Deze transformatie hangt van het [&#x200B; stijl-aan-markering van afbeelding &#x200B;](http://www.dita4publishers.org/docs/repo/org.dita4publishers.word2dita/word2dita/style-to-tag-map-overview.html) configuratiedossier af. Als u de Word2DITA-transformatie met succes wilt kunnen gebruiken, moet u de volgende richtlijnen in overweging nemen voor het voorbereiden van uw Word-document voor conversie:

>[!NOTE]
>
> Als u wijzigingen aanbrengt in het standaardconfiguratiebestand voor de toewijzing van stijl naar label, moet u de richtlijnen bijwerken en gebruiken die bevestigen bij uw bijgewerkte stijltoewijzing.

- Zorg ervoor dat het document begint met een titel. Deze titel wordt toegewezen aan de titel van de DITA-kaart. Daarnaast moet de titel worden gevolgd door gewone inhoud.

- Na de titel moet er rubriek 1, rubriek 2 enzovoort zijn. Elke kop moet inhoud bevatten. De rubrieken worden omgezet in nieuwe Concept typeonderwerpen. De hiërarchie van de gegenereerde onderwerpen is afhankelijk van de niveaus van Kop in het document. Kop 1 komt bijvoorbeeld voor Kop 2 en Kop 2 komt voor Inhoud Kop 3.

- Het document moet ten minste één koptekstinhoud hebben.

- Zorg ervoor dat u geen gegroepeerde afbeeldingen hebt. Als u afbeeldingen in uw document hebt gegroepeerd, degroepeert u deze allemaal.

- Alle kop- en voetteksten verwijderen.

- Inline stijlen zoals vet, cursief en onderstrepen worden omgezet in `b` -, `i` - en `u` -elementen.

- Alle geordende en ongeordende lijsten worden geconverteerd naar `ol` - en `ul` -elementen. Dit geldt ook voor geneste lijsten, lijsten binnen tabellen, notities of voetnoten.

- Alle hyperlinks worden geconverteerd naar `xref` .

- De bestandsnaam van de omgezette bestanden is gebaseerd op de koptekst gevolgd door een bestandsnummer. Het bestandsnummer is een opeenvolgend nummer op basis van de positie van de koptekst in het document. Als een koptekst bijvoorbeeld &#39;Voorbeeldkop&#39; is en de tekst een tiende kop in het document heeft, is de resulterende bestandsnaam voor dit onderwerp vergelijkbaar met Sample\_Heading\_10.dita.


Voer de volgende stappen uit om uw bestaande documenten van Word in DITA onderwerptype document om te zetten:

1. Gebruik Pakketbeheer om het bestand /libs/fmdita/config/w2d\_io.xml te downloaden.

1. Pas het gedownloade bestand w2d\_io.xml aan.

1. Voeg het bestand toe op de volgende locatie in de Cloud Manager Git-opslagplaats:

   /apps/fmdita/config/w2d\_io.xml

   Het bestand `w2d_io.xml` bevat de volgende configureerbare parameters:

   - Geef in het element `inputDir` de locatie op van de invoermap waarin uw Word-brondocumenten beschikbaar zijn. Als uw Word-documenten bijvoorbeeld zijn opgeslagen in een map met de naam `wordtodita` in de map `projects` , geeft u de locatie op als: `/content/dam/projects/wordtodita/`

   - In het `outputDir` element, specificeer de plaats van de outputomslag of houd de standaardoutputplaats om het omgezette DITA- document te bewaren. Als de opgegeven uitvoermap niet bestaat op DAM, maakt de conversieworkflow de uitvoermap.

   - Voor het `createRev` element, specificeer of een nieuwe versie van het omgezette onderwerp DITA \ (`true` \) of niet \ (`false` \) moet worden gecreeerd.

   - Geef in het element `s2tMap` de locatie op van het kaartbestand dat toewijzingen voor Word-documentstijlen aan DITA-elementen bevat. De standaardtoewijzing wordt opgeslagen in het bestand dat zich bevindt op:

     ```
     /libs/fmdita/word2dita/word-builtin-styles-style2tagmap.xml
     ```

     >[!NOTE]
     >
     > Voor meer informatie over de structuur van `word-builtin-styles-style2tagmap.xml` dossier en hoe u het kunt aanpassen, zie [&#x200B; Stijl aan Tagtoewijzing &#x200B;](http://www.dita4publishers.org/docs/repo/org.dita4publishers.word2dita/word2dita/style-to-tag-map-overview.html) in *DITA voor de Gids van de Gebruiker van Uitgevers*.

   - In het element props2Propagate, specificeer de eigenschappen die tot de kaart moeten worden overgegaan DITA. Dit bezit wordt vereist om de standaardmeta-gegevens zoals dc :title, dc :subject, dam :keywords over te gaan, dam :category van documentmeta-gegevens aan omgezette activa DITA.

1. Stel de pijpleiding van Cloud Manager in werking om de bijgewerkte configuratie op te stellen.

1. Nadat u de vereiste parameters in het `w2d_io.xml` -bestand hebt geconfigureerd, meldt u zich aan bij AEM en opent u de gebruikersinterface van Assets.

1. Navigeer naar de locatie van de invoermap \(`wordtodita`\).

1. Upload de Word-brondocumenten naar deze map. Voor informatie bij het uploaden van inhoud op DAM, zie [&#x200B; Bestaande inhoud uploaden DITA &#x200B;](migrate-content-upload-existing-dita-content.md#).


Met behulp van het blok `config` `/config` kunt u een of meer configuraties definiëren voor conversie. De omzettingswerkstroom wordt uitgevoerd en de definitieve output in de vorm van een onderwerp DITA wordt bewaard in de plaats die in het `outputDir` element wordt gespecificeerd.

**updates van de Aanpassing voor bestaande gebruikers**

Als u een bestaande gebruiker voor AEM Guides as a Cloud Service bent en vanaf de release van augustus 2021 een upgrade uitvoert naar de versies januari 2022 of hoger, moet u de opgegeven eigenschappen bijwerken omdat er maar weinig bestanden zijn verplaatst.

>[!NOTE]
>
> Deze update is alleen van toepassing als u de conversieworkflow Microsoft Word naar DITA al gebruikt.

- Bestandspad: /apps/fmdita/config/w2d\_io.xml
- Wijzig de waarde voor `<s2tMap>` in /libs/fmdita/word2dita/word-builtin-styles-style2tagmap.xml
- Breng de noodzakelijke wijzigingen aan in uw Cloud Manager Git-opslagplaats, net zoals voor cloudservice, worden alle bestanden in /apps overschreven via Cloud Manager Git.

## Adobe InDesign-documenten migreren {#id195AD0B0K5Z}

Met AEM Guides kunt u InDesign-documenten converteren. Net als in FrameMaker kunt u met InDesign ook ongestructureerde en gestructureerde documenten maken. De ongestructureerde documenten gebruiken de alinea- en tekenstijlen om inhoud op te maken. In het gestructureerde document worden elementen en de bijbehorende kenmerken gebruikt.

Voor het conversieproces moeten de opmaak van de alinea- en tekenstijl worden toegewezen aan relevante DITA-elementen. Op dezelfde manier bevat het toewijzingsbestand in het geval van gestructureerde documenten een-op-een-toewijzing van InDesign-elementen en -kenmerken met DITA-elementen en -kenmerken.

Het conversieproces omvat de volgende acties op de achtergrond:

- Het *dossier van de Taal van de Prijsverhoging van InDesign* \ (IDML \) is uitgepakt aan een werkende folder.
- Het bestand designmap.xml wordt gelezen om de afzonderlijke InDesign-artikelen te zoeken.
- Alle artikelen worden samengevoegd tot één XML-instantie, &#39;lege&#39; artikelen worden genegeerd.
- Alle ingesloten afbeeldingen worden geëxporteerd.
- Pre-conversie van standaardstructuren zoals tabellen en afbeeldingen naar DITA-indeling.
- Stijl- of structuurtoewijzing aan de uiteindelijke uitvoer op basis van het toewijzingsbestand.
- Creatie en bevestiging van individuele onderwerpen DITA en DITA kaartdossiers.
- Verwijderen van tijdelijke bestanden.

Breedweg, vereist het omzettingsproces u om [&#x200B; InDesign dossiers voor omzetting &#x200B;](appendix.md#id195DBF0045Z) [&#x200B; appendix.md voor te bereiden \ #id195DBF0045Z &#x200B;](appendix.md#id195DBF0045Z) en [&#x200B; het kaartdossier voor InDesign aan migratie DITA &#x200B;](appendix.md#id194AF0003HT) [&#x200B; appendix.md \ #id194AF003HT &#x200B;](appendix.md#id194AF0003HT), dan hebt u nodig de voorgeschreven procedure voor het uitvoeren van het conversieproces te volgen.

Voer de volgende stappen uit om uw bestaande InDesign-documenten om te zetten in DITA-onderwerpdocument:

1. Meld u aan bij AEM en open de CRXDE Lite-modus.

1. Navigeer naar het standaardconfiguratiebestand dat beschikbaar is op de volgende locatie:

   `/libs/fmdita/config/idml2dita_io.xml`
1. Als u een aangepaste configuratie wilt maken die voldoet aan uw vereisten, maakt u een overlayknooppunt van de map `config` in het knooppunt `apps` .

1. Kopieer de volgende bestanden of mappen vanuit de map `libs` naar de map Apps:

   - `/fmdita/config/idml2dita_io.xml`
   - `/fmdita/idml2dita/config`
   - `/fmdita/idml2dita/xsl`

1. Navigeer naar het configuratiebestand dat beschikbaar is in het knooppunt `apps` :

   `/apps/fmdita/config/idml2dita_io.xml`

1. Voeg de toewijzing van de configuraties toe die aanwezig zijn in de map `idml12dita` in het `idml2dita_io.xml` -bestand.
1. Voeg de volgende eigenschappen toe aan het bestand `idml2dita_io.xml` :

   ```
   <entry          key="idml2DitaConfig">/apps/fmdita/idml2dita/config</entry>
   
   <entry key="idml2DitaXsl">/apps/fmdita/idml2dita/xsl</entry>
   ```

1. Maak een overlayknooppunt van de map `config` in het knooppunt `apps` .


   Configureer de volgende parameters in het `idml2dita_io.xml` -bestand:

   - Geef in het element `inputDir` de locatie op van de invoermap waarin uw InDesign-brondocumenten beschikbaar zijn. Als uw InDesign-documenten bijvoorbeeld zijn opgeslagen in een map met de naam `indesigntodita` in de map `projects` , geeft u de locatie op als: `/content/dam/idmlfiles/indesigntodita/`

   - In het `outputDir` element, specificeer de plaats van de outputomslag of houd de standaardoutputplaats om het omgezette DITA- document te bewaren. Als de opgegeven uitvoermap niet bestaat op DAM, maakt de conversieworkflow de uitvoermap.

   - Geef in het element `mapStyle` de locatie op van het toewijzingsbestand dat toewijzingen voor InDesign-documentstijlen aan DITA-elementen bevat. De standaardtoewijzing wordt opgeslagen in het bestand dat zich bevindt op:

     ```
     /stmap.adobeidml.xml
     ```

     >[!NOTE]
     >
     > Voor meer informatie over de structuur van `stmap.adobeidml.xml` dossier en hoe u het kunt aanpassen, zie de sectie [&#x200B; appendix.md \#id194AF003HT &#x200B;](appendix.md#id194AF0003HT) in Bijlage.

1. Sla het `idml2dita_io.xml` -bestand op.

1. Nadat u de vereiste parameters in het `idml2dita_io.xml` -bestand hebt geconfigureerd, meldt u zich aan bij AEM en opent u de gebruikersinterface van Assets.

1. Navigeer naar de locatie van de invoermap \(`indesigntodita`\).

1. Upload de InDesign-brondocumenten naar deze map. Voor informatie bij het uploaden van inhoud op DAM, zie [&#x200B; Bestaande inhoud uploaden DITA &#x200B;](migrate-content-upload-existing-dita-content.md#).


## XHTML-documenten migreren {#id1949B04L0Y4}

Met AEM Guides kunt u uw bestaande XHTML-documenten converteren naar DITA-onderwerpdocumenten. U moet de locatie van de invoer- en uitvoermap en andere parameters opgeven en de documenten worden geconverteerd naar DITA-indeling. U kunt uw gestructureerde HTML-documenten op twee manieren converteren:

- Alle documenten uploaden naar de invoermap, of
- Maak een ZIP van alle documenten samen met de mediabestanden en upload deze naar de invoermap. Deze aanpak wordt over het algemeen gebruikt voor een set HTML-bestanden die aan elkaar zijn gekoppeld en er is een inhoudsopgave \(index.html\). Het bestand index.html bevat koppelingen naar alle HTML-bestanden in de set.

Of u nu alle bestanden afzonderlijk uploadt of in een ZIP-bestand gebundeld, het conversieproces zorgt voor een een-op-een-toewijzing tussen de HTML-bestanden en de resulterende DITA-bestanden. Dit betekent in wezen dat er een .dita dossier voor elk .html dossier in de inputomslag wordt gecreeerd.

Voor het uploaden van uw documenten in een ZIP-bestand moet u rekening houden met de volgende punten:

- Alle onderwerpen waarnaar wordt verwezen, moeten in het ZIP-bestand worden geplaatst.

- Alle mediabestanden waarnaar wordt verwezen, moeten worden doorverwezen in de onderwerpbestanden met behulp van de relatieve koppeling.

- Maak een bestand index.html en voeg koppelingen toe naar de onderwerpen die u wilt toevoegen aan de inhoudsopgave. Dit bestand index.html wordt gebruikt om het DITA-kaartbestand te maken. In het bestand index.html kunt u ook geneste onderwerpen maken die worden vermeld in het volgende codevoorbeeld:

  ```
  <?xml version="1.0" encoding="UTF-8"?>
  <html
  xmlns="http://www.w3.org/1999/xhtml">
      <head>
          <title>Sample Index File</title>
      </head>
      <body>
          <h1>Sample Index</h1>
          <div class="content">
              <ul class="book">
                  <li class="topicref">
                      <a href="Topic1.html">Topic 1</a>
                      <ul class="book">
                          <li class="topicref">
                              <a href="Topic1-1.html">Topic 1.1</a>
                          </li>
                          <li class="topicref">
                              <a href="Topic1-2.html">Topic 1.2</a>
                          </li>
                      </ul>
                  </li>
                  <li class="topicref">
                      <a href="Topic2.html">Topic 2</a>
                  </li>
              </ul>
          </div>
      </body>
  </html>
  ```

  Voor elke `ul` -tag moet het `class` -kenmerk zijn ingesteld op `book` . Op dezelfde manier moet elke `li` tag `class` worden ingesteld op `topicref` .

- Als u inline stijlen gebruikt, zet u de inline stijlen om in op CSS gebaseerde stijlklassen in uw XHTML-bestand. Gebruik vervolgens stijlkenmerktoewijzing om deze op klassen gebaseerde stijlen te converteren naar het attribuut DITA `outputclass` in het geconverteerde DITA-bestand.

  Tijdens het genereren van HTML- of AEM-site-uitvoer uit deze DITA-bestanden, kunnen de `outputclass` -kenmerken worden gebruikt om stijlklasse toe te passen op gegenereerde HTML- of AEM-site, zodat deze overeenkomt met uw HTML-broninhoud.


Naast de overwegingen voor het maken van het ZIP-bestand moet uw XHTML-document ook goed gestructureerd zijn. Bijvoorbeeld, zou uw document a *Titel* moeten hebben, die door *Kop 1* wordt gevolgd, *Kop 2*, etc. Elk van de rubrieken zou wat inhoud in het moeten hebben. Als uw document niet goed gestructureerd is, werkt het migratieproces mogelijk niet naar behoren.

Voer de volgende stappen uit om uw bestaande XHTML-document om te zetten in DITA-onderwerp:

1. Gebruik Pakketbeheer om het bestand /libs/fmdita/config/h2d\_io.xml te downloaden.

1. Pas het gedownloade bestand h2d\_io.xml aan.

1. Voeg het bestand toe op de volgende locatie in de Cloud Manager Git-opslagplaats:

   /apps/fmdita/config/h2d\_io.xml

   Het bestand `h2d_io.xml` bevat de volgende configureerbare parameters:

   - Geef in het element `inputDir` de locatie op van de invoermap waarin uw bron-XHTML-documenten beschikbaar zijn. Als uw XHTML-documenten bijvoorbeeld zijn opgeslagen in een map met de naam `xhtmltodita` in de `projects` -map, geeft u de locatie op als: `/content/dam/projects/xhtmltodita/`

   - In het `outputDir` element, specificeer de plaats van uw outputomslag of houd de standaardoutputplaats. Als de opgegeven uitvoermap niet bestaat op DAM, maakt de conversieworkflow de uitvoermap.

   - Voor het `createRev` element, specificeer of een nieuwe versie van het omgezette onderwerp DITA \ (`true` \) of niet \ (`false` \) moet worden gecreeerd.

1. Stel de pijpleiding van Cloud Manager in werking om de bijgewerkte configuratie op te stellen.

1. Nadat u de vereiste parameters in het `w2d_io.xml` -bestand hebt geconfigureerd, meldt u zich aan bij AEM en opent u de gebruikersinterface van Assets.

1. *\(Optioneel\)* U kunt de verwante sectie van verbindingen aan de omgezette documenten ook toevoegen. Voer de volgende stappen uit om deze functie in te schakelen:

   >[!NOTE]
   >
   > Standaard wordt de sectie Verwante koppelingen niet gemaakt in de omgezette documenten.

   1. Gebruik Package Manager om het bestand /libs/fmdita/html2dita/h2d.xsl te downloaden.

   2. Zoek naar de volgende parameter:

      `<xsl:param name="generate-related-links" select="false()"/>`

   3. Stel de waarde van de bovenstaande parameter in op `true()` .

   4. Leg het bijgewerkte bestand vast op de volgende locatie in de Cloud Manager Git-opslagplaats:

      /libs/fmdita/html2dita/

   5. Stel de pijpleiding van Cloud Manager in werking om de bijgewerkte configuratie op te stellen.

1. Navigeer naar de locatie van de invoermap \(`xhtmltodita`\).

1. Upload de bron-XHTML-documenten naar deze map. Voor informatie bij het uploaden van inhoud op DAM, zie [&#x200B; Bestaande inhoud uploaden DITA &#x200B;](migrate-content-upload-existing-dita-content.md#).


Met behulp van het blok `<config> </config>` kunt u een of meer configuraties definiëren voor conversie. De omzettingswerkstroom wordt uitgevoerd en de definitieve output in de vorm van een onderwerp DITA wordt bewaard in de plaats die in het `outputDir` element wordt gespecificeerd.

## Niet-gestructureerde FrameMaker-documenten migreren {#id1949B050VUI}

Als u ongestructureerde Adobe FrameMaker-inhoud (.fm en .book) wilt converteren naar gestructureerde DITA, kunt u het tabelmechanisme voor FrameMaker-conversie gebruiken. Het proces richt zich op het evalueren van bestaande inhoud, het gebruiken van een op malplaatje-gebaseerde benadering, en het in kaart brengen van de stijlen van FrameMaker aan DITA door omzettingslijsten. Voor meer details, mening [&#x200B; migrerend technische documentatie van ongestructureerd aan DITA in Adobe FrameMaker &#x200B;](https://migrate-from-unstructured-to-dita-step-by-step-guide.meetus.adobeevents.com/).

Na de conversie kan de gestructureerde inhoud naar AEM Guides worden gemigreerd.  Voor meer details, uploadt de mening [&#x200B; bestaande inhoud DITA &#x200B;](./migrate-content-upload-existing-dita-content.md).

<!-- Deprecated information -
 //The first step is to create style mappings using FrameMaker and save those settings in a .sts file. Next, if you are using custom DITA, then you can map your custom elements with the source FrameMaker formats in the `ditaElems.xml` file. For example, if you have created a custom element named `impnote` to handle all important notes, then you can define this custom element in the `ditaElems.xml` file. Once this custom element is defined, AEM Guides would not raise an error while converting FrameMaker document containing `impnote` element.

Also, If you want to specify some additional attributes with your custom or valid DITA element, you can define those in the style2attrMap.xml file. For example, you can specify the `type` attribute with the value of `important` to be passed on with the `impnote` element. This additional information can be specified in the style2attrMap.xml file.

In addition to specifying

To convert your existing unstructured FrameMaker documents into DITA format, perform the following steps:

1.  Create style mappings in FrameMaker and save those settings in a .sts file.

1.  Log into AEM and open the CRXDE Lite mode.

1.  If you have custom DITA elements, define those in the `ditaElems.xml` file available at the following location:

    `/libs/fmdita/config/ditaElems.xml`

1.  Create an overlay node of the `config` folder within the `apps` node.

1.  Navigate to the configuration file available in the `apps` node:

    `/apps/fmdita/config/ditaElems.xml`

    The `ditaElems.xml` file contains a single configurable parameter:

    -   In the `elem` parameter, specify the name of the custom element that you want to use in your converted DITA documents. This element would be passed on as is in the generated DITA documents.

1.  If you want to specify additional attributes, define those in the `style2attrMap.xml` file available at the following location:

    `/libs/fmdita/config/style2attrMap.xml`

1.  Create an overlay node of the `config` folder within the `apps` node.

1.  Navigate to the configuration file available in the `apps` node:

    `/apps/fmdita/config/style2attrMap.xml`

    The `style2attrMap.xml` file contains the following configurable parameters:

    -   In the `fmStyle` parameter, specify the source format used in the FrameMaker document that you want to map.

    -   In the`ditaAttr` element, specify the DITA attribute that you want to map with the source format.

    -   In the `ditaVal` element, specify the value for the mapped attribute. If you don't have any value, you can leave this entry blank.

1.  Save the `style2attrMap.xml` file.

1. After configuring the required parameters in the `style2attrMap.xml` file, log into AEM and open the Assets UI.

1. Navigate to and click on the FrameMaker document that you want to convert.

    The DITA map console appears showing the list of Output Presets available to generate output.

1. Select DITA output format and configure the required parameters.

    >[!NOTE]
    >
    > You must use the same settings file \(.sts\) that you created in FrameMaker. Also, specify the Settings Name and Destination Path.

1. Click the **Generate** icon to start the output generation process.


Using the `<attrMap> </attrMap>` block, you can define one or multiple blocks of configurations for conversion. Depending on the content, you could have a .dita file and a .ditamap file as the converted files.

-->

## Andere gestructureerde documenten migreren {#id1949B0590YK}

Met AEM Guides kunt u uw bestaande gestructureerde documenten converteren naar geldige DITA-documenten. U moet de locatie van de invoer- en uitvoermap, de locatie van het transformatiebestand, de extensie opgeven waarmee de uiteindelijke uitvoer wordt opgeslagen en of een nieuwe versie van het document is vereist of niet.

Voer de volgende stappen uit om uw bestaande gestructureerde documenten om te zetten in DITA-indeling:

1. Gebruik Package Manager om het bestand /libs/fmdita/config/XSLConfig.xml te downloaden.

1. Maak een kopie van het bestand XSLConfig.xml op de volgende locatie in de Cloud Manager Git-opslagplaats:

   `/apps/fmdita/config/XSLConfig.xml`

   Het bestand `XSLConfig.xml` bevat de volgende configureerbare parameters:

   - Geef in het element `inputDir` de locatie op van de invoermap waarin de gestructureerde brondocumenten beschikbaar zijn. Als uw gestructureerde documenten bijvoorbeeld zijn opgeslagen in een map met de naam `xsltodita` in de map `projects` , geeft u de locatie op als: `/content/dam/projects/xsltodita/`

   - In het `outputDir` element, specificeer de plaats van uw outputomslag of houd de standaardoutputplaats. Als de opgegeven uitvoermap niet bestaat op DAM, maakt de conversieworkflow de uitvoermap.

   - Geef in het element `xslFolder` de locatie op van de map waarin de XSL-transformatiebestanden zijn opgeslagen.

   - Geef in het element ``xslPath`` de locatie op van het primaire XSL-bestand waarmee het conversieproces wordt gestart.

   - Geef in het element ``outputExt`` de bestandsextensies op van het uiteindelijke uitvoerbestand dat met de transformatiestream is gemaakt.

   - Voor het `createRev` element, specificeer of een nieuwe versie van het omgezette onderwerp DITA \ (`true` \) of niet \ (`false` \) moet worden gecreeerd.

1. Sla het `XSLConfig.xml` -bestand op.

1. Nadat u de vereiste parameters in het `XSLConfig.xml` -bestand hebt geconfigureerd, meldt u zich aan bij AEM en opent u de gebruikersinterface van Assets.

1. Navigeer naar de locatie van de invoermap \(`xsltodita`\).

1. Upload de gestructureerde brondocumenten naar deze map. Voor informatie bij het uploaden van inhoud op DAM, zie [&#x200B; Bestaande inhoud uploaden DITA &#x200B;](migrate-content-upload-existing-dita-content.md#).


Met behulp van het blok `<config> </config>` kunt u een of meer configuraties definiëren voor conversie. De omzettingswerkstroom wordt uitgevoerd en de definitieve output in de vorm van een onderwerp DITA wordt bewaard in de plaats die in het `outputDir` element wordt gespecificeerd.

**Bovenliggend onderwerp:**&#x200B;[&#x200B; Migreer bestaande inhoud &#x200B;](migrate-content.md)
