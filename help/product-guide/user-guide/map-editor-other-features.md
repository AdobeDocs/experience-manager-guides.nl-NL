---
title: Andere functies in de kaarteditors
description: Ontdek enkele veelvoorkomende functies in de Basic- en Advanced Map Editors. Leer hoe u belangrijke verwijzingen in de Kaart-editor kunt oplossen.
exl-id: f0e7a402-ac12-4c63-9d7f-92567ee29a39
feature: Authoring, Map Editor
role: User
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Andere functies in de kaarteditors {#id1942D0T0HUI}

Enkele veelvoorkomende functies in de Basic- en Advanced Map Editors zijn:

## Belangrijke verwijzingen oplossen {#id176GD01H05Z}

Een verwijzing naar een DITA-inhoudssleutel of `conkeyref` is een mechanisme om een deel van de inhoud van het ene onderwerp in een ander onderwerp in te voegen. Dit mechanisme gebruikt sleutel om van de inhoud de plaats te bepalen om te hergebruiken eerder dan het directe inhoud verwijzende mechanisme. Voor meer informatie over direct en indirect van verwijzingen voorzien in DITA, zie *DITA richtend* in de Specificatie van de Taal van OASIS DITA.

Als het onderwerp DITA bijbehorende zeer belangrijke verwijzingen heeft, dan moeten zij worden opgelost alvorens, een onderwerp te previewing uit te geven of te herzien.

De belangrijkste verwijzingen worden opgelost op basis van de wortelkaart die in de volgende orde van prioriteit wordt geplaatst:

1. Gebruikersvoorkeuren
1. Deelvenster Kaartweergave
1. Mapprofiel

De hoofdmap die u in de gebruikersvoorkeuren hebt geselecteerd, krijgt de hoogste prioriteit om toetsverwijzingen op te lossen, gevolgd door het deelvenster Kaartweergave en de hoofdmap van het mapprofiel. Als er dus geen kaart is ingesteld in de gebruikersvoorkeuren, wordt de kaart gebruikt die is geopend in het deelvenster Kaartweergave. Als er geen kaart is geopend in het deelvenster Kaartweergave, wordt de kaart die is ingesteld in de Mapprofielen gebruikt om de toetsverwijzingen op te lossen.

De belangrijkste verwijzingen kunnen binnen een DITA kaartdossier of een afzonderlijk DITA- dossier worden opgeslagen. In AEM Guides, kunt u zeer belangrijke verwijzingen of op het projectniveau of een zittingsniveau specificeren. Als er al een hoofdmap is gedefinieerd voor de gebruikerssessie, wordt deze gebruikt voor het oplossen van de toetsen. Anders wordt de standaardhoofdmap voor die map gebruikt. Als er geen standaardhoofdmap is geconfigureerd, worden de ontbrekende toetsverwijzingen gemarkeerd voor de gebruiker.

Er zijn verscheidene manieren om zeer belangrijke verwijzingen in een onderwerp op te lossen DITA door de kaart te bepalen DITA die op de volgende plaatsen moet worden gebruikt:

**de eigenschappen van het Project** - u kunt een wortelkaart voor het oplossen van zeer belangrijke verwijzingen bepalen terwijl het creëren van een Project in de sectie van de Eigenschappen van het Project.

Deze hoofdmap is van toepassing op alle elementen \(mappen en submappen\) die bij dat project horen. Voor inhoud die in veelvoudige projecten van verwijzingen wordt voorzien, wordt een alfabetische lijst van projecten gehandhaafd en de standaardwortelkaart verbonden aan het eerste project wordt gebruikt. U kunt ook de DITA-kaart kiezen die u wilt gebruiken in de lijst voor het oplossen van toetsverwijzingen.

**voorproef van het Onderwerp** - op de wijze van de onderwerpvoorproef, klik op het Belangrijkste pictogram van de Resolutie in de toolbar en selecteer het DITA- dossier dat voor zeer belangrijke verwijzingen moet worden gebruikt.

**het Onderwerp geeft mening** uit - klik op het Zeer belangrijke pictogram van de Resolutie terwijl het uitgeven van een onderwerp DITA en selecteer het DITA- dossier voor het oplossen van de belangrijkste verwijzingen te gebruiken.

**Bovenliggend onderwerp:**[ Werk met de Redacteur van de Kaart ](map-editor.md)
