---
title: Experience Manager Guides en Edge Delivery Services (Beta)
description: Begrijp hoe Edge Delivery Services (Beta) de creatie- en publicatiemogelijkheden voor Experience Manager Guides uitbreidt.
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 7ca2eeb0356f3c82a8d970f291006fc6d19aca23
workflow-type: tm+mt
source-wordcount: '1532'
ht-degree: 0%

---

# Experience Manager Guides en Edge Delivery Services (Beta)

Adobe Experience Manager Guides staat u toe om uw inhoud DITA aan Edge Delivery Services (EDS), momenteel beschikbaar in *Beta*, door een specifiek op GitHub-Gebaseerd te publiceren profiel. Met deze mogelijkheid kunnen organisaties krachtige, responsieve documentatieervaringen bieden en tegelijk op DITA gebaseerde ontwerpworkflows in Experience Manager Guides onderhouden.

Voor meer details bij het gebruiken van EDS in Adobe Experience Manager, mening [ het Overzicht van Edge Delivery Services ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/edge-delivery/overview).

Om het publiceren van Experience Manager Guides aan EDS (Beta) toe te laten, moet u een reeks configuratiestappen over GitHub en Experience Manager Guides voltooien. In de onderstaande secties wordt elke stap in de juiste volgorde beschreven en wordt uitgelegd hoe deze in de algemene publicatieworkflow samenwerken.

1. [GitHub instellen en configureren voor EDS (Beta)](#set-up-and-configure-github-for-eds-beta)
2. [Een publicatieprofiel voor EDS (Beta) maken en configureren in Experience Manager Guides](#create-and-configure-a-publish-profile-for-eds-beta-in-experience-manager)
3. [Uitvoer aanpassen met EDS-blokken](#customize-output-using-eds-blocks)

Voor een snelle videoanalyse, mening [ het Publiceren in AEM Guides ](https://experienceleague.adobe.com/en/docs/experience-manager-guides/using/knowledge-base/expert-session/publishing-in-aem-guides-aug25).



## GitHub instellen en configureren voor EDS (Beta)

Deze sectie beschrijft hoe te opstelling en GitHub voor gebruik met EDS (Beta) te vormen. Het behandelt het creëren van een bewaarplaats gebruikend het Adobe boilerplate, die GitHub met Adobe Experience Manager door de Synchronisatie van de Code van AEM verbindt, vormend de vereiste toepassingen GitHub en OAuth, en het bepalen van de opslagplaats montpoint die voor het publiceren van inhoud wordt gebruikt.

### Een GitHub-opslagplaats maken voor EDS (Beta)

EDS (Beta) vereist een GitHub-opslagplaats met een vooraf gedefinieerde structuur. Adobe biedt een officiële opslagplaats voor bouwplaten die speciaal is ontworpen voor Experience Manager Guides-gebruikers.

Voer de volgende stappen uit om uw opslagplaats te maken:

1. Open de Experience Manager Guides boilerplate sjabloonopslagplaats [`aem-guides-boilerplate` ](https://github.com/adobe/aem-guides-boilerplate) .
   ![](assets/eds-boilerplate-template.png){align="left"}

2. Een nieuwe opslagplaats maken met deze sjabloon. Leer over [ Creërend een bewaarplaats van een malplaatje ](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template). Zorg ervoor dat het bewaarplaatszicht aan *Openbaar* wordt geplaatst zodat kan het door EDS worden betreden.

   ![](assets/eds-create-new-repo.png){align="left"}

De repository wordt nu gemaakt en uitgelijnd op de bouwsteensjabloonstructuur.

![](assets/eds-repo-created-github-view.png){align="left"}

### Connect GitHub aan Adobe via AEM Code Sync

Adobe Experience Manager gebruikt een toepassing GitHub genoemd **de Synchronisatie van de Code van AEM** om inhoud van Experience Manager Guides aan GitHub te duwen.

Voer de volgende stappen uit om de *toepassing van de Synchronisatie van de Code van AEM te installeren en te vormen*:

1. Navigeer aan de [ pagina van de Synchronisatie van de Code van AEM ](https://github.com/apps/aem-code-sync) en selecteer **installeer**.
2. *de Synchronisatie van de Code van AEM* controleert bewaarplaatsveranderingen en zorgt ervoor dat de updates correct aan GitHub worden geduwd.

   >[!NOTE]
   >
   > Terwijl het installeren van de toepassing, zorg ervoor dat u de zelfde rekening GitHub gebruikt die de bewaarplaats bezit.

   ![](assets/eds-aem-code-sync-page.png){align="left"}
3. Geef op de volgende pagina toegang tot de opslagplaats die u hebt gemaakt. Om dit te doen, selecteer **slechts bewaarplaatsen** optie en selecteer dan uw bewaarplaats van dropdown.

   ![](assets/eds-aem-code-sync-install-authorize.png){width="350" align="left"}
4. Selecteer **installeren en machtigen**.

U wordt opnieuw gericht aan de opstellingspagina van GitHub, die succesvolle registratie van de *de Synchronisatie van de Code van AEM bevestigen* toepassing. U kunt de voorbeeld- en live URL&#39;s voor uw website ook opslaan vanaf deze pagina.

![](assets/eds-aem-code-sync-registered.png){align="left"}

### Een nieuwe GitHub-app maken

1. Voor GitHub, navigeer aan linkerzijbalk en selecteer **montages van de Ontwikkelaar**.
2. In linkerzijbalk, uitgezochte **Apps GitHub**.
3. Selecteer **Nieuwe App GitHub**.

   ![](assets/eds-new-github-app.png){width="650" align="left"}
4. Op de **pagina van de Toepassing van GitHub van het Register nieuwe**, verstrek de volgende details:
   - **GitHub App naam**: ga een naam voor uw app in. Bijvoorbeeld, `USERNAME-eds-app` waar de GEBRUIKERSNAAM uw gebruikersnaam GitHub is.
   - **Homepage URL**: Ga URL aan de instantie van Experience Manager Guides in.

     Voorbeeld-URL (indeling): `https://<aem-author-url>/libs/fmdita/clientlibs/xmleditor/page.html`

     Voorbeeld-URL: `https://author-p16602-e335172-cmstg.adobeaemcloud.com/libs/fmdita/clientlibs/xmleditor/page.html`
   - **Callback URL**: Gelijk zoals Homepage URL.
   - **Webhaak URL**: maak deze optie onbruikbaar.
   - {de toestemmingen van de Bewaarplaats 0} **: Plaats** leest en schrijft **toestemmingen voor** Acties, Beleid, en Verklaring *.*
5. Selecteer **Create GitHub App**.

Uw app is nu klaar. U wordt opnieuw gericht aan de **pagina van Montages** van uw App GitHub.

![](assets/eds-github-app-registered-page.png){align="left"}

### Een nieuwe OAuth-app maken

Een OAuth-app is vereist om gebruikers te verifiëren tijdens het maken van een EDS (Beta)-publicatieprofiel in Experience Manager Guides. Het laat een veilige login stroom toe gebruikend identiteitskaart van de a *Cliënt* en *Geheime Cliënt*.

Voer de volgende stappen uit om een nieuwe OAuth App tot stand te brengen:

1. Voor GitHub, navigeer aan linkerzijbalk en selecteer **montages van de Ontwikkelaar**.
2. In linkerzijbalk, uitgezochte **OAuth Apps**.
3. Selecteer **Nieuwe OAuth App**.

   ![](assets/eds-new-oauth-app.png){width="650" align="left"}
4. Registreer uw toepassing door de volgende verplichte gegevens op te geven:
   - **naam van de Toepassing**: Ga de naam van uw bewaarplaats EDS in
   - **Homepage URL**: Ga URL aan de instantie van Experience Manager Guides in. (Voor steekproefformaat URL, verwijs naar stap 4 van [ creeer een nieuwe sectie van de App GitHub ](#create-a-new-github-app)).
   - **callback URL van de Vergunning**: Zelfde zoals Homepage URL
5. Selecteer **toelaten de Stroom van het Apparaat** optie en selecteer dan **toepassing van het Register** om de registratie te voltooien.

   ![](assets/eds-new-github-app-register.png){width="650" align="left"}

Uw app is nu klaar. Noteer neer *identiteitskaart van de Cliënt*. U kunt tot vijf *Secreten van de Cliënt* nu of later produceren terwijl het vormen van het publicatieprofiel in Experience Manager Guides.

![](assets/eds-new-oauth-app-page.png){align="left"}


### De URL van het montagepunt configureren in de EDS-opslagplaats (Beta)

EDS (Beta) leest inhoud van een weg van de bewaarplaats GitHub die als a *wordt bepaald bergpunt* URL in het `fstab.yaml` dossier.

U configureert als volgt de URL van het montagepunt in het `fstab.yaml` -bestand:

1. Open het `fstab.yaml` -bestand in uw opslagplaats en werk het volgende bij:
   - `your-user-name`
   - `your-repo-name`

   >[!NOTE]
   >
   > In de URL van het bevestigingspunt geeft `main` de vertakking aan waarop u de inhoud wilt publiceren en `docs` geeft de hoofdmap aan van de EDS (Beta)-opslagplaats waaraan u werkt. Als u verkiest om de taknaam op GitHub te veranderen, dan moet u de zelfde taknaam in *bijwerken montpoint* URL (in het `fstab.yaml` dossier) en overeenkomstige EDS publiceren profiel in Experience Manager Guides.

   ![](assets/eds-fstab-yaml-file.png){width="650" align="left"}
2. Selecteer **veranderingen** vastleggen, ga details in, en bevestig.
3. Terugkeer aan [ montages van de Ontwikkelaar ](https://github.com/settings/apps), bepaal de plaats van uw app, en selecteer **uitgeven**.

   ![](assets/eds-edit-github-app.png){width="650" align="left"}
4. Navigeer aan **installeer App** pagina en selecteer **installeer**.

   ![](assets/eds-install-eds-app.png){width="650" align="left"}
5. Herhaal stap 2 en 3 van [ Connect GitHub aan Adobe via de sectie van de Synchronisatie van de Code van AEM ](#connect-github-to-adobe-via-aem-code-sync) om de bewaarplaats te machtigen.

## Een publicatieprofiel voor EDS (Beta) maken en configureren in Experience Manager

In de onderstaande secties wordt elke stap in de juiste volgorde beschreven en wordt uitgelegd hoe u EDS (Beta)-publicatieprofiel instelt, een uitvoervoorinstelling configureert en uitvoer genereert met behulp van EDS (Beta) in Experience Manager Guides.

### Het EDS-publicatieprofiel (Beta) maken

1. Ga naar **[de montages van Workspace](/help/product-guide/cs-install-guide/workspace-settings.md)** **>** **publiceer profielen**.
2. Selecteer het pictogram **+** om een nieuw publicatieprofiel te maken en geef de volgende details op:
   - **Type van Server**: Selecteer **Edge Delivery Services GitHub (Beta)** van dropdown.
   - **Naam**: Ga een naam voor dit profiel in.
   - **Naam van de Bewaarplaats**: Gebruik de bewaarplaatsnaam GitHub die van boilerplate wordt gecreeerd.
   - **Gebruikersnaam**: Ga uw GitHub gebruikersbenaming in.
   - **Belangrijkste Tak**: Reeks aan hoofd (gebrek).
   - **omslag van de Wortel**: Reeks aan docs (gebrek).
   - **identiteitskaart van de Cliënt en Geheim van de Cliënt**: Vets deze van uw App GitHub (verwijs naar [ creeer een nieuwe App OAuth ](#create-a-new-oauth-app) sectie voor details).
3. Selecteer **Login** om voor authentiek te verklaren.

   ![](assets/eds-publish-profile.png){width="650" align="left"}
4. Voor succesvolle authentificatie, uitgezocht **sparen**.

Uw EDS-publicatieprofiel (Beta) is nu geconfigureerd.

### Een uitvoervoorinstelling maken voor EDS (Beta) en uitvoer genereren

1. Open uw kaart in de console van de Kaart.
2. In **vooraf instelt van de Output** lusje, selecteert **+** om een nieuwe output tot stand te brengen vooraf ingesteld.
3. In de **Nieuwe output vooraf ingestelde** dialoog, verstrek de volgende details:
   - **Type**: Selecteer **de Dienst van Edge Delivery (Beta)**
   - **Naam**: Verstrek een naam voor dit vooraf ingesteld
4. Selecteer **toevoegen**.

   ![](assets/eds-output-preset.png){width="650" align="left"}
5. Open nieuw gecreeerd EDS (Beta) output vooraf ingesteld en navigeer aan **Config** tabel.
   - Selecteer het publicatieprofiel dat u in de vorige stap hebt gemaakt.
   - Laat **Duw toe om** te leven.

   Wanneer **aan levende** wordt gedreven, wordt de geproduceerde output geëngageerd aan GitHub, en de overeenkomstige updates worden onmiddellijk verspreid aan de levende website.

   ![](assets/eds-output-preset-config-tab.png){width="650" align="left"}

6. Selecteer **sparen**, en dan **produceer output**.

>[!NOTE]
>
> De geproduceerde output wordt opgeslagen in de **docs** omslag van de bewaarplaats EDS (Beta).

De EDS-uitvoer (Beta) wordt nu gegenereerd. De inhoud wordt gepresenteerd in een schone, responsieve indeling. Het omvat regelmatige elementen zoals de paginatitel, broodkruimels, lichaamsinhoud, en om het even welke blokken die in het onderwerp worden gebruikt. Met de inhoudsopgave aan de linkerkant (die op basis van de kaart wordt gegenereerd) kunt u door onderwerpen navigeren, terwijl met een miniinhoudsopgave aan de rechterkant de secties op de huidige pagina worden gemarkeerd. De volledige uitvoer reageert volledig en zorgt voor een geoptimaliseerde, consistente leeservaring op alle apparaten.

![](assets/eds-site-output.png){align="left"}

## Uitvoer aanpassen met EDS-blokken

EDS gebruikt `blocks` om te bepalen hoe verschillende onderdelen van uw inhoud worden vormgegeven en weergegeven. U kunt bestaande blokken wijzigen of aangepaste blokken maken.

In de onderstaande voorbeelden wordt uitgelegd hoe u een bestaand blok aanpast en een nieuw blok maakt om de uiteindelijke EDS-uitvoer (Beta) in Experience Manager Guides op te maken.

### Een balkcrumb-blok aanpassen om de tekstkleur ervan bij te werken

Broodkruimels worden op verschillende pagina&#39;s gebruikt om gebruikers te helpen begrijpen waar ze zich in de documentatie bevinden. Aangezien dit blok overal op de website consistent wordt weergegeven, kunt u bij het bijwerken van de opmaak een uniforme ontwerpupdate uitvoeren.

Voer de volgende stappen uit om een broodkruimelblok aan te passen om zijn tekstkleur bij te werken:

1. Ga naar de GitHub-opslagplaats en open de `blocks` -map.
2. Selecteer het **broodkruimelblok**.

   ![](assets/eds-breadcrumbs.png){width="650" align="left"}
3. Open het `css` -bestand en werk de tekstkleur bij.
4. Leg de wijzigingen in GitHub vast.
5. Vernieuw de live website om de updates weer te geven.

### EDS-scripts (Beta) bijwerken om een aangepast element in de gepubliceerde uitvoer te maken

In sommige gevallen wilt u wellicht alleen een specifiek gedeelte van de inhoud opmaken. Voer de volgende stappen uit om dit te bereiken gebruikend een douaneblok.

1. Open het onderwerpbestand en selecteer de tekst in een labelelement.

   In de volgende schermafbeelding wordt de inhoud binnen de tag `example` geselecteerd.
   ![](assets/eds-example-tag-org-output.png){width="650" align="left"}
2. De tekst binnen de tag `example` configureren:
   - Navigeer aan **eigenschappen van de Inhoud**.
   - Voeg het kenmerk `outputclass` toe.
   - Stel de waarde in op `example eds-force-block` .
   - Selecteer **toevoegen**.
     ![](assets/eds-example-tag.png){width="650" align="left"}
3. Sla de uitvoer op en genereer deze opnieuw.
4. Maak een nieuwe map met dezelfde naam als de map `outputclass` in de map `blocks` . Leer over [ toevoegend dossiers aan een bewaarplaats ](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository#adding-a-file-to-a-repository-using-the-command-line).

   ![](assets/eds-example-folder.png){width="650" align="left"}
5. Voeg de vereiste `css` en optionele `js` bestanden toe.

   ![](assets/eds-example-folder-subfolders.png){width="650" align="left"}
6. Wijzigingen vastleggen en uitvoer opnieuw genereren.

De geselecteerde inhoud geeft nu de aangepaste opmaak weer die in uw blok is gedefinieerd.

![](assets/eds-example-output.png){width="650" align="left"}