---
title: Publicatietaken beheren met het dashboard Publiceren
description: Publicatietaken beheren met het publicatiedashboard in AEM Guides. Zorg dat u weet hoe u toegang krijgt tot het publicatiedashboard en annuleer een publicatietaak.
exl-id: d9e25e52-ba9d-4088-ac95-8df76b69f5d3
feature: Publishing
role: User
source-git-commit: ac83f613d87547fc7f6a18070545e40ad4963616
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 0%

---

# Publicatietaken beheren met het dashboard Publiceren {#id205CC08305Z}

Wanneer u een grote reeks het publiceren taken hebt die op uw systeem lopen, wordt het praktisch onmogelijk om elke kaart afzonderlijk te controleren DITA om zijn het publiceren taak te controleren. Adobe Experience Manager Guides geeft de beheerders en uitgevers één enkele mening van alle het publiceren taken die in het systeem lopen. Een lijst met alle actieve publicatietaken is beschikbaar op het dashboard Publiceren.

Het publicatiedashboard geeft een volledig overzicht van alle publicatietaken die momenteel in het systeem worden uitgevoerd.

![](images/publish-dashboard.png){align="left"}

Het publicatiedashboard bevat de volgende gegevens:

- **Titel van de Kaart** - de titel van een kaartdossier dat momenteel wordt gepubliceerd of in publiceer rij is.

- **Naam van het Dossier** - de dossiernaam van de kaart DITA.

- **Vooraf ingestelde Output** - Naam van de output vooraf ingesteld die wordt gebruikt om de output te produceren.

- **die door** wordt geïnitieerd - Gebruikersnaam van de gebruiker die de het publiceren taak in werking stelde.

- **begonnen op** - Datum en tijd toen de het publiceren taak was begonnen.

- **Verstreken Tijd** - Tijd sinds wanneer de het publiceren taak in het systeem loopt.

- **pictogram van de Schrapping** - annuleer of eindig een het publiceren taak.

Het linkerdeelvenster van het publicatiedashboard biedt de volgende filteropties:

- **Vooraf ingestelde Output** - selecteer één of meerdere output vooraf instelt waarvoor u de momenteel actieve het publiceren taken wilt bekijken. In de volgende schermafbeelding worden de publicatietaken gefilterd om alleen die taken weer te geven die gebruikmaken van de voorinstelling voor AEM-siteuitvoer:

  ![](images/publish-dashboard-preset-filter.png){align="left"}

- **die door** wordt geïnitieerd - selecteer een gebruikersbenaming van de lijst om de het publiceren taken te tonen door de geselecteerde gebruiker in werking worden gesteld.

- **Kaart** - selecteer een kaartdossier van de lijst om de het publiceren taken te tonen die voor de geselecteerde kaart lopen.

## Het dashboard Publiceren openen

U kunt tot **toegang hebben publiceer Dashboard** direct van de [&#x200B; homepage van Experience Manager Guides &#x200B;](./intro-home-page.md). Open de homepage en selecteer **publiceren rij** optie van het linkerpaneel.

>[!NOTE]
>
> Alleen een beheerder of uitgever heeft toegang tot het dashboard Publiceren.

U kunt tot **toegang hebben publiceer Dashboard** van de Adobe Experience Manager **Hulpmiddelen** pagina. Voer de volgende stappen uit om deze methode te gebruiken:

1. Selecteer het embleem van Adobe Experience Manager bij de bovenkant en selecteer dan **Hulpmiddelen**.

1. Selecteer **Gidsen** van de lijst van hulpmiddelen.

1. Selecteer de **Publish Dashboard** tegel.

   Het dashboard Publiceren wordt geopend met een lijst van alle actieve publicatietaken in het systeem.

   Als u de verbinding van de Naam van het Dossier selecteert, wordt het dashboard van de kaart DITA van de geselecteerde kaart getoond.

   ![](images/publish-dashboard-click-filename-link.png){align="left"}


>[!NOTE]
>
> U kunt tot het Publish Dashboard van het **lusje van Output** ook toegang hebben terwijl u output van het kaartdashboard produceert. Voor meer details, verwijs naar [&#x200B; Mening het statuut van de taak van de outputgeneratie &#x200B;](generate-output-for-a-dita-map.md#viewing_output_history).

## Een publicatietaak annuleren

Voer de volgende stappen uit om een taak van de outputgeneratie van het Publish Dashboard te annuleren:

1. [&#x200B; heb toegang tot het Publish dashboard &#x200B;](#access-the-publish-dashboard).

1. Selecteer in de lijst met actieve publicatietaken het verwijderpictogram van een taak die u wilt annuleren.

   ![](images/publish-dashboard-cancel-task.png){align="left"}

1. Selecteer **ja** op **Bevestig annulering** berichtherinnering.

   De opdracht Annuleren wordt geaccepteerd en de annulering wordt geprobeerd zolang de taak actief blijft. Zodra de taak met succes wordt geëindigd, wordt het verwijderd uit de momenteel actieve takenlijst. De status van de taak wordt ook bijgewerkt in het dashboard van de kaart DITA zoals Geannuleerd. In het volgende schermschot, wordt de *HTML5* taak geannuleerd van het Publish Dashboard en zijn status wordt ook veranderd in het DITA kaartdashboard.

   ![](images/cancelled-output-task.png){align="left"}


**Bovenliggend onderwerp:**&#x200B;[&#x200B; Productie van de Output &#x200B;](generate-output.md)
