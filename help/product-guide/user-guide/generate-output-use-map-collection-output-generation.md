---
title: Kaartverzameling gebruiken voor het genereren van uitvoer
description: Leer om een kaartinzameling tot stand te brengen en te schrappen en een kaart toe te voegen of te schrappen DITA. Vorm, produceer en annuleer een taak van de outputgeneratie van een kaartinzameling in AEM Gidsen.
exl-id: 41152fa4-f739-44d2-9ccd-74072f53e31b
feature: Publishing
role: User
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 0%

---

# Kaartverzameling gebruiken voor het genereren van uitvoer {#id1723F20G0HS}

In elke organisatie kan een product meerdere typen documentatie hebben. Als uitgeverspecialist, zou u willen controleren welke output u voor welk document wilt produceren. Bovendien moet u meerdere documenten met één klik in batch publiceren.

AEM de Gidsen verstrekt u de capaciteit om uw inhoud voor het publiceren te organiseren door een dashboard te gebruiken genoemd de Inzameling van de Kaart. Met een kaartverzameling kunt u alle verschillende typen documenten in één eenheid samenstellen. U kunt kiezen welk type van output u voor elk document in uw Inzameling van de Kaart wilt produceren. Bovendien kunt u output ook produceren en de vooruitgang van de outputgeneratie van het het publiceren dashboard zien.

De Inzameling van de kaart geeft u een optie om te bekijken als er om het even welke verandering in om het even welke kaart van de laatst gepubliceerde output is. U kunt de details op het lusje van Kaarten en van Voorinstellingen van uw Inzameling van de Kaart bekijken en dan de output indien nodig opnieuw publiceren. Voor meer informatie, zie het Toevoegen van een kaart aan een kaartinzameling.

## Een kaartverzameling maken en DITA-kaarten toevoegen

Voer de volgende stappen uit om een Kaartverzameling te maken en DITA-kaarten toe te voegen aan de verzameling:

1. Klik in de interface Middelen op **Verzamelingen toewijzen**.

   Als de koppeling Verzamelingen toewijzen niet beschikbaar is, selecteert u de optie **Navigatie** in de linkerspoorstaaf en klik dan **Verzamelingen toewijzen**.

   ![](images/access-map-collection-left-rail.png){width="350" align="left"}

1. Ga een Titel voor uw kaartinzameling in.
1. Klikken **Maken**.

   Een bericht van het Succes wordt getoond bij verwezenlijking van de kaartinzameling.

1. Klikken **Sluiten** op het bericht Succes.

   Het nieuwe kaartbestand wordt weergegeven op de pagina Kaartweerzamelingen.

1. Klik op het grijze vak in de tegel van de verzameling die u wilt bewerken.
1. Klikken **Bewerken** en klik vervolgens op **Kaarten toevoegen**.
1. Zoek en voeg de DITA-kaarten toe die u aan de verzameling Kaarten wilt toevoegen.

   Standaard worden alle voorinstellingen en landinstellingen die aan de kaart zijn gekoppeld, automatisch toegevoegd.

1. Selecteer de gewenste uitvoer door de schuifknop in of uit te schakelen.
1. Klikken **Gereed**.

   De DITA kaartdossiers worden toegevoegd aan uw Inzameling van de Kaart.

   ![kaartverzamelingsdashboard](./images/map-collection-dashboard.png){width="800" align="left"}

De volgende filteropties en kaartdetails worden getoond op de inzamelingspagina:

- **Filter:** In de laatste spoorstaaf worden de volgende filters getoond:
   - **gewijzigd**: U kunt Ja of Nee selecteren. Als u ja selecteert, slechts zullen de gewijzigde kaarten DITA in de Kaarten en de Vooraf ingestelde lijst worden getoond.
   - **Voorinstelling**: Selecteer een voorinstelling waarvoor u de kaartbestanden wilt uitfilteren. Als u bijvoorbeeld *Site AEM* voorinstelling, worden alleen de kaarten weergegeven die de *Site AEM* uitvoervoorinstelling geconfigureerd op deze apparaten.
   - **Taal**: U kunt alle beschikbare taalcodes selecteren en alleen de geselecteerde taal in de tabel Kaarten en Voorinstellingen weergeven.
- **Kaarten en voorinstellingen** tabel: de tabel Kaarten en voorinstellingen bevat informatie in de volgende kolommen:
   - **Kaart**: geeft de titel van het DITA-kaartbestand weer.
   - **Bestandsnaam**: geeft de bestandsnaam van de DITA-kaart weer.
   - **Taal**: Geeft de taal van de DITA-kaart weer.
   - **Voorinstelling**: Hiermee geeft u het type uitvoervoorinstelling weer dat op het kaartbestand is geconfigureerd.
   - **Basislijn**: Geeft de basislijn weer die wordt gebruikt door de uitvoervoorinstelling.  Als er geen basislijn wordt gebruikt, wordt er een afbreekstreepje &#39;-&#39; weergegeven
   - **gewijzigd**: Geeft aan of de DITA-kaart wordt bijgewerkt na de laatste publicatie. Gebaseerd op deze informatie, kunt u besluiten als u de output voor deze kaart wilt opnieuw publiceren DITA of niet.
   - **Laatst gegenereerd**: Geeft de datum en tijd weer van de laatst gegenereerde uitvoer.

## Vorm en produceer de output gebruikend een Inzameling van de Kaart

Om de output te vormen en te produceren gebruikend een Inzameling van de Kaart, voer de volgende stappen uit:

1. Open de verzameling Kaarten. U kunt de verschillende uitvoervoorinstellingen bekijken, zoals de voorinstellingen AEM Site, PDF (inclusief native PDF), HTML5, EPUB en Aangepast. U kunt ook de voorinstellingen voor het algemene profiel en het mapprofiel weergeven die door de beheerder zijn gemaakt.

   De ![](images/global-preset-icon.svg) geeft een voorinstelling voor het mapprofielniveau aan.
1. \(Optioneel\) Voer naar wens een van de volgende handelingen uit:
   - Pas filters van de linkerspoorstaaf toe om de gewijzigde kaarten, de outputvooraf ingestelde, of de taal te filtreren.
   - Klik indien nodig op **Bewerken** en wijzig de gewenste uitvoer door de schuifknop in of uit te schakelen.



     >[!NOTE]
     >  
     > Nieuwe voorinstellingen worden standaard uitgeschakeld.

1. U kunt de voorinstellingen voor een DITA-kaart op de volgende manieren inschakelen:

   - Een afzonderlijke voorinstelling inschakelen.
   - Inschakelen **Alle voorinstellingen** voor een DITA-kaart om alle voorinstellingen in één keer te selecteren. Deze optie is standaard uitgeschakeld.
   - Inschakelen **Voorinstellingen voor mapprofielen** voor een DITA-kaart om alle voorinstellingen voor het mapprofiel te selecteren. Deze optie is standaard uitgeschakeld.
     ![een kaartverzameling bewerken op cloudservices](images/edit-map-collection-cs.png){width="800" align="left"}



1. Voer een van de volgende handelingen uit:

   - Als u uitvoer van geselecteerde kaarten wilt genereren, selecteert u de kaartbestanden en klikt u op **Geselecteerde genereren**.
   - Om output van alle kaarten DITA met hun gevormde voorinstellingen te produceren, klik **Alles genereren**.

   >[!IMPORTANT]
   >
   > Als een proces voor het genereren van uitvoer voor een voorinstelling of een DITA-kaart zich in de wachtrij of in uitvoering bevindt, kunt u geen andere uitvoergeneratietaak voor dezelfde voorinstelling of dezelfde kaart starten.

## De eigenschappen van metagegevens configureren

In de kaartinzameling, kunt u de meta-gegevenseigenschappen voor de kaarten vormen DITA. Selecteren **Metagegevens configureren**  om de **Metagegevens van element** pagina. Op de **Metagegevens van element** pagina, worden alle kaarten in de verzameling links weergegeven.

![metagegevens configureren](images/map-collection-asset-metadata.png){width="800" align="left"}

Voer de volgende stappen uit om de eigenschappen van metagegevens te configureren:

1. U kunt kiezen voor welke kaarten u de metagegevens wilt bijwerken. Standaard zijn alle aanwezige DITA-kaarten geselecteerd.

1. Zodra u de kaarten DITA selecteert, kunt u eigenschappen zoals meta-gegevens, programma (de)activering, verwijzingen, documentstaat, en meer bekijken.

1. Werk de eigenschappen van de metagegevens bij.

1. Klikken **Opslaan en sluiten** bovenaan om de updates op te slaan.
1. (Optioneel) Wanneer u de codes bijwerkt, kunt u ook Toevoegen selecteren in het dialoogvenster **Opslaan en sluiten** vervolgkeuzelijst om de nieuwe tags aan de bestaande lijst toe te voegen.
1. Klikken **Verzenden** van de **Opslaan en sluiten** vervolgkeuzelijst.
De eigenschappen van metagegevens worden bijgewerkt voor de DITA-kaarten die u bulksgewijs in de kaartverzameling selecteert.

>[!NOTE]
> 
>Voor de **Documentstatus** in het vervolgkeuzemenu kunt u alleen de documentstaten selecteren die algemeen zijn toegestaan voor alle geselecteerde DITA-kaarten. Voor meer informatie bekijkt u [**Documentstatus**](./web-editor-document-states.md).

De eigenschappen van de metagegevens zijn synchroon met de bestandseigenschappen. Als u deze eenmaal hebt bijgewerkt, kunt u ze weergeven vanuit het dialoogvenster **Bestandseigenschappen** in de webeditor.



## Schrap een inzameling van de Kaart of een kaart DITA van de Inzameling van de Kaart

- Om een kaartinzameling te schrappen, selecteer een inzameling in de pagina van de Inzameling van de Kaart, en klik **Verwijderen**.
- Om een kaart DITA van een kaartinzameling te schrappen, open de Inzameling van de Kaart op Edit wijze, selecteer het DITA kaartdossier, en klik **Verwijderen uit verzameling**.

Hierdoor worden ook eventuele voorinstellingen of landinstellingen die aan de DITA-kaart zijn gekoppeld, verwijderd uit de Map Collection.


## Annuleer een taak van de outputgeneratie van een Inzameling van de Kaart

Gelijkaardig aan de manier om een taak van de outputgeneratie van te annuleren [DITA-kaartconsole](generate-output-for-a-dita-map.md#id2061H100T5Z) of de [Dashboard publiceren](generate-output-publish-dashboard.md#), kunt u een taak van de outputgeneratie van een Inzameling van de Kaart annuleren. Open het lusje van Output van een Inzameling van de Kaart, en ga naar de publicatietaak die u wilt annuleren, en klik **Deze taak annuleren** pictogram om de publicatietaak te annuleren.

![](images/cancel-publish-task-map-collection.png){width="800" align="left"}

**Bovenliggend onderwerp:**[ Uitvoergeneratie](generate-output.md)
