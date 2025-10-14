---
title: Gewijzigde onderwerpen vertalen
description: Leer hoe u een gewijzigd onderwerp opnieuw vertaalt in AEM Guides.
exl-id: b3228ea9-24a8-44aa-8ba4-e8f44754ffe4
feature: Translation
role: User
source-git-commit: ac83f613d87547fc7f6a18070545e40ad4963616
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# Gewijzigde onderwerpen vertalen {#id16A5A0B6072}

Als u veranderingen in sommige onderwerpen aanbrengt, dan vereisen die onderwerpen re-vertaling. U kunt spoor van gewijzigde onderwerpen van kaart houden DITA. Selecteer het DITA-kaartbestand in de Kaartconsole in de kopiëren-map van de brontaal en selecteer het tabblad Vertaling. U kunt de status van elk onderwerp bekijken of het al dan niet opnieuw moet worden vertaald.

Voer de volgende stappen uit om een gewijzigd onderwerp voor re-vertaling te verzenden:

1. Selecteer het DITA kaartdossier van de omslag van het brontaalexemplaar van de **Console van de Kaart** in de Redacteur.

1. Selecteer het **Vertaling** lusje.

1. In het **Vertaling** paneel op de linkerzijde, selecteer **Beschikbare Talen** die u de status wilt controleren **toepassen**.

   U kunt de vertaalstatus voor elk onderwerp bekijken. De onderwerpen die een andere revisie van onderwerp beschikbaar hebben dan wat voor vertaling werd verzonden, tonen een **uit status van de Synchronisatie**.

   >[!NOTE]
   >
   > De vertaalwerkstroom vergelijkt de laatste opgeslagen revisie van het onderwerpdossier in de brontaalomslag met de vertaalde versie.

   Als u de pijl selecteert om meer details weer te geven, kunt u de specifieke taalkopie bekijken die niet gesynchroniseerd is.

   ![](images/out-of-sync-uuid-new.png){align="left"}

1. Schakel het selectievakje in om de onderwerpen te selecteren die u wilt verzenden voor hervertaling.

   Wanneer u uit synchronisatieonderwerp selecteert, **Teken in Synchronisatie** knoop verschijnt boven de titelbar.

   U kunt het **Teken in Synchronisatie** knoop gebruiken om uit de status van de Synchronisatie voor de onderwerpen in de kaart met DITA met voeten te treden.  Als u bijvoorbeeld enkele kleine wijzigingen hebt aangebracht waarvoor geen vertaling nodig is, kunt u de status van de wijzigingen markeren op Sync.

   >[!NOTE]
   >
   > Als u het **Teken in Synchronisatie** knoop selecteert, plaatst het de onderwerpstatus aan in Synchronisatie voor geselecteerde uit onderwerpen van de Synchronisatie.

1. U kunt **selecteren verzendt voor Vertaling knoop**.

1. U kunt verkiezen om een nieuw vertaalproject tot stand te brengen of onderwerpen aan een bestaand vertaalproject toe te voegen. Verstrek de vereiste details om het vertaalproject te vormen.

1. Selecteer **voorleggen**.

   Er wordt een bevestigingsbericht weergegeven waarin wordt aangegeven dat het onderwerp voor vertaling is verzonden.

1. Navigeer aan het vertaalproject in de console van het Project. Er wordt een nieuwe vertaalopdrachtkaart gemaakt in de map. Selecteer de ellips om de elementen van de map weer te geven.

   ![](images/incremental-job-new.png){width="300" align="left"}

1. Om de vertaling te beginnen, selecteer de pijl op de kaart van de vertaalbaan en selecteer **Begin** van de lijst. Een bericht geeft aan dat de taak is gestart.

   U kunt de status van het onderwerp dat wordt vertaald ook bekijken wanneer u de ellips bij de bodem van de kaart van de vertaalbaan selecteert.

   >[!NOTE]
   >
   > Als u de vertaalservice Human gebruikt, moet u de inhoud exporteren voor vertaling. Zodra u de vertaalde inhoud hebt, dan moet u het terug in het vertaalproject invoeren.

1. Nadat de vertaling voltooit, de statusveranderingen in **Klaar aan Overzicht**. Selecteer de ellips om de onderwerpdetails te bekijken en één van het volgende van de toolbar te doen:

   - Selecteer **onthullen in Assets** om de vertaling te bekijken en te verifiëren.

   - Selecteer **Vertaling** goedkeuren als u denkt dat de veranderingen correct zijn vertaald. Er wordt een bevestigingsbericht weergegeven.

   - Selecteer **Vertaling van de Weigering** als u denkt dat de baan opnieuw moet worden gedaan. Er wordt een afwijzingsbericht weergegeven.

   >[!NOTE]
   >
   > Het is belangrijk het vertaalde element te accepteren of af te wijzen, anders blijft het bestand op de tijdelijke locatie en wordt het niet naar DAM gekopieerd.

1. Navigeer terug naar het DITA-kaartbestand in de brontaalmap in de gebruikersinterface van Assets. De opnieuw vertaalde onderwerpen zijn nu synchroon.


**Bovenliggend onderwerp:**&#x200B;[&#x200B; het vertaaloverzicht van de Inhoud &#x200B;](translation.md)
