---
title: Workflows configureren en aanpassen
description: Leer hoe u workflows kunt configureren en aanpassen
exl-id: 3be387b9-6ac2-4b61-afdf-fbe9d8b6cc1e
feature: Workflow Configuration
role: Admin
level: Experienced
source-git-commit: 439be49e8f4c8cfacb16679257352f4197574365
workflow-type: tm+mt
source-wordcount: '2126'
ht-degree: 0%

---

# Workflows configureren en aanpassen {#id181AI0OJ0RO}

Met workflows kunt u Adobe Experience Manager \(AEM\)-activiteiten automatiseren. Een werkstroom bestaat uit een reeks stappen die in een specifieke volgorde worden uitgevoerd. U kunt een afzonderlijke activiteit bepalen om op elke stap uit te voeren. U kunt bijvoorbeeld een e-mailbericht sturen naar alle revisoren in een groep wanneer een onderwerprevisie wordt gemaakt. U kunt ook een bericht naar de uitgever sturen wanneer een uitvoergeneratietaak is voltooid.

Zie voor meer informatie over workflows in AEM:

- [ het beheren van Werkschema&#39;s ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/workflows.html)

- Het toepassen van en het deelnemen aan werkschema&#39;s: [ Werkend met Werkschema&#39;s ](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/workflows.html).

- Creërend werkschemamodellen en het uitbreiden van werkschemamogelijkheden: [ het Ontwikkelen en het Uitbreiden van Werkschema&#39;s ](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/workflows.html).

- Het verbeteren van de prestaties van werkschema&#39;s die significante servermiddelen gebruiken: [ Gelijktijdige Verwerking van het Werkschema ](https://helpx.adobe.com/experience-manager/6-5/sites/deploying/using/configuring-performance.html#ConfiguringforPerformance).


De secties in dit onderwerp zullen u door diverse aanpassingen lopen die u in de standaardwerkschema&#39;s kunt maken die in AEM Guides worden verscheept.

## De revisiewerkstroom aanpassen {#id176NE0C00HS}

Het team van het inhoudauteurs van elke organisatie werkt op een specifieke manier om aan hun bedrijfsvereisten te voldoen. In sommige organisaties is er een toegewijde editor, terwijl een andere organisatie een geautomatiseerd systeem voor redactionele herziening had kunnen opzetten. In een organisatie kan bijvoorbeeld een typische ontwerp- en publicatieworkflow taken bevatten zoals taken die elke auteur uitvoert met ontwerpinhoud, die automatisch naar de revisoren worden doorgestuurd wanneer de revisie is voltooid en die naar de uitgever worden doorgestuurd om de definitieve uitvoer te genereren. In AEM kunnen activiteiten die u uitvoert op uw inhoud en middelen worden gecombineerd in de vorm van een proces en worden toegewezen aan een AEM-workflow. Voor meer informatie over werkschema&#39;s in AEM, zie [ het Beheer Werkstromen ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/workflows.html) in de documentatie van AEM.

Met AEM Guides kunt u de standaardrevisiewerkstroom aanpassen. U kunt de volgende vier aangepaste revisiegerelateerde processen gebruiken in combinatie met andere workflows voor ontwerpen of publiceren.

- **creeer Overzicht**: Dit proces bereidt de meta-gegevens voor die worden vereist om een overzichtstaak tot stand te brengen. Zo wordt bijvoorbeeld revisiemachtigingen toegewezen aan de revisoren, wordt de status van de onderwerpen ingesteld op onderwerpen die worden gecontroleerd, worden de tijdlijnen van de revisie ingesteld enzovoort. Van de vier processen, is dit het enige verplichte proces dat in uw douanewerkschema moet worden omvat. In uw werkstroom kunt u de andere drie processen opnemen of uitsluiten.

- **wijs de Taak van het Overzicht** toe: Dit proces leidt tot de overzichtstaak en verzendt het taakbericht naar de initiatiefnemer en de recensenten.

- **verzendt E-mail van het Overzicht**: Dit proces verzendt het overzicht e-mail naar de initiatiefnemer en de recensenten.

- **Baan van het Programma om Overzicht** te sluiten: Dit proces zorgt ervoor dat het revisieproces op het bereiken van de deadline voltooit.


Wanneer u een aangepaste revisiewerkstroom maakt, moet u eerst de vereiste metagegevens instellen die nodig zijn voor het revisieproces maken. Hiertoe kunt u een ECMA-script maken. Een voorbeeld van het ECMA-script dat de metagegevens toewijst, wordt hieronder gegeven voor zowel het onderwerp als de kaart.

**voor Onderwerp**

```json
var workflowdata=workItem.getWorkflowData();
workflowdata.getMetaDataMap().put("initiator","admin");
workflowdata.getMetaDataMap().put("operation","AEM_REVIEW");
workflowdata.getMetaDataMap().put("orgTopics","/content/dam/xml-solution/review.xml");
workflowdata.getMetaDataMap().put("payloadJson","{\"base\":\"/content/dam/xml-solution\",\"asset\":[\"/content/dam/xml-solution/review.xml\"],\"referrer\":\""}");
workflowdata.getMetaDataMap().put("deadline","2017-06-27T13:19:00.000+05:30");
workflowdata.getMetaDataMap().put("title","Review through custom workflow");
workflowdata.getMetaDataMap().put("description","Initiate this review process using the AEM workflow");
workflowdata.getMetaDataMap().put("assignee","user-one", "user-two");
workflowdata.getMetaDataMap().put("status","1");
workflowdata.getMetaDataMap().put("projectPath","/content/projects/review");
workflowdata.getMetaDataMap().put("startTime", System.currentTimeMillis());
workflowdata.getMetaDataMap().put("reviewType", "AEM");
workflowdata.getMetaDataMap().put("versionJson", "[{\"path\":\"GUID-ca6ae229-889a-4d98-a1c6-60b08a820bb3.dita\",\"review\":true,\"version\":\"1.0\",\"reviewers\":[\"projects-samplereviewproject-owner\"]}]");
workflowdata.getMetaDataMap().put("isDitamap","false");
workflowdata.getMetaDataMap().put("reviewVersion","3.0");
```

**voor Kaart**

```json
var workflowdata = workItem.getWorkflowData();
workflowdata.getMetaDataMap().put("initiator", "admin");
workflowdata.getMetaDataMap().put("operation", "AEM_REVIEW");
workflowdata.getMetaDataMap().put("orgTopics", "GUID-ae42f13c-7201-4453-9a3a-c87675a5868e.dita|GUID-28a6517b-1b62-4d3a-b7dc-0e823225b6a5.dita|GUID-dd699e10-118d-4f1b-bf19-7f1973092227.dita|");
var payloadJson = "{\"referrer\":\"\",\"rootMap\":\"GUID-17feb385-acf3-4113-b838-77b11fd6988d.ditamap\",\"asset\":[\"GUID-17feb385-acf3-4113-b838-77b11fd6988d.ditamap\"],\"base\":\"/content/dam\"}";
workflowdata.getMetaDataMap().put("payloadJson", payloadJson);
workflowdata.getMetaDataMap().put("deadline", "2047-06-27T13:19:00.000+05:30");
workflowdata.getMetaDataMap().put("title", "Review task via workflow with map");
workflowdata.getMetaDataMap().put("description", "Review task via workflow with map Description");
workflowdata.getMetaDataMap().put("assignee", "user-one");
workflowdata.getMetaDataMap().put("status", "1");
workflowdata.getMetaDataMap().put("projectPath", "/content/projects/review_project_via_workflow");
workflowdata.getMetaDataMap().put("startTime", new Date().getTime());
var versionJson = "[{\"path\":\"GUID-ae42f13c-7201-4453-9a3a-c87675a5868e.dita\",\"version\":\"1.0\",\"review\":true,\"reviewers\":[\"starling-regression-user\"]},{\"path\":\"GUID-28a6517b-1b62-4d3a-b7dc-0e823225b6a5.dita\",\"version\":\"1.0\",\"review\":true,\"reviewers\":[\"starling-regression-user\"]},{\"path\":\"GUID-dd699e10-118d-4f1b-bf19-7f1973092227.dita\",\"version\":\"1.0\",\"review\":true,\"reviewers\":[\"starling-regression-user\"]}]";
workflowdata.getMetaDataMap().put("versionJson", versionJson);
workflowdata.getMetaDataMap().put("notifyViaEmail", "true");
workflowdata.getMetaDataMap().put("allowAllReviewers", "false");
workflowdata.getMetaDataMap().put("isDitamap", "true");
workflowdata.getMetaDataMap().put("ditamap", "GUID-17feb385-acf3-4113-b838-77b11fd6988d.ditamap");
var ditamapHierarchy = "[{\"path\":\"GUID-17feb385-acf3-4113-b838-77b11fd6988d.ditamap\",\"items\":[{\"path\":\"GUID-db5787bb-5467-4dc3-b3e5-cfde562ee745.ditamap\",\"items\":[{\"path\":\"GUID-ae42f13c-7201-4453-9a3a-c87675a5868e.dita\",\"items\":[],\"title\":\"\"},{\"path\":\"GUID-28a6517b-1b62-4d3a-b7dc-0e823225b6a5.dita\",\"items\":[],\"title\":\"\"}],\"title\":\"\"},{\"path\":\"GUID-dd699e10-118d-4f1b-bf19-7f1973092227.dita\",\"items\":[],\"title\":\"\"}]}]";
workflowdata.getMetaDataMap().put("ditamapHierarchy", ditamapHierarchy);
workflowdata.getMetaDataMap().put("reviewVersion","3.0");
```

U kunt dit script maken in het knooppunt `/etc/workflows/scripts` . In de volgende tabel worden de eigenschappen beschreven die door dit ECMA-script worden toegewezen:

| Eigenschap | Type | Beschrijving |
|--------|----|-----------|
| `initiator` | String | Gebruikersnaam van de gebruiker die de revisietaak heeft gestart. |
| `operation` | String | Een statische waarde die is ingesteld als `AEM_REVIEW` . |
| `orgTopics` | String | Pad van de onderwerpen die worden gedeeld voor revisie. Geef meerdere onderwerpen op, gescheiden door komma&#39;s. |
| `payloadJson` | JSON-object | Specificeer de volgende waarden:<br> - `base`: weg van de ouderomslag die het onderwerp bevat dat voor overzicht wordt verzonden.<br> - `asset` : pad van het onderwerp dat ter controle is verzonden. <br> - `referrer` : laat het leeg. |
| `deadline` | String | Geef de tijd op in de notatie `yyyy-MM-dd'T'HH:mm:ss.SSSXXX` . |
| `title` | String | Voer een titel in voor de revisietaak. |
| `description` | String | Voer een beschrijving in voor de revisietaak. |
| `assignee` | String | Gebruikersnaam van de gebruikers naar wie u het onderwerp ter controle wilt verzenden. |
| `status` | Geheel | Een statische waarde ingesteld als 1. |
| `startTime` | Lang | Gebruik de functie `System.currentTimeMillis()` om de huidige systeemtijd op te halen. |
| `projectPath` | String | Pad van het revisieproject waaraan de toetsingstaak zal worden toegewezen, bijvoorbeeld: /content/projects/samplereviewproject. |
| `reviewType` | String | Statische waarde &quot;AEM&quot;. |
| `versionJson` | JSON-object | versionJson is een lijst van onderwerpen die in de revisie gaan waar elk onderwerpobject de volgende structuur heeft [ &quot;weg&quot;: &quot;/content/dam/1-topic.dita&quot;, &quot;versie&quot;: &quot;1.1&quot;, &quot;overzicht&quot;: waar, &quot;recensenten&quot;: [ &quot;projects-we_retail-editor&quot;] ] |
| `isDitamap` | Boolean | false/true |
| `ditamapHierarchy` | JSON-object | Als de kaart wordt verzonden voor overzicht dan zou de waarde hier als moeten zijn:[ { &quot;weg&quot;: &quot;GUID-f0df1513-fe07-473f-9960-477d4df29c87.ditamap&quot;, &quot;punten&quot; GUID [ &quot;weg&quot;: &quot;-97 47e8ab-8cf1-45dd-9e20-d47d482f667d.dita&quot;, &quot;title&quot;: &quot;&quot;, &quot;items&quot;: [] } ] &rbrace; ]. |
| `ditamap` | String | Het pad opgeven van de tijdelijke aanduiding van de revisietaak |
| `allowAllReviewers` | Boolean | false/true |
| `notifyViaEmail` | Boolean | false/true |
| `reviewVersion` | String | Geeft de huidige versie van de revisieworkflow op. De standaardwaarde wordt ingesteld op `3.0` .<br> om de nieuwe eigenschappen van het overzichtswerkschema voor [ Auteurs ](../user-guide/review-close-review-task.md) en [ Reviewers ](../user-guide/review-complete-review-tasks.md) toe te laten, zorg ervoor dat `reviewVersion` aan `3.0` wordt geplaatst. |


Nadat u het script hebt gemaakt, roept u het aan voordat u het revisieproces maken in uw workflow oproept. Afhankelijk van uw vereisten kunt u vervolgens de andere revisiewerkstroomprocessen aanroepen.

### De revisiewerkstroom verwijderen uit de zuiveringsconfiguratie

Om de prestaties van de workflow-engine te verbeteren, kunt u regelmatig voltooide workflowexemplaren uit de AEM-opslagplaats wissen. Als u de standaard AEM-configuraties gebruikt, worden alle voltooide workflowinstanties na een bepaalde periode opgeschoond. Dit leidt er ook toe dat alle workflows voor revisie worden gewist uit de AEM-opslagplaats.

U kunt voorkomen dat revisiewerkstromen automatisch worden gewist door het model \(informatie\) van de revisiewerkstroom te verwijderen uit de configuratie voor automatisch leegmaken. U moet de **Configuratie van de Wrijving van het Werkschema van Adobe Granite** gebruiken om de modellen van het overzichtswerkschema uit auto-zuiverende lijst te verwijderen.

In de **Configuratie van de Woorden van het Werkschema van Adobe Granite**, zorg ervoor dat u minstens één werkschema een lijst maakt dat u veilig kunt zuiveren. U kunt bijvoorbeeld de volgende workflows gebruiken die door AEM Guides zijn gemaakt:

- /etc/workflow/models/publishditamap/jcr:content/model
- /etc/workflow/models/post-dita-project-creation-tasks/ jcr:content/model

Toevoegend een werkschema in de **Configuratie van de Woorden van het Werkschema van Adobe Granite** zorgt ervoor dat AEM slechts die werkschema&#39;s zuivert die in de configuratie vermeld zijn. Zo voorkomt u dat AEM de informatie over de revisiewerkstroom opschoont.

Voor meer details over het vormen van de **Configuratie van de Woorden van het Werkschema van Adobe Granite**, zie *het Beheer van de Instanties van het Werkschema* in de documentatie van AEM.

### E-mail- en AEM-meldingen aanpassen

Een aantal AEM Guides-workflows maakt gebruik van e-mailmeldingen. Als u bijvoorbeeld een revisietaak start, wordt een e-mailmelding verzonden naar de revisoren. Om ervoor te zorgen dat het e-mailbericht wordt verzonden, moet u deze functionaliteit echter in AEM inschakelen. Om e-mailbericht in AEM toe te laten, zie het artikel [ Vormend E-mailbericht ](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=en) in de documentatie van AEM.

AEM Guides bevat een set e-mailberichten en AEM-berichten die u kunt aanpassen. Voer de volgende stappen uit om deze meldingen aan te passen:

1. Gebruik Pakketbeheer om de map `/libs/fmdita/mail/review` te downloaden.

   >[!NOTE]
   >
   > Breng geen aanpassingen aan in de standaardconfiguratiebestanden in het knooppunt ``libs`` . U moet een overlay van het knooppunt ``libs`` in het knooppunt ``apps`` maken en de vereiste bestanden alleen in het knooppunt ``apps`` bijwerken.

1. De map `review` bevat de volgende submappen:

   - `aem-notification`
   - `CSS`
   - `email-notification`

   De gedetailleerde beschrijving van deze submappen wordt hieronder uitgelegd:

   | Submappen controleren | Beschrijving |
   |-----------------|-----------|
   | `aem-notification` | Bevat verschillende AEM-berichttypen die kunnen worden aangepast. <br> `closed` <br> `content-updated` <br> `feedback-addressed` <br> `feedback-provided` <br> `requested` <br> `reviewer-removed` <br> `tag-mention` <br> In deze submappen bevinden zich `primary.vm` - en `secondary.vm` -bestanden waarmee u de AEM-berichttitel en -beschrijving kunt aanpassen. |
   | `CSS` | Bevat het bestand `email-notification.css` voor het aanpassen van de opmaak van e-mailmeldingen. |
   | `email-notification` | Bevat verschillende typen e-mailmeldingen die u kunt aanpassen. <br> `closed` <br> `content-updated` <br> `feedback-addressed` <br> `feedback-provided` <br> `requested` <br> `reviewer-removed` <br> `tag-mention` <br> In deze submappen bevinden zich `primary.vm` - en `secondary.vm` -bestanden waarmee u het onderwerp en de hoofdtekst van de e-mailmelding kunt aanpassen. |

De definitie van elk meldingstype wordt hieronder beschreven:

- `closed`: activeert wanneer een revisietaak wordt gesloten.
- `content-updated`: activeert wanneer een auteur of aanvrager de inhoud bijwerkt.
- `feedback-addressed`: activeert wanneer de auteur of aanvrager de opmerkingen behandelt en een revisie aanvraagt bij de Revisor.
- `feedback-provided` Triggers wanneer Reviewer de taak als voltooid markeert door opmerkingen op taakniveau te leveren aan de auteur of initiator van de revisietaak.
- `requested`: activeert wanneer een auteur of aanvrager een revisietaak maakt.
- `reviewer-removed`: activeert wanneer een revisor niet is toegewezen aan de revisietaak.
- `tag-mention`: activeert wanneer een gebruiker wordt genoemd of gelabeld in revisieopmerkingen.

Zorg tijdens het aanpassen van een e-mail- of AEM-melding dat u alleen de volgende vooraf gedefinieerde set variabelen gebruikt die in `primary.vm` - en `secondary.vm` -bestanden worden gebruikt.


| **naam van Variabele** | **Beschrijving** | **Type van Gegevens** |
|-------------------------|---------------------------------------------------------------|---------------|
| `projectPath` | Pad naar het project met de overzichtstaak | String |
| `reviewTitle` | Titel van de toetsingstaak | String |
| `projectName` | Naam van het project | String |
| `commentator` | Naam van de gebruiker die een opmerking heeft toegevoegd | String |
| `commentExcerpt` | Fragment van de toegevoegde opmerking | String |
| `taskLink` | Directe koppeling naar de revisietaak | URL |
| `authorName` | Naam van de auteur die de revisietaak heeft gemaakt of bijgewerkt | String |
| `dueDate` | Vervaldatum van de toetsingstaak | Datum |
| `reviewerName` | Naam van de controleur die aan de taak is toegewezen | String |
| `user` | Gebruiker die is betrokken bij de revisietaak, zoals Auteur, Reviewer of zelfs Beheerder. | String |
| `recipient` | Specifieke gebruiker die de melding ontvangt | String |


## Workflow voor het genereren na uitvoer aanpassen {#id17A6GI004Y4}

AEM Guides biedt u de flexibiliteit om een workflow voor het genereren van producten na de uitvoer op te geven. U kunt sommige naverwerkingstaken uitvoeren op de uitvoer die met AEM Guides wordt gegenereerd. U kunt bijvoorbeeld bepaalde CQ-tags toepassen op de gegenereerde AEM Site-uitvoer of bepaalde eigenschappen instellen voor de PDF-uitvoer, of u kunt een e-mail naar een set gebruikers sturen zodra de uitvoer is gegenereerd.

U kunt een nieuw workflowmodel maken dat u kunt gebruiken als workflow voor het genereren van producten na de uitvoer. Wanneer een productiewerkstroom na de uitvoer wordt geactiveerd, deelt de werkstroom voor het genereren van de uitvoer contextafhankelijke informatie via de metagegevenskaart van de werkstroom, die u kunt gebruiken om de verwerking op de gegenereerde uitvoer uit te voeren. In de volgende tabel worden de contextuele gegevens beschreven die als metagegevens worden gedeeld:

| Eigenschap | Type | Beschrijving |
|--------|----|-----------|
| ``outputName`` | String | Naam van de uitvoervoorinstelling die wordt gebruikt om de uitvoer te genereren. |
| `generatedPath` | String | Pad in DAM waar de gegenereerde uitvoer wordt opgeslagen. |
| `outputType` | com.adobe.fmdita.output.OutputType | Type uitvoervoorinstelling. |
| `outputTitle` | String | Titel van de uitvoervoorinstelling. |
| `outputHistoryPath` | String | Pad naar opslagplaats van het historieknooppunt. |
| `isSuccess` | Boolean | Een vlag die de definitieve status van het productieproces van de output toont - succes of mislukking. |
| `logPath` | String | Pad in DAM waar de logbestanden voor het genereren van de uitvoer worden opgeslagen. |
| `generatedTime` | Lang | Tijdstip waarop het productieproces van de output werd teweeggebracht. |
| `initiator` | String | De gebruikers-id van de gebruiker die de workflow voor het genereren van de uitvoer heeft geactiveerd. |

Als u de metagegevens voor de uitvoergeneratie wilt gebruiken, kunt u een ECMA-script of een OSGi-bundel maken. Hieronder ziet u een voorbeeld van het ECMA-script dat de metagegevens gebruikt:

>[!NOTE]
>
> U kunt dit script maken in het knooppunt ``/etc/workflows/scripts`` .

```json
var session = workflowSession.getSession(); // Obtain session object to read/write the repository.
var payload = workItem.getWorkflowData().getPayload().toString(); // Get the workflow payload (the ditamap file on which the generation was triggered)
var metadata = workItem.getWorkflowData().getMetaDataMap(); // Get the workflow metadata object
var generatedPath = metadata.get("generatedPath"); // supplied by AEM Guides
var username = metadata.get("initiator"); // supplied by AEM Guides
var successful = metadata.get("isSuccess"); // supplied by AEM Guides
var title = metadata.get("outputTitle"); // supplied by AEM Guides
var subject = "Output Generation Finished";
var message = "Generation of output " + title + " just finished " + 
(successful ? "successfully. " : "unsuccessfully. ");
    message += "It was triggered by " + username;    
if (successful) {
    message += "<br/><br/>The path to the generated output is " + 
generatedPath;
}
/*
    MailerAPI.sendMail("dl-docs-authors", subject, message);
*/
```

Nadat u het script hebt gemaakt, roept u het aangepaste script in uw workflow aan. Afhankelijk van uw vereisten kunt u vervolgens de andere workflowprocessen aanroepen. Zodra u uw douanewerkschema hebt ontworpen, roep *Finalize Post Generation* als laatste stap in uw werkschemaproces. De *voltooit PostGeneratie* stap zorgt ervoor dat het statuut van de taak van de outputgeneratie aan *wordt bijgewerkt die* op voltooiing van het proces van de outputgeneratie wordt voltooid. Nadat u een aangepaste workflow voor het genereren van na de uitvoer hebt gemaakt, kunt u deze configureren met al uw voorinstellingen voor het genereren van uitvoer. Selecteer het vereiste werkschema in het *bezit van het Werkschema van de Post van de Generatie van de Looppas* van vereiste vooraf ingesteld. Wanneer u een taak van de outputgeneratie gebruikend de gevormde output vooraf instelt in werking stelt, verandert de taakstatus \ (in het lusje \ van de Output) in *post-Verwerking*.

## Workflow voor bijwerken van middelen aanpassen {#id18C3D0I0B5Z}

Door gebrek, teweegbrengt het *DAM de werkschema van de Activa van de Update* teweeg wanneer u creeert of om het even welke Activa \ van AEM (XML of niet-XML \) bijwerkt. Bijvoorbeeld, wanneer u een onderwerp creeert of het bijwerkt, wordt het *DAM werkschema van de Activa van de Update* uitgevoerd. Het *DAM werkschema van de Activa van de Update* probeert om relevante meta-gegevens uit Assets te halen. Het uit-van-doos *Werkschema van de Update van Activa* heeft geen stappen om het even welke relevante meta-gegevens uit een DITA- dossier te halen en het *DAM werkschema van de Activa van de Update* produceert veel logboeken op het tijdstip van uitvoering. Als u extra logboeken wilt vermijden, kunt u het werkschema vormen om alle dossiers van XML van verwerking over te slaan.

Voer de volgende stappen uit om het *DAM werkschema van de Activa van de Update* aan te passen:

1. open de **pagina van de Lanceertoestellen van het Werkschema**.

   De standaard-URL voor toegang tot de pagina Workflowopstartpers is:

   ```http
   http://<server name>:<port>/libs/cq/workflow/admin/console/content/launchers.html
   ```

1. Van de lijst van werkschemalanceerders, open de eigenschappen van het **DAM werkschema van de Activa van de Update**.

1. Voeg een voorwaarde toe met de volgende expressie:

   ```json
   jcr:content/metadata/dc:format!=application/xml
   ```

1. Klik **sparen &amp; Sluiten**


## XML-workflow na verwerking configureren {#id18CJB03J0Y4}

AEM Guides maakt een aantal workflows waarmee u in AEM kunt werken met DITA-inhoud. Er zijn bijvoorbeeld workflows die worden uitgevoerd wanneer u DITA-inhoud uploadt of bestaande inhoud bijwerkt. Deze workflows parseren DITA-documenten en voeren verschillende taken uit, zoals het instellen van de metagegevens, het toevoegen van standaarduitvoervoorinstellingen aan nieuwe DITA-kaarten en andere gerelateerde taken.

>[!NOTE]
>
> Om de standaard post-verwerkingswerkschema&#39;s aan te passen of uit te breiden, kunt u de post-verwerkende gebeurtenismanager gebruiken die in de *API verwijzing voor Adobe Experience Manager Guides* wordt beschreven.

De volgende eigenschappen bepalen hoe AEM Guides de naverwerkingsworkflows uitvoert:

>[!NOTE]
>
> De volgende eigenschappen zijn toegankelijk via de webconsole: http://&lt;servernaam\>:&lt;poort\>/system/console/configMgr.

| Eigenschap | Bundnaam | Beschrijving |
|--------|-----------|-----------|
| Dynamische voorkeuren | `com.adobe.fmdita.postprocess.PostProcessObservation` | Voor alle dossiers waarop de naverwerking niet is uitgevoerd, wint het de uitgaande verwijzingen terug door de onderwerpdossiers te ontleden. Aanbevolen wordt deze optie niet in te schakelen omdat het systeem overbelast kan worden als het aantal te verwerken bestanden groot is. |
| Threads na verwerking | `com.adobe.fmdita.config.ConfigManager` | Hiermee stelt u het aantal naverwerkingsthreads in dat moet worden gebruikt voor de naverwerkingsworkflow. <br> de standaardwaarde is 1. |
