---
title: AEM Sites
description: Creeer en vorm vooraf ingesteld AEM Sites in de Redacteur van het Web en produceer de output van AEM Sites voor kaart DITA, geselecteerde onderwerpen, en verbonden onderwerpen.
feature: Publishing
role: User
source-git-commit: fa07db6a9cb8d8f5b133258acd5647631b22e28a
workflow-type: tm+mt
source-wordcount: '2732'
ht-degree: 0%

---

# AEM Sites-voorinstellingen in de webeditor


U kunt AEM Sites-voorinstellingen maken in de webeditor en deze configureren om de AEM Sites-uitvoer te genereren. De AEM Sites-uitvoer is gebaseerd op de samengestelde componenttoewijzing samen met de `guides-components` , waardoor het maken en beheren van efficiënte inhoud wordt vergemakkelijkt.

Experience Manager Guides biedt vooraf gedefinieerde sjablonen voor het maken van AEM Sites. Deze voorinstellingen zorgen voor consistentie in de indeling en structuur van de inhoud.
- [ creeer homepages ](../cs-install-guide/download-install-aem-sites-templates-cs.md#create-a-home-page-using-the-template) die op deze vooraf bepaalde malplaatjes worden gebaseerd.
- U kunt [ onderwerpmalplaatjes ](../cs-install-guide/download-install-aem-sites-templates-cs.md#package-installation) uitgeven en stijlen volgens uw vereisten toepassen.
- U kunt [ bestaande malplaatjes van AEM Sites ](../cs-install-guide/download-install-aem-sites-templates-cs.md#customize-existing-aem-sites-templates) ook aanpassen.



## AEM Sites-voorinstellingen maken

Voer de volgende stappen uit om de AEM Sites-voorinstellingen te maken van de webeditor:

1. Open het DITA-kaartbestand in de Kaartweergave in het deelvenster Opslagplaats.
1. In het **lusje van de Output**, selecteer + pictogram om tot een output vooraf ingesteld te leiden.
1. Selecteer **AEM Sites** van het **Type** drop-down in de **Nieuwe output vooraf ingestelde** dialoogdoos.
1. Deselecteer de **optie van de erfeniscomponentenafbeelding van het Gebruik** van de **Nieuwe vooraf ingestelde output** dialoogdoos.

![ Nieuw ](images/new-aem-sites-dialog-box.png)





>[!NOTE]
>
>Voordat u de AEM Sites-voorinstellingen voor Experience Manager Guides kunt configureren, moet uw beheerder een AEM Sites-structuur maken met de sjablonen.
- **Op-gebouwSoftware**: Leer meer over hoe te [ download en installeer de malplaatjes van AEM Sites ](../install-guide/download-install-aem-sites-templates.md) voor Software op-gebouw.
- **Cloud Service**: Leer meer over hoe te [ download en installeer de malplaatjes van AEM Sites ](../cs-install-guide/download-install-aem-sites-templates-cs.md) voor Cloud Service.




### Voorinstellingen toevoegen aan het huidige mapprofiel

Als beheerder kunt u met Experience Manager Guides uitvoervoorinstellingen voor de algemene profielen en de mapprofielen maken en beheren. Selecteer **toevoegen aan huidige omslagprofiel** optie van **Nieuwe output vooraf ingestelde** dialoogdoos om een output tot stand te brengen vooraf ingesteld voor het huidige omslagprofiel. ![ pictogram van het omslagprofiel ](images/global-preset-icon.svg) wijst op een vooraf ingesteld niveau van het omslagprofiel.  Leer meer over [ beheer Globale en de outputpresets van het Profiel van de Omslag ](./web-editor-manage-output-presets.md).

### AEM Sites-voorinstellingen op basis van toewijzing van oudere componenten

U kunt de AEM Sites-voorinstellingen ook maken met behulp van de toewijzing van oudere componenten. Om de AEM Sites tot stand te brengen stelt op de afbeelding van de erfeniscomponent worden gebaseerd, selecteert de uitgezochte **optie van de afbeelding van de erfeniscomponent van het Gebruik** van de **Nieuwe output vooraf ingestelde** dialoogdoos.

Sommige opties kunnen verschillen voor de voorinstellingen die oude componenttoewijzing gebruiken.



## De AEM Sites-voorinstellingen configureren

De configuraties worden georganiseerd onder **Algemene**, **Inhoud**, **Lijst van het Onderwerp**, en **de verwijzingen van de Cross-map** lusjes.

![ plaatsen vooraf ingestelde montages ](images/aem-sites-new-config.png)
**Algemeen**

Het **Algemene** lusje bevat de volgende configuraties met betrekking tot het produceren van output:

- Sitepad gebruiken
- Sitepad
- Site
- Publish-pad
- Sjabloon voor onderwerppagina
- Paginanamen genereren op basis van
   - Naam onderwerpbestand
   - Onderwerptitel
- Eerder gegenereerde pagina&#39;s opschonen
   - Eerder gegenereerde pagina&#39;s verwijderen voor onderwerpen die van de kaart zijn verwijderd
   - Verwijder alle pagina&#39;s die door andere bronnen zijn gemaakt op dit pad:
- Workflow na generatie



**Inhoud**

Het **lusje van de Inhoud** bevat de volgende configuraties:

- Basislijn gebruiken
- Voorwaarde filteren
- Aanvullende DITA-OT-opdrachtregelargumenten
- Metagegevens
   - File (Assets)-eigenschappen
   - Kaarteigenschappen gebruiken als fallback


Voor details, verwijs naar [ configuratie van AEM Sites ](#aem_sites_config).

**Lijst van het Onderwerp**

De **Lijst van het Onderwerp** toont de lijst van onderwerpen aanwezig in het huidige werkende exemplaar van de kaart DITA. Standaard worden alle onderwerpen opgenomen. U kunt specifieke onderwerpen selecteren en de output van AEM Sites slechts voor hen produceren. Bijvoorbeeld, hebt u sommige onderwerpen bijgewerkt zodat kunt u slechts die onderwerpen publiceren in plaats van de volledige kaart DITA publiceren.

**Lijst van het Onderwerp** het lusje is aanwezig in de AEM vooraf instelt die niet gebaseerd op erfenisafbeelding worden gecreeerd.

**verwijzingen dwars-kaart**
Deze lijst bevat onderwerpen met verwijzingen naar andere mappen met `scope ="peer"` . U kunt de publicatiecontext voor een lijst van verwijzingen naar cross-maps met `scope="peer"` aan onderwerpen specificeren beschikbaar in andere kaarten DITA. Dit tabblad wordt weergegeven als u de Experience Manager Guides-versie (UUID) gebruikt.



Leer meer over hoe te om [ verbonden onderwerpen ](#publish-linked-topics) te publiceren.





## AEM Sites-configuratie {#aem_sites_config}

De volgende opties zijn beschikbaar voor de AEM Sites-uitvoer:

| AEM Sites-opties | Beschrijving |
| --- | --- |
| Sitepad gebruiken | Gebruik deze optie om uw inhoud naar een site van de Experience Manager te publiceren. Selecteer deze optie als u precies weet waar u de uitvoer wilt publiceren. Geef ook het volledige pad op in het veld Sitepad. |
| Sitepad | Deze optie verschijnt als u **de optie van de de plaatsweg van het Gebruik** selecteert. Blader door het exacte pad naar de site van de Experience Manager waar u de uitvoer wilt publiceren. |
| Site | Naam van de Experience Manager Sites waarnaar u de inhoud wilt publiceren. De opties in het vervolgkeuzemenu worden gevuld op basis van de lijst met sites die beschikbaar zijn in AEM Sites. <br> Uitgezochte **verfrist zich** ![ refreseh pictogram ](images/navtitle-refresh-icon.svg) om een nieuwe lijst van opties te halen en op de bijgewerkte gegevens te wijzen. |
| Publish-pad | Het pad in de AEM opslagplaats waar de uitvoer wordt opgeslagen. Het Publish-pad wordt gevuld met alle paden die pagina&#39;s bevatten die zijn gemaakt op basis van de sjabloon Startpagina. De AEM Sites-uitvoer van de DITA-kaart wordt gegenereerd onder dit pad.  Als u bijvoorbeeld de Site opgeeft als `AEMG-Docs` en het Publish-pad als `aemg-docs-en/docs/product-abc.` , wordt de AEM Sites-uitvoer gegenereerd onder het knooppunt `aemg-docs-en/docs/product-abc/` in `crx/de` . |
| Sjabloon voor onderwerppagina | De structurele componenten die u kunt gebruiken om inhoud consistent in meerdere documenten te organiseren. Deze sjablonen zijn vooraf gedefinieerd in de Adobe Experience Manager-sitesjabloon. De opties worden bevolkt met alle malplaatjes van de onderwerppagina beschikbaar voor de geselecteerde Plaats. Selecteer het malplaatje u op alle outputonderwerpen wilt toepassen. |
| Paginanamen genereren op basis van | **filename van het Onderwerp**: Gebruikt het dossier van het onderwerp DITA naam om de Plaats URL tot stand te brengen. <br> **Titel van het Onderwerp**: Gebruikt de titel van het onderwerp DITA om de namen van de Plaats van de Experience Manager tot stand te brengen. |
| Eerder gegenereerde pagina&#39;s opschonen | - **schrapping eerder geproduceerde pagina&#39;s voor onderwerp dat van de kaart** wordt verwijderd: Als de structuur van de kaart DTIA verandert, kunt u deze optie gebruiken om de eerder geproduceerde pagina&#39;s voor de verwijderde onderwerpen te verwijderen. Deze functie is alleen beschikbaar voor volledige publicatie op de kaart.<br><br> zegt u een kaart DITA hebt gepubliceerd, die onderwerpen a.dita, b.dita, en c.dita bevat. Alvorens de kaart opnieuw te publiceren, verwijderde u b.dita onderwerp van de kaart. Als u deze optie hebt geselecteerd, wordt alle inhoud met betrekking tot b.dita verwijderd uit de AEM Sites-uitvoer en worden alleen a.dita en c.dita gepubliceerd.<br><br>**Nota**: De informatie over geschrapte pagina&#39;s wordt ook gevangen in de logboeken van de outputgeneratie. Voor meer informatie over de toegang tot van de logboekdossiers, [ Mening en controleer het logboekdossier ](generate-output-basic-troubleshooting.md#id1821I0Y0G0A__id1822G0P0CHS). <br><br>**Voorzichtigheid**: Bij het schrappen van de onderwerpen, worden de pagina&#39;s niet beschikbaar van de gepubliceerde plaats. Dus voordat de onderwerpen worden verwijderd, verschijnt er een waarschuwing. U moet bevestigen om hen te schrappen.<br><br> - **schrap alle pagina&#39;s die door andere bronnen bij deze weg** worden gecreeerd: Als u deze optie selecteert, worden alle pagina&#39;s die op deze weg van andere kaarten, individuele onderwerpen, of een andere bron worden gepubliceerd geschrapt. De pagina&#39;s zijn ook niet meer beschikbaar op de gepubliceerde site. Dus voordat de onderwerpen worden verwijderd, verschijnt er een waarschuwing. U moet bevestigen om hen te schrappen. |
| Workflow na generatie | Wanneer u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Werkstroom na generatie weergegeven met alle werkstromen die in AEM zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid. |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br>**Belangrijk**: Wanneer u stijgende output voor de AEM Plaats produceert, dan wordt de output gecreeerd gebruikend de huidige versie van de dossiers en niet de in bijlage Basislijn.<br><br> het Werk van de Mening [ met Basislijn ](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer details. |
| Voorwaardelijk filteren | Selecteer één van de volgende opties:<br><br>**niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>**Gebruikend DITAVAL**: Selecteer DITAVal dossier(s) om geconditionaliseerde inhoud te produceren. U kunt meerdere DITAVal-bestanden selecteren via het dialoogvenster Bladeren of door een bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVal-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVal-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch verwijderd van het kaartdashboard. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad weer te geven in de AEM opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVal-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype selecteert.<br>**Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. Deze optie is zichtbaar als u een voorwaarde voor het DITA kaartdossier hebt toegevoegd. De voorwaardelijke instellingen zijn beschikbaar op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Meer over voorwaarde vooraf ingesteld, mening [ vooraf instelt van het Gebruik van de voorwaarde ](generate-output-use-condition-presets.md#id1825FL004PN). |
| Aanvullende DITA-OT opdrachtregelargumenten | Geef de aanvullende argumenten op die u tijdens het genereren van uitvoer wilt laten verwerken door DITA-OT. Voor details over de bevel-lijn argumenten die in DITA-OT worden gesteund, mening [ DITA-OT documentatie ](https://www.dita-ot.org/). |
| Metagegevens <br> <br> Dossier (Assets) Eigenschappen | Selecteer de eigenschappen die u als metagegevens wilt verwerken. Deze eigenschappen worden ingesteld op de pagina Eigenschappen van de DITA-kaart of het bladwijzerbestand. De eigenschappen u van de dropdown lijst selecteert verschijnen onder het **gebied van de Eigenschappen van het Dossier 0} {.** Selecteer het kruispictogram naast de eigenschap om deze te verwijderen. <br><br>**Nota**: De meta-gegevenseigenschappen zijn case-sensitive.<br><br>*als u een Basislijn hebt geselecteerd, dan zijn de waarden voor de eigenschappen gebaseerd op de versie van de geselecteerde Basislijn.<br>* Als u geen basislijn hebt geselecteerd, zijn de waarden voor de eigenschappen gebaseerd op de meest recente versie.<br><br> u kunt de meta-gegevens tot de output ook overgaan gebruikend DITA-OT het publiceren. Voor meer detailmening, [ pas op de meta-gegevens aan de output over gebruikend DITA-OT ](pass-metadata-dita-ot.md#id21BJ00QD0XA).<br><br>**Nota**: Als u niet `cq:tags` in de optie van Eigenschappen hebt bepaald, dan worden de waarden voor `cq:tags` genomen van het huidige het werk exemplaar zelfs als u een Basislijn voor het publiceren hebt geselecteerd. |
| Metagegevens <br> <br> Kaarteigenschappen gebruiken als fallback | Als deze optie is geselecteerd, worden de eigenschappen die voor het kaartbestand zijn gedefinieerd, ook gekopieerd naar de onderwerpen waar deze eigenschappen niet zijn gedefinieerd. Overweeg de volgende punten terwijl het gebruiken van deze optie:<br><br>*slechts Koord, Datum, of Lange (enig en multi-getaxeerd) eigenschappen kunnen tot de pagina&#39;s van de AEMPlaats worden overgegaan.<br>* De metagegevenswaarden voor een eigenschap van het type String ondersteunen geen speciale tekens (zoals `@, #, " "` ).<br>* Deze optie moet samen met de optie `Properties` worden gebruikt. |
| Tijdelijke bestanden behouden | Selecteer deze optie om de tijdelijke bestanden te behouden die door DITA-OT worden gegenereerd. Als er fouten optreden bij het genereren van uitvoer via DITA-OT, selecteert u deze optie om de tijdelijke bestanden te behouden. U kunt die dossiers dan gebruiken om de fouten van de outputgeneratie problemen op te lossen.<br> <br> Na het produceren van de output, selecteer het **tijdelijke dossiers van de Download** ![ pictogram van de download tijdelijke dossiers ](images/download-temp-files-icon.png) om de omslag te downloaden van het PIT die de tijdelijke dossiers bevat. <br><br> **Nota**: Als de dossiereigenschappen tijdens generatie worden toegevoegd, omvatten de output tijdelijke dossiers ook a *metadata.xml* dossier die die eigenschappen bevatten. |


### De AEM Sites-uitvoer genereren met behulp van de sjablonen

Met Experience Manager Guides kunt u de out of box-sjablonen gebruiken of uw eigen AEM Sites-sjablonen toevoegen.

Voordat u de AEM Sites-voorinstellingen configureert, moet u ervoor zorgen dat u een AEM Sites-structuur maakt met de sjablonen.\
Voor meer details, mening [ Download en installeer de malplaatjes van AEM Sites ](../install-guide/download-install-aem-sites-templates.md).



Voer de volgende stappen uit om een AEM Sites-voorinstelling te maken en te configureren:
1. Open de **Output vooraf instelt** lusje van de kaart DITA u wilt publiceren.
1. Selecteer **AEM Sites** vooraf ingestelde output.
1. (Facultatief) uncheck **optie van de afbeelding van de erfeniscomponent van het Gebruik** om een niet erfenisAEM Sites tot stand te brengen vooraf ingesteld.
1. Klik **toevoegen**. De voorinstelling voor AEM Sites wordt gemaakt.
1. U kunt uit-van-de-doos malplaatje van Plaatsen op twee manieren vormen:
   1. Selecteer **Plaats** en kies dan de publicatieweg en de malplaatjes van de onderwerppagina van de bevolkte opties:
      1. Selecteer de site.
      1. Selecteer **Plaats**. Bijvoorbeeld `AEMG Docs` .
      1. De **weg van Publish** en de **pagina van het Onderwerp sjabloon** opties worden automatisch geplaatst in dropdown. U kunt ook de opties kiezen. `AEMG-Docs-Site/en/docs/product1` en `Topic page` worden bijvoorbeeld ingesteld.
   1. Selecteer het volledige pad naar de site:
      1. Selecteer **de weg van de Plaats van het Gebruik** optie.
      1. Selecteer het volledige pad naar de site. Bijvoorbeeld `/content/AEMG-Docs-Site/en/docs/product1` .
      1. De sjabloon &#39;Onderwerppagina&#39; wordt automatisch ingesteld als `Topic Page` .


1. Sla de wijzigingen in de voorinstelling op.
1. Selecteer **produceren** optie.
1. AEM Sites genereren voor de corresponderende kaart. Bijvoorbeeld `/content/AEMG-Docs-Site/en/docs/product` .


   >[!NOTE]
   >
   > Als u voor het eerst inhoud op een AEM site publiceert, is het raadzaam de pagina&#39;s op siteniveau te publiceren. Dit verzekert de output correct op de **Publish** instantie zonder enige CSS verstoring wordt getoond.



### Aan Publish gekoppelde onderwerpen

Experience Manager Guides vereenvoudigt het publiceren van complexe documenten door u toe te staan om onderwerpverwijzingen tot stand te brengen gebruikend `peer @scope`. Vervolgens kunt u de publicatiecontext van deze verwijzingen definiëren in de AEM Sites-voorinstellingen en ten slotte de uitvoer van de gekoppelde onderwerpen genereren.
Voor meer details, produceren de mening [ output van het verbinden onderwerpen van andere kaarten ](../user-guide/generate-output-aem-site.md#generate-output-linking-topics-from-other-maps).




Voer de volgende stappen uit om de publicatiecontext voor cross-linked bestanden op te geven:
1. Open de **Output vooraf instelt** lusje van de kaart DITA u wilt publiceren.
1. Selecteer **AEM Sites** vooraf ingestelde output.

   U kunt de **Algemene** bekijken, **Inhoud**, **Lijst van het Onderwerp**, en **Verwijzingen van de Cross-map** lusjes. **de verwijzingen van de Cross-map** tabel verschijnt als u de versie van Experience Manager Guides (UUID) gebruikt.

   In de volgende gevallen kunt u de cross-map link niet bekijken:
   - Voor de voorinstellingen die vóór de release 4.6 zijn gemaakt. Het tabblad Kruisverwijzingen is uitgeschakeld en knopinfo, Verwijzen naar het dashboard Kaart, wordt weergegeven.
   - Voor voorinstellingen die zijn gemaakt van het kaartdashboard. De knopinfo Kaart verwijst naar de knopinfo voor het dashboard.
   - Voor OOTB-voorinstellingen wordt de knopinfo Verwijzen naar het dashboard Kaart weergegeven.
   - Voor algemene voorinstellingen maakt u een lokale kopie van deze algemene voorinstelling om verwijzingen naar kruismappen in te stellen.
Als u AEM Sites-voorinstellingen uit de webeditor wilt gebruiken, maakt u een nieuwe voorinstelling of dupliceert u de bestaande voorinstelling.

1. Open de **verwijzingen van de Cross-map** tabel.

   U wordt getoond een lijst van onderwerpen en hun verwijzingen. U kunt de het publiceren context voor een lijst van dwars-kaartverwijzingen naar onderwerpen specificeren beschikbaar in andere kaarten DITA met `scope="peer"`.

   `<xrefs>` moet unieke id&#39;s hebben om het referentiepaneel voor kruisverwijzingen in de webeditor te kunnen gebruiken. Unieke id&#39;s voor `<xrefs>` worden automatisch gegenereerd bij het bewerken/opslaan van de oudere inhoud als de id er niet is.

   >[!NOTE]
   >
   >Het **lusje van de Verwijzingen van de Cross-map** toont onderwerpen die het gebruiken van slechts `scope="peer"` verbonden zijn. Voor koppelingen met `scope="local"` hoeft u de publicatiecontext niet op te geven.

   Voor alle gekoppelde onderwerpen is de laatste uitvoervoorinstelling en de kaart standaard geselecteerd. De publicatiecontext voor alle gekoppelde onderwerpen wordt standaard ingesteld op `<Most recently generated>` mapping.

   ![ de verwijzingen van de Cross-map ](images/aem-sites-cross-map-references.png)

1. Als u de onlangs gepubliceerde output van elk afhankelijk dossier in de kaart wilt gebruiken, selecteert het uitgezochte **Gebruik onlangs geproduceerd** publiceer context voor alle afhankelijke onderwerpen.
U zou de kaart moeten publiceren die als ouderkaart wordt geselecteerd alvorens de kaart te publiceren die verbonden onderwerpen bevat. Als de kaart met verbonden onderwerpen niet wordt gepubliceerd, verschijnen de verbindingen als normale teksten in plaats van hyperlinks in de output van AEM Sites.
U moet hetzelfde type AEM Sites-voorinstelling selecteren voor het gekoppelde onderwerp. Als de huidige AEM Sites-voorinstelling bijvoorbeeld gebruikmaakt van oudere componenttoewijzing, selecteert u een vergelijkbare AEM Sites-voorinstelling van het gekoppelde onderwerp.
1. Selecteer in de vervolgkeuzelijst Bovenliggende kaart het kaartbestand met de uitvoer die u wilt koppelen aan de uitvoer van de huidige kaart.
Als u een kaartbestand selecteert, wordt de UUID van de kaart weergegeven in de kolom UUID van bovenliggende kaart. De uitvoervoorinstellingen die aan de gekozen kaart zijn gekoppeld, worden vermeld in de lijst Voorinstellingen bovenliggende kaart. Bijvoorbeeld, bevat Onderwerp 1 in Kaart A een verwijzing naar Onderwerp 2. Onderwerp 2 kan aanwezig zijn in enige of veelvoudige kaarten. U kunt de bovenliggende kaart en een specifieke voorinstelling selecteren of de meest recente gepubliceerde uitvoer voor elke koppeling.

1. Als het zelfde onderwerp naar meer dan eens in een dossier wordt verwezen, dan kunt u een verschillende het publiceren context voor elke instantie toevoegen. Dit biedt meer flexibiliteit en controle over de inhoud ervan. Bijvoorbeeld, is Onderwerp 3 aanwezig in zowel Kaart B als Kaart C. Onderwerp 1 bevat twee verwijzingen naar Onderwerp 3. U kunt Kaart B als ouderkaart voor de eerste verbinding en Kaart C als ouder voor de tweede verbinding kiezen.

1. Selecteer in de vervolgkeuzelijst Voorinstelling bovenliggende kaart de uitvoervoorinstelling waarmee u de uitvoer van de huidige kaart wilt koppelen.
   >[!NOTE]
   >
   > De verschillende AEM Sites-voorinstellingen van de huidige kaart worden weergegeven in de vervolgkeuzelijst. Als u geen voorinstelling selecteert, wordt een waarschuwingspictogram weergegeven en mislukt het genereren van de uitvoer.
1. Selecteer de vereiste kaart en zijn output vooraf instelt voor alle brononderwerpen en uitgezocht **produceert**.







**Bovenliggend onderwerp:** [ Begrijpend de output stelt ](generate-output-understand-presets.md) vooraf in
