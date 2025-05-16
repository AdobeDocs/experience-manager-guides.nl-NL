---
title: Opmerkingen bij de release | Nieuwe functies in de Adobe Experience Manager Guides 2025.04.0-release
description: Meer informatie over de nieuwe en verbeterde functies in de 2025.04.0-release van Adobe Experience Manager Guides
role: Leader
exl-id: 5d28119b-641f-402b-833c-6f7554e7c273
source-git-commit: fe7d81f1826fe4ee0c716df36daabe3c5efd8994
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# Nieuwe functies in de release van 2025.04.0 (april 2025)

Dit artikel behandelt de nieuwe en verbeterde functies die zijn geïntroduceerd met de release 2025.04.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor de lijst van kwesties die in deze versie worden bevestigd, mening [ Vaste kwesties in de versie 2025.04.0 ](fixed-issues-2025-04-0.md).

Leer over [ verbeteringsinstructies voor de versie 2025.04.0 ](../release-info/upgrade-instructions-2025-04-0.md).

## &#39;Format&#39;-kenmerk toegevoegd voor verwijzingskoppelingen

Adobe Experience Manager Guides voegt nu a **formaat** attributen voor verwijzingsverbindingen binnen de Redacteur toe. Dit attribuut wordt getoond in de **mening van Source** en wijst duidelijk op het dossiertype, zoals:

- Voor dossiers met a **.pdf** uitbreiding, zal het formaat aan **pdf** worden geplaatst
- Voor dossiers met a **.html** uitbreiding, zal het formaat aan **html** worden geplaatst
- Voor dossiers met a **.dita** of **** dossiers.ditamap, zal het formaat aan **dita** worden geplaatst

Bovendien, zullen de dossiers met a **.xml** uitbreiding ook hun formaat hebben dat aan **wordt geplaatst dita**. Voor bestanden zonder extensie blijft de indeling leeg. Voorts voor om het even welke verwijzingsverbindingen met een werkingsgebied dat aan **wordt geplaatst extern**, zal het formaat aan **html** ongeacht de dossieruitbreiding in de verwijzingsverbindingen worden geplaatst.

## Geëxporteerde basislijn bevat nu de documentstatus

De eigenschap van de Basislijn van de Uitvoer omvat nu de **documentstaat** naast zeer belangrijke details zoals titel, dossiernaam, dossiertype, en versieaantal in de basislijnmomentopname. Deze verbetering verbetert het basislijnbeheer door een uitgebreider overzicht van de basislijn te verstrekken.

Voor meer details, leidt de mening [ basislijnen van de console van de Kaart ](../user-guide/web-editor-baseline.md#manage-baselines) tot en beheert.

## Verbeterde zoekervaring voor het deelvenster Herbruikbare inhoud

Experience Manager Guides introduceert een verbeterde zoekervaring in het deelvenster Herbruikbare inhoud. Bij deze update worden bij het zoeken naar trefwoorden nu alle bestanden gescand die zijn toegevoegd als herbruikbare inhoud, en niet alleen de geopende bestanden. Op deze manier kunt u de exacte positie van het trefwoord in alle gevallen vinden, ongeacht of de containers zijn geopend of samengevouwen. Wanneer u de zoekbalk wist, blijft bovendien de oorspronkelijke staat van alle containers behouden, wat een efficiëntere en gebruikersvriendelijkere zoekfunctionaliteit biedt.

Voor meer details, mening [ Herbruikbare inhoud ](../user-guide/web-editor-features.md#reusable-content).


## Java-versieverbetering voor microservicecontainers

Voor cloud-omgevingen met microservice gaan we over naar Java 21, zodat de bestaande DITA-OT- en native PDF-generatieprocessen ongewijzigd blijven. De bestaande workflow van DITA-OT 3 blijft naadloos functioneren met Java 21.  Bovendien is DITA-OT 4 volledig operationeel, zodat gebruikers PDF&#39;s kunnen genereren met DITA-OT en native PDF, en uitvoer kunnen produceren voor native AEM-sites en andere indelingen.
