---
title: De AI-assistent gebruiken om documenten slim te maken
description: Leer hoe u de AI Assistant gebruikt om documenten met slimme efficiëntie te maken.
exl-id: 47d37323-20bf-4444-a2c9-41c44b2c8daf
source-git-commit: 3d344a1d1b8d51ddadd618db5296531f549dc70b
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 0%

---

# Documenten slim ontwerpen met AI Assistant (Beta)

Adobe Experience Manager Guides biedt een AI Assistant-hulpprogramma waarmee u sneller en slimmer kunt ontwerpen. Bekijk de slimme suggesties om de inhoud uit de bestaande opslagplaats voor inhoud opnieuw te gebruiken. Met de functie voor tekstprompt kunt u een vraag weergeven en de inhoud naar wens wijzigen. Met de AI-assistent kunt u een alinea slim omzetten in een lijst. U kunt een korte beschrijving maken voor het huidige onderwerp op basis van de geselecteerde inhoud. Met deze functie kunt u de geselecteerde inhoud ook gemakkelijk verbeteren en vertalen.

>[!NOTE]
>
> Deze eigenschap van de Authoring is beschikbaar voor slechts onderwerpen DITA, en kan van de interface van de Redacteur slechts worden betreden. Op de pagina van het Huis en de console van de Kaart, slechts wordt het **paneel van de Hulp** getoond. De opties die beschikbaar zijn onder de ontwerpfunctie worden geconfigureerd op mapprofielniveau door de beheerders met behulp van de Editor-instellingen.

Na het selecteren van de tekst in een onderwerp, kunt u verkiezen om het even welke AI Hulpacties uit te voeren:

![ Hulp ai ](./images/ai-assistant-panel.png){width="300" align="left"}

## Herbruikbare inhoud voorstellen


Gebruik het **Voorstellen herbruikbare inhoud** ![ probeert opnieuw te gebruiken inhoudspictogram ](./images/ai-suggest-reusable-content-icon.svg) eigenschap aan auteursinhoud constant en nauwkeurig voor te stellen. U kunt de inhoud selecteren en Experience Manager Guides geeft suggesties voor het hergebruik van de bestaande inhoud in uw opslagplaats.
Leer meer over het gebruiken van [ AI-Aangedreven slimme suggesties aan auteursinhoud ](authoring-ai-based-smart-suggestions.md).


## Tekstprompt gebruiken

Een tekstprompt is een instructie, vraag of instructie die de AI Assistant begeleidt bij het genereren van een specifieke reactie.

U kunt een tekstprompt gebruiken om de inhoud te wijzigen. Bijvoorbeeld, kunt u de inhoud van uw huidig onderwerp selecteren en gebruiken de herinnering *maakt de tekst beknopter*. U kunt ook een tekstprompt gebruiken om een kenmerk toe te voegen aan de code die wordt gebruikt in de geselecteerde inhoud.

1. Selecteer de tekst waarvoor u de tekstprompt wilt gebruiken.
1. Selecteer **de tekstherinnering van het Gebruik** ![ ai pictogram van de gebruikstekstherinnering ](./images/ai-use-text-prompt.svg) van het **Authoring** paneel.
1. Geef een herinnering op één van de volgende manieren:

   - Kies een vraag van de voorgestelde herinneringen.
   - Reviseer of bewerk een voorgestelde aanwijzing om een aangepaste vraag te maken naar wens.

     >[!NOTE]
     >
     > De voorgestelde herinneringen worden gevormd in `ui_config.json` door uw beheerder.

   - Typ de vraag in het tekstvak.


1. Selecteer **Regenerate** ![ pictogram Regenerate ](./images/refresh-icon.svg) voor een andere reactie of output die op uw herinnering wordt gebaseerd.

1. (Facultatief) Uitgezochte **breid** uit ![ ](./images/expand-icon.svg) om de **de tekstherinnering van het Gebruik** redacteur te openen. De huidige en de gegenereerde inhoud worden weergegeven. U kunt de inhoud van de bronlay-out bewerken en de voorvertoning controleren.

   ![ de snelle redacteur van de hulptekst van de ai {](./images/text-prompt.png)


   >[!NOTE]
   >
   > De reacties worden gegenereerd op basis van de geselecteerde inhoud.



1. U kunt de vraag in de redacteur ook uitgeven en de reactie regenereren. U kunt bijvoorbeeld de vraag wijzigen om de tekst overzichtelijker te maken in ongeveer 40 woorden.

1. U kunt de bron van de gegenereerde inhoud verifiëren en deze indien nodig bewerken.

1. Selecteer **goedkeuren** om de geselecteerde inhoud in het onderwerp met de geproduceerde inhoud te vervangen.
1. **annuleert**: Annuleert de actie van de tekstherinnering. Hiermee gaat u terug naar het deelvenster Authoring.

   >[!NOTE]
   >
   > Het selecteren van **verwerpen** pictogram in het Authoring paneel keert u aan de aanvankelijke staat van de AI Medewerker terug.

## Inhoud verbeteren

Gebruik **verbeter inhoud** eigenschap om de kwaliteit van de geselecteerde inhoud van het huidige onderwerp te verbeteren. U kunt de inhoud selecteren om spelling, taal en grammaticale structuur te controleren en een betere versie van de inhoud voor te stellen. Het verbetert ook de kwaliteit van zinnen.

1. Selecteer de inhoud.
1. Selecteer **verbetert inhoud** ![ verbetert inhoudspictogram ](./images/ai-improve-icon.svg) om de suggesties voor de betere inhoud te vinden.
1. Selecteer **Regenerate** voor een andere suggestie van betere inhoud.

1. (Optioneel) Selecteer **Uitbreiden** om de verbeterde inhoudseditor te openen. De huidige en gegenereerde inhoud wordt weergegeven. U kunt de inhoud in de bronlay-out bewerken en ook de voorvertoning controleren.



   ![ hulp verbetert hulpmedewerker inhoudsredacteur ](./images/ai-assisstant-improve-content.png)

Accepteer de suggestie, bewerk de reactie in de bronweergave voordat u de aanvraag accepteert, regenereer deze voor een andere reactie of annuleer de actie om terug te keren naar de vorige status.





## Sneltoetsen maken

Maak in ongeveer 30 tot 50 woorden een korte beschrijving voor het onderwerp op basis van de geselecteerde inhoud. Met de korte beschrijving kunnen gebruikers relevante inhoud zoeken en vinden.
U kunt bijvoorbeeld een overzicht van de systeemvereisten geven en een korte beschrijving genereren.



1. Selecteer de inhoud.
1. Selecteer **creeer kortere weg** ![ wil korte beschrijvingspictogram ](./images/ai-create-shortdesc-icon.svg) creëren om een korte beschrijving voor het huidige onderwerp tot stand te brengen.
1. Selecteer **Accepteren** om een nieuwe korte beschrijving tot stand te brengen als de korte beschrijving niet reeds aanwezig is. Als er een korte beschrijving bestaat, moet u deze bevestigen voordat u deze vervangt door de nieuwe korte beschrijving.

U kunt ook de volgende handelingen uitvoeren:

- Selecteer **Regenereer** om een andere korte beschrijving voor uw onderwerp te produceren.
- Selecteer **uitbreiden** om **te openen creeer kortere weg** redacteur.

  ![ de medewerker van de ai creeert korte beschrijvingsredacteur ](./images/ai-assistant-create-short-desc.png)




## Inhoud specificeren

Met deze functie wordt een geselecteerde alinea op intelligente wijze omgezet in een lijst.  De inhoud wordt geanalyseerd en er wordt een logische lijst met items gemaakt. U hoeft de items niet handmatig te maken. Als u bijvoorbeeld een alinea hebt waarin de stappen voor het maken van een gebruikersaccount worden beschreven, kan het programma deze stap voor stap omzetten in een lijst, zodat items niet handmatig één voor één hoeven te worden gemaakt.

![ AI hulpondergeschikt specificeer inhoudspictogram ](./images/ai-assisstant-itemise-content.png)



1. Selecteer de inhoud.
1. Selecteer **inhoud** specificeren ![ ai specificeer inhoudspictogram ](./images/ai-itemize-icon.svg) om de geselecteerde inhoud in een lijst om te zetten.
Met het ontwerpgereedschap in het deelvenster AI-assistent zet u de inhoud slim om in een lijst met items.
1. (Facultatief) Uitgezochte **breid** uit om de **inhoud** redacteur van het Punt te openen.
1. Als uw lijst gereed is, accepteert u de wijzigingen in de gegenereerde inhoud. De gegenereerde inhoud vervangt vervolgens de geselecteerde inhoud.



## Inhoud vertalen

Met deze intelligente functie kunt u de geselecteerde inhoud vertalen naar de doeltaal. Dit is bijzonder handig wanneer u notities toevoegt in verschillende talen. U kunt bijvoorbeeld inhoud in het Engels toevoegen en deze snel omzetten in het Arabisch.

Voer de volgende stappen uit om de inhoud te vertalen:

1. Selecteer de inhoud die u wilt vertalen.
1. Selecteer **Vertaal inhoud** ![ ai vertaalt inhoudspictogram ](./images/ai-translate-content-icon.svg) van het **Authoring** paneel.
1. Selecteer de doeltaal in het vervolgkeuzemenu. De vertaalde inhoud wordt weergegeven in het deelvenster AI Assistant.

1. (Facultatief) Uitgezochte **breid** uit om de **Vertaalde inhoud** redacteur te openen.
1. U kunt ook een andere taal selecteren in het vervolgkeuzemenu en de inhoud opnieuw genereren in de gekozen taal. Bijvoorbeeld, als u Frans selecteert en dan **selecteert Regenerate**, wordt de inhoud vertaald in Frans.

![ de hulpmedewerker van ai vertaalt inhoud ](./images/ai-assisstant-translate-content.png)
