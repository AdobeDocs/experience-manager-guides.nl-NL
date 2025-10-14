---
title: Andere functies in de Kaarteditor
description: Ontdek enkele veelvoorkomende functies in de Kaarteditor. Leer hoe u belangrijke verwijzingen kunt oplossen in de Kaarteditor.
exl-id: f0e7a402-ac12-4c63-9d7f-92567ee29a39
feature: Authoring, Map Editor
role: User
source-git-commit: 41c6e4edb470038c4934c01f1c28539f1e4d4f86
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---

# Extra functies in de Kaarteditor {#id1942D0T0HUI}

Enkele veelvoorkomende functies in de Kaarteditor zijn:

## Belangrijke verwijzingen oplossen {#id176GD01H05Z}

Een verwijzing naar een DITA-inhoudssleutel of `conkeyref` is een mechanisme om een deel van de inhoud van het ene onderwerp in een ander onderwerp in te voegen. Dit mechanisme gebruikt sleutel om van de inhoud de plaats te bepalen om te hergebruiken eerder dan het directe inhoud verwijzende mechanisme. Voor meer informatie over direct en indirect van verwijzingen voorzien in DITA, mening *DITA richtend* in de Specificatie van de Taal van OASIS DITA.

Als het onderwerp DITA bijbehorende zeer belangrijke verwijzingen heeft, dan moeten zij worden opgelost alvorens, een onderwerp te previewing uit te geven of te herzien.

De belangrijkste verwijzingen worden opgelost op basis van de wortelkaart die in de volgende orde van prioriteit wordt geplaatst:

1. Gebruikersvoorkeuren
1. Deelvenster Kaartweergave
1. Mapprofiel

De hoofdmap die u in de gebruikersvoorkeuren hebt geselecteerd, krijgt de hoogste prioriteit om toetsverwijzingen op te lossen, gevolgd door het deelvenster Kaartweergave en de hoofdmap van het mapprofiel. Als er dus geen kaart is ingesteld in de gebruikersvoorkeuren, wordt de kaart gebruikt die is geopend in het deelvenster Kaartweergave. Als er geen kaart is geopend in het deelvenster Kaartweergave, wordt de kaart die is ingesteld in de Mapprofielen gebruikt om de toetsverwijzingen op te lossen.

De belangrijkste verwijzingen kunnen binnen een DITA kaartdossier of een afzonderlijk DITA- dossier worden opgeslagen. In Experience Manager Guides, kunt u zeer belangrijke verwijzingen of op het projectniveau of een zittingsniveau specificeren. Als er al een hoofdmap is gedefinieerd voor de gebruikerssessie, wordt deze gebruikt voor het oplossen van de toetsen. Anders wordt de standaardhoofdmap voor die map gebruikt. Als er geen standaardhoofdmap is geconfigureerd, worden de ontbrekende toetsverwijzingen gemarkeerd voor de gebruiker.

Er zijn verscheidene manieren om zeer belangrijke verwijzingen in een onderwerp op te lossen DITA door de kaart te bepalen DITA die op de volgende plaatsen moet worden gebruikt:

**de eigenschappen van het Project** - u kunt een wortelkaart voor het oplossen van zeer belangrijke verwijzingen bepalen terwijl het creëren van een Project in de sectie van de Eigenschappen van het Project.

Deze hoofdmap is van toepassing op alle elementen \(mappen en submappen\) die bij dat project horen. Voor inhoud die in veelvoudige projecten van verwijzingen wordt voorzien, wordt een alfabetische lijst van projecten gehandhaafd en de standaardwortelkaart verbonden aan het eerste project wordt gebruikt. U kunt ook de DITA-kaart kiezen die u wilt gebruiken in de lijst voor het oplossen van toetsverwijzingen.

**voorproef van het Onderwerp** - op de wijze van de onderwerpvoorproef, selecteer het Zeer belangrijke pictogram van de Resolutie in de toolbar en selecteer het DITA- dossier dat voor zeer belangrijke verwijzingen moet worden gebruikt.

**het Onderwerp geeft mening** uit - selecteer het Zeer belangrijke pictogram van de Resolutie terwijl het uitgeven van een onderwerp DITA en selecteer het DITA- dossier voor het oplossen van de belangrijkste verwijzingen te gebruiken.

## Navigatieverwijzingen toevoegen

Het element `navref` wordt gebruikt binnen een kaart DITA om navigatieverwijzingen van een andere kaart te omvatten DITA. Op deze manier kunnen auteurs de navigatiestructuur, zoals gedeelde menu&#39;s of koppelingen, opnieuw gebruiken zonder de feitelijke inhoud van de structuurafbeelding waarnaar wordt verwezen, samen te voegen in de uitvoer.

>[!NOTE]
>
> Het element `navref` is uitsluitend bedoeld voor navigatiedoeleinden binnen de structuur van de kaart. Het draagt niet bij aan de gegenereerde DITA-kaartuitvoer en is uitgesloten van verwerking en weergave in de Kaartweergave, Rapporten, Basislijn, Vertaling en Voorvertoning.

Voer de volgende stappen uit om navigatiereferenties toe te voegen aan een kaart:

1. Open het DITA-kaartbestand waar u een navigatieverwijzing wilt toevoegen.

   Het kaartbestand wordt geopend in de Kaarteditor.
1. Schakel over naar de weergave Auteur en plaats de cursor op een geldige locatie voor een navigatieverwijzing.
1. Selecteer de **optie van het Element** van de toolbar.
1. In het **element van het Tussenvoegsel** dialoog, uitgezochte **navref**.

   ![](./images/select-navref-element.png)
1. De **Uitgezochte weg** dialoog wordt getoond. Selecteer een kaartdossier u als navigatieverwijzing in uw kaart wilt omvatten, en **Uitgezocht** kiezen.

Er wordt een navigatieverwijzing van het geselecteerde kaartbestand toegevoegd op de opgegeven locatie. De titel van de structuurafbeelding waarnaar wordt verwezen, wordt zowel in de weergave Auteur als in de layoutweergave weergegeven.

![](./images/navref-added-author-view.png)

*de mening van de Auteur*

![](./images/navref-added-layout-view.png)

*mening van de Lay-out*


**Bovenliggend onderwerp:**&#x200B;[&#x200B; Inleiding aan de Redacteur van de Kaart &#x200B;](map-editor.md)
