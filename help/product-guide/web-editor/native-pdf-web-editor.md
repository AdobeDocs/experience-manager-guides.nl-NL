---
title: Native PDF | PDF-uitvoergeneratie
description: Leer hoe u het publiceren van eigen PDF kunt gebruiken, een voorinstelling voor PDF-uitvoer kunt maken en genereren, tijdelijke bestanden kunt downloaden nadat u de eigen PDF-uitvoer hebt gegenereerd en taalvariabelen in AEM Guides kunt gebruiken.
exl-id: ec3d59b7-1dda-4fd1-848e-21d8a36ff5e4
feature: Publishing, Web Editor, Native PDF Output
role: User
source-git-commit: e78749b1d5b4ba944cbca69ba65c6d28355b2c34
workflow-type: tm+mt
source-wordcount: '3362'
ht-degree: 0%

---

# Publish PDF uitvoer

Met AEM Guides kunt u PDF van afzonderlijke onderwerpen of een volledig kaartbestand genereren. U kunt de inhoud publiceren in een PDF-indeling met een van de volgende drie methoden:

* **DITA-OT**

Gebruik deze methode om een uitvoer van PDF voor een kaart van het kaartdashboard te produceren. U kunt publicatie-eigenschappen instellen voordat u de PDF genereert door een uitvoervoorinstelling te maken voor de kaart die is geopend in het kaartdashboard. Om tot stand te brengen of uit te geven vooraf ingesteld output, *Begrijpend de output stelt* sectie in de [ as a Cloud Service Gids van de Gebruiker van AEM Guides ](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/cs-apr-22/XML-Documentation-for-Adobe-Experience-Manager_CS_User-Guide_EN.pdf) vooraf in.

Voor meer informatie bij het produceren van een PDF gebruikend de methode DITA-OT, zie [ PDF gebruikend DITA-OT ](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-pdf.html) produceren.

* **FrameMaker Publishing Server (FMPS)**

Met deze methode kunt u een PDF-uitvoer genereren op basis van niet alleen de DITA-inhoud, maar ook FrameMaker-documenten (.book en .fm) die beschikbaar zijn in uw AEM opslagplaats. De PDF kan worden gemaakt door een uitvoervoorinstelling te configureren en te publiceren met behulp van FrameMaker Publishing Server (FMPS). U kunt het uiterlijk van uw uitvoer voor PDF en andere indelingen ontwerpen en configureren en deze opslaan in een instellingsbestand (.sts). Dit instellingsbestand wordt vervolgens door FMPS gebruikt om uitvoer te genereren voor een DITA-kaart of .book-bestand. Om tot stand te brengen of uit te geven vooraf ingesteld output, zie *Begrijpend de output vooraf instelt* sectie in de [ as a Cloud Service Gids van de Gebruiker van AEM Guides ](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/cs-apr-22/XML-Documentation-for-Adobe-Experience-Manager_CS_User-Guide_EN.pdf).

Voor meer informatie bij het vormen FMPS, zie [ output van de documenten van de FrameMaker ](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Ffm-output-generatation.html) produceren.

* **Eigen PDF het publiceren**

Gebruik deze methode om een PDF-uitvoer met veel functies te genereren op basis van W3C CSS3- en CSS-paginanormen. Met de publicatie Native PDF kunt u sjablonen gebruiken om de lay-out en opmaak voor uw inhoud in te stellen en verschillende instellingen toepassen om uw PDF te verfijnen. Daarnaast kunt u uw eigen sjablonen wijzigen en maken met de sjablooneditor.

Voor meer informatie bij het inheemse publiceren van PDF, zie [ Gebruikend het Inheemse publiceren van PDF ](#native-pdf-publishing).


## De publicatie Native PDF gebruiken {#native-pdf-publishing}

Bij het ontwerpen van inhoud wordt het van essentieel belang dat de inhoud is geoptimaliseerd voor weergave, bewerking en afdrukken. Met standaarden zoals W3C CSS3 voor inhoudsopmaak en CSS-normen voor gepagineerde media voor eigenschappen van paginadefinities, zoals grootte, marges, afdrukstand, pagina-einden, kop- en voetteksten en paginanummering, kunt u de weergave en lay-out voor uw PDF-document instellen, zodat deze consistent en bruikbaar zijn. De publicatiefunctie Native PDF gebruikt deze standaarden om een PDF te genereren.

Met de native publicatie van PDF kunt u vooraf gedefinieerde sjablonen gebruiken om consistentie in de indeling en structuur van de inhoud te garanderen, stijlpagina&#39;s toepassen om de vormgeving van de uitvoer te wijzigen, PDF te optimaliseren, drukkermarkeringen in te stellen, ondersteuning voor schermlezers mogelijk te maken, PDF-conformiteit in te stellen, lettertypen in te sluiten en nog veel meer.

Het genereren van een PDF met behulp van Native PDF-publicaties heeft twee aspecten:

* Gebruik sjablonen om opmaak toe te passen op inhoud, paginalay-outs en verschillende instellingen in te stellen om de PDF te perfectioneren. Auteurs kunnen de voorbeeldsjablonen gebruiken of wijzigen of aangepaste sjablonen maken en geavanceerde configuratieopties instellen die door uitgevers en ontwikkelaars worden gebruikt.

* Maak of configureer een voorinstelling voor PDF-uitvoer om de PDF-instellingen te bepalen. Nadat u een voorinstelling voor PDF-uitvoer hebt gemaakt, kunt u de PDF genereren.

Voor meer informatie, zie [ een output van PDF ](#generate-pdf-output) produceren.

## Een voorinstelling voor PDF-uitvoer maken {#create-output-preset}

De eerste stap bij het genereren van een PDF-uitvoer bestaat uit het maken van een voorinstelling voor PDF-uitvoer. Dit is een verzameling publicatie-eigenschappen die aan een kaart zijn toegewezen. U kunt een uitvoervoorinstelling maken voor elke kaart die is geopend in het deelvenster Kaartweergave, of een bestaande voorinstelling configureren om snel een PDF voor dezelfde kaart te genereren.

Vanuit de voorinstelling voor PDF-uitvoer kunt u een sjabloon selecteren, voorwaarden toepassen, beperkingen instellen om te bepalen hoe een gebruiker met de PDF werkt, geavanceerde instellingen configureren, zoals compressie, conformiteit en meer.

Een voorinstelling voor PDF-uitvoer maken of configureren:

1. In het lusje van de Output, klikt **vooraf instelt** in linkerzijbalk.
Het deelvenster Voorinstelling wordt geopend. <br>
<img src="assets/preset-panel.png" alt="deelvenster met voorinstellingen" width="600">

1. In de output **stelt** paneel vooraf in, doe één van het volgende:
   * Dubbelklik op een vooraf gedefinieerde PDF-uitvoervoorinstelling om deze weer te geven.
   * Klik + pictogram tegen **vooraf instelt** om een nieuwe outputvoorinstelling van **Type toe te voegen: PDF**

1. Instellingen configureren van een bestaande PDF-voorinstelling:
   * Klik het **pictogram van Opties** ![ opties ](assets/options.svg) naast de gewenste output vooraf instelt en selecteert **uitgeeft**.
U kunt de volgende montages in de **Algemene** gebruiken, **Meta-gegevens**, **Lay-out**, **Veiligheid**, en **Geavanceerde** lusjes om een PDF vooraf ingestelde output te vormen:

**Algemeen**

Gebruik deze optie om basisuitvoerinstellingen op te geven, zoals een uitvoerpad, een bestandsnaam voor PDF en meer.

| Instelling | Beschrijving |
| --- | --- |
| **Pad van de Output** | Het pad binnen de AEM opslagplaats waar de PDF-uitvoer wordt opgeslagen. Zorg ervoor dat het uitvoerpad zich niet in de projectmap bevindt. Als deze optie leeg wordt gelaten, wordt de uitvoer gegenereerd op de standaarduitvoerlocatie voor de DITA-kaart.<br> u kunt de volgende uit-van-doos variabelen ook gebruiken om de Weg van de Output te bepalen. U kunt een enkele of een combinatie van variabelen gebruiken om deze optie te definiëren. <br> `${map_filename}`: gebruikt de naam van de DITA-kaartbestanden om het doelpad te maken. <br> `${map_title}`: gebruikt de DITA-maptitel om het doelpad te maken. <br>`${preset_name}`: gebruikt de naam van de uitvoervoorinstelling om het doelpad te maken. <br> `${language_code}`: gebruikt de taalcode waar het kaartbestand zich bevindt om het doelpad te maken. <br> `${map_parentpath}`: gebruikt het volledige pad van het kaartbestand om het doelpad te maken.  <br>`${path_after_langfolder}`: gebruikt het pad van het kaartbestand na de taalmap om het doelpad te maken. |
| **Dossier van PDF** | Geef een bestandsnaam op om de PDF op te slaan. Standaard wordt in de bestandsnaam PDF de naam van de DITA-kaart en de naam van de voorinstelling toegevoegd. ditamap is bijvoorbeeld &#39;TestMap&#39; en de naam van de voorinstelling is &#39;preset1&#39;. De standaardnaam van de pdf is &#39;TestMap_preset1.pdf&#39;. <br> u kunt de volgende uit-van-doos variabelen ook gebruiken om het Dossier van de PDF te bepalen. U kunt een enkele of een combinatie van variabelen gebruiken om deze optie te definiëren. <br>`${map_filename}`<br>`${map_title}`<br>`${preset_name}` <br> `${language_code}`. |
| **pas Voorwaarden toe gebruikend** | Kies voor geconditioneerde inhoud een van de onderstaande opties om op basis van deze voorwaarden een PDF-uitvoer te genereren: <br><ul> <li> **Geen Toegepaste** Selecteer deze optie als u geen voorwaarde op de kaart en broninhoud wilt toepassen. <br><li> **Ditaval Dossier** Selecteer een DITAVAL dossier om geconditionaliseerde inhoud te produceren. Klik op Voorinstelling voorwaarde om dit te selecteren en zoek het bestand. <br> <li> **Vooraf ingestelde Voorwaarde van de Voorwaarde** Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. Deze optie is zichtbaar als u een voorwaarde voor het DITA kaartdossier hebt toegevoegd. De voorwaardelijke instellingen zijn beschikbaar op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Meer over voorwaarde vooraf ingesteld, zie [ Voorinstellingen van het Gebruik ](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-use-condition-presets.html). <br> </ul> |
| **Basislijn van het Gebruik** | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren. Zie [ Werk met Basislijn ](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-use-baseline-for-publishing.html) voor meer details. |
| **creeer PDF met de Bar van de Verandering tussen Gepubliceerde Versies** | Gebruik de volgende opties om een PDF te maken die de verschillen in inhoud tussen twee versies weergeeft met wijzigingsbalken:   <br><ul><li> **Basislijn van de Vorige Versie** kiest de basislijnversie die u met de huidige versie of een andere basislijn wilt vergelijken. Er wordt een wijzigingsbalk weergegeven in de PDF om de gewijzigde inhoud aan te geven. Een wijzigingsbalk is een verticale lijn die nieuwe of herziene inhoud visueel identificeert. De wijzigingsbalk verschijnt links van de inhoud die is ingevoegd, gewijzigd of verwijderd. <br> **Nota**: Als u **Basislijn van het Gebruik** selecteert en een basislijn kiest om te publiceren, zal de vergelijking tussen de twee geselecteerde basislijnversies worden gedaan. Bijvoorbeeld, als u basislijnversie 1.3 onder **Basislijn van het Gebruik** kiest, en Versie 1.1 onder **Basislijn van de Vorige Versie**, zal de vergelijking tussen basislijnversie 1.1 en basislijnversie 1.3 worden gedaan. <br><li> **toon Toegevoegde Tekst** Uitgezocht om de opgenomen tekst in groene kleur en onderstreept te tonen. Deze optie is standaard ingeschakeld. <br> <li> **toon Geschrapte Tekst** Uitgezocht om de geschrapte tekst in rode kleur en duidelijk met een doorhaling te tonen. Deze optie is standaard ingeschakeld. <br>**Nota** U kunt het stileren van de veranderingsbar, opgenomen inhoud, of geschrapte inhoud ook aanpassen gebruikend stylesheet.<br></ul> |
| **het Werkschema van de Generatie van Post** | Selecteer deze optie om een vervolgkeuzelijst weer te geven met alle workflows die in AEM zijn geconfigureerd. U kunt de workflow selecteren die u wilt uitvoeren nadat de workflow voor het genereren van PDF is voltooid. |

**Metagegevens**

Metagegevens zijn de beschrijving of definitie van de inhoud. Metagegevens helpen bij inhoudsbeheer en helpen bij het zoeken naar bestanden op internet.

Gebruik het tabblad Metagegevens om de metagegevensvelden in te stellen, zoals de naam van de auteur, de documenttitel, trefwoorden, copyrightinformatie en andere gegevensvelden voor de uitvoer van de PDF. U kunt ook aangepaste metagegevens toevoegen voor uw PDF-uitvoer.

Deze meta-gegevens wordt in kaart gebracht aan de meta-gegevens in het **1} lusje van de Beschrijving {binnen de** Eigenschappen van het Document **van uw output PDF.**



<img src="assets/pdf-metadata.png" alt="tabblad Metagegevens" width="600">

Van de Output stelt vooraf in, selecteert de uitgezochte **PDF** > **Native-PDF** > **Meta-gegevens** om meta-gegevensopties toe te voegen en aan te passen.
* **Metagegevens van het Gebruik die in topicmeta** worden toegevoegd

  Deze optie is standaard ingeschakeld. U kunt de meta-gegevens gebruiken die u in het topicmeta element van de kaart DITA hebt toegevoegd om de meta-gegevensgebieden van de output van de PDF te bevolken.

* **verstrekken XMP dossier**

  U kunt de meta-gegevensgebieden ook direct bevolken door [ XMP ](https://www.adobe.com/products/xmp.html) (het Verlengbare Platform van Meta-gegevens) dossier in te voeren. U kunt hier een voorbeeld XMP bestand downloaden.

[Downloaden](assets/SampleXMP.xmp)

  U kunt ook een XMP bestand genereren met Adobe Acrobat.
   1. Klik **Dossier** > **Eigenschappen** in Acrobat.
   1. Onder **Beschrijving**, klik **Extra Meta-gegevens**.
   1. Van het linkerpaneel, uitgezochte **Geavanceerd**.
   1. Klik op **sparen**.

  XMP bestand wordt opgeslagen op het apparaat.

* **verstrekt meta-gegevensnamen en waarden**

   1. Voeg naam toe door uit de drop-down te selecteren of een douanemetagegevens toe door direct op het naamgebied te typen.
   1. Voer de waarde voor de metagegevens in en klik op het pictogram &#39;+&#39;.
De metagegevens worden toegevoegd aan de lijst met metagegevens voor de PDF.

U kunt ook variabelen gebruiken om de waarden van metagegevens te definiëren.  U kunt de metagegevens die voor de DITA-kaart of het bladwijzerbestand zijn gedefinieerd, als variabelen gebruiken. De metagegevens vindt u onder het knooppunt `/jcr:content/metadata` van de DITA-kaart of het bladwijzerbestand.
Wanneer u een variabele gebruikt, wordt de waarde ervan gekozen uit de eigenschappen van metagegevens.

Als u een variabele wilt gebruiken, moet u deze definiëren in de `${<variable>}` -indeling.

Een van de metagegevenseigenschappen die bijvoorbeeld in het knooppunt /`jcr:content/metadata` zijn gedefinieerd, is
`dc:title` . U kunt `${dc:title}` specificeren, en de titelwaarde wordt gebruikt in de definitieve output.

U kunt een enkele of een combinatie van variabelen gebruiken om de metagegevens te definiëren. Bijvoorbeeld `${dc:title} ${dc:docstate}` . U kunt ook de combinatie van een variabele en een tekenreeks gebruiken.  Bijvoorbeeld `View ${dc:title} in ${dc:language}` .

Taalvariabelen gebruiken om de gelokaliseerde waarde van eigenschappen van metagegevens te definiëren. Afhankelijk van de gekozen taal wordt de gelokaliseerde waarde automatisch gekozen in de uitvoer van de PDF. U kunt bijvoorbeeld &quot;Auteur&quot; afdrukken als de metagegevenswaarde in het Engels en &quot;Autorin&quot; in het Duits.

Indeling: `${lng:<variable name>}`. `${lng:author-label}` waarbij `author-label` bijvoorbeeld een taalvariabele is.

Overslaan <img src="./assets/info-details.svg" alt= "info icon" width="25"> in de buurt van de optie voor meer informatie over de optie.


**Lay-out**

Hiermee kunt u paginalay-outs instellen en paginaweergaveopties opgeven voor PDF-uitvoer, zoals Paginaweergave en Zoomniveaus instellen.

| Instelling | Beschrijving |
| --- | --- |
| **Malplaatje van PDF** | PDF-sjablonen bieden een duidelijke structuur voor het definiëren van paginalay-outs, het opmaken van inhoud en het toepassen van verschillende instellingen op de PDF-uitvoer. Selecteer een sjabloon in de vervolgkeuzelijst PDF-sjabloon om uw voorkeursjabloon te kiezen. <br> u kunt **ook selecteren doorbladert Malplaatje** <img src="./assets/browse-templates-icon.svg"  alt= "bladersjablonen, pictogram" width="25"> om een sjabloon te kiezen. In het **Uitgezochte PDF malplaatje** dialoog kunt u de duimnagel ook voorproef en de titel en de beschrijving voor het geselecteerde malplaatje bekijken. |
| **Vertoning van de Pagina** | Gebruik de paginaweergave voor de paginaweergave waarin wordt getoond hoe de PDF wordt weergegeven wanneer deze wordt geopend. Selecteer een optie in het keuzemenu Paginaweergave om een voorkeursweergave te kiezen. <br><ul><li> **Gebrek** Vertoningen zoals per het gebrek dat van de kijker van de PDF op de machine van een gebruiker plaatst.  <br> <li> **Enige Mening van de Pagina** toont één pagina tegelijkertijd.   <br> <li> **Enige Pagina die** scrolt toont één enkele pagina in een ononderbroken verticale kolom.  <br> <li> **Twee Mening van de Pagina** toont twee-pagina uitgespreid zij aan zij tegelijkertijd. .<br> <li> **Twee het Schuiven van de Pagina** toont twee-pagina uitgespreid zij aan zij met ononderbroken het scrollen. </ul> |
| **Gezoem** | Selecteer deze optie om het formaat te wijzigen van de paginaweergave waarin wordt getoond hoe de PDF wordt weergegeven wanneer deze wordt geopend.  <br><ul><li> **Gebrek** vertoningen zoals per het gebrek dat van de kijker van de PDF op de machine van een gebruiker plaatst    <br> <li> **100%** maakt de pagina in zijn daadwerkelijke grootte verschijnen.     <br> <li> **Passend Pagina** maakt de paginabreedte en de hoogte om binnen de documentruit te passen.   .<br> <li> **Passend de Breedte van de Pagina** maakt de breedte van de pagina de breedte van de documentruit vullen.  <br> <li> **de Hoogte van de Pagina van de Passende** maakt de hoogte van de pagina de hoogte van de documentruit vullen. </ul> |

**Veiligheid**

Protect uw PDF door beperkingen toe te voegen om het bestand te openen en te lezen. Gebruik de onderstaande opties om ongeoorloofde toegang te voorkomen.

| Instelling | Beschrijving |
| --- | --- |
| **plaats wachtwoord om het document** te openen | Selecteer deze optie om een beveiligd wachtwoord toe te voegen om uw PDF-bestand weer te geven. Specificeer een wachtwoord op het **gebied van het wachtwoord van de Gebruiker 0}.** Gebruikers kunnen de PDF alleen openen door het wachtwoord in te voeren dat in dit veld is opgegeven. |
| **plaats de documentbeperkingen** | Selecteer deze optie om de interactie tussen gebruikers en uw PDF te beperken. Specificeer een wachtwoord op het **gebied van het Wachtwoord van de Eigenaar 0} {voor de hieronder beperkingsmontages te werken.  <br>**<ul><li> **het Druk** Uitgezocht om een gebruiker toe te staan om de PDF te drukken. <br> <li> **Uitgezocht van de kwaliteit van het 0} Ontwerp {om een gebruiker toe te staan om de PDF in een lagere resolutie te drukken.  <br>** <li> **Inhoud het kopiëren** Uitgezocht om een gebruiker toe te staan om inhoud van de PDF te kopiëren.   <br> <li> **Annotaties** Uitgezocht om een gebruiker toe te staan om een nota of een commentaar in de PDF toe te voegen. <br> <li> **de wijzigingen van de Inhoud** Uitgezocht om een gebruiker toe te staan om de inhoud in de PDF te veranderen. <br> <li> **Inhoud het kopiëren voor toegankelijkheid** Uitgezocht om het schermlezers toe te staan om inhoud in PDF te lezen en te navigeren. <br>  **de assemblage van het Document** Uitgezocht om gebruikers toe te staan om pagina&#39;s in de PDF op te nemen. <br> **Nota**: De gebruikers moeten het eigenaarwachtwoord ingaan om het even welke beperkingen van het Dossier te veranderen > Eigenschappen in Adobe Acrobat. |

**Geavanceerd**

Gebruik de volgende opties om geavanceerde instellingen op te geven voor het samenvoegen van PDF, compressie gebruiken, compatibiliteitsnorm selecteren en meer.

| Instelling | Beschrijving |
| --- | --- |
| **creeer toegankelijke (geëtiketteerde) PDF** | Selecteer deze optie als u een PDF met tags wilt genereren. Met een gecodeerde PDF kunnen schermlezers gemakkelijker inhoud, hyperlinks, bladwijzers enzovoort lezen en door de inhoud navigeren. Als een tabel bijvoorbeeld is gecodeerd, weet de schermlezer dat deze de tabel leest en niet alleen regels en tekst. |
| **de PDF van de Fusie inbegrepen in TOC** | Selecteer deze optie om bestaande PDF in uw output samen te voegen door hen aan uw kaart DITA als middeldossier toe te voegen. De PDF worden ingevoegd op de locatie die op de kaart wordt weergegeven en de pagina&#39;s worden dienovereenkomstig verhoogd. |
| **bed gebruikte doopvonten** in | Selecteer deze optie als u lettertypen gebruikt die mogelijk niet op de computer van de eindgebruiker zijn geïnstalleerd. Als deze optie is ingeschakeld, worden de gebruikte lettertypen ingesloten in de PDF, zodat de gebruiker de PDF kan zien zoals deze is bedoeld, zelfs als de lettertypen niet op zijn computer zijn geïnstalleerd. <br> **Nota**: Een doopvont kan worden ingebed slechts als het het plaatsen door de doopvontverkoper bevat die het om toelaat worden ingebed. Zorg ervoor dat u de vereiste instelling of licentie hebt voordat u een lettertype insluit. |
| **gebruik automatische woordafbreking** | Als automatische woordafbreking is ingeschakeld, worden woorden aan het einde van regels op grammaticaal correcte plaatsen afgebroken met een afbreekstreepje. |
| **laat JavaScript** toe | Schakel deze optie in als u een JavaScript-code hebt waarmee u de inhoud dynamisch wilt transformeren voordat u een PDF genereert. |
| **bed de dossiers van multimedia** in | Selecteer deze optie als u alle audio, video en interactieve inhoud van de PDF wilt opnemen. |
| **volledige compressie van het Gebruik om de grootte van de PDF te optimaliseren** | Selecteer deze optie als u een grote PDF wilt comprimeren of verkleinen. Houd er rekening mee dat het comprimeren van de PDF de bestandskwaliteit kan verminderen. |
| **de beeldcompressie van het Gebruik om de grootte van de PDF te optimaliseren** | Selecteer deze optie als u de gebruikte afbeeldingen in uw PDF wilt comprimeren of verkleinen. Houd er rekening mee dat het comprimeren van een afbeelding de afbeeldingskwaliteit kan verminderen. |
| **de douaneresolutie van het Gebruik (pixel per duim)** | Dit is de resolutie van de paginaweergave bij pixels per inch. Voer in het veld een voorkeurswaarde in die wordt weergegeven wanneer deze optie wordt geselecteerd. De standaardwaarde is 96 pixels per inch. Stel een hogere waarde in om meer inhoud in een inch te passen en andersom als u een lagere waarde instelt. |
| **toon Watermerk** | Selecteer deze optie als u een watermerk in de uitvoer wilt plaatsen. U kunt een nieuwe tekstreeks in het tekstvak invoeren met de tekenbehuizing zoals u wilt. <br><br> de statische tekst of taalvariabelen van het Gebruik om de gelokaliseerde versie van het watermerk te publiceren.  Afhankelijk van de gekozen taal wordt de gelokaliseerde waarde automatisch gekozen in de uitvoer van de PDF. U kunt bijvoorbeeld &quot;Publisher&quot; afdrukken als een watermerk in het Engels en &quot;Auteure&quot; in het Frans.  <br> Indeling: `${lng:<variable name>}` . `$ {lng:publisher-label}` waarbij `publisher-label` bijvoorbeeld een taalvariabele is. <br> Houd de cursor boven <img src="./assets/info-details.svg" alt= "info icon" width="25"> in de buurt van de optie voor meer informatie over de optie. |
| **laat vergelijkingen MathML** toe | Selecteer deze optie om MathML-vergelijkingen in uw inhoud te renderen. De vergelijkingen worden anders standaard genegeerd. |
| **Download tijdelijke dossiers** | Selecteer deze optie als u de tussentijdse HTML-bestanden wilt downloaden die tijdens het genereren van de native PDF-uitvoer zijn gemaakt. U kunt de tijdelijke bestanden later downloaden nadat u de uitvoer hebt gegenereerd. |
| **PDF conformance** | Dit is de standaard waarmee u de PDF wilt opslaan om ervoor te zorgen dat deze compatibel is. Selecteer een optie in het vervolgkeuzemenu om een keuze te maken in de lijst met beschikbare PDF-standaarden. Voor meer details over de gesteunde normen, zie [ Ongeveer de normen van de PDF ](https://helpx.adobe.com/acrobat/using/pdf-conversion-settings.html#about_pdf_x_pdf_e_and_pdf_a_standards). |
| **eigenschappen van het Dossier** | Selecteer de metagegevens die u wilt doorgeven aan het publiceren van de native PDF. In het vervolgkeuzemenu worden zowel de aangepaste als de standaardeigenschappen weergegeven. `dc:description`, `dc:language`, `dc:title` en `docstate` zijn bijvoorbeeld de standaardeigenschappen, terwijl u `author` als de aangepaste eigenschap kunt hebben. De geselecteerde eigenschappen van metagegevens worden doorgegeven aan het PDF-bestand dat wordt gegenereerd met Native PDF. <br> Deze eigenschappen worden gekozen uit het `metadataList` dossier beschikbaar bij:`/libs/fmdita/config/metadataList`. <br> Dit dossier kan bij worden bedekt: `/apps/fmdita/config/metadataList`. |


## Een PDF-uitvoer genereren {#generate-pdf-output}

Zodra u vooraf ingesteld output hebt gevormd kunt u output van het Vooraf ingestelde paneel produceren, gebruikend **produceert Vooraf ingestelde** eigenschap.

1. Onder het **lusje van de Auteur**, selecteer de **Bewaarplaats** Mening.\
   Hiermee wordt het deelvenster Opslagplaats geopend.

1. In het paneel van de Bewaarplaats, open het DITA kaartdossier in **Mening van de Kaart**.

1. In het **lusje van de Output**, klikt **vooraf instelt** om het Vooraf ingestelde paneel te bekijken.
Om een output tot stand te brengen of te vormen vooraf ingesteld, zie [ een PDF output vooraf ingesteld ](#create-output-preset) creëren.
1. Om uw montages te bewaren, klik **sparen allen** ![ sparen al ](assets/SaveFloppy_icon.svg) pictogram in de upper-left hoek van de standaardtoolbar in de mening van de Output.
1. Klik **produceren Vooraf ingesteld** ![ produceren vooraf ingesteld ](assets/generate-output.svg) pictogram op de hoogste bar.
In het deelvenster Voorinstellingen uitvoer kunt u een voortgangsbalk weergeven naast de geselecteerde uitvoervoorinstelling.
1. Zodra de outputgeneratie volledig is, klik **Uitvoer van de Mening** ![ meningsoutput ](assets/view-output.svg) pictogram op de hoogste bar om de output te bekijken.\
   A **de dialoogdoos van het Succes** is zichtbaar bij de laag-juiste hoek van het scherm.
Als de uitvoer niet is gelukt, wordt het onderstaande foutbericht weergegeven.
<img src="assets/error-log.png" alt="foutenlogboek" width="250">

Om het foutenlogboek te bekijken, klik **Ontwerpen**, over het geselecteerde vooraf ingestelde lusje, en klik ![ opties ](assets/options.svg) **Opties** > **Logboek van de Mening**.

### Tijdelijke bestanden downloaden nadat de uitvoer van de native PDF is gegenereerd

Als u de **tijdelijke dossiers van de Download** optie in de Geavanceerde montages selecteert, kunt u de tussentijdse HTML dossiers ook downloaden die terwijl het produceren van de Inheemse output van de PDF worden gecreeerd. Zodra u de output hebt geproduceerd, kunt u de tijdelijke dossiers downloaden gebruikend de **tijdelijke dossiers van de Download** ![ download tijdelijk dossiers ](assets/native-pdf-download-temporary-files-icon.svg) pictogram op de hoogste bar. Met deze functie kunt u uw tijdelijke stijlen en lay-outs voor HTML weergeven en kunt u uw CSS-stijlen naar wens corrigeren of wijzigen.


>[!NOTE]
>
> Het **tijdelijke dossiers van de Download** ![ download tijdelijke dossiers ](assets/native-pdf-download-temporary-files-icon.svg) pictogram verschijnt slechts als u de laatste output van de PDF gebruikend vooraf ingesteld hebt geproduceerd waar u de optie in **Geavanceerd** tabel hebt geselecteerd.



### Taalvariabelen gebruiken

AEM Guides ondersteunt ook taalvariabelen. Selecteer **Variabelen van de Taal** <img src="./assets/language-variables.svg" width="25"> in het linkerpaneel om een gelokaliseerde versie van de uit-van-de-doos etiketten zoals Nota, Waarschuwing, en Waarschuwing of statische tekst in de output van de PDF te bepalen. Voor meer details, zie [ Steun voor taalvariabelen ](../native-pdf/native-pdf-language-variables.md).



### Ondersteuning voor opmaakdocumenten

Experience Manager Guides biedt ook ondersteuning voor je prijsopmaakdocumenten.  Markeringsbestanden zijn gemakkelijk te maken en
biedt diverse opmaakopties. Leer hoe te [ documenten van de Markering van de auteur van de Redacteur van het Web ](../user-guide/web-editor-markdown-topic.md).

U kunt de onderwerpen van de Prijsverhoging aan uw kaart toevoegen DITA en de output van de PDF produceren gebruikend de Inheemse PDF output stelt vooraf in.  Leer hoe te om te vormen of [ tot een PDF vooraf ingestelde output ](#create-a-pdf-output-preset-create-output-preset) leiden.