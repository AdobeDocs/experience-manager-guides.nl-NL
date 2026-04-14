---
title: Publiceren van inhoudsopgave (Inhoudsopgave) met NativePDF
description: Inhoudsopgave en andere boekenlijst voor uw dita-boekmap publiceren met NativePDF
feature: Native PDF Output
author: Pulkit Nagpal(punagpal)
role: User, Admin
exl-id: c551f0a8-f973-4c5a-bd34-f52890a91342
source-git-commit: 9c53ac725618db1164b0ed310a47b258a7224778
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Inhoudsopgave van boekmap genereren in PDF-publicaties

## Uw boekmap instellen

Neem het element `<toc>` op:
Zoek binnen het `<frontmatter>` -element van uw boekmap het `<booklists>` -element.  Een `<toc>` -element op deze manier nesten in `<booklists>` :

```
<frontmatter>
  <booklists>
    <toc/>  <figurelist/>
    <tablelist/>
  </booklists>
</frontmatter>
```

Met de DITA-specificatie kunnen de inhoudsopgave en de opnamelijsten ook in de sectie `<backmatter>` worden geplaatst.


```
<backmatter>
    <booklists>
      <toc/>
      <figurelist/>
      <indexlist/>
    </booklists>
  </backmatter>
```

Voorbeeldstructuur van een boekenkaart met inhoudsopgave, figuurlijst en tabellijst op voorgrond en indexlijst op achtergrond.

```
<bookmap>
  <title>My Bookmap Title </title>
  <frontmatter>
    <booklists>
      <toc/>
      <figurelist/>
      <tablelist/>
    </booklists>
  </frontmatter>

  <chapter href="chapter1.ditamap">
  <chapter href="chapter2.ditamap">
  </chapter>

  <backmatter>
    <booklists>
      <indexlist/>
    </booklists>
  </backmatter>
</bookmap>
```

De inhoudsopgave en de opnamelijsten worden automatisch gegenereerd op basis van de structuur die in uw boekenkaart is gedefinieerd.

Zodra uw boekenkaart opstelling is, gebruik inheemse PDF om de output van PDF te produceren. De bladwijzerstructuur en verwijzingen worden verwerkt, inclusief de inhoudsopgave en de opnamelijsten.

## Ontwerp van inhoudsopgave en de volgorde ervan in PDF

De native PDF-functionaliteit biedt een handige methode voor het aanpassen van de lay-out en het ontwerp van uw inhoudsopgave.

U kunt het ontwerp beheren door de paginalay-out voor de inhoudsopgave en de stijlen te scheiden via layout.css.

Inhoudsopgave en andere volgorde voor opnamelijsten in PDF zijn alleen gebaseerd op de structuur van de boekenkaart.

![ toc ](../assets/publishing/toc.png)


## Veelgestelde vragen

### Hoe te om TOC van een Ditamap in een PDF op te nemen

Ditamaps hebben zelf niet direct een inhoudsopgave (TOC) zoals een boekenkaart. Nochtans, spelen ditamaps een cruciale rol bij het bepalen van de structuur voor uw inhoud en onrechtstreeks bijdragen aan het proces van de Inhoudsopgave.

Als u Ditamap publiceert, biedt Native PDF automatisch functionaliteit voor het genereren van inhoudsopgave en boekenlijst. U kunt het genereren van inhoudsopgave bij ditamap vanuit native PDF-instellingen in- en uitschakelen.

![ laat onbruikbaar maken TOC ](../assets/publishing/pageorder.png) toe

## Aanvullende bronnen:

- [ Inheemse documentatie van de het ontwerppagina van PDF ](https://experienceleague.adobe.com/en/docs/experience-manager-guides/using/install-guide/on-prem-ig/output-gen-config/config-native-pdf-publish/design-page-layout)
- [ Eigen de essentiële elementen van PDF pre-geregistreerde Deskundige zitting ](https://experienceleague.adobe.com/en/docs/experience-manager-guides/using/knowledge-base/expert-session/native-pdf-publishing-essentials-feb23)

<br>
<br>

Plaats op het communautair van AEM Guides [ forum ](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/ct-p/aem-xml-documentation) voor om het even welke vragen.



