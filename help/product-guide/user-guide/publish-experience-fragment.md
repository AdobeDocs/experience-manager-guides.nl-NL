---
title: Een onderwerp naar een ervaringsfragment Publish
description: Publish een onderwerp of de elementen binnen een onderwerp aan een Fragment van de Ervaring in AEM Guides.  Leer hoe te om de Fragments van de Ervaring voor een onderwerp te bekijken en hen opnieuw te publiceren.
feature: Publishing
role: User
exl-id: 4cdce8c2-2ccf-4bf1-8b92-4dfeb10de186
source-git-commit: d525775afeeb89754762ff514126b1c3a3307b3f
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 0%

---

# Publish Experience Fragmenten

De Fragmenten van de ervaring zijn stukken van modulaire inhoud in Adobe Experience Manager. Deze inhoudsblokken zijn gebaseerd op sjablonen en kapselen zowel de inhoud als de lay-out in. Met deze herbruikbare stukken inhoud kunnen makers van inhoud consistente, schaalbare ervaringen samenstellen en leveren op meerdere kanalen die door de Experience Manager worden ondersteund. Met deze functie kunt u eenvoudig consistente marketingervaringen maken, zoals nieuwsbrieven, promotiebanners en klantengetuigenissen.

Met Experience Manager Guides kunt u een onderwerp of de bijbehorende elementen publiceren naar een ervaringsfragment. U kunt een op JSON-Gebaseerde afbeelding tussen een onderwerp en zijn elementen in een Fragment van de Ervaring tot stand brengen. Dan, gebruik de afbeelding om een onderwerp of zijn elementen aan een Fragment van de Ervaring te publiceren. U kunt de Fragmenten van de Ervaring in om het even welke Plaats van de Experience Manager dan gebruiken of de details via APIs halen die door de Fragments van de Ervaring worden gesteund.




Voer de volgende stappen uit om een ervaringsfragment te genereren:


1. Maak een map in de Experience Fragments. Gebruik deze map om de Experience Fragments op te slaan die u maakt op basis van de Experience Fragment-sjablonen. Bijvoorbeeld, *verkoop-ervaring-fragmenten*.
1. Selecteer de omslag en selecteer dan het **pictogram van Eigenschappen** van de bovenkant.
1. Bewerk de eigenschappen van de omslag (bijvoorbeeld, *verkoop-ervaring-fragmenten*).


   * **Titel**: Bekijk of geef de titel van de omslag uit.

   * **Toegestane Malplaatjes**: Bevat de lijst van malplaatjes die als kindpagina&#39;s van de ervaring kunnen worden toegevoegd. Om het toegestane malplaatje toe te voegen, specificeer de regelmatige uitdrukking voor het terugwinnen van de vereiste malplaatjes op het **Toegelaten gebied van Malplaatjes**.
Bijvoorbeeld:
     `/libs/cq/experience-fragments/components/experiencefragment/template`

     Als u geen toegestane sjabloon voor een map definieert, worden de sjablonen standaard gekozen uit de bovenliggende map of de sjabloonmap.
   * **Bestelbaar**: Staat u toe om de orde van de activa binnen een omslag te veranderen.
     ![ voeg de details van de wolkenconfiguratie in de omslageigenschappen ](images/experience-fragment-folder-properties.png){width="650" align="left"} toe
     *voeg de wolkenconfiguratie in de omslageigenschappen toe om het met de fragmentmalplaatjes te verbinden.*
1. Om een Fragment van de Ervaring te produceren, selecteer **Nieuwe Output ![ nieuw outputpictogram ](./images/Add_icon.svg) van de** Output **sectie in de** Eigenschappen van het Dossier **van een onderwerp.**
1. Selecteer **Fragment van de Ervaring**.\
   ![ dossier eigenschappen opties tabel ](./images/file-properties-outputs.png){width="300" align="left"}

   *voeg een nieuw Fragment van de Ervaring van de Eigenschappen van het Dossier van een onderwerp* toe.

   >[!NOTE]
   >
   > U kunt een Fragment van de Ervaring van de **Mening van de Bewaarplaats** ook publiceren. Selecteer het onderwerp dat u als Fragment van de Ervaring wilt publiceren. Dan, van het **menu van Opties**, uitgezochte **Publish als** > **Fragment van de Ervaring**.

1. In **produceer de dialoogdoos van het Fragment van de Ervaring**, vul de volgende details in:
   ![ voeg het fragmentmodel en de kaartdetails in Publish toe als de dialoog van het Fragment van de Ervaring ](images/experience-fragment-generate.png){width="500" align="left"}

   *voeg de weg, het malplaatje, en kaartdetails toe om een onderwerp of zijn elementen als Fragment van de Ervaring te publiceren. U kunt een bestaand Fragment van de Ervaring beschrijven.*

   * **Weg**: Blader en selecteer de weg van de omslag waar u het Fragment van de Ervaring wilt publiceren. U kunt ook een bestaand ervaringsfragment selecteren en opnieuw publiceren.
   * **Titel**: Type de titel van het Fragment van de Ervaring. Door gebrek, wordt de titel bevolkt met de titel van het onderwerp. U kunt het bestand bewerken. Deze titel wordt gebruikt om de naam van het fragment van de Ervaring te produceren.
   * **Naam**: Type de naam van het Fragment van de Ervaring. Door gebrek, wordt de naam bevolkt met de titel van het onderwerp, en de ruimten worden vervangen met &quot;_&quot;. Bijvoorbeeld, *sample_experience_fragment*. U kunt het bestand bewerken. Deze naam wordt gebruikt om URL voor het Fragment van de Ervaring te produceren.
   * **Malplaatje**: Selecteer het malplaatje van het Fragment van de Ervaring dat u wilt gebruiken om uw Fragment van de Ervaring tot stand te brengen. De sjablonen worden gekozen uit de map die u in de eigenschappen hebt geconfigureerd.
   * **Afbeelding**: Het plukt de afbeelding van het {*dossier 2} experienceFragmentMapping.json en toont het.*



     Uw beheerder kan de afbeeldingen in het {*dossier toevoegen 0} experienceFragmentMapping.json.*  Leer meer over hoe te om [ een afbeelding tussen een onderwerp en een Fragment van de Ervaring ](../cs-install-guide/conf-experience-fragment-mapping-cs.md) in de Gids van de Installatie en van de Configuratie tot stand te brengen.

   * U kunt ook verschillende voorwaarden selecteren om de inhoud te publiceren.  Selecteer een van de volgende opties:


      * **niets**: selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.
      * **Gebruikend DITAVAL**: Selecteer het DITAVAL dossier om gepersonaliseerde inhoud te produceren. U kunt het DITAVAL-bestand selecteren in het dialoogvenster Bladeren of door het bestandspad te typen.
      * **Gebruikend attributen**: U kunt voorwaardenattributen in uw onderwerpen bepalen DITA. Selecteer vervolgens het kenmerk condition om de relevante inhoud te publiceren.

     >[!NOTE]
     > 
     >De voorwaarden worden toegelaten slechts als voorwaardelementen in het onderwerp worden bepaald.


   * Selecteer **overschrijven bestaande inhoud** checkbox als uw Fragment van de Ervaring reeds bestaat en u wenst om het te beschrijven. Experience Manager Guides geeft een fout weer als u het selectievakje niet inschakelt en uw ervaringsfragment al bestaat.
1. Klik **produceren** om het Fragment van de Ervaring te publiceren.
1. U kunt de Fragmenten van de Ervaring voor een onderwerp onder de **sectie van Output** in de **Eigenschappen van het Dossier** bekijken. De fragmenten van de Ervaring verschijnen volgens de datum en de tijd van hun publicatie, met als laatste als eerste.

   ![ Mening de Fragmenten van de Ervaring voor een onderwerp ](images/experience-fragment-outputs.png) {width=300 align=&quot;links&quot;}

   *Mening de Fragments van de Ervaring aanwezig voor een onderwerp en herpubliceer hen.*




Nadat u de Experience Fragments hebt gepubliceerd, kunt u deze ook op elke Adobe Experience Manager-site gebruiken.


## Menu Opties voor een Ervingsplugment

U kunt de volgende acties voor een Fragment van de Ervaring van het **menu van Opties** ook uitvoeren:

* **produceer**: Herpubliceer het Fragment van de Ervaring om het met de recentste inhoud van het onderwerp bij te werken DITA. Wanneer u de uitvoer opnieuw genereert, kunt u het pad, de naam, de titel en de sjabloon van het ervaringsfragment niet wijzigen. U kunt echter verschillende voorwaarden selecteren wanneer u de uitvoer opnieuw genereert.

* **dupliceer**: Dupliceer een Fragment van de Ervaring. U kunt het pad, de naam, de titel en de sjabloon wijzigen. U kunt ook verschillende voorwaarden selecteren wanneer u een ervaringsfragment dupliceert.

* **verwijder**: Verwijder een Fragment van de Ervaring uit de outputlijst. Er verschijnt een bevestigingsbericht. Zodra u bevestigt, wordt het Fragment van de Ervaring verwijderd uit de **lijst van Output**. Het ervaringsfragment wordt echter niet verwijderd uit de map.

* **Mening**: Bekijk de redacteur van het Fragment van de Ervaring. U kunt ook wijzigingen aanbrengen en opslaan.
