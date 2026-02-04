---
title: Componenttoewijzing voor AEM Sites
description: Meer informatie over componenttoewijzing voor AEM Sites
feature: Installation
role: Admin
level: Experienced
source-git-commit: 2b29c0a4a9c7be4a8dcf1110f31912be712eb47a
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---

# Componenttoewijzing voor AEM Sites (met samengestelde componenttoewijzing)

In het artikel wordt gesproken over de verschillende aspecten van componenttoewijzing voor AEM-sites (met samengestelde componenttoewijzing).

## Componenttoewijzingsregels

Gebruik een JSON-array met regels (uw `componentmapping.json` ) om HTML om te zetten in componenten. Houd de regels zo eenvoudig, expliciet en specifiek mogelijk.

### Het HTML-element en de bijbehorende klasse als doel instellen

- Schrijf de naam van de HTML-tag in `name` .
- Neem de CSS-klasse die op dat element is toegepast op in `class` als de klasse bestaat.
Voorbeeld:

  ```html
  <div class ="sample-class">
  <p> Sample html element </p>
  </div>
  ```

  ```json
  {
  "name": "div",
  "class": "sample-class",
  "resourceType": "guides-components/components/table",
  "attributeMap": []
  }
  ```

Zorg bij het definiëren van de bovenstaande elementen voor het volgende:

- `name` kan een door komma&#39;s gescheiden lijst zijn (bijvoorbeeld `"h1, h2"` ).
- `class` moet aanwezig zijn op het element (alle vermelde klassen moeten overeenkomen).
- `resourceType` geeft aan dat u de component `table` wilt gebruiken. Het pakket `guides-components` is een OOTB dat wordt geleverd door hulplijnen. U kunt desgewenst ook andere componentpakketten gebruiken, zoals `core/wcm/` .

### attributeMap gebruiken om eigenschappen op te slaan op de JCR-node

Voeg items toe aan `attributeMap` om eigenschappen voor het uitvoerknooppunt in te stellen. Elk item produceert `attrs[to] = value` .
Algemene patronen:

```json
// copy an attribute
{ "attribute": "src", "to": "image-src" }
// read content or tag name
{ "from": "textContent", "to": "jcr:title" }
{ "from": "outerHTML",  "to": "text" }
{ "from": "innerHTML",  "to": "text" }
{ "from": "name",       "to": "type" }  // the tag name, e.g., "h2"
// constant value
{ "value": true, "to": "textIsRich" }
```

Hieronder ziet u een voorbeeld voor HTML naar JSON voor een afbeeldingselement.

```html
<img src="sample.png" class="cmp-image__image" itemprop="contentUrl" data-cmp-hook-image="image" alt="">
```

```json
{
    "name": "img",
    "resourceType": "core/wcm/components/image/v2/image",
    "attributeMap": [
      {
        "from": "src",
        "to": "fileReference"
      },
      {
        "value": ["fileReference"],
        "to": "path-attributes"
      }
    ]
  }
```

### Paden normaliseren via een toegewezen item

Als u (absolute) waarden wilt normaliseren, verklaar welke attributensleutels zouden moeten worden genormaliseerd gebruikend:

```json
{
  "value": ["text"],
  "to": "path-attributes"
}
```

Zorgen voor de volgende belangrijke punten:

- Plaats de lijst met namen van eigenschappen die u wilt normaliseren in `value` (bijvoorbeeld `["text"]` of `["href", "src"]` ).
- Het systeem zal om het even welke waarden normaliseren die onder die bezitsnamen worden gevonden wanneer het bouwen van de definitieve component.


### HTML-waarden extraheren voordat deze worden gesplitst in componenten

Met `from` kunt u opgeven hoe een waarde uit het element moet worden gelezen voordat het document in afzonderlijke componenten wordt gesplitst:

- `"textContent"`: onbewerkte tekst van het element
- `"outerHTML"`: het element en de binnenste markering
- `"innerHTML"`: alleen de binnenste markering van het element
- Een andere tekenreeks: wordt behandeld als een kenmerknaam (bijvoorbeeld `"src"`, `"href"` )


Voorbeelden:

```json
{ "from": "textContent", "to": "jcr:title" }
{ "from": "outerHTML",  "to": "text" }
{ "from": "innerHTML",  "to": "snippet" }
{ "from": "src",        "to": "image#src" }
```

### Minimale voorbeeld van begin tot eind in component entmapping.json

```json
[
  {
    "name": "h1, h2",
    "class": "topic-title",
    "resourceType": "core/wcm/components/title/v2/title",
    "attributeMap": [
      { "from": "textContent", "to": "text" },
      { "from": "name",        "to": "type" }
    ]
  },
  {
    "name": "img",
    "class": "hero",
    "resourceType": "weretail/components/content/heroimage",
    "attributeMap": [
      { "from": "src", "to": "image#src" },
      { "value": ["image#src"], "to": "path-attributes" }
    ]
  },
  {
    "name": "#element",
    "resourceType": "core/wcm/components/text/v2/text",
    "attributeMap": [
      { "from": "outerHTML", "to": "text" },
      { "value": true,        "to": "textIsRich" }
    ]
  }
]
```

Definieer het element en de klasse waarop u wilt toepassen, gebruik `attributeMap` om de knoopeigenschappen in te stellen, voeg een `path-attributes` -item toe om paden te normaliseren en kies de juiste `from` waarden voor de waarden die u wilt extraheren. De `heroimage` die hierboven wordt gebruikt, is een component in een `we-retail` -site.

**Nota**: Het is belangrijk om de standaard rijke tekst te bespreken en de elementen te identificeren waarvoor het wordt gebruikt.

## Een aangepaste component maken

Leer hoe u een aangepaste tabelcomponent maakt die afbeeldingen in de bijbehorende cellen weergeeft. Deze aanpak garandeert een schoon, herbruikbaar ontwerp voor dynamische inhoud. Het omvat wat u zult bouwen, waarom het efficiënt is, de belangrijkste eerste vereisten, ontwerp op hoog niveau, en meer.

### Wat u gaat bouwen

Een aangepaste tabelcomponent die HTML-tabelinhoud accepteert en elke `<img>` binnenin deze component vervangt door de uitvoer van de AEM Core Image-component. Zo kunt u de functies van Core Image (responsieve afbeeldingen, alt-verwerking, toegankelijkheid) opnieuw gebruiken en de volledige controle over de tabelmarkeringen behouden.
Op deze manier kunt u andere aangepaste componenten voor uw AEM-site maken (met samengestelde componenttoewijzing).

### Waarom deze aanpak

- **hergebruik**: Het volwassen gedrag van het Beeld van de Kern van de hefboomwerking in plaats van het opnieuw uit te voeren.
- **Consistentie**: De beelden in uw lijst gedragen zich het zelfde als beelden elders op de plaats.
- **server-kant**: De beelden worden teruggegeven op de server voor prestaties, SEO, en toegankelijkheid.

### Vereisten

- AEM SDK loopt en dit project is uitgecheckt.
- Basiscomponenten die op uw AEM-instantie zijn geïnstalleerd.
- Beschikbaar gemaakt voor het bouwen en implementeren.

### Ontwerp op hoog niveau

- Auteur biedt HTML voor de tabel in het dialoogvenster Component.
- Een Sling Model parseert die HTML, vindt `<img>` markeringen, en voor elke beeld roept een dienst aan die de de componentenserver-kant van het Beeld van de Kern teruggeeft.
- Het model vervangt het origineel `<img>` door de vastgelegde Core Image HTML en geeft de voltooide HTML door aan HTML voor uitvoer.

Uw tabel wordt één keer uitgevoerd en bevat al de markering Core Image. Er is geen client-side DOM-manipulatie nodig.

### Mapstructuur en sleutelbestanden (in dit antwoord)

- Component HTL en clientlibs: `ui.apps/src/main/content/jcr_root/apps/guides-components/components/table/`
   - `table.html` (HTML-renderer)
   - `_cq_editConfig.xml` (listeners vernieuwen)
   - `clientlibs/` with `css.txt` , `js.txt` , `css/table.css` , `js/table.js`
- Sling-model: `core/src/main/java/com/adobe/guides/aem/components/core/models/TableModel.java`
- Renderservice afbeelding: `core/src/main/java/com/adobe/guides/aem/components/core/services/ImageComponentRenderer.java`

### Implementatiestappen

**bepaalt de component van de Lijst (componentenknoop)**

Maak de component onder `apps/guides-components/components/table` . Als u er nog geen hebt, voegt u een minimale `.content.xml` zoals hieronder toe om deze in het zijpaneel te registreren.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:sling="http://sling.apache.org/jcr/sling/1.0"
          xmlns:jcr="http://www.jcp.org/jcr/1.0"
          jcr:primaryType="cq:Component"
          jcr:title="Table"
          componentGroup="Guides - Custom"/>
```

Geeft aan AEM door dat dit een component is die auteurs kunnen toevoegen aan pagina&#39;s.

**geeft met HTML terug en omvat stijlen**

Gebruik een verkoopmodel en voer de verwerkte HTML uit. Neem de clientlib-categorie op voor CSS/JS.

```html
<sly data-sly-use.model="com.adobe.guides.aem.components.core.models.TableModel"
     data-sly-use.clientLib="/libs/granite/sightly/templates/clientlib.html">
</sly>
<sly data-sly-call="${clientLib.css @ categories='guides-components.table'}"></sly>
<sly data-sly-test="${wcmmode.edit && !model.hasContent}">
  <div class="cq-placeholder" data-emptytext="${component.title}"></div>
</sly>
<div data-sly-test="${model.hasContent}"
     class="gu-table-wrapper ${model.enableResponsive ? 'gu-table--responsive' : ''} gu-table--style-${model.tableStyle}"
     id="${model.componentId}">
  ${model.processedTableHtml @ context='unsafe'}
</div>
```

Het model retourneert complete HTML met Core Image al gerenderd, dus HTL drukt deze gewoon af.

**voeg het het Verdelen Model toe om HTML te verwerken en het Beeld van de Kern terug te geven**

Het model leest dialooggebieden, ontleedt de lijst HTML, vindt elk `<img>`, en vervangt het met het Beeld van de Kern HTML via de dienst.

Hier volgen enkele belangrijke kennis van `TableModel` :

- Leest `tableHtml` , `enableResponsive` , `tableStyle` uit resource-eigenschappen.
- Gebruikt Jsoup om HTML veilig te parseren en te bewerken.
- Roept `ImageComponentRenderer` aan om het Beeld van de Kern terug te geven en de HTML te vangen.
- Behoudt CSS-klassen en -stijl van het origineel `<img>` .
- Normaliseert DAM-paden (verwijdert `/jcr:content/renditions/*` ).

```java
@Model(adaptables = {Resource.class, SlingHttpServletRequest.class},
       defaultInjectionStrategy = DefaultInjectionStrategy.OPTIONAL)
public class TableModel {
  @ValueMapValue private String tableHtml;
  @ValueMapValue private boolean enableResponsive;
  @ValueMapValue private String tableStyle;
  @OSGiService private ImageComponentRenderer imageRenderer;
  // ...
  @PostConstruct
  protected void init() {
    // parse HTML, for each <img> build image props (fileReference, alt, title)
    // call imageRenderer.renderImageComponent(...)
    // replace <img> with returned Core Image HTML
  }
  public String getProcessedTableHtml() { /* return final HTML */ }
}
```

Dit centraliseert de logica op de server en gebruikt het gedrag van het Beeld van de Kern opnieuw.

**geeft het Beeld van de Kern via de dienst terug (server-kant omvat)**

`ImageComponentRenderer` rendert de component Core Image en legt de uitvoer vast. IT

- verpakt een bron die `core/wcm/components/image/v2/image` afdwingt.
- gebruikt `RequestDispatcher#include` om het te renderen.
- vangt de reactie als koord.

```java
@Component(service = ImageComponentRenderer.class)
public class ImageComponentRenderer {
  private static final String IMAGE_RESOURCE_TYPE = "core/wcm/components/image/v2/image";
  public String renderImageComponent(Resource base, Map<String,Object> props,
                                     SlingHttpServletRequest req, SlingHttpServletResponse resp) {
    // create wrapped resource with IMAGE_RESOURCE_TYPE and props
    // dispatcher.include(...) with a response wrapper to capture HTML
    // return captured HTML
  }
}
```

Dit laat u **in** Beeld van de Kern vallen waar u het, niet alleen als kindcomponent nodig hebt.

**de bibliotheken van de Cliënt**

Maak een clientlib voor kleine stijlen of toekomstige JS. De HTML boven laadt de categorie `guides-components.table` .

```java
clientlibs/css.txt
  #base=css
  table.css
clientlibs/js.txt
  #base=js
  table.js
  
```

Zo blijven de stijlen/scripts modulair en kunnen ze worden gedetecteerd.

**de gebieden van de Dialoog (de input van de Auteur)**

Voeg een dialoogvenster toe met ten minste de volgende eigenschappen:

- **Lijst HTML**: `./tableHtml` (textarea); HTML van de lijst.
- **laat ontvankelijke** toe: `./enableResponsive` (checkbox); knevels een ontvankelijke omslagklasse.
- **stijl van de Lijst**: `./tableStyle` (uitgezocht); past een klasse van de stijlbepaling toe.

Deze kaart 1 :1 aan de eigenschappen van het Sling Model en controle het teruggeven.

**sta de component op malplaatjes toe**

In de Redacteur van het Malplaatje, geef het beleid van de Container van de Lay-out uit > Toegestane Componenten > laat uw component van de Lijst onder **Gidsen - Douane** toe.

Auteurs kunnen geen componenten toevoegen tot het beleid hen toestaat.

## Tips voor ontwerpen

- Plak geldige HTML voor de tabel. Het model maakt en past afbeelding-URL&#39;s aan.
- Gebruik DAM-middelenpaden voor afbeeldingen; uitvoeringen worden genormaliseerd ten opzichte van het oorspronkelijke middelenpad.
- Geef waar mogelijk alternatieve tekst op in de HTML, anders worden afbeeldingen gemarkeerd als decoratief.

## Restricties

- De service forceert Core Image v2. Werk `IMAGE_RESOURCE_TYPE` bij om te wisselen tussen versies.
- Voor synthetische rendering vervangt het model de gegenereerde `.coreimg.` URL&#39;s van Core Image door directe DAM-paden en verwijdert `srcset` om verbroken URL&#39;s te voorkomen.
- Alle rendering vindt eenmaal plaats op de server. JavaScript is optioneel.

## Snelle referentie (implementatie)

- HTML: `ui.apps/.../components/table/table.html`
- Clientlibs: `ui.apps/.../components/table/clientlibs/`
- Model: `core/.../models/TableModel.java`
- Service: `core/.../services/ImageComponentRenderer.java`

Dit patroon toont hoe te om een douanecomponent met een server-kant van de Component van de Kern samen te stellen, die uw prijsverhoging terwijl het hergebruiken van de logica van de Kern houdt.
