---
sidebar_position: 8
source-git-commit: eb3fe92d36bc58a11e47f786a10d5938e2ed0184
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---


# Voorbeelden

In dit pakket hebben we ook enkele aanpassingsvoorbeelden (beschikbaar op `guides_extension/src` ) gegeven. Hieronder vindt u een korte beschrijving van elk van deze aspecten.

1. [ Contextmenu ](./../../src/file_options.ts)
In dit voorbeeld hebben we het contextmenu van `file_options` aangepast om de opties `Delete` en `Edit` te verwijderen en de optie `Duplicate` te vervangen door een optie `Download` .

2. [ Linkerpaneel ](../../src/left_panel_container.ts)
In dit voorbeeld hebben we de `left tab panel` aangepast zodat er nog een `tab` EXTENSION met de naam TEST en een bijbehorende `tab panel` met een label is: `Test Tab Panel`

3. [ Juiste Comité ](../../src/right_panel_container.ts)
In dit voorbeeld hebben we de `right tab panel` aangepast zodat er nog een `tab` EXTENSION met de naam TEST is en een bijbehorende `tab panel` met een label: `New Tab Panel`

4. [Deelvenster Opslagplaats](../../src/repository_panel.ts)

5. [ Toolbar ](../../src/toolbar.ts)
In dit voorbeeld hebben we de knoppen `Insert Element`, `Insert Paragraph`, `Insert Numbered List` en `Insert Bulleted List` vervangen door één knop `More Insert Options` die al deze knoppen bevat.

[ de Voorbeelden van de Overzicht App ]

1. [ Toolbox van de Annotatie ](../../src/review_app_examples/annotation_extension.ts)
In dit voorbeeld hebben we een andere knop toegevoegd aan de gereedschapset voor annotaties waarmee het huidige revisieonderwerp in AEM wordt geopend.

2. [ Commentaar van het Overzicht ](../../src/review_app_examples/review_comment.ts)
In dit voorbeeld hebben we de gebruikersnaam vervangen door gebruikersgegevens (bestaande uit de volledige naam en titel van de opmerking), een unieke opmerking-id, een mailpictogram en invoervelden toegevoegd voor het vermelden van de ernst en de motivering van de opmerking.
Er is ook een knop `accept with modification` toegevoegd aan opmerkingen aan de zijde van XMLEditor waarmee een dialoogvenster wordt geopend.

3. [ Antwoord van de Commentaar ](../../src/review_app_examples/comment_reply.ts)
In dit voorbeeld hebben we de gebruikersnaam vervangen door gebruikersgegevens (bestaande uit de volledige naam en titel van de opmerking) en een pictogram mailto toegevoegd aan de koptekst van de opmerking.

4. [ Inline het Comité van het Overzicht ](../../src/review_app_examples/inline_review_panel.ts)
In dit bestand berekenen en toewijzen we de unieke opmerking-id die in de voorbeelden `Review Comment` en `Comment Reply` wordt vermeld.
   - De methode `setCommentId` stelt de unieke opmerking-id in voor elke opmerking, afhankelijk van het aantal opmerkingen.

   - In `setUserInfo` wordt de waarde van userInfo ingesteld, waarbij voor elke opmerking de volledige naam en titel worden gebruikt.

   - `onNewCommentEvent` zorgt ervoor dat de methode `setUserInfo` wordt aangeroepen voor elke nieuwe opmerking of elk nieuw antwoord.

   - De functie `updatedProcessComments` wordt uitgevoerd voor elke nieuwe opmerkingsgebeurtenis en zorgt ervoor dat `setCommentId` wordt aangeroepen als we een nieuwe opmerkingsgebeurtenis krijgen.

5. [ het Comité van de Revisies van het Onderwerp ](../../src/review_app_examples/topic_reviews.ts): Dit dossier breidt [ Inline het Comité van het Overzicht ](../../src/review_app_examples/inline_review_panel.ts) uit zodat de toegevoegde aanpassingen ook aan de kant van de App van het Overzicht werken.

6. [ Accepteer met de Dialoog van de Wijziging ](../../src/review_app_examples/accept_with_modification_dialog.ts)
Dit is een voorbeeld van het toevoegen van nieuwe widgets aan app. Hier hebben we een nieuw dialoogvenster gemaakt met twee invoertekstvelden: `Revised Text` en `Adjudicator Comment Rationale`

![ keurt met de dialoog van de Wijziging goed ](./imgs/accept_with_modification_dialogue.png)

Hier volgt het revisievenster voor en na de aanpassing:

![ het Comité van het Overzicht;](./imgs/review_panel.png)
![ keurt met de dialoog van de Wijziging goed ](./imgs/customised_review_panel.png)
