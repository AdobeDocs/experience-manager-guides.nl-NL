---
title: Uitvoergeneratie
description: Beheer het productieproces voor uitvoer in AEM Sites, PDF, HTML5, EPUB, custom en JSON via DITA-OT plug-ins, Native PDF-publicatie en FMPS in AEM Guides.
feature: Publishing
role: User
source-git-commit: b061bcbcefba1700665bed33f017a962e84a0433
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# Uitvoerproductieproces beheren

Met Adobe Experience Manager Guides kunt u de volgende handelingen uitvoeren op de gegenereerde uitvoer:

- [ Mening het statuut van de taak van de outputgeneratie ](#view-the-status-of-the-output-generation-task)
- [Een uitvoergeneratietaak annuleren](#cancel-an-output-generation-task)
- [Een uitvoertaak verwijderen](#delete-an-output-task)

## De status van de uitvoergeneratietaak weergeven

Zodra u de taak van de outputgeneratie voor een kaart in werking stelt of geselecteerde onderwerpen regenereert, verzendt Experience Manager Guides deze taak naar de rij van de outputgeneratie. Deze rij wordt bijgewerkt in echt - tijd, die de status van elke taak van de outputgeneratie in de rij toont.

1. In Assets UI, navigeer aan en open het kaartdossier waarvoor u de status van de outputgeneratie wilt controleren.

1. Selecteer **UITVOER**.

   ![](images/output-queued.png){width="800" align="left"}

   De pagina Uitvoer bestaat uit twee delen:

   - **in de rij geplaatste Output:**

     Vermeldt de output die of wachten om worden geproduceerd of onder generatieproces zijn. De taken in de wachtrij of die momenteel worden uitgevoerd, worden vóór de naam van de voorinstelling weergegeven met een blauw kleurenpictogram. U kunt ook de instelling of voorinstelling voor het genereren van uitvoer vinden die wordt gebruikt voor de taak in de wachtrij, het type, de gebruiker die de taak heeft gestart, de tijd sinds het moment waarop de taak in de wachtrij wordt geplaatst en de huidige status.

     Selecteer de verbinding om tot **toegang te hebben publiceer Dashboard** en bekijk de huidige lopende status. Een lijst met alle actieve publicatietaken is beschikbaar op het dashboard Publiceren. De **In een rij gevormde Output** en **publiceren de verbinding van het Dashboard** wordt getoond slechts wanneer er output is die of wachten om te worden geproduceerd of onder generatieproces zijn. Zij verschijnen niet wanneer de outputtaken zijn voltooid.Voor meer details op Publish Dashboard, publiceert de mening [ taken gebruikend het Publish Dashboard ](generate-output-publish-dashboard.md#).

   - **Gegenereerde Output**

     Hiermee geeft u de uitvoertaken weer die zijn voltooid. Nogmaals, is de hier getoonde informatie gelijkaardig aan de Gloonde sectie van Output met een paar verschillen. U hebt nieuwe informatie in de vorm van het pictogram van het outputresultaat en de tijd van de outputgeneratie.

     In deze lijst kunt u taken uitvoeren die met succes zijn uitgevoerd, taken die met een bericht zijn uitgevoerd of mislukte taken. De geslaagde taken worden weergegeven met een groen kleurpictogram, de taken met een bericht hebben een oranje kleurpictogram en de mislukte taken worden weergegeven met een rood kleurpictogram.

     Voor alle taken maakt het publicatieproces een logbestand \(logs.txt\) dat kan worden geopend door de koppeling te selecteren in de kolom Gegenereerd op. Voor taken die hebben ontbroken of berichten hebben, kunt u het logboekdossier controleren, dat in de sectie [ Mening wordt verklaard en het logboekdossier ](generate-output-basic-troubleshooting.md#id1822G0P0CHS) controleert.

     >[!NOTE]
     >
     > Wanneer u de koppeling van de gegenereerde PDF-uitvoer selecteert, wordt u gevraagd de PDF te downloaden.


## Een uitvoergeneratietaak annuleren

Experience Manager Guides biedt uitgevers een eenvoudige en eenvoudige manier om lopende publicatietaken te annuleren. Als uitgever, kunt u aan de gang zijnde het publiceren taak van de DITA kaartconsole of [ annuleren Dashboard ](generate-output-publish-dashboard.md#).

Voer de volgende stappen uit om een taak van de outputgeneratie van de DITA kaartconsole te annuleren:

1. In Assets UI, navigeer aan en open het kaartdossier waarvoor u een aan de gang zijnde taak van de outputgeneratie wilt annuleren.

1. Selecteer **UITVOER**.

1. In de **In een rij gevormde lijst van Output**, bewaar de wijzer over een taak die u wilt annuleren.

1. Selecteer **annuleert dit Taakpictogram**.

   ![](images/cancel-publish-task-map-console.png){width="800" align="left"}

1. Selecteer **ja** op **Bevestig annulering** berichtherinnering.

   ![](images/confirm-cancel-output-map-console.png){width="800" align="left"}

   Als de taak nog niet is gestart, wordt de opdracht Annuleren uitgevoerd op de taak. Voor een taak die wordt geannuleerd, wordt de Status geplaatst aan het Annuleren.

   Zodra de taak met succes wordt geannuleerd, wordt het verplaatst naar de **Gegenereerde lijst van Output** met a **Geannuleerde** status. Wanneer u de muisaanwijzer op de geannuleerde taak plaatst, ziet u de naam van de gebruiker die de taak heeft geannuleerd. In het volgende schermafbeelding, wordt de *HTML5* taak geannuleerd.

   ![](images/cancelled-output-task.png){width="800" align="left"}


## Een uitvoertaak verwijderen

Wanneer u veelvoudige output voor een kaart DITA produceert, over een periode de Gegenereerde lijst van Output voor zulk een kaart zeer lang wordt. Als uitgever kunt u de outputgeschiedenis van om het even welk kaartdossier schoonmaken door de verouderde taken uit de *Gegenereerde lijst van Output* te verwijderen. Merk op dat de output niet uit het systeem wordt verwijderd, slechts wordt de ingang van de geproduceerde output verwijderd uit de *Gegenereerde lijst van Output*.

Voer de volgende stappen uit om een uitvoertaak uit de Gegenereerde lijst van de Output te verwijderen:

1. In Assets UI, navigeer aan en open het kaartdossier waarvan u de taken wilt schrappen.

1. Selecteer **UITVOER**.

1. In de **Gegenereerde lijst van Output**, bewaar de wijzer over een taak die u wilt schrappen.

1. Selecteer het verwijderpictogram.

   ![](images/delete-output-task.png){width="800" align="left"}

1. Selecteer **ja** op **bevestigen schrapping** berichtherinnering.

   De taak wordt verwijderd uit de lijst Gegenereerde uitvoer.

