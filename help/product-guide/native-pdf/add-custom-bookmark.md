---
title: Systeemeigen PDF-publicatiefunctie | Een aangepaste bladwijzer toevoegen in PDF-uitvoer
description: Leer hoe u gebruiksstijlen maakt en stijlen voor uw inhoud maakt.
exl-id: 6e6dbba3-da41-4066-b7b2-735a3d92b70a
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 1c96f25c3b970d04d23e8faf94a8f39095f6bd2c
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Een aangepaste bladwijzer toevoegen in PDF-uitvoer

Over het algemeen, wordt TOC in een kaart DITA herhaald als referenties in de definitieve output van PDF, met inbegrip van de **Inhoud** titel die de pagina opent van TOC wanneer geselecteerd. Deze TOC wordt gecreeerd van de onderwerp of sectietitels in uw kaart DITA.

Soms wilt u een aangepaste bladwijzer toevoegen aan een bepaalde inhoud in de PDF-uitvoer voor eenvoudige navigatie. Dit kan worden bereikt door een `outputclass` -kenmerk toe te voegen aan het element en er het volgende kenmerk op toe te passen:

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

In de output van PDF, wordt de *lijst van het Contact* toegevoegd op het tweede niveau in de bladwijzerlijst van PDF, zoals hieronder getoond:

![](assets/custom-bookmark-in-pdf-output.png) {width="300" align="left"}

>[!NOTE]
>
>U moet het juiste niveau kiezen waar de aangepaste bladwijzer wordt toegevoegd. Als u een getal opgeeft dat kleiner is dan de bladwijzer van het bovenliggende onderwerp, neemt de aangepaste bladwijzer de positie van de bovenliggende bladwijzer en worden alle andere bladwijzers als onderliggende bladwijzers weergegeven. Dit kan tot onverwachte bladwijzerstructuur leiden.

**het Verwijderen van de titel van Inhoud van de de outputreferenties van PDF**

Als u niet de **titel van de Inhoud** in de output van PDF wilt omvatten, kunt u het verwijderen door **Inhoud** binnen `<p>` element in plaats van `<h1>` element te plaatsen.

Het proces voor het stapsgewijs verwijderen van de titel Inhoud uit bladwijzers is als volgt:

1. Open de PDF-sjabloon die u gebruikt voor de PDF-uitvoer.
2. Open de **pagina van TOC** binnen **Lay-outs van de Pagina**.
De pagina van TOC wordt getoond op het recht.
3. Schakelaar aan de **Source** wijze en verander het element waar de Inhoud van `<h1>` aan `<p>` wordt gevestigd.

Voor de wijziging:

```
<h1 class="toc-title">Contents</h1>
```

Na de wijziging:

```
<p class="toc-title">Contents</p>
```

Sla de wijzigingen op en genereer de uitvoer opnieuw.





