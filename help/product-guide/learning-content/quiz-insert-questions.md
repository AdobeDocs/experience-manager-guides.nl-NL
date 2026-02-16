---
title: Vragen invoegen in een quiz
description: Leer hoe u vragen kunt invoegen in een quiz in de producttraining en -training.
feature: Authoring
role: User
exl-id: dff38476-c078-4970-b967-05a902430015
source-git-commit: 1df47cf35590f10bdfe7fdbc3501d7c47137ed56
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Vragen invoegen in een quiz

Voer de volgende stappen uit om vragen in een quiz in te voegen:

1. Kies het gewenste vraagtype van het **drop-down menu van Vragen** in de toolbar. Gebaseerd op uw vereisten, kunt u vragen toevoegen gebruikend om het even welke vier beschikbare formaten: Waar of Onwaar, Enige correct, Meervoudig correct, Gelijke het volgende en Korte antwoord zoals hieronder getoond. Voor meer details, bekijk [&#x200B; types van Vraag &#x200B;](#question-types).

   ![](assets/question-types.png){width="650" align="left"}

   Wanneer u een vraag invoegt, wordt de nieuwe vraag standaard toegevoegd als de cursor zich op een vraagblok bevindt.

   Om een vraag tussen de twee bestaande vragen op te nemen, neem eerst [&#x200B; een paragraaf &#x200B;](#insert-paragraph-within-the-quiz) op, en neem dan vragen op.

1. Een vraag wordt ingevoegd in de geselecteerde indeling. Vervolgens kunt u de vraag op basis van uw vereisten bewerken.

1. U kunt om het even welke vraag selecteren en zijn eigenschappen vormen gebruikend het **eigenschappen van de Inhoud** paneel.

   ![](assets/question-properties.png){width="650" align="left"}

1. Sla alle wijzigingen op die u in de quiz hebt aangebracht.


## Eigenschappen van Vraag

U kunt de vragen vormen gebruikend de volgende vraageigenschappen van het **Eigenschappen van de Inhoud** paneel:

![](assets/question-properties-new.png){width="350" align="left"}

- **Opties**: Specificeer het correcte antwoord van de vraag
- **Identiteitskaart van de Vraag**: Specificeert vraagidentiteitskaart voor elke vraag. Als er geen vraag-id aanwezig is, wordt aangeraden deze altijd toe te voegen.
- **Punten voor correct antwoord**: Specificeer de punten die voor het correcte antwoord moeten worden toegekend.
- **Straal voor onjuist antwoord**: Specificeer de punten die voor een onjuist antwoord moeten worden afgetrokken.
- **Etiket van de Vraag**: Laat toe om een vraagetiket toe te voegen.
- **Terugkoppeling**: Laat toe om te verstrekken terugkoppelt voor correct of onjuist antwoord.
- **Vastzetten optie aan positie**: Wanneer een specifieke optie voor een vraag wordt vastgezet, blijft het vast in de gespecificeerde positie in de optielijst, zelfs als **antwoordkeuzen van willekeurig formaat voor elke poging** in de SCORM vooraf ingestelde configuratie wordt toegelaten, die anders de beschikbare opties zou veranderen. U kunt de muisaanwijzer boven de gewenste optie voor een vraag plaatsen in het deelvenster Eigenschappen van inhoud en deze vastzetten.

  ![](assets/pin-question.png){width="350" align="left"}

## Alinea invoegen in de quiz

Wanneer u de cursor op een bepaalde vraag of op een lege ruimte tussen de twee vragen plaatst, wordt een blauwe horizontale lijn weergegeven met een blauwe pijl in de rechterbovenhoek van het scherm. Als u de blauwe pijl selecteert, kunt u een alinea in de quizontwerpinterface invoegen.

![](assets/insert-paragraph-here-arrow.png){width="650" align="left"}

- Als u deze optie gebruikt in een vraag, kunt u meer elementen toevoegen, zoals afbeeldingen, tabellen, tekstelementen en meer in de vraag.
- Wanneer u deze vragen met elkaar verbindt, kunt u een andere vraag invoegen of andere ontwerpelementen toevoegen, zoals hierboven vermeld.

## Vraag of optie verwijderen

Voer de volgende stappen uit om een vraag of specifieke optie uit een quiz te verwijderen:

1. Klik met de rechtermuisknop op de vraag of de optie die u wilt verwijderen.
1. In het contextmenu, uitgezochte **vraag van de Schrapping** (om de volledige vraag te verwijderen) of **optie van de Schrapping** (om slechts de geselecteerde optie te verwijderen).

![](assets/delete-options-lc.png){width="650" align="left"}

## Vraagtypen

De volgende vraagtypen worden ondersteund in een quiz:

- **Enige correct**: Een vraag met veelvoudige opties waar slechts één antwoord correct is.

  ![](assets/single-correct.png){width="650" align="left"}

- **Waar/Vals**: Een op verklaring-gebaseerde vraag waar de studenten kiezen of het Waar of Vals is.

  ![](assets/true-false.png){width="650" align="left"}


- **Meerdere correcte**: Een vraag met veelvoudige opties waar meer dan één antwoord correct kan zijn.

  ![](assets/multi-correct.png){width="650" align="left"}

- **Gelijke de volgende** aan: Staat studenten toe om punten van twee lijsten aan vorm correcte paren aan te passen. U kunt nieuwe optiesreeksen van het **eigenschappen van de Inhoud** paneel toevoegen. Om de complexiteit te vergroten, kunt u één optie uit de eerste lijst verwijderen en een extra overeenkomst opnemen in de kolom Overeenkomst. Dit leidt tot een element van moeilijkheid door studenten te vereisen om kritisch te denken over welke optie geen direct paar heeft.

  ![](assets/match-the-following.png){width="650" align="left"}

  In de gepubliceerde output, **gelijke de volgende** vraag verschijnt met dropdown menu voor elk punt, toestaand u om de correcte gelijke van de beschikbare opties te selecteren.

  ![](assets/question-type-publishing.png){width="650" align="left"}


- **Kort antwoord**: Staat studenten toe om het gebruiken van een korte tekstinput te antwoorden. Alfanumerieke antwoorden worden geaccepteerd, reacties worden niet hoofdlettergevoelig weergegeven en voor zeer lange antwoorden wordt een horizontale schuifbalk weergegeven.

  ![](assets/short-answer.png){width="650" align="left"}
