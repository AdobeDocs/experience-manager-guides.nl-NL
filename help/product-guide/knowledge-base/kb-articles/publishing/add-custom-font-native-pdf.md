---
title: Aangepaste lettertypen toevoegen aan uw DITA PDF
description: Aangepaste lettertypeintegratie bereiken om de merkidentiteit en visuele consistentie in al uw inhoud in Native DITA PDF's te versterken.
feature: Native PDF Output
author: Pulkit Nagpal(punagpal)
role: User, Admin
exl-id: 151e3b1c-6340-4ff2-84d4-246bc4b68065
source-git-commit: 9c53ac725618db1164b0ed310a47b258a7224778
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Aangepaste lettertypen toevoegen aan uw eigen DITA PDF

## Dit artikel betreft:

Het aangepaste lettertype toevoegen om de merkidentiteit en visuele consistentie in al uw inhoud te versterken.

Dit proces omvat drie stappen:

- [Het aangepaste lettertype uploaden](#step-1--upload-the-custom-font-to-the-resource-folder-of-your-template)
- [Breng de gewenste wijzigingen aan in de stijlpagina van de PDF-sjablonen](#step-2--make-necessary-changes-in-pdf-templatess-stylesheet)

- [Gebruikte lettertypen insluiten (optioneel)](#step-3-optional--embed-used-font-in-pdf)

## Stap 1: Upload het douanedoopvont aan de middelomslag van uw malplaatje

![&#x200B; Aangepaste upload en import van lettertypen &#x200B;](../assets/publishing/custom-font1.png)

## Stap 2: Breng de noodzakelijke wijzigingen aan in het stijlblad van PDF-sjablonen

![&#x200B; Lettertype in stijlblad van PDF-sjabloon &#x200B;](../assets/publishing/custom-font2.png)

## Stap 3 (Optioneel): gebruikt lettertype insluiten in PDF

![&#x200B; Aangepast font dat is ingesloten in DITA PDF &#x200B;](../assets/publishing/custom-font3.png)

## Veelgestelde vragen

### Mag ik Adobe Fonts gebruiken?

> Ja, ga naar fonts.adobe.com en klik op Toevoegen aan webproject.
> 
> Importcode kopiëren zoals `" @import url("https://use.typekit.net/xxxx.css")` ;
>
> Plak de inhoud in CSS en wijzig de inhoud in het CSS-bestand.

![&#x200B; de doopvont van de Adobe van het gebruik in DITA PDF &#x200B;](../assets/publishing/custom-font4.png)


### Mijn lettertype wordt niet weergegeven in PDF

> De spelling van de lettertypenaam controleren (meest voorkomende fout)
>
> Zorg ervoor dat u een lettertype insluit als lettertypen niet beschikbaar zijn op het systeem waarop PDF is geopend

## Voor andere vragen contacteer uw respectieve CSMs


## Overige bronnen:

- [Inhoudsopgave van DITA-boekmap opnemen in PDF](./how-to-include-bookmap-toc-in-pdf-publishing.md)
- [Inhoudsopgave opnemen in PDF-publicaties](./how-to-include-bookmap-toc-in-pdf-publishing.md)
- [Expertsessie-video op native PDF](../../expert-sessions/native-pdf-publishing-eamples-part1-june2023.md)
