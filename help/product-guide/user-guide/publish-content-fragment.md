---
title: Een onderwerp naar een inhoudsfragment publiceren
description: Publiceer een onderwerp of de elementen binnen een onderwerp aan een Fragment van de Inhoud in AEM Guides.  Leer hoe te om de aanwezige Fragments van de Inhoud voor een onderwerp te bekijken en hen opnieuw te publiceren.
exl-id: b1769e48-d721-4e93-b10f-04b385272be7
feature: Publishing
role: User
source-git-commit: 26aacde56e84c9f3a5ee5106b9271b4b12f8969a
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 0%

---

# Inhoudsfragmenten publiceren

Inhoudsfragmenten zijn afzonderlijke stukken inhoud in Adobe Experience Manager. Het zijn gestructureerde inhoud die is gebaseerd op een inhoudsmodel. Inhoudsfragmenten zijn pure inhoud zonder ontwerp- of layoutgegevens. Ze kunnen onafhankelijk van de kanalen die Adobe Experience Manager ondersteunt, worden ontworpen en beheerd. Inhoudsfragmenten zijn modulair, waarbij de inhoud wordt opgedeeld in kleinere componenten.

Met Experience Manager Guides kunt u een onderwerp of de elementen ervan publiceren naar een inhoudsfragment.

>[!NOTE]
>
>U kunt alleen die elementen in een onderwerp kiezen waarvoor een id-kenmerk is gedefinieerd.


Voer de volgende stappen uit om een inhoudsfragment te maken:

1. Creeer het model van het Fragment van de a [ Inhoud ](https://experienceleague.adobe.com/docs/experience-manager-65/assets/content-fragments/content-fragments-models.html?lang=en) in Adobe Experience Manager Assets.
1. Maak een map waarin u de inhoudsfragmenten wilt opslaan die u maakt op basis van het model Inhoudsfragment. Bijvoorbeeld &#39;stock-content-fragments&#39;.
1. Bewerk de eigenschappen van de map (bijvoorbeeld &quot;stock-content-fragments&quot;) en voeg het pad van de map toe, die het model Content Fragment bevat in de cloudconfiguratie.
Voeg bijvoorbeeld `/conf/we-retail` toe in de cloudconfiguratie. Deze configuratie verbindt alle modellen van het Fragment van de Inhoud met de omslag.\
   ![ voeg de details van de wolkenconfiguratie in de omslageigenschappen ](images/fragment-folder-cloud-configuration.png){width="650" align="left"} toe
   *voeg de wolkenconfiguratie in de omslageigenschappen toe om het met de fragmentmodellen te verbinden.*

1. Om een Fragment van de Inhoud te produceren, selecteer **Nieuwe Output ![ nieuw outputpictogram ](./images/Add_icon.svg) van de** Uitvoer **sectie in de** Eigenschappen van het Dossier **van een onderwerp.**
1. Selecteer **het Fragment van de Inhoud**.\
   ![ dossier eigenschappen opties tabel ](./images/file-properties-outputs-tab-new.png) {width="300" align="left"}

   *voeg een nieuw Fragment van de Inhoud van de Eigenschappen van het Dossier van een onderwerp* toe.

1. In **produceer de dialoogdoos van het Fragment van de Inhoud**, vul de volgende details onder de **Algemene** en **Afbeelding** lusjes in.

   **Algemene** tabel
   ![ voeg het fragmentmodel en de kaartdetails in toe publiceren als de dialoog van het Fragment van de Inhoud ](images/generate-content-fragment.png)
   *voeg de weg, de naam, de titel, en voorwaarde het filtreren toe om een onderwerp of zijn elementen als Fragment van de Inhoud te publiceren.*


   * **Weg**: Doorblader en selecteer de weg van de omslag waar u het Fragment van de Inhoud wilt publiceren. Als u een bestaand inhoudsfragment selecteert, wordt de inhoud van de toegewezen velden overschreven.
   * **Titel**: Type de titel van het Fragment van de Inhoud. Door gebrek, wordt de titel bevolkt met de titel van het onderwerp. U kunt het bestand bewerken. Deze titel wordt gebruikt om de naam van het inhoudsfragment te genereren.
   * **Naam**: Type de naam van het Fragment van de Inhoud. Door gebrek, wordt de naam bevolkt met de titel van het onderwerp, en de ruimten worden vervangen met &quot;_&quot;. Bijvoorbeeld, *sample_content_fragment*. U kunt het bestand bewerken.  Deze naam wordt gebruikt om de URL voor het inhoudsfragment te genereren.

   * U kunt verschillende voorwaarden selecteren om varianten van inhoudsfragmenten te maken. Selecteer een van de volgende opties:

     >[!NOTE]
     > 
     > De voorwaarden worden toegelaten slechts als voorwaardelementen in het onderwerp worden bepaald.

      * **niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.
      * **Gebruikend DITAVAL**: Selecteer het DITAVAL dossier om specifieke inhoud in de geproduceerde output te omvatten of uit te sluiten. U kunt het DITAVAL-bestand selecteren in het dialoogvenster Bladeren of door het bestandspad te typen.
      * **Gebruikend attributen**: U kunt voorwaardenattributen in uw onderwerpen bepalen DITA. Selecteer vervolgens het kenmerk condition om de relevante inhoud te publiceren.






   **Toewijzing** lusje

   ![ voeg het fragmentmodel en de kaartdetails in toe publiceren als de dialoog van het Fragment van de Inhoud ](images/content-fragment-mapping.png)

   *selecteer het model van het inhoudsfragment, en voeg de kaartdetails toe om een onderwerp of zijn elementen als Fragment van de Inhoud te publiceren.*

   * **Model**: Selecteer het model van het Fragment van de Inhoud dat u wilt gebruiken om uw Fragment van de Inhoud tot stand te brengen. De modellen worden gekozen uit de map die u hebt geconfigureerd op de Experience Manager Guides-server.
   * **Afbeelding**: U kunt de onderwerpelementen bekijken die een identiteitskaart hebben die op hen wordt toegepast. Sleep de onderwerpelementen naar de velden in het fragmentmodel van de inhoud.
De rechterzijde wordt gevuld met de inhoud van het gepubliceerde inhoudsfragment in het geval van een bestaand inhoudsfragment. Deze kunnen met de onderwerpinhoud indien nodig worden beschreven. U kunt **ook selecteren ongedaan maakt** om de toewijzingsveranderingen terug te keren.


     >[!NOTE]
     >
     > Als u 4.4 of vroegere versies gebruikt, selecteer een afbeelding van drop-down. Het plukt de afbeeldingen van het {*dossier 0} contentFragmentMapping.json.*  Uw beheerder kan de afbeeldingen in het {*dossier toevoegen 0} contentFragmentMapping.json.* Leer meer over hoe te om [ een afbeelding tussen een onderwerp en een Fragment van de Inhoud ](../cs-install-guide/conf-content-fragment-mapping-cs.md) in de Gids van de Installatie en van de Configuratie tot stand te brengen.

1. Selecteer **produceren** om het Fragment van de Inhoud te publiceren.

1. U kunt de Fragmenten van de Inhoud voor een onderwerp onder de **sectie van Output** in de **Eigenschappen van het Dossier** bekijken.

   ![ Mening de Fragmenten van de Inhoud voor een onderwerp ](images/outputs-options-menu-new.png){width="300" align="left"}

   *Mening de fragmenten van de Inhoud aanwezig voor een onderwerp en herpubliceer hen.*


Nadat u de inhoudsfragmenten hebt gepubliceerd, kunt u deze ook gebruiken in elke Adobe Experience Manager-site.




## Menu Opties voor een inhoudsfragment

U kunt de volgende acties voor een Fragment van de Inhoud van het **menu van Opties** ook uitvoeren:

* **produceer**: Herpubliceer het Fragment van de Inhoud om het met de recentste inhoud van het onderwerp bij te werken DITA. Wanneer u de uitvoer opnieuw genereert, kunt u het pad, de naam, de titel, het model en de toewijzing van het inhoudsfragment wijzigen. U kunt ook verschillende voorwaarden selecteren wanneer u de uitvoer opnieuw genereert.

* **Dupliceer**: Dupliceer een Fragment van de Inhoud. U kunt het pad, de naam, de titel, het model en de toewijzing wijzigen. U kunt ook verschillende voorwaarden selecteren wanneer u een inhoudsfragment dupliceert om een Content Fragment-variant te maken.

* **verwijder**: Verwijder een Fragment van de Inhoud uit de outputlijst. Er verschijnt een bevestigingsbericht. Zodra u bevestigt, wordt het Fragment van de Inhoud verwijderd uit de **lijst van Output**.

  >[!NOTE]
  >
  > Met deze actie wordt geen inhoud verwijderd uit het inhoudsfragment.

* **Mening**: Bekijk de redacteur van het Fragment van de Inhoud. U kunt ook wijzigingen aanbrengen en opslaan.