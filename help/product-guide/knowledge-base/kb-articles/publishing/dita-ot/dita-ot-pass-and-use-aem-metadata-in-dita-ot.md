---
title: AEM Assets-metagegevens doorgeven aan door DITA-OT-plug-in gegenereerde uitvoer
description: DITA-OT-plug-in en inhoud in AEM configureren om metagegevens naar gegenereerde uitvoer te verzenden
source-git-commit: b48f5a342989d3be48bbc1e8af51a2ce477d0ac7
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 0%

---


# AEM Assets-metagegevens doorgeven aan door DITA-OT-plug-in gegenereerde uitvoer

In dit artikel zullen wij verklaren hoe te om veranderingen in stop uit te voeren DITA-OT om metadata.xml _(beschikbaar in tijdelijke dossiers)_ te lezen en de eigenschappen te gebruiken, die door AEM Guides worden overgegaan publicerend werkschema, in stoppen DITA-OT en het te plaatsen in de geproduceerde output.

Hieronder vindt u een overzicht van de stappen die u in dit artikel zult leren:
- Metagegevens instellen voor de uitvoervoorinstelling van een ditamap in AEM Guides
- Bij het genereren van uitvoer krijgt u toegang tot dit metadata.xml in de map DITA-OT temp
- Implementatie in de stop DITA-OT om dit _metadata.xml_ te lezen en de beschikbare eigenschappen in de geproduceerde output te gebruiken
- De gegenereerde uitvoer controleren om de doorgegeven metagegevens weer te geven

## Achtergrond

Met AEM Guides kunt u DITA-OT-plug-ins gebruiken om naar de gewenste uitvoerindelingen te publiceren met behulp van de geconfigureerde plug-ins, en
u kunt meta-gegevens van de activa ook overgaan die in AEM DAM aan het DITA-OT proces worden beheerd om het in de geproduceerde output te gebruiken - zie de documentatie op [&#x200B; hoe te opstelling ditamap/onderwerpen om meta-gegevens door output vooraf ingesteld &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-guides/using/user-guide/output-gen/pass-metadata-dita-ot) over te gaan


## Veronderstellingen

U hebt een AEM met AEM Guides-versie 4.4.0/2024.6 of hoger
U hebt vroegere kennis van hoe DITA-OT werkt en zijn folderstructuur


## Uitgelegde stappen

### Metagegevens instellen voor het element

Met het AEM Assets-metagegevensschema kunt u in AEM aangepaste eigenschapvelden voor de Assets maken en kunnen gebruikers metagegevens aan de elementen toewijzen. Het nemen van een voorbeeld van a _onderwerp_ activa waar een meta-gegevens genoemd _aangepaste prop_ voor een voorbeeld kan worden geplaatst - verwijs hieronder screenshot:

![&#x200B; vastgestelde eigenschappen in meta-gegevensredacteur voor een activa &#x200B;](../../assets/publishing/assets-metadata-properties-ui-customprop.png)


### De metagegevens voor de uitvoervoorinstelling van ditamap configureren om door te geven aan DITA-OT

Een uitvoervoorinstelling naar keuze op de kaart configureren om metagegevens te exporteren en door te geven aan DITA-OT
Laten wij zeggen wij HTML5 output gebruikend een stop DITA-OT zeggen _adobe.html_ produceren.
Zie onderstaande schermafbeelding voor informatie over het configureren van de uitvoervoorinstelling voor een kaart om metagegevens door te geven aan de DITA-OT-plug-in.
1. Open een kaart en doorblader aan het _lusje van de Output_ voor deze kaart en open HTML5 vooraf ingesteld, en klik _Geavanceerd_ lusje, op deze reeks de naam van de Transformatie als _adobe.html_ (dit is de stop die wij zullen vormen en voor ons voorbeeld gebruiken, kunt u uw douanestop eveneens bepalen)
2. De reeks _behoudt tijdelijke dossiers_ om de tijdelijke dossiers te kunnen downloaden en te controleren hoe metadata.xml wordt gevormd, kunt u dit voor ontwikkeling gebruiken
3. Selecteer de eigenschappen van metagegevens die u via metadata.xml wilt doorgeven aan DITA-OT. In dit voorbeeld laat zeggen wij _dc willen overgaan:titel_ en _customprop_
4. De voorinstelling opslaan en de uitvoer genereren
5. Het tijdelijke bestand downloaden met de knop die in de voorinstelling wordt weergegeven

Raadpleeg de onderstaande screenshot voor meer informatie over de bovenstaande stappen:
![&#x200B; vorm output vooraf ingesteld voor een kaart om meta-gegevens over te gaan &#x200B;](../../assets/publishing/map-outputpreset-html5-customprop.png)


### De DITA-OT-plug-in implementeren

#### De map metadata.xml openen in de tijdelijke map

In het gedownloade tijdelijke bestandspakket zult u een metadata.xml-bestand zien waarin de structuur van de eigenschappen en waarden wordt weergegeven (zie onderstaande schermafbeelding)
![&#x200B; metadata.xml structuur en bouwt &#x200B;](../../assets/publishing/publish-tempfiles-metadata-structure.png)

##### Metagegevens begrijpen.xml

- Dit bestand bevat een lijst met alle elementen die worden gepubliceerd, met elk de volgende kenmerken:
   - weg van het dossier in DITA folder [ identiteitskaart attributen van het element van de Weg ]
   - en lijst van de waardeparen van het meta-gegevensbezit [ onder _meta-gegevens_ element ]

```
        <Path id="topics\about-this-document.dita">
            <sourceProps>
                ...
            </sourceProps>
            <metadata>
                <meta isArray="false" key="dc:title">About This Document</meta>
                <meta isArray="false" key="customprop">customval</meta>
            </metadata>
        </Path>
```

#### De metagegevens openen voor elk element in de DITA-OT-plug-in

Voor de insteekmodule DITA-OT om _metadata.xml_ en eigenschappen te lezen beschikbaar in het moeten wij het volgende doen:
- Bepaal de montages van de douanestop in _plugins.xml_, waar de params en de integrator voor plugininleiding bepalen, zal ons dossier van de steekproefstop hieronder kijken:

```
<?xml version="1.0" encoding="UTF-8"?>
<plugin id="com.adobe.html">
    <require plugin="org.dita.html5"/>
    <feature extension="dita.conductor.transtype.check" value="adobe.html"/>
    <feature extension="ant.import" file="integrator.xml"/>
    <feature extension="dita.conductor.html5.param" file="params.xml"/>
    <feature extension="package.version" value="2024.1"/>
</plugin>
```

- Bij opstarten van de insteekmodule:
   - plaats een variabele om aan het metadata.xml- dossier te richten i.e. in _integrator.xml_ onder de stop reeks een bezit om de weg van het meta-gegevensdossier te bepalen, en
   - bepaal het dossier dat de transformatieregels van douane xsl in werking stelt, d.w.z. _args.xsl_, die in ons geval aan het dossier _xsl/adobe-html5.xsl_ zal richten.
Verwijs hieronder code:

```
    <property name="adobe.html.xsl.dir" value="${dita.plugin.com.adobe.html.dir}${file.separator}xsl${file.separator}"/>
    <property name="args.xsl" location="${adobe.html.xsl.dir}adobe-html5.xsl" />
    <dirname property="input.dirname" file="${args.input}"/>
    <makeurl file="${input.dirname}/metadata.xml" property="metadata.url"/>
```

- Ga de waarde van veranderlijke _metadata.url_ tot douaneXSL over om het te gebruiken aangezien u nodig hebt, d.w.z. in bestaand/gecreeerd _param.xml_ gaat de parameter tot de stop over, zie onder een steekproef params.xml- dossier:

```
    <?xml version="1.0" encoding="UTF-8"?>
    <params xmlns:if="ant:if">
        <param name="metadata.url" expression="${metadata.url}" if:set="metadata.url"/>
    </params>
```

- In het de transformatiedossier van douaneXSL _xsl/adobe-html5.xsl_ kunt u de meta-gegevenswaarden van het meta-gegevensdossier lezen en het plaatsen in de output de manier u wilt. In dit voorbeeld voegen we de metagegevenswaarden toe aan de html head > meta-tags. Verwijs hieronder code:

```
<xsl:import href="plugin:org.dita.html5:xsl/dita2html5.xsl"/>
    <xsl:param name="metadata.url"/>
    <xsl:template name="copyright">
        <xsl:if test="doc-available( $metadata.url )">
            <xsl:variable name="docName" select="tokenize( base-uri(), '/' )[ last() ]"/>
            <xsl:variable name="doc" select="doc( $metadata.url )"/>
            <xsl:for-each select="$doc//Path[ ends-with( @id, concat( '\', $docName ) ) ]/metadata/meta">
                <meta name="{ @key }" content="{ . }"/>
            </xsl:for-each>
        </xsl:if>
    </xsl:template>
```

Zie de onderstaande schermafbeelding en de bovenstaande stappen.
![&#x200B; stappen om dia-aan stop &#x200B;](../../assets/publishing/publishing-metadata-dita-ot-plugin-implementation.png) uit te voeren


### De insteekmoduleimplementatie testen

U kunt de insteekmodule testen door de volgende opdracht uit te voeren om de insteekmodule te testen met de tijdelijke bestanden die zijn gedownload van AEM (met kaartinhoud en de bijbehorende metadata.xml)

```
./dita --input=docsrc/samples/HTML5/aem_forms_documentation.ditamap --format=adobe.html
```

Ervan uitgaande dat u de gedownloade tijdelijke bestanden hebt gekopieerd onder de map &quot;DITA-OT/docsrc/samples/HTML5&quot;.
U kunt ook het voorbeeld downloaden dat in de onderstaande sectie Bronnen wordt gegeven.

Wanneer het bovengenoemde bevel wordt uitgevoerd kunt u de output in de folder &quot;DITA-OT/bin/out&quot;controleren, waar u de HTML- dossiers kunt controleren die voor het onderwerp &quot;over-dit-document.dita&quot;worden geproduceerd die de douanemetagegevens in het _hoofd_ element zullen hebben

```
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <meta charset="UTF-8">
    <meta name="copyright" content="(C) Copyright 2024">
    <meta name="DC.format" content="HTML5">
    <meta name="DC.identifier" content="GUID-f193ea85-989d-4d80-99e2-2f5dea3d5310">
    <meta name="DC.language" content="en-US">
    <meta name="dc:title" content="About This Document">
    <meta name="customprop" content="customval">
    <title>About This Document</title>
</head>
```

### Implementatie

Zodra u de stop DITA-OT hebt ontwikkeld, kunt u dit in DITA-OT integreren gebruikend _dita - installeer_ bevel onder de folder DITA-OT, en het opstellen aan de AEM server [&#x200B; verwijs dit artikel voor meer details &#x200B;](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/steps-to-setup-a-custom-dita-ot/td-p/407659)


## Bronnen

1. De tijdelijke dossiers van de steekproef die van steekproefditamap worden gedownload - [&#x200B; downloaden gebruikend deze verbinding &#x200B;](../../assets/publishing/sample-temp-html5-adobe.html-content.zip)
2. DITA-OT stop met hierboven verklaarde implementatie [&#x200B; download gebruikend deze verbinding &#x200B;](../../assets/publishing/sample-custom-plugin-com.adobe.html.zip)