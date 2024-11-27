---
title: Produceer output voor een kaart DITA van de kaartconsole
description: Produceer output voor een kaart DITA van de kaartconsole in AEM Guides. Zorg voor meer informatie over het genereren van uitvoer en hoe u de status kunt bekijken, een uitvoertaak kunt annuleren en verwijderen.
exl-id: d6cbd44c-e74c-4192-bcc4-fb7752c59508
feature: Publishing
role: User
source-git-commit: 7db3df07fd17eecae1c502554118ca12f95fb5ab
workflow-type: tm+mt
source-wordcount: '1418'
ht-degree: 0%

---

# Produceer output voor een kaart DITA van de kaartconsole {#id1825FG00UHT}

Voer de volgende stappen uit om output voor een kaart te produceren DITA:

1. In Assets UI, navigeer aan en klik op het DITA kaartdossier dat u wilt publiceren.

   De DITA kaartconsole verschijnt met de lijst van de Voorinstellingen van de Output beschikbaar om output te produceren.

1. Selecteer een of meerdere uitvoervoorinstellingen die u wilt gebruiken voor het genereren van de uitvoer.

   ![](images/generate-multiple-outputs-uuid.png){width="800" align="left"}

   >[!NOTE]
   >
   > Als u de AEM Site-uitvoer genereert, gebruikt het publicatieproces de structuur die in het `.ditamap` -bestand is gedefinieerd om AEM sitestructuur te maken.

1. Klik op het pictogram Genereren om het genereren van de uitvoer te starten.


U kunt de huidige status van het verzoek van de outputgeneratie bekijken door op Output te klikken. Voor meer informatie, zie [ Mening het statuut van de taak van de outputgeneratie ](#viewing_output_history)

>[!IMPORTANT]
>
> Als een uitvoergeneratieproces voor een voorinstelling zich in de wachtrij of in uitvoering bevindt, kunt u geen andere uitvoergeneratietaak voor dezelfde voorinstelling starten.

U kunt de uitvoer van de PDF voor één of meerdere die outputvoorinstellingen produceren voor een kaart DITA van de Redacteur van het Web worden gecreeerd. Voor meer details, zie [ Snel van het Gebruik paneel produceren om output voor vooraf instelt ](web-editor-quick-generate-panel.md#) te produceren en te bekijken.

U kunt de output van de Plaats van de AEM voor één of meerdere onderwerpen, of de volledige kaart DITA van de Redacteur van het Web ook produceren. Voor meer details, zie [ Op artikel-gebaseerde het publiceren van de Redacteur van het Web ](web-editor-article-publishing.md#id218CK0U019I).

## Incrementele productie van uitvoer {#generating_standalone_topic}

>[!NOTE]
>
> Incrementele uitvoergeneratie is alleen van toepassing op AEM Site-uitvoer. U kunt ook alleen DITA \(.dita/.xml\)-onderwerpen opnieuw genereren op basis van een DITA-kaart of submappen. Als u een kaart DITA, sub-kaart, onderwerpgroep, of een onderwerp met `@processing-role="resource-only"` selecteert, dan is de regenerate optie niet beschikbaar.

Er zou een aantal instanties kunnen zijn waar u slechts een paar onderwerpen in uw kaart zou bijwerken DITA en duw slechts die bijgewerkte onderwerpen levend. Om dergelijke scenario&#39;s te behandelen, staat AEM Guides u toe om stijgende output tot stand te brengen. Als u een paar onderwerpen hebt bijgewerkt, te hoeven u niet om de volledige kaart opnieuw te produceren DITA. U kunt alleen de bijgewerkte onderwerpen selecteren en opnieuw genereren.

Als uw kaart wordt bebroed en u één enkel onderwerp in die kaart hebt bijgewerkt, dan moet u de volledige kaart voor het bijgewerkte onderwerp of de inhoud regenereren om in de output te weerspiegelen. U zult niet de optie van de outputregeneratie op een onderwerpniveau krijgen, is het slechts beschikbaar op het \(gescheurde \) kaartniveau. Dit is van toepassing op de bovenliggende kaart en alle submaps.

Voer de volgende stappen uit om output voor een specifiek onderwerp of een groep onderwerpen opnieuw te produceren:

>[!IMPORTANT]
>
> Wanneer u de AEM Site-uitvoer opnieuw genereert, wordt de uitvoer gemaakt met de huidige versie van de bestanden en niet met de gekoppelde basislijn.

1. Navigeer in de gebruikersinterface van Assets naar het DITA-kaartbestand en klik erop.

   De DITA kaartconsole verschijnt met de lijst van de Voorinstellingen van de Output beschikbaar om output te produceren.

1. Selecteer de **Onderwerpen** tabel.

   Een lijst van onderwerpen beschikbaar in de kaart DITA wordt getoond.

1. Selecteer de onderwerpen die u opnieuw wilt genereren.

   >[!NOTE]
   >
   > Als u nieuwe onderwerpen aan de kaart DITA hebt toegevoegd, zult u niet die nieuwe onderwerpen van hier kunnen produceren. U moet de onlangs toegevoegde onderwerpen eerst publiceren door de DITA kaart te gebruiken publiceert functie.

   ![](images/regenerate-topics.png){width="800" align="left"}

1. Klik **Regenerate**.

   De pagina Geselecteerde onderwerpen opnieuw genereren wordt weergegeven.

1. Selecteer de uitvoervoorinstelling die u wilt gebruiken om de geselecteerde onderwerpen opnieuw te genereren.

1. Klik **Regenereren** om het proces van de outputgeneratie te beginnen.


>[!IMPORTANT]
>
> Als u een onderwerptitel anders noemt en het onderwerp regenereert, reflecteert de bijgewerkte onderwerptitel niet in de DITA kaartlijst van inhoud. Om de onderwerptitel in TOC bij te werken, moet u de volledige kaart DITA produceren.

U kunt de huidige status van het verzoek van de outputgeneratie bekijken door op Output te klikken. Voor meer informatie, zie [ Mening het statuut van de taak van de outputgeneratie ](#viewing_output_history).

## De status van de uitvoergeneratietaak weergeven {#viewing_output_history}

Zodra u de taak van de outputgeneratie voor een kaart in werking stelt of geselecteerde onderwerpen regenereert, verzendt AEM Guides deze taak naar de rij van de outputgeneratie. Deze rij wordt bijgewerkt in echt - tijd, die de status van elke taak van de outputgeneratie in de rij toont.

Voer de volgende stappen uit om de rij van de outputgeneratie te bekijken:

1. In Assets UI, navigeer aan en klik op het kaartdossier waarvoor u de status van de outputgeneratie wilt controleren.

1. Klik **Output**.

   ![](images/output-queued.png){width="800" align="left"}

   De pagina Uitvoer bestaat uit twee delen:

   - **in de rij geplaatste Output:**

     Vermeldt de output die of wachten om worden geproduceerd of onder generatieproces zijn. De taken in de wachtrij of die momenteel worden uitgevoerd, worden vóór de naam van de voorinstelling weergegeven met een blauw kleurenpictogram. U kunt ook de instelling of voorinstelling voor het genereren van uitvoer vinden die wordt gebruikt voor de taak in de wachtrij, het type, de gebruiker die de taak heeft gestart, de tijd sinds het moment waarop de taak in de wachtrij wordt geplaatst en de huidige status.

     Klik op de verbinding om tot het **dashboard van Publish** toegang te hebben en de huidige lopende status te bekijken. In het Publish-dashboard vindt u een lijst met alle actieve publicatietaken. De **in de rij geplaatste Output** en **verbinding van het Dashboard van Publish** worden getoond slechts wanneer er output is die of wachten om te worden geproduceerd of onder generatieproces zijn. Zij verschijnen niet wanneer de outputtaken zijn voltooid.Voor meer details op het dashboard van Publish, zie [ publiceer taken gebruikend het dashboard van Publish ](generate-output-publish-dashboard.md#) leiden.

   - **Gegenereerde Output**

     Hiermee geeft u de uitvoertaken weer die zijn voltooid. Nogmaals, is de hier getoonde informatie gelijkaardig aan de Gloonde sectie van Output met een paar verschillen. U hebt nieuwe informatie in de vorm van het pictogram van het outputresultaat en de tijd van de outputgeneratie.

     In deze lijst kunt u taken uitvoeren die met succes zijn uitgevoerd, taken die met een bericht zijn uitgevoerd of mislukte taken. De geslaagde taken worden weergegeven met een groen kleurpictogram, de taken met een bericht hebben een oranje kleurpictogram en de mislukte taken worden weergegeven met een rood kleurpictogram.

     Voor alle taken maakt het publicatieproces een logbestand \(logs.txt\) dat kan worden geopend door op de koppeling in de kolom Gegenereerd op te klikken. Voor taken die hebben ontbroken of berichten hebben, kunt u het logboekdossier controleren, dat in de sectie [ Mening wordt verklaard en het logboekdossier ](generate-output-basic-troubleshooting.md#id1822G0P0CHS) controleert.

     >[!NOTE]
     >
     > Wanneer u op een koppeling van de gegenereerde PDF-uitvoer klikt, wordt u gevraagd de PDF te downloaden. Dit is het standaardgedrag in AEM 6.5 en 6.4.


## Een uitvoergeneratietaak annuleren {#id2061H100T5Z}

AEM Guides biedt uitgevers een eenvoudige en eenvoudige manier om lopende publicatietaken te annuleren. Als uitgever, kunt u aan de gang zijnde het publiceren taak van de DITA kaartconsole of het [ dashboard van Publish ](generate-output-publish-dashboard.md#) annuleren.

Voer de volgende stappen uit om een taak van de outputgeneratie van de DITA kaartconsole te annuleren:

1. In Assets UI, navigeer aan en klik op het kaartdossier waarvoor u een aan de gang zijnde taak van de outputgeneratie wilt annuleren.

1. Klik **Output**.

1. Houd de aanwijzer in de lijst Uitvoer in wachtrij boven een taak die u wilt annuleren.

1. Klik *annuleert Dit Taakpictogram*.

   ![](images/cancel-publish-task-map-console.png){width="800" align="left"}

1. Klik **ja** op de Bevestig berichtherinnering van de Annulering.

   ![](images/confirm-cancel-output-map-condole.png){width="800" align="left"}

   Als de taak nog niet is gestart, wordt de opdracht Annuleren uitgevoerd op de taak. Voor een taak die wordt geannuleerd, wordt de Status geplaatst aan het Annuleren.

   Zodra de taak met succes wordt geannuleerd, wordt het verplaatst naar de **Gegenereerde lijst van Output** met a **Geannuleerde** status. Wanneer u de muisaanwijzer op de geannuleerde taak plaatst, ziet u de naam van de gebruiker die de taak heeft geannuleerd. In het volgende schermafbeelding, wordt de *HTML5* taak geannuleerd.

   ![](images/cancelled-output-task.png){width="800" align="left"}


## Een uitvoertaak verwijderen uit de DITA-kaartconsole

Wanneer u veelvoudige output voor een kaart DITA produceert, over een periode de Gegenereerde lijst van Output voor zulk een kaart zeer lang wordt. Als uitgever kunt u de outputgeschiedenis van om het even welk kaartdossier schoonmaken door de verouderde taken uit de *Gegenereerde lijst van Output* te verwijderen. Merk op dat de output niet uit het systeem wordt verwijderd, slechts wordt de ingang van de geproduceerde output verwijderd uit de *Gegenereerde lijst van Output*.

Voer de volgende stappen uit om een uitvoertaak uit de Gegenereerde lijst van de Output te verwijderen:

1. Navigeer in de gebruikersinterface van Assets naar het kaartbestand waaruit u de taken wilt verwijderen en klik erop.

1. Klik **Output**.

1. Houd de aanwijzer in de lijst Gegenereerde uitvoer boven een taak die u wilt verwijderen.

1. Klik op het verwijderpictogram.

   ![](images/delete-output-task.png){width="800" align="left"}

1. Klik **ja** op Bevestig het berichtherinnering van de Schrapping.

   De taak wordt verwijderd uit de lijst Gegenereerde uitvoer.


**Bovenliggend onderwerp:**[ Productie van de Output ](generate-output.md)
