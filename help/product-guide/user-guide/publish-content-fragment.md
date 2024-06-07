---
title: Een onderwerp naar een inhoudsfragment publiceren
description: Publiceer een onderwerp of de elementen binnen een onderwerp aan een Fragment van de Inhoud in AEM Gidsen.  Leer hoe te om de aanwezige Fragments van de Inhoud voor een onderwerp te bekijken en hen opnieuw te publiceren.
exl-id: b1769e48-d721-4e93-b10f-04b385272be7
feature: Publishing
role: User
source-git-commit: 7c7e3dcddf733793a5d6db50205ba60d24702451
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 0%

---

# Inhoudsfragmenten publiceren

Inhoudsfragmenten zijn afzonderlijke stukken inhoud in Adobe Experience Manager. Het zijn gestructureerde inhoud die is gebaseerd op een inhoudsmodel. Inhoudsfragmenten zijn pure inhoud zonder ontwerp- of layoutgegevens. Ze kunnen onafhankelijk van de kanalen worden ontworpen en beheerd die Adobe Experience Manager ondersteunt. Inhoudsfragmenten zijn modulair, waarbij de inhoud wordt opgedeeld in kleinere componenten.

Met Adobe Experience Manager-hulplijnen kunt u een onderwerp of de elementen in een onderwerp naar een inhoudsfragment publiceren. U kunt een op JSON-Gebaseerde afbeelding tussen een onderwerp en een model van het Fragment van de Inhoud tot stand brengen. Gebruik deze afbeelding om een onderwerp of de elementen binnen een onderwerp naar een inhoudsfragment te publiceren. Vervolgens kunt u Content Fragments gebruiken op elke Adobe Experience Manager-site of de gegevens extraheren via API&#39;s die worden ondersteund door Content Fragments.


Voer de volgende stappen uit om een inhoudsfragment te maken:

1. Een [Inhoudsfragmentmodel](https://experienceleague.adobe.com/docs/experience-manager-65/assets/content-fragments/content-fragments-models.html?lang=en) in Adobe Experience Manager Assets.
1. Maak een map waarin u de inhoudsfragmenten wilt opslaan die u maakt op basis van het model Inhoudsfragment. Bijvoorbeeld &#39;stock-content-fragments&#39;.
1. Bewerk de eigenschappen van de map (bijvoorbeeld &quot;stock-content-fragments&quot;) en voeg het pad van de map toe, die het model Content Fragment bevat in de cloudconfiguratie.
Voeg bijvoorbeeld `/conf/we-retail` in de cloudconfiguratie. Deze configuratie verbindt alle modellen van het Fragment van de Inhoud met de omslag.\
   ![gegevens over de cloudconfiguratie toevoegen aan de mapeigenschappen](images/fragment-folder-cloud-configuration.png){width="650" align="left"}
   *Voeg de wolkenconfiguratie in de omslageigenschappen toe om het met de fragmentmodellen te verbinden.*

1. Selecteer **Nieuwe uitvoer** ![nieuw uitvoerpictogram](./images/Add_icon.svg) van de **Uitvoer** in de **Bestandseigenschappen** van een onderwerp.
1. Selecteren **Inhoudsfragment**.\
   ![opties op het tabblad Bestandseigenschappen](./images/file-properties-outputs-tab.png){width="300" align="left"}

   *Een nieuw inhoudsfragment toevoegen uit de bestandseigenschappen van een onderwerp*.

1. In de **Inhoudsfragment genereren** , vult u de volgende gegevens in:
   ![Het fragmentmodel en toewijzingsdetails toevoegen in het dialoogvenster Publiceren als inhoudsfragment](images/content-fragment-publish.png){width="500" align="left"}
   *Voeg het pad, het model en de toewijzingsdetails toe om een onderwerp of de elementen ervan te publiceren als een inhoudsfragment. U kunt een bestaand inhoudsfragment overschrijven.*

   >[!NOTE]
   >
   >U kunt ook een inhoudsfragment publiceren vanuit het dialoogvenster **Weergave opslagplaats**. Selecteer het onderwerp dat u wilt publiceren als een inhoudsfragment. Dan, van **Opties** menu, selecteert u **Publiceren als** > **Inhoudsfragment**.

   * **Pad**: Blader en selecteer het pad van de map waarin u het inhoudsfragment wilt publiceren. Als u een bestaand inhoudsfragment selecteert, wordt de inhoud van de toegewezen velden overschreven.
   * **Titel**: Typ de titel van het inhoudsfragment. Door gebrek, wordt de titel bevolkt met de titel van het onderwerp. U kunt het bestand bewerken. Deze titel wordt gebruikt om de naam van het inhoudsfragment te genereren.
   * **Naam**: Typ de naam van het inhoudsfragment. Door gebrek, wordt de naam bevolkt met de titel van het onderwerp, en de ruimten worden vervangen met &quot;_&quot;. Bijvoorbeeld: *sample_content_fragment*. U kunt het bestand bewerken.  Deze naam wordt gebruikt om de URL voor het inhoudsfragment te genereren.
   * **Model**: Selecteer het inhoudsfragmentmodel dat u wilt gebruiken om het inhoudsfragment te maken. De modellen worden gekozen uit de map die u hebt geconfigureerd in de cloudservices.
   * **Toewijzing**: Selecteer een toewijzing in de keuzelijst. De toewijzingen worden gekozen uit de *contentFragmentMapping.json* bestand.



     Uw beheerder kan de toewijzingen toevoegen in de *contentFragmentMapping.json* bestand. Meer informatie over hoe [een toewijzing maken tussen een onderwerp en een inhoudsfragment](../cs-install-guide/conf-content-fragment-mapping-cs.md) in de Installatie- en configuratiehandleiding.

   * U kunt ook verschillende voorwaarden selecteren om de inhoud te publiceren.  Selecteer een van de volgende opties:


      * **Geen**: Selecteer deze optie als u geen voorwaarde wilt toepassen op de gepubliceerde uitvoer.
      * **DITAVAL gebruiken**: Selecteer het DITAVAL-bestand om uitvoer te genereren die specifieke inhoud bevat. U kunt het DITAVAL-bestand selecteren in het dialoogvenster Bladeren of door het bestandspad te typen.
      * **Kenmerken gebruiken**: U kunt voorwaardenattributen in uw onderwerpen bepalen DITA. Selecteer vervolgens het kenmerk condition om de relevante inhoud te publiceren.
     >[!NOTE]
     > 
     >De voorwaarden worden toegelaten slechts als voorwaardelementen in het onderwerp worden bepaald.



   * Selecteren **Bestaande inhoud overschrijven** als het inhoudsfragment al bestaat en u dit wilt overschrijven. In de hulplijnen voor Experience Managers wordt een fout weergegeven als u het selectievakje niet inschakelt en het inhoudsfragment al bestaat.
1. Klikken **Genereren** om het inhoudsfragment te publiceren.

1. U kunt de Inhoudsfragmenten voor een onderwerp weergeven onder de categorie **Uitvoer** in de **Bestandseigenschappen**.

   ![De fragmenten met inhoud voor een onderwerp weergeven](images/outputs-options-menu.png){width="300" align="left"}

   *Bekijk de aanwezige Fragments van de Inhoud voor een onderwerp en publiceer hen opnieuw.*


Nadat u de inhoudsfragmenten hebt gepubliceerd, kunt u deze ook op elke Adobe Experience Manager-site gebruiken.




## Menu Opties voor een inhoudsfragment

U kunt ook de volgende handelingen uitvoeren voor een inhoudsfragment via het dialoogvenster **Opties** menu:

* **Genereren**: Publiceer het inhoudsfragment opnieuw om het bij te werken met de meest recente inhoud van het DITA-onderwerp. Wanneer u de uitvoer opnieuw genereert, kunt u het pad, de naam, de titel, het model en de toewijzing van het inhoudsfragment niet wijzigen. U kunt echter verschillende voorwaarden selecteren wanneer u de uitvoer opnieuw genereert.

* **Dupliceren**: Dupliceer een inhoudsfragment. U kunt het pad, de naam, de titel, het model en de toewijzing wijzigen. U kunt ook verschillende voorwaarden selecteren wanneer u een inhoudsfragment dupliceert.

* **Verwijderen**: Verwijder een inhoudsfragment uit de lijst met uitvoerbestanden. Er verschijnt een bevestigingsbericht. Nadat u hebt bevestigd, wordt het inhoudsfragment verwijderd uit het dialoogvenster **Uitvoer** lijst.

  >[!NOTE]
  >
  > Met deze actie wordt geen inhoud verwijderd uit het inhoudsfragment.

* **Weergave**: Geef de editor voor het inhoudsfragment weer. U kunt ook wijzigingen aanbrengen en opslaan.


