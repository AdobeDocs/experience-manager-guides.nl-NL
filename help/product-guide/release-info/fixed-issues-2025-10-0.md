---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2025.10.0
description: Meer informatie over de opgeloste problemen vindt u in de release 2025.10.0 van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: ff3cf777bd348edded29d780031df59bbb03035d
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 0%

---

# Opgeloste problemen in de release 2025.10.0

Dit artikel heeft betrekking op de fouten die zijn verholpen in verschillende gebieden van de release 2025.10.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [&#x200B; wat in de versie 2025.10.0 &#x200B;](whats-new-2025-10-0.md) nieuw is.

Leer over [&#x200B; verbeteringsinstructies voor de versie 2025.10.0 &#x200B;](upgrade-instructions-2025-10-0.md).

## Authoring

- Wanneer de veelvoudige kaarten DITA of de onderwerpen open zijn en één van de onderwerpen wordt gesloten, **>>** knoop die toont alle open lusjes wordt overlapt met de resterende open lusjes op de bar van het Lusje. (GUIDEN-31421)
- Met het **toegelaten werkschema van de Goedkeuring**, is het **Begin een Nieuwe Versie** knoop niet zichtbaar op de toolbar van de Redacteur als zowel het Linkerpaneel als het tevreden eigenschappen paneel open zijn. (GUIDEN-29093)
- Wanneer de namen van fragmenten de breedte van het fragmentpaneel overschrijden, lopen zij verkeerd op de volgende lijn, resulterend in overlapping met aangrenzende fragmenten en beïnvloedend leesbaarheid. (GUIDEN-22685)
- Wanneer u de zelfde verwijzing veelvoudige tijden aan een kaart DITA toevoegt, toont de **kaart** mening de titel slechts voor het laatste voorkomen, terwijl vorige degenen UUID van de verwijzing tonen. (GUIDEN-9699)
- De DITAVAL dossiers blijven editable, zelfs wanneer zij door een andere gebruiker worden gesloten of wanneer de server **uitgeeft heeft onbruikbaar maken zonder het toegelaten dossier** te sluiten en het dossier wordt geopend op read-only wijze. (HIDEN-27754)
- Logbestanden voor ontbrekende knooppunten worden gegenereerd op basis van interne opschoontaken die niet vereist zijn en die onjuist zijn gemarkeerd als fouten, wat resulteert in geclusterde logbestanden. (GUIDEN-31765)


## Publiceren

- Bij het genereren van PDF&#39;s worden de filterregels in een DITAVAL-bestand genegeerd als een eigenschapsnaam een punt bevat. (HULPLIJNEN-3329)
- Publiceren door Salesforce mislukt vanwege een toepassingsfout, wanneer er al een onderwerp met dezelfde naam en URL bestaat. (HULPLIJNEN- 32390)
- Bij publicatie in Salesforce wordt een geslaagde status weergegeven in de gebruikersinterface, zelfs als een DITA-kaart met een `topichead` -element de onderwerpen in de gebruikersinterface niet publiceert. (GUIDEN-32143)
- Voor HTML5-uitvoervoorinstelling werkt de functie van het zoekfilter niet in AEM Assets voor DITAVAL-filtering, omdat de corresponderende bestanden niet worden weergegeven wanneer het DITAVAL-filter wordt geselecteerd. (HIDEN-28231)
- Wanneer u een native PDF voor een DITA-kaart met meerdere onderwerpen genereert en een onderwerp een `fig` -element in een `figgroup` samen met een `title` bevat, wordt de `figgroup` -titel onjuist weergegeven als een hoofdstuktitel in de inhoudsopgave. (HULPLIJNEN-2323)
- Wanneer u PDF-sjablonen dupliceert vanuit de gebruikersinterface, wordt de UUID ook gedupliceerd, waardoor sjabloonbestanden worden verwijderd en onjuiste PDF-uitvoerbestanden ontstaan. (GUIDEN-30456)
- Bij het genereren van Native PDF voor een DITA-kaart geeft de titel van `example` -element weer als kopniveau `h1` , wat resulteert in visuele inconsistentie en onjuiste inhoudsopgavestructuur. (GUIDEN-19958)

## Vertaling

- Wanneer het zoemen in het scherm van Vertaling UI, verzendt **voor Vertaling** knoopbewegingen onder de ellips en wordt toegelaten zelfs zonder enig element dat wordt geselecteerd. (GUIDEN-33720)
- Wanneer het selecteren van dossiers met **uit de status van de Synchronisatie** op de Vertaling UI, en de het schermbreedte wordt beperkt toe te schrijven aan open Linker en Juiste panelen, verzendt **voor vertaling** etiket wordt beknot. (GUIDEN-33692)

## Controleren

- Wanneer een revisor een revisietaak voltooit of een aanvrager een revisietaak bijwerkt zonder opmerkingen in te voeren, wordt in het e-mailbericht dat wordt verzonden de meest recente vorige opmerking weergegeven. (HIDEN-33590)

## Bekende problemen

Adobe heeft de volgende bekende problemen vastgesteld voor de release 2025.10.0:

- Wanneer het openen van URL met een eerder geopend onderwerp DITA of het verfrissen van een geopend onderwerp DITA, ontbreekt het om van het onderwerp in de bewaarplaats de plaats te bepalen ondanks **altijd van dossiers in bewaarplaats** plaatsen die in de voorkeur van de Gebruiker worden toegelaten. (HULPLIJNEN-35565) <br>**Oplossing**: Selecteer het onderwerplusje om van het dossier in de bewaarplaats de plaats te bepalen.

- Wanneer u een nieuw bestand maakt in de weergave Auteur en er meerdere bestanden zijn geopend, wordt het deelvenster Rechts niet vernieuwd en worden onjuiste gegevens weergegeven als de cursor op een elementtag in een ander bestand is geplaatst. (HULPLIJNEN-35450) <br>**Oplossing**: De lusjes van de schakelaar of verfrissen de pagina om de kwestie op te lossen.

- Wanneer het schakelen naar de mening van de Auteur van de mening van Source voor een onlangs geopend onderwerp (dat aanvankelijk op de wijze van Source wordt geopend), wordt de onderwerpinhoud leeg. (HULPLIJNEN-35000) <br>**Oplossing**: vernieuw de pagina of open het onderwerp opnieuw om de kwestie op te lossen.

- **verfrist navigatie** knoop verschijnt voor DITA onderwerpdossiers, hoewel het slechts voor kaarten DITA, boekkaarten, en onderwerpregelingen beschikbaar zou moeten zijn. (GUIDEN-35452)






