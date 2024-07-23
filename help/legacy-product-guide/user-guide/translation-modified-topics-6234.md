---
title: Gewijzigde onderwerpen vertalen
description: Leer hoe u een gewijzigd onderwerp opnieuw vertaalt in AEM Guides.
feature: Translation
role: User
source-git-commit: 76c731c6a0e496b5b1237b9b9fb84adda8fa8a92
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 0%

---

# Gewijzigde onderwerpen vertalen {#id16A5A0B6072}

Als u veranderingen in sommige onderwerpen aanbrengt, dan vereisen die onderwerpen re-vertaling. U kunt spoor van gewijzigde onderwerpen van kaart houden DITA. Klik in de map met de brontaalkopie op het DITA-kaartbestand en klik op het tabblad Vertaling. U kunt het statuut van elk onderwerp zien of het al dan niet hervertaling vereist.

Voer de volgende stappen uit om een gewijzigd onderwerp voor re-vertaling te verzenden:

1. Klik het DITA kaartdossier van de brontaalexemplaaromslag.

1. Klik de **Vertaling** tabel.

1. In het **paneel van de Filter** op de linkerzijde, selecteer **Vertaal Talen** dat u de status wilt controleren en **Gedaane** klikken.

   U kunt de vertaalstatus voor elk onderwerp zien. De onderwerpen die een andere revisie van onderwerp beschikbaar hebben dan wat voor vertaling werd verzonden, tonen een **Verouderd van Datum** status.

   >[!NOTE]
   >
   > De vertaalwerkstroom vergelijkt de laatste opgeslagen revisie van het onderwerpdossier in de brontaalomslag met de vertaalde versie.

   Als u op de pijl klikt, ziet u meer details. u kunt de specifieke taalkopie zien die verouderd is.

   ![](images/out-of-sync-uuid.png){width="800" align="left"}

1. Klik het controlevakje om de onderwerpen te selecteren die u voor re-vertaling wilt verzenden.

   Wanneer u een uit synchronisatiedatum selecteert, **creeert/de optie van de Taal van de Update** verschijnt in het paneel van Verwijzingen en de **Ontkenning uit de knoop van de Status van de Synchronisatie** boven het **pictogram van de Filter**.

   U kunt de **Ontkenning uit Synchronisatie** knoop gebruiken om de Verouderde status voor de onderwerpen in de kaart met DITA met voeten te treden. Bijvoorbeeld, als u sommige veranderingen in de Engelse versie van het onderwerp aanbracht die geen vertaling vereist, kunt u deze knoop gebruiken en de status van Verouderd voor het geselecteerde onderwerp veranderen.

   >[!NOTE]
   >
   > Als u de **Ontkenning uit de knoop van de Status van de Synchronisatie** klikt, plaatst het de onderwerpstatus aan Up aan Datum voor de geselecteerde Onderwerpen van Verouderd.

1. Klik {de Kopieën van de Taal van 0} Update **en vorm de vertaalbaan.**

1. U kunt verkiezen om een nieuw vertaalproject tot stand te brengen of onderwerpen aan een bestaand vertaalproject toe te voegen. Verstrek de vereiste details om het vertaalproject te vormen.

1. Klik **Begin**.

   Er wordt een bevestigingsbericht weergegeven waarin wordt aangegeven dat het onderwerp voor vertaling is verzonden.

1. Navigeer aan het vertaalproject in de console van het Project. Er wordt een nieuwe vertaalopdrachtkaart gemaakt in de map. Klik op de ellips om de elementen van de map weer te geven.

   ![](images/incremental-job.PNG){width="300" align="left"}

1. Om de vertaling te beginnen, klik de pijl op de kaart van de vertaalbaan en selecteer **Begin** van de lijst. Een bericht geeft aan dat de taak is gestart.

   U kunt de status van het onderwerp dat wordt vertaald ook bekijken wanneer u de ellips bij de bodem van de kaart van de vertaalbaan klikt.

   >[!NOTE]
   >
   > Als u de vertaalservice Human gebruikt, moet u de inhoud exporteren voor vertaling. Zodra u de vertaalde inhoud hebt, dan moet u het terug in het vertaalproject invoeren.

1. Nadat de vertaling voltooit, de statusveranderingen in **Klaar aan Overzicht**. Klik op de ellips om de onderwerpdetails weer te geven en voer een van de volgende handelingen uit op de werkbalk:

   - Klik **onthullen in Assets** om de vertaling te zien en te verifiëren.

   - Klik **goedkeuren Vertaling** als u denkt dat de veranderingen correct zijn vertaald. Er wordt een bevestigingsbericht weergegeven.

   - Klik **Vertaling van de Weigering** als u denkt dat de baan opnieuw moet worden gedaan. Er wordt een afwijzingsbericht weergegeven.

   >[!NOTE]
   >
   > Het is belangrijk het vertaalde element te accepteren of af te wijzen, anders blijft het bestand op de tijdelijke locatie en wordt het niet naar DAM gekopieerd.

1. Navigeer terug naar het DITA-kaartbestand in de brontaalmap in de gebruikersinterface van Assets. De opnieuw vertaalde onderwerpen zijn nu synchroon.


**Bovenliggend onderwerp:**[ vertaal inhoud ](translation.md)
