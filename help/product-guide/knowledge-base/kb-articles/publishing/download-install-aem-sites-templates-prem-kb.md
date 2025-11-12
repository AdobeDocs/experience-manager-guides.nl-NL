---
title: AEM Sites-sjablonen voor services op locatie downloaden en installeren
description: Leer hoe u AEM Sites-sjablonen kunt downloaden en installeren voor op Prem Services
feature: Installation
role: Admin
level: Experienced
exl-id: aa843a72-ff0d-4c9a-a87d-48d099087b5e
source-git-commit: 4c564a0ffaa8f287bcaf012634d49dbf1e0682b4
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# AEM Sites-sjablonen downloaden en installeren (services op locatie)

Deze handleiding bevat stapsgewijze instructies voor het instellen en configureren van de nieuwste AEM Guides-sjabloon voor het genereren van AEM Sites. Voer de volgende stappen uit om de vereiste pakketten te installeren, voorinstellingen te maken en te configureren en AEM Sites te genereren.

## Vereisten

Voordat u verdergaat met de installatie, moet u controleren of aan de volgende voorwaarden is voldaan:

- **Adobe Experience Manager (AEM):** Een lopende instantie van **AEM 6.5** met **Service Pack** 21, 20, en 19 en **AEM Guides 4.6.0**, of recentere geïnstalleerde versies.

- **Vereiste Toestemmingen**: Zorg ervoor om de volgende toestemmingen te hebben:

   - Toegang tot **Portaal van de Distributie van de Software** om de vereiste pakketten te downloaden
   - Toegang tot **de Manager van het Pakket van CRX** om pakketten in AEM te installeren.
   - Machtigingen voor het maken en wijzigen van voorinstellingen in AEM Guides.

- **Pakketten van de Download**: Download de volgende pakketten van **het Portaal van de Distributie van de Software**:

   - Componentpakket: on-prem-guides-components.all-1.x.0.zip
   - Sites-pakket: aemg-docs.all-1.x.0.zip

## Installatie van pakketten met CRX Package Manager

1. **installeer het Pakket van Componenten:**
   1. Navigeer aan [**de Manager van het Pakket van CRX** &#x200B;](http://&lt;your-name-instance>/crx/packmgr).
   2. Upload en installeer het zip-pakket on-prem-guides-components.all-1.x.0.zip.

2. **installeer het Pakket van Plaatsen:** upload en installeer het pakket aemg-docs.all-1.x.0.zip gebruikend de Manager van het Pakket van CRX.


## AEM-sitevoorinstelling maken en configureren

1. **creeer nieuwe vooraf ingesteld:**
   1. Open een kaart DITA in AEM Guides en navigeer aan het **paneel van de Output**.
   2. Selecteer **creeer Vooraf ingesteld**.
   3. Selecteer het type als **AEM Sites**.
   4. Voer een naam in voor de voorinstelling.
   5. Uncheck het **plaatsen van de erfeniscomponentenafbeelding van het Gebruik**.
   6. Selecteer **toevoegen** om vooraf ingesteld tot stand te brengen.

      ![&#x200B; Nieuwe output vooraf ingestelde dialoog &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/new-output-preset.png){width="350" align="left"}


2. **vorm de Vooraf ingestelde Plaats van AEM:** Er zijn twee opties om de uit-van-de-doos (OTB) plaats te vormen:

   **Optie 1: Gebruik Dropdown van de Plaats**

   1. Selecteer **Plaats** als **AEMG Docs**.
   2. Verifieer dat het **publiceren weg** en **de paginamalplaatje van het Onderwerp** automatisch wordt geplaatst aan:
      - Publicatiepad: `aemg-docs/en/docs/product1`
      - Sjabloon voor onderwerppagina: onderwerppagina.

      ![&#x200B; Vervolgkeuzelijst van de Plaats van het Gebruik &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/use-site-dropdown.png){width="350" align="left"}

   **Optie 2: Gebruik de Weg van de Plaats**

   1. Plaats de **weg van de Plaats** manueel als `/content/aemg-docs/en/docs/product1`.
   2. Verifieer dat het **paginamalplaatje van het Onderwerp** automatisch aan de Pagina van het Onderwerp wordt geplaatst.

      ![&#x200B; Pad van de Plaats van het Gebruik &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/use-site-path.png){width="350" align="left"}

3. **sparen vooraf ingesteld:** sparen de veranderingen die aan vooraf ingesteld worden aangebracht.

## AEM Sites genereren

1. **produceer Plaats:**
   1. Als de voorinstelling is geconfigureerd, kunt u nu de AEM-site voor de bijbehorende DITA-kaart genereren.
   2. De gegenereerde site is beschikbaar via het pad: `/content/aemg-docs/en/docs/product1` .
2. **verander de StandaardWeg van de Generatie (Facultatief):** als u de standaardweg voor plaatsgeneratie wilt veranderen, voer de volgende stappen uit:

   1. Navigeer aan **AEM Sites**.
   2. Maak een nieuwe productpagina onder de OOTB-sitestructuur.
   3. Navigeer aan **Dokken van AEMG** > **Engels** > **Dokken**.

      ![&#x200B; Pagina maken in AEM-sitestructuur &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/create-new-page.png){width="350" align="left"}

   4. Selecteer de **pagina van het Huis** tegel en selecteer dan **daarna**.

      ![&#x200B; Uitgezochte de tegel van de homepage &#x200B;](/help/product-guide/knowledge-base/kb-articles/assets/publishing/home-page-tile.png){width="350" align="left"}

   5. Ga de **Titel** en **Naam** voor de pagina in.
   6. Selecteer **creeer**.
