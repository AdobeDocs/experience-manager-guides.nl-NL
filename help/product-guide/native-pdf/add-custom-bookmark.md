---
title: Native PDF Publish-functie | Een aangepaste bladwijzer toevoegen in PDF-uitvoer
description: Leer hoe u gebruiksstijlen maakt en stijlen voor uw inhoud maakt.
exl-id: 6e6dbba3-da41-4066-b7b2-735a3d92b70a
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# Een aangepaste bladwijzer toevoegen in PDF-uitvoer

Over het algemeen wordt de inhoudsopgave in een DITA-kaart gerepliceerd als bladwijzers in de uiteindelijke PDF-uitvoer. Deze TOC wordt gecreeerd van de onderwerp of sectietitels in uw kaart DITA. Soms wilt u een aangepaste bladwijzer toevoegen aan een bepaalde inhoud in uw PDF-uitvoer, zodat u gemakkelijk kunt navigeren. Dit kan worden bereikt door een `outputclass` -kenmerk toe te voegen aan het element en er het volgende kenmerk op toe te passen:

`bookmark-level: 3`

Hier is `bookmark-level` een kenmerk en is het getal `3` de waarde die het niveau in de bladwijzerhiërarchie aangeeft waar de bladwijzer wordt toegevoegd. In het volgende voorbeeld heeft het onderwerp &#39;Contacten&#39; op het eerste niveau een tabel, &#39;Lijst met contactpersonen&#39;, waaraan we een `outputclass` -kenmerk met de waarde van `custom-bookmark` hebben toegevoegd.


<img src="./assets/custom-bookmark-attribute.png" width="500">

De volgende definitie van de klasse `custom-bookmark` wordt toegevoegd aan het CSS-bestand:

```css
…
/*Adding a custom bookmark*/
.custom-bookmark{
    bookmark-level: 2
}
…
```

In de output van PDF, wordt de *lijst van het Contact* toegevoegd op het tweede niveau in de PDF bladwijzerlijst, zoals hieronder getoond:

<img src="./assets/custom-bookmark-in-pdf-output.png" width="500">

>[!NOTE]
>
>U moet het juiste niveau kiezen waar de aangepaste bladwijzer wordt toegevoegd. Als u een getal opgeeft dat kleiner is dan de bladwijzer van het bovenliggende onderwerp, neemt de aangepaste bladwijzer de positie van de bovenliggende bladwijzer en worden alle andere bladwijzers als onderliggende bladwijzers weergegeven. Dit kan tot onverwachte bladwijzerstructuur leiden.
