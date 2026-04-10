---
title: Adobe Experience Manager Guides upgraden op locatie vorige versies
description: Meer informatie over het upgraden van Adobe Experience Manager Guides
feature: Installation
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '3159'
ht-degree: 0%

---

# Upgrade uitvoeren van Adobe Experience Manager Guides op locatie (versie 4.4.0 en eerder)

Dit artikel verstrekt instructies om **versies van Adobe Experience Manager Guides** **voorafgaand aan 4.6.0** (tot en met omvat **4.4.0**) te bevorderen.

Als u op een versie **voorafgaand aan 3.8.5** bent, verwijs naar de **Verbetering Experience Manager Guides** sectie in de product-specifieke installatiegids beschikbaar op [&#x200B; Adobe Experience Manager Guides Help PDF archief &#x200B;](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).

Voor verbeteringsinstructies voor nieuwere versies, verwijs naar [&#x200B; Verbetering Adobe Experience Manager Guides voor versie 4.6.0 en hierboven &#x200B;](./upgrade-aemg-latest-version.md).

## Voordat u begint

>[!NOTE]
>
> U moet instructies bijwerken die specifiek zijn voor de versie met licentie van uw product en u moet het servicepakket voor AEM installeren voordat u de Experience Manager Guides-versie kunt upgraden.

>[!IMPORTANT]
>
> Alvorens u begint te bevorderen, neem a **volledige systeemsteun** om het even welk verlies van gegevens te vermijden.

## Paden upgraden die in dit artikel worden behandeld

Dit artikel omvat procedures voor:

- [Upgrade naar versie 4.4.0](#upgrade-to-version-440)
- [Upgrade naar versie 4.3.1.5](#upgrade-to-version-4315)
- [Upgrade naar versie 4.3.1](#upgrade-to-version-431)
- [Upgrade naar versie 4.3.0](#upgrade-to-version-430)
- [Upgrade naar versie 4.2.1](#upgrade-to-version-421)
- [Upgrade naar versie 4.2](#upgrade-to-version-42)
- [Upgrade van 3.8.5 naar versie 4.0](#upgrade-from-version-385-to-version-40)


## Algemene voorwaarden (geldt voor alle upgrades, tenzij een procedure anders bepaalt)

Voer de volgende taken uit voordat u het upgradeproces uitvoert:

1. Opmerkingen bij revisies importeren in onderwerpen die zijn geopend voor revisie.
2. Sluit alle actieve revisies.
3. Sluit alle vertaaltaken.
4. Verwijder alle Experience Manager Guides-hotfixes die boven op de vorige versie (hoofdversie of patchrelease) zijn geïnstalleerd.

Voor sommige upgrades moet het logniveau ook worden ingesteld op `INFO` voor een vertaalupgradeklasse en moet worden aangemeld bij een afzonderlijk bestand. Deze vereisten worden in de desbetreffende upgradeprocedure(s) vermeld.

## Upgrade van versie 3.8.5 naar versie 4.0

>[!NOTE]
>
> Dit verbeteringsproces is van toepassing **slechts** van **3.8.5** aan **4.0**. Voor verbeteringen van **3.4 of hoger** aan **3.8.5**, verwijs naar de product-specifieke installatiegids beschikbaar op [&#x200B; Adobe Experience Manager Guides Help PDF archiveren &#x200B;](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).

Als u versie van Experience Manager Guides **3.8.5** gebruikt, kunt u aan versie **4.0** bevorderen zonder de vorige versie te desinstalleren.

### Voordat u versie 4.0 installeert

1. Verzeker Experience Manager Guides op versie **3.8.5** is.
2. Download het pakket met het upgradescript: zoek naar **&quot;XML Documentation-oplossing 4.0 Upgradepakket&quot;** op de Adobe Software Distribution Portal (downloadt een `.zip` ).
3. Upload het pakket aan AEM via **Manager van het Pakket** en installeer het.
4. Nadat het upgradepakket is geïnstalleerd, voert u de scripts in de hieronder beschreven volgorde uit.

**de verbeteringsverenigbaarheid van de Controle API**

Deze API is ontworpen om de huidige systeemstatus te beoordelen en te rapporteren of de upgrade mogelijk is of niet. Als u dit script wilt uitvoeren, activeert u het onderstaande eindpunt:

| Eindpunt | /bin/dxml/upgrade/3xto4x/report |
| --- | --- |
| Type aanvraag | **GET** <br> **Nota**: U kunt Webbrowser gebruiken, waar u aan de instantie van AEM als beheerder het programma wordt geopend. |
| Verwachte reactie | -   Als alle vereiste knooppunten kunnen worden verplaatst, wordt een controle geslaagd weergegeven. <br>-   Als er een knooppunt aanwezig is op de doellocatie, wordt er een relevante fout gegenereerd. Maak de opslagplaats \(verwijder knoop /var/dxml\) schoon en installeer het verbeteringspakket opnieuw en breng dan dit eindpunt opnieuw teweeg. <br>**Nota:** dit is geen gemeenschappelijke fout aangezien de doelplaats niet vroeger door 3.x Experience Manager Guides wordt gebruikt. <br> -   Als dit manuscript niet slaagt, ga niet te werk en rapporteer aan uw team van het klantensucces. |

**API van de de gegevensmigratie van het Systeem**

Dit API wordt ontworpen om de systeemgegevens zoals die in de **Verwijzing van de Migratie** sectie worden vermeld te migreren.

1. Voer dit script niet uit als de API voor compatibiliteit van upgrades controleren \(ga niet door\) mislukt.
1. Zodra de API voor upgradeconformiteit controleren succesvol is, kunt u het upgradescript uitvoeren.

| Eindpunt | /bin/dxml/upgrade/3xto4x |
| --- | --- |
| Type aanvraag | **POST** <br>**Nota**: Dit manuscript is een POST- verzoek vandaar zou via agenten zoals Postman moeten worden uitgevoerd. |
| Verwachte reactie | -   Zodra de migratie succesvol is, kunt u XML Documentation oplossing versie 4.0 installeren.<br> -   Als er fouten zijn, herstel aan het laatste controlepunt en deel de foutenlogboeken samen met API output met uw team van de klantensucces. |


**Migratietoewijzing**

Deze API migreert alle gegevens onder de bronplaats aan de doelplaats.

| Source | Target |
|------|------|
| /content/fmdita | /var/dxml |
| /content/dxml | /var/dxml |
| /etc/fmdita | /libs/fmdita |

### Versie 4.0 installeren

1. Installeer versie 4.0 slechts als de verbeteringsstappen succesvol waren.
1. Download 4.0 versiepakket van [&#x200B; het Portaal van de Distributie van de Software van Adobe &#x200B;](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html):

   - Als u de UUID-versie van software gebruikt, zoekt u naar &quot;4.0 UUID Release for XML Documentation solution for AEM 6.5&quot;.
   - Als u niet-UUID versie van software gebruikt, zoek naar &quot;4.0 Non-UUID Release for XML Documentation oplossing for AEM 6.5&quot;.
Upload het pakket naar de bestaande AEM-serverinstantie\(s\) met CRX Package Manager en installeer het.

     >[!NOTE]
     >
     > Wacht tot alle systeemcomponenten zijn gestart.

1. Wis de browsercache nadat u het pakket hebt geïnstalleerd.
1. Voer de volgende stappen uit als een verzender is geconfigureerd voor de AEM Author-instantie:
   - Zorg ervoor dat het volgende wordt verwerkt in verzendersregels:
   - Het URL-patroon/home/users/\*/preferences is whitelisted.
   - Het URL-patroon /libs/cq/security/userinfo.json wordt niet in de cache opgeslagen.
1. Cache van verzender wissen \(om `clientlibs` caching\) te wissen.

## Upgrade naar versie 4.2

U kunt aan versie **4.2** direct bevorderen als u versie **4.0**, **4.1**, of **4.1.x** gebruikt.

### Voordat u versie 4.2 installeert

Voordat u het Experience Manager Guides 4.2-upgradeproces start, moet u controleren of:

1. Geüpgraded aan Experience Manager Guides **4.0**, **4.1**, of **4.1.x**.
2. Alle vertaaltaken zijn afgesloten.
3. Stel het logniveau in op `INFO` voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` en meld u aan bij een nieuw logbestand (bijvoorbeeld `logs/translation_upgrade.log` ).

   >[!NOTE]
   > 
   > Sluit alle actieve revisies. Als revisies niet worden gesloten tijdens de upgrade naar 4.2, kunnen oudere revisietaken in uitvoering oudere revisiepagina&#39;s blijven openen. Nieuwe revisietaken die na de upgrade worden gemaakt, geven de meest recente functionaliteitsupdates weer.

### Versie 4.2 installeren

1. Download het **4.2** pakket van [&#x200B; het Portaal van de Distributie van de Software van Adobe &#x200B;](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
2. Installeer het 4.2-pakket.
3. Wacht na de installatie op het volgende bericht in de logboeken:

   `Completed the post deployment setup script`

   Het bovenstaande bericht geeft aan dat alle installatiestappen zijn voltooid.

   Als u een van de volgende fouten tegenkomt, rapporteert u deze aan Klantsucces:

   - `Error in post deployment setup script`
   - `Exception while porting the translation MAP`
   - `Unable to port translation map from v1 to v2 for property`

4. (Optioneel) Upgrade de insteekmodule Zuurstofconnector die wordt losgelaten met versie 4.2.
5. Wis de browsercache nadat u het pakket hebt geïnstalleerd.
6. U kunt de aanpassingen blijven bijwerken zoals in de volgende sectie wordt beschreven.

### Na installatie van versie 4.2

>[!IMPORTANT]
>
> Hi-tech-sjabloon wordt niet weergegeven op een geüpgrade server. Als u de hi-tech sjabloon op uw server wilt opnemen, kunt u deze kopiëren: Source: `/libs/fmdita/pdf/Hi-Tech` Doel: `/content/dam/dita-templates/pdf` .

Dan ga met de gedeelde post-verbeteringstaken in [&#x200B; Gemeenschappelijke post verbeteringstaken (alle versies) &#x200B;](#common-postupgrade-tasks-all-versions) te werk.

## Upgrade naar versie 4.2.1

>[!TIP]
>
> Het wordt geadviseerd om **Hotfix4.2.1.3** bovenop versie **4.2.1** te installeren.

U kunt aan versie **4.2.1** direct bevorderen als u **4.1**, **4.1.x**, of **4.2** gebruikt.

>[!NOTE]
>
> De nabewerking en indexering kunnen enkele uren in beslag nemen. Start de upgrade tijdens een periode buiten de piekuren.

### Voordat u versie 4.2.1 installeert

1. Bevorder aan Experience Manager Guides **4.1**, **4.1.x**, of **4.2**.
2. Sluit alle vertaaltaken.
3. Stel het logniveau in op `INFO` voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` en meld u aan bij een nieuw bestand (bijvoorbeeld `logs/translation_upgrade.log` ).

>[!NOTE]
>
> Sluit alle actieve revisies (hetzelfde gedrag als in 4.2).

### Versie 4.2.1 installeren

1. Download het **4.2.1** pakket van [&#x200B; het Portaal van de Distributie van de Software van Adobe &#x200B;](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
2. Installeer het 4.2.1-pakket.
3. U kunt de upgradetaak van de vertaalkaart optioneel activeren. Voor details, zie [&#x200B; trekker van manuscript via een Servlet &#x200B;](#enable-trigger-of-script-via-a-servlet) toelaten.

4. Wacht na de installatie op: `Completed the post deployment setup script` in logbestanden.

   Deze fouten rapporteren aan Klantsucces:

   - `Error in post deployment setup script`
   - `Exception while porting the translation MAP`
   - `Unable to port translation map from v1 to v2 for property`
5. (Facultatief) de schakelaarstop van de Verbetering Zuurstof die met versie **4.2** wordt vrijgegeven
6. Cache van browser wissen.
7. Ga met [&#x200B; Gemeenschappelijke post verbeteringstaken (alle versies) &#x200B;](#common-postupgrade-tasks-all-versions) voort.

### Na installatie van versie 4.2.1

>[!IMPORTANT]
>
> Hi-tech-sjabloon wordt niet weergegeven op een geüpgrade server. Als u de hi-tech sjabloon op uw server wilt opnemen, kunt u deze kopiëren: Source: `/libs/fmdita/pdf/Hi-Tech` Doel: `/content/dam/dita-templates/pdf` .

Ga met [&#x200B; Gemeenschappelijke post verbeteringstaken (alle versies) &#x200B;](#common-postupgrade-tasks-all-versions) en (indien vereist) [&#x200B; Index bestaande inhoud voor kaart vinden en vervangen &#x200B;](#index-existing-content-for-map-find-and-replace) te werk.


## Upgrade naar versie 4.3.0

De upgrade naar versie 4.3.0 is afhankelijk van de huidige versie van Experience Manager Guides. Als u versie 4.2 of 4.2.x gebruikt, kunt u rechtstreeks upgraden naar versie 4.3.0.

>[!NOTE]
>
>De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

### Voordat u versie 4.3.0 installeert

Voordat u het Experience Manager Guides 4.3.0-upgradeproces start, moet u controleren of:

1. Geüpgraded naar Experience Manager Guides versie 4.2 of 4.2.x en hun respectieve installatiestappen voltooid.
1. Alle vertaaltaken zijn afgesloten.

### Versie 4.3.0 installeren

1. Download 4.3.0 versiepakket van [&#x200B; het Portaal van de Distributie van de Software van Adobe &#x200B;](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installeer versie 4.3.0.
1. Wis de browsercache nadat u het pakket hebt geïnstalleerd.
1. Bevorder het `ui_config.json` dossier van het **lusje van de Configuratie van de Redacteur van XML** in het Profiel van de Omslag.

### Na installatie van versie 4.3.0

Doorgaan met:

- [&#x200B; Gemeenschappelijke post verbeteringstaken (alle versies) &#x200B;](#common-postupgrade-tasks-all-versions)
- Indien van toepassing: [&#x200B; post bestaande inhoud voor gebroken verbindingsrapport &#x200B;](#post-process-existing-content-for-broken-link-report)

## Upgrade naar versie 4.3.1

De upgrade naar versie 4.3.1 is afhankelijk van de huidige versie van Experience Manager Guides. Als u versie 4.3.0, 4.2 of 4.2.1 gebruikt, kunt u rechtstreeks upgraden naar versie 4.3.1.

>[!NOTE]
>
>De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

### Voordat u versie 4.3.1 installeert

Voordat u het Experience Manager Guides 4.3.1-upgradeproces start, moet u controleren of:

1. Geüpgraded naar Experience Manager Guides versie 4.3.0, 4.2 of 4.2.1 en hun respectieve installatiestappen voltooid.
1. (Optioneel) Alle vertaaltaken zijn afgesloten.
1. Veranderde het logboekniveau in **INFO** voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` klasse en voeg deze logboeken in een nieuw logboekdossier toe, bijvoorbeeld, `logs/translation_upgrade.log`.

### Versie 4.3.1 installeren

1. Download 4.3.1 versiepakket van [&#x200B; het Portaal van de Distributie van de Software van Adobe &#x200B;](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installeer versie 4.3.1.
1. U kunt de upgradetaak van de vertaalkaart optioneel activeren. Voor details, zie [&#x200B; trekker van manuscript via een Servlet &#x200B;](#enable-trigger-of-script-via-a-servlet) toelaten.
1. Wacht na de installatie op: `Completed the post deployment setup script` in logbestanden.
Deze fouten rapporteren aan Klantsucces:\
   `Error in post deployment setup script`, `Exception while porting the translation MAP`, `Unable to port translation map from v1 to v2 for property`
1. (Facultatief) de schakelaarstop van de Verbetering Zuurstof die met versie **4.2** wordt vrijgegeven.
1. Cache van browser wissen.

### Na installatie van versie 4.3.1

Doorgaan met:

- [&#x200B; Gemeenschappelijke post verbeteringstaken (alle versies) &#x200B;](#common-postupgrade-tasks-all-versions)
- Indien van toepassing: [&#x200B; Index bestaande inhoud voor kaart vinden en vervangen &#x200B;](#index-existing-content-for-map-find-and-replace)
- Indien van toepassing: [&#x200B; post bestaande inhoud voor gebroken verbindingsrapport &#x200B;](#post-process-existing-content-for-broken-link-report)


## Upgrade naar versie 4.3.1.5

U kunt aan **4.3.1.5** direct bevorderen als u versie **4.3.1** gebruikt.

### Versie installeren 4.3.1.5

1. Download het **4.3.1.5** pakket van [&#x200B; het Portaal van de Distributie van de Software van Adobe &#x200B;](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
2. Installeer het pakket 4.3.1.5 .
3. Wacht tot het installatieproces is voltooid.
4. De aanpassingen blijven bijwerken zoals in de volgende sectie wordt beschreven.

## Na installatie van versie 4.3.1.5

>[!NOTE]
>
>Als u de bundel org.apache.velocity wilt gebruiken, voert u de volgende stappen uit voordat u de bundel uploadt:
> 1. Ga naar `<server>:<port>/system/console/bundles`
> 1. Zoeken naar org.apache.velocity.
> 1. Verwijder de gezochte bundel.
> 1. Installeer de vereiste snelheidsbundel.

1. Nadat de upgrade is voltooid, zorgt u ervoor dat alle aanpassingen/overlays worden gevalideerd en bijgewerkt zodat ze overeenkomen met de nieuwe toepassingscode. Hieronder volgen enkele voorbeelden:
   - Componenten die worden overschreven door `/libs/fmdita` of ` /libs` , moeten met de nieuwe productcode worden vergeleken en updates moeten worden uitgevoerd in overlaybestanden onder `/apps` .
   - Alle clientlibcategorieën die worden gebruikt van het product, dienen te worden gecontroleerd op wijzigingen. Overschreven configuraties \(voorbeelden verderop\) moeten worden vergeleken met de nieuwste configuraties om de nieuwste functies te krijgen:
   - `elementmapping.xml`
   - `ui\_config.json\` (kan zijn ingesteld in mapprofielen\)
   - modified `com.adobe.fmdita.config.ConfigManager`


## Upgrade naar versie 4.4.0

U kunt aan **4.4.0** direct bevorderen als u gebruikt: **4.3.1**, **4.3.0**, **4.2**, of **4.2.1 (Hotfix 4.2.1.3)**.

>[!NOTE]
>
>De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

### Voordat u versie 4.4.0 installeert

Voordat u het Experience Manager Guides 4.4.0-upgradeproces start, moet u controleren of:

1. Geüpgraded naar Experience Manager Guides versie 4.3.1, 4.3.0 of 4.2.1 (Hotfix 4.2.1.3) en de desbetreffende installatiestappen voltooid.
1. (Optioneel) Alle vertaaltaken zijn afgesloten.
1. Veranderde het logboekniveau in **INFO** voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` klasse en voeg deze logboeken in een nieuw logboekdossier toe, bijvoorbeeld, `logs/translation_upgrade.log`.

### Versie 4.4.0 installeren

1. Download 4.4.0 versiepakket van [&#x200B; het Portaal van de Distributie van de Software van Adobe &#x200B;](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
2. Installeer het 4.4.0-pakket.
3. U kunt de upgradetaak van de vertaalkaart optioneel activeren. Voor details, zie [&#x200B; trekker van manuscript via een Servlet &#x200B;](#enable-trigger-of-script-via-a-servlet) toelaten.
4. Nadat u de pakketinstallatie hebt voltooid, wacht u op het volgende bericht in de logboeken:

   `Completed the post deployment setup script`

   Het bovenstaande bericht geeft aan dat alle installatiestappen zijn voltooid.

   Als u om het even welke volgende prefix van de FOUT ontmoet, rapporteer hen aan uw team van het klantensucces:

   - `Error in post deployment setup script`
   - `Exception while porting the translation MAP`
   - `Unable to port translation map from v1 to v2 for property`
5. (Facultatief) de schakelaarstop van de Verbetering Zuurstof die met versie **4.4.0** wordt vrijgegeven.
6. Cache van browser wissen.
7. Doorgaan met:

   - [Algemene taken na de upgrade (alle versies)](#common-ppostupgrade-tasks-all-versions)
   - [&#x200B; Index bestaande inhoud voor kaart vindt en vervangt &#x200B;](#index-existing-content-for-map-find-and-replace) (slechts indien van toepassing)
   - [&#x200B; post-proces bestaande inhoud voor gebroken verbindingsrapport &#x200B;](#post-process-existing-content-for-broken-link-report) (slechts indien van toepassing)
   - [&#x200B; Verbetering van de Omzettingskaart (servlet trekker) &#x200B;](#translation-map-upgrade-servlet-trigger) (slechts als toepasselijk)


## Algemene taken na de upgrade (alle versies)

Nadat u Experience Manager Guides hebt geïnstalleerd, moet u mogelijk configuraties samenvoegen die van toepassing zijn vanaf de nieuw geïnstalleerde versie tot aan uw installatie.

>[!NOTE]
>
> Het **DAM de werkschemamodel van de Activa van de Update** kan worden aangepast. Als u aanpassingen hebt, synchroniseert u deze met Experience Manager Guides-wijzigingen in de werkkopie van het model.

### Workflow voor DAM-update-elementen valideren (wijzigingen na verwerking)

1. Open de gebruikersinterface voor AEM Workflow Models (voorbeeld weergegeven in de bron):\
   `http://<host>:4502/libs/cq/workflow/admin/console/content/models.html`
2. Selecteer **DAM het werkschema van Activa van de Update**.
3. Selecteer **uitgeven**.
4. Als de **component van de Initiator van het Proces van 0&rbrace; DXML &lbrace;aanwezig is, zorg aanpassingen ervoor worden gesynchroniseerd.**
5. Als de component afwezig is, neem het op:
   1. Klik **component van het Tussenvoegsel** (verantwoordelijk voor Gidsen na verwerking als definitieve stap).
   2. Vorm de **stap van het Proces**:
      **Gemeenschappelijke lusje**
- Titel: `DXML Post Process Initiator`
- Beschrijving: `DXML post process initiator step which will trigger a sling job for DXML post-processing of the modified/created asset`
      **lusje van het Proces**
- Proces: selecteren `DXML Post Process Initiator`
- Selecteren `Handler Advance`
- Selecteren `Done`
   3. Klik **Synchronisatie** op het hoogste recht na de voltooiing van de veranderingen. Je ontvangt een melding over succes.

>[!NOTE]
>
> Vernieuw en controleer of de aangepaste wijzigingen en de naverwerkingsstap van Experience Manager Guides aanwezig zijn in het uiteindelijke workflowmodel.

### Startconfiguraties valideren

1. Ga naar de interface van het Werkschema van AEM en open **Lanceertoestellen**.

```http
    http://localhost:4502/libs/cq/workflow/content/console.html
```

1. Vind en breng veranderingen \ (indien nodig \) in de volgende twee lanceerinrichtingen \ (die actief zouden moeten zijn \) die aan **DAM het werkschema van de Activa van de Update** beantwoorden:

1. Lanceerprogramma voor &quot;*Gemaakt Knoop*&quot;voor **DAM het werkschema van de Activa van de Update** - voor voorwaarde `"jcr:content/jcr:mimeType!=video"`, zou de &quot;het Globaliseren&quot;waarde moeten zijn:

   ```json
   /content/dam(/((?!/subassets|/translation_output).)*/)renditions/original
   ```

   - `excludeList` moet `"event-user-data:changedByWorkflowProcess"` hebben.
   - Lanceerprogramma voor *Gewijzigde Knoop* voor **DAM het werkschema van de Activa van de Update -** voor voorwaarde &quot;`jcr:content/jcr:mimeType!=video`&quot;, zou de &quot;het Globaliseren&quot;waarde moeten zijn:

   ```json
   /content/dam(/((?!/subassets|/translation_output).)*/)renditions/original
   ```

   - `excludeList` moet `"event-user-data:changedByWorkflowProcess"` hebben.

### Bedekkingen en aanpassingen valideren

Nadat de upgrade is voltooid:

1. Nadat de upgrade is voltooid, zorgt u ervoor dat alle aanpassingen/overlays worden gevalideerd en bijgewerkt zodat ze overeenkomen met de nieuwe toepassingscode. Hieronder volgen enkele voorbeelden:
   - Alle componenten die worden overschreven door/libs/fmditor/libsc, moeten worden vergeleken met de nieuwe productcode en updates moeten worden uitgevoerd in overlay bestanden onder/apps.
   - Alle clientlibcategorieën die worden gebruikt van het product, dienen te worden gecontroleerd op wijzigingen. Overschreven configuraties \(voorbeelden verderop\) moeten worden vergeleken met de nieuwste configuraties om de nieuwste functies te krijgen:
   - elementmapping.xml
   - ui\_config.json\(kan zijn ingesteld in mapprofielen\)
   - modified `com.adobe.fmdita.config.ConfigManager`

1. Als u aanpassingen hebt toegevoegd in damAssetLucene, kan het nodig zijn deze opnieuw toe te passen. Nadat u deze wijzigingen hebt aangebracht, stelt u de index in op true. Hierdoor worden alle bestaande knooppunten opnieuw gecompileerd met de aanpassingen. Nadat de rendex-markering is voltooid, wordt deze weer op false ingesteld. Dit kan een paar uur duren, afhankelijk van het aantal elementen in het systeem.

## Bestaande inhoud voor zoeken en vervangen van toewijzing indexeren

Deze sectie consolideert de herhaalde **indexerende** procedure die wordt gebruikt om nieuwe **kaart-niveau toe te laten vindt en vervangt** mogelijkheden.

**wanneer u het indexeren** kunt overslaan

De bron bevat &#39;skip&#39;-notities, afhankelijk van het upgradepad (bijvoorbeeld &#39;U hoeft deze stappen niet uit te voeren als u een upgrade uitvoert van 4.3.0 of 4.3.1&#39; en vergelijkbare notities). Volg de slaat nota in uw verbeteringssectie wordt vermeld over.

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe tekst zoeken en vervangen op kaartniveau te gebruiken:

1. Een POST-aanvraag (met verificatie) uitvoeren:

```http
POST http://<server:port>/bin/guides/map-find/indexing
```

Optionele parameters die in de bron worden ondersteund:

- Specifieke kaartpaden indexeren (standaardinstellingen voor het indexeren van alle toewijzingen):

  ```http
  POST http://<server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>
  ```

- De kaarten van DITA van de index onder een wortelomslag (en zijn subfolders):

  ```http
  POST http://<server:port>/bin/guides/map-find/indexing?root=/content/dam/test
  ```

  >[!NOTE]
  >
  > Als zowel `paths` als `root` worden doorgegeven, wordt alleen `paths` beschouwd.

1. De API retourneert een `jobId` . Als je de status wilt controleren, stuur je een GET-aanvraag:

   ```http
   GET http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}
   ```

   Uitvoergedrag verwacht:

   - Als GET klaar is, reageert het met succes en wordt aangegeven of kaarten zijn mislukt.
   - Bevestig met succes geïndexeerde kaarten in serverlogboeken.

### Controleer of de indexering van damAssetLucene volledig is (indien van toepassing)

De bron merkt op dat damAssetLucene het indexeren uren afhankelijk van de gegevensgrootte uren kan vergen en u kunt bevestigen dat de bewerking is voltooid wanneer `reindex` `false` onder is:

`http://<server:port>/oak:index/damAssetLucene`

Als u aanpassingen hebt toegevoegd in `damAssetLucene` , moet u deze mogelijk opnieuw toepassen nadat de herindex is voltooid.

### Workaround for &quot;query read or traversed more than 100000 nodes&quot; (if the job failed)

Als de indexeertaak mislukt en de fout wordt weergegeven:

&quot;De query heeft meer dan 100000 knooppunten gelezen of doorlopen. Om te voorkomen dat andere taken worden beïnvloed, is de verwerking gestopt.&quot;

Probeer deze tijdelijke oplossing uit de bron:

1. Voeg in de `damAssetLucene` eikenindex een booleaanse eigenschap `indexNodeName=true` in `/oak:index/damAssetLucene/indexRules/dam:Asset` toe.
2. Voeg een nieuw knooppunt met de naam `excerpt` onder `/oak:index/damAssetLucene/indexRules/dam:Asset/properties` toe en stel de eigenschappen in zoals in de bron:
   - `name=rep:excerpt`
   - `propertyIndex=true`
   - `notNullCheckEnabled=true`
3. Wijzig de index van `damAssetLucene` door `reindex=true` in te stellen en wacht tot deze `false` wordt (kan uren duren).
4. Voer het indexeringsscript opnieuw uit (herhaal de POST en het bijhouden van taken).

## Bestaande inhoud voor verbroken-koppelingsrapport naverwerken

Deze sectie consolideert de herhaalde **post-verwerkende** procedure die wordt gebruikt om het **gebroken verbindingsrapport** toe te laten.

**wanneer u post-verwerking** kunt overslaan

De bron bevat &#39;skip&#39;-notities, afhankelijk van het upgradepad (u hoeft deze stappen bijvoorbeeld niet uit te voeren als u een upgrade uitvoert van 4.3.0 of 4.3.0 of 4.3.1). Volg de slaat nota in uw verbeteringssectie wordt vermeld over.

Voer de volgende stappen uit om het gebroken verbindingsrapport toe te laten:

1. (Optioneel) Meer Oak queryLimitLezen voor grote opslagruimten

   Als er meer dan **100.000 DITA- dossiers** zijn, werk `queryLimitReads` onder `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` aan een waarde groter dan het aantal activa (voorbeeld: `200000`) bij, herstelt, en gaat te werk.

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|---|---|
   | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitReads | Waarde: 200000 <br> Standaardwaarde: 100000 |

1. Voer de volgende API&#39;s uit om naverwerking uit te voeren op alle bestanden:

   | Eindpunt | /bin/guides/reports/upgrade |
   |---|---|
   | Type aanvraag | **POST** Dit manuscript is een POST- verzoek vandaar zou via agenten zoals Postman moeten worden uitgevoerd. |
   | Verwachte reactie | De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden.<br> Voorbeeld-URL: `http://<server:port>/bin/guides/reports/upgrade` |

   | Eindpunt | /bin/guides/reports/upgrade |
   |---|---|
   | Type aanvraag | **GET** |
   | Param | jobId: geef de taak-id door die is ontvangen van de vorige postaanvraag. |
   | Verwachte reactie | - Zodra de taak is voltooid, reageert de GET-aanvraag met succes. <br> - Als er fouten zijn, deelt u de foutlogboeken samen met de API-uitvoer met het succesteam van de klant.  <br> Voorbeeld-URL: `http://<server:port>/bin/guides/reports/upgrade?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678` |

1. Terugkeren naar de standaardwaarde of vorige bestaande waarde van `queryLimitReads` als u deze hebt gewijzigd in stap 1.

## Triggerscript activeren via een Servlet

Verschillende versies bevatten een optionele stap voor het activeren van een upgradetaak voor een vertaalkaart via een servlet. In deze paragraaf wordt die herhaalde procedure geconsolideerd en worden alle gegevens uit de bron opgenomen.


>[!NOTE]
>
> U hoeft deze stappen niet uit te voeren als u een upgrade uitvoert van 4.3.0 of 4.3.1.

POST:

```
http://localhost:4503/bin/guides/script/start?jobType=translation-map-upgrade
```

Reactie:

```
{
"msg": "Job is successfully submitted and lock node is created for future reference",
"lockNodePath": "/var/dxml/executor-locks/translation-map-upgrade/1683190032886",
"status": "SCHEDULED"
}
```

In het bovenstaande antwoord JSON bevat de sleutel `lockNodePath` het pad naar het knooppunt dat is gemaakt in de opslagplaats dat wijst naar de verzonden taak. Het wordt automatisch verwijderd als de taak is voltooid. Tot dan kunt u naar dit knooppunt verwijzen voor de huidige status van de taak.

Zoek `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Completed porting of translation map from V1 to V2` en `com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Completed the thread to upgrade translation map from V1 to V2` voordat u verdergaat met de volgende stappen.

>[!NOTE]
>
> Controleer of het knooppunt nog aanwezig is en wat de status van de taak is.

**GET**: `http://<aem_domain>/var/dxml/executor-locks/translation-map-upgrade/1683190032886.json`


### Stappen om het fmdita rewriter-conflict te verwerken

Experience Manager Guides omvat een aangepaste Sling rewriter module (`fmditarewriter`) voor het behandelen van verbindingen die voor dwars-kaart het verbinden worden geproduceerd.

Als je nog een aangepaste herschrijver voor verkopers in je codebase hebt:

- Gebruik een `order` waarde **groter dan 50** omdat de gidsen `order=50` gebruiken.
- Tijdens deze upgrade verandert de waarde van `order` van `1000` in `50` , dus moet u de bestaande aangepaste rewriter (indien aanwezig) samenvoegen met `fmditarewriter` .

