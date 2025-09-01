---
title: Bestaande AEM-sitesjablonen aanpassen voor AEM Guides
description: Leer hoe u bestaande AEM Site-sjablonen voor AEM Guides kunt aanpassen
feature: Installation
role: Admin
level: Experienced
source-git-commit: 1cec8975e8aad56184793a023d066aa467d8cec5
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 0%

---

# Bestaande AEM-sitesjablonen aanpassen voor AEM Guides

Deze gids verstrekt geleidelijke instructies om bestaande malplaatjes van de Plaats van AEM voor gebruik met AEM Guides aan te passen om AEM Sites van kaarten DITA en onderwerpen te produceren.

Als u de uit-van-de-doos AEM Guides (AEMG Docs) malplaatje gebruikt, zijn de configuraties en de componenten reeds op zijn plaats en kunnen worden gebruikt aangezien-is om uw inhoud van AEM Guides te publiceren. Als u echter uw bestaande AEM Sites-sjablonen met aangepaste branding wilt gebruiken om AEM Guides-inhoud te publiceren, volgt u de onderstaande stappen om uw sitesjablonen uit te lijnen met de AEM Guides-renderingvereisten.


## Vereisten

- U hebt de juiste machtigingen en toegang tot AEM-sjablonen.
- U kent bewerkbare AEM-sjablonen en de AEM-sitestructuur.
- U hebt een bestaande sitehiërarchie gemaakt met bewerkbare sjablonen.
- U hebt minstens twee malplaatjes van uw bestaand project:

   - **het Malplaatje van de Pagina van de Container van de Documentatie** wordt gebruikt voor het teruggeven van de kaart DITA als documentatiewortel die.
   - {het Malplaatje van de Pagina van 0} Onderwerp **wordt gebruikt om individuele DITA onderwerppagina&#39;s terug te geven die.**

## Overwegingen voor sjabloonnaamgeving

De namen van het malplaatje zullen variëren gebaseerd op projectopstelling. Bijvoorbeeld in de configuratie OOTB AEMG Docs:

- Documentatiecontainerpagina: /conf/AEMG-Docs-Site/settings/wcm/templates/kb-content

- Onderwerppagina: /conf/AEMG-Docs-Site/settings/wcm/templates/topic-content

**Aanpassing:** het aanpassingsproces impliceert twee belangrijke stappen:

1. De opstelling van het malplaatje: Identificeer en vorm de twee malplaatjes (container en onderwerp).
2. Componenten van Hulplijnen renderen: de vereiste AEM Guides-componenten insluiten om functies zoals inhoudsopgave, navigatie en weergave van metagegevens in te schakelen.

## Sjablooninstelling

Kies en configureer twee bewerkbare sjablonen op uw AEM-site.

### Documentatiecontainerpaginasjabloon

De sjabloon Documentatiecontainerpagina wordt gebruikt om de Containerpagina voor productdocumentatie te maken die de inhoud van een DITA-kaart weergeeft.

- Het dient als ingangspunt of startpagina voor een specifieke reeks documentatie (bijvoorbeeld een producthandleiding of gids).
- Voeg id= &quot;categorie-pagina&quot;bezit aan jcr :content van de aanvankelijke knoop van het malplaatje toe. Op deze manier worden alle pagina&#39;s die met deze sjabloon zijn gemaakt, automatisch door AEM Guides behandeld als documentcontainers.

  ![ Toevoegend id= &quot;categorie-pagina&quot;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/add-id-category-page.png){width="650" align="left"}

- Voeg een component Text toe met de verplichte eigenschap: text=&quot;$category.html$&quot;.

  ![ Toevoegend tekstcomponent ](/help/product-guide/knowledge-base/kb-articles/assets/publishing/add-text-component.png){width="650" align="left"}

- Bevat doorgaans navigatie-elementen, zoals koppelingen naar secties of onderwerpen in de documentatie.
- Het kan worden aangepast om branding, kopballen, footers, en andere ontwerpelementen te omvatten.

**het gebruiksgeval van het Voorbeeld:**
Als u een kaart DITA voor een producthandboek hebt, zal het malplaatje van de documentatiecontainerpagina de homepage voor die handleiding produceren, die een overzicht en verbindingen met individuele onderwerpen toont.

### Sjabloon voor onderwerppagina

- Het **malplaatje van de Pagina van het Onderwerp** wordt gebruikt om pagina&#39;s voor individuele **onderwerpen DITA** tot stand te brengen.
- Elk onderwerp in een kaart DITA wordt teruggegeven als afzonderlijke pagina gebruikend dit malplaatje.
- Bevat de component van de a **Tekst** met het verplichte bezit: text= &quot;$topic.content$&quot;.

  ![ Toevoegend tekstcomponent met verplicht bezit ](/help/product-guide/knowledge-base/kb-articles/assets/publishing/add-text-component-mandatory-property.png){width="650" align="left"}

- Deze placeholder wordt vervangen met de daadwerkelijke inhoud van het onderwerp DITA tijdens plaatsgeneratie.
   - De tekstcomponent wordt typisch geplaatst binnen de component van de a **Container** om juiste lay-out en het stileren te verzekeren.
   - Kan worden aangepast om consistente kopteksten, footers, en navigatieelementen over alle onderwerppagina&#39;s te omvatten.

**het gebruiksgeval van het Voorbeeld:**
Als u een onderwerp DITA over &quot;de Instructies van de Installatie hebt,&quot;zal het malplaatje van de onderwerppagina een pagina produceren die de inhoud van dat onderwerp toont.

**component van de Container:**

![ Toevoegend containercomponent ](/help/product-guide/knowledge-base/kb-articles/assets/publishing/add-container-component.png){width="650" align="left"}

>[!NOTE]
>
> Zorg ervoor dat de componenten die helling gebruiken :resourceType onder wcm/stichting/componenten worden gemigreerd aan de overeenkomstige kern/wcm/componenten.

Voeg hetzelfde element (container en tekstcomponent) toe aan de structuur van dezelfde sjabloon:

![ Toevoegend container en tekstcomponent ](/help/product-guide/knowledge-base/kb-articles/assets/publishing/add-container-and-text-component.png){width="650" align="left"}

## Hulplijncomponenten renderen in aangepaste sjablonen

Als u de belangrijkste functies van AEM Guides-componenten wilt inschakelen, zoals de inhoudsopgave, de omleiding van pagina&#39;s, de navigatie en de weergave van metagegevens, moet u specifieke AEM Guides-componenten opnemen in uw aangepaste sjablonen. Deze componenten moeten expliciet worden toegevoegd aan de bijbehorende bewerkbare sjablonen (Documentatie Container Page of Topic Page) om ervoor te zorgen dat de bedoelde functionaliteit beschikbaar is tijdens het genereren en uitvoeren van de site.

Raadpleeg de onderstaande tabel voor de lijst met componenten en het gebruik ervan:

| Functie | Componentnaam | Beschrijving | Aanbevolen sjabloon |
|---|---|---|---|
| Inhoudsopgave | guidessieavigatie | Hiermee wordt de volledige inhoudsopgave van de DITA-kaart weergegeven | Documentatiecontainer |
| Pagina omleiden | kinderdirecte | Omleiding naar de eerste onderwerppagina in de kaart | Documentatiecontainer |
| Mini-inhoudsopgave | minitoc | De TOC van vertoningen voor het huidige onderwerp | Onderwerppagina |
| Laatst bijgewerkt | pageproperty | Laatste gewijzigde datum weergeven | Onderwerppagina |
| Semafoon | pager | Staat navigatie tussen vorige en volgende onderwerppagina&#39;s toe | Onderwerppagina |
| Taalnavigatie | taalavigatie | Laat het schakelen tussen verschillende taalversies toe | Willekeurige sjabloon |


## Onderdeelgebruik

- **Redirect component (onderliggende componenten):** voeg dit aan het malplaatje van de documentcontainer pagina toe zodat de pagina van het producthuis die van de kaart DITA wordt geproduceerd automatisch aan de eerste onderwerppagina opnieuw richt. Als de pagina met de documentatiecontainer is ontworpen als zelfstandige startpagina met aangepaste componenten en lay-out, is deze component niet vereist.

- **Inhoudsopgave (gidsenavigatie):** voeg dit aan het malplaatje van de onderwerppagina toe om navigable TOC naast de onderwerpinhoud terug te geven. TOC wordt afgeleid uit de kaart DITA en helpt gebruikers over sibling onderwerpen navigeren.


## Hulplijnen-clientbibliotheken inschakelen

Standaard worden de clientbibliotheken (clientlibs) in het AEM Guides-componentenpakket niet toegepast op aangepaste sjablonen. Om hen toe te laten:

1. **geef het Malplaatje uit:**

   1. Open de **Pagina van het Product** in **Wijze van de Redacteur**.
   2. Selecteer **uitgeven Malplaatje** (dit zal URL zoals conf/settings/wcm/templates/structure.html openen).

      ![ geef malplaatje ](/help/product-guide/knowledge-base/kb-articles/assets/publishing/edit-template.png){width="650" align="left"} uit

2. **het Beleid van de Pagina van de Update:**

   1. Ga naar de **knoop van de Informatie van de Pagina** en selecteer **Beleid van de Pagina**.
   2. Voeg de volgende clientbibliotheken toe:
      - **Bibliotheken van de Cliënt**
      - **de Bibliotheken van de Cliënt JavaScript het Hoofd van de Pagina**

3. **sparen veranderingen:** sparen het malplaatje na het toevoegen van de vereiste cliëntbibliotheken.

   ![ voegt cliëntbibliotheken ](/help/product-guide/knowledge-base/kb-articles/assets/publishing/add-client-libraries.png){width="650" align="left"} toe


>[!NOTE]
>
> Zorg ervoor dat de sjablonen worden getest in een niet-productieomgeving voordat u ze implementeert op productie.<br><br> verwijs naar de officiële [ AEM Guides ](https://experienceleague.adobe.com/en/docs/experience-manager-guides/using/overview) en [ AEM Sites ](https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/get-started/authoring) documentatie voor extra details.
