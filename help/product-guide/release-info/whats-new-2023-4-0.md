---
title: Opmerkingen bij de release | Adobe Experience Manager Guides as a Cloud Service, release april 2023
description: Release van Adobe Experience Manager Guides as a Cloud Service in april 2023
exl-id: 269e3a13-584d-4cff-a18a-d4fa89646a5a
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Nieuwe functies in april 2023 van Adobe Experience Manager Guides as a Cloud Service

Dit artikel behandelt de nieuwe en verbeterde eigenschappen in versie April 2023 van Adobe Experience Manager Guides (later genoemd als *as a Cloud Service van AEM Guides*).

Voor meer details op de verbeteringsinstructies, verenigbaarheidsmatrijs, en de kwesties die in deze versie worden bevestigd, zie het [ de nota&#39;s van de Versie ](release-notes-2023-4-0.md) artikel.

## Geavanceerde ondersteuning voor metagegevens in PDF-publicaties

AEM Guides biedt nu geavanceerde ondersteuning voor de metagegevens die zijn toegewezen aan de metagegevens in uw PDF-uitvoer. De opties voor metagegevens bevatten informatie over het document en de inhoud ervan, zoals de naam van de auteur, de documenttitel, trefwoorden, copyrightinformatie en andere gegevensvelden.

<img src="assets/pdf-metadata.png" alt=" native PDF-metagegevens">

U kunt een XMP importeren en AEM Guides kan de gegevens uit het bestand kiezen. U kunt ook de namen en waarden van metagegevens opgeven met het vervolgkeuzemenu. U kunt ook aangepaste metagegevens toevoegen door deze rechtstreeks in het naamveld te typen.


## Verbeterd deelvenster Omtrekweergave

AEM Guides biedt een verbeterd deelvenster Omtrekweergave waarin u de hiërarchische weergave kunt bekijken van de elementen die in het document worden gebruikt.

<img src="assets/select-element-content-outline-view_cs.png" alt=" native PDF-metagegevens">

De omtrekweergave biedt de volgende verbeteringen:

* Het vervolgkeuzemenu Weergaveopties wordt boven in het deelvenster Omtrekweergave weergegeven. Als een element een id, kenmerk en tekst heeft, kunt u deze selecteren in het vervolgkeuzemenu en ze samen met het element weergeven. De attributen die in het paneel van de Mening van het Overzicht kunnen worden getoond worden bepaald door de montages van de Attributen van de Vertoning die door uw beheerder binnen de **Montages van de Redacteur** zijn gevormd.

* Met de zoekfunctie kunt u naar een element zoeken op basis van de naam, id, tekst of kenmerkwaarde.


## Op microservices gebaseerde publicaties voor AEM Guides as a Cloud Service

AEM Guides as a Cloud Service biedt de functie om grote publicatiewerklasten tegelijk uit te voeren met op microservices gebaseerde publicaties en het toonaangevende Adobe I/O Runtime-serverloze platform te benutten.

Nu in de versie van April kunt u veelvoudige het publiceren verzoeken tezelfdertijd in werking stellen en bulkoutput van PDF zeer efficiënt produceren gebruikend de op microdienst-gebaseerde Inheemse PDF het publiceren.
Voor meer details, zie [ nieuwe op microservice-gebaseerde het publiceren voor AEM Guides as a Cloud Service ](../knowledge-base/publishing/configure-microservices.md) vormen.
