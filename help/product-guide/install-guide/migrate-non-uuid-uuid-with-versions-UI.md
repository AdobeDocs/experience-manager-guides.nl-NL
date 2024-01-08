---
title: Niet-UUID-inhoud met versies vanuit de gebruikersinterface converteren naar UUID-inhoud
description: Leer hoe u niet-UUID-inhoud migreert met 4.3.x-versies.
source-git-commit: f18c19eb493cd4d2003f68b082e71ebe7b3e6b7a
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Niet-UUID-inhoud migreren met versies vanuit de gebruikersinterface

Als u versie 4.3.x of later gebruikt, voert u deze stappen uit om uw niet-UUID-inhoud met versies te migreren naar UUID-inhoud.

## Compatibiliteitsmatrix

| Huidige versie van AEM (niet-UUID) | Vereiste versie voor migratie naar UUID | Ondersteund upgradepad |
|---|---|---|
| 4.3.x of hoger | 4.3.0 niet-UUID | 4.3.1 (UUID) installeren |

## Vereiste pakketten

1. **Versieverwijdering**: `com.adobe.guides.version-purge-1.0.11.zip` (optioneel)
1. **Pre-migratie**: `com.adobe.guides.pre-uuid-migration-1.1.2 .zip`
1. **Migratie**: `com.adobe.guides.uuid-upgrade-1.1.13.zip`



## Pre-migratie

1. (Optioneel) Voer versiebeheer uit op de inhoud om overbodige versies te verwijderen en het migratieproces te versnellen. Installeer het pakket om versiebeheer uit te voeren op versie 4.1 (NIET ondersteund op 4.0) `com.adobe.guides.version-purge-1.0.11.zip`en ga naar de gebruikersinterface met deze URL `http://<server-name> /libs/fmdita/clientlibs/xmleditor_version_purge/page.html`.

   >[!NOTE]
   >
   >Dit hulpprogramma verwijdert geen versies die in basislijnen of revisies worden gebruikt of heeft labels.
1. Het pre-migratiepakket installeren (`ccom.adobe.guides.pre-uuid-migration-1.1.2 .zip`).

   >[!NOTE]
   >
   >* U hebt beheerdersmachtigingen nodig om de migratie uit te voeren.
   >* Het wordt aanbevolen de bestanden met fouten te corrigeren voordat u verdergaat met de migratie.

1. Selecteren **Compatibiliteitsbeoordeling**  in het linkerdeelvenster en bladert u door een mappad.
1. Controleer de compatibiliteit om de volgende informatie weer te geven:
   * Totaal aantal bestanden
   * Totaal aantal versies
   * Geschatte tijd voor migratie
   * Aantal bestanden met fouten



![compatibiliteitsbeoordelingstabblad in migratie](assets/migration-compatibility-assessment.png){width="800" align="left"}


1. Selecteren **Validaties configureren** in het linkerdeelvenster. Vervolgens **Kaart selecteren** en **Voorinstelling selecteren** van de kaart om hen te vormen. De huidige lijst van de outputbevestiging zal de outputdossiers tonen aanwezig vóór migratie en kan tegen de outputdossiers worden bevestigd die na migratie later worden geproduceerd.

![Tabblad Validaties configureren in migratie](assets/migration-configure-validation.png){width="800" align="left"}




## Migratie

### Stap 1: Configuratie bijwerken

1. Zorg ervoor dat de beschikbare vrije ruimte ten minste tien keer zo groot is als AEM (crx-quickstart-map) tijdens de migratie. Wanneer u de migratie hebt voltooid, kunt u het grootste deel van de schijfruimte vrijmaken door een compactie uit te voeren (raadpleeg [Revisie opschonen](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=en)).

1. Inschakelen *Launchers voor naverwerking inschakelen* in `com.adobe.fmdita.config.ConfigManager` en *Version Postprocessing inschakelen* in `com.adobe.fmdita.postprocess.version.PostProcessVersionObservation.`

1. Installeer de UUID-versie van de ondersteunde versie op de niet-UUID-versie. Als u bijvoorbeeld een 4.0-build zonder UUID of een 4.1-build zonder UUID gebruikt, moet u UUID-versie 4.1 installeren.

1. Installeer het nieuwe pakket voor uuid-migratie (`com.adobe.guides.uuid-upgrade-1.1.13`).

1. De volgende workflows uitschakelen en eventuele andere workflows uitschakelen die worden uitgevoerd `/content/dam` draagraketten gebruiken in `http://localhost:4502/libs/cq/workflow/content/console.html`.

   * Workflow voor DAM-update-middelen
   * DAM-workflow Metagegevens terugschrijven

1. Uitschakelen *Launchers voor naverwerking inschakelen* in `com.adobe.fmdita.config.ConfigManager` en uitschakelen *Version Postprocessing inschakelen* in `com.adobe.fmdita.postprocess.version.PostProcessVersionObservation`.

1. De eigenschap Validatie inschakelen uitschakelen (`validation.enabled`) in Day CQ Tagging Service.

1. Zorg ervoor dat `uuid.regex` eigenschapmap is ingesteld in `com.adobe.fmdita.config.ConfigManager`. Als deze leeg is, stelt u de standaardwaarde in - `^GUID-(?<id>.*)`.
1. Een afzonderlijk logger toevoegen voor `com.adobe.fmdita.uuid.upgrade.UuidUpgrade` De browserreactie is ook beschikbaar op `/content/uuid-upgrade/logs`.

### Stap 2: De migratie uitvoeren en valideren

#### Het migratiepakket installeren

![Tabblad Systeemupgrade voor migratie](assets/migration-system-upgrade.png){width="800" align="left"}

* Selecteren **Systeemupgrade** vanuit het linkerdeelvenster om de migratie uit te voeren. Begin op een omslag met kleinere gegevens alvorens het te lopen `/content/dam`.

* Selecteren **Rapport downloaden** tijdens het uitvoeren van de migratie om te controleren of alle bestanden in de map correct zijn bijgewerkt en of alle functies alleen voor die map werken.


>[!NOTE]
>
> De migratie van de inhoud kan op een omslagniveau of volledig worden in werking gesteld `/content/dam` of in dezelfde map (migratie opnieuw uitvoeren).

Daarnaast is het belangrijk om ervoor te zorgen dat de migratie van inhoud ook wordt uitgevoerd voor alle media-elementen, zoals afbeeldingen en afbeeldingen die u in de DITA-inhoud hebt gebruikt.

#### Migratie van basislijn en revisie

Selecteren **Upgrade basislijn/revisie** in het linkerdeelvenster om de basislijnen te migreren en deze op mapniveau te bekijken.

![Baseline- en revisietabblad in migratie](assets/migration-baseline-review-upgrade.png){width="800" align="left"}


### Stap 3: Herstel de configuratie

Nadat de server is gemigreerd, kunt u naverwerking, codering en de volgende workflows (inclusief alle andere workflows die aanvankelijk tijdens de migratie zijn uitgeschakeld) inschakelen om te blijven werken op de server.

* Workflow voor DAM-update-middelen
* DAM-metagegevensworkflow

>[!NOTE]
>
>Als sommige bestanden niet worden verwerkt of vóór de migratie zijn beschadigd, worden ze vóór de migratie beschadigd en blijven ze zelfs na de migratie beschadigd.

## Migratievalidatie

Als de migratie is voltooid, selecteert u **Systeemupgrade valideren** in het linkerdeelvenster en valideer de uitvoerbestanden voor en na de migratie om ervoor te zorgen dat de migratie is gelukt.

![Tabblad Systeemupgrade bij migratie valideren](assets/migration-validate-system-upgrade.png){width="800" align="left"}


1. Wanneer de migratie is voltooid, kan het grootste deel van de schijfruimte worden teruggewonnen door compactie uit te voeren (verwijs naar `https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=en`).

