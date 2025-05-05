---
title: Bijlage
description: Leer hoe u InDesigns kunt voorbereiden voor conversie
exl-id: 02da0e61-7a73-4c4c-9bd7-2664d90fa728
feature: InDesign File Conversion
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '2851'
ht-degree: 0%

---

# Bijlage {#id195AD0L60Y4}

## Bestanden van InDesigns voorbereiden voor conversie {#id195DBF0045Z}

InDesign biedt auteurs een uitgebreide reeks functies voor het maken van aantrekkelijke en complexe documenten. Dit betekent vaak dat de verschillende delen van een document visueel op de pagina worden geplaatst, maar zonder dat wordt geprobeerd om stroom tussen die tekstkaders tot stand te brengen. Wanneer &quot;*lezingsorde*&quot;van de tekstkaders niet wordt bepaald, zal het IDML- dossier verhalen bevatten die geen zinvolle orde kunnen volgen. Het eindresultaat zal één of meerdere onderwerpen DITA met paragrafen, lijsten en grafiek in een willekeurige orde zijn.

Terwijl het mogelijk is om de inhoud DITA in een zinnige orde in een redacteur uit te geven DITA, is het veel gemakkelijker om het dossier van het InDesign te bevestigen alvorens het IDML- dossier tot stand te brengen. Dit kan worden gedaan zonder de blik van het brondocument te veranderen. Het heeft ook het voordeel dat het brondocument toegankelijk wordt gemaakt door de leesvolgorde correct te definiëren.

***het Verbinden tekstkaders***

InDesign gebruikt de term *&quot;threading&quot;* voor het proces om één kader aan een andere te verbinden. Voor meer details over het verbinden van tekstkaders, zie *[Verbindend tekst ](https://helpx.adobe.com/in/indesign/using/threading-text.html)* onderwerp in de documentatie van het InDesign.

***Overlappende kaders***

Sommige documenten van het InDesign gebruiken niet-verbonden overlappende kaders voor lay-outredenen. Het kan erg moeilijk zijn om deze inhoud samen te voegen in de hoofdthread. De beste optie kan zijn om het resultaat in het milieu uit te geven DITA.

***de verhalen van het InDesign***

Elke verbonden stroom van inhoud in een document van het InDesign is een genoemd a &#39;*verhaal*&#39;. Voor de beste resultaten is het raadzaam het aantal artikelen beperkt te houden. Er zijn echter delen van uw document die niet nodig zijn in de DITA-uitvoer. Pagina-voetteksten zijn bijvoorbeeld zelden nodig, maar kunnen in het midden van een onderwerp verschijnen als ze niet zorgvuldig worden verwerkt.

De gemakkelijkste manier om tekst uit te sluiten die niet in het document wordt vereist is het een speciale *Markering van de Paragraaf* te geven die slechts voor de ongewenste inhoud wordt gebruikt. Bijvoorbeeld, in plaats van het hergebruiken van a *\ [Basisparagraaf \]* voor footer, creeer een specifieke *Voettekst* markering. Dan in het MapStyle- dossier plaats eenvoudig de *Voettekst* paragrafen om als dit te laten vallen:

```XML
<paraRule style="Footer" local="0" refactor="drop">
   <attributeRules createID="false"/>
</paraRule>
```

***Toewijzing aan DITA doctypes***

Het is van essentieel belang dat uw brondocument ten minste één alineastijl of -element heeft die het begin van een onderwerp kan markeren. Het is gemeenschappelijk voor documenten om *Heading1* als naam van de top-level titels in het document te gebruiken. U kunt dan een afbeelding van die stijl aan een specifiek DITA documenttype tot stand brengen. Als uw document goed georganiseerd is en het gebruik van *Heading1* constant door is, dan zult u goede resultaten krijgen.

***Veelvoudige DITA doctypes***

Als sommige van *Heading1* paragrafen in verschillende DITA documenttypes moeten omzetten, dan dupliceer de paragraafstijl in InDesign. Geef deze stijlen een gemakkelijke om naam zoals *te erkennen Heading1 \_genTask* of *Kop1 \_het oplossen van problemen* zoals aangewezen. Stel vervolgens het mapStyle-bestand in zoals hieronder wordt weergegeven:

```XML
<doctypes>
   <doctypeParaRule style="Heading1" local="0" mapToDoctype="concept">
      <attributeRules createID="true"/>
   </doctypeParaRule>
   <doctypeParaRule style="Heading1_genTask" local="0" mapToDoctype=" generalTask">
      <attributeRules createID="true"/>
   </doctypeParaRule>
   <doctypeParaRule style="Heading1_troubleshooting" local="0"mapToDoctype=" troubleshooting">
      <attributeRules createID="true"/>
   </doctypeParaRule>
</doctypes>
```

***Gestructureerde documenten van het InDesign***

InDesign heeft een losse relatie met XML. Hoewel een document een XML DTD kan bevatten en het hoofdartikel geldig kan zijn tegen die DTD, is het ook mogelijk om hybride documenten te maken waar sommige inhoud XML is, maar geen DTD is inbegrepen. Dit zijn de ongewenste gevallen van een geslaagde conversie naar DITA. Als een document XML-onderdelen bevat, probeert u de uitvoer op te slaan in XML en controleert u of de resultaten acceptabel zijn. Als dat niet het geval is, bevat de DITA-inhoud ook ongeldige inhoud of kan deze volledig mislukken.

***het formatteren van de Lijst***

De conversie van InDesign van de de lijsthet formatteren regels aan het gelijkwaardige lijst formatteren in DITA is een complex proces. Dit komt door de rijke opmaakkenmerken die beschikbaar zijn in de bronbestanden in vergelijking met de basisopties in het tabelmodel Oasis \(CALS\) dat wordt gebruikt in DITA. Verticale en horizontale tekstuitlijning is beschikbaar en geeft vergelijkbare resultaten, hoewel uitgevulde tekst altijd wordt uitgevuld volgens de tekstrichting, terwijl InDesign Links uitvullen en Rechts uitgevuld toestaat.

De manier waarop InDesigns kolom- en rijscheidingstekens hanteren, is weer veel beter dan de basisopties van het tabelmodel Oasis. InDesign biedt vier celranden: randtype \(effen of patroondikte\), randdikte, randkleur, randtint, randtussenkleur en randtussenruimtetint. Deze moeten allemaal worden toegewezen aan de randen rechts en onder aan elke cel \(entry-element\), waarbij de enige opties 0 of 1 zijn: de rand verbergen of de rand tonen.

De grens in InDesign kan op de volgende niveaus worden toegepast:

- Tabelstijlen
- Celstijlen
- Lokale overschrijvingen op elke cel

Het InDesign naar DITA-omzettingsproces past de grensregeling als volgt toe:

- Tabelstijlen worden voor verticale regels toegewezen aan het kenmerk `colspec/@colsep` . Horizontale regels worden toegewezen aan het kenmerk `row/@rowsep` . In beide gevallen wordt het kenmerk niet gemaakt als de rand niet is gedefinieerd.
- Celstijlen worden toegewezen aan de kenmerken `entry/@colsep` en `entry/@rowsep` . Deze waarden zullen om het even welke van de Stijl van de Lijst afgeleide grensheerser met voeten treden.
- Bij lokale overschrijvingen wordt de opmaak rechtstreeks op de cel toegepast en worden de tabelstijlen en celstijlen genegeerd.

***Afwisselende patronen***

Met Tabelstijlen voor InDesigns kunnen de kolom- en cellijnen een wisselend patroon volgen. Hoewel deze functie wordt ondersteund voor conversie, zijn de resultaten alleen duidelijk wanneer een patroongroep de regel \(1\) weergeeft en de andere patroongroep de toewijzingen \(0\) verbergt.

## Het toewijzingsbestand voorbereiden voor InDesign naar DITA-migratie {#id194AF0003HT}

Voor de juiste DITA-conversie is een toewijzingsbestand vereist dat overeenkomt met de inhoud van het brondocument. Voor documenten met ongestructureerde InDesigns betekent dit dat alle beschikbare alineastijlen en tekenstijlen moeten worden toegewezen. Voor documenten van het gestructureerde InDesign van XML moeten alle elementen in zijn bijbehorende DTD in kaart worden gebracht.

De toewijzingsbestanden voor ongestructureerde en gestructureerde documenten van InDesigns zijn verschillend. Dit is toe te schrijven aan de complexere verwerkingsvereisten voor het omzetten van ongestructureerde broninhoud in DITA.

Hieronder volgt een voorbeeld van het toewijzingsbestand:

```XML
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE styleMap SYSTEM "mapStyle.dtd">
<styleMap xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="mapStyle.xsd" >
   <doctypes>
      <mapDoctypeParaRule root="itpx:stories" mapToDoctype="map">
         <attributeRules createID="true">
            <addNew name="outputclass" value="map"/>
         </attributeRules>
      </mapDoctypeParaRule>
      <doctypeParaRule style="Heading 1" local="0" mapToDoctype="concept">
         <attributeRules createID="true"/>
      </doctypeParaRule>
      <doctypeParaRule style="Heading A" local="0" mapToDoctype="topic">
         <attributeRules createID="true"/>
      </doctypeParaRule>
   </doctypes>
   <wrappingRules>
      <wrap elements="li+" context="number" wrapper="ol">
         <attributeRules createID="true"/>
      </wrap>
      <wrap elements="li+" context="bullet" wrapper="ul">
         <attributeRules createID="true"/>
      </wrap>
   </wrappingRules>
   <paragraphStyleRules>
      <paraRule style="Heading 2" local="0"  mapTo="p">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="Heading 3" local="0"  mapTo="p">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="List Paragraph" local="p[-|-|-|-|-|b|-|-]" context="bullet" mapTo="li">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="List Paragraph" local="p[-|-|-|-|-|n|-|-]" context="number" mapTo="li">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="List Paragraph" local="0" context="bullet" mapTo="li">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="Normal" local="0"  mapTo="p">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="Normal" local="p[-|-|-|-|-|b|-|-]" context="bullet" mapTo="li">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="Title" local="0"  mapTo="p">
         <attributeRules createID="true"/>
      </paraRule>
   </paragraphStyleRules>
   <characterStyleRules>
      <charRule style="Bold" local="0" mapTo="b">
         <attributeRules createID="false"/>
      </charRule>
      <charRule style="Code" local="0" mapTo="codeph">
         <attributeRules createID="false"/>
      </charRule>
      <charRule style="[No character style]" local="c[Bold|-|-|-|-|-|-|-]" mapTo="b">
         <attributeRules createID="false"/>
      </charRule>
      <charRule style="[No character style]" local="c[Italic|-|-|-|-|-|-|-]" mapTo="i">
         <attributeRules createID="false"/>
      </charRule>
   </characterStyleRules>
</styleMap>
```

Het toewijzingsbestand is een XML-bestand met een eenvoudige structuur waarin alle bronalineastijlen en tekenstijlcodes worden vermeld. De bestandsinhoud wordt hieronder uitgelegd:

**Toewijzing van de Stijl**

In het element `styleMap` kunt u twee optionele kenmerken opgeven - `@map_date` en `@map_version` voor het opnemen van de versie van het toewijzingsbestand.

**Type van Document**

Het element `doctypes` bevat een lijst met de ondersteunde DITA-kaart en onderwerptoewijzingen.

**het documenttype van de Kaart paragraafregels**

Het element `mapDoctypeParaRule` is verplicht. De attributen van dit element moeten niet worden uitgegeven omdat het het wortelelement van bronXML altijd aan het wortel `map` element van de kaart DITA in kaart wordt gebracht.

**het type van Document paragraafregel**

Het element `doctypeParaRule` is verplicht. Dit geeft het omzettingsproces een manier om het begin van een nieuw onderwerp te identificeren. Normaal gesproken wordt het kenmerk `@style` op zichzelf gebruikt en wordt het kenmerk `@local` ingesteld op 0. Als er echter altijd lokale opmaakoverschrijvingen op de gekozen stijl staan, moet u een regel toevoegen voor elke stijl plus de lokale overschrijvingen. Dit is eenvoudig te herkennen in het gegenereerde toewijzingsbestand waar dit of een vergelijkbaar bestand kan worden gevonden:

```XML
<paraRule style="Heading 1" local="0" mapTo="p">
   <attributeRules createID="true"/>
</paraRule>
<paraRule style="Heading 1" local="p[Italic|-|-|-|-|-|-|-]" mapTo="p">
   <attributeRules createID="true"/>
</paraRule>
```

In het bovenstaande voorbeeld zijn er twee `paraRule` -elementen voor `@style` = &quot;Kop1&quot;. Maak gewoon een equivalent `doctypeParaRule` -element met het `@mapToDoctype` -kenmerk ingesteld als vereist.

De kenmerken die worden gebruikt in `doctypeParaRule` worden hieronder uitgelegd:

- `@style`: De naam van een stijl in het document van het bronInDesign.
- `@local`: Zie [\#id194CG0V005Z ](#id194CG0V005Z).
- `@mapToDoctype`: De naam van een DITA onderwerptype van een opgesomde lijst van alle geldige `doctypes`.

**Regels van de het verpakken van het Element**

De elementomsluitende regels bepalen de manieren om elementen in het binnenkomende document om te zetten in een vooraf gedefinieerd element volgens een reeks kenmerkwaarden.

***`wrap`element***

Dit is een optioneel element. Het element `wrap` bevat een lijst met de elementen die omlopen of worden verplaatst. Wrapping wordt doorgaans gebruikt wanneer een reeks elementen een gemeenschappelijk bovenliggend element moet krijgen. Bijvoorbeeld, veelvoudige `li` elementen die in een `ol` element worden verpakt. Daarnaast kan `wrap` worden gebruikt voor het verplaatsen van elementen, zoals titels voor figuren en tabellen.

De kenmerken die worden gebruikt in `wrap` worden hieronder uitgelegd:

- `@element`: Een plusteken na een elementnaam toont aan dat alle aangrenzende elementen met de zelfde naam in het element zullen worden verpakt dat in het `@wrapper` wordt genoemd attribuut.
- `@wrapper`: De naam van het element dat de omloop bevat.
- `@context`: biedt een manier om verder te verfijnen hoe een bepaald element omloopt. In het volgende voorbeeld wordt een manier getoond om een reeks `li` -elementen in een geordende lijst `ol` of een ongeordende lijst `ul` toe te wijzen volgens de `@context` waarde \(de context wordt gedefinieerd op het `paraRule` -element\):

  ```XML
  <wrap elements="li+" context="number" wrapper="ol">
     <attributeRules createID="true"/>
  </wrap>
  <wrap elements="li+" context="bullet" wrapper="ul">
     <attributeRules createID="true"/>
  </wrap>
  ```


In het volgende voorbeeld wordt getoond hoe u een `fig` -element maakt op basis van een `title` - en `image` -element:

- `@elements`: De elementen die worden vermeld en gescheiden door een komma, worden opgenomen in het element dat wordt genoemd in het kenmerk `@wrapper` . Omdat het gebruikelijk is om figuurtitels onder de afbeelding op te nemen, is de titel het `title` -element dat direct volgt op de `image` .

  De volgende omloopregel:

  ```XML
  <wrap elements="title, image" context="FigTitle" wrapper="fig">
     <attributeRules createID="true"/>
  </wrap>
  ```

  Hiermee wordt de volgende tussenliggende XML geconverteerd:

  ```XML
  <image href="Links/myImage.png" scale="59">
     <title>IDML2DITA workflow</title>
  ```

  In de volgende geldige DITA figuurstructuur:

  ```XML
  <fig id="id397504">
     <title>IDML2DITA workflow</title>
     <image href="Links/myImage.png" scale="59">
  </fig>
  ```

- `@wrapper`: De naam van het element dat de omloop bevat.
- `@context`: biedt een manier om verder te verfijnen hoe een bepaald element omloopt \(de context is gedefinieerd voor het `paraRule` element\).

In het volgende voorbeeld wordt getoond hoe u een `title` naar een `table` verplaatst:

- `@elements`: Het `title` -element dat zich direct voor of direct na een `table` bevindt, wordt opgenomen in het element dat in het `@wrapper` -kenmerk wordt genoemd. Een predikaat van XPath-stijl kan de positie van het titelelement als `[before]` of `[after]` identificeren.

  Voorbeeld: de volgende omloopregel:

  ```XML
  <wrap elements="title[before]" context="TableTitle" wrapper="table">
     <attributeRules createID="true"/>
  </wrap>
  ```

  Hiermee wordt de volgende tussenliggende XML geconverteerd:

  ```XML
  <title>IDML2DITA workflow</title>
  <table id="id289742" outputclass="BasicTable">
     <tgroup cols="2">
        <colspec colname="0" colwidth="0.7*">
           <colspec colname="1" colwidth="0.3*">
  ```

  In deze geldige DITA-figuurstructuur:

  ```XML
  <table id="id289742" outputclass="BasicTable">
     <title>IDML2DITA workflow</title>
     <tgroup cols="2">
        <colspec colname="0" colwidth="0.7*">
           <colspec colname="1" colwidth="0.3*">
  ```

- `@wrapper`: De naam van het element dat de omloop bevat.

- `@context`: biedt een manier om verder te verfijnen hoe een bepaald element omloopt \(de context is gedefinieerd voor het `paraRule` element\).


**de stijlregels van de Paragraaf**

De elementen van `<paragraphStyleRule>` worden hieronder beschreven:

***`paraRule`element***

Het element `paraRule` is verplicht. Hiermee geeft u de toewijzingsregels voor alle alineastijlen op. In een document van het InDesign, is al tekst bevat binnen substructuur van de Stijlen van de Paragraaf, zelfs de paragrafen zonder enige stijl worden genoemd `[No paragraph style]`. De vierkante haakjes geven een ingebouwde stijlnaam voor een InDesign aan.

>[!NOTE]
>
> De vierkante haakjes geven een ingebouwde stijlnaam van een InDesign aan.

De kenmerken die worden gebruikt in `paraRule` worden hieronder uitgelegd:

- `@style`: De naam van een stijl in het document van het bronInDesign.
- `@local`: Zie [\#id194CG0V005Z ](#id194CG0V005Z).
- `@mapTo`: De naam van een DITA-doelelement.

- `@context`: Dit attribuut wordt gebruikt om aan een specifieke **omslag** regel te verbinden wanneer meer dan één omslagkeus beschikbaar is. Voorbeeld: het `li` -element kan zijn verpakt in een `ol` - of `ul` -element. Als u de verschillende lijsttypen wilt identificeren, kunt u een specifieke stijlnaam of het kenmerk `@local` gebruiken, die het volgende kan weergeven:
   - `local="p[-|-|-|-|-|b|-|-]"` Waar &#39;`b`&#39; in veld 6 een lijstitem met opsommingstekens aangeeft. In dit geval stelt u `@context` in op &#39;`bullet`&#39;.
   - `local="p[-|-|-|-|-|n|-|-]"` Waar &#39;`n`&#39; in veld 6 een genummerd lijstitem aangeeft. In dit geval stelt u `@context` in op &#39;`number`&#39;.

- `@commentOut`: Dit kenmerk schakelt de terugloop van het doelelement in XML-opmerkingen in, zodat de informatie niet verloren gaat, maar handmatig door de gebruiker kan worden verwerkt. Dit is nuttig als de broninhoud niet kan worden gedwongen om aan de DITA-structuurregels te voldoen.

- `@refactor`: Dit optionele kenmerk heeft twee waarden:

- `unwrap`: het overeenkomende element wordt verwijderd terwijl de inhoud behouden blijft.

- `drop`: Het overeenkomende element en de inhoud ervan worden verwijderd.


**de stijlregels van het Karakter**

De elementen van `charRule` worden hieronder beschreven:

>[!NOTE]
>
> De ingebouwde tekenstijl `[No character style]` wordt bij `local="0"` niet in kaart gebracht, omdat deze tijdens de voorbehandeling worden verwijderd.

***`charRule`element***

Dit is een optioneel element.

Dit zijn de toewijzingsregels voor alle tekenstijlen. In een document van het InDesign, is al tekst bevat binnen kindelementen van de Stijlen van het Karakter.

De kenmerken die worden gebruikt in `charRule` worden hieronder uitgelegd:

- `@style`: De naam van een stijl in het document van het bronInDesign.
- `@local`: Zie [\#id194CG0V005Z ](#id194CG0V005Z).
- `@mapTo`: De naam van een DITA-doelelement.
- `@refactor`: Dit optionele kenmerk heeft twee waarden:
   - `unwrap`: het overeenkomende element wordt verwijderd terwijl de inhoud behouden blijft.

   - `drop`: Het overeenkomende element en de inhoud ervan worden verwijderd.


**de regels van Attributen**

Dit element kan een onderliggend element zijn van de volgende elementcontexten:

- `mapDoctypeParaRule`
- `mapDoctypeElemRule`
- `doctypeParaRule`
- `doctypeElemRule`
- `paraRule`
- `charRule`
- `elementRule`

Het doel van kenmerkregels is het beheren van de kenmerken voor de overeenkomende elementen.

Afhankelijk van de context zijn de volgende kenmerken beschikbaar voor het element `attributeRules` :

- `@createID`: genereert een unieke id voor de overeenkomende elementen. Toegestane waarden `true` of `false` . Beschikbaar in alle contexten.
- `@copyAll`: kopieert alle kenmerken van de bron-XML-inhoud alleen voor gestructureerde bronbestanden. Toegestane waarden zijn `true` of `false` . Beschikbaar voor contexten `mapDoctypeParaRule` , `mapDoctypeElemRule` , `doctypeElemRule` en `elementRule` .


De kenmerken die worden gebruikt in `attributeRules` worden hieronder uitgelegd:

>[!NOTE]
>
> Dit element kan meerdere onderliggende elementen bevatten.

- `addNew`: voegt een nieuw kenmerk toe aan het overeenkomende element. Beschikbaar voor alle contexten. Het heeft twee attributen:
   - `@name`: moet een geldige XML-naam zijn, bij voorkeur geldig voor de DITA-context.
   - `@value`: kan letterlijke tekst of een eenvoudige XPath-expressie zijn.
- `copyAtt`: kopieert één kenmerk naar het doel en wijzigt desgewenst de naam ervan in het proces. De waarde wordt niet gewijzigd. Beschikbaar voor contexten `mapDoctypeParaRule` , `mapDoctypeElemRule` , `doctypeElemRule` en `elementRule` . Wanneer dit element aanwezig is, wordt de waarde `@copyAllAtts` aangenomen op `false` . Het heeft twee attributen:
   - `@name`: moet de naam zijn van een kenmerk dat aanwezig is op het bron-XML-element.
   - `@mapTo`: moet een geldige XML-naam zijn, bij voorkeur geldig voor de DITA-context.

**Lokale het formatteren codes**

In elk document van een InDesign kunnen alineastijlen en tekenstijlen honderden verschillende opmaakoverschrijvingen bevatten. De meeste van deze eigenschappen bieden geen nuttige rol in het conversieproces. We hebben echter een kernset opmaakfuncties geïdentificeerd die wel van invloed zijn op de semantiek van het document en die het conversieproces moeten beïnvloeden.

De `@local` -kenmerken worden weergegeven als een speciale indeling met scheidingstekens, waarbij acht velden worden opgegeven en een voorvoegsel voor het type opmaakoverschrijving. De velden met opmaakcodes worden hieronder weergegeven:

- Prefix **p** voor lokale opheffing van de parastijl of **c** voor lokale opheffing van de karakterstijl.
- **stijl van de Doopvont** die de familienaam en eigenschappen zoals &quot;***Vet Verdicht Cursief***&quot;is.
- **de grootte van de Doopvont** in punten.
- **positie van het Karakter** voor superscript of subscript.
- **onder** voor underscore.
- **Slag** voor doorhaling.
- **code van de Lijst** om lijsttype als bulleted of Genummerd te identificeren - niet altijd gebruikt door InDesign.
- **de code van de Bullet** maakt een lijst van alle bepaalde bullettypes in het document.
- **de code van het Aantal** maakt een lijst van alle bepaalde nummeringsstijlen in het document.

Wanneer u deze functie zorgvuldig gebruikt, kan verloren lokale opmaak de kwaliteit van een overdracht van gestileerde inhoud naar DITA verbeteren. Dit voorbeeld kan worden omgezet in cursieve, 16-pt tekst in een lijst met opsommingstekens: `p[Italic|16|-|-|-|b|-|-]` .

**Toewijzing van de Structuur**

Het structuurtoewijzingsbestand lijkt op het stijltoewijzingsbestand met een eenvoudige structuur die alle bronelementen en relevante kenmerktypen opsomt. Er zijn twee kenmerken `@map_date` en `@map_version` beschikbaar voor het opnemen van de versie van het te gebruiken toewijzingsbestand.

**Type van Document**

Het element `doctypes` bevat een lijst met de ondersteunde DITA-kaart en onderwerptoewijzingen.

**de regels van het documenttype van de Kaart element**

Het element `mapDoctypeElemRule` is verplicht. De attributen van dit element moeten niet worden uitgegeven omdat het het wortelelement van bronXML altijd aan het wortel `map` element van de kaart DITA in kaart wordt gebracht.

**Regels van de het verpakken van het Element**

**`elementRules`element** Dit maakt een lijst van alle elementen.

**`elementRule`element** Het element `elementRule` is verplicht. Dit zijn de toewijzingsregels voor alle bronelementen. Terwijl een document van het InDesign ongestructureerde stijlelementen bevat, worden deze genegeerd voor gestructureerde inhoud tenzij de &quot;***hybride wijze***&#39; verwerking wordt toegelaten.

De kenmerken die worden gebruikt in `elementRule` worden hieronder uitgelegd:

- `@elementName`: De naam van een element in het document met het bronelement.

- `@local`: Zie [\#id194CG0V005Z ](#id194CG0V005Z). \(Alleen handig voor hybride documenten\).

- `@mapTo`: De naam van een DITA-doelelement.

- `@refactor`: Dit optionele kenmerk heeft twee waarden:

   - `unwrap`: het overeenkomende element wordt verwijderd terwijl de inhoud behouden blijft.

   - `drop`: Het overeenkomende element en de inhoud ervan worden verwijderd.

- `@context`: Dit kenmerk wordt gebruikt om een koppeling te maken naar een specifieke omloopregel wanneer meerdere wrapper-keuzen beschikbaar zijn. Voorbeeld: het `li` -element kan zijn verpakt in een `ol` - of `ul` -element.

- `@commentOut`: Dit kenmerk schakelt de terugloop van het doelelement in XML-opmerkingen in, zodat de informatie niet verloren gaat, maar handmatig door de gebruiker kan worden verwerkt. Dit is nuttig als de broninhoud niet kan worden gedwongen om aan de DITA-structuurregels te voldoen.


## Problemen met AEM Guides oplossen

Nadat u AEM Guides hebt geïnstalleerd en geconfigureerd, kunt u de problemen oplossen.

## Referenties valideren

U kunt de opgegeven scripts uitvoeren om de referenties te valideren. Deze scripts kunnen u helpen de verbroken verwijzingen te identificeren en deze vervolgens te repareren of te herstellen.

- `/bin/fmdita/validatebtree?operation=validate` - hiermee worden verbroken inhoudsverwijzingen gerapporteerd, maar worden deze niet hersteld.
- `/bin/fmdita/validatebtree?operation=patch` - geeft een overzicht van de verbroken inhoudsverwijzingen en patches of corrigeert deze.

**bevestigt manuscript**

Voer de volgende stappen uit om de verwijzingen te controleren, gebruikend het validate manuscript beschikbaar in het productpakket:

1. Voer het script voor validatie \[`/bin/fmdita/validatebtree?operation=validate`\] uit om te controleren of er nieuwe verbroken verwijzingen zijn.
1. Als het validate manuscript om het even welke fouten meldt, kunt u het herstellen gebruikend het flardmanuscript.
1. Registreer de hieronder gegeven details en deel hen indien nodig met uw team van het klantensucces:
1. &#x200B;
   - Wordt afgedrukt door script voor validatie
- Pakket met &quot;`/content/fmdita/references`&quot;
- Eventuele andere vereiste details, afhankelijk van het gerapporteerde scenario

**manuscript van het Reparatie**

Voer de volgende stappen uit om verbroken verwijzingen te repareren met behulp van het patchscript dat beschikbaar is in het productpakket:

1. Voer het patchscript `[/bin/fmdita/validatebtree?operation=patch]` uit om de verbroken verwijzingen te herstellen. De uitvoering van het script neemt een paar minuten in beslag en drukt de logbestanden af terwijl deze worden uitgevoerd. Zodra de uitvoering voltooit, drukt het &quot;`Done`&quot;aan het eind.

   **Nota:* men adviseert dat u en sparen de logboeken voor verwijzingsdoel kopieert.

1. Nadat het patchscript is uitgevoerd, kunt u de volgende controles uitvoeren:
1. &#x200B;
   - Controleren of er een nieuw knooppunt is gemaakt onder `/content/fmdita` `references_backup_<timestamp>"`
- Controleer of de referenties zijn gecorrigeerd

**Logger**

U kunt ook een afzonderlijk logger maken voor de uitvoering van dit script, zoals beschreven in de volgende details:

- Mlanger toevoegen aan klasse &quot;`adobe.fmdita.common.BTreeReferenceValidator`&quot;
- Instellen op `DEBUG`

In het gemaakte logbestand wordt alle informatie opgenomen die betrekking heeft op de uitvoering van het script. Deze informatie is handig voor het geval de sessietime-outs van de browser worden uitgeschakeld en wordt het script geactiveerd vanuit de browser.
