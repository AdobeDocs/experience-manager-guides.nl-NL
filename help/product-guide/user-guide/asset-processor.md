---
title: Bezig met verwerken van elementen
description: Leer hoe u elementen kunt verwerken
feature: Migration
role: Admin
level: Experienced
exl-id: 27786098-119c-4b7a-8275-8a89d435294f
source-git-commit: 62221031e445ccdbf1f2567f38fa888ff52017d4
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# Proceselementen

In gegevensintensieve workflows, zoals publicaties, is efficiënt beheer van bedrijfsmiddelen van cruciaal belang voor het behoud van prestaties en betrouwbaarheid. De workflow voor het verwerken van bedrijfsmiddelen is ontworpen voor het beheer van gebruikersspecifieke elementen die intensieve gegevensbewerkingen vereisen. Het behandelt hoofdzakelijk twee gevallen: wanneer de aanvankelijke verwerking wegens fouten ontbreekt of wanneer de dossiers onverwerkt blijven omdat geen trekker van de activaverwerking werd in werking gesteld. Door gerichte verwerking op mapniveau in te schakelen, kunnen gebruikers alleen de benodigde middelen isoleren en verwerken, waardoor onnodige berekeningen overbodig worden. Deze selectieve aanpak verbetert de prestaties aanzienlijk, waardoor de vereiste tijd voor kritieke bewerkingen, zoals het publiceren en genereren van rapporten, wordt verkort. In het algemeen draagt het bij aan een efficiëntere en snellere verwerking van complexe gegevenstaken.

>[!NOTE]
>
> - Voor grote datasets, is het best om verwerking tijdens off-piek uren in werking te stellen om beïnvloedende systeemprestaties te vermijden. Nadat de verwerkingstaak voltooit, kunt u de details herzien om de resultaten te analyseren.<br>
>- Het systeem activeert de verwerking van elementen voor de map `/content/dam` om de 15 minuten. Tijdens elke cyclus worden activa die nieuw zijn toegevoegd of niet zijn verwerkt binnen het meest recente interval van 15 minuten, opgehaald en opnieuw verwerkt. Om de automatische de eigenschapmening van de activaverwerking te vormen, [&#x200B; vorm de eigenschap van de activaverwerking &#x200B;](../cs-install-guide/configure-asset-processing-cs.md).

## De elementen verwerken

Voer de onderstaande stappen uit om de elementen te verwerken:

1. Selecteer het embleem van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. In het **paneel van Hulpmiddelen** uitgezocht **Gidsen**.
1. Selecteer de **tegel van de Bewerker van 0&rbrace; Bulk &lbrace;.**

   ![&#x200B; stroom-activa-bewerker &#x200B;](images/flow-asset-processor.png){align="left"}

1. Het venster van de Bewerker van het Bulk van Gidsen opent met de hieronder getoonde details. Bovendien worden alleen de gegevens over de laatste vijf migraties weergegeven in dit venster.

   - **type van Eigenschap**: Toont de eigenschap van het proces dat wordt uitgevoerd.

   - **identiteitskaart van de Uitvoering**: Het is unieke identiteitskaart voor elke verwerkingstaak die u uitvoert.

   - **Omslag**: Toont de omslag die voor verwerking wordt geselecteerd.

   - **Uitgesloten Omslagen**: Toont de omslag die van verwerking wordt uitgesloten.

   - **die door** wordt gecreeerd: Toont die de taak of het proces creeerde. Het kan zowel jij als het systeem zijn.

   - **tijd van het Begin:** toont de datum en de tijd het verwerkingsproces in werking wordt gesteld.

   - **Eind Tijd**: Toont de datum en de tijd het verwerkingsproces beëindigt.

   - **Status**: Toont de status van verwerking zoals Bezig, Voltooid of Geannuleerd.

   ![&#x200B; gidsen-activa-bewerker &#x200B;](images/guides-asset-processor-new.png){align="left"}

1. Selecteer **Nieuw Proces** lusje op de hoogste juiste hoek van het venster om een nieuwe verwerkingstaak te beginnen.

   Het **Nieuwe proces** dialoog opent.

   ![&#x200B; nieuw-proces-activa-bewerker &#x200B;](images/new-asset-processor.png){width="350" align="left"}

1. Geef de volgende gegevens op in het dialoogvenster:

   1. **Type van Eigenschap**: Selecteer **de verwerking van Activa** van het drop verdrinken.
   1. **Uitgezochte omslagen en dossiers**: Navigeer en kies één of veelvoudige omslagen en dossiers om te verwerken.
   1. **Uitgezochte omslagen om** te negeren: Naar keuze, selecteer subfolders binnen de gekozen ouderomslag om van verwerking uit te sluiten.
   1. **Type van Activa**: Van dropdown, selecteer het specifieke activatype aan proces (b.v., Onderwerp DITA, Kaart DITA, Prijsverhoging, HTML/CSS, DITAVAL, of andere dossiers). Alleen het geselecteerde elementtype wordt verwerkt vanuit de map(pen) die u eerder hebt opgegeven.
Voorbeeld: het selecteren van DITA Onderwerp verwerkt slechts onderwerpen DITA binnen de geselecteerde omslag, toelatend gericht filtreren.
   1. **creeerde na/Gemaakt vóór**: Pas datumfilters op procesactiva toe die binnen gespecificeerde timeframe worden gecreeerd.

   >[!NOTE]
   >
   > Als er al een proces voor een map wordt uitgevoerd, kunt u pas een nieuw proces voor dezelfde map starten als de huidige taak is voltooid.

1. Selecteer **Maken**. U krijgt pop-up die **Succes toont en het Proces met succes teweeggebracht**. U kunt de status van de verwerkingstaak in het venster zien.

   ![&#x200B; bericht-activa-bewerker &#x200B;](images/message-asset-processor.png){width="350" align="left"}


## Aanvullende opties voor taken voor het verwerken van bedrijfsmiddelen

Er zijn extra opties beschikbaar voor de verwerkingstaak nadat deze is gestart. U hebt toegang tot deze opties door de muis boven de uitvoerings-id van uw taak te houden. Hieronder vindt u nadere informatie over deze opties:

- **Begin** opnieuw: Herstart de eerder succesvolle taak van de activaverwerking.

  ![&#x200B; opnieuw beginnen-activa-bewerker &#x200B;](images/restart-asset-processor.png){width="650" align="left"}

- **hervatten**: Hervat de eerder geannuleerde of ontbroken taak van de activaverwerking.

  ![&#x200B; hervat-activa-bewerker &#x200B;](images/resume-asset-processor.png){width="650" align="left"}

- **annuleert**: Annuleert de momenteel lopende taak van de activaverwerking.

  ![&#x200B; annuleren-activa-bewerker &#x200B;](images/cancel-asset-processor.png){width="650" align="left"}

- **Logboeken van de Mening**: Toont de logboeken voor de taak van de activaverwerking. Voor lopende taken, toont het logboek gedetailleerde verwerkingsinformatie, met inbegrip van geschatte resterende tijd en activastatus. In deze logbestandlijst worden maximaal de laatste 500 berichten weergegeven. Het volledige logboek kan worden gedownload.

  ![&#x200B; logboeken-activa-bewerker &#x200B;](images/logs-asset-processor.png){width="650" align="left"}
