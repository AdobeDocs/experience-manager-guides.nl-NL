---
title: AEM Sites-sjablonen voor Cloud-services downloaden en installeren
description: Leer hoe u AEM Sites-sjablonen voor Cloud-services kunt downloaden en installeren
feature: Installation
role: Admin
level: Experienced
exl-id: 67f7ff26-fbc7-426c-aa7d-9bf4debf05d8
source-git-commit: 4c564a0ffaa8f287bcaf012634d49dbf1e0682b4
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# AEM Sites-sjablonen downloaden en installeren (cloudservices)

Deze handleiding bevat stapsgewijze instructies voor het instellen en configureren van de nieuwste AEM Guides-sjabloon voor het genereren van AEM Sites-pagina&#39;s in een cloud-omgeving. Voer de volgende stappen uit om de vereiste pakketten te installeren, voorinstellingen te maken en te configureren en AEM Sites te genereren.

## Vereisten

Voordat u verdergaat met de installatie, moet u controleren of aan de volgende voorwaarden is voldaan:

- **Adobe Experience Manager (AEM) Wolk**: Een lopende instantie van **AEM as a Cloud Service** met **AEM Guides 2502 of recentere versies**.

- **Vereiste Toestemmingen**: U moet de volgende toestemmingen hebben:

   - Toegang tot **Cloud Manager** om pakketten op te stellen.
   - Toegang tot **Bewaarplaats van de it** verbonden aan uw milieu.
   - Machtigingen voor het maken en wijzigen van voorinstellingen in AEM Guides.

- **de Pakketten van de Download**: Download de volgende pakketten van het Portaal van de Distributie van de Software:

   - Componentpakket: guides-components.all-1.x.0.zip
   - Sitesjabloon: aemg-docs-1.x.0.zip

## Installatie van pakketten via cloud-implementatie

Installeer het **Pakket van Componenten (gidsen-componenten.all-1.x.x.zip)** en voer de volgende stappen uit

1. **de bewaarplaats van de Git van de Kloon:**
   1. Navigeer aan **Bewaarplaatsen** in het linkerpaneel van Cloud Manager.
   2. Selecteer **Info van de Reactie van de Toegang** en kopieer het bevel van de kloonkloon van de it.

      ![&#x200B; Uitgezochte Info van de Reactie van de Toegang &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/access-repo.png){width="350" align="left"}

   3. Clone the repository to your local system using the provided username and password (generate password if required).
2. **voeg Pakket aan Geweven Bundel toe:**
   1. Maak in uw lokaal gekloonde opslagplaats een nieuwe Maven-bundel of voeg deze toe aan een bestaande bundel.
   2. Controleer of de structuur van `/jcr_root/apps/fmdita/` aanwezig is in het Maven-project.

      ![&#x200B; Structuur in Geweven project &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/maven-structure.png){width="650" align="left"}


   3. Plaats het gedownloade bestand guides-components.all-1.x.x.zip in de installatiemap.

3. **Update filters.xml:**

   1. Open het bestand filters.xml in de map META-INF van de bovenliggende inhoudsmap.
   2. Voeg het volgende filter toe: filterroot=`/apps/fmdita` mode=`merge`/


      ![&#x200B; voeg filter &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/add-filter-xml.png){width="650" align="left"} toe


4. **vormt pom.xml:** werk het pom.xml- dossier volgens uw milieuvereisten bij.
5. **duw verandert en looppas Pijpleiding:**
   1. Verplaats de wijzigingen naar de Git-hoofdopslagplaats.
   2. Navigeer aan **Pijpleidingen** in Cloud Manager en stel de pijpleiding voor het gewenste milieu in werking.
6. **verifieer installatie:** Zodra de plaatsing volledig is, zal het componentenpakket op het milieu van de Wolk van AEM worden geïnstalleerd.

## Site maken met geïnstalleerde sjablonen

1. **Sjabloon van Plaatsen van de Invoer:**
   1. Ga naar de AEM Sites-pagina (servername/sites.html/content).
   2. Selecteer **creeer** > **Plaats** van Malplaatje.
   3. Importeer het plaatsmalplaatje aemg-docs-1.x.x.zip gebruikend de **optie van de Invoer**.
2. **Uitgezochte Malplaatje:** selecteer **AEMG Docs 1.x.x** en selecteer dan **daarna**.
3. **ga de Details van de Plaats in:** ga de **Titel van de Plaats** in en **Naam van de Plaats**.

   ![&#x200B; creeer Plaats &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/create-site.png){width="350" align="left"}

4. Selecteer **creeer**.

## AEM-sitevoorinstelling maken

1. **creeer nieuwe vooraf ingesteld:**
   1. Open een kaart DITA in AEM Guides en navigeer aan het **paneel van de Output**.
   2. Selecteer **creeer Vooraf ingesteld**.
   3. Selecteer het type als **AEM Sites**.
   4. Voer een naam in voor de voorinstelling.
   5. Uncheck het **plaatsen van de erfeniscomponentenafbeelding van het Gebruik**.

      ![&#x200B; creeer nieuwe vooraf ingestelde Plaats van AEM &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/create-new-output-preset.png){width="350" align="left"}

   6. Selecteer **toevoegen** om vooraf ingesteld tot stand te brengen.
2. **vorm de Vooraf ingestelde Plaats van AEM:** Er zijn twee opties om de uit-van-de-doos (OTB) plaats te vormen:

   **Optie 1: Gebruik Dropdown van de Plaats**

   1. Selecteer **Plaats** zoals hierboven gecreeerd (b.v., de Plaats van Docs AEMG).
   2. Verifieer dat het **publiceren weg** en **pagina van het Onderwerp** malplaatje automatisch wordt geplaatst aan:
      - Publicatiepad: `/content/AEMG-Docs-Site/en/docs/product`
      - Sjabloon voor onderwerppagina:

      ![&#x200B; Gebruik plaatsdrop-down om de Plaats van AEM &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/use-site-dropdown-cs.png){width="350" align="left"} te vormen

   **Optie 2: Gebruik de Weg van de Plaats**

   1. Plaats de **weg van de Plaats** manueel als `/content/AEMG-Docs-Site/en/docs/product`.
   2. Verifieer dat het **pagina van het Onderwerp** malplaatje automatisch aan de Pagina van het Onderwerp wordt geplaatst.

      ![&#x200B; Gebruik de plaatsweg om de Plaats van AEM te vormen &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/use-site-path-cs.png){width="650" align="left"}

3. **sparen vooraf ingesteld:** sparen de veranderingen die aan vooraf ingesteld worden aangebracht.

## AEM Sites genereren

1. **produceer Plaats:**
   1. Als de voorinstelling is geconfigureerd, genereert u de AEM-site voor de corresponderende DITA-kaart.
   2. De gegenereerde site is beschikbaar via het pad: `/content/AEMG-Docs-Site/en/docs/product` .
2. **verander de StandaardWeg van de Generatie (Facultatief):** als u de standaardweg voor plaatsgeneratie wilt veranderen, voer de volgende stappen uit:
   1. Navigeer aan **AEM Sites**.
   2. Maak een nieuwe productpagina onder de OOTB-sitestructuur.
   3. Navigeer aan **Dokken van AEMG** > **Engels** > **Dokken**.

      ![&#x200B; creeer pagina &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/create-page-cs.png){width="650" align="left"}

   4. Selecteer de **pagina van het Huis** tegel en selecteer dan **daarna**.

      ![&#x200B; Uitgezochte Titel van het Huis &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/home-tile-cs.png){width="650" align="left"}

   5. Ga de **Titel** en **Naam** voor de pagina in.
   6. Selecteer **creeer**.

>[!NOTE]
>
> Zorg ervoor dat alle configuraties in een niet-productieomgeving worden getest voordat u ze implementeert op productie. <br><br> verwijs naar het officiële [&#x200B; Opstellen aan de documentatie van AEM as a Cloud Service &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview) voor extra details.
