---
title: Systeemeigen PDF-publicatiefunctie | Streepjescode toevoegen
description: Leer hoe u streepjescodes kunt toevoegen.
exl-id: 206bdcf9-2bcd-4bf1-815a-c97cdf0dc415
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# Een streepjescode toevoegen aan de PDF-uitvoer

Een streepjescode is een gegevenspatroon dat machines kunnen lezen. Klanten kunnen streepjescodes scannen met een streepjescodescanner of hun smartphonecamera. Coderingsgegevens zoals productdetails, inventarisnummers of URL&#39;s van websites kunnen nuttig zijn. Door streepjescodes toe te voegen, kunt u de gegevens gemakkelijk vastleggen, de klantervaring verbeteren en gegevensbeheer en -beveiliging verbeteren.

U kunt een stijl voor de streepjescode maken. en gebruiken om een streepjescode in te voegen in een paginalay-out. U kunt de stijl toepassen op een voorbeeldstreepjescode in de gewenste paginalay-out.


Deze zelfstudie helpt u streepjescodes toe te voegen in de PDF-uitvoer.

## Stappen voor het genereren van een streepjescode

Voer de volgende stappen uit om een streepjescode te genereren:

### De CSS van de sjabloon bijwerken om een streepjescodewaarde te renderen

Wijzig het `layout.css` -bestand om een streepjescode te renderen tijdens het genereren van PDF. Verschillende typen streepjescodes, zoals &#39;qrcode&#39; en &#39;pdf417&#39;, worden ondersteund.  Voor meer details, mening [ de types van Streepjescode ](#barcode-types).



```css
...
.barcode { 
-ro-replacedelement: barcode;   
-ro-barcode-type: code128;   
-ro-barcode-size: 100%;   
-ro-barcode-content: content();   
object-fit: contain;   
margin-top: 2mm;
 
}
...
```

### De CSS-stijl gebruiken om de streepjescode te genereren

U kunt de streepjescode op verschillende manieren genereren. Enkele voorbeelden zijn als volgt:

**Voorbeeld 1**

Voeg een tijdelijke aanduiding voor streepjescodes toe aan de sjabloonkoptekst en pas de stijl toe:

1. Bewerk **Malplaatjes** > **Lay-outs van de Pagina**
1. Selecteer een pagina-indeling. U kunt bijvoorbeeld de pagina-indeling BackCover selecteren, die de kop- of voettekst bevat.
1. Voeg het volgende bereik toe aan de locatie waar u de streepjescode wilt invoegen.

   `<span class="barcode">Sample barcode</span></p>`.

   >[!NOTE]
   >
   > Gebruik dezelfde klassenaam die u in de `layout.css` hebt gedefinieerd.

1. Vervang `<Sample barcode>` door de waarde die u wilt dat de streepjescodescanner wordt gelezen.

U kunt de streepjescode bekijken bij het genereren van de uitvoer van PDF met behulp van de sjabloon, die de paginalay-out bevat. Nadat u de vorige stappen hebt uitgevoerd, kunt u de PDF-uitvoer genereren met een streepjescode.

In de volgende schermafbeelding wordt een voorbeeldstreepjescode weergegeven in een PDF-uitvoer.

<img src="./assets/barcode-output-sample.png" alt="Voorbeeld van uitvoer met streepjescode" width="700" border="2px">

**Voorbeeld 2**

Wijzig het `Common.plt` dossier in het **Basis** malplaatje om een streepjescode na de projecttitel toe te voegen.

Als u een streepjescode voor een ISBN-nummer wilt maken, voegt u een ISBN-nummer toe. Gebruik vervolgens het ISBN-nummer om de streepjescode te genereren.

```html
...

  <div data-region="header">
    <p class="chapter-header"><span data-field="project-title" data-format="default">Project Title</span> </p>
    <p><span class="barcode">978-1-56619-909-4</span></p>
  </div>
} 
...
```

**Voorbeeld 3**

Een streepjescode maken met de metagegevens van de kaart:

Gebruik metagegevens die zich in het element `<topicmeta>` van een DITA-kaart bevinden, om weer te geven als streepjescode. Zorg ervoor dat u het juiste XPath gebruikt. U kunt bijvoorbeeld een `<resourceid>` toevoegen in de `<topicmeta>` van een DITA-kaart.

In het volgende voorbeeld dient de bron-id als de belangrijkste invoer voor het genereren van de streepjescode.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "technicalContent/dtd/map.dtd">
<map id="GUID-3c330691-4dac-4020-904a-d2d6246aeeb1-en">
  <title>Barcode Sample</title>
  <topicmeta>
    <resourceid id="7a5bda1c-b1db-4fd8-8763-a731e2e8abba">
    </resourceid>
  </topicmeta>
  <topicref href="GUID-139f6c64-bea3-4f17-8b22-ee131557e249-en.dita" type="topic">
  </topicref>
</map>  
```



U kunt de bron-id als volgt gebruiken in een paginalay-out:


```html
  <div data-region="header">
    <p class="chapter-header"><span data-field="project-title" data-format="default">Project Title</span> </p>
    <p><span class="barcode" data-field="metadata" data-format="default" data-subtype="//resourceid/@id">Resource ID (barcode)</span></p>
  </div>
} 
```

## Typen streepjescodes {#barcode-types}

Enkele veelgebruikte streepjescodes zijn als volgt:

| Type | -ro-streepjescode-type | Aanvullende gegevens |
| ---| --- | --- |
| QR-code | qrcode | De QR Code bar code symbolen volgens ISO/IEC 18004 :2015. |
| Code 128 | code128 | De Code 128-streepjescodesymbologie zoals gedefinieerd in ISO/IEC 15417 :2007. |
| Code 32 | code32 | Code 32, ook bekend als Italiaans geneesmiddel. |
| Code 49 | code49 | Code 49 volgens ANSI/AIM-BC6-2000. |
| Code 11 | code11 |                            |
| Code 93 | code93 |                            |
| Code16k | code16k |                            |
| PDF417 | pdf417 | De PDF417/MicroPDF417-streepjescodeconflicten volgens ISO/IEC 15438 :2006 en ISO/IEC 24728 :2006. |
| Code 3 of 9 | code39 | De code 3 van 9 bar codecymbologie volgens ISO/IEC 16388 :2007. |
| MSI Plessey | msiplessey |                            |
| Kanaalcode | kanaalcode | Kanaalcode volgens ANSI/AIM BC12-1998. |
| Codabar | codabar | Codabar barcode symbology according to BS EN 798 :1996. |
| EAN-8 | ean-8 | EAN-streepjescodecymbologie volgens BS EN 797 :1996. |
| EAN-13 | ean-13 | EAN-streepjescodecymbologie volgens BS EN 797 :1996. |
| UPC-A | upc-a | UPC bar code symbology according to BS EN 797 :1996. |
| UPC-E | upc-e | UPC bar code symbology according to BS EN 797 :1996. |
| Ean/UPC Addon | ademen | EAN/UPC toe:voegen-op de symbolen van de bar volgens BS EN 797 :1996. |
| Telepen | telpen | Ook bekend als Telepen Alpha. |
| GS1-databar / Databar 14 | gegevensbank | GS1 DataBar volgens ISO/IEC 24724 :2011. |
| GS1 Databar Expanded / Databar 14 Expanded | uitgevouwen database | GS1 Gegevensbalk Uitgebreid volgens ISO/IEC 24724 :2011. |
| GS1 Databar Limited | beperkt tot databases | GS1 DataBar Limited volgens ISO/IEC 24724 :2011. |
| POSTNET (techniek voor numerieke codering van postzendingen) | postnet | De POSTNET-streepjescodesymbologie (Postal Numeric Encoding Technique) die door de United States Postal Service wordt gebruikt. |
| Pharmazentralnummer (PZN-8) | pzn8 | Een op code 39 gebaseerde symbolen die door de farmaceutische industrie in Duitsland worden gebruikt. |
| Farmacode | farmacode |                            |
| Codablock F | codablockf | Symbology according to AIM Europe &quot;Uniform Symbology Specification Codablock F&quot;, 1995. |
| Logmars | logmars | De norm LOGMARS (Logistics Applications of Automated Marking and Reading Symbols) die door het Amerikaanse Ministerie van Defensie wordt gebruikt. |
| Aztec Runes | aztec-runes | Aztec kent codeconflicten volgens ISO/IEC 24778 :2008 bijlage A. |
| Aztec-code | aztec code | Codebalkcode van de Aztec volgens ISO/IEC 24778 :2008. |
| DataMatrix | data-matrix | Gegevensmatrix ECC 200 bar code symbology Conform ISO/IEC 16022 :2006. |
| Code One | code-on |                            |
