---
title: Native PDF Publish-functie | Aangepaste stijl toepassen op inhoudsopgave-items en onderwerpinhoud
description: Leer hoe u gebruiksstijlen maakt en stijlen voor uw inhoud maakt.
exl-id: f65c9683-a1fc-432a-854b-83e8f39d7dae
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: db4c823e592e249e1d828a7071fc0848a5e68c0f
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Aangepaste stijl toepassen op inhoudsopgave-items en onderwerpinhoud

Mogelijk wilt u soms aangepaste opmaak toepassen op de inhoudsopgave-items of een bepaald onderwerp. Dit kan worden bereikt door een `outputclass` -kenmerk te koppelen aan het `<topicref>` -element in uw DITA-kaart. Ook, voor het geval u een douaneformaat op een volledig onderwerp wilt toepassen, dan kan dat ook worden bereikt door de de stijldefinitie van de attributen in CSS uit te breiden.

Neem een voorbeeld van een nieuw onderwerp dat u voor overzicht wilt verzenden. Voor een eenvoudige identificatie van het bijgewerkte onderwerp moet u een `outputclass` -kenmerk toevoegen aan het `<topicref>` -element in uw DITA-kaart en vervolgens een aangepaste opmaak voor dit kenmerk definiëren in de CSS.

In het volgende voorbeeld, is de *Geschiedenis van vluchten* onderwerp toegewezen een `outputclass` attribuut met de waarde van `new-topic`.

<img src="./assets/new-topic-attribute-in-map.png" width="500">

Met de klassedefinitie van `new-topic` in een CSS kunt u de stijl definiëren voor de volgende items:
* De belangrijkste vermelding in de inhoudsopgave of de miniinhoudsopgave
* De titel van het onderwerp in de hoofdinhoud
* De volledige inhoud van het onderwerp, inclusief de titel

Zie hoe elk van deze scenario&#39;s in CSS kan worden bepaald. In de volgende CSS-definitie van de `new-topic` -klasse is de tekstkleur gewijzigd.

```css
…
.new-topic {
  color: #CC5309
}
…
```

Deze definitie controleert de kleur van de tekst in TOC en de titel van het onderwerp. In de volgende PDF-uitvoer ziet u de andere kleur die op het inhoudsopgave-item wordt toegepast:

<img src="./assets/pdf-output-toc-entry.jpg" width="500">

De titel van het onderwerp wordt ook opgemaakt met dezelfde kleur.

<img src="./assets/pdf-output-topic-title.jpg" width="500">

Als u de ingang van TOC en de titel van het onderwerp verschillende stijlen wilt hebben, dan kunt u hen afzonderlijk bepalen zoals hieronder getoond:

```css
...
/*for styling TOC entry */
.new-topic {
  color: #CC3509
}

/* for styling topic's title */
.new-topic.title {
  color: #092ACC
}
...
```

Tot slot kunt u stijlen op de volledige inhoud binnen het onderwerp ook toepassen. Voor dit, moet u een achtervoegsel &quot;`-content`&quot;aan de klassennaam toevoegen. In het volgende voorbeeld, is een veranderingsbar toegevoegd op de volledige inhoud van het onderwerp:

```css
...
/* for styling the topic's content */
.new-topic-content {
  -ro-change-bar-color: #A609CC;
}
...
```

Gebruikend de bovengenoemde het stileren attributen, wordt een veranderingsbar toegevoegd links van de *Geschiedenis van vlucht* onderwerp, zoals hieronder getoond:

<img src="./assets/pdf-output-topic-content.jpg" width="500">

## Lege rijen uit de inhoudsopgave verwijderen

Als u de titel voor geen onderwerpen hebt bepaald, verschijnen de lege rijen in TOC voor dergelijke onderwerpen.

Als u de lege rijen uit de inhoudsopgave en de miniinhoudsopgave wilt verwijderen, voegt u de volgende stijl toe in de `layout.css` :

```css
.toc-body a:empty,
.chaptoc-body a:empty {
    display: none;
} 
```

