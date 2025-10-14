---
title: Aangepaste lettertypen toevoegen aan uw DITA-PDF
description: Zorg voor integratie van aangepaste lettertypen om uw merkidentiteit en visuele consistentie in al uw inhoud in Native DITA-PDF te versterken.
feature: Native PDF Output
author: Pulkit Nagpal(punagpal)
role: User, Admin
source-git-commit: 518bec870dc07e88a422d889a1c54be26c248799
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Aangepaste lettertypen toevoegen aan uw eigen PDF van DITA

## Dit artikel betreft:

Het aangepaste lettertype toevoegen om de merkidentiteit en visuele consistentie in al uw inhoud te versterken.

Dit proces omvat drie stappen:

- [Het aangepaste lettertype uploaden](#step-1--upload-the-custom-font-to-the-resource-folder-of-your-template)
- [Breng de gewenste wijzigingen aan in het stijlblad van de sjablonen PDF](#step-2--make-necessary-changes-in-pdf-templatess-stylesheet)

- [Gebruikte lettertypen insluiten (optioneel)](#step-3-optional--embed-used-font-in-pdf)

## Stap 1: Upload het douanedoopvont aan de middelomslag van uw malplaatje

![&#x200B; Aangepaste upload en import van lettertypen &#x200B;](../assets/publishing/custom-font1.png)

## Stap 2: Breng noodzakelijke veranderingen in de stijlpagina van PDF malplaatjes aan

![&#x200B; Gezicht van de doopvont in PDF stylesheet &#x200B;](../assets/publishing/custom-font2.png)

## Stap 3 (optioneel): gebruikt lettertype insluiten in PDF

![&#x200B; De doopvont van de Douane die in PDF DITA inbedt &#x200B;](../assets/publishing/custom-font3.png)

## Veelgestelde vragen

- ### Mag ik Adobe Fonts gebruiken?

> Ja, ga naar fonts.adobe.com en klik op Toevoegen aan webproject.
> 
> Importcode kopiëren zoals `" @import url("https://use.typekit.net/xxxx.css")` ;
>
> Plak de inhoud in CSS en wijzig de inhoud in het CSS-bestand.

![&#x200B; het doopvont van de Adobe van het gebruik in PDF DITA &#x200B;](../assets/publishing/custom-font4.png)


- ### Mijn lettertype wordt niet weergegeven in PDF

> De spelling van de lettertypenaam controleren (meest voorkomende fout)
>
> Zorg ervoor dat u een lettertype insluit als lettertypen niet beschikbaar zijn op het systeem waar PDF is geopend

- ## Voor andere vragen contacteer uw respectieve CSMs


## Overige bronnen:

- [Hoe te om TOC van DITA Bookmap in PDF te omvatten](./how-to-include-bookmap-toc-in-pdf-publishing.md)
- [Inhoudsopgave opnemen in PDF-publicatie](./how-to-include-bookmap-toc-in-pdf-publishing.md)
- [Expertsessie-video op native PDF](../../expert-sessions/native-pdf-publishing-eamples-part1-june2023.md)