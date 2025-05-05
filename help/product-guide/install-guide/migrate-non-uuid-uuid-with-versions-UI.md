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

| Huidige AEM Guides-versie (niet-UUID) | Vereiste versie voor migratie naar UUID | Ondersteund upgradepad |
|---|---|---|
| 4.3.x of hoger | 4.3.0 niet-UUID | 4.3.1 (UUID) installeren |

## Vereiste pakketten

1. **Wissen van de Versie**: `com.adobe.guides.version-purge-1.0.11.zip` (facultatief)
1. **pre-migratie**: `com.adobe.guides.pre-uuid-migration-1.1.2 .zip`
1. **Migratie**: `com.adobe.guides.uuid-upgrade-1.1.13.zip`



## Pre-migratie

1. (Optioneel) Voer versiebeheer uit op de inhoud om overbodige versies te verwijderen en het migratieproces te versnellen. Als u versiereiniging wilt uitvoeren op versie 4.1 (NIET ondersteund op 4.0), installeert u het pakket `com.adobe.guides.version-purge-1.0.11.zip` en gaat u naar de gebruikersinterface met deze URL `http://<server-name> /libs/fmdita/clientlibs/xmleditor_version_purge/page.html` .

   >[!NOTE]
   >
   >Dit hulpprogramma verwijdert geen versies die in basislijnen of revisies worden gebruikt of heeft labels.
1. Installeer het pre-migratiepakket (`ccom.adobe.guides.pre-uuid-migration-1.1.2 .zip`).

   >[!NOTE]
   >
   >* U hebt beheerdersmachtigingen nodig om de migratie uit te voeren.
   >* Het wordt aanbevolen de bestanden met fouten te corrigeren voordat u verdergaat met de migratie.

1. Selecteer **Beoordeling van de Verenigbaarheid** van het linkerpaneel en doorblader een omslagweg.
1. Controleer de compatibiliteit om de volgende informatie weer te geven:
   * Totaal aantal bestanden
   * Totaal aantal versies
   * Geschatte tijd voor migratie
   * Aantal bestanden met fouten



![ lusje van de verenigbaarheidsbeoordeling in migratie ](assets/migration-compatibility-assessment.png){width="800" align="left"}


1. Selecteer **vormen Bevestigingen** van het linkerpaneel. Dan **Uitgezochte kaart** en **Uitgezochte vooraf ingesteld** van de kaart om hen te vormen. De huidige lijst van de outputbevestiging zal de outputdossiers tonen aanwezig vóór migratie en kan tegen de outputdossiers worden bevestigd die na migratie later worden geproduceerd.

![ vormt het lusje van Bevestigingen in migratie ](assets/migration-configure-validation.png){width="800" align="left"}




## Migratie

### Stap 1: Configuratie bijwerken

1. Zorg ervoor dat de beschikbare vrije ruimte ten minste tien keer zo groot is als AEM (crx-quickstart-map) tijdens de migratie. Zodra u de migratie voltooit, kunt u het grootste deel van de schijfruimte terugwinnen door compilatie in werking te stellen (verwijs naar [ Opruiming van de Revisie ](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=nl-NL)).

1. Laat *toe de Lancers van het Werkschema van de Verwerking van Post* in `com.adobe.fmdita.config.ConfigManager` toe en *laat Versie post-processing* in `com.adobe.fmdita.postprocess.version.PostProcessVersionObservation.` toe

1. Installeer de UUID-versie van de ondersteunde versie op de niet-UUID-versie. Als u bijvoorbeeld een 4.0-build zonder UUID of een 4.1-build zonder UUID gebruikt, moet u UUID-versie 4.1 installeren.

1. Installeer het nieuwe pakket voor uuid migratie (`com.adobe.guides.uuid-upgrade-1.1.13`).

1. Schakel de volgende workflows en een andere workflow uit die op `/content/dam` wordt uitgevoerd met behulp van draagraketten in `http://localhost:4502/libs/cq/workflow/content/console.html` .

   * Workflow voor DAM-update-middelen
   * DAM-workflow Metagegevens terugschrijven

1. Schakel *toe laat de Lancers van het Werkschema van de Verwerking van Post* in `com.adobe.fmdita.config.ConfigManager` toe en maak *toe laat Versie post-processing* in `com.adobe.fmdita.postprocess.version.PostProcessVersionObservation`.

1. Schakel de eigenschap Validatie inschakelen (`validation.enabled`) in CQ-tagservice op dag uit.

1. Controleer of de eigenschapmap `uuid.regex` juist is ingesteld in `com.adobe.fmdita.config.ConfigManager` . Als de waarde leeg is, stelt u deze in op de standaardwaarde - `^GUID-(?<id>.*)` .
1. Voeg een apart logger toe voor `com.adobe.fmdita.uuid.upgrade.UuidUpgrade` De browserreactie is ook beschikbaar via `/content/uuid-upgrade/logs` .

### Stap 2: De migratie uitvoeren en valideren

#### Het migratiepakket installeren

![ de verbeteringslusje van het Systeem in migratie ](assets/migration-system-upgrade.png){width="800" align="left"}

* Selecteer **verbetering van het Systeem** van het linkerpaneel om de migratie in werking te stellen. Start op een map met kleinere gegevens voordat u deze uitvoert op `/content/dam` .

* Selecteer **Rapport van de Download** terwijl de migratie loopt om te controleren of alle dossiers in de omslag correct worden bevorderd en of alle eigenschappen slechts voor die omslag werken.


>[!NOTE]
>
> U kunt de migratie van inhoud uitvoeren op mapniveau, in de volledige map `/content/dam` of in dezelfde map (migratie opnieuw uitvoeren).

Daarnaast is het belangrijk om ervoor te zorgen dat de migratie van inhoud ook wordt uitgevoerd voor alle media-elementen, zoals afbeeldingen en afbeeldingen die u in de DITA-inhoud hebt gebruikt.

#### Migratie van basislijn en revisie

Selecteer **Verbetering van de Basislijn/van het Overzicht** van het linkerpaneel om de basislijnen en overzicht op omslagniveau te migreren.

![ Basislijn en overzicht lusje in migratie ](assets/migration-baseline-review-upgrade.png){width="800" align="left"}


### Stap 3: Herstel de configuratie

Nadat de server is gemigreerd, kunt u naverwerking, codering en de volgende workflows (inclusief alle andere workflows die aanvankelijk tijdens de migratie zijn uitgeschakeld) inschakelen om te blijven werken op de server.

* Workflow voor DAM-update-middelen
* DAM-metagegevensworkflow

>[!NOTE]
>
>Als sommige bestanden niet worden verwerkt of vóór de migratie zijn beschadigd, worden ze vóór de migratie beschadigd en blijven ze zelfs na de migratie beschadigd.

## Migratievalidatie

Zodra de migratie wordt voltooid, bevestigt de uitgezochte **systeemverbetering** van het linkerpaneel en bevestigt de outputdossiers vóór en na de migratie om de migratie succesvol te verzekeren.

![ bevestigt systeemverbeteringslusje in migratie ](assets/migration-validate-system-upgrade.png){width="800" align="left"}


1. Wanneer de migratie is voltooid, kan het grootste deel van de schijfruimte worden teruggespoeld door een compactie uit te voeren (zie `https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=nl-NL`).

