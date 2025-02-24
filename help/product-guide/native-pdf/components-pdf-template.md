---
title: Systeemeigen PDF-publicatiefunctie | Componenten van een PDF-sjabloon
description: Leer de verschillende componenten van een PDF-sjabloon en hoe u deze kunt aanpassen en configureren.
exl-id: 0ddb3b81-42ca-4a66-be7d-051a5175d53a
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 47a6819654877e9a4e3e542fa6e5e360b3f3938f
workflow-type: tm+mt
source-wordcount: '4716'
ht-degree: 0%

---

# Componenten van een PDF-sjabloon {#components-pdf-template}

Een PDF-sjabloon heeft vier componenten: Pagina-indelingen, Stijlbladen, Bronnen en Instellingen. U kunt een sjabloon maken door deze afzonderlijke componenten aan te passen en de sjabloon aan een uitvoervoorinstelling te koppelen tijdens het genereren van een PDF-uitvoer. In de volgende secties worden deze componenten en hun aanpassingsproces uitgebreid besproken.


## Paginalay-outs maken en aanpassen {#create-customize-page-layout}

Met de instellingen in de component Pagina-indelingen kunt u de structuur van een pagina ontwerpen door de koptekst, voettekst en het inhoudsgebied op een pagina te definiëren. Met de WYSIWYG-paginaopmaakeditor kunt u een paginalay-out maken voor verschillende secties in een PDF, zoals de voorpagina&#39;s en achteromslag, het hoofdstuk, de tabel
Inhoud (TOC), index, lege pagina, Voorste basispagina&#39;s, Achtergrond basispagina&#39;s, Lijst met figuren (LOF), Lijst met tabellen (LOT), verklarende woordenlijst of maak een indeling voor een aangepaste pagina. In de PDF-sjablooninstellingen kunt u een pagina-indeling met verschillende secties binnen een PDF toewijzen. Deze secties worden vervolgens gebruikt om de PDF-uitvoer te genereren.

### Een nieuwe pagina-indeling maken {#create-page-layout}

>[!NOTE]
>
>Er zijn voorbeeldpaginalay-outs die uit de doos worden verzonden. U kunt deze aanpassen of nieuwe paginalay-outs maken.

1. In de Redacteur van het Web, ga naar de **Output** tabel.
1. Breid linkerzijbalk uit en klik **Malplaatjes**.
1. Open de sjabloon waarmee u wilt werken.

   >[!NOTE]
   >
   >U kunt een sjabloon openen door te dubbelklikken op de naam of op het pictogram > naast de naam.

1. Voer een van de volgende handelingen uit om een nieuwe pagina-indeling te maken:

   * Beweeg over **Lay-outs van de Pagina** en klik (*het pictogram van Opties*) **...** en kies **Nieuwe Lay-out van de Pagina**.


   * In het **paneel van Malplaatjes**, klik **+** pictogram naast **Malplaatjes** en kies **Lay-out van de Pagina** van het contextmenu.


     Dit opent **toevoegt de dialoog van de Lay-out**.

     <img src="assets/add-layout-2.png" alt="Dialoogvenster Lay-out toevoegen" width="250">

1. Geef een naam op voor de nieuwe pagina-indeling.
   >[!NOTE]
   >
   >Gebruik geen speciale tekens wanneer u een paginalay-out een naam geeft. Een spatie in de naam wordt vervangen door een onderstrepingsteken &quot;_&quot;.

1. Klik **Gedaan**.

   De nieuwe indeling wordt gemaakt en toegevoegd onder Pagina-indelingen.


### Een pagina-indeling dupliceren {#duplicate-page-layout}

1. In de **sectie van Malplaatjes** van het malplaatje dat u wilt dupliceren, **Lay-outs van de Pagina** tweemaal klikken of **klikken>** pictogram vóór **Lay-outs van de Pagina**.

   Hiermee wordt de lijst met paginalay-outs in de sjabloon weergegeven.

1. Beweeg over de paginalay-out die u wilt dupliceren en klikken (*het pictogram van Opties*) **...** en selecteert **Dupliceer** van het contextmenu.

1. In het _Dubbele dialoog van de Lay-out_, ga een naam voor de paginalay-out in.

1. Klik **Gedaan**.
Onder Pagina-indelingen wordt een kopie van de geselecteerde pagina-indeling gemaakt en toegevoegd.

### Een pagina-indeling aanpassen {#customize-page-layout}

1. In de **sectie van Malplaatjes** van het malplaatje dat u wilt uitgeven, **Lay-outs van de Pagina** tweemaal klikken of **klikken>** pictogram vóór **Lay-outs van de Pagina**.

   Hiermee wordt de lijst met paginalay-outs in de sjabloon weergegeven.
1. Voer een van de volgende handelingen uit om een pagina-indeling aan te passen:
   * Dubbelklik op een pagina-indeling.
   * Beweeg over om het even welke paginalay-out en klik (*het pictogram van Opties*) **..** en selecteer **uitgeven** van het contextmenu.

   Hiermee opent u de pagina-indeling-editor voor aanpassing.
1. Zodra u de gewenste veranderingen hebt aangebracht, klik *sparen allen* (of `Crl+S`).

   Voor meer informatie bij het bepalen van individuele lay-outelementen zoals kopbal, footer, paginanummer, titel, en meer, zie [ Ontwerp een paginalay-out ](design-page-layout.md).

## Stijlbladen gebruiken om PDF aan te passen {#stylesheet-customization}

Met de instellingen in de component Stylesheets kunt u de onderdelen voor de paginalay-out en de DITA-inhoud opmaken met de WYSIWYG-editor of rechtstreeks met het CSS-bestand werken. U kunt uw eigen stijlen maken of de standaardstijleigenschappen aanpassen. De redacteur van WYSIWYG geeft u de toegang tot de meeste eigenschappen die u uw paginalay-out of inhoud DITA zou moeten opmaken. Voor geavanceerde aanpassingen kunt u rechtstreeks in de Source-weergave werken.

### Een nieuw stijlblad maken {#create-stylesheet}

Terwijl CSS-bestanden worden geleverd voor inhoud en lay-out, kunt u een nieuwe stijlpagina maken om meerdere aanpassingen toe te passen op een specifiek stijltype dat vervolgens kan worden toegepast op een doelcomponent. Standaard worden CSS-voorbeeldbestanden gebundeld in het product. Deze CSS-bestanden zijn bedoeld om u te helpen bij het ordenen van uw opmaakgegevens over inhoud en lay-outs. U kunt deze stijlen samenvoegen in één CSS-bestand of in meerdere bestanden.

Wanneer u een nieuwe pagina-indeling maakt, wordt het bestand `layout.css` standaard opgenomen in de nieuwe pagina-indeling. Als u wilt dat de paginalay-out stijlen uit een ander CSS-bestand bevat, kunt u het gewenste CSS-bestand gewoon slepen en neerzetten in het inhoudsbewerkingsgebied van de nieuwe paginalay-out. Als u wilt controleren of het CSS-bestand is ingesloten in de pagina-indeling, schakelt u over naar de Source-weergave en vindt u een koppeling naar het CSS-bestand in het element `<head>` .

Voer de volgende stappen uit om een stijlpagina te maken:
1. In het **paneel van Malplaatjes**, doe één van het volgende:
   * Beweeg over het **Stylesheets** lusje en klik (*het pictogram van Opties*) **...** en kies **Nieuwe Stylesheet**.
   * Klik **+** pictogram naast **Malplaatjes** en kies **Stijlblad** van het contextmenu.

   Hiermee wordt het dialoogvenster Stijlpagina toevoegen geopend.

   <img src="assets/add-stylesheet.png" alt="Stijlpagina toevoegen" width="250">
1. Geef een naam op voor de nieuwe stijlpagina.
1. Klik **Gedaan**.

   Er wordt een nieuwe stijlpagina gemaakt en toegevoegd onder de sectie Stijlvoorbladen.

### Een nieuwe stijl maken {#create-style}

Standaard bevatten de CSS-bestanden die bij de sjabloon horen stijlen voor kop, alinea, teken, hyperlink, afbeelding, tabel, div, pagina en andere stijlen. U kunt de standaardopmaak overschrijven of een nieuwe stijl maken.


U kunt een nieuwe stijl tot stand brengen om het in de paginalay-out van het malplaatje te gebruiken of een douanestijl voor om het even welk element toepassen DITA. Als u deze aangepaste stijlen op het DITA-element wilt toepassen, moet u ervoor zorgen dat de klassennaam van de stijl gelijk is aan de naam van het DITA-element of het kenmerk `outputclass` .  `<div>` in DITA wordt bijvoorbeeld bepaald door het kenmerk `.div {}` in CSS of het kenmerk `outputclass` ervan. Als u `<div outputclass="my-div">` toepast in DITA, wordt deze beheerd door de `.div {}` of `.my-div {}` in de CSS.



Voer de volgende stappen uit om een nieuwe stijl te maken:
1. Vouw de linkerzijbalk uit en dubbelklik op de sjabloon waarin u de stijl wilt maken.
1. Breid de **Stylesheets** sectie uit. Het opent het **paneel van Stijlen** dat alle het stileren opties bevat.
1. Selecteer + pictogram om een nieuwe stijl toe te voegen.

   **voegt de dialoogdoos van de Stijl** toe opent.


   <img src="assets/add-style.png" alt="Nieuwe stijl toevoegen" width="500"/>

1. Specificeer de naam van de a **Klasse**. Als u een stijl op het DITA-element wilt toepassen, moet u ervoor zorgen dat de klassenaam van de stijl gelijk is aan de naam van het DITA-element of het kenmerk `outputclass` .
1. Op het **gebied van de Markering** (facultatief), kies een markering waarvoor u een nieuwe stijl wilt tot stand brengen.


1. Selecteer de Klasse van de a **Pseudo** om een element te stileren. Met een pseudoklasse kunt u een speciale status van het element definiëren. Gebruik bijvoorbeeld de pseudo-klasse om een element op te maken wanneer u de muisaanwijzer op het element plaatst of wanneer u de focus op het element plaatst. U kunt ook meerdere pseudoklassen selecteren. U kunt bijvoorbeeld pseudo-klasse `a::visited {color: blue;}` gebruiken om de bezochte koppelingen op te maken.

1. Voeg de kiezer voor de nieuwe stijl toe. Het **gebied van de Selector** {helpt u om douanekiezers naast de klasse, de Markering, en de combinatie van de Klasse toe te voegen Pseudo. U kunt bijvoorbeeld een `table a.link` -stijl maken voor alle hyperlinks in een tabel.

   Voor meer informatie betreffende CSS markeringen, verwees de mening [ naar CSS stijlgrammatica ](https://www.w3.org/TR/CSS21/syndata.html#characters).

1. Klik **Gedaan**.

   Er wordt een nieuwe stijl gemaakt en toegevoegd aan de lijst met stijlen.

### Een vooraf gedefinieerde of nieuwe stijl aanpassen {#customize-style}

Nadat u een nieuw CSS-bestand met standaardstijlen hebt gemaakt of stijlen in een bestaand CSS-bestand wilt aanpassen, kunt u hiervoor de stijleneditor gebruiken.

Voer de volgende stappen uit om een stijl aan te passen:
1. Dubbelklik **Stylesheets** of klik het **>** pictogram vóór **Stylesheets**.

   Hiermee worden de standaard (Inhoud en Lay-out) en aangepaste CSS-bestanden weergegeven.
1. Open een stijlpagina om te bewerken.

   Voer een van de volgende handelingen uit om stijlpagina te openen voor bewerken:
   * Dubbelklik op de naam van het stijlblad.
   * Houd de muisaanwijzer boven de naam van het stijlblad en klik op (pictogram Opties) ... en kies Bewerken.

   Hiermee wordt het stijlblad geopend voor bewerking en wordt de lijst met stijlen weergegeven in het deelvenster Stijlen.

   <img src="assets/customize-style.png" alt="Stijl aanpassen" width="800">

1. Als u een stijl wilt aanpassen, selecteert u de stijl die u wilt weergeven en past u deze aan met de Stijleditor.


### Eigenschappen van stijlen

In het middelste deelvenster kunt u de eigenschappen bewerken, maar het kan lastig zijn om een opname te krijgen van alle waarden.  De **ruit van Eigenschappen** geeft een snelle mening van alle attributen en waarden van de stijl.

In het middelste deelvenster kunt u de veelgebruikte eigenschappen bewerken, maar niet alle eigenschappen die CSS ondersteunt. In de **ruit van Eigenschappen**, kunt u alle eigenschappen uitgeven die CSS steunt en hen voorproef. U hoeft niet over te schakelen naar de bronweergave om eigenschappen te bewerken.


Leer meer over het gebruiken van de stijlredacteur aan [ werk met de gemeenschappelijke inhoudsstijlen ](stylesheet.md).

## Werken met bronnen {#work-with-resources}

Dit is een container voor alle elementen die worden gebruikt om een sjabloon te ontwerpen. U kunt de map beschouwen als een map die elementen bevat zoals achtergrondafbeeldingen, aangepaste lettertypen, logo&#39;s en meer. Telkens wanneer u middelen in uw malplaatje toevoegt, wordt het geupload of controleert in de activaomslag. Vervolgens kunt u deze elementen gebruiken om uw PDF-sjablonen aan te passen of te ontwerpen.

Voer de volgende stappen uit om een elementbestand toe te voegen aan de map Resources:

1. Houd de cursor boven het tabblad Bronnen, klik op het pictogram Opties ... en kies Importeren.

   Hiermee wordt het dialoogvenster Assets uploaden geopend.

   <img src="assets/resources-import-assets.png" alt="Elementen uploaden" width="300">

   De weg waar het activadossier zal worden geupload wordt getoond op het **Uitgezochte gebied van de Omslag van Activa**.
   >[!NOTE]
   >
   >U kunt het pad voor het uploaden van elementen niet wijzigen. Standaard worden alle elementen opgeslagen in de map `/content/dam/dita-templates/pdf/<PDF-template-name>` .

1. Klik **kiezen Dossiers** om het activadossier van uw lokale machine te doorbladeren

1. Klik **uploaden**.
Het geselecteerde bestand wordt geïmporteerd en vermeld in de map Bronnen.

## Geavanceerde PDF-instellingen {#advanced-pdf-settings}

Met de sectie Instellingen kunt u de geavanceerde instellingen configureren voor de PDF-paginalay-out, PDF starten vanaf een oneven of even pagina, indelingen voor de kruisverwijzingen en drukkermarkeringen inschakelen in de uiteindelijke PDF die wordt gegenereerd
het gebruiken van het malplaatje.

>
>
> Beginnend met Experience Manager Guides 5.0/2025.02.0 versie, is de **sectie van de Druk** in de Geavanceerde montages van PDF verplaatst naar het **vooraf instelt van de Output** paneel. Om de montages van de Druk te vormen, publiceer de mening [ output van PDF ](../web-editor/native-pdf-web-editor.md#print).

Om te vormen, klik **Montages** in het **paneel van Malplaatjes** om de volgende opties te bekijken:

### Algemeen

Stel de basisconfiguratie-instellingen in voor het starten van een hoofdstuk van een oneven of even pagina, de inhoudsopgavestructuur en definieer de opmaak van de leaderregel voor de inhoudsopgave-items. U kunt de volgende instelling definiëren:

* **Begin om het even welk nieuw hoofdstuk van**: Staat u toe om te bepalen hoe elk hoofdstuk in definitieve PDF wordt gepubliceerd. U kunt van a **Nieuwe Pagina** kiezen, **Oneven Pagina**, **zelfs Pagina**, of **Huidige pagina** opties. Als u ervoor kiest om een nieuw hoofdstuk te beginnen vanaf een oneven pagina, wordt een lege pagina ingevoegd na een hoofdstuk dat op een oneven pagina eindigt. Bijvoorbeeld, als uw hoofdstuk op paginanummer 15 beëindigt, dan zal het het publiceren proces een lege 16 <sup> de </sup> pagina opnemen zodat het nieuwe hoofdstuk van de 17 <sup> de </sup> pagina kan beginnen.  Als u de **Huidige optie van de Pagina** kiest, dan worden alle hoofdstukken gepubliceerd in voortzetting zonder enige pagina einden. Als een hoofdstuk bijvoorbeeld halverwege pagina 15 eindigt, wordt het volgende hoofdstuk ook vanaf de 15e pagina zelf gestart.

* **Begin elk onderwerp van een nieuwe pagina**: Als u elk onderwerp binnen uw hoofdstuk van een nieuwe pagina wilt beginnen, dan selecteren **Begin elk onderwerp van een nieuwe pagina** optie. Schakel deze optie uit als u uw onderwerpen wilt voortzetten zonder tussenruimten op de pagina.

* **Structuur van TOC**: Staat u toe om de hiërarchie van de Inhoudsopgave aan te passen. Hiervoor worden de volgende aanvullende instellingen gebruikt:

   * **Koppen van het Gebruik tot Niveau**: Het staat u toe om het aantal kopniveaus aan te passen die in de structuur van TOC van uw PDF moeten worden getoond.
   * **toon geen paginanummer voor het eerste niveau in TOC**: Selecteer deze optie om de overeenkomstige paginaaantallen voor alle hoofdstukken te verbergen die genestelde of kindonderwerpen bevatten. Bekijk het volgende voorbeeld waarin een uitvoer wordt gemaakt zonder deze optie te selecteren.

  <img src="assets/page-number-in-toc.png" alt="Elementen uploaden" width="250">

  In het bovenstaande voorbeeld zijn Geavanceerde PDF-instellingen, Bijlage en Juridische informatie de onderwerpkoppen of hoofdstuktitels op het eerste niveau. Aan al deze koppen wordt een paginanummer toegewezen.

  Nu, als u deze optie selecteert en de output produceert, dan zult u volgende TOC krijgen:

  <img src="assets/page-number-missing-in-toc.png" alt="Elementen uploaden" width="250">

  Hier kunt u zien dat het eerste hoofdstuk Geavanceerde PDF-instellingen geen paginanummer krijgt, omdat het geneste of onderliggende onderwerpen bevat. Terwijl een paginanummer indien toegewezen aan Bijlage en Juridisch omdat zij standalone onderwerpen zonder enig kindonderwerp zijn.

* **toon geen hoofdstukaantal in TOC**: Selecteer deze optie om de hoofdstuknamen zonder de hoofdstukaantallen in TOC te tonen.   Standaard worden de hoofdstuknummers weergegeven in de inhoudsopgave van uw PDF-uitvoer.
* **formaat van de Leider**: Gebruik drop-down om Gestippelde, Ononderbroken, of de lijnen van de Leider van de Ruimte te selecteren om rubriekniveaus met zijn overeenkomstige paginanummers te verbinden.
Voor het toepassen van de structuur van TOC en het stileren van rubriekniveaus, zie [ hoofdstukTOC ](design-page-layout.md#add-chapter-toc) toevoegen.

  >[!NOTE]
  >
  >Als u een CSS-ontwikkelaar bent, kunt u de leaderindeling ook rechtstreeks in het CSS-bestand definiëren.

* **markering van de lijstvoortzetting van het Gebruik**: Selecteer deze optie om tellers voor lange lijsten te bepalen die zich over veelvoudige pagina&#39;s verspreiden.
U kunt de tekst definiëren die voor en na het einde moet worden weergegeven. Bijvoorbeeld, breken een lijst op pagina 5, en u bepaalt `<Continued on page %page-num%>` voor **Tekst vóór Break**.  Onder aan pagina 5 wordt &quot;Vervolg op pagina 6&quot; weergegeven.

  Taalvariabelen gebruiken om de tekst voor en na het einde van de vervolgmarkering te definiëren. Afhankelijk van uw gekozen taal wordt de gelokaliseerde waarde automatisch gekozen in de PDF-uitvoer. U kunt `Continued on page %page-num%` bijvoorbeeld publiceren als tekst in het Engels en `Fortsetzung auf Seite %page-num%` in het Duits.

  Overslaan <img src="./assets/info-details.svg" alt= "info icon" width="25"> in de buurt van de optie voor meer informatie over de optie.
* **de verklarende woordenlijsttermijnen van de Verbinding aan de verklarende woordenlijstpagina**: Selecteer deze optie om de verklarende woordenlijsttermijnen als hyperlinks in de inhoud te tonen en hen te verbinden met de termijnen op de verklarende woordenlijstpagina. Hierdoor kunnen lezers snel de definitie bekijken van een term die is gedefinieerd in de woordenlijst.

  Als u de termen in de woordenlijst wilt omzetten in hyperlinks, moet u:
   * Laat **Verklarende woordenlijst** in het **lusje van de Orde van de Lay-out van de Pagina** voor een kaart DITA toe.
   * Voeg de Verklarende woordenlijst in de Achterpagina&#39;s van de Matter voor een kaart van het Boek toe.

  Als u de pagina Woordenlijst niet inschakelt, worden de termen in de woordenlijst in de inhoud niet geconverteerd naar hyperlinks in de PDF-uitvoer.
  <!--For more information on using table continuation markers, see Use table continuation markers.-->

### Pagina-indelingen {#page-layouts}

Met de instellingen voor Pagina-indelingen hebt u volledige controle over het opgeven van de paginalay-out die moet worden gebruikt voor een bepaalde sectie van het document. Als u bijvoorbeeld een indeling voor de inhoudsopgave wilt selecteren, klikt u op het vervolgkeuzemenu onder het veld Inhoudsopgave en selecteert u de indeling die u hebt ontworpen om de inhoudsopgave te genereren.

Het is belangrijk om op te merken dat de montages van de boekenkaart een belangrijkheid over de montages van de paginalay-out nemen.

De volgende instellingen zijn beschikbaar in de sectie Pagina-indeling:

<img src="assets/template-page-layout.png" alt="Paginalay-outs" width="550">


**StandaardLay-out van de Pagina**: Selecteer een paginalay-out die als standaardlay-out voor alle pagina&#39;s in uw PDF dienst doet. Dit is de lay-out van de basispagina die op die secties of onderwerpen wordt toegepast waar u geen specifieke paginalay-out hebt gecreeerd.

**lay-out van de Pagina voor verschillende secties**: U kunt een paginalay-out met de volgende secties van uw output van PDF in kaart brengen. Als u een paginalay-out voor de verwante sectie hebt ontworpen, dan selecteer het van de drop-down lijst. Als er geen paginalay-outs zijn gemaakt voor een bepaalde sectie, wordt de standaardpagina-indeling toegepast.

* **Hoofdstuk &amp; Onderwerpen**: U kunt de paginalay-out voor het Hoofdstuk specificeren &amp; Onderwerpen. De geselecteerde lay-out wordt toegepast op alle hoofdstukken en onderwerpen.

* **TOC**: Als u de TOC paginalay-out hebt ontworpen, uitgezochte **TOC** in de drop-down lijst, en alle TOC pagina&#39;s in uw document zal de TOC paginalay-out hebben.

* **Lijst van Cijfers en Lijst van Lijsten**: U kunt de paginalay-out voor figuren en lijsten ook specificeren. De geselecteerde lay-out wordt toegepast op alle figuren en tabellen.

* **Index**: Als u een de paginalay-out van de Index hebt ontworpen, kaart het aan de optie van de Index. Met behulp van de opmaakmodellen kunt u verschillende indexelementen opmaken in de PDF-uitvoer. Gebruik de indexstijlen `.idx-header`, `.idx-footer`, `.idx-body`, `.idx-title`, `.idx-keyword-group`, `.idx-unit`, `.idx-keyword`, `.idx-name`, `.idx-link` en `.idx-child` om de stijlen voor de elementen van de index aan te passen.

* **Verklarende woordenlijst**: Als u een de paginalay-out van de Verklarende woordenlijst hebt, dan kaart het aan de optie van de Verklarende woordenlijst.

  De termen in de woordenlijst van de PDF-uitvoer worden altijd in alfabetische volgorde gesorteerd.

  U kunt ook de tag `sort-as` toevoegen om een sorteersleutel voor de termen in de woordenlijst te definiëren. Experience Manager Guides gebruikt vervolgens de sorteersleutel om de termen in de woordenlijst te sorteren in plaats van de termen in de woordenlijst. Als u de sorteersleutel niet hebt gedefinieerd, worden de termen in de woordenlijst gebruikt om te sorteren. U kunt bijvoorbeeld de tag `sort-as` toevoegen aan de `glossterm` en de waarde ervan instellen op `A` voor de term &quot;USB&quot; (bijvoorbeeld `<glossterm>USB<sort-as>A</sort-as></glossterm>` ). Op dezelfde manier kunt u ook de tag `sort-as` toevoegen en de waarde ervan instellen op `B` voor de term &#39;Pendagina&#39;. Wanneer u deze verklarende woordenlijsttermijnen sorteert, verschijnt de soortsleutel `A` voor de verklarende woordenlijsttermijn &quot;USB&quot;vóór de soortsleutel `B` voor de verklarende woordenlijsttermijn &quot;de Aandrijving van de Pen&quot;. In de PDF-uitvoer komt &#39;USB&#39; voor &#39;Pen Drive&#39; op de woordenlijstpagina.

  Met de opmaakmodellen kunt u verschillende woordenlijstelementen opmaken in de PDF-uitvoer. Gebruik de verklarende woordenlijststijlen `.glo-header`, `.glo-footer`, `.glo-body`, `.glo-title`, `.glo-unit`, `.glo-link` en `.glo-term` om de stijlen voor de elementen van de verklarende woordenlijst aan te passen.

  Leer meer over het gebruiken van de stijlredacteur aan [ werk met de gemeenschappelijke inhoudsstijlen ](stylesheet.md).

* **Voorste de Pagina&#39;s van de Matter en de Achterpagina&#39;s van de Matte**: Deze paginalay-outs bepalen het stileren voor of achtermaterie pagina&#39;s in uw boek. Als u de voorste materialay-out hebt ontworpen, kaart het aan de **Voorste optie van de Pagina&#39;s van de Matter**. Wanneer u de lay-out van de voormaterie van dropdown selecteert, wordt de voorproeflay-out toegepast op alle onderwerpen in de voorkwestie.

  Als u de achtermaterialay-out hebt ontworpen, kaart het aan de **Achteroptie van de Pagina&#39;s van de Matte**. Wanneer u de lay-out van de achtermaterie van dropdown selecteert, wordt de achtermaterialenlay-out toegepast op alle onderwerpen in de achterzaak.

  **Voorste de Pagina&#39;s van de Matter** wordt ook gebruikt als reserve lay-out voor **TOC**, **Lijst van Cijfers**, en Lijst van Lijsten.  Op dezelfde manier wordt de **Achtergrondpagina&#39;s van de Matter** ook gebruikt als reserve lay-out voor de **Index** en **Verklarende woordenlijst** lay-outs. Als u de lay-out voor deze pagina&#39;s niet hebt geselecteerd, wordt de geselecteerde lay-out Pagina&#39;s vóór of achter toegepast.  Als u de lay-out Pagina&#39;s vóór of achter niet hebt geselecteerd, wordt de standaardpaginalay-out op hen toegepast.

* **Lay-out van de Pagina voor Lege Pagina&#39;s**:    U kunt ook de pagina-indeling voor de lege pagina&#39;s opgeven. De geselecteerde indeling wordt toegepast op alle lege pagina&#39;s. Bijvoorbeeld, als u een Lege paginalay-out voor alle lege pagina&#39;s hebt ontworpen, dan uitgezochte **Lege** in de drop-down lijst, en alle lege pagina&#39;s in uw document zullen de Lege paginalay-out hebben.

* **de Pagina en Achterpagina van de Omslag**: Als u een omslag paginalay-out hebt ontworpen, dan kaart het aan de **optie van de Pagina van de Omslag**. Op dezelfde manier als u een achterpaginalay-out hebt, dan kaart het aan de **Achteroptie van de Pagina**. Als er geen lay-outs voor de omslag- of achtergrondpagina zijn gemaakt, wordt de standaardpagina-indeling toegepast.



Voor meer informatie over paginalay-outs, zie [ Ontwerp een paginalay-out ](design-page-layout.md).

### Volgorde pagina-indeling {#page-order}

U kunt de volgende secties in uw PDF tonen of verbergen en ook de volgorde schikken waarin ze in de uiteindelijke PDF-uitvoer moeten worden weergegeven:



* Inhoudsopgave
* Hoofdstuk en onderwerp
* Lijst met figuren
* Lijst met tabellen
* Index
* Verklarende woordenlijst
* Visum

  <img src="assets/page-order-advance-settings.png" alt="Paginalay-outvolgorde" width="550">

  Als u geen bepaalde sectie wilt tonen in de PDF-uitvoer, kunt u die verbergen door de schakeloptie uit te schakelen.

  U kunt ook de volgorde definiëren waarin deze verschillende secties worden gegenereerd in uw PDF. Als u de standaardvolgorde van deze secties wilt wijzigen, selecteert u de stippelbalken om de secties naar de gewenste locatie te slepen.

  >[!NOTE]
  >
  > De instellingen voor volgorde en opname zijn alleen van toepassing op een DITA-kaart. Deze instellingen zijn niet van toepassing op een bladwijzer. De pagina&#39;s in een bladwijzer worden weergegeven in de volgorde van de secties in de bladwijzer.


.
**Hoofdstuk &amp; de lay-out van Onderwerpen** wordt altijd toegelaten door gebrek. U kunt niet schakelen.

**pagina&#39;s van de Fusie**

Standaard beginnen alle secties op een nieuwe pagina. Selecteer de **Vorige Pagina** of **Volgende Pagina** optie van **Fusie met** dropdown om een sectie met een vorige of volgende pagina samen te voegen. Hiermee wordt de sectie gepubliceerd in overeenstemming met de geselecteerde pagina in de PDF-uitvoer. Hierdoor is er geen pagina-einde tussen.

>[!NOTE]
>
> Deze instelling is alleen van toepassing op de sectie en niet op de componenten ervan.  Bijvoorbeeld, als u de **Vorige pagina** optie voor **Hoofdstuk &amp; Onderwerpen** selecteert, de **Hoofdstukken en Onderwerpen** sectie samenvoegen met de vorige pagina. De diverse hoofdstukken en de onderwerpen worden gepubliceerd zoals per **Algemene** montages.Bijvoorbeeld, als in **om het even welk nieuw hoofdstuk van het plaatsen** begint, selecteert u **Oneven Pagina**, dan wordt een lege pagina opgenomen na een hoofdstuk dat op een oneven pagina beëindigt.

Wanneer u een sectie samenvoegt tot de vorige of volgende pagina, wordt de inhoud samengevoegd en wordt de stijl toegepast van de doelsectie waarin de inhoud is samengevoegd.

Bijvoorbeeld, als u **TOC** en **Hoofdstuk &amp; Onderwerpen** toelaat en de **Volgende Pagina** voor **TOC** selecteert, **TOC** samenvoegt met de volgende sectie, die **Hoofdstuk &amp; Onderwerpen** is. De stijl van de **Hoofdstuk &amp; sectie van Onderwerpen** wordt toegepast op de samengevoegde inhoud van beide secties.

De fusieoptie werkt achtereenvolgens, zodat als u **Volgende Pagina** voor veelvoudige ononderbroken secties hebt geselecteerd, zij allen samenvoegen met de eerste sectie (in de volgende richting), die deze bezitsreeks niet heeft. Bijvoorbeeld, laat u **TOC** toe, **Hoofdstuk &amp; Onderwerpen**, **Lijst van Cijfers**, en **Index**. Dan, als u **Volgende Pagina** voor **TOC** plaatst, **Hoofdstuk &amp; Onderwerpen**, **Lijst van Cijfers**, en **niets** voor **Index**, zij allen samenvoegen met **Index**.


**Statische pagina&#39;s**

De verschillende paginalay-outs helpen u de output van de diverse secties ontwerpen. Deze secties worden geproduceerd van de kaart DITA terwijl u de output publiceert.
U kunt ook aangepaste paginalay-outs maken en deze als statische pagina&#39;s publiceren in de PDF-uitvoer. Zo kunt u statische inhoud toevoegen, zoals notities of lege pagina&#39;s.

Voer de volgende stappen uit om een aangepaste pagina-indeling toe te voegen:

1. Selecteer **toevoegen** ![](assets/add-icon.svg) om een nieuwe paginalay-out toe te voegen. Het deelvenster Paginalay-out toevoegen wordt geopend.
2. Selecteer de pagina-indeling in de lijst en klik op Toevoegen. De nieuwe paginalay-out wordt toegevoegd aan de lijst met paginalay-outs.


U kunt ook de volgende handelingen uitvoeren:

* Selecteer de stippelbalken om de paginalay-out naar de gewenste locatie te slepen.

* Selecteer **verwijderen Lay-out** ![](assets/delete-icon.svg) om een lay-out te verwijderen.

* U kunt ook een statische pagina samenvoegen met de vorige of de volgende pagina.

* U kunt ook meerdere keren een aangepaste indeling toevoegen en bestellen. Hierdoor kunt u de statische inhoud op de juiste wijze publiceren.

  U kunt bijvoorbeeld een aangepaste indeling gebruiken om een statische waarschuwing meerdere keren te publiceren in de PDF-uitvoer.



### Paginaorganisatie

De pagina&#39;s in een PDF-document worden doorgaans gepubliceerd op basis van de inhoud die is geordend in de DITA-kaart of het bladwijzerbestand. U kunt echter ook de volgorde van pagina&#39;s in het PDF-document wijzigen. U kunt bijvoorbeeld een document met meerdere pagina&#39;s afdrukken als een boekje. Wanneer u de vellen sorteert, vouwt en niet, is het resultaat één boek met de juiste paginavolgorde.  Je kan het gepubliceerde boek dan lezen als een boek.

<img src="assets/template-page-organization.png" alt="Paginaorganisatie" width="550">


De volgende montages zijn beschikbaar onder de **sectie van de Organisatie van de Pagina 0} {:**

#### Paginavolgorde

Selecteer een paginavolgorde die de volgorde bepaalt van de pagina&#39;s in uw PDF-document. U kunt de volgende opties kiezen in het vervolgkeuzemenu:

* **Gebrek**: De standaardorde van de pagina&#39;s zoals per het brondossier.
* **Oneven pagina&#39;s eerst**: Alle oneven pagina&#39;s worden bewogen vóór alle even pagina&#39;s.
* **Even pagina&#39;s eerst**: Alle even pagina&#39;s worden bewogen vóór alle oneven pagina&#39;s.
* **Omgekeerd**: De paginaorde wordt omgekeerd.
* **Boek**: Alle pagina&#39;s worden bevolen zoals in een boekje.
* **recht aan LinkerBoekje**: Alle pagina&#39;s zijn in orde van rechts naar links boekje.
* **Douane**: Bepaal een douaneorde van pagina&#39;s in plaats van een vooraf bepaalde orde.
   * &quot;a..b&quot; — Alle opeenvolgende pagina&#39;s van a tot en met b.
   * &quot;a,b,c&quot; — Nieuwe paginavolgorde a, b, c.
   * &quot;a*b&quot; — De pagina a wordt telkens herhaald.
   * &quot;-a&quot; — Negatieve paginanummers worden vanaf de laatste pagina teruggeteld en kunnen met andere aangepaste bestellingen worden gecombineerd.
   * &quot;X&quot; — Alle pagina&#39;s van het document. Hetzelfde resultaat als &quot;1..-1&quot;.

U kunt bijvoorbeeld een aangepaste volgorde geven zoals &quot;2,3,5*2,7.10,-1,-2.
De gegeven paginavolgorde leidt ertoe dat een PDF de volgende paginanummers heeft van het oorspronkelijke document, ervan uitgaande dat het 25 pagina&#39;s in totaal heeft: 2, 3, 5, 5,7, 8, 9, 10, 25, 24.

#### Meer dan één pagina per vel configureren

Kies deze optie als u meerdere pagina&#39;s op één vel papier wilt publiceren.  Selecteer vervolgens het aantal rijen en kolommen en publiceer de pagina&#39;s als een raster op één blad. U kunt de pagina&#39;s bijvoorbeeld publiceren als een raster van 2 rijen en 4 kolommen.

Definieer de grootte van het doelblad en de afdrukstand waarin u het blad wilt publiceren. U kunt ook de marge- en opvullingseigenschappen van het blad opgeven.

### Kruisverwijzingen {#cross-references}

Gebruik het **lusje van de Verwijzing** om te bepalen hoe de verwijzingen PDF worden gepubliceerd. U kunt de kruisverwijzingen opmaken voor onderwerptitel, tabellen, figuren en meer.

>[!NOTE]
>
> Als u de koppelingstekst hebt gedefinieerd terwijl u de kruisverwijzing invoegt, heeft deze voorrang op de opmaak voor kruisverwijzingen die is gedefinieerd in de Native PDF-sjabloon.

U kunt ook variabelen gebruiken om een kruisverwijzing te definiëren.  Wanneer u een variabele gebruikt, wordt de waarde ervan gekozen uit de eigenschappen. U kunt een kruisverwijzing definiëren met behulp van één variabele of een combinatie van variabelen. U kunt ook een combinatie van een tekenreeks en een variabele gebruiken.

U kunt bijvoorbeeld `View details on {chapter}` gebruiken. Als de naam van het Hoofdstuk &quot;Algemene montages is,&quot;is de verwijzing in de output &quot;zie details op Algemene montages.&quot;

AEM Guides biedt de volgende variabelen voor een out-of-the-box:

* {title}: hiermee maakt u een kruisverwijzing naar de titel van het onderwerp. Zie bijvoorbeeld Nuttige koppelingen op pagina 2.
* {page} Hiermee voegt u een kruisverwijzing toe aan de paginanummers. Zie bijvoorbeeld op pagina 1.
* {description}: voegt een kruisverwijzing toe aan de tekst van de beschrijving. Zie bijvoorbeeld de details van AEM Guides.
* {chapter}: hiermee wordt een kruisverwijzing toegevoegd naar de hoofdstuknummers. Zie bijvoorbeeld hoofdstuk 1.
* {bookmarkText}: hiermee maakt u een kruisverwijzing naar de tekst met bladwijzer. Zie stop_words bijvoorbeeld op pagina 5.
* {captionText}: hiermee maakt u een kruisverwijzing naar het bijschrift van de afbeelding of tabel in het onderwerp. Zie bijvoorbeeld Airflow op pagina 2.
* {figure}: voegt een kruisverwijzing toe aan het figuurnummer. Kies deze optie om het figuurnummer te kiezen uit de stijlen voor automatische nummering die u voor figuren hebt gedefinieerd.  U kunt bijvoorbeeld &quot;Zie {figure} op pagina {page}&quot; gebruiken. De kruisverwijzing in de uitvoer bevat het automatisch gegenereerde figuurnummer en het bijbehorende paginanummer &quot;Zie Figuur 1 op pagina 5&quot;.
* {table}: voegt een kruisverwijzing toe aan het tabelnummer. Hiermee selecteert u het tabelnummer op basis van de stijlen voor automatische nummering die u voor het bijschrift hebt gedefinieerd. U kunt bijvoorbeeld &quot;Zie {table} op pagina {page}&quot; gebruiken. De kruisverwijzing in de uitvoer bevat het automatisch gegenereerde tabelnummer en het bijbehorende paginanummer &quot;Zie Tabel 1 op pagina 5&quot;.



  >[!NOTE]
  >
  >U kunt automatische nummerstijlen maken voor bijschrift- en figuurcodes.

#### Standaardindeling voor kruisverwijzing

Als u het tekstveld leeg laat en u de koppelingstekst niet hebt gedefinieerd terwijl u een kruisverwijzing invoegt, voegt Experience Manager Guides de volgende variabelen voor de respectievelijke kruisverwijzingen toe:

* **Titel**: `{title}`
* **Beschrijving**: `{description}`
* **Paragraaf**: `{bookmarkText}`
* **Bladwijzer**: `{bookmarkText}`
* **Cijfer**: `{captionText}`
* **Lijst**: `{captionText}`

De prioriteitsvolgorde voor kruisverwijzingen is:
* Tekst koppelen die is toegevoegd aan de kruisverwijzingen
* Opmaak voor kruisverwijzingen gedefinieerd in de Native PDF-sjabloon
* Standaardindeling voor kruisverwijzing


#### Taalvariabelen in kruisverwijzingen

U kunt ook taalvariabelen gebruiken om gelokaliseerde kruisverwijzingen te definiëren. Afhankelijk van uw gekozen taal wordt de gelokaliseerde waarde automatisch gekozen in de PDF-uitvoer.

U kunt bijvoorbeeld een taalvariabele &quot;reference-label&quot; toevoegen en de waarden in het Engels en het Duits definiëren.

* Engels - &quot;View on page {page}&quot;
* Duits - &quot;Einzelheiten finden Sie auf der Seite {page}&quot;


Wanneer u `${lng:<variable name>}` toevoegt aan de sectie Alinea, bevatten de kruisverwijzingen in de alinea&#39;s van de uitvoer de gelokaliseerde tekst en het paginanummer.\
In de volgende schermafbeeldingen ziet u bijvoorbeeld de kruisverwijzingen &quot;Weergeven op pagina 1&quot; in het Engels en &quot;Einzelheiten finden Sie auf der Seite 1&quot; in het Duits.

<img src="./assets/english-output-corss-reference.png" alt="Engelse uitvoer van een kruisverwijzing in een alinea" width ="800" border="2px">

*kruisverwijzing van A binnen een paragraaf wanneer gepubliceerd in de Engelse taal.*

<img src="./assets/german-output-corss-reference.png" alt="Duitse uitvoer van een kruisverwijzing in een alinea" width ="800" border="2px">


*kruisverwijzing van A binnen een paragraaf wanneer gepubliceerd in de Duitse taal.*

<!--For more information, see *Format cross-references*.-->
