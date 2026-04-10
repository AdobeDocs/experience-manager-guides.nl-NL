---
title: Upgrade uitvoeren voor Adobe Experience Manager Guides
description: Meer informatie over het upgraden van Adobe Experience Manager Guides
feature: Installation
role: Admin
level: Experienced
source-git-commit: 453da51a42984b912547570f2e1de70806b41171
workflow-type: tm+mt
source-wordcount: '1661'
ht-degree: 0%

---

# Upgrade uitvoeren van Adobe Experience Manager Guides voor versie 4.6.0 en hoger

Dit artikel bevat instructies voor het upgraden van uw Experience Manager Guides-versies voor 4.6.0 en hoger.

>[!NOTE]
>
> Volg de upgrade-instructies voor de versie met licentie van uw product.

U kunt uw huidige versie van Experience Manager Guides upgraden naar versie 5.1.0 Service Pack 3:

- Als u versie 5.1.0 of 5.1.x gebruikt, kunt u rechtstreeks upgraden naar versie 5.1.0 Service Pack 3.
- Als u versie 4.6.0, 4.6.x, 5.0.0, of 5.0.x gebruikt, dan moet u aan versie 5.1.0 bevorderen.
- Als u op een versie voorafgaand aan 4.6.0 bent, verwijs naar [ Verbetering Adobe Experience Manager Guides voor versie 4.4.0 en vroeger ](./upgrade-aemg-prev-versions.md) voor gedetailleerde verbeteringsinstructies.

>[!NOTE]
>
> U moet AEM Service Pack installeren voordat u de Experience Manager Guides-versie kunt upgraden.

Raadpleeg de volgende procedures voor meer informatie:

- [Upgrade naar versie 5.1.0](#upgrade-to-version-510)
- [Upgrade naar versie 5.0.0](#upgrade-to-version-500)
- [Upgrade naar versie 4.6.0](#upgrade-to-version-460)

>[!IMPORTANT]
>
> Voordat u begint met een upgrade, moet u een volledige back-up van het systeem maken om gegevensverlies te voorkomen.


## Upgrade naar versie 5.1.0


>[!IMPORTANT]
>
> Als u momenteel op AEM 6.5 werkt en van plan bent over te stappen op AEM 6.5 LTS, dient u eerst de AEM-upgrade te voltooien voordat u verdergaat met de Experience Manager Guides 5.1.0-upgrade. Voor details, mening [ Bevorderend aan Adobe Experience Manager (AEM) 6.5 LTS ](https://experienceleague.adobe.com/en/docs/experience-manager-65-lts/content/implementing/deploying/upgrading/upgrade).

**Eerste vereisten**

>[!NOTE]
>
>Als u aan 5.1.0 Service Pack 3 bevordert, dan moet u op versie 5.1.0 of 5.1.x van Experience Manager Guides zijn. Het verbeteringsproces voor 5.1.0 Service Pack 3 versie volgt de zelfde stappen zoals de 5.1.0 versie.

Voordat u het Experience Manager Guides 5.1.0-upgradeproces start, moet u controleren of:

1. Bijgewerkt naar Experience Manager Guides versie 4.6.3, 4.6.4, 5.0.0 of 5.0.0 Service Pack 1.
1. (Optioneel) Alle vertaaltaken zijn afgesloten.
1. Veranderde het logboekniveau in **INFO** voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` klasse en voeg deze logboeken in een nieuw logboekdossier toe, bijvoorbeeld, `logs/translation_upgrade.log`.

>[!NOTE]
>
> De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

**installeer versie 5.1.0**

Download het 5.1.0 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) en volg de instructies die in [ het werkschema van de Installatie en van de post-installatiedesverbetering ](#installation-and-post-installation-upgrade-workflow) worden verstrekt om het verbeteringsproces te voltooien.


## Upgrade naar versie 5.0.0

>[!TIP]
>
> De bevordering aan versie 5.0.0 Service Pack 3 hangt van de huidige versie van Experience Manager Guides af. Als u versie 5.0.0 Service Pack 2, 5.0.0 Service Pack 1 of 5.0.0 gebruikt, dan kunt u aan versie 5.0.0 Service Pack 3 direct bevorderen. De upgradestappen zijn gelijk aan die voor versie 5.0.0.

>[!NOTE]
>
> De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

**Eerste vereisten**

Voordat u het Experience Manager Guides 5.0.0-upgradeproces start, moet u controleren of:

1. Bijgewerkt naar Experience Manager Guides versie 4.6.3, 4.6.1, 4.6.0 of 4.4.
1. (Optioneel) Alle vertaaltaken zijn afgesloten.
1. Veranderde het logboekniveau in **INFO** voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` klasse en voeg deze logboeken in een nieuw logboekdossier toe, bijvoorbeeld, `logs/translation_upgrade.log`.


**installeer versie 5.0.0**

Download het 5.0.0 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) en volg de instructies die in [ het werkschema van de Installatie en van de post-installatiedesverbetering ](#installation-and-post-installation-upgrade-workflow) worden verstrekt om het verbeteringsproces te voltooien.

## Upgrade naar versie 4.6.0

>[!TIP]
>
> Het wordt aanbevolen om 4.6.0 Service Pack 4 bovenop versie 4.6.0, 4.6.0 Service Pack 1 of 4.6.0 Service Pack 3 te installeren. Het verbeteringsproces voor 4.6.0 Service Pack 4 versie volgt de zelfde stappen zoals de versie 4.6.0.

De upgrade naar versie 4.6.0 is afhankelijk van de huidige versie van Experience Manager Guides. Als u versie 4.4.0, 4.3.1, 4.3.0, 4.2 of 4.2.1 (Hotfix 4.2.1.3) gebruikt, kunt u rechtstreeks upgraden naar versie 4.6.0.

>[!NOTE]
>
> De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

**Eerste vereisten**

Voordat u het Experience Manager Guides 4.6.0-upgradeproces start, moet u controleren of:

1. Geüpgraded naar Experience Manager Guides versie 4.3.1, 4.3.0 of 4.2.1 (Hotfix 4.2.1.3).
1. (Optioneel) Alle vertaaltaken zijn afgesloten.
1. Veranderde het logboekniveau in **INFO** voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` klasse en voeg deze logboeken in een nieuw logboekdossier toe, bijvoorbeeld, `logs/translation_upgrade.log`.

**installeer versie 4.6.0**

Download het 4.6.0 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) en volg de instructies die in [ het werkschema van de Installatie en van de post-installatiedesverbetering ](#installation-and-post-installation-upgrade-workflow) worden verstrekt om het verbeteringsproces te voltooien.

## Workflow voor installatie en upgrade na installatie

### Het versiepakket installeren

Voer de volgende stappen uit om het versiepakket te installeren:

1. Installeer het versiepakket waarop u een upgrade wilt uitvoeren.
1. U kunt ervoor kiezen om op de trigger te drukken om de upgrade-taak voor de vertaalkaart te starten. Voor details, zie [ trekker van manuscript via een Servlet ](#enable-trigger-of-script-via-a-servlet) toelaten.

1. Nadat u de pakketinstallatie hebt voltooid, wacht u op het volgende bericht in de logboeken:

   `Completed the post deployment setup script`

   Het bovenstaande bericht geeft aan dat alle installatiestappen zijn voltooid.

   Als u om het even welke volgende fouten ontmoet, rapporteer hen aan uw team van het klantensucces:

   - Fout tijdens een setupscript voor implementatie na plaatsing
   - Uitzondering tijdens het exporteren van de MAP voor vertaling
   - Kan vertaalkaart van v1 naar v2 voor eigenschap niet importeren
1. (Optioneel) Upgrade de insteekmodule Zuurstofconnector die wordt vrijgegeven met de versie die u wilt upgraden naar.
1. Wis de browsercache nadat u het pakket hebt geïnstalleerd.

### Na de installatie

Nadat u Experience Manager Guides hebt geïnstalleerd, kunt u de verschillende configuraties samenvoegen die van toepassing zijn vanaf de nieuw geïnstalleerde versie tot aan uw installatie.

>[!NOTE]
>
> Het dampupdate-assetmodel kan worden aangepast. Dus als er aanpassingen zijn uitgevoerd, moeten we de aanpassingen en Experience Manager Guides synchroniseren in de werkkopie van het model.

**DAM het werkschema van de Activa van de Update \ (veranderingen \):**

1. URL openen:

   ```
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html 
   ```

1. Selecteer **DAM het werkschema van Activa van de Update**.
1. Selecteer **uitgeven**.
1. Als de **component van de Initiator van het Proces van 0} DXML {aanwezig is, zorg ervoor dat de aanpassingen worden gesynchroniseerd.**
1. Als de **component van de Initiator van het Proces van 0} DXML {ontbreekt, voer de volgende stappen uit om het op te nemen:**

   - Selecteer **component van het Tussenvoegsel** \ (Verantwoordelijk voor Experience Manager Guides post-verwerking als definitieve stap in het proces \).
   - Vorm de **stap van het Proces** met hieronder details:

     **Gemeenschappelijke tabel:**

      - **Titel:** DXML de Initiator van het Proces van het Post

      - **Beschrijving**: De stap van de initiator van het postproces DXML die een slingerbaan voor DXML post-verwerking van het gewijzigde/gecreeerde element zal teweegbrengen

     **lusje van het Proces**

      - Selecteer **DXML de Initiator van het Proces van het Post** van het **Proces** drop down
      - Selecteer **de Geavanceerde Behandeling van 0}**
      - Selecteer **Gereed**

1. Selecteer **Synchronisatie** op het hoogste recht na de voltooiing van de veranderingen. Je ontvangt een melding over succes.

   >[!NOTE]
   >
   > Vernieuw en controleer of de aangepaste wijzigingen en de naverwerkingsstap van Experience Manager Guides aanwezig zijn in het uiteindelijke workflowmodel.

1. Zodra **DAM het werkschema van de Activa van de Update** wordt bevestigd, controleer overeenkomstige lanceringsconfiguraties. Ga hiertoe naar de AEM Workflow-interface en open draagraketten.

   ```http
   http://localhost:4502/libs/cq/workflow/content/console.html
   ```

   Vind en breng veranderingen \ (indien nodig \) in de volgende twee lanceerinrichtingen \ (die actief zouden moeten zijn \) die aan **DAM het werkschema van de Activa van de Update** beantwoorden:

1. Lanceerprogramma voor &quot;*Gemaakt Knoop*&quot;voor **DAM het werkschema van de Activa van de Update** - voor voorwaarde `"jcr:content/jcr:mimeType!=video"`, zou de &quot;het Globaliseren&quot;waarde moeten zijn:

   ```json
   /content/dam(/((?!/subassets|/translation_output).)*/)renditions/original
   ```

   - &#39;excludeList&#39; moet `"event-user-data:changedByWorkflowProcess"` hebben.
   - Lanceerinrichting voor &quot;*Gewijzigde Knoop*&quot;voor **DAM het werkschema van de Activa van de Update -** voor voorwaarde &quot;`jcr:content/jcr:mimeType!=video`&quot;, zou de &quot;het Globaliseren&quot;waarde moeten zijn:

   ```json
   /content/dam(/((?!/subassets|/translation_output).)*/)renditions/original
   ```

   - `excludeList` moet `"event-user-data:changedByWorkflowProcess"` hebben.

1. Nadat de upgrade is voltooid, zorgt u ervoor dat alle aanpassingen/overlays worden gevalideerd en bijgewerkt zodat ze overeenkomen met de nieuwe toepassingscode. Hieronder volgen enkele voorbeelden:
   - Componenten die door `/libs/fmditaor/libsshould` worden overschreven, moeten met de nieuwe productcode worden vergeleken en updates moeten worden uitgevoerd in overlaybestanden onder/apps.
   - Alle `clientlib` -categorieën die in het product worden gebruikt, moeten voor wijzigingen worden gecontroleerd. Overschreven configuraties `\(examples below\)` moeten worden vergeleken met de meest recente configuraties, zodat u de nieuwste functies krijgt:
   - elementmapping.xml
   - `ui\_config.json\(may have been set in folder profiles\)`
   - modified `com.adobe.fmdita.config.ConfigManager`

1. Als u aanpassingen hebt toegevoegd in damAssetLucene, kan het nodig zijn deze opnieuw toe te passen. Nadat u deze wijzigingen hebt aangebracht, stelt u de index in op true. Hierdoor worden alle bestaande knooppunten opnieuw gecompileerd met de aanpassingen. Nadat de rendex-markering is voltooid, wordt deze weer op false ingesteld. Dit kan een paar uur duren, afhankelijk van het aantal elementen in het systeem.

### Stappen om de Experience Manager Guides-indexen opnieuw te indexeren

1. Open `crx/de` en navigeer naar het indexpad: `/oak:index/guidesAssetProperties`
2. Plaats het herindexbezit als `true` (`false` door gebrek) en klik **sparen allen**.
3. Zodra de redex volledig is, wordt de redex-eigenschap opnieuw ingesteld op `false` en wordt de redex-telling met 1 verhoogd.

   >[!NOTE]
   >
   > Dit kan een paar minuten duren, afhankelijk van de hoeveelheid gegevens die aanwezig is.
4. Voer dezelfde stappen uit voor andere toegevoegde of gewijzigde indexen: `guidesBulkActivation`, `guidesPeerLinkIndex` en `guidesKonnectTemplateIndex` .

### Stappen om de bestaande inhoud te indexeren

Voer de volgende stappen uit om de bestaande inhoud te indexeren:

- Voer een POST-aanvraag uit op de server \(met correcte verificatie\) - `http://<server:port\>/bin/guides/map-find/indexing` . (Optioneel: u kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd || Voorbeeld: `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

- De API retourneert een `jobId` . Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(bijvoorbeeld: ` http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

- Zodra de taak is voltooid, reageert het bovenstaande GET-verzoek met succes en vermeldt het of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.


>[!NOTE]
>
> Als u het douaneschema gebruikt, moet u de weg van de dossiers van douane DTD en XSD catalog.xml in de bewaarplaats van AEM in **bepalen integreer Catalogi** optie.

### Stappen voor het afhandelen van het `'fmdita rewriter'` -conflict

Experience Manager Guides heeft de module van de a [**douane die herschrijver**](../install-conf-guide/conf-output-generation.md#custom-rewriter) voor de behandeling van de verbindingen in het geval van dwars-kaarten (verbindingen tussen de onderwerpen van twee verschillende kaarten) worden geproduceerd.

Als u nog een aangepaste schrijfbewerking voor tekenreeksen in uw codebase hebt, gebruikt u een `'order'` -waarde groter dan 50, omdat Experience Manager Guides anders `'order'` 50 gebruikt.  Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer details, mening [ Output die pijplijnen herschrijft ](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Aangezien de waarde van `'order'` tijdens deze upgrade is gewijzigd van 1000 in 50, moet u eventueel de bestaande aangepaste rewriter samenvoegen met `'fmdita-rewriter'` .


### Stappen om de damAssetLucene opnieuw te indexeren

De indexdefinitie is bijgewerkt voor damAssetLucene met AEM Guides. Na bevordering aan de vereiste versie, verwijs naar [ dit artikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-16460) voor het opnieuw indexeren van damAssetLucene.

>[!NOTE]
>
> Zorg dat beide eigenschappen ( `reindex=true` en `reindex-async=true` for `/oak:index/damAssetLucene` ) tijdens het volgen van de documentatie tegelijkertijd worden bijgewerkt via de opslagbewerking.

