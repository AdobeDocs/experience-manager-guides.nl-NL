---
title: Slimme suggesties voor AI-toepassingen om inhoud te ontwerpen
description: Leer hoe u op AI gebaseerde slimme suggesties in de Webeditor kunt weergeven en gebruiken.
exl-id: 23c5285e-0d4f-484a-a062-fe1ba1608b8d
source-git-commit: dd6fae108ddca23d36615fe38d176723bc4cfe86
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Intelligente suggesties voor het schrijven van inhoud door AI

Adobe Experience Manager Guides biedt de slimme suggesties die u helpen consistente en nauwkeurige inhoud te maken.

Terwijl u auteursinhoud, **voorstellen herbruikbare inhoud** eigenschap in het AI Hulphulpmiddel kan zoeken gebruikend AI en de bestaande inhoud tonen die semantisch aan uw inhoud gelijkaardig is. Vervolgens kunt u de beste overeenkomende inhoud kiezen die u als referentie in het huidige onderwerp wilt opnemen.

Zo kunt u bestaande inhoud uit de opslagplaats van de documentatie hergebruiken en consistente inhoud maken. Bijvoorbeeld, maakt u een document dat informatie over **Adobe Firefly** bevat, met inbegrip van een paragraaf over **Adobe**. In dat geval, kunt u de inhoudsverwijzing van een ander onderwerp, als **Adobe Photoshop** snel bekijken en toevoegen, dat de zelfde paragraaf omvat.
>[!NOTE]
>
> In de [ globale of omslag-vlakke profielen ](../cs-install-guide/conf-folder-level.md#conf-ai-smart-suggestions), moet uw beheerder de dossiers of de omslagen bepalen om voor slimme suggesties te indexeren, het minimumaantal karakters u moet ingaan om de suggesties te bekijken, en het maximumaantal suggesties u in de lijst kunt bekijken.

Voer de volgende stappen uit om de slimme suggesties te bekijken om aangewezen inhoudsverwijzingen aan uw onderwerp toe te voegen:


1. Selecteer de inhoud in het onderwerp om de verwante suggesties te bekijken. Zorg ervoor dat de tekenlengte van de inhoud groter is dan de tekenlengte die de beheerder in het mappenprofiel heeft ingesteld om de inhoudsuggesties weer te geven.
1. Van het **Authoring paneel** in AI Medewerker, uitgezochte **Voorstellen herbruikbare inhoud** ![ ai voorstelt herbruikbaar inhoudspictogram ](./images/ai-suggest-reusable-content-icon.svg).

1. Selecteer een tag om de ontwerpsuggesties voor de huidige tag weer te geven.  De suggesties om inhoudsverwijzingen uit de geïndexeerde bestanden weer te geven en toe te voegen, worden weergegeven op basis van de inhoud van de huidige tag. U kunt ook meerdere tags selecteren.


1. Selecteer alle labels om de suggesties weer te geven op basis van de inhoud in het volledige document.  Het **Voorgestelde herbruikbare inhoud** ![ stelt voor het herbruikbare pictogram van de inhoudspictogram ](./images/ai-suggest-reusable-content-icon.svg) naast de inhoud wordt getoond waar een geschikte gelijke wordt gevonden.



   >[!NOTE]
   >
   > U kunt alleen de suggesties voor de huidige viewport weergeven (de inhoud is zichtbaar op het scherm). Om suggesties voor een andere inhoud in het document te bekijken, scrol omhoog of omlaag om het in viewport te tonen, en dan te selecteren **stel opnieuw te gebruiken inhoud** voor ![ ai het herbruikbare inhoudspictogram ](./images/ai-suggest-reusable-content-icon.svg) voor.


1. U kunt de slimme suggesties weergeven in het deelvenster met suggesties.  Experience Manager Guides biedt suggesties voor inhoud die in een context lijkt of dezelfde betekenis heeft. Bijvoorbeeld, kunt u naar het onderwerp zoeken dat het nauwkeurige versieaantal, zoals &quot;versie 2023.03.12&quot;bevat. U kunt ook zoeken naar &quot;Adobe is hoofdkwartier in San Jose, Californië&quot; en vergelijkbare inhoud vinden zoals &quot;San Jose heeft de kwartalen van veel softwarebedrijven zoals Adobe.&quot;
1. Selecteer **![ Informatie van de Inhoud 1} ](images/smart-suggestions-content-info-icon.svg) de Informatie van de Inhoud {om de details te bekijken.**

   ![ het informatiepaneel van de Inhoud ](images/smart-suggestions-content-information.png){width="300" align="left"}

   *Mening de gedetailleerde informatie over de inhoudsverwijzing.*

   1. De titel van het onderwerp dat de inhoudsverwijzing bevat wordt getoond als hyperlink.
   1. Het pad van het bestand dat de inhoudsverwijzing bevat.
   1. Het referentietype waarnaar de inhoud wordt verwezen.
   1. De namen van DITA- dossiers waar het onderwerp wordt bedoeld worden getoond als hyperlinks.
1. Selecteer **![ voorproefpictogram van de Voorproef** ](./images/expand-icon.svg) om de huidige inhoud met de voorgestelde inhoud te vergelijken. Op deze manier kunt u de verschillen vergelijken en bepalen of u de inhoudsverwijzing voor de voorgestelde inhoud wilt toevoegen en deze consistent wilt maken of de huidige inhoud wilt behouden.

   ![ Voorproef van opnieuw te gebruiken inhoud ](images/ai-assistant-suggest-reusable-content.png) voorstellen

   *voorproef de vergelijking tussen de huidige inhoud en de voorgestelde inhoud.*

1. Selecteer **Accepteren** om de voorgestelde inhoudsverwijzing in de **Voorstellen herbruikbare inhoud** voorproef toe te voegen.
1. U kunt **ook selecteren keurt** goed of **verwerpt** in het suggesties paneel voor de aangewezen aanbevelingen.


Deze intelligente functie is handig en minimaliseert het handmatig zoeken naar inhoud, zodat u zich meer kunt concentreren op het genereren van nieuwe inhoud. Het vergemakkelijkt ook betere teamsamenwerking en helpt consistentie in de inhoud te handhaven die door diverse auteurs wordt gecreeerd.

>[!NOTE]
>
>Met slimme suggesties blijven uw gegevens na de huidige sessie behouden. Voor reacties baseren slimme suggesties zich alleen op de index die is gemaakt op de inhoud in uw interne database. Externe AI-gereedschappen worden niet gebruikt, zodat uw gegevens binnen het systeem blijven.
