---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2025.11.0
description: Meer informatie over de opgeloste problemen vindt u in de release 2025.11.0 van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: d9a46a009477b1110208a509d4ad8c0616139661
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Opgeloste problemen in de release 2025.11.0

Dit artikel heeft betrekking op de fouten die zijn verholpen in verschillende gebieden van de release 2025.11.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de versie 2025.11.0 ](whats-new-2025-11-0.md) nieuw is.

Leer over [ verbeteringsinstructies voor de versie 2025.11.0 ](upgrade-instructions-2025-11-0.md).

## Authoring

- Als een leeg `prop` -element zonder kenmerken of waarden wordt toegevoegd aan een DITAVAL-bestand, kunnen geen aanvullende `prop` -elementen worden toegevoegd. (GUIDEN-33597)
- Na bevordering Experience Manager Guides aan versie 2025.08.0, verschijnt de optie om de douane **Acrolinx** tabel toe te laten of onbruikbaar te maken niet meer in **montages van Workspace**. (GUIDEN-35261)
- Aangepaste CSS die wordt toegepast in een mapprofiel voor onderwerpen of mappen, wordt teruggezet naar de standaardstijl in de modus Voorbeeld wanneer de browser wordt vernieuwd. (GUIDEN-31098)
- **ongedaan maken** en **opnieuw** verrichtingen werken niet zoals verwacht in de mening van Source van de Redacteur voor DITA- dossiers. (HIDEN-24914, HULPLIJNEN-25034)
- Wanneer u verwijst naar een DITA-kaart in een onderwerp met behulp van het element `Xref` , wordt de bestandsnaam van de kaart waarnaar wordt verwezen, weergegeven in plaats van de titel van de kaart. (GUIDEN-21759)
- Wanneer het toevoegen van veelvoudige dossiers van het Schema voor bevestiging door het juiste paneel van de interface van de Redacteur, bestaat een fout **dossier(s) van het Schema niet of heeft fouten** wordt getoond zelfs als de toegevoegde dossiers geldig zijn en geen fouten hebben. (GUIDEN-33731)
- Grote of complexe MathML-vergelijkingen worden niet weergegeven in de Editor. (GUIDEN-29095)

## Beheer van bedrijfsmiddelen

- Wanneer u een bewerkte afbeelding opnieuw uploadt via de gebruikersinterface van Experience Manager Guides, wordt de oorspronkelijke uitvoering van de afbeelding bijgewerkt, maar wordt de vorige versie van de afbeelding wel weergegeven door de bijbehorende DITA-inhoud. (GUIDEN-33693)
- Wanneer u twee of meer mappen probeert te verplaatsen van de bronlocatie naar een andere locatie (met het gereedschap Bulk verplaatsen), mislukt de bewerking als de mapnamen beginnen met dezelfde tekenreeks (bijvoorbeeld Product en ProductImages). (GUIDEN-29096)
- Het schrappen van een gezocht bezit van Assets UI van het Onderzoek omzeilt de **Forceer schrapt** waarschuwingsdialoog en schrapt direct het activa, zelfs wanneer het in bestaande inhoud DITA van verwijzingen wordt voorzien. (GUIDEN-17232)

## Publiceren

- Wanneer u een DITA-kaart publiceert met een basislijn op AEM Sites (met toewijzing van verouderde componenten), worden ook de structuurelementen met het kenmerk `processing-role = resource-only` gepubliceerd. (GUIDEN-37649)
- In sommige gevallen ontbreekt de eigenschap `jcr:content/fmUuidOfSource` op de AEM Sites-uitvoerpagina&#39;s (met toewijzing van verouderde componenten), wat leidt tot nieuwe inhoudspagina&#39;s die niet kunnen worden gedetecteerd.
- Filteren van inhoud via DITAVal-filters en voorwaardelijke voorinstellingen werkt niet voor Salesforce-publicaties. (HIDEN-33515)
- Kan geen eigen PDF-voorinstelling maken voor een kaart als er een map met dezelfde naam bestaat in de inhoudshiërarchie. (GUIDEN-33012)
- Wanneer de Inheemse output van PDF gebruikend een dynamische basislijn wordt geproduceerd, wordt de termijn **PDFProject** getoond als titel van PDF in plaats van de daadwerkelijke kaarttitel. (GIDS-31102)
- Het genereren van eigen PDF-uitvoer met bepaalde `print` -kenmerkwaarden in onderwerpverwijzingen werkt niet zoals verwacht. (GIDS-31101)
- Wanneer een omslag die kaarten DITA bevat wordt bewogen gebruikend Assets UI of **Bulk beweging** optie, de bestaande kaartinzamelingen en bulkactiveringsinzamelingen die die kaarten van verwijzingen voorzien niet laden. (HIDEN-28355)
- Wanneer u een map met een map met voorinstellingen voor voorwaarden verplaatst, worden de voorwaarden niet toegepast in de gegenereerde uitvoer na de verplaatsing. (HIDEN-28352)
- Wanneer u AEM Sites-uitvoer genereert met behulp van oude componenttoewijzing, worden onderwerpen die het kenmerk `copy-to` gebruiken, gepubliceerd met de naam van het `copy-from` -onderwerp in plaats van de naam die is ingesteld in het kenmerk `copy-to` . (HULPLIJNEN-22155)
- Het activeren van één of meerdere kaarten DITA van **Bulk publiceert dashboard** produceert bovenmatig grote logboeken. (GUIDEN-20746)

## Platform

- Foutlogboeken die worden gegenereerd wanneer een element wordt geüpload via de gebruikersinterface van Assets of wanneer een nieuw bestand wordt gemaakt via de Editor-interface, worden de term `predecessor` onjuist gebruikt in plaats van `successor` in het logbericht. (GUIDEN-35607)

## Bekende problemen

Adobe heeft de volgende bekende problemen vastgesteld voor de release 2025.11.0:

- Wanneer u een dubbel onderwerp maakt met het kenmerk `copy-to` en ernaar verwijst met het kenmerk `scope=peer` , veroorzaakt dit problemen met de omleiding in AEM Sites-uitvoer, waarbij koppelingen van AEM Sites (met samengestelde componenttoewijzing) worden omgeleid naar AEM Sites (met oudere componenttoewijzing) en andersom. (GUIDEN-37656)











