---
title: Inhoud beheren
description: Inhoud beheren en uw rollen en machtigingen in AEM Guides identificeren. Leer de belangrijkste concepten van inhoudsbeheer en het werken met globale of omslag-vlakke profielen.
exl-id: 84926dc2-1180-48ef-85d0-50e3478bf26a
feature: Content Management
role: User
source-git-commit: 461692ce786f914dd196f289efef726e42bf9660
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Inhoud beheren {#id164JBG0M0T1}

Voordat u begint met het maken van inhoud, moet u bekend zijn met enkele basisbeginselen van contentbeheer in Adobe Experience Manager Guides. Begin vervolgens met het maken van verschillende gebruikersgroepen en het ordenen van uw middelen.

## Belangrijkste concepten

Enkele belangrijke concepten voor inhoudsbeheer in Adobe Experience Manager zijn:

**Beheer van Activa**

Experience Manager Guides gebruikt Adobe Experience Manager Digital Asset Management \(DAM\) om uw DITA-bestanden te beheren. De bestanden die u uploadt of incheckt in de DAM worden opgeslagen als digitale elementen. U kunt uw middelen in Adobe Experience Manager Assets beheren en bewerken. Voor meer informatie over activabeheer, mening [&#x200B; beheert activa &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html?lang=nl-NL).

**het beheer van de Verbinding**

Verplaats of wijzig de naam van bestanden of wijzig de mapstructuur in de opslagplaats voor inhoud zonder dat u zich zorgen hoeft te maken over verbroken verwijzingen. Alle verwijzingen naar en van de beïnvloede inhoud worden automatisch bijgewerkt. Hiermee krijgt u waarschuwingen wanneer u inhoud verwijdert waarnaar elders wordt verwezen, om onbedoelde onderbrekingen te voorkomen.

**het Leiden versies**

Experience Manager Guides biedt versiebeheer voor uw digitale middelen. U kunt deze functionaliteit gemakkelijk van een DITA auteurstoepassing van keus toelaten. Uw schrijvers toestaan de standaardfuncties voor versiebeheer uit te voeren, zoals inchecken en uitchecken.

Voor meer informatie over het creëren van versies of het terugkeren naar een specifieke versie, mening [&#x200B; Tak, keer terug, en verdere versioning &#x200B;](web-editor-preview-topics.md#branch-revert-and-subsequent-versioning).

**Inheemse behandeling DITA**

Hoewel Experience Manager Guides de structuur van uw DITA-bestanden behoudt, kan Adobe Experience Manager DITA ook op native wijze afhandelen met behulp van elementtoewijzing om de DITA-elementen toe te wijzen aan Adobe Experience Manager-componenten. De native DITA-afhandeling wordt gebruikt in functies zoals onderwerpvoorvertoning, Adobe Experience Manager Sites-publicatie en de revisieworkflows.

## Uw rol en machtigingen identificeren {#id181TF0K0MHT}

Experience Manager Guides biedt drie groepen buiten de doos. Deze groepen zijn: *Auteurs*, *Recensenten*, en *Uitgevers*. Afhankelijk van de groep waaraan u bent gekoppeld, hebt u machtigingen om specifieke taken uit te voeren, zoals in de onderstaande tabel wordt vermeld. Zo kan het publiceren alleen worden uitgevoerd door een uitgever, maar niet door een auteur of een revisor. Op dezelfde manier kan een auteur een nieuw onderwerp tot stand brengen, en een recensent kan slechts een onderwerp herzien.

>[!TIP]
>
> Bekijk de *sectie van Toestemmingen* in de Beste praktijken gids voor beste praktijken rond het plaatsen van gebruikerstoestemmingen.

De volgende lijst maakt een lijst van diverse taken en de groepen die die taken kunnen uitvoeren:

| Taak | Auteurs | Revisoren | Uitgevers |
|----|-------|---------|----------|
| DITA-onderwerp maken | Ja |   | Ja |
| DITA-kaart maken | Ja |   | Ja |
| Verzamelingen toewijzen | Ja |   | Ja |
| Revisietaak maken | Ja |   | Ja |
| Het Onderwerp van het overzicht [&#x200B; 1 &#x200B;](#fntarg_1) | Ja | Ja | Ja |
| Belangrijkste resolutie | Ja |   | Ja |
| Uitchecken/Inchecken | Ja |   | Ja |
| Onderwerp bewerken | Ja |   | Ja |
| Onderwerp verplaatsen | Ja |   | Ja |
| Eigenschappen van onderwerp bewerken | Ja |   | Ja |
| Kopiëren | Ja |   | Ja |
| Verwijderen | Ja |   | Ja |
| Delen | Ja |   | Ja |
| **de staat van het Document** |
| Profiel documentstatus maken/bewerken |   |   | Ja |
| De documentstaat van de verandering [&#x200B; 2 &#x200B;](#fntarg_2) | Ja | Ja | Ja |
| **Eigenschappen beschikbaar in DITA kaartconsole \ (Output stelt lusje \ vooraf in)** |
| Genereren |   |   | Ja |
| Bewerken |   |   | Ja |
| Dupliceren |   |   | Ja |
| Maken |   |   | Ja |
| Voorinstelling verwijderen |   |   | Ja |
| **Eigenschappen beschikbaar in DITA kaartconsole \ (Output tabel \)** |
| Gegenereerde uitvoer weergeven | Ja |   | Ja |
| **Eigenschappen beschikbaar in DITA kaartconsole \ (Onderwerpen lusje \)** |
| Revisietaak maken | Ja |   | Ja |
| Bewerken | Ja |   | Ja |
| **Eigenschappen beschikbaar in DITA kaartconsole \ (het lusje van Basislijnen \)** |
| Maken |   |   | Ja |
| Bewerken |   |   | Ja |
| Dupliceren |   |   | Ja |
| Verwijderen |   |   | Ja |
| DITA-kaartconsole \(tabblad Rapporten\) | Ja |   | Ja |
| **Eigenschappen beschikbaar in DITA kaartconsole \ (Voorinstellingen van de Voorwaarde \)** |
| Voorinstelling voorwaarde maken/bewerken |   |   | Ja |

[&#x200B; 1 &#x200B;](#fnsrc_1) als *Auteurs* en *Uitgevers* voor een overzicht worden uitgenodigd.

[&#x200B; 2 &#x200B;](#fnsrc_2) afhankelijk van de rechten die aan de gebruiker in het profiel van de documentstaat worden gegeven.
