---
title: Niet-UUID-inhoud met versies omzetten in UUID-inhoud
description: Leer hoe u niet-UUID-inhoud met versies naar UUID-inhoud migreert.
source-git-commit: 0d985688af601ca51822b116ea4baafce19f0658
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Inhoud met versiebeheer migreren

Voer de volgende stappen uit om uw inhoud zonder UUID-versie te migreren naar UUID-inhoud.

>[!NOTE]
>
>Volg de [upgradeinstructies](./upgrade-xml-documentation.md) specifiek voor de versie van uw product met licentie.

## Compatibiliteitsmatrix

| Huidige versie van hulplijnen voor Experience Managers (niet-UUID) | Vereiste versie voor migratie naar UUID | Ondersteund upgradepad |
|---|---|---|
| 3.8.5, 4.0.x of 4.1.x | 4.1 niet-UUID | 4.1 (UUID) installeren en de migratie uitvoeren |
| 4.2, 4.2.x of 4.3 | 4.3.0 niet-UUID | 4.3.1 (UUID) installeren en de migratie uitvoeren |
| 4.3.1. | NA | NA |

## Pakketinstallatie

Download de vereiste pakketten van het Portaal van de Distributie van de Software van de Adobe, die op uw versie wordt gebaseerd:
<details>
<summary>  Pakketten voor het upgradepad van versie 4.1</summary>

1. **Pre-migratie**: [com.adobe.guides.pre-uuid-migration-1.0.9.zip](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2Fother-packages%2Fuuid-migration%2F1-0%2Fcom.adobe.guides.pre-uuid-migration-1.0.9.zip)
1. **Migratie**: [com.adobe.guides.uuid-upgrade-1.0.19.zip](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2Fother-packages%2Fuuid-migration%2F1-0%2Fcom.adobe.guides.uuid-upgrade-1.0.19.zip)
</details>


<details>
<summary> Pakketten voor het upgradepad van versie 4.3.1</summary>

1. **Pre-migratie**: [com.adobe.guides.pre-uuid-migration-1.1.3.zip](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2Fother-packages%2Fuuid-migration%2Fcom.adobe.guides.pre-uuid-migration-1.1.3.zip)
1. **Migratie**: [com.adobe.guides.uuid-upgrade-1.1.15.zip](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2Fother-packages%2Fuuid-migration%2Fcom.adobe.guides.uuid-upgrade-1.1.15.zip)

</details>

## Pre-migratie

Voer de volgende controles uit op de niet-UUID-versie (4.1 niet-UUID of 4.3.0 niet-UUID):

1. Installeer het pre-migratiepakket volgens uw versie.

   >[!NOTE]
   >
   >* U hebt beheerdersmachtigingen nodig om de migratie uit te voeren.
   >* Het wordt aanbevolen de bestanden met fouten te corrigeren voordat u verdergaat met de migratie.
1. (Optioneel) Voer versiebeheer uit op de inhoud om overbodige versies te verwijderen en het migratieproces te versnellen. Selecteer de optie als u versiereiniging wilt uitvoeren **Versie wissen** vanuit het migratiescherm en ga naar de gebruikersinterface met de URL `http://<server-name>/libs/fmdita/clientlibs/xmleditor_uuid_upgrade/page.html`.
   >[!NOTE]
   >
   >Dit hulpprogramma verwijdert geen versies die in basislijnen of revisies worden gebruikt of heeft labels.
1. Starten `http://<server-name>/libs/fmdita/clientlibs/xmleditor_uuid_upgrade/page.html`.
1. Selecteren **Compatibiliteitsbeoordeling**  in het linkerdeelvenster en bladert u door een mappad.
1. Controleer de compatibiliteit om de volgende informatie weer te geven:
   * Totaal aantal bestanden
   * Totaal aantal versies
   * Geschatte tijd voor migratie
   * Aantal bestanden met fouten



   ![compatibiliteitsbeoordelingstabblad in migratie](assets/migration-compatibility-assessment.png){width="800" align="left"}


1. Selecteren **Validaties configureren** in het linkerdeelvenster. Dan, **Kaart selecteren** en **Voorinstelling selecteren** van de kaart om hen te vormen. De huidige lijst van de outputbevestiging toont de outputdossiers aanwezig vóór migratie en kan tegen de outputdossiers worden bevestigd die na migratie later worden geproduceerd.

   ![Tabblad Validaties configureren in migratie](assets/migration-configure-validation.png){width="800" align="left"}




## Migratie

### Stap 1: Configuratie bijwerken

1. Zorg ervoor dat de beschikbare vrije ruimte ten minste tien keer zo groot is als AEM (crx-quickstart-map) tijdens de migratie. Wanneer u de migratie hebt voltooid, kunt u het grootste deel van de schijfruimte vrijmaken door een compactie uit te voeren (raadpleeg [Revisie opschonen](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=en)).

1. Inschakelen *Launchers voor naverwerking inschakelen* in `com.adobe.fmdita.config.ConfigManager` en *Version Postprocessing inschakelen* in `com.adobe.fmdita.postprocess.version.PostProcessVersionObservation.`

1. Installeer de UUID-versie van de ondersteunde versie op de niet-UUID-versie. Als u bijvoorbeeld 4.1 niet-UUID-build gebruikt, moet u UUID-versie 4.1 installeren en de migratie uitvoeren.

1. Installeer het nieuwe pakket voor uuid-migratie.

1. De volgende workflows uitschakelen en eventuele andere workflows uitschakelen die worden uitgevoerd `/content/dam` draagraketten gebruiken in `http://<server-name>/libs/cq/workflow/content/console.html`.

   * Workflow voor DAM-update-middelen
   * DAM-workflow Metagegevens terugschrijven

1. Uitschakelen *Launchers voor naverwerking inschakelen* in `com.adobe.fmdita.config.ConfigManager` en uitschakelen *Version Postprocessing inschakelen* in `com.adobe.fmdita.postprocess.version.PostProcessVersionObservation`.

1. De eigenschap Validatie inschakelen uitschakelen (`validation.enabled`) in Day CQ Tagging Service.

1. Zorg ervoor dat `uuid.regex` eigenschapmap is ingesteld in `com.adobe.fmdita.config.ConfigManager`. Als deze leeg is, stelt u de standaardwaarde in - `^GUID-(?<id>.*)`.
1. Een afzonderlijk logger toevoegen voor `com.adobe.fmdita.uuid` De browserreactie is ook beschikbaar op `/content/uuid-upgrade/logs`.

### Stap 2: De migratie uitvoeren en valideren

#### Het migratiepakket installeren

1. Starten `http://<server-name>/libs/fmdita/clientlibs/xmleditor_uuid_upgrade/page.html`.

   ![Tabblad Systeemupgrade voor migratie](assets/migration-system-upgrade.png){width="800" align="left"}

1. Selecteren **Systeemupgrade** vanuit het linkerdeelvenster om de migratie uit te voeren. Begin op een omslag met kleinere gegevens alvorens het te lopen `/content/dam`.

1. Selecteren **Rapport downloaden** tijdens het uitvoeren van de migratie om te controleren of alle bestanden in de map correct zijn bijgewerkt en of alle functies alleen voor die map werken.


>[!NOTE]
>
> De migratie van de inhoud kan op een omslagniveau, volledig worden in werking gesteld `/content/dam`of dezelfde map (opnieuw uitvoeren).

Het is ook belangrijk om ervoor te zorgen dat de migratie van inhoud wordt uitgevoerd voor alle media-elementen, zoals afbeeldingen en afbeeldingen die u hebt gebruikt in de DITA-inhoud.

#### Migratie van basislijn en revisie

Selecteren **Upgrade basislijn/revisie** in het linkerdeelvenster om de basislijnen te migreren en deze op mapniveau te bekijken.

![Baseline- en revisietabblad in migratie](assets/migration-baseline-review-upgrade.png){width="800" align="left"}


### Stap 3: Herstel de configuratie

Nadat de server is gemigreerd, kunt u naverwerking, codering en de volgende workflows (inclusief alle andere workflows die aanvankelijk tijdens de migratie waren uitgeschakeld) inschakelen om te blijven werken op de server.

* Workflow voor DAM-update-middelen
* DAM-metagegevensworkflow

>[!NOTE]
>
>Als sommige bestanden niet worden verwerkt of beschadigd voordat ze worden gemigreerd, zijn ze vóór de migratie beschadigd en blijven ze zelfs na de migratie beschadigd.

## Migratievalidatie

1. Als de migratie is voltooid, selecteert u **Systeemupgrade valideren** in het linkerdeelvenster en valideer de uitvoerbestanden voor en na de migratie om ervoor te zorgen dat de migratie is gelukt.

   ![Tabblad Systeemupgrade bij migratie valideren](assets/migration-validate-system-upgrade.png){width="800" align="left"}


1. Nadat de validatie is uitgevoerd, kan het grootste deel van de schijfruimte worden vrijgemaakt door compactie uit te voeren (zie `https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=en`).

