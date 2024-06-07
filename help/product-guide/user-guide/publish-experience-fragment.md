---
title: Een onderwerp publiceren naar een ervaringsfragment
description: Publiceer een onderwerp of de elementen binnen een onderwerp aan een Fragment van de Ervaring in AEM Gidsen.  Leer hoe te om de Fragments van de Ervaring voor een onderwerp te bekijken en hen opnieuw te publiceren.
feature: Publishing
role: User
source-git-commit: 7c7e3dcddf733793a5d6db50205ba60d24702451
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 0%

---


# Fragmenten voor ervaring publiceren

De Fragmenten van de ervaring zijn stukken van modulaire inhoud in Adobe Experience Manager. Deze inhoudsblokken zijn gebaseerd op sjablonen en kapselen zowel de inhoud als de lay-out in. Met deze herbruikbare stukken inhoud kunnen makers van inhoud consistente, schaalbare ervaringen samenstellen en leveren op meerdere kanalen die door de Experience Manager worden ondersteund. Met deze functie kunt u eenvoudig consistente marketingervaringen maken, zoals nieuwsbrieven, promotiebanners en klantengetuigenissen.

Met de hulplijnen voor Experience Managers kunt u een onderwerp of de bijbehorende elementen publiceren naar een ervaringsfragment. U kunt een op JSON-Gebaseerde afbeelding tussen een onderwerp en zijn elementen in een Fragment van de Ervaring tot stand brengen. Dan, gebruik de afbeelding om een onderwerp of zijn elementen aan een Fragment van de Ervaring te publiceren. U kunt de Fragmenten van de Ervaring in om het even welke Plaats van de Experience Manager dan gebruiken of de details via APIs halen die door de Fragments van de Ervaring worden gesteund.




Voer de volgende stappen uit om een ervaringsfragment te genereren:


1. Maak een map in de Experience Fragments. Gebruik deze map om de Experience Fragments op te slaan die u maakt op basis van de Experience Fragment-sjablonen. Bijvoorbeeld: *verkoopervaringsfragmenten*.
1. Selecteer de map en selecteer vervolgens de **Eigenschappen** bovenaan.
1. Bewerk de eigenschappen van de map (bijvoorbeeld *verkoopervaringsfragmenten*).


   * **Titel**: De titel van de map weergeven of bewerken.

   * **Toegestane sjablonen**: Bevat de lijst met sjablonen die kunnen worden toegevoegd als onderliggende pagina&#39;s van de ervaring. Om het toegestane malplaatje toe te voegen, specificeer de regelmatige uitdrukking voor het terugwinnen van de vereiste malplaatjes in **Toegestane sjablonen** veld.
Bijvoorbeeld:
     `/libs/cq/experience-fragments/components/experiencefragment/template`

     Als u geen toegestane sjabloon voor een map definieert, worden de sjablonen standaard gekozen uit de bovenliggende map of de sjabloonmap.
   * **Bestelbaar**: Hiermee kunt u de volgorde van de elementen in een map wijzigen.
     ![gegevens over de cloudconfiguratie toevoegen aan de mapeigenschappen](images/experience-fragment-folder-properties.png){width="650" align="left"}
     *Voeg de wolkenconfiguratie in de omslageigenschappen toe om het met de fragmentmalplaatjes te verbinden.*
1. Selecteer **Nieuwe uitvoer** ![nieuw uitvoerpictogram](./images/Add_icon.svg) van de **Uitvoer** in de **Bestandseigenschappen** van een onderwerp.
1. Selecteren **Ervaar fragment**.\
   ![opties op het tabblad Bestandseigenschappen](./images/file-properties-outputs.png){width="300" align="left"}

   *Voeg een nieuw Fragment van de Ervaring van de Eigenschappen van het Dossier van een onderwerp toe*.

   >[!NOTE]
   >
   > U kunt ook een Experience Fragment publiceren vanuit het dialoogvenster **Weergave opslagplaats**. Selecteer het onderwerp dat u als Fragment van de Ervaring wilt publiceren. Dan, van **Opties** menu, selecteert u **Publiceren als** > **Ervaar fragment**.

1. In de **Experience Fragment genereren** , vult u de volgende gegevens in:
   ![Het fragmentmodel en toewijzingsdetails toevoegen in het dialoogvenster Publiceren als ervaringsfragment](images/experience-fragment-generate.png){width="500" align="left"}

   *Voeg de weg, het malplaatje, en de kaartdetails toe om een onderwerp of zijn elementen als Fragment van de Ervaring te publiceren. U kunt een bestaand ervaringsfragment overschrijven.*

   * **Pad**: Blader en selecteer het pad van de map waarin u het ervaringsfragment wilt publiceren. U kunt ook een bestaand ervaringsfragment selecteren en opnieuw publiceren.
   * **Titel**: Typ de titel van het ervaringsfragment. Door gebrek, wordt de titel bevolkt met de titel van het onderwerp. U kunt het bestand bewerken. Deze titel wordt gebruikt om de naam van het fragment van de Ervaring te produceren.
   * **Naam**: Typ de naam van het ervaringsfragment. Door gebrek, wordt de naam bevolkt met de titel van het onderwerp, en de ruimten worden vervangen met &quot;_&quot;. Bijvoorbeeld: *sample_experience_fragment*. U kunt het bestand bewerken. Deze naam wordt gebruikt om URL voor het Fragment van de Ervaring te produceren.
   * **Sjabloon**: Selecteer de sjabloon Experience Fragment die u wilt gebruiken om uw Experience Fragment te maken. De sjablonen worden gekozen uit de map die u in de eigenschappen hebt geconfigureerd.
   * **Toewijzing**: De afbeelding wordt gekozen uit de *experienceFragmentMapping.json* en geeft deze weer.



     Uw beheerder kan de toewijzingen toevoegen in de *experienceFragmentMapping.json* bestand.  Meer informatie over hoe [een afbeelding maken tussen een onderwerp en een ervaringsfragment](../cs-install-guide/conf-experience-fragment-mapping-cs.md) in de Installatie- en configuratiehandleiding.

   * U kunt ook verschillende voorwaarden selecteren om de inhoud te publiceren.  Selecteer een van de volgende opties:


      * **Geen**: Selecteer deze optie als u geen voorwaarde wilt toepassen op de gepubliceerde uitvoer.
      * **DITAVAL gebruiken**: Selecteer het DITAVAL-bestand om gepersonaliseerde inhoud te genereren. U kunt het DITAVAL-bestand selecteren in het dialoogvenster Bladeren of door het bestandspad te typen.
      * **Kenmerken gebruiken**: U kunt voorwaardenattributen in uw onderwerpen bepalen DITA. Selecteer vervolgens het kenmerk condition om de relevante inhoud te publiceren.

     >[!NOTE]
     > 
     >De voorwaarden worden toegelaten slechts als voorwaardelementen in het onderwerp worden bepaald.


   * Selecteer de **Bestaande inhoud overschrijven** Schakel het selectievakje in als uw ervaringsfragment al bestaat en u dit wilt overschrijven. In de hulplijnen voor Experience Managers wordt een fout weergegeven als u het selectievakje niet inschakelt en het fragment voor uw ervaring al bestaat.
1. Klikken **Genereren** om het Experience Fragment te publiceren.
1. U kunt de Fragmenten van de Ervaring voor een onderwerp onder bekijken **Uitvoer** in de **Bestandseigenschappen**. De fragmenten van de Ervaring verschijnen volgens de datum en de tijd van hun publicatie, met als laatste als eerste.

   ![Bekijk de Fragmenten van de Ervaring voor een onderwerp](images/experience-fragment-outputs.png){width=300 align=&quot;left&quot;}

   *Bekijk de aanwezige Fragments van de Ervaring voor een onderwerp en publiceer hen opnieuw.*




Nadat u de Experience Fragments hebt gepubliceerd, kunt u deze ook op elke Adobe Experience Manager-site gebruiken.


## Menu Opties voor een Ervingsplugment

U kunt ook de volgende handelingen uitvoeren voor een ervaringsfragment in het dialoogvenster **Opties** menu:

* **Genereren**: Publiceer het fragment van de Ervaring om het met de recentste inhoud van het DITA onderwerp bij te werken. Wanneer u de uitvoer opnieuw genereert, kunt u het pad, de naam, de titel en de sjabloon van het ervaringsfragment niet wijzigen. U kunt echter verschillende voorwaarden selecteren wanneer u de uitvoer opnieuw genereert.

* **Dupliceren**: Dupliceer een ervaringsfragment. U kunt het pad, de naam, de titel en de sjabloon wijzigen. U kunt ook verschillende voorwaarden selecteren wanneer u een ervaringsfragment dupliceert.

* **Verwijderen**: Verwijder een fragment van de Ervaring uit de outputlijst. Er verschijnt een bevestigingsbericht. Zodra u bevestigt, wordt het Fragment van de Ervaring verwijderd uit **Uitvoer** lijst. Het ervaringsfragment wordt echter niet verwijderd uit de map.

* **Weergave**: Bekijk de Experience Fragment-editor. U kunt ook wijzigingen aanbrengen en opslaan.


