---
title: Inhoud beheren
description: Inhoud beheren en uw rollen en machtigingen in AEM Guides identificeren. Leer de belangrijkste concepten van inhoudsbeheer en het werken met globale of omslag-vlakke profielen.
feature: Content Management
role: User
hide: true
exl-id: 54b960cf-fb00-4d4a-a836-9de4738c49a8
source-git-commit: 7286c3fb36695caa08157296fd6e0de722078c2b
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 0%

---

# Inhoud beheren {#id164JBG0M0T1}

Voordat u begint met het maken van inhoud, moet u bekend zijn met enkele basisbeginselen van contentbeheer in AEM Guides. Begin vervolgens met het maken van verschillende gebruikersgroepen en het ordenen van uw middelen.

## Belangrijkste concepten

Enkele belangrijke concepten voor inhoudsbeheer in AEM zijn:

**Beheer van Activa**

AEM Guides gebruikt AEM Digital Asset Management \(DAM\) om uw DITA-bestanden te beheren. De bestanden die u uploadt of incheckt in de DAM worden opgeslagen als digitale elementen. U kunt uw middelen in AEM Assets beheren en bewerken. Voor meer informatie over activabeheer, zie [ activa ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html?lang=en) beheren.

**het beheer van de Verbinding**

Verplaats of wijzig de naam van bestanden of wijzig de mapstructuur in de opslagplaats voor inhoud zonder dat u zich zorgen hoeft te maken over verbroken verwijzingen. Alle verwijzingen naar en van de beïnvloede inhoud worden automatisch bijgewerkt. Hiermee krijgt u waarschuwingen wanneer u inhoud verwijdert waarnaar elders wordt verwezen, om onbedoelde onderbrekingen te voorkomen.

**het Leiden versies**

AEM Guides biedt versiebeheer voor uw digitale middelen. U kunt deze functionaliteit gemakkelijk van een DITA auteurstoepassing van keus toelaten. Uw schrijvers toestaan de standaardfuncties voor versiebeheer uit te voeren, zoals inchecken en uitchecken.

Voor meer informatie over het creëren van versies of het terugkeren naar een specifieke versie, zie [ Tak, terugkeren, en verdere versioning ](web-editor-preview-topics.md#id193PG0Y051X).

**Inheemse behandeling DITA**

Hoewel AEM Guides de structuur van uw DITA-bestanden behoudt, kan AEM DITA ook op native wijze afhandelen met behulp van elementtoewijzing om de DITA-elementen toe te wijzen aan AEM-componenten. De native DITA-afhandeling wordt gebruikt in functies zoals onderwerpvoorvertoning, AEM Sites-publicatie en de revisieworkflows.

## Uw rol en machtigingen identificeren {#id181TF0K0MHT}

AEM Guides biedt drie groepen buiten de doos. Deze groepen zijn: *Auteurs*, *Recensenten*, en *Uitgevers*. Afhankelijk van de groep waaraan u bent gekoppeld, hebt u machtigingen om specifieke taken uit te voeren, zoals in de onderstaande tabel wordt vermeld. Zo kan het publiceren alleen worden uitgevoerd door een uitgever, maar niet door een auteur of een revisor. Op dezelfde manier kan een auteur een nieuw onderwerp tot stand brengen, en een recensent kan slechts een onderwerp herzien.

>[!TIP]
>
> Zie de *sectie van Toestemmingen* in de Beste praktijken gids voor beste praktijken rond het plaatsen van gebruikerstoestemmingen.

De volgende lijst maakt een lijst van diverse taken en de groepen die die taken kunnen uitvoeren:

| Taak | Auteurs | Revisoren | Uitgevers |
|----|-------|---------|----------|
| DITA-onderwerp maken | Ja |   | Ja |
| DITA-kaart maken | Ja |   | Ja |
| Verzamelingen toewijzen | Ja |   | Ja |
| Revisietaak maken | Ja |   | Ja |
| Het Onderwerp van het overzicht [ 1 ](#fntarg_1) | Ja | Ja | Ja |
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
| De documentstaat van de verandering [ 2 ](#fntarg_2) | Ja | Ja | Ja |
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

[ 1 ](#fnsrc_1) als *Auteurs* en *Uitgevers* voor een overzicht worden uitgenodigd.

[ 2 ](#fnsrc_2) afhankelijk van de rechten die aan de gebruiker in het profiel van de documentstaat worden gegeven.

## Voorwaarden voor het ontwerpen van inhoud

**Werk met globale of omslag-vlakke profielen**

In een onderneming, kunnen de verschillende groepen of de producten verschillende auteursmalplaatjes, outputmalplaatjes, voorwaardelijke attributenprofielen \ (of onderwerpregelingen \), en de configuraties van de Redacteur van het Web gebruiken. Als u deze alleen op ondernemingsniveau \(of algemeen\) configureert, kunnen auteurs problemen ondervinden omdat ze sjablonen of profielen zien die voor hen niet relevant zijn.

Met AEM Guides kunt u ontwerpsjablonen \(onderwerp of kaart\), uitvoersjablonen, voorwaardelijke kenmerken en webeditorconfiguraties op ondernemingsniveau en op mapniveau configureren. Op deze manier kunt u de configuraties voor verschillende afdelingen of producten in uw onderneming van elkaar scheiden.

Ook, kunt u de omslag-specifieke configuraties aan een afdeling of productbeheerders delegeren om het beleid te decentraliseren.

Voor details bij vestiging globale en omslag-vlakke profielen, zie *globale of omslag-vlakke profielen* vormen in installeer en vorm Adobe Experience Manager Guides as a Cloud Service.
