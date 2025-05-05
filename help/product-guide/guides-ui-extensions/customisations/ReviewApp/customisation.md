---
title: Aanpassen
description: De revisie-app aanpassen
role: User, Admin
exl-id: 9f6a4e9f-fc13-40b5-a30f-151c94faff81
source-git-commit: 492f72768e0de74a91eb7acc9db8264e21bfc810
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# De revisie-app aanpassen

Om de aanpassing van de revisie-app te vereenvoudigen, hebben we enkele haken weergegeven die hieronder worden beschreven en uitgelegd:

## Reviseren-opmerking

- id: `review_comment`
- haak: `this.next('updateExtraProps')`:

Zoals hier besproken [&#128279;](../../aem_guides_framework/basic-customisation.md), gaat om het even welk nieuw attribuut dat tijdens aanpassing wordt toegevoegd onder `this.model.extraProps`. Met de methode `updateExtraProps` kunt u kenmerken toevoegen aan een revisieopmerking en kunt u de update en opslag van het toegevoegde kenmerk ook op de server uitvoeren.

### Voorbeeld van gebruik

U wilt bijvoorbeeld velden `commentRationale` en `severity` toevoegen aan uw opmerkingen.
Laten we `commentRationale` bijwerken naar &quot;Dit is een belangrijke zin.&quot; en de `severity` naar &quot;KRITIEK&quot;.
Dit kan worden gedaan gebruikend de syntaxis:

```typescript
  this.next('updateExtraProps', {
    'commentRationale': 'This is an important sentence.',
    'severity': 'CRITICAL'
  })
```

In het bovenstaande codefragment worden de waarden bijgewerkt en opgeslagen. De opgeslagen waarden kunnen worden weergegeven in de gebruikersinterface door de weergave te definiëren.

```JSON
{
    "component" : "label",
    "label": "@extraProps.commentRationale"
}
```

## Deelvenster Inline revisie

- id: `inline_review_panel`

1. haak: `onNewCommentEvent`
Met de haak `onNewCommentEvent` kunt u een gebeurtenis genereren of een methode aanroepen voor een nieuwe opmerking- of antwoordgebeurtenis.
De args die in `onNewCommentEvent` worden ontvangen, zijn onder andere:
   - gebeurtenissen: de opmerking-/antwoordgebeurtenis die is verzonden.
   - newComment: boolean
Als de verzonden gebeurtenis een nieuwe opmerkingsgebeurtenis was, dus `highlight`, `insertion`, `deletion`, `sticky note comment`
   - newReply: boolean
Als de verzonden gebeurtenis een nieuwe antwoordgebeurtenis was.

2. haak: `sendExtraProps`

Deze haak is nuttig als u een `event` wilt uitbreiden en `extraProps` wilt verzenden vanuit het deelvenster voor inline-revisie. We zullen het gebruik van deze twee haken hieronder toelichten.

### Voorbeeld van het deelvenster Inline Review

Stel dat we een extraProp, `userInfo` , willen verzenden telkens wanneer een nieuwe opmerking of een nieuw antwoord wordt verzonden. Dit gebeurt nu via het deelvenster voor inline revisie, maar we hebben geen verwijzing naar de opmerking-id van de zojuist gegenereerde opmerking. Daarom kunnen we de volgende code schrijven.

```typescript
    onNewCommentEvent(args){
      const events = _.get(args, "events")
      const currTopicIndex = tcx.model.getValue(tcx.model.KEYS.REVIEW_CURR_TOPIC) || this.getValue('currTopicIndex') || "0"
      const event = _.get(_.get(events, currTopicIndex), '0')
      const newComment = _.get(args, 'newComment')
      const newReply = _.get(args, 'newReply')
      if ((newComment || newReply) && event) {
        this.next('setUserInfo', event)
      }
    },
```

In het bovenstaande codefragment controleren we of de verzonden gebeurtenis een nieuwe opmerking of een nieuw antwoord is. In het geval van een nieuwe opmerking of reactie roepen we de methode aan `setUserInfo`

```typescript
    const getUserInfo = (userId) => {
      return $.ajax({
        url: '/bin/dxml/xmleditor/userinfo',
        data: {
          username: userId,
        },
        success: (data) => {
          return data
        }
      })
    }

    setUserInfo(event) {
      getUserInfo(event.user).done(userData => {
        const extraProps = {
          "userFirstName": userData?.givenName || '',
          "userLastName": userData?.familyName || '',
          "userTitle": userData?.title || '',
          "userJobTitle": userData?.jobTitle || '',
          'userEmail': userData?.email || '',
        }
        const data = {... event, extraProps}
        this.next(
          'sendExtraProps',
          data
        )
      })
    },
```

In de bovenstaande methode breiden we de gebeurtenis uit om extraProps te verzenden, inclusief de voornaam, e-mail, titel, enzovoort. Als u de gebeurtenis op deze manier uitbreidt, zorgt u ervoor dat de extraProps met de juiste commentId worden verzonden, zodat deze aan de juiste opmerking worden gekoppeld.

De haak `updateExtraProps` roept inherent de haak `sendExtraProps` aan, dus wanneer om te gebruiken wat?

We gebruiken `updateExtraProps` in de `review_comment` -controller, die al de opmerkingen `id` bevat. Daarom hoeft u alleen maar de `extraProps.` -component te noemen

De `inline_review_panel` heeft echter geen toegang tot de id van de opmerking. Daarom is `sendExtraProps` altijd handig als u een gebeurtenis wilt verzenden vanuit het deelvenster voor inline-revisie.
