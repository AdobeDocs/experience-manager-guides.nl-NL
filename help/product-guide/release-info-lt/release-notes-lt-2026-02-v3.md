---
title: Opmerkingen bij de release | Nieuwe functies in de release van februari 2026 met producttraining en leerinhoud
description: Meer informatie over de nieuwe en verbeterde functies in de release van februari 2026 met producttraining en leerinhoud
role: Leader
hidefromtoc: true
source-git-commit: 16e7f12ddc9e72e4344bf98e65718c0f3681b348
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 0%

---

# Release van februari 2026 van producttraining en leerinhoud

In deze releaseopmerking worden de verbeteringen en problemen besproken die in de release van februari 2026 zijn opgelost met betrekking tot producttraining en leerinhoud.

## Nieuwe functieverbeteringen

De volgende functies zijn geïntroduceerd in de release van februari 2026 met producttraining en leerinhoud:

- **Steun voor ondertitels**: U kunt ondertitels aan uw het leren inhoud nu toevoegen gebruikend nieuwe **ondertitel** optie toevoegen in **eigenschappen van het Dossier**. Dit verbetert de helderheid en verbetert de zoekbaarheid in de cursusinhoud.

  Voor meer details, mening [ voeg titel en ondertitel aan het leren inhoud ](../learning-content/lc-basic-blocks.md#add-title-and-subtitle-to-learning-content) toe.

  ![](assets/add-subtitles.png)

- **laat of maak definitief negatief het scoren** toe onbruikbaar: Terwijl het vormen quizeigenschappen, kunt u negatief het scoren controleren gebruikend **toestaan negatieve definitieve score** optie. Als deze optie is ingeschakeld, behalen studenten een minimale eindscore van nul, zelfs als een negatieve markering is toegepast. Zo blijven studenten gemotiveerd door ervoor te zorgen dat de score nooit onder nul daalt.

  Leer meer over [ eigenschappen van de Quiz ](../learning-content/quiz-properties.md).

  ![](assets/negative-scores-lc.png)

- **schrapt widgets met de rechtermuisknop aanklikken**: Naast het schrappen van quizvragen, kunt u widgets zoals Accordeons, Kaarten van de Tik, en andere widgets met **met de rechtermuisknop aanklikken > punt van de Schrapping** nu schrappen. Deze verhoging breidt de bestaande *vraag* functionaliteit van de Schrapping tot widgets uit, toestaand u om hen met minder kliks en minimale navigatie te verwijderen.

  Leer meer over [ Interactieve widgets van het Gebruik ](../learning-content/lc-widgets.md).

  ![](assets/delete-widget-items.png)
- **Vastzetten antwoordkeuzen**: U kunt specifieke antwoordkeuzen nu vastzetten zodat hun positie onveranderd blijft, zelfs wanneer de antwoorden tijdens SCORM outputgeneratie willekeurig worden gemaakt. Dit is vooral nuttig voor opties zoals *allen van hierboven* of *niets van hierboven*.

  Leer meer over [ eigenschappen van de Vraag ](../learning-content/quiz-insert-questions.md#question-properties).

  ![](assets/pin-question.png)
- **Kort antwoordtype**: Het Kort antwoordvraagtype staat studenten toe om het gebruiken van korte, beschrijvende alfanumerieke antwoorden in plaats van het selecteren van vooraf bepaalde opties te antwoorden. Met dit vraagtype worden studenten aangemoedigd om hun begrip in hun eigen woorden actief in herinnering te brengen en te verwoorden, waardoor beoordelingen aantrekkelijker worden voor studenten.

  Leer meer over [ types van Vraag ](../learning-content/quiz-insert-questions.md#question-types).


  ![](assets/short-answer.png)
- **Opeenvolgende poging voor quizvragen**: U kunt opeenvolgende quizpogingen voor output nu afdwingen SCORM gebruikend de **Leerlingen moeten elke vraag proberen om** optie in SCORM vooraf ingestelde output te werk te gaan. Als deze optie is ingeschakeld, moeten studenten elke vraag beantwoorden voordat ze naar de volgende vraag gaan. De navigatie wordt beperkt tot de huidige vraag is voltooid. Dit zorgt voor een geleide, stapsgewijze evaluatiestroom en een consistente leerervaring.

  Voor meer details, vorm de mening [ output SCORM vooraf ingesteld ](../learning-content/config-scorm-preset.md).

  ![](assets/scorm-general-tab-v3.png)

## Opgeloste problemen

De volgende problemen zijn opgelost in de release van februari 2026 met producttraining en leerinhoud:

- Wanneer het publiceren van de output SCORM en het opstellen van het op ALM, toont het L2 Quiz rapport onjuiste totale en maximumscores voor quiz die veelvoudige pogingen en gerandomiseerde selectie van de vraagbank gebruiken. (GUIDEN-38855)
- Wanneer een cursus op de cloudserver wordt gegenereerd, wordt een onbedoelde witruimte onder de copyrightvoettekst weergegeven vanwege de `coralui3.css` -stijlpagina, wat leidt tot inconsistentie in de lay-out. (GUIDEN-38853)
- Wanneer u via het toetsenbord naar een cursus Leren met een accordeon navigeert, wordt het plusteken (+) of de tabtitel niet gemarkeerd, waardoor het actieve element niet visueel kan worden geïdentificeerd. (GUIDEN-38852)
- Voor cursussen die worden gegenereerd met de SCORM-sjabloon voor koolstof of de standaardsjabloon, worden koppelingen die navigatie voorkomen, niet weergegeven in de inhoudsopgave (menu Cursus) wanneer ze worden geopend op een mobiel apparaat in de liggende modus. (GUIDEN-38851)
- Wanneer u de hiërarchie voor een cursus in Experience Manager Guides dupliceert, moet u eerst een Leergroep maken voordat u een Leerobject kunt maken, omdat toevoegingen op objectniveau niet worden ondersteund. (HULPLIJNEN-38849)
- Pogingen om tot de dropdown opties in Gelijke het volgende vraagtype toegang te hebben gebruikend het toetsenbord ontbreken aangezien de opties niet aan lusje of pijlsleutel verhinderen navigatie antwoorden. (GUIDEN-38985)
- Als u een voorinstelling voor een kopstijl toepast, verdwijnt de geselecteerde tekst. De tekenkleur verandert in wit, waardoor de tekst niet-selecteerbaar en niet zichtbaar is. (GUIDEN-39981)
- Als u Experience Manager Guides gebruikt op Mozilla Firefox, wordt de tekst aan de voorzijde na het spiegelen achteruit weergegeven met de Flip-kaart. (GUIDEN-39983)
- Wanneer u op de inhoudsopgave in het linkerdeelvenster voor de cursus klikt, wordt in de cursus nog steeds een voltooiingsstatus weergegeven, zelfs als de quiz is mislukt. (HULPLIJNEN-40398)
- Als u probeert om het volgende vraagtype in een quiz op een onjuiste manier in ALM weer te geven, worden de geselecteerde opties niet in het rapport weergegeven. (HULPLIJNEN-38640)
- Bij het genereren van de PDF-uitvoer blijven de toegepaste ontwerpstijlen niet behouden, wat resulteert in inconsistenties in het ontwerp. (GUIDEN-38642)

