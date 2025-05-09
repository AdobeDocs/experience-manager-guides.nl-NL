---
title: Publicatietaken beheren met het dashboard Publiceren
description: Publicatietaken beheren met het publicatiedashboard in AEM Guides. Zorg dat u weet hoe u toegang krijgt tot het publicatiedashboard en annuleer een publicatietaak.
feature: Publishing
role: User
hide: true
exl-id: 9d311979-a7d7-47f5-945c-520eda99798f
source-git-commit: 1426cdaecdd358f06e76908b09330e65997e8452
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---

# Publicatietaken beheren met het dashboard Publiceren {#id205CC08305Z}

Wanneer u een grote reeks het publiceren taken hebt die op uw systeem lopen, wordt het praktisch onmogelijk om elke kaart afzonderlijk te controleren DITA om zijn het publiceren taak te controleren. AEM Guides geeft de beheerders en uitgevers één enkele mening van alle het publiceren taken die in het systeem lopen. Een lijst met alle actieve publicatietaken is beschikbaar op het dashboard Publiceren.

Het publicatiedashboard geeft een volledig overzicht van alle publicatietaken die momenteel in het systeem worden uitgevoerd.

![](images/publish-dashboard.png){width="800" align="left"}

Het publicatiedashboard bevat de volgende gegevens:

- **Titel van de Kaart** - de titel van een kaartdossier dat momenteel wordt gepubliceerd of in publiceer rij is.

- **Naam van het Dossier** - de dossiernaam van de kaart DITA.

- **Vooraf ingestelde Output** - Naam van de output vooraf ingesteld die wordt gebruikt om de output te produceren.

- **die door** wordt geïnitieerd - Gebruikersnaam van de gebruiker die de het publiceren taak in werking stelde.

- **begonnen op** - Datum en tijd toen de het publiceren taak was begonnen.

- **Verstreken Tijd** - Tijd sinds wanneer de het publiceren taak in het systeem loopt.

- **pictogram van de Schrapping** - annuleer of eindig een het publiceren taak.

Het linkerdeelvenster van het publicatiedashboard biedt de volgende filteropties:

- **Vooraf ingestelde Output** - selecteer één of meerdere output vooraf instelt waarvoor u de momenteel actieve het publiceren taken wilt zien. In de volgende schermafbeelding worden de publicatietaken gefilterd om alleen die taken weer te geven die gebruikmaken van de voorinstelling voor AEM-siteuitvoer:

  ![](images/publish-dashboard-preset-filter.png){width="800" align="left"}

- **die door** wordt geïnitieerd - selecteer een gebruikersbenaming van de lijst om de het publiceren taken te tonen door de geselecteerde gebruiker in werking worden gesteld.

- **Kaart** - selecteer een kaartdossier van de lijst om de het publiceren taken te tonen die voor de geselecteerde kaart lopen.

## Het dashboard Publiceren openen {#id205CC100DY4}

Voer de volgende stappen uit om toegang te krijgen tot het dashboard Publiceren:

>[!NOTE]
>
> Alleen een beheerder of uitgever heeft toegang tot het dashboard Publiceren.

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.

1. Selecteer **Gidsen** van de lijst van hulpmiddelen.

1. Klik op de **Publish Dashboard** tegel.

   Het dashboard Publiceren wordt geopend met een lijst van alle actieve publicatietaken in het systeem.

   Als u op de verbinding van de Naam van het Dossier klikt, wordt de DITA kaartconsole van de geselecteerde kaart getoond.

   ![](images/publish-dashboard-click-filename-link.png){width="800" align="left"}


>[!NOTE]
>
> U kunt het publicatiedashboard ook openen via het tabblad Uitvoer terwijl u uitvoer genereert via het kaartdashboard. Voor meer details, zie [ Mening het statuut van de taak van de outputgeneratie ](generate-output-for-a-dita-map.md#viewing_output_history).

## Een publicatietaak annuleren

Voer de volgende stappen uit om een taak van de outputgeneratie van het Publish Dashboard te annuleren:

1. [ heb toegang tot het Publish dashboard ](#id205CC100DY4).

1. Klik in de lijst met actieve publicatietaken op het pictogram Verwijderen van een taak die u wilt annuleren.

   ![](images/publish-dashboard-cancel-task.png){width="800" align="left"}

1. Klik **ja** op de Bevestig berichtherinnering van de Annulering.

   De opdracht Annuleren wordt geaccepteerd en de annulering wordt geprobeerd zolang de taak actief blijft. Zodra de taak met succes wordt geëindigd, wordt het verwijderd uit de momenteel actieve takenlijst. De status van de taak wordt ook bijgewerkt in de DITA kaartconsole zoals Geannuleerd. In het volgende screenshot, wordt de *HTML5* taak geannuleerd van het Publish Dashboard en zijn status wordt ook veranderd in de DITA kaartconsole.

   ![](images/cancelled-output-task.png){width="800" align="left"}


**Bovenliggend onderwerp:**&#x200B;[ Productie van de Output ](generate-output.md)
