---
title: Workflows configureren en aanpassen
description: Leer hoe u workflows kunt configureren en aanpassen
exl-id: 3be387b9-6ac2-4b61-afdf-fbe9d8b6cc1e
feature: Workflow Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '1744'
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

Het team van het inhoudauteurs van elke organisatie werkt op een specifieke manier om aan hun bedrijfsvereisten te voldoen. In sommige organisaties is er een toegewijde editor, terwijl een andere organisatie een geautomatiseerd systeem voor redactionele herziening had kunnen opzetten. In een organisatie kan bijvoorbeeld een typische ontwerp- en publicatieworkflow taken bevatten zoals taken die elke auteur uitvoert met ontwerpinhoud, die automatisch naar de revisoren worden doorgestuurd wanneer de revisie is voltooid en die naar de uitgever worden doorgestuurd om de definitieve uitvoer te genereren. In AEM, kunnen de activiteiten die u op uw inhoud en activa doet in de vorm van een proces worden gecombineerd en aan een AEM werkschema in kaart gebracht. Voor meer informatie over werkschema&#39;s in AEM, zie [ het Beheer Werkstromen ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/workflows.html) in AEM documentatie.

Met AEM Guides kunt u de standaardrevisiewerkstroom aanpassen. U kunt de volgende vier aangepaste revisiegerelateerde processen gebruiken in combinatie met andere workflows voor ontwerpen of publiceren.

- **creeer Overzicht**: Dit proces bereidt de meta-gegevens voor die worden vereist om een overzichtstaak tot stand te brengen. Zo wordt bijvoorbeeld revisiemachtigingen toegewezen aan de revisoren, wordt de status van de onderwerpen ingesteld op onderwerpen die worden gecontroleerd, worden de tijdlijnen van de revisie ingesteld enzovoort. Van de vier processen, is dit het enige verplichte proces dat in uw douanewerkschema moet worden omvat. In uw werkstroom kunt u de andere drie processen opnemen of uitsluiten.

- **wijs de Taak van het Overzicht** toe: Dit proces leidt tot de overzichtstaak en verzendt het taakbericht naar de initiatiefnemer en de recensenten.

- **verzendt E-mail van het Overzicht**: Dit proces verzendt het overzicht e-mail naar de initiatiefnemer en de recensenten.

- **Baan van het Programma om Overzicht** te sluiten: Dit proces zorgt ervoor dat het revisieproces op het bereiken van de deadline voltooit.


Wanneer u een aangepaste revisiewerkstroom maakt, moet u eerst de vereiste metagegevens instellen die nodig zijn voor het revisieproces maken. Hiertoe kunt u een ECMA-script maken. Hieronder ziet u een voorbeeld van het ECMA-script dat de metagegevens toewijst:

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

Nadat u het script hebt gemaakt, roept u het aan voordat u het revisieproces maken in uw workflow oproept. Afhankelijk van uw vereisten kunt u vervolgens de andere revisiewerkstroomprocessen aanroepen.

### De revisiewerkstroom verwijderen uit de zuiveringsconfiguratie

Om de prestaties van de workflow-engine te verbeteren, kunt u regelmatig voltooide workflowexemplaren uit de AEM opslagplaats verwijderen. Als u de standaard AEM configuraties gebruikt, worden alle voltooide workflowinstanties na een bepaalde periode opgeschoond. Dit leidt er ook toe dat alle workflows van de revisie uit de AEM opslagplaats worden verwijderd.

U kunt voorkomen dat revisiewerkstromen automatisch worden gewist door het model \(informatie\) van de revisiewerkstroom te verwijderen uit de configuratie voor automatisch leegmaken. U moet de **Configuratie van de Wrijving van het Werkschema van de Adobe gebruiken granite** om de modellen van het overzichtswerkschema uit auto-zuiverende lijst te verwijderen.

In de **Configuratie van de Wrijving van het Werkschema van de Adobe Granite**, zorg ervoor dat u minstens één werkschema een lijst maakt dat u veilig kunt zuiveren. U kunt bijvoorbeeld de volgende workflows gebruiken die door AEM Guides zijn gemaakt:

- /etc/workflow/models/publishditamap/jcr:content/model
- /etc/workflow/models/post-dita-project-creation-tasks/jcr:content/model

Toevoegend een werkschema in de **Configuratie van de Wrijving van het Werkschema van de Adobe Granite** zorgt ervoor dat AEM slechts die werkschema&#39;s zuivert die in de configuratie vermeld zijn. Zo voorkomt u dat AEM de informatie over de revisiewerkstroom leegmaakt.

Voor meer details over het vormen van de **Configuratie van de Wrijving van het Werkschema van de Adobe granite**, zie *het Beheer van de Instanties van het Werkschema* in AEM documentatie.

### E-mailsjablonen aanpassen

Een aantal AEM Guides-workflows maakt gebruik van e-mailmeldingen. Als u bijvoorbeeld een revisietaak start, wordt een e-mailmelding verzonden naar de revisoren. Als u er echter voor wilt zorgen dat het e-mailbericht wordt verzonden, moet u deze functie in AEM inschakelen. Om e-mailbericht in AEM toe te laten, zie het artikel [ Vormend E-mailbericht ](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=en) in AEM documentatie.

AEM Guides bevat een set e-mailsjablonen die u kunt aanpassen. Voer de volgende stappen uit om deze sjablonen aan te passen:

1. Meld u aan bij AEM en open de modus CRXDE Lite.

1. Ga op het tabblad Navigator naar de volgende locatie:

   `/libs/fmdita/mail`

   >[!NOTE]
   >
   > Breng geen aanpassingen aan in de standaardconfiguratiebestanden in het knooppunt ``libs`` . U moet een overlay van het knooppunt ``libs`` in het knooppunt ``apps`` maken en de vereiste bestanden alleen in het knooppunt ``apps`` bijwerken.

1. De e-mailmap bevat de volgende aanpasbare sjablonen:

   | Naam sjabloonbestand | Beschrijving |
   |-----------------|-----------|
   | closereview.html | Deze e-mailsjabloon wordt gebruikt wanneer een revisietaak wordt gesloten. |
   | createreview.html | Deze e-mailsjabloon wordt gebruikt wanneer een nieuwe revisietaak wordt gemaakt. |
   | reviewapproval.css | Dit CSS-bestand bevat de opmaak van e-mailsjablonen. |


## Workflow voor het genereren na uitvoer aanpassen {#id17A6GI004Y4}

AEM Guides biedt u de flexibiliteit om een workflow voor het genereren van producten na de uitvoer op te geven. U kunt sommige naverwerkingstaken uitvoeren op de uitvoer die met AEM Guides wordt gegenereerd. U kunt bijvoorbeeld bepaalde CQ-tags toepassen op de gegenereerde AEM Site-uitvoer of bepaalde eigenschappen instellen voor de PDF-uitvoer, of u kunt een e-mailbericht naar een set gebruikers sturen zodra de uitvoer is gegenereerd.

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

Nadat u het script hebt gemaakt, roept u het aangepaste script in uw workflow aan. Afhankelijk van uw vereisten kunt u vervolgens de andere workflowprocessen aanroepen. Zodra u uw douanewerkschema hebt ontworpen, roep *Finalize de Generatie van Post* als laatste stap in uw werkschemaproces. *voltooit de Generatie van Post* stap ervoor dat het statuut van de taak van de outputgeneratie aan *wordt bijgewerkt* op voltooiing van het proces van de outputgeneratie. Nadat u een aangepaste workflow voor het genereren van na de uitvoer hebt gemaakt, kunt u deze configureren met al uw voorinstellingen voor het genereren van uitvoer. Selecteer het vereiste werkschema in het *bezit van het Werkschema van de Generatie van Post van de Looppas* van vereiste vooraf ingesteld. Wanneer u een taak van de outputgeneratie gebruikend de gevormde output vooraf instelt in werking stelt, verandert de taakstatus \ (in het lusje \ van de Output) in *Post-Verwerking*.

## Workflow voor bijwerken van middelen aanpassen {#id18C3D0I0B5Z}

Door gebrek, teweegbrengt het *DAM de werkschema van de Activa van de Update* teweeg wanneer u creeert of om het even welk AEM Middel \ (XML of niet-XML \) bijwerkt. Bijvoorbeeld, wanneer u een onderwerp creeert of het bijwerkt, wordt het *DAM werkschema van de Activa van de Update* uitgevoerd. Het *DAM werkschema van de Activa van de Update* probeert om relevante meta-gegevens uit Assets te halen. Het uit-van-doos *Werkschema van de Update van Activa* heeft geen stappen om het even welke relevante meta-gegevens uit een DITA- dossier te halen en het *DAM werkschema van de Activa van de Update* produceert veel logboeken op het tijdstip van uitvoering. Als u extra logboeken wilt vermijden, kunt u het werkschema vormen om alle dossiers van XML van verwerking over te slaan.

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
| Post Process Threads | `com.adobe.fmdita.config.ConfigManager` | Hiermee stelt u het aantal naverwerkingsthreads in dat moet worden gebruikt voor de naverwerkingsworkflow. <br> de standaardwaarde is 1. |
