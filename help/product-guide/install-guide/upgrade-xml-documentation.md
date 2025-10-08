---
title: Upgrade uitvoeren voor Adobe Experience Manager Guides
description: Meer informatie over het upgraden van Adobe Experience Manager Guides
exl-id: f058b39f-7408-4874-942b-693e133886cf
feature: Installation
role: Admin
level: Experienced
source-git-commit: bece5e257370f458de8878814da290086eea344e
workflow-type: tm+mt
source-wordcount: '9124'
ht-degree: 0%

---

# Upgrade uitvoeren voor Adobe Experience Manager Guides {#id224MBE0M0XA}

>[!NOTE]
>
> Volg de upgrade-instructies voor de versie met licentie van uw product.

U kunt uw huidige versie van Experience Manager Guides upgraden naar versie 5.1.0:

- Als u versie 4.6.3, 4.6.4, 5.0.0, 5.0.0 Service Pack 1, of 5.0.0 Service Pack 2 gebruikt, dan kunt u aan versie 5.1.0 direct bevorderen.
- Als u versie 4.6.0 en 4.6.1 gebruikt, moet u een upgrade naar versie 4.6.3 of 4.6.4 of 5.0.0 uitvoeren voordat u een upgrade naar versie 5.1.0 uitvoert.
- Als u versie 4.3.x, 4.2, 4.2.1 (Hotfix 4.2.1.3), 4.1 of 4.1.x gebruikt, moet u een upgrade naar versie 4.4 uitvoeren voordat u een upgrade naar versie 5.0.0 uitvoert.
- Als u versie 4.0 gebruikt, moet u een upgrade naar versie 4.2 uitvoeren voordat u een upgrade naar versie 4.3.x uitvoert.
- Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
- Als u op een versie voorafgaand aan 3.8.5 bent, verwijs naar de sectie van Experience Manager Guides van de Verbetering in de product-specifieke installatiegids beschikbaar op [ Adobe Experience Manager Guides Help het archief van PDF ](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).


>[!NOTE]
>
> U moet AEM Service Pack installeren voordat u de Experience Manager Guides-versie kunt upgraden.

Raadpleeg de volgende procedures voor meer informatie:

- [Upgrade van 3.8.5 naar versie 4.0](#upgrade-from-version-385-to-version-40)
- [Upgrade naar versie 4.2](#upgrade-to-version-42)
- [Upgrade naar versie 4.2.1](#upgrade-to-version-421)
- [Upgrade naar versie 4.3.0](#upgrade-to-version-430)
- [Upgrade naar versie 4.3.1](#upgrade-to-version-431)
- [Upgrade naar versie 4.3.1.5](#upgrade-to-version-4315)
- [Upgrade naar versie 4.4.0](#upgrade-to-version-440)
- [Upgrade naar versie 4.6.0](#upgrade-to-version-460)
- [Upgrade naar versie 5.0.0](#upgrade-to-version-500)
- [Upgrade naar versie 5.1.0](#upgrade-to-version-510)



>[!IMPORTANT]
>
> Voordat u begint met een upgrade, moet u een volledige back-up van het systeem maken om gegevensverlies te voorkomen.

## Upgrade van versie 3.8.5 naar versie 4.0

Als u Experience Manager Guides versie 3.8.5 gebruikt, kunt u een upgrade uitvoeren naar versie 4.0 van Experience Manager Guides. Met de upgradefunctie hoeft u de vorige versie van Experience Manager Guides niet te verwijderen.

Voordat u het proces uitvoert, moet u bepaalde taken uitvoeren. De volgende subsecties zullen u door de eerste vereisten, rapportgeneratie, en migratieproces lopen. Nadat u Experience Manager Guides versie 4.0 hebt geïnstalleerd, kunt u bovendien verschillende configuraties aanpassen aan de wensen van de klant.

>[!NOTE]
>
> Dit upgradeproces is alleen van toepassing van versie 3.8.5 tot versie 4.0. Voor het proces om van versie 3.4 of hoger aan 3.8.5 te bevorderen, verwijs naar de *sectie van de Verbetering Experience Manager Guides* in de product-specifieke installatiegids beschikbaar op [ Adobe Experience Manager Guides Help PDF archief ](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).



****Eerste vereisten****

Voordat u het Experience Manager Guides-upgradeproces start, moet u controleren of:

1. De revisieopmerkingen zijn geïmporteerd in onderwerpen die zijn geopend voor revisie.
1. Alle actieve revisies zijn gesloten.
1. Alle vertaaltaken zijn afgesloten.
1. Verwijder alle Experience Manager Guides-hotfixes die boven op de vorige versie \(Belangrijke versie of patchrelease\) van Experience Manager Guides zijn geïnstalleerd.

**alvorens u versie 4.0** installeert

Voer de volgende stappen uit voordat u versie 4.0 installeert:

1. Zorg ervoor dat Experience Manager Guides nu versie 3.8.5 is ingeschakeld.
1. Download het pakket met het upgradescript. Om dit te doen, onderzoek naar &quot;XML Documentation oplossing 4.0 het Pakket van de Verbetering&quot;op [ Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) die een zip dossier zal downloaden.
1. Upload dit pakket naar AEM via Package Manager en installeer dit pakket.
1. Nadat het upgradepakket is geïnstalleerd, voert u de onderstaande scripts in dezelfde volgorde uit en volgt u de gegeven instructies:

**de verbeteringsverenigbaarheid van de Controle API**

Deze API is ontworpen om de huidige systeemstatus te beoordelen en te rapporteren of de upgrade mogelijk is of niet. Als u dit script wilt uitvoeren, activeert u het onderstaande eindpunt:

| Eindpunt | /bin/dxml/upgrade/3xto4x/report |
| --- | --- |
| Type aanvraag | **GET** U kunt Webbrowser gebruiken, waar u aan de instantie van AEM als beheerder het programma wordt geopend. |
| Verwachte reactie | -   Als alle vereiste knooppunten kunnen worden verplaatst, wordt een controle geslaagd weergegeven. <br>-   Als er een knooppunt aanwezig is op de doellocatie, wordt er een relevante fout gegenereerd. Maak de opslagplaats \(verwijder knoop /var/dxml\) schoon en installeer het verbeteringspakket opnieuw en breng dan dit eindpunt opnieuw teweeg. <br>**Nota:** dit is geen gemeenschappelijke fout aangezien de doelplaats niet vroeger door 3.x Experience Manager Guides wordt gebruikt. <br> -   Als dit manuscript niet slaagt, ga niet te werk en rapporteer aan uw team van het klantensucces. |

**API van de de gegevensmigratie van het Systeem**

Dit API wordt ontworpen om de systeemgegevens zoals die in de **Verwijzing van de Migratie** sectie worden vermeld te migreren.

1. Voer dit script niet uit als de API voor compatibiliteit van upgrades controleren \(ga niet door\) mislukt.
1. Zodra de API voor upgradeconformiteit controleren succesvol is, kunt u het upgradescript uitvoeren.

| Eindpunt | /bin/dxml/upgrade/3xto4x |
| --- | --- |
| Type aanvraag | **POST** Dit manuscript is een POST- verzoek vandaar zou via agenten zoals Postman moeten worden uitgevoerd. |
| Verwachte reactie | -   Zodra de migratie succesvol is, kunt u XML Documentation oplossing versie 4.0 installeren.<br> -   Als er fouten zijn, herstel aan het laatste controlepunt en deel de foutenlogboeken samen met API output met uw team van de klantensucces. |

**Toewijzing van de Migratie**: Bovenstaande API migreert alle gegevens onder de bronplaats aan de doelplaats.

| Source | Doel |
|------|------|
| /content/fmdita | /var/dxml |
| /content/dxml | /var/dxml |
| /etc/fmdita | /libs/fmdita |

## Versie 4.0 installeren {#id23598G006XA}

1. Installeer versie 4.0 slechts als de verbeteringsstappen succesvol waren.
1. Download 4.0 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html):

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

De upgrade naar versie 4.2 is afhankelijk van de huidige versie van Experience Manager Guides.

Als u versie 4.0, 4.1 of 4.1.x gebruikt, kunt u rechtstreeks upgraden naar versie 4.2.

****Eerste vereisten****

Voordat u het Experience Manager Guides 4.2-upgradeproces start, moet u controleren of:

1. Bijgewerkt naar Experience Manager Guides versie 4.0, 4.1 of 4.1.x.
1. Alle vertaaltaken zijn afgesloten.
1. Veranderde het logboekniveau in **INFO** voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` klasse en voeg deze logboeken in een nieuw logboekdossier toe, bijvoorbeeld, `logs/translation_upgrade.log.`

>[!NOTE]
>
> Sluit alle actieve revisies. Als de revisietaken niet worden afgesloten tijdens de upgrade naar 4.2, nemen de oudere revisietaken in uitvoering voortdurend gebruikers op de oudere revisiepagina&#39;s. De revisietaken die na de upgrade worden gemaakt, geven de nieuwste updates in de functionaliteit weer.

## Versie 4.2 installeren {#id2245IK0E0EV}

1. Download 4.2 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installeer het pakket versie 4.2.
1. Nadat u de pakketinstallatie hebt voltooid, wacht u op het volgende bericht in de logbestanden:

   `Completed the post deployment setup script`

   Het bovenstaande bericht geeft aan dat alle installatiestappen zijn voltooid.

   Als u om het even welke volgende prefix van de FOUT ontmoet, rapporteer hen aan uw team van het klantensucces:

   - Fout tijdens een setupscript voor implementatie na plaatsing
   - Uitzondering tijdens het exporteren van de MAP voor vertaling
   - Kan vertaalkaart van v1 naar v2 voor eigenschap niet importeren
1. Upgrade de insteekmodule Zuurstofaansluiting die wordt vrijgegeven met versie 4.2 \(indien nodig\).
1. Wis de browsercache nadat u het pakket hebt geïnstalleerd.
1. U kunt de aanpassingen blijven bijwerken zoals in de volgende sectie wordt beschreven.

## Nadat u versie 4.2 hebt geïnstalleerd {#id2326F02004K}

>[!IMPORTANT]
>
> Hi-tech-sjabloon wordt niet weergegeven op een geüpgrade server. Als u de hi-tech sjabloon op uw server wilt opnemen, kunt u deze kopiëren: Source: /libs/fmdita/pdf/Hi-Tech Destination: /content/dam/dita-templates/pdf

Nadat u Experience Manager Guides hebt geïnstalleerd, kunt u de verschillende configuraties samenvoegen die van toepassing zijn vanaf de nieuw geïnstalleerde versie tot aan uw installatie.

>[!NOTE]
>
> Het dampupdate-assetmodel kan worden aangepast. Dus als er aanpassingen zijn uitgevoerd, moeten we de aanpassingen en Experience Manager Guides synchroniseren in de werkkopie van het model.

1. **DAM het werkschema van de Activa van de Update \ (veranderingen \):**

1. URL openen:

   ```http
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html
   ```

1. Selecteer **DAM het werkschema van Activa van de Update**.
1. Klik op **uitgeven**.
1. Als de **component van de Initiator van het Proces van 0} DXML {aanwezig is, zorg ervoor dat de aanpassingen worden gesynchroniseerd.**
1. Als de **component van de Initiator van het Proces van 0} DXML {ontbreekt, voer de volgende stappen uit om het op te nemen:**

1. Klik **component van het Tussenvoegsel** \ (Verantwoordelijk voor Experience Manager Guides post-verwerking als definitieve stap in het proces \).
1. Vorm de **stap van het Proces** met hieronder details:

   **Gemeenschappelijke lusje**

   **Titel:** DXML de Initiator van het Proces van het Post

   **Beschrijving**: De stap van de initiator van het postproces DXML die een slingerbaan voor DXML post-verwerking van het gewijzigde/gecreeerde element zal teweegbrengen

   **lusje van het Proces**

   - Selecteer **DXML de Initiator van het Proces van het Post** van het **Proces** drop down

   - Selecteer **de Geavanceerde Behandeling van 0}**

   - Selecteer **Gereed**

1. Klik **Synchronisatie** op het hoogste recht na de voltooiing van de veranderingen. Je ontvangt een melding over succes.

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
   - Lanceerprogramma voor &quot;*Gewijzigde Knoop*&quot;voor **DAM het werkschema van de Activa van de Update -** voor voorwaarde &quot;`jcr:content/jcr:mimeType!=video`&quot;,
   - De waarde &#39;Globbing&#39; moet als volgt zijn:

   ```json
   /content/dam(/((?!/subassets|/translation_output).)*/)renditions/original
   ```

   - &#39;excludeList&#39; moet `"event-user-data:changedByWorkflowProcess"` hebben.
1. Nadat de upgrade is voltooid, zorgt u ervoor dat alle aanpassingen/overlays worden gevalideerd en bijgewerkt zodat ze overeenkomen met de nieuwe toepassingscode. Hieronder volgen enkele voorbeelden:
   - Alle componenten die worden overschreven door/libs/fmditor/libsc, moeten worden vergeleken met de nieuwe productcode en updates moeten worden uitgevoerd in overlay bestanden onder/apps.
   - Alle clientlibcategorieën die worden gebruikt van het product, dienen te worden gecontroleerd op wijzigingen. Overschreven configuraties \(voorbeelden verderop\) moeten worden vergeleken met de nieuwste configuraties om de nieuwste functies te krijgen:
   - elementmapping.xml
   - ui\_config.json\(kan zijn ingesteld in mapprofielen\)
   - modified `com.adobe.fmdita.config.ConfigManager`
   - Controle als om het even welke douanecode om het even welke oude wegen \ (zoals vermeld in de [ Afbeelding van de Migratie ](#id2244LE040XA) sectie \) gebruikte - zou aan de nieuwe wegen moeten worden bijgewerkt zodat de aanpassingen ook zoals verwacht werken.
1. Lees over om het even welke nieuwe configuraties die in de huidige versie \ (controle [ worden gebracht de Nota&#39;s van de Versie ](../release-info/release-notes-4-3.md) \) en zie of wordt om het even welke functionaliteit beïnvloed dan aangewezen actie. Een voorbeeld hiervan is &quot;Verbeterde bestands- en versieverwerking&quot; die is geïntroduceerd in versie 4.0, waarvoor u een configuratie moet inschakelen.

## Stappen om de bestaande inhoud te indexeren voor het gebruik van de nieuwe zoek- en vervangactie:

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe tekst zoeken en vervangen op kaartniveau te gebruiken:

- Voer een POST-aanvraag uit op de server \(met correcte verificatie\) - `http://<server:port\>/bin/guides/map-find/indexing` . \(Optioneel: u kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd \|\| Bijvoorbeeld: `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`\)

- De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden -

`http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)

- Zodra de taak is voltooid, reageert het bovenstaande GET-verzoek met succes en vermeldt het of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

Als de upgradetaak mislukt en in het foutenlogboek de volgende fout wordt weergegeven:

&quot;De *vraag* leest of overging meer dan *100000 knopen*. Om te voorkomen dat andere taken worden beïnvloed, is de verwerking gestopt.&quot;

Dit kan gebeuren omdat de index niet correct is ingesteld voor de query die wordt gebruikt in de upgrade. U kunt de volgende tijdelijke oplossing uitproberen:

1. Voeg in de dammerAssetLucene-eikenindex de booleaanse eigenschap `indexNodeName` als `true` toe in het knooppunt.
   `/oak:index/damAssetLucene/indexRules/dam:Asset`
1. Voeg een nieuw knooppunt toe met het naamfragment onder het knooppunt.

   `/oak:index/damAssetLucene/indexRules/dam:Asset/properties`
en stel de volgende eigenschappen in het knooppunt in:

   ```
   name - rep:excerpt
   propertyIndex - {Boolean}true
   notNullCheckEnabled - {Boolean}true
   ```

   De structuur van `damAssetLucene` moet er ongeveer als volgt uitzien:

   ```
   <damAssetLucene compatVersion="{Long}2" async="async, nrt" jcr:primaryType="oak:QueryIndexDefinition" evaluatePathRestrictions="{Boolean}true" type="lucene">
   <indexRules jcr:primaryType="nt:unstructured">
     <dam:Asset indexNodeName="{Boolean}true" jcr:primaryType="nt:unstructured">
       <properties jcr:primaryType="nt:unstructured">
         <excerpt name="rep:excerpt" propertyIndex="{Boolean}true" jcr:primaryType="nt:unstructured" notNullCheckEnabled="{Boolean}true"/>
       </properties>
       </dam:Asset>
     </indexRules>
   </damAssetLucene>    
   ```


   (samen met andere bestaande knooppunten en eigenschappen)

1. De index van de `damAssetLucene` index opnieuw indexeren (door de herindexmarkering in te stellen als `true` onder
en wacht tot het `false` opnieuw is (dit geeft aan dat het opnieuw indexeren is voltooid). Het kan een paar uur duren, afhankelijk van de grootte van de index.
1. Voer de vorige stappen uit om het indexeringsscript opnieuw uit te voeren.


## Upgrade naar versie 4.2.1

>[!TIP]
>
>U wordt aangeraden Hotfix 4.2.1.3 vóór versie 4.2.1 te installeren.

De upgrade naar versie 4.2.1 is afhankelijk van de huidige versie van Experience Manager Guides. Als u versie 4.1 of 4.1.x of 4.2 gebruikt, kunt u rechtstreeks een upgrade uitvoeren naar versie 4.2.1.

>[!NOTE]
>
>De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

****Eerste vereisten****

Voordat u het Experience Manager Guides 4.2.1-upgradeproces start, moet u controleren of:

1. Bijgewerkt naar Experience Manager Guides versie 4.1, 4.1.x of 4.2.
1. Alle vertaaltaken zijn afgesloten.
1. Veranderde het logboekniveau in **INFO** voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` klasse en voeg deze logboeken in een nieuw logboekdossier toe, bijvoorbeeld, `logs/translation_upgrade.log.`

>[!NOTE]
>
> Sluit alle actieve revisies. Als de revisietaken niet worden afgesloten tijdens de upgrade naar 4.2, nemen de oudere revisietaken in uitvoering voortdurend gebruikers op de oudere revisiepagina&#39;s. De revisietaken die na de upgrade worden gemaakt, geven de nieuwste updates in de functionaliteit weer.

## Versie 4.2.1 installeren

1. Download 4.2.1 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installeer versie 4.2.1.
1. U kunt ervoor kiezen om de trigger te HIT om de upgradetaak voor de vertaalkaart te starten. Voor details, zie [ trekker van manuscript via een Servlet ](#enable-trigger-of-script-via-a-servlet-for-421) toelaten.


1. Nadat u de pakketinstallatie hebt voltooid, wacht u op het volgende bericht in de logbestanden:

   `Completed the post deployment setup script`

   Het bovenstaande bericht geeft aan dat alle installatiestappen zijn voltooid.

   Als u om het even welke volgende prefix van de FOUT ontmoet, rapporteer hen aan uw team van het klantensucces:

   - Fout tijdens een setupscript voor implementatie na plaatsing
   - Uitzondering tijdens het exporteren van de MAP voor vertaling
   - Kan vertaalkaart van v1 naar v2 voor eigenschap niet importeren
1. Upgrade de insteekmodule Zuurstofaansluiting die wordt vrijgegeven met versie 4.2 \(indien nodig\).
1. Wis de browsercache nadat u het pakket hebt geïnstalleerd.
1. U kunt de aanpassingen blijven bijwerken zoals in de volgende sectie wordt beschreven.

### Stapsgewijze activering van het script via een servlet inschakelen (voor 4.2.1)

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

Voorbeeldlogboek:
Hieronder volgt een voorbeeld van logboeken die in het logbestand worden weergegeven nadat u het script hebt geactiveerd.

```
04.05.2023 14:17:12.876 *INFO* [[0:0:0:0:0:0:0:1] [1683190032736] POST /bin/guides/script/start HTTP/1.1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Acquiring lock for job : translation-map-upgrade
04.05.2023 14:17:12.897 *INFO* [pool-59-thread-1] com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Starting the thread to upgrade translation map from V1 to V2
04.05.2023 14:17:12.899 *INFO* [pool-59-thread-1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Initiating lock for node : /var/dxml/executor-locks/translation-map-upgrade/1683190032886
04.05.2023 14:17:12.901 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Starting porting of translation map from V1 to V2
04.05.2023 14:17:12.904 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Memory increase is of : 764 kB
04.05.2023 14:17:12.906 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Completed porting of translation map from V1 to V2
04.05.2023 14:17:12.907 *INFO* [pool-59-thread-1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Releasing lock for node : /var/dxml/executor-locks/translation-map-upgrade/1683190032886
04.05.2023 14:17:12.909 *INFO* [pool-59-thread-1] com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Completed the thread to upgrade translation map from V1 to V2
```

Zoek `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Completed porting of translation map from V1 to V2` en `com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Completed the thread to upgrade translation map from V1 to V2` voordat u verdergaat met de volgende stappen.



## Nadat u versie 4.2.1 hebt geïnstalleerd

>[!IMPORTANT]
>
> Hi-tech-sjabloon wordt niet weergegeven op een geüpgrade server. Als u de hi-tech sjabloon op uw server wilt opnemen, kunt u deze kopiëren: Source: /libs/fmdita/pdf/Hi-Tech Destination: /content/dam/dita-templates/pdf

Nadat u Experience Manager Guides hebt geïnstalleerd, kunt u de verschillende configuraties samenvoegen die van toepassing zijn vanaf de nieuw geïnstalleerde versie tot aan uw installatie.

>[!NOTE]
>
> Het dampupdate-assetmodel kan worden aangepast. Dus als er aanpassingen zijn uitgevoerd, moeten we de aanpassingen en Experience Manager Guides synchroniseren in de werkkopie van het model.

1. **DAM het werkschema van de Activa van de Update \ (veranderingen \):**

1. URL openen:

   ```http
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html
   ```

1. Selecteer **DAM het werkschema van Activa van de Update**.
1. Klik op **uitgeven**.
1. Als de **component van de Initiator van het Proces van 0} DXML {aanwezig is, zorg ervoor dat de aanpassingen worden gesynchroniseerd.**
1. Als de **component van de Initiator van het Proces van 0} DXML {ontbreekt, voer de volgende stappen uit om het op te nemen:**

1. Klik **component van het Tussenvoegsel** \ (Verantwoordelijk voor Experience Manager Guides post-verwerking als definitieve stap in het proces \).
1. Vorm de **stap van het Proces** met hieronder details:

   **Gemeenschappelijke lusje**

   **Titel:** DXML de Initiator van het Proces van het Post

   **Beschrijving**: De stap van de initiator van het postproces DXML die een slingerbaan voor DXML post-verwerking van het gewijzigde/gecreeerde element zal teweegbrengen

   **lusje van het Proces**

   - Selecteer **DXML de Initiator van het Proces van het Post** van het **Proces** drop down

   - Selecteer **de Geavanceerde Behandeling van 0}**

   - Selecteer **Gereed**

1. Klik **Synchronisatie** op het hoogste recht na de voltooiing van de veranderingen. Je ontvangt een melding over succes.

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
   - Alle componenten die worden overschreven door/libs/fmditor/libsc, moeten worden vergeleken met de nieuwe productcode en updates moeten worden uitgevoerd in overlay bestanden onder/apps.
   - Alle clientlibcategorieën die worden gebruikt van het product, dienen te worden gecontroleerd op wijzigingen. Overschreven configuraties \(voorbeelden verderop\) moeten worden vergeleken met de nieuwste configuraties om de nieuwste functies te krijgen:
   - elementmapping.xml
   - ui\_config.json\(kan zijn ingesteld in mapprofielen\)
   - modified `com.adobe.fmdita.config.ConfigManager`
   - Controle als om het even welke douanecode om het even welke oude wegen \ (zoals vermeld in de [ Afbeelding van de Migratie ](#id2244LE040XA) sectie \) gebruikte - zou aan de nieuwe wegen moeten worden bijgewerkt zodat de aanpassingen ook zoals verwacht werken.
1. Lees over om het even welke nieuwe configuraties die in de huidige versie \ (controle [ worden gebracht de Nota&#39;s van de Versie ](../release-info/release-notes-4-2-1.md) \) en zie of wordt om het even welke functionaliteit beïnvloed dan aangewezen actie. Een voorbeeld hiervan is &quot;Verbeterde bestands- en versieverwerking&quot; die is geïntroduceerd in versie 4.0, waarvoor u een configuratie moet inschakelen.

## Stappen om de bestaande inhoud te indexeren voor het gebruik van de nieuwe zoek- en vervangactie:

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe tekst zoeken en vervangen op kaartniveau te gebruiken:

- Controleer of de indexering van `damAssetLucene` is voltooid. Het kan een paar uur duren, afhankelijk van de hoeveelheid gegevens die aanwezig is op de server. U kunt bevestigen dat het opnieuw indexeren is voltooid door te controleren of het veld voor opnieuw indexeren in
  `http://<server:port>/oak:index/damAssetLucene`.  Als u aanpassingen hebt toegevoegd in `damAssetLucene` , moet u deze mogelijk opnieuw toepassen.

- Voer een POST-aanvraag uit op de server \(met correcte verificatie\) - `http://<server:port\>/bin/guides/map-find/indexing` . (Optioneel: u kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd \|\| Bijvoorbeeld : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

- U kunt ook een hoofdmap doorgeven om de DITA-kaarten van een specifieke map (en de bijbehorende submappen) te indexeren. Bijvoorbeeld `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test` . Wanneer zowel de parameter paths als de hoofdparameter worden doorgegeven, wordt alleen de parameter paths gebruikt.

- De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


- Zodra de taak is voltooid, reageert het bovenstaande GET-verzoek met succes en vermeldt het of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.


## Upgrade naar versie 4.3.0

De upgrade naar versie 4.3.0 is afhankelijk van de huidige versie van Experience Manager Guides. Als u versie 4.2 of 4.2.x gebruikt, kunt u rechtstreeks upgraden naar versie 4.3.0.

>[!NOTE]
>
>De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

****Eerste vereisten****

Voordat u het Experience Manager Guides 4.3.0-upgradeproces start, moet u controleren of:

1. Geüpgraded naar Experience Manager Guides versie 4.2 of 4.2.x en hun respectieve installatiestappen voltooid.
1. Alle vertaaltaken zijn afgesloten.



## Versie 4.3.0 installeren

1. Download 4.3.0 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installeer versie 4.3.0.
1. Wis de browsercache nadat u het pakket hebt geïnstalleerd.
1. Bevorder het `ui_config.json` dossier van het **lusje van de Configuratie van de Redacteur van XML** in het Profiel van de Omslag.


## Nadat u versie 4.3.0 hebt geïnstalleerd

Nadat u Experience Manager Guides hebt geïnstalleerd, kunt u de verschillende configuraties samenvoegen die van toepassing zijn vanaf de nieuw geïnstalleerde versie tot aan uw installatie.

## Stappen om de bestaande inhoud te posten om het verbroken koppelingsrapport te gebruiken


Voer de volgende stappen uit voor de naverwerking van de bestaande inhoud en het gebruik van het nieuwe verbroken koppelingsrapport:

1. (Optioneel) Als het systeem meer dan 100.000 dita-bestanden bevat, werkt u `queryLimitReads` under `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` bij tot een hogere waarde (een waarde die groter is dan het aantal aanwezige elementen, bijvoorbeeld 200.000) en herstelt u deze vervolgens.

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



## Upgrade naar versie 4.3.1

De upgrade naar versie 4.3.1 is afhankelijk van de huidige versie van Experience Manager Guides. Als u versie 4.3.0, 4.2 of 4.2.1 gebruikt, kunt u rechtstreeks upgraden naar versie 4.3.1.

>[!NOTE]
>
>De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

****Eerste vereisten****

Voordat u het Experience Manager Guides 4.3.1-upgradeproces start, moet u controleren of:

1. Geüpgraded naar Experience Manager Guides versie 4.3.0, 4.2 of 4.2.1 en hun respectieve installatiestappen voltooid.
1. (Optioneel) Alle vertaaltaken zijn afgesloten.
1. Veranderde het logboekniveau in **INFO** voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` klasse en voeg deze logboeken in een nieuw logboekdossier toe, bijvoorbeeld, `logs/translation_upgrade.log`.


## Versie 4.3.1 installeren

1. Download 4.3.1 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installeer versie 4.3.1.
1. U kunt ervoor kiezen om de trigger te HIT om de upgradetaak voor de vertaalkaart te starten. Voor details, zie [ trekker van manuscript via een Servlet ](#enable-trigger-of-script-via-a-servlet-for-431) toelaten.


1. Nadat u de pakketinstallatie hebt voltooid, wacht u op het volgende bericht in de logbestanden:

   `Completed the post deployment setup script`

   Het bovenstaande bericht geeft aan dat alle installatiestappen zijn voltooid.

   Als u om het even welke volgende prefix van de FOUT ontmoet, rapporteer hen aan uw team van het klantensucces:

   - Fout tijdens een setupscript voor implementatie na plaatsing
   - Uitzondering tijdens het exporteren van de MAP voor vertaling
   - Kan vertaalkaart van v1 naar v2 voor eigenschap niet importeren
1. Upgrade de insteekmodule Zuurstofaansluiting die wordt vrijgegeven met versie 4.2 \(indien nodig\).
1. Wis de browsercache nadat u het pakket hebt geïnstalleerd.
1. U kunt de aanpassingen blijven bijwerken zoals in de volgende sectie wordt beschreven.

### Stapsgewijze activering van het script via een servlet inschakelen (voor 4.3.1)

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

Voorbeeldlogboek:
Hieronder volgt een voorbeeld van logboeken die in het logbestand worden weergegeven nadat u het script hebt geactiveerd.

```
04.05.2023 14:17:12.876 *INFO* [[0:0:0:0:0:0:0:1] [1683190032736] POST /bin/guides/script/start HTTP/1.1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Acquiring lock for job : translation-map-upgrade
04.05.2023 14:17:12.897 *INFO* [pool-59-thread-1] com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Starting the thread to upgrade translation map from V1 to V2
04.05.2023 14:17:12.899 *INFO* [pool-59-thread-1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Initiating lock for node : /var/dxml/executor-locks/translation-map-upgrade/1683190032886
04.05.2023 14:17:12.901 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Starting porting of translation map from V1 to V2
04.05.2023 14:17:12.904 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Memory increase is of : 764 kB
04.05.2023 14:17:12.906 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Completed porting of translation map from V1 to V2
04.05.2023 14:17:12.907 *INFO* [pool-59-thread-1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Releasing lock for node : /var/dxml/executor-locks/translation-map-upgrade/1683190032886
04.05.2023 14:17:12.909 *INFO* [pool-59-thread-1] com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Completed the thread to upgrade translation map from V1 to V2
```

Zoek `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Completed porting of translation map from V1 to V2` en `com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Completed the thread to upgrade translation map from V1 to V2` voordat u verdergaat met de volgende stappen.

## Nadat u versie 4.3.1 hebt geïnstalleerd



Nadat u Experience Manager Guides hebt geïnstalleerd, kunt u de verschillende configuraties samenvoegen die van toepassing zijn vanaf de nieuw geïnstalleerde versie tot aan uw installatie.

>[!NOTE]
>
> Het dampupdate-assetmodel kan worden aangepast. Dus als er aanpassingen zijn uitgevoerd, moeten we de aanpassingen en Experience Manager Guides synchroniseren in de werkkopie van het model.

1. **DAM het werkschema van de Activa van de Update \ (veranderingen \):**

1. URL openen:

   ```
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html 
   ```

1. Selecteer **DAM het werkschema van Activa van de Update**.
1. Klik op **uitgeven**.
1. Als de **component van de Initiator van het Proces van 0} DXML {aanwezig is, zorg ervoor dat de aanpassingen worden gesynchroniseerd.**
1. Als de **component van de Initiator van het Proces van 0} DXML {ontbreekt, voer de volgende stappen uit om het op te nemen:**

1. Klik **component van het Tussenvoegsel** \ (Verantwoordelijk voor Experience Manager Guides post-verwerking als definitieve stap in het proces \).
1. Vorm de **stap van het Proces** met hieronder details:

   **Gemeenschappelijke lusje**

   **Titel:** DXML de Initiator van het Proces van het Post

   **Beschrijving**: De stap van de initiator van het postproces DXML die een slingerbaan voor DXML post-verwerking van het gewijzigde/gecreeerde element zal teweegbrengen

   **lusje van het Proces**

   - Selecteer **DXML de Initiator van het Proces van het Post** van het **Proces** drop down

   - Selecteer **de Geavanceerde Behandeling van 0}**

   - Selecteer **Gereed**

1. Klik **Synchronisatie** op het hoogste recht na de voltooiing van de veranderingen. Je ontvangt een melding over succes.

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
   - Alle componenten die worden overschreven door/libs/fmditor/libsc, moeten worden vergeleken met de nieuwe productcode en updates moeten worden uitgevoerd in overlay bestanden onder/apps.
   - Alle clientlibcategorieën die worden gebruikt van het product, dienen te worden gecontroleerd op wijzigingen. Overschreven configuraties \(voorbeelden verderop\) moeten worden vergeleken met de nieuwste configuraties om de nieuwste functies te krijgen:
   - elementmapping.xml
   - ui\_config.json\(kan zijn ingesteld in mapprofielen\)
   - modified `com.adobe.fmdita.config.ConfigManager`


## Stappen om de bestaande inhoud te indexeren

>[!NOTE]
>
> U hoeft deze stappen niet uit te voeren als u een upgrade uitvoert van 4.3.0 of 4.2.1.

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe tekst zoeken en vervangen op kaartniveau te gebruiken:


- Voer een POST-aanvraag uit op de server \(met correcte verificatie\) - `http://<server:port\>/bin/guides/map-find/indexing` . (Optioneel: u kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd \|\| Bijvoorbeeld : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)


- De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


- Zodra de taak is voltooid, reageert het bovenstaande GET-verzoek met succes en vermeldt het of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

## Stappen om de bestaande inhoud te posten om het verbroken koppelingsrapport te gebruiken

>[!NOTE]
>
> U hoeft deze stappen niet uit te voeren als u een upgrade uitvoert van 4.3.0

Voer de volgende stappen uit voor de naverwerking van de bestaande inhoud en het gebruik van het nieuwe verbroken koppelingsrapport:

1. (Optioneel) Als het systeem meer dan 100.000 dita-bestanden bevat, werkt u `queryLimitReads` under `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` bij tot een hogere waarde (een waarde die groter is dan het aantal aanwezige elementen, bijvoorbeeld 200.000) en herstelt u deze vervolgens.

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



## Upgrade naar versie 4.3.1.5

De upgrade naar versie 4.3.1.5 is afhankelijk van de huidige versie van Experience Manager Guides. Als u versie 4.3.1 gebruikt, kunt u rechtstreeks een upgrade uitvoeren naar versie 4.3.1.5 .



## Versie installeren 4.3.1.5

1. Download 4.3.1.5 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installeer versie 4.3.1.5 .

1. Wacht tot het installatieproces is voltooid.
1. U kunt de aanpassingen blijven bijwerken zoals in de volgende sectie wordt beschreven.


## Nadat u versie hebt geïnstalleerd 4.3.1.5


>[!NOTE]
>
>Als u de bundel org.apache.velocity wilt gebruiken, voert u de volgende stappen uit voordat u de bundel uploadt:
> 1. Ga naar `<server>:<port>/system/console/bundles` .
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

De upgrade naar versie 4.4.0 is afhankelijk van de huidige versie van Experience Manager Guides. Als u versie 4.3.1, 4.3.0, 4.2 of 4.2.1 (Hotfix 4.2.1.3) gebruikt, kunt u rechtstreeks upgraden naar versie 4.4.0

>[!NOTE]
>
>De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

****Eerste vereisten****

Voordat u het Experience Manager Guides 4.4.0-upgradeproces start, moet u controleren of:

1. Geüpgraded naar Experience Manager Guides versie 4.3.1, 4.3.0 of 4.2.1 (Hotfix 4.2.1.3) en de desbetreffende installatiestappen voltooid.
1. (Optioneel) Alle vertaaltaken zijn afgesloten.
1. Veranderde het logboekniveau in **INFO** voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` klasse en voeg deze logboeken in een nieuw logboekdossier toe, bijvoorbeeld, `logs/translation_upgrade.log`.


## Versie 4.4.0 installeren

1. Download 4.4.0 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installeer versie 4.4.0.
1. U kunt ervoor kiezen om de trigger te HIT om de upgradetaak voor de vertaalkaart te starten. Voor details, zie [ trekker van manuscript via een Servlet ](#enable-trigger-of-script-via-a-servlet) toelaten.

1. Nadat u de pakketinstallatie hebt voltooid, wacht u op het volgende bericht in de logbestanden:

   `Completed the post deployment setup script`

   Het bovenstaande bericht geeft aan dat alle installatiestappen zijn voltooid.

   Als u om het even welke volgende prefix van de FOUT ontmoet, rapporteer hen aan uw team van het klantensucces:

   - Fout tijdens een setupscript voor implementatie na plaatsing
   - Uitzondering tijdens het exporteren van de MAP voor vertaling
   - Kan vertaalkaart van v1 naar v2 voor eigenschap niet importeren
1. Upgrade de insteekmodule Zuurstofaansluiting die wordt vrijgegeven met versie 4.4.0 \(indien nodig\).
1. Wis de browsercache nadat u het pakket hebt geïnstalleerd.
1. U kunt de aanpassingen blijven bijwerken zoals in de volgende sectie wordt beschreven.


## Nadat u versie 4.4.0 hebt geïnstalleerd

Nadat u Experience Manager Guides hebt geïnstalleerd, kunt u de verschillende configuraties samenvoegen die van toepassing zijn vanaf de nieuw geïnstalleerde versie tot aan uw installatie.

>[!NOTE]
>
> Het dampupdate-assetmodel kan worden aangepast. Dus als er aanpassingen zijn uitgevoerd, moeten we de aanpassingen en Experience Manager Guides synchroniseren in de werkkopie van het model.

1. **DAM het werkschema van de Activa van de Update \ (veranderingen \):**

1. URL openen:

   ```
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html 
   ```

1. Selecteer **DAM het werkschema van Activa van de Update**.
1. Klik op **uitgeven**.
1. Als de **component van de Initiator van het Proces van 0} DXML {aanwezig is, zorg ervoor dat de aanpassingen worden gesynchroniseerd.**
1. Als de **component van de Initiator van het Proces van 0} DXML {ontbreekt, voer de volgende stappen uit om het op te nemen:**

1. Klik **component van het Tussenvoegsel** \ (Verantwoordelijk voor Experience Manager Guides post-verwerking als definitieve stap in het proces \).
1. Vorm de **stap van het Proces** met hieronder details:

   **Gemeenschappelijke lusje**

   **Titel:** DXML de Initiator van het Proces van het Post

   **Beschrijving**: De stap van de initiator van het postproces DXML die een slingerbaan voor DXML post-verwerking van het gewijzigde/gecreeerde element zal teweegbrengen

   **lusje van het Proces**

   - Selecteer **DXML de Initiator van het Proces van het Post** van het **Proces** drop down

   - Selecteer **de Geavanceerde Behandeling van 0}**

   - Selecteer **Gereed**

1. Klik **Synchronisatie** op het hoogste recht na de voltooiing van de veranderingen. Je ontvangt een melding over succes.

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
   - Alle componenten die worden overschreven door/libs/fmditor/libsc, moeten worden vergeleken met de nieuwe productcode en updates moeten worden uitgevoerd in overlay bestanden onder/apps.
   - Alle clientlibcategorieën die worden gebruikt van het product, dienen te worden gecontroleerd op wijzigingen. Overschreven configuraties \(voorbeelden verderop\) moeten worden vergeleken met de nieuwste configuraties om de nieuwste functies te krijgen:
   - elementmapping.xml
   - ui\_config.json\(kan zijn ingesteld in mapprofielen\)
   - modified `com.adobe.fmdita.config.ConfigManager`

1. Als u aanpassingen hebt toegevoegd in damAssetLucene, kan het nodig zijn deze opnieuw toe te passen. Nadat u deze wijzigingen hebt aangebracht, stelt u de index in op true. Hierdoor worden alle bestaande knooppunten opnieuw gecompileerd met de aanpassingen. Nadat de rendex-markering is voltooid, wordt deze weer op false ingesteld. Dit kan een paar uur duren, afhankelijk van het aantal elementen in het systeem.

## Stappen om de bestaande inhoud te indexeren

>[!NOTE]
>
> U hoeft deze stappen niet uit te voeren als u een upgrade uitvoert van 4.3.0 of 4.3.1.

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe tekst zoeken en vervangen op kaartniveau te gebruiken:

- Voer een POST-aanvraag uit op de server \(met correcte verificatie\) - `http://<server:port\>/bin/guides/map-find/indexing` . (Optioneel: u kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd \|\| Bijvoorbeeld : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

- De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)

- Zodra de taak is voltooid, reageert het bovenstaande GET-verzoek met succes en vermeldt het of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

## Stappen om de bestaande inhoud te posten om het verbroken koppelingsrapport te gebruiken

>[!NOTE]
>
> U hoeft deze stappen niet uit te voeren als u een upgrade uitvoert van 4.3.0 of 4.3.1.

Voer de volgende stappen uit voor de naverwerking van de bestaande inhoud en het gebruik van het nieuwe verbroken koppelingsrapport:

1. (Optioneel) Als het systeem meer dan 100.000 dita-bestanden bevat, werkt u `queryLimitReads` under `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` bij tot een hogere waarde (een waarde die groter is dan het aantal aanwezige elementen, bijvoorbeeld 200.000) en herstelt u deze vervolgens.

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

### Triggerscript activeren via een Servlet

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



## Stappen voor het afhandelen van het `'fmdita rewriter'` -conflict

Experience Manager Guides heeft de module van de a [**douane die herschrijver**](../cs-install-guide/conf-output-generation.md#custom-rewriter) voor de behandeling van de verbindingen in het geval van dwars-kaarten (verbindingen tussen de onderwerpen van twee verschillende kaarten) worden geproduceerd.

Als u nog een aangepaste schrijfbewerking voor tekenreeksen in uw codebase hebt, gebruikt u een `'order'` -waarde groter dan 50, omdat Experience Manager Guides anders `'order'` 50 gebruikt.  Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer details, mening [ Output die pijplijnen herschrijft ](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Aangezien de waarde van `'order'` tijdens deze upgrade is gewijzigd van 1000 in 50, moet u eventueel de bestaande aangepaste rewriter samenvoegen met `'fmdita-rewriter'` .


**Bovenliggend onderwerp:**[ Download en installeer ](download-install.md)


## Upgrade naar versie 4.6.0

>[!TIP]
>
> Het wordt aanbevolen om 4.6.0 Service Pack 4 bovenop versie 4.6.0, 4.6.0 Service Pack 1 of 4.6.0 Service Pack 3 te installeren. Het verbeteringsproces voor 4.6.0 Service Pack 4 versie volgt de zelfde stappen zoals de versie 4.6.0.

De upgrade naar versie 4.6.0 is afhankelijk van de huidige versie van Experience Manager Guides. Als u versie 4.4.0, 4.3.1, 4.3.0, 4.2 of 4.2.1 (Hotfix 4.2.1.3) gebruikt, kunt u rechtstreeks upgraden naar versie 4.6.0.

>[!NOTE]
>
> De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

****Eerste vereisten****

Voordat u het Experience Manager Guides 4.6.0-upgradeproces start, moet u controleren of:

1. Geüpgraded naar Experience Manager Guides versie 4.3.1, 4.3.0 of 4.2.1 (Hotfix 4.2.1.3) en de desbetreffende installatiestappen voltooid.
1. (Optioneel) Alle vertaaltaken zijn afgesloten.
1. Veranderde het logboekniveau in **INFO** voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` klasse en voeg deze logboeken in een nieuw logboekdossier toe, bijvoorbeeld, `logs/translation_upgrade.log`.


## Versie 4.6.0 installeren

1. Download 4.6.0 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installeer versie 4.6.0.
1. U kunt ervoor kiezen om de trigger te HIT om de upgradetaak voor de vertaalkaart te starten. Voor details, zie [ trekker van manuscript via een Servlet ](#enable-trigger-of-script-via-a-servlet) toelaten.

1. Nadat u de pakketinstallatie hebt voltooid, wacht u op het volgende bericht in de logbestanden:

   `Completed the post deployment setup script`

   Het bovenstaande bericht geeft aan dat alle installatiestappen zijn voltooid.

   Als u om het even welke volgende prefix van de FOUT ontmoet, rapporteer hen aan uw team van het klantensucces:

   - Fout tijdens een setupscript voor implementatie na plaatsing
   - Uitzondering tijdens het exporteren van de MAP voor vertaling
   - Kan vertaalkaart van v1 naar v2 voor eigenschap niet importeren
1. Upgrade de insteekmodule Zuurstofaansluiting die wordt vrijgegeven met versie 4.6.0 \(indien nodig\).
1. Wis de browsercache nadat u het pakket hebt geïnstalleerd.

## Nadat u versie 4.6.0 hebt geïnstalleerd

Nadat u Experience Manager Guides hebt geïnstalleerd, kunt u de verschillende configuraties samenvoegen die van toepassing zijn vanaf de nieuw geïnstalleerde versie tot aan uw installatie.

>[!NOTE]
>
> Het dampupdate-assetmodel kan worden aangepast. Dus als er aanpassingen zijn uitgevoerd, moeten we de aanpassingen en Experience Manager Guides synchroniseren in de werkkopie van het model.

1. **DAM het werkschema van de Activa van de Update \ (veranderingen \):**

1. URL openen:

   ```
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html 
   ```

1. Selecteer **DAM het werkschema van Activa van de Update**.
1. Klik op **uitgeven**.
1. Als de **component van de Initiator van het Proces van 0} DXML {aanwezig is, zorg ervoor dat de aanpassingen worden gesynchroniseerd.**
1. Als de **component van de Initiator van het Proces van 0} DXML {ontbreekt, voer de volgende stappen uit om het op te nemen:**

1. Klik **component van het Tussenvoegsel** \ (Verantwoordelijk voor Experience Manager Guides post-verwerking als definitieve stap in het proces \).
1. Vorm de **stap van het Proces** met hieronder details:

   **Gemeenschappelijke lusje**

   **Titel:** DXML de Initiator van het Proces van het Post

   **Beschrijving**: De stap van de initiator van het postproces DXML die een slingerbaan voor DXML post-verwerking van het gewijzigde/gecreeerde element zal teweegbrengen

   **lusje van het Proces**

   - Selecteer **DXML de Initiator van het Proces van het Post** van het **Proces** drop down

   - Selecteer **de Geavanceerde Behandeling van 0}**

   - Selecteer **Gereed**

1. Klik **Synchronisatie** op het hoogste recht na de voltooiing van de veranderingen. Je ontvangt een melding over succes.

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
   - Alle componenten die worden overschreven door/libs/fmditor/libsc, moeten worden vergeleken met de nieuwe productcode en updates moeten worden uitgevoerd in overlay bestanden onder/apps.
   - Alle clientlibcategorieën die worden gebruikt van het product, dienen te worden gecontroleerd op wijzigingen. Overschreven configuraties \(voorbeelden verderop\) moeten worden vergeleken met de nieuwste configuraties om de nieuwste functies te krijgen:
   - elementmapping.xml
   - ui\_config.json\(kan zijn ingesteld in mapprofielen\)
   - modified `com.adobe.fmdita.config.ConfigManager`

1. Als u aanpassingen hebt toegevoegd in damAssetLucene, kan het nodig zijn deze opnieuw toe te passen. Nadat u deze wijzigingen hebt aangebracht, stelt u de index in op true. Hierdoor worden alle bestaande knooppunten opnieuw gecompileerd met de aanpassingen. Nadat de rendex-markering is voltooid, wordt deze weer op false ingesteld. Dit kan een paar uur duren, afhankelijk van het aantal elementen in het systeem.

## Stappen om de Experience Manager Guides-indexen opnieuw te indexeren

1. Open `crx/de` en navigeer naar het indexpad: `/oak:index/guidesAssetProperties`
2. Plaats het herindexbezit als `true` (`false` door gebrek) en klik **sparen allen**.
3. Zodra de redex volledig is, wordt de redex-eigenschap opnieuw ingesteld op `false` en wordt de redex-telling met 1 verhoogd.

   >[!NOTE]
   >
   > Dit kan een paar minuten duren, afhankelijk van de hoeveelheid gegevens die aanwezig is.
4. Voer dezelfde stappen uit voor andere toegevoegde of gewijzigde indexen: `guidesBulkActivation`, `guidesPeerLinkIndex` en `guidesKonnectTemplateIndex` .

## Stappen om de bestaande inhoud te indexeren



Voer de volgende stappen uit om de bestaande inhoud te indexeren:

- Voer een POST-aanvraag uit op de server \(met correcte verificatie\) - `http://<server:port\>/bin/guides/map-find/indexing` . (Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd || Voorbeeld: `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

- De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(bijvoorbeeld: ` http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

- Zodra de taak is voltooid, reageert het bovenstaande GET-verzoek met succes en vermeldt het of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.


>[!NOTE]
>
> Als u het douaneschema gebruikt, moet u de weg van de dossiers van douane DTD en XSD catalog.xml in de bewaarplaats van AEM in **bepalen integreer Catalogi** optie.




## Stappen voor het afhandelen van het `'fmdita rewriter'` -conflict

Experience Manager Guides heeft de module van de a [**douane die herschrijver**](../cs-install-guide/conf-output-generation.md#custom-rewriter) voor de behandeling van de verbindingen in het geval van dwars-kaarten (verbindingen tussen de onderwerpen van twee verschillende kaarten) worden geproduceerd.

Als u nog een aangepaste schrijfbewerking voor tekenreeksen in uw codebase hebt, gebruikt u een `'order'` -waarde groter dan 50, omdat Experience Manager Guides anders `'order'` 50 gebruikt.  Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer details, mening [ Output die pijplijnen herschrijft ](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Aangezien de waarde van `'order'` tijdens deze upgrade is gewijzigd van 1000 in 50, moet u eventueel de bestaande aangepaste rewriter samenvoegen met `'fmdita-rewriter'` .


## Upgrade naar versie 5.0.0

>[!TIP]
>
> De bevordering aan versie 5.0.0 Service Pack 2 hangt van de huidige versie van Experience Manager Guides af. Als u versie 5.0.0 Service Pack 1 of 5.0.0 gebruikt, dan kunt u aan versie 5.0.0 Service Pack 2 direct bevorderen.

>[!NOTE]
>
> De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

****Eerste vereisten****

Voordat u het Experience Manager Guides 5.0.0-upgradeproces start, moet u controleren of:

1. Geüpgraded naar Experience Manager Guides versie 4.6.3, 4.6.1, 4.6.0 of 4.4 en hun respectieve installatiestappen voltooid.
1. (Optioneel) Alle vertaaltaken zijn afgesloten.
1. Veranderde het logboekniveau in **INFO** voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` klasse en voeg deze logboeken in een nieuw logboekdossier toe, bijvoorbeeld, `logs/translation_upgrade.log`.


## Versie 5.0.0 installeren

1. Download 5.0.0 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installeer het pakket versie 5.0.0.
1. U kunt ervoor kiezen om de trigger te HIT om de upgradetaak voor de vertaalkaart te starten. Voor details, zie [ trekker van manuscript via een Servlet ](#enable-trigger-of-script-via-a-servlet) toelaten.

1. Nadat u de pakketinstallatie hebt voltooid, wacht u op het volgende bericht in de logbestanden:

   `Completed the post deployment setup script`

   Het bovenstaande bericht geeft aan dat alle installatiestappen zijn voltooid.

   Als u om het even welke volgende prefix van de FOUT ontmoet, rapporteer hen aan uw team van het klantensucces:

   - Fout tijdens een setupscript voor implementatie na plaatsing
   - Uitzondering tijdens het exporteren van de MAP voor vertaling
   - Kan vertaalkaart van v1 naar v2 voor eigenschap niet importeren
1. Upgrade de insteekmodule Zuurstofaansluiting die wordt vrijgegeven met versie 5.0.0 \(indien nodig\).
1. Wis de browsercache nadat u het pakket hebt geïnstalleerd.

## Nadat u versie 5.0.0 hebt geïnstalleerd

Nadat u Experience Manager Guides hebt geïnstalleerd, kunt u de verschillende configuraties samenvoegen die van toepassing zijn vanaf de nieuw geïnstalleerde versie tot aan uw installatie.

>[!NOTE]
>
> Het dampupdate-assetmodel kan worden aangepast. Dus als er aanpassingen zijn uitgevoerd, moeten we de aanpassingen en Experience Manager Guides synchroniseren in de werkkopie van het model.

1. **DAM het werkschema van de Activa van de Update \ (veranderingen \):**

1. URL openen:

   ```
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html 
   ```

1. Selecteer **DAM het werkschema van Activa van de Update**.
1. Klik op **uitgeven**.
1. Als de **component van de Initiator van het Proces van 0} DXML {aanwezig is, zorg ervoor dat de aanpassingen worden gesynchroniseerd.**
1. Als de **component van de Initiator van het Proces van 0} DXML {ontbreekt, voer de volgende stappen uit om het op te nemen:**

1. Klik **component van het Tussenvoegsel** \ (Verantwoordelijk voor Experience Manager Guides post-verwerking als definitieve stap in het proces \).
1. Vorm de **stap van het Proces** met hieronder details:

   **Gemeenschappelijke lusje**

   **Titel:** DXML de Initiator van het Proces van het Post

   **Beschrijving**: De stap van de initiator van het postproces DXML die een slingerbaan voor DXML post-verwerking van het gewijzigde/gecreeerde element zal teweegbrengen

   **lusje van het Proces**

   - Selecteer **DXML de Initiator van het Proces van het Post** van het **Proces** drop down

   - Selecteer **de Geavanceerde Behandeling van 0}**

   - Selecteer **Gereed**

1. Klik **Synchronisatie** op het hoogste recht na de voltooiing van de veranderingen. Je ontvangt een melding over succes.

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
   - Alle componenten die worden overschreven door/libs/fmditor/libsc, moeten worden vergeleken met de nieuwe productcode en updates moeten worden uitgevoerd in overlay bestanden onder/apps.
   - Alle clientlibcategorieën die worden gebruikt van het product, dienen te worden gecontroleerd op wijzigingen. Overschreven configuraties \(voorbeelden verderop\) moeten worden vergeleken met de nieuwste configuraties om de nieuwste functies te krijgen:
   - elementmapping.xml
   - ui\_config.json\(kan zijn ingesteld in mapprofielen\)
   - modified `com.adobe.fmdita.config.ConfigManager`

1. Als u aanpassingen hebt toegevoegd in damAssetLucene, kan het nodig zijn deze opnieuw toe te passen. Nadat u deze wijzigingen hebt aangebracht, stelt u de index in op true. Hierdoor worden alle bestaande knooppunten opnieuw gecompileerd met de aanpassingen. Nadat de rendex-markering is voltooid, wordt deze weer op false ingesteld. Dit kan een paar uur duren, afhankelijk van het aantal elementen in het systeem.

## Stappen om de Experience Manager Guides-indexen opnieuw te indexeren

1. Open `crx/de` en navigeer naar het indexpad: `/oak:index/guidesAssetProperties`
2. Plaats het herindexbezit als `true` (`false` door gebrek) en klik **sparen allen**.
3. Zodra de redex volledig is, wordt de redex-eigenschap opnieuw ingesteld op `false` en wordt de redex-telling met 1 verhoogd.

   >[!NOTE]
   >
   > Dit kan een paar minuten duren, afhankelijk van de hoeveelheid gegevens die aanwezig is.
4. Voer dezelfde stappen uit voor andere toegevoegde of gewijzigde indexen: `guidesBulkActivation`, `guidesPeerLinkIndex` en `guidesKonnectTemplateIndex` .

## Stappen om de bestaande inhoud te indexeren



Voer de volgende stappen uit om de bestaande inhoud te indexeren:

- Voer een POST-aanvraag uit op de server \(met correcte verificatie\) - `http://<server:port\>/bin/guides/map-find/indexing` . (Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd || Voorbeeld: `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

- De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(bijvoorbeeld: ` http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

- Zodra de taak is voltooid, reageert het bovenstaande GET-verzoek met succes en vermeldt het of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.


>[!NOTE]
>
> Als u het douaneschema gebruikt, moet u de weg van de dossiers van douane DTD en XSD catalog.xml in de bewaarplaats van AEM in **bepalen integreer Catalogi** optie.




## Stappen voor het afhandelen van het `'fmdita rewriter'` -conflict

Experience Manager Guides heeft de module van de a [**douane die herschrijver**](../cs-install-guide/conf-output-generation.md#custom-rewriter) voor de behandeling van de verbindingen in het geval van dwars-kaarten (verbindingen tussen de onderwerpen van twee verschillende kaarten) worden geproduceerd.

Als u nog een aangepaste schrijfbewerking voor tekenreeksen in uw codebase hebt, gebruikt u een `'order'` -waarde groter dan 50, omdat Experience Manager Guides anders `'order'` 50 gebruikt.  Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer details, mening [ Output die pijplijnen herschrijft ](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Aangezien de waarde van `'order'` tijdens deze upgrade is gewijzigd van 1000 in 50, moet u eventueel de bestaande aangepaste rewriter samenvoegen met `'fmdita-rewriter'` .



## Stappen om de damAssetLucene opnieuw te indexeren

De indexdefinitie wordt bijgewerkt voor damAssetLucene met gidsen. Verwijs naar [ dit artikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-16460) voor het opnieuw indexeren van damAssetLucene na bevordering aan versie 5.0.0.

>[!NOTE]
>
> Terwijl het volgen van de documentatie ervoor zorgt beide eigenschappen (reindex=true en redex-async=true voor /oak :index/damAssetLucene) gelijktijdig via sparen verrichting worden bijgewerkt.

## Upgrade naar versie 5.1.0

>[!IMPORTANT]
>
> Als u momenteel op AEM 6.5 werkt en van plan bent over te stappen op AEM 6.5 LTS, dient u eerst de AEM-upgrade te voltooien voordat u verdergaat met de Experience Manager Guides 5.1.0-upgrade. Voor details, mening [ Bevorderend aan Adobe Experience Manager (AEM) 6.5 LTS ](https://experienceleague.adobe.com/en/docs/experience-manager-65-lts/content/implementing/deploying/upgrading/upgrade).

****Eerste vereisten****

Voordat u het Experience Manager Guides 5.1.0-upgradeproces start, moet u controleren of:

1. Bijgewerkt naar Experience Manager Guides versie 4.6.3, 4.6.4, 5.0.0 of 5.0.0 Service Pack 1 en hun respectieve installatiestappen voltooien.
1. (Optioneel) Alle vertaaltaken zijn afgesloten.
1. Veranderde het logboekniveau in **INFO** voor `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` klasse en voeg deze logboeken in een nieuw logboekdossier toe, bijvoorbeeld, `logs/translation_upgrade.log`.

>[!NOTE]
>
> De nabewerking en indexering kunnen een paar uur duren. Wij adviseren u om het verbeteringsproces tijdens de off-piek uren te beginnen.

## Versie 5.1.0 installeren

1. Download 5.1.0 versiepakket van [ het Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installeer het pakket versie 5.1.0.
1. U kunt ervoor kiezen om de trigger te HIT om de upgradetaak voor de vertaalkaart te starten. Voor details, zie [ trekker van manuscript via een Servlet ](#enable-trigger-of-script-via-a-servlet) toelaten.

1. Nadat u de pakketinstallatie hebt voltooid, wacht u op het volgende bericht in de logbestanden:

   `Completed the post deployment setup script`

   Het bovenstaande bericht geeft aan dat alle installatiestappen zijn voltooid.

   Als u om het even welke volgende prefix van de FOUT ontmoet, rapporteer hen aan uw team van het klantensucces:

   - Fout tijdens een setupscript voor implementatie na plaatsing
   - Uitzondering tijdens het exporteren van de MAP voor vertaling
   - Kan vertaalkaart van v1 naar v2 voor eigenschap niet importeren
1. Upgrade de insteekmodule Zuurstofaansluiting die wordt vrijgegeven met versie 5.1.0 \(indien nodig\).
1. Wis de browsercache nadat u het pakket hebt geïnstalleerd.

## Nadat u versie 5.1.0 hebt geïnstalleerd

Nadat u Experience Manager Guides hebt geïnstalleerd, kunt u de verschillende configuraties samenvoegen die van toepassing zijn vanaf de nieuw geïnstalleerde versie tot aan uw installatie.

>[!NOTE]
>
> Het dampupdate-assetmodel kan worden aangepast. Dus als er aanpassingen zijn uitgevoerd, moeten we de aanpassingen en Experience Manager Guides synchroniseren in de werkkopie van het model.

1. **DAM het werkschema van de Activa van de Update \ (veranderingen \):**

1. URL openen:

   ```
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html 
   ```

1. Selecteer **DAM het werkschema van Activa van de Update**.
1. Selecteer **uitgeven**.
1. Als de **component van de Initiator van het Proces van 0} DXML {aanwezig is, zorg ervoor dat de aanpassingen worden gesynchroniseerd.**
1. Als de **component van de Initiator van het Proces van 0} DXML {ontbreekt, voer de volgende stappen uit om het op te nemen:**

1. Selecteer **component van het Tussenvoegsel** \ (Verantwoordelijk voor Experience Manager Guides post-verwerking als definitieve stap in het proces \).
1. Vorm de **stap van het Proces** met hieronder details:

   **Gemeenschappelijke lusje**

   **Titel:** DXML de Initiator van het Proces van het Post

   **Beschrijving**: De stap van de initiator van het postproces DXML die een slingerbaan voor DXML post-verwerking van het gewijzigde/gecreeerde element zal teweegbrengen

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
   - Alle componenten die worden overschreven door/libs/fmditor/libsc, moeten worden vergeleken met de nieuwe productcode en updates moeten worden uitgevoerd in overlay bestanden onder/apps.
   - Alle clientlibcategorieën die worden gebruikt van het product, dienen te worden gecontroleerd op wijzigingen. Overschreven configuraties \(voorbeelden verderop\) moeten worden vergeleken met de nieuwste configuraties om de nieuwste functies te krijgen:
   - elementmapping.xml
   - ui\_config.json\(kan zijn ingesteld in mapprofielen\)
   - modified `com.adobe.fmdita.config.ConfigManager`

1. Als u aanpassingen hebt toegevoegd in damAssetLucene, kan het nodig zijn deze opnieuw toe te passen. Nadat u deze wijzigingen hebt aangebracht, stelt u de index in op true. Hierdoor worden alle bestaande knooppunten opnieuw gecompileerd met de aanpassingen. Nadat de rendex-markering is voltooid, wordt deze weer op false ingesteld. Dit kan een paar uur duren, afhankelijk van het aantal elementen in het systeem.

## Stappen om de Experience Manager Guides-indexen opnieuw te indexeren

1. Open `crx/de` en navigeer naar het indexpad: `/oak:index/guidesAssetProperties`
2. Plaats het herindexbezit als `true` (`false` door gebrek) en klik **sparen allen**.
3. Zodra de redex volledig is, wordt de redex-eigenschap opnieuw ingesteld op `false` en wordt de redex-telling met 1 verhoogd.

   >[!NOTE]
   >
   > Dit kan een paar minuten duren, afhankelijk van de hoeveelheid gegevens die aanwezig is.
4. Voer dezelfde stappen uit voor andere toegevoegde of gewijzigde indexen: `guidesBulkActivation`, `guidesPeerLinkIndex` en `guidesKonnectTemplateIndex` .

## Stappen om de bestaande inhoud te indexeren



Voer de volgende stappen uit om de bestaande inhoud te indexeren:

- Voer een POST-aanvraag uit op de server \(met correcte verificatie\) - `http://<server:port\>/bin/guides/map-find/indexing` . (Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd || Voorbeeld: `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

- De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(bijvoorbeeld: ` http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

- Zodra de taak is voltooid, reageert het bovenstaande GET-verzoek met succes en vermeldt het of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.


>[!NOTE]
>
> Als u het douaneschema gebruikt, moet u de weg van de dossiers van douane DTD en XSD catalog.xml in de bewaarplaats van AEM in **bepalen integreer Catalogi** optie.




## Stappen voor het afhandelen van het `'fmdita rewriter'` -conflict

Experience Manager Guides heeft de module van de a [**douane die herschrijver**](../cs-install-guide/conf-output-generation.md#custom-rewriter) voor de behandeling van de verbindingen in het geval van dwars-kaarten (verbindingen tussen de onderwerpen van twee verschillende kaarten) worden geproduceerd.

Als u nog een aangepaste schrijfbewerking voor tekenreeksen in uw codebase hebt, gebruikt u een `'order'` -waarde groter dan 50, omdat Experience Manager Guides anders `'order'` 50 gebruikt.  Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer details, mening [ Output die pijplijnen herschrijft ](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Aangezien de waarde van `'order'` tijdens deze upgrade is gewijzigd van 1000 in 50, moet u eventueel de bestaande aangepaste rewriter samenvoegen met `'fmdita-rewriter'` .



## Stappen om de damAssetLucene opnieuw te indexeren

De indexdefinitie wordt bijgewerkt voor damAssetLucene met gidsen. Verwijs naar [ dit artikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-16460) voor het opnieuw indexeren van damAssetLucene na bevordering aan versie 5.1.0.

>[!NOTE]
>
> Terwijl het volgen van de documentatie ervoor zorgt beide eigenschappen (reindex=true en redex-async=true voor /oak :index/damAssetLucene) gelijktijdig via sparen verrichting worden bijgewerkt.



**Bovenliggend onderwerp:** [ Download en installeer ](download-install.md)
