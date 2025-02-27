---
title: Een onderwerp naar een AEM Sites-pagina publiceren
description: Publiceer een onderwerp of de elementen binnen een onderwerp aan een output van Adobe Experience Manager Sites.  Leer hoe u de Experience Manager Sites-pagina voor een onderwerp kunt weergeven en deze opnieuw kunt publiceren.
feature: Publishing
role: User
hide: true
source-git-commit: ea597cd14469f21e197c700542b9be7c373aef14
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 0%

---

# Adobe Experience Manager Sites-pagina&#39;s publiceren


Experience Manager Sites-pagina verwijst naar inhoud die op de Adobe Experience Manager-website is gepubliceerd. Met Experience Manager Guides kunt u een zelfstandig onderwerp naar een sitepagina publiceren.

Met deze functie kunt u een onderwerp en de bijbehorende elementen publiceren zonder een DITA-kaart en de uitvoervoorinstellingen te maken. U kunt het onderwerp gemakkelijk bijwerken, de pagina van Plaatsen opnieuw publiceren, en het hergebruiken over verschillende Web-pagina&#39;s. Met deze functie kunt u eenvoudig zelfstandige artikelen of marketinginhoud publiceren.





Voer de volgende stappen uit om een sitepagina te genereren:




1. Selecteer **Nieuwe Output** ![ nieuw outputpictogram ](./images/Add_icon.svg) van de **Output** sectie in de **Eigenschappen van het Dossier** van een onderwerp.
1. Selecteer **de pagina van Plaatsen**.


1. In **produceer de pagina van Plaatsen** dialoogdoos, vul de volgende details in:
   ![ voeg de weg en malplaatjedetails in Generate de pagina van Plaatsen ](images/aem-sites-page-generate.png){width="500" align="left"} toe

   *Voeg de weg, de titel, de naam, en malplaatjedetails toe om een onderwerp of zijn elementen als pagina van Plaatsen te publiceren. *

   * **Weg**: Doorblader en selecteer de weg van de omslag waar u de pagina van Plaatsen wilt publiceren.
   * **Titel**: Type de titel van de pagina van Plaatsen. Door gebrek, wordt de titel bevolkt met de titel van het onderwerp. U kunt het bestand bewerken. Deze titel wordt gebruikt om de naam van de pagina van Plaatsen te produceren.
   * **Naam**: Type de naam van de pagina van Plaatsen. Standaard wordt de naam gevuld met de titel van het onderwerp en niet-toegestane tekens zoals spaties en speciale tekens worden vervangen door &#39;_&#39;. Bijvoorbeeld, *sample_sites_page*. U kunt het bestand bewerken. Deze naam wordt gebruikt om URL voor de pagina van Plaatsen te produceren.
   * **malplaatje van de Pagina**: Selecteer het de paginamalplaatje van Plaatsen om uw pagina van Plaatsen tot stand te brengen. U kunt de sjablonen weergeven in de map op het pad dat u selecteert. Uw beheerder kan ook aangepaste sjablonen uploaden.


   * U kunt ook verschillende voorwaarden selecteren om de inhoud te publiceren.  Selecteer een van de volgende opties:


      * **niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.
      * **Gebruikend DITAVAL**: Selecteer het DITAVAL dossier om gepersonaliseerde inhoud te produceren. U kunt het DITAVAL-bestand selecteren in het dialoogvenster Bladeren of door het bestandspad te typen.
      * **Gebruikend attributen**: U kunt voorwaardenattributen in uw onderwerpen bepalen DITA. Selecteer vervolgens het kenmerk condition om de relevante inhoud te publiceren.

     >[!NOTE]
     > 
     >De voorwaarden worden toegelaten slechts als voorwaardelementen in het onderwerp worden bepaald.



1. Klik **produceren** om de pagina van Plaatsen te publiceren.
1. U kunt de pagina van Plaatsen voor een onderwerp onder de **sectie van Output** in de **Eigenschappen van het Dossier** bekijken. De sitepagina&#39;s worden weergegeven op basis van de datum en het tijdstip van publicatie, met als laatste de eerste pagina.

   ![ Mening de pagina van Plaatsen voor een onderwerp ](images/aem-sites-outputs.png) {width=300 align=&quot;links&quot;}

   *Mening de pagina van Plaatsen aanwezig voor een onderwerp en publiceer hen opnieuw.*




Nadat u de sitepagina hebt gepubliceerd, kunt u deze ook op elke Adobe Experience Manager-site gebruiken.


## Menu Opties voor een Experience Manager Sites

U kunt de volgende acties voor een Experience Manager Sites van het **menu van Opties** ook uitvoeren:

* **produceer**: Publiceer de pagina van Plaatsen om het met de recentste inhoud van het onderwerp bij te werken DITA. Wanneer u de uitvoer opnieuw genereert zonder het pad, de naam, de titel, de sjabloon en de voorwaarden te wijzigen, wordt de sitepagina eenvoudig bijgewerkt met de nieuwste inhoud.

* **Dupliceer**: Dupliceer een pagina van Plaatsen. U kunt het pad, de naam, de titel en de sjabloon wijzigen. U kunt ook verschillende voorwaarden selecteren wanneer u een sitepagina dupliceert.

* **verwijder**: Verwijder een pagina van Plaatsen uit de outputlijst. Er verschijnt een bevestigingsbericht. Zodra u bevestigt, wordt de pagina van Plaatsen verwijderd uit de **Output** lijst. De pagina Sites wordt echter niet permanent verwijderd.

* **Mening**: Bekijk de de paginaredacteur van Plaatsen. U kunt ook wijzigingen aanbrengen en opslaan.
