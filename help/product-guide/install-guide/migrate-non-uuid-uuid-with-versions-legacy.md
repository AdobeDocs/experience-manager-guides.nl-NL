---
title: Niet-UUID-inhoud met versies omzetten in UUID-inhoud
description: Leer hoe u niet-UUID-inhoud met versies naar UUID-inhoud migreert.
feature: Migration
role: Admin
level: Experienced
exl-id: 8f3a89fc-7d18-453d-909d-6dff5e275cab
source-git-commit: f86d8f2d2e6aa48941cf16526e608df4845420fd
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 0%

---

# Inhoud met versiebeheer migreren

>[!NOTE]
>
> U kunt niet-UUID-inhoud migreren naar UUID-inhoud in Experience Manager Guides. Dit artikel wordt in november 2024 gearchiveerd.
>De mening [**niet-UUID aan de inhoudsmigratie van UUID**](./migrate-non-uuid-uuid.md) voor de recentste en gedetailleerde documentatie.

Voer de volgende stappen uit om uw inhoud zonder UUID-versie te migreren naar UUID-inhoud.

>[!NOTE]
>
>Volg de [ verbeteringsinstructies ](./upgrade-xml-documentation.md) specifiek voor de vergunning gegeven versie van uw product.

## Compatibiliteitsmatrix

| Huidige Experience Manager Guides-versie (niet-UUID) | Vereiste versie voor migratie naar UUID | Ondersteund upgradepad |
|---|---|---|
| 3.8.5, 4.0.x of 4.1.x | 4.1 niet-UUID | 4.1 (UUID) installeren en de migratie uitvoeren |
| 4.2, 4.2.x of 4.3 | 4.3.0 niet-UUID | 4.3.1 (UUID) installeren en de migratie uitvoeren |
| 4.3.1. | NA | NA |

## Pakketinstallatie

Download de vereiste pakketten van het Portaal van de Distributie van de Software van de Adobe, die op uw versie wordt gebaseerd:
<details>
<summary>  Pakketten voor het upgradepad van versie 4.1</summary>

1. **pre-migratie**: [ com.adobe.guides.pre-uuid-migratie-1.0.9.zip ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2Fother-packages%2Fuuid-migration%2F1-0%2Fcom.adobe.guides.pre-uuid-migration-1.0.9.zip)
1. **Migratie**: [ com.adobe.guides.uuid-verbetering-1.0.19.zip ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2Fother-packages%2Fuuid-migration%2F1-0%2Fcom.adobe.guides.uuid-upgrade-1.0.19.zip)
</details>


<details>
<summary> Pakketten voor het upgradepad van versie 4.3.1</summary>

1. **pre-migratie**: [ com.adobe.guides.pre-uuid-migratie-1.1.3.zip ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2Fother-packages%2Fuuid-migration%2Fcom.adobe.guides.pre-uuid-migration-1.1.3.zip)
1. **Migratie**: [ com.adobe.guides.uuid-verbetering-1.1.15.zip ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2Fother-packages%2Fuuid-migration%2Fcom.adobe.guides.uuid-upgrade-1.1.15.zip)

</details>

## Pre-migratie

Voer de volgende controles uit op de niet-UUID-versie (4.1 niet-UUID of 4.3.0 niet-UUID):

1. Installeer het pre-migratiepakket volgens uw versie.

   >[!NOTE]
   >
   >* U hebt beheerdersmachtigingen nodig om de migratie uit te voeren.
   >* Het wordt aanbevolen de bestanden met fouten te corrigeren voordat u verdergaat met de migratie.

1. (Optioneel) Voer versiebeheer uit op de inhoud om overbodige versies te verwijderen en het migratieproces te versnellen. Om versie het zuiveren uit te voeren, selecteer de optie **Woorden van de Versie** van het migratiescherm en ga naar het gebruikersinterface gebruikend URL `http://<server- name>/libs/fmdita/clientlibs/xmleditor_uuid_upgrade/page.html`.
   >[!NOTE]
   >
   >Dit hulpprogramma verwijdert geen versies die in basislijnen of revisies worden gebruikt of heeft labels.

1. Start `http://<server-name>/libs/fmdita/clientlibs/xmleditor_uuid_upgrade/page.html` .
1. Selecteer **Beoordeling van de Verenigbaarheid** van het linkerpaneel en doorblader een omslagweg.
1. Controleer de compatibiliteit om de volgende informatie weer te geven:
   * Totaal aantal bestanden
   * Totaal aantal versies
   * Geschatte tijd voor migratie
   * Aantal bestanden met fouten

   ![ lusje van de verenigbaarheidsbeoordeling in migratie ](assets/migration-compatibility-assessment.png){width="800" align="left"}


1. Selecteer **vormen Bevestigingen** van het linkerpaneel. Dan, **Uitgezochte kaart** en **Uitgezochte vooraf ingesteld** van de kaart om hen te vormen. De huidige lijst van de outputbevestiging toont de outputdossiers aanwezig vóór migratie en kan tegen de outputdossiers worden bevestigd die na migratie later worden geproduceerd.

   ![ vormt het lusje van Bevestigingen in migratie ](assets/migration-configure-validation.png){width="800" align="left"}




## Migratie

### Stap 1: Configuratie bijwerken

1. Zorg ervoor dat de beschikbare vrije ruimte ten minste tien keer zo groot is als AEM (crx-quickstart-map) tijdens de migratie. Zodra u de migratie voltooit, kunt u het grootste deel van de schijfruimte terugwinnen door compilatie in werking te stellen (verwijs naar [ Opruiming van de Revisie ](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=nl-NL)).

1. Laat *toe de Lancers van het Werkschema van de PostProcessing* in `com.adobe.fmdita.config.ConfigManager` toe en *laat Versie post-processing* in `com.adobe.fmdita.postprocess.version.PostProcessVersionObservation.` toe

1. Installeer de UUID-versie van de ondersteunde versie op de niet-UUID-versie. Als u bijvoorbeeld 4.1 niet-UUID-build gebruikt, moet u UUID-versie 4.1 installeren en de migratie uitvoeren.

1. Installeer het nieuwe pakket voor uuid-migratie.

1. Schakel de volgende workflows en een andere workflow uit die op `/content/dam` wordt uitgevoerd met behulp van draagraketten in `http://<server-name>/libs/cq/workflow/content/console.html` .

   * Workflow voor DAM-update-middelen
   * DAM-workflow Metagegevens terugschrijven

1. Schakel *toe laat de Lanceerders van het Werkschema van de Post- Verwerking* in `com.adobe.fmdita.config.ConfigManager` en maak *toe laat Versie post-processing* in `com.adobe.fmdita.postprocess.version.PostProcessVersionObservation`.

1. Schakel de eigenschap Validatie inschakelen (`validation.enabled`) in CQ-tagservice op dag uit.

1. Controleer of de eigenschapmap `uuid.regex` juist is ingesteld in `com.adobe.fmdita.config.ConfigManager` . Als de waarde leeg is, stelt u deze in op de standaardwaarde - `^GUID-(?<id>.*)` .
1. Voeg een apart logger toe voor `com.adobe.fmdita.uuid` De browserreactie is ook beschikbaar via `/content/uuid-upgrade/logs` .

### Stap 2: De migratie uitvoeren en valideren

#### Het migratiepakket installeren

1. Start `http://<server-name>/libs/fmdita/clientlibs/xmleditor_uuid_upgrade/page.html` .

   ![ de verbeteringslusje van het Systeem in migratie ](assets/migration-system-upgrade.png){width="800" align="left"}

1. Selecteer **verbetering van het Systeem** van het linkerpaneel om de migratie in werking te stellen. Start op een map met kleinere gegevens voordat u deze uitvoert op `/content/dam` .

1. Selecteer **Rapport van de Download** terwijl de migratie loopt om te controleren of alle dossiers in de omslag correct worden bevorderd en of alle eigenschappen slechts voor die omslag werken.


>[!NOTE]
>
> De migratie van de inhoud kan op een omslagniveau, volledige `/content/dam`, of de zelfde omslag (herun migratie) worden in werking gesteld.

Het is ook belangrijk om ervoor te zorgen dat de migratie van inhoud wordt uitgevoerd voor alle media-elementen, zoals afbeeldingen en afbeeldingen die u hebt gebruikt in de DITA-inhoud.

#### Migratie van basislijn en revisie

Selecteer **Verbetering van de Basislijn/van het Overzicht** van het linkerpaneel om de basislijnen en overzicht op het omslagniveau te migreren.

![ Basislijn en overzicht lusje in migratie ](assets/migration-baseline-review-upgrade.png){width="800" align="left"}


### Stap 3: Herstel de configuratie

Nadat de server is gemigreerd, kunt u naverwerking, codering en de volgende workflows (inclusief alle andere workflows die aanvankelijk tijdens de migratie waren uitgeschakeld) inschakelen om te blijven werken op de server.

* Workflow voor DAM-update-middelen
* DAM-metagegevensworkflow

>[!NOTE]
>
>Als sommige bestanden niet worden verwerkt of beschadigd voordat ze worden gemigreerd, zijn ze vóór de migratie beschadigd en blijven ze zelfs na de migratie beschadigd.

## Migratievalidatie

1. Zodra de migratie wordt voltooid, bevestigt de uitgezochte **systeemverbetering** van het linkerpaneel en bevestigt de outputdossiers vóór en na de migratie om ervoor te zorgen dat de migratie succesvol is.

   ![ bevestigt systeemverbeteringslusje in migratie ](assets/migration-validate-system-upgrade.png){width="800" align="left"}


1. Nadat de validatie is uitgevoerd, kan het grootste deel van de schijfruimte worden vrijgemaakt door compactie uit te voeren (zie `https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=nl-NL`).
