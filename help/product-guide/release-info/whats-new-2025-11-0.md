---
title: Opmerkingen bij de release | Nieuwe functies in de Adobe Experience Manager Guides 2025.11.0-release
description: Meer informatie over de nieuwe en verbeterde functies in de 2025.11.0-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: a13fdb36efb5cfb548f8e128977469763836537a
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Nieuwe functies in de release van 2025.11.0 (november 2025)

Dit artikel behandelt de nieuwe en verbeterde functies die zijn geïntroduceerd met de release van 2025.11.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor de lijst van kwesties die in deze versie worden bevestigd, mening [ Vaste kwesties in de versie 2025.11.0 ](fixed-issues-2025-11-0.md).

Leer over [ verbeteringsinstructies voor de versie 2025.11.0 ](../release-info/upgrade-instructions-2025-11-0.md).


## Introductie van nieuwe opslagplaats op de startpagina en verbeterde zoekervaring

De Repository, die nu rechtstreeks vanaf de Startpagina toegankelijk is, fungeert als een gecentraliseerde ruimte voor betere ontdekkingsmogelijkheden voor mappen en bestanden. Het kenmerkt gewijd **navigatievenster van de Omslag** en een klantgerichte **tabelvormige mening van Bewaarplaats**. Dankzij de vernieuwde zoek- en filterervaring is het aanzienlijk eenvoudiger om bestanden te zoeken en te zoeken. Voor meer details, zie [ de interface van de Bewaarplaats ](../user-guide/home-page-repository-view.md) kennen.

![](assets/repository-view-home.png){align="left"}

De ervaring met zoeken en filteren voor bestanden in de Editor is nu consistent met de startpagina. Een nieuw [ paneel van het Onderzoek ](../user-guide/search-panel-explorer.md) dat bij de bodem van de interface van de Redacteur wordt gevestigd wordt geïntroduceerd om onderzoeksresultaten te tonen. Bovendien, wordt de Bewaarplaats nu anders genoemd aan **Ontdekkingsreiziger** in de Redacteur, toestaand u om omslagen en dossiers te doorbladeren zoals voordien.

![](assets/search-panel-explorer.png){align="left"}


## Verbeterde indexering voor slimme suggesties in AI Assistant

U kunt de status van elke indexeringspoging voor slimme suggesties in AI Assistant nu eenvoudig bijhouden met nieuwe statusindicatoren: indexeren voltooid, niet synchroon, Bezig en indexeren mislukt. De laatste indexerende tijdstempel wordt nu opgenomen op het mapprofielniveau voor een betere traceerbaarheid. Bovendien worden beperkingen voor bovenliggende en onderliggende mappen afgedwongen wanneer een map of bestandspad wordt opgegeven voor indexering.

Voor meer details, vormt de mening [ AI Medewerker voor slimme hulp en creatie ](../cs-install-guide/conf-folder-level.md#configure-ai-assistant-for-smart-help-and-authoring).

## Prestatieverbeteringen

### Automated B-tree Cleup for optimal performance

Om de efficiëntie van het systeem te handhaven en congestie van de bronnen te voorkomen, worden met een nieuw achtergrondproces regelmatig de B-bomen op systeemniveau gewist. Hierdoor wordt voorkomen dat elementen die niet meer bestaan of tijdelijk zijn toegevoegd, overbodige ruimte innemen.

Het systeem identificeert kandidaten voor schoonmaak intelligent en voert geautomatiseerde verwijdering uit. Bovendien, is deze eigenschap configureerbaar, die Beheerders controle over zijn gedrag geven dat op operationele behoeften wordt gebaseerd.

Voor meer details, vorm de mening [ B-boom schoonmaak ](../cs-install-guide/configure-btree-cleanup-cs.md).

### Verbeterde verwerking van DITA-kaarten met een groot aantal toetsen

U kunt nu naadloos werken met DITA-kaarten die een groot aantal toetsen bevatten. Deze verbetering zorgt voor een sneller laden en verbeterde prestaties, waardoor het eenvoudiger wordt om complexe kaarten zonder onderbrekingen te beheren.

Na de upgrade van de build kan het systeem worden geconfronteerd met een tijdelijke toename van de belasting, waardoor de verwerking van nieuw geüploade gegevens vertraging oploopt. Dit wordt veroorzaakt door een geautomatiseerd eenmalig script (OTS) dat op de achtergrond wordt uitgevoerd. Zodra het manuscript voltooit, zullen de systeemprestaties aan normaal terugkeren.

### Verbeterde verwerking van bedrijfsmiddelen

Er is een geautomatiseerd proces geïntroduceerd om elementen in de `/content/dam` up-to-date te houden. Het systeem activeert de herverwerking van bedrijfsmiddelen om de 15 minuten. Tijdens elke cyclus worden elementen die nieuw zijn toegevoegd of niet zijn verwerkt binnen het meest recente interval van 15 minuten opgehaald en opnieuw verwerkt, waardoor de efficiëntie en consistentie in de gehele inhoudsplaats worden verbeterd.

Voor meer details, mening [ activa van het Proces ](../user-guide/asset-processor.md).




