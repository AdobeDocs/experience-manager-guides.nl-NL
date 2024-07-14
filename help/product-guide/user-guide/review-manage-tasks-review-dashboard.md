---
title: Revisietaken beheren met het dashboard Revisie
description: Revisietaken beheren via het revisiedashboard in AEM Guides. Leer de handelingen uitvoeren onder de taak, inhoud, tabblad revisoren en controleer de status van een revisietaak.
exl-id: 4fef5653-1c73-4b68-adf2-b24145555142
feature: Reviewing
role: User
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 0%

---

# Revisietaken beheren met het dashboard Revisie {#id2056B0Y70X4}

De werkstroom voor revisiebeheer kan verschillende taken bevatten. U kunt bijvoorbeeld revisoren toevoegen voor een bepaald onderwerp of de deadline voor een revisie verlengen. U kunt de revisietaak ook als volledig markeren als u denkt dat alle belanghebbenden hun feedback hebben gegeven. Deze taken kunnen worden beheerd met het dashboard Revisie.

Voer de volgende stappen uit om toegang te krijgen tot en gebruik te maken van het revisiedashboard:

>[!NOTE]
>
> U kunt revisietaken alleen beheren voor die projecten waarvoor u de auteur \(of aanvrager\) bent. Zelfs als u Revisor of Uitgever \(gebruiker\) bent, hebt u geen toegang tot de projecttaken.

1. In de **console van Projecten**, klik het overzichtsproject u wilt beheren.

   Er wordt een deelvenster Project met taaktegels weergegeven.

   ![](images/review-management.png){width="800" align="left"}

1. Klik de drie punten in de **tegel van Revisies**.

   Het revisiedashboard wordt weergegeven. Het dashboard bevat een lijst met alle revisietaken die u hebt gemaakt.

   ![](images/review-dashboard.png){width="800" align="left"}

   Het revisiedashboard bevat de details over de revisietaak, zoals de taaknaam, die de revisie heeft gestart, de datum waarop de revisie is gestart, de datum waarop de revisie is gestart, de status, het aantal nieuwe opmerkingen dat niet is geaccepteerd of afgewezen door de auteur en de naam van de controleurs. De taken worden weergegeven in de volgorde van nieuw gemaakte taken naar oudere taken.

   >[!NOTE]
   >
   > Als u op de verbinding van de Taak van het Overzicht klikt, wordt het onderwerp of kaartdossier dat voor overzicht wordt verzonden geopend.

1. Selecteer een revisietaak.

   U wordt getoond geeft Eigenschappen uit en [ 1} opties van de Status {in de toolbar.](#check-review-status-id199RF0A0UHS)

1. Als u **klikt geef Eigenschappen** uit, wordt de pagina van de Details van de Taak getoond.

   De pagina Taakdetails bevat drie tabbladen: Taak, Inhoud en Revisoren. In de volgende secties worden de verschillende functies beschreven die onder elk tabblad beschikbaar zijn.


## Tabblad Taak

![](images/review-task-page.png){width="800" align="left"}

U kunt de volgende acties onder de **Taak** tabel uitvoeren:

- Wijzig de titel van de taak op het **gebied van de Titel**.
- Voeg standaardwijzers in **toe toewijzen aan** drop-down lijst. De revisoren die u hier toevoegt, hebben toegang tot alle onderwerpen die deel uitmaken van deze revisietaak. U kunt verkiezen om meer recensenten aan specifieke onderwerpen te verwijderen of selectief toe te voegen van het [ lusje van Revisoren ](#reviewer-tab-id199RF0N0MUI).
- Werk de beschrijving van de taak op het **gebied van de Beschrijving** bij.
- Wijzig **Verschuldigde Datum**. U kunt de deadline voor het voltooien van de taak voorbereiden of uitstellen.
- Selecteer de optie om gebruikers te beperken tot het bekijken van alleen die onderwerpen die aan hen zijn toegewezen.
- Klik **Update** om de gewijzigde details bij te werken.
- Klik **Voltooien** om de overzichtstaak te merken zoals volledig vóór de vervaldatum. Wanneer de taak van een individueel onderwerp als Voltooid wordt duidelijk, wordt de overzicht van het geselecteerde onderwerp gesloten. Nochtans, in het geval van onderwerpen die voor overzicht door een kaart DITA worden gedeeld, zal het merken van de DITA kaarttaak als Voltooid de overzicht van alle onderwerpen binnen de kaart sluiten die voor overzicht werden gedeeld.
- Klik **Dupliceren** om een exemplaar van de overzichtstaak tot stand te brengen. Het maken van een dubbele revisietaak lijkt op het maken van een nieuwe revisietaak. Zodra u de gedupliceerde taakwerkstroom start, wordt de pagina Revisietaak maken weergegeven. U moet de nieuwe taakdetails verstrekken zoals die in [ worden verklaard verzendt onderwerpen voor overzicht ](review-send-topics-for-review.md#).

  Als u een overzichtstaak hebt geselecteerd die van een kaart DITA wordt gecreeerd, dan wordt u getoond de onderwerpen die een deel van de kaart zijn. U kunt dan de onderwerpen kiezen die u in de nieuwe overzichtstaak wilt omvatten.

  Als de overzichtstaak van één of veelvoudige onderwerpenoverzicht wordt gedupliceerd, dan slechts worden die onderwerpen getoond in de lijst van de overzichtstaak. U kunt deze onderwerpen ter controle delen met een andere set revisoren.

- Klik **dicht** om naar de Inbox pagina te gaan.

## Inhoud, tabblad

![](images/review-content-page.png){width="800" align="left"}

U kunt de volgende acties onder de **Inhoud** tabel uitvoeren:

- Wijzig de versie van het onderwerp dat ter controle wordt verzonden. U kunt de recentste versie van het onderwerp, versie zoals op datum, versie met specifiek etiket, of versie met een specifieke basislijn kiezen \(voor een kaart DITA \).

- Klik **Update** om de bijgewerkte versie van het onderwerp met de recensenten te delen. De controleurs krijgen een e-mailbericht met de mededeling dat de nieuwere versie van het onderwerp ter controle is verzonden. De volgende keer dat een controleur het onderwerp opent, zien zij de bijgewerkte versie van het onderwerp.

  >[!NOTE]
  >
  > In het geval van een bijgewerkte versie van een onderwerp, worden de oude commentaren behouden ook in de nieuwere versie. Revisoren kunnen ook de verschillen tussen de twee versies zien.

- Klik **Voltooien** om de overzichtstaak te merken zoals volledig vóór de vervaldatum. Wanneer de taak van een individueel onderwerp als Voltooid wordt duidelijk, wordt de overzicht van het geselecteerde onderwerp gesloten. Nochtans, in het geval van onderwerpen die voor overzicht door een kaart DITA worden gedeeld, zal het merken van de DITA kaarttaak als Voltooid de overzicht van alle onderwerpen binnen de kaart sluiten die voor overzicht werden gedeeld.

- Klik **Dupliceer** om een nieuwe overzichtstaak tot stand te brengen gebruikend de huidige taak als basis.


## Het tabblad Revisoren {#reviewer-tab-id199RF0N0MUI}

![](images/reviewers-tab.png){width="800" align="left"}

U kunt de volgende acties onder **Recensenten** tabel uitvoeren:

- **Uitgezocht allen**: Selecteert alle onderwerpen in de onderwerpenlijst. U kunt een partijverrichting gemakkelijk uitvoeren na het selecteren van alle onderwerpen.
- **Duidelijke Selectie**: Deselecteert de onderwerpen die in de onderwerpenlijst worden geselecteerd.

  >[!NOTE]
  >
  > U kunt een onderwerp ook individueel selecteren of schrappen door op checkbox naast het onderwerp te klikken.

- **voeg toe**: Toont de Add dialoog van Recensenten. U kunt de naam typen van een revisor of gebruikersrol \(of groep\) die u als controleur wilt toevoegen aan de geselecteerde onderwerpen.
- **verwijder**: Toont de Remove dialoog van Recensenten. U kunt de naam typen van een revisor of gebruikersrol \(of groep\) die u als controleur wilt verwijderen uit de geselecteerde onderwerpen.
- **opnieuw toewijzen**: Toont het Opnieuw toewijzen van de dialoog van Revisoren. U kunt de naam typen van een revisor of gebruikersrol \(of groep\) waaraan u de revisietaak wilt toewijzen. Hiermee verwijdert u alle bestaande revisoren uit de geselecteerde onderwerpen en wijst u de nieuw geselecteerde revisoren toe aan deze onderwerpen.
- **Uitvoer**: Staat u toe om de details van de overzichtstaak in een Csv- dossier uit te voeren. Het bestand bevat details zoals het pad en de titel van het onderwerp, de naam van de controleur en de versie van de onderwerpen die ter controle zijn verzonden.
- **geeft Recensenten** uit: Het klikken van het ![](images/edit_pencil_icon.svg) pictogram in de onderwerpenlijst toont de Edit dialoog van Reviewers. U kunt revisoren voor het geselecteerde onderwerp toevoegen aan of verwijderen uit dit dialoogvenster.

## De status van een revisietaak controleren {#check-review-status-id199RF0A0UHS}

Van de belangrijkste pagina van het Dashboard van het Overzicht, als u een overzichtstaak selecteert en **Status** klikt, wordt het statusrapport van de overzichtstaak getoond:

![](images/review-status-report.png){width="800" align="left"}

Het statusrapport voor de controletaak bevat de volgende details:

- Naam of namen van de controleur aan wie de revisietaak is toegewezen.
- De kolom Status geeft de revisiestatus aan. De status kan een van de volgende zijn:
   - **niet Begonnen**: De recensent heeft nog niet de overzichtsverbinding geopend.
   - **Bezig**: De recensent heeft de overzichtsverbinding geopend en is bezig het onderwerp te herzien.
   - **Voltooid**: De recensent heeft de overzicht door de overzichtstaak te voltooien die aan hen wordt toegewezen. De controletaak bevindt zich in het AEM-vak voor elke controleur.
- Wanneer een recensent een overzichtsverbinding opent en aan een bepaald onderwerp navigeert dat het onderwerp aan de Onderwerpen Gereviseerde lijst wordt toegevoegd. Op deze manier kunnen auteurs bepalen of de revisoren hun respectievelijke secties al dan niet hebben geopend. Eventuele opmerkingen worden tussen haakjes weergegeven.
- Het totale aantal opmerkingen over alle onderwerpen. In het geval van veelvoudige onderwerpen onder overzicht, wordt het aantal commentaren voor elk onderwerp vermeld \ (tussen haakjes \) naast de onderwerpnaam.
- De datum waarop een onderwerp voor het laatst is geopend door de revisor.

**Bovenliggend onderwerp:**[ onderwerpen of kaarten van het Overzicht ](review.md)
