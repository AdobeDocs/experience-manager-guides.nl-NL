---
title: De dita-elementtoewijzing aanpassen met AEM-componenten
description: Leer hoe u de toewijzing van dita-elementen kunt aanpassen met AEM-componenten
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 834959a6a0e22cd5d2b2c5d0e57ceb6d45c0c666
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 1%

---


# DITA-elementtoewijzing aanpassen met AEM-componenten {#id1679J600HEL}

DITA-elementen in de AEM Guides worden toegewezen aan hun overeenkomstige AEM-componenten. AEM Guides gebruikt deze toewijzing in workflows, zoals publiceren en reviseren, om DITA-elementen om te zetten in een corresponderende AEM-component. De toewijzing wordt gedefinieerd in het `elementmapping.xml` -bestand, dat kan worden geopend via pakketbeheer voor Cloud Service-instellingen en via de URL: `/libs/fmdita/config/elementmapping.xml` in de CRXDE Lite-modus voor installatie op locatie.

>[!NOTE]
>
> Breng geen aanpassingen aan in de standaardconfiguratiebestanden in het knooppunt ``libs`` . U moet een overlay van het knooppunt ``libs`` in het knooppunt ``apps`` maken en de vereiste bestanden alleen in het knooppunt ``apps`` bijwerken.

U kunt de vooraf gedefinieerde DITA-elementtoewijzingen gebruiken of u kunt DITA-elementen toewijzen aan uw aangepaste AEM-componenten. Als u uw aangepaste AEM-componenten wilt gebruiken, moet u de structuur van het `elementmapping.xml` -bestand begrijpen.

## elementmapping.xml-structuur

Hieronder vindt u een overzicht op hoog niveau van de `elementmapping.xml` -structuur:

1. Elk element DITA wordt eerst gezocht naar een overeenkomstige componentenafbeelding die op de elementnaam wordt gebaseerd. Bijvoorbeeld:

   ```XML
   <ditaelement>     
      <name>**substeps**</name>  
      <class>- topic/ol task/substeps</class>  
      <componentpath>dita/components/ditaolist</componentpath>  
      <type>COMPOSITE</type>  
      <target>para</target>
   </ditaelement>
   ```

   In het bovenstaande voorbeeld worden alle `substeps` DITA-elementen gerenderd met de `dita/components/ditaolist` -component.

1. Als een element DITA geen gelijke vindt die op de naam wordt gebaseerd, dan wordt een gelijke op de basis van `class` gedaan. Bijvoorbeeld:

   ```XML
   <ditaelement>  
      <name>topic</name>  
      <class>**- topic/topic**</class>  
      <componentpath>fmdita/components/dita/topic</componentpath>  
      <type>COMPOSITE</type>  
      <target>para</target>  
      <attributemap> 
         <attribute from="id" to="id" />  
      </attributemap>
   </ditaelement>
   ```

   Als er in het bovenstaande voorbeeld geen toewijzing is gedefinieerd voor het element `task` , wordt het element `task` toegewezen aan de bovenstaande component omdat `task` wordt overgeërfd van de component `topic` .

1. Wanneer een element een overeenkomstige componentenafbeelding heeft, dan wordt de verdere verwerking van zijn kindelementen bepaald door `type`. Bijvoorbeeld:

   ```XML
   <ditaelement>  
      <name>title</name>  
      <class>- topic/title</class>  
      <componentpath>foundation/components/title</componentpath>  
      <type>**STANDALONE**</type>  
      <target>para</target>  
      <textprop>jcr:title</textprop>
   </ditaelement>
   ```

   `type` gebruikt de volgende waarden:

   - COMPOSITE: element aan component *afbeelding gaat ook voor kindelementen* verder.

   - STANDALONE: De kindelementen van het huidige element worden *niet verder in kaart gebracht*.

   In het bovenstaande voorbeeld, als het `<title>` -element onderliggende elementen bevat, worden deze niet toegewezen aan een andere component. De component voor `<title>` -element is verantwoordelijk voor het renderen van alle onderliggende elementen binnen het `<title>` -element.

1. Als er meerdere componenten zijn toegewezen aan één DITA-element, wordt de beste overeenkomst voor het element geselecteerd. Om de beste overeenkomende component te selecteren, worden het domein en de structurele specialisatie van elementen DITA overwogen.

   Als er elementen DITA met domeinspecialisatie zijn en een component voor domeinspecialisatie in kaart wordt gebracht, dan wordt die component hoge prioriteit gegeven.

   Op dezelfde manier als er elementen DITA met structurele specialisatie zijn en een component voor structurele specialisatie in kaart wordt gebracht, dan wordt die component hoge prioriteit gegeven.

1. U kunt `<attributemap>` gebruiken in elementtoewijzing om kenmerkwaarden toe te wijzen aan de overeenkomstige knoopeigenschappen.
1. `textprop` kan worden gebruikt voor het serialiseren van de tekstinhoud van een DITA-element naar een node-eigenschap. Bovendien kan de klasse meerdere keren worden gebruikt in een elementtag om de tekstinhoud op meerdere locaties in de gepubliceerde hiërarchie te serialiseren. U kunt ook de locatie en naam van de eigenschap target aanpassen. Bijvoorbeeld:

   ```XML
   <ditaelement>
      <name>title</name>
      <componentpath>foundation/components/title</componentpath>
      <type>STANDALONE</type>
      <target>para</target>
       <textprop>**jcr:title**</textprop>
   </ditaelement>
   ```

   In de bovenstaande elementtoewijzing wordt opgegeven dat de tekstinhoud van het element `<title>` wordt opgeslagen als waarde van een eigenschap met de naam `jcr:title` op het uitvoerknooppunt.

1. `xmlprop` kan worden gebruikt voor het serialiseren van de volledige XML voor een bepaald element aan een knoopbezit. De component kan deze knoopeigenschap vervolgens lezen en aangepaste rendering uitvoeren. Bijvoorbeeld:

   ```XML
   <ditaelement>
       <name>svg-container</name>
      <class>+ topic/foreign svg-d/svg-container</class>
       <componentpath>fmdita/components/dita/svg</componentpath>
       <type>STANDALONE</type>
       <target>para</target>
      <xmlprop>**data**</xmlprop>
   </ditaelement>
   ```

   In de bovenstaande elementtoewijzing wordt opgegeven dat de volledige XML-opmaak voor element `<svg-container>` wordt opgeslagen als waarde van een eigenschap met de naam `data` op het uitvoerknooppunt.

1. Er is een speciale kenmerktoewijzing om wegresolutie in het proces van de outputgeneratie te behandelen. Bijvoorbeeld:

   ```XML
   <attributemap>
      <attribute from="href" to="fileReference" ispath="true" rel="source" />
      <attribute from="height" to="height" />
       <attribute from="width" to="width" />
   </attributemap>
   ```

   Voor het bovenstaande `attributemap` wordt het kenmerk `href` in het DITA-element toegewezen aan een knoopeigenschap met de naam `fileReference` . Nu `ispath` is ingesteld op `true` , wordt dit pad door het productieproces van de uitvoer omgezet en vervolgens ingesteld in de eigenschap node `fileReference` .

   Hoe deze resolutie gebeurt, wordt bepaald op basis van de waarde van het kenmerk `rel` in de kenmerktoewijzing.

   - Als `rel=source` , wordt de waarde van `href` omgezet met betrekking tot het DITA-bronbestand dat momenteel wordt verwerkt. De waarde van `href` wordt omgezet en in de waarde van `fileReference` -eigenschap geplaatst.

   - Als `rel=target` , wordt de waarde van `href` omgezet met betrekking tot de hoofdpublicatielocatie. De waarde van `href` wordt omgezet en in de waarde van `fileReference` -eigenschap geplaatst.

   Als u geen voorbewerking of resolutie wilt toepassen op padkenmerken, hoeft u het kenmerk `ispath` niet op te geven. De waarde wordt ongewijzigd gekopieerd en de component kan de vereiste resolutie uitvoeren.


## DITA-elementschema

Hieronder ziet u een voorbeeld van het DITA-elementschema in het bestand `elementmapping.xml` :

```XML
<ditaelement>        
    <name>element_name</name>    
    <class>element_class</class>    
    <componentpath>fmdita/components/dita/component_name</componentpath>    
    <type>COMPOSITE|STANDALONE</type>     
    <attributeprop>propname_a</attributeprop>      
    <textprop>propname_t</textprop>    
    <xmlprop>propname_x</xmlprop>     
    <xpath>xpath expression string</xpath>     
    <target>head|para</target>     
    <wrapelement>div</wrapelement>     
    <wrapclass>class_name</wrapclass>     
    <attributemap>         
        <attribute from="attrname"         to="propname"         ispath="true|false"         rel="source|target" />    
    </attributemap>    
    <skip>true|false</skip> 
</ditaelement>
```

De volgende lijst beschrijft de elementen in het DITA elementenschema:

| Element | Beschrijving |
|-------|-----------|
| `<ditaelement>` | The top-level node for each mapping element. |
| `<class>` | Het klassenkenmerk van het doel-DITA-element waarvoor u de component schrijft.<br> Het klassenkenmerk voor het DITA-onderwerp is bijvoorbeeld: <br> `- topic/topic` |
| `<componentpath>` | Het CRXDE-pad van de toegewezen AEM-component. |
| `<type>` | Mogelijke waarden:<br> -   **COMPOSITE**: Proces de kindelementen eveneens <br> -   **STANDALONE**: Overslaat verwerking van kindelementen |
| `<attributeprop>` | Wordt gebruikt voor het toewijzen van geserialiseerde DITA-kenmerken en -waarden aan AEM-knooppunten als eigenschap. Als u bijvoorbeeld `<note type="Caution">` -element hebt en de component die voor dit element is toegewezen, `<attributeprop>attr_t</ attributeprop>` heeft, worden het kenmerk en de waarde van het knooppunt geserialiseerd naar de eigenschap `attr_t` van het corresponderende AEM-knooppunt \( `attr_t->type="caution"`\). |
| `<textprop>propname_t</textprop>` | De uitvoer van `getTextContent()` opslaan naar de eigenschap die wordt gedefinieerd door `propname_t.` <br> **Nota:** dit is een geoptimaliseerd bezit. |
| `<xmlprop>propname_x </xmlprop>` | Sparen geserialiseerde XML van deze knoop aan bezit dat door `propname_x.<br> `**wordt bepaald Nota:** Dit is een geoptimaliseerd bezit. |
| `<xpath>` | Als het element van XPath in de elementenafbeelding wordt verstrekt, dan samen met elementnaam en klasse zou de voorwaarde van XPath ook voor de componentenafbeelding moeten worden voldaan om te worden gebruikt. |
| `<target>` | Plaats voor het element DITA in de crx bewaarplaats op gespecificeerde plaats.<br> Mogelijke waarden: <br> - **hoofd**: Onder de hoofdknoop <br> - **tekst**: Onder de paragraafknoop |
| `<wrapelement>` | Het HTML-element waarin de inhoud moet worden verpakt. |
| `<wrapclass>` | De elementwaarde voor de eigenschap `wrapclass.` |
| `<attributemap>` | Containerknooppunt met een of meer `<attribute>` knooppunten. |
| `<attribute from="attrname" to="propname" ispath="true\|false" rel="source\|target" />` | Wijst de DITA-kenmerken toe aan AEM-eigenschappen: <br> -   **`from`**: DITA-kenmerknaam <br> -   **`to`**: AEM-componenteigenschap name <br> -   **`ispath`**: Als het attribuut een wegwaarde \ is (bijvoorbeeld: *beeld* \) <br> -   **`rel`**: als het pad de bron of het doel is <br> **Nota:** als `attrname` met `%` begint, dan kaart `attrname minus '%'` aan steun &#39; `propname`&#39;. |

**Extra nota&#39;s**

- Als u de standaardelement-toewijzing wilt overschrijven, wordt u aangeraden de wijzigingen in het standaard `elementmapping.xml` -bestand niet aan te brengen. Maak een nieuw XML-toewijzingsbestand en plaats het bestand op een andere locatie, bij voorkeur in de aangepaste map voor apps die u maakt.

- In het `elementmapping.xml` -bestand zijn er veel toewijzingsitems die verwijzen naar de component fmdita/components/dita/wrapper. Wrapper is een generische component die relatief eenvoudige concepten DITA gebruikend eigenschappen op hun plaatsknoop teruggeeft om relevante HTML te produceren. De eigenschap `wrapelement` wordt gebruikt om omsluitende tags te genereren en de onderliggende rendering wordt gedelegeerd aan de corresponderende componenten. Dit is handig wanneer u alleen een containercomponent wilt. In plaats van een nieuwe component te maken die een specifieke containertag zoals `div` of `p` rendert, kunt u de component Wrapper met de eigenschappen `wrapelement` en `wrapclass` gebruiken om hetzelfde effect te bereiken.

- Het wordt niet aanbevolen grote hoeveelheden tekst op te slaan in JCR-eigenschappen van String. De geoptimaliseerde berekening van het eigenschapstype bij het genereren van de uitvoer zorgt ervoor dat grote tekstinhoud niet wordt opgeslagen als tekenreekstype. In plaats daarvan, wanneer de inhoud groter dan een bepaalde drempel moet worden bewaard, wordt het type van het bezit veranderd in binair. Door gebrek, wordt deze drempel gevormd aan 512 bytes, maar kan in de Manager van de Configuratie \ (*worden veranderd com.adobe.fmdita.config.ConfigManager* \) door **te veranderen sparen als Binaire Drempel** het plaatsen.

- Als u een deel van \(en niet alle\) van de elementtoewijzingen wilt overschrijven, hoeft u niet het gehele `elementmapping.xml` -bestand te repliceren. U moet een nieuw XML-toewijzingsbestand maken en alleen de elementen definiëren die u overschrijft.

- Nadat u het XML-bestand op de aangepaste locatie hebt gemaakt, werkt u de instelling `Override Element Mapping` in de `com.adobe.fmdita.config.ConfigManager` -bundel bij.


