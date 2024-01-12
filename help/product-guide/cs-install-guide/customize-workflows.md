---
title: Workflows configureren en aanpassen
description: Leer hoe u workflows kunt configureren en aanpassen
exl-id: a5742082-cc0b-49d9-9921-d0da1b272ea5
feature: Workflow Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '1362'
ht-degree: 0%

---

# Workflows configureren en aanpassen {#id181AI0OJ0RO}

Met workflows kunt u Adobe Experience Manager \(AEM\)-activiteiten automatiseren. Een werkstroom bestaat uit een reeks stappen die in een specifieke volgorde worden uitgevoerd. U kunt een afzonderlijke activiteit bepalen om op elke stap uit te voeren. U kunt bijvoorbeeld een e-mailbericht sturen naar alle revisoren in een groep wanneer een onderwerprevisie wordt gemaakt. U kunt ook een bericht naar de uitgever sturen wanneer een uitvoergeneratietaak is voltooid.

Zie voor meer informatie over workflows in AEM:

- [Workflowinstanties beheren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/workflows-administering.html)

- Workflows toepassen en deelnemen aan workflows: [Werken met projectworkflows](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/projects/workflows.html).


De secties in dit onderwerp zullen u door diverse aanpassingen lopen die u in de standaardwerkschema&#39;s kunt maken die in de Gidsen van de AEM worden verscheept.

## De revisiewerkstroom aanpassen {#id176NE0C00HS}

Het team van het inhoudauteurs van elke organisatie werkt op een specifieke manier om aan hun bedrijfsvereisten te voldoen. In sommige organisaties is er een toegewijde editor, terwijl een andere organisatie een geautomatiseerd systeem voor redactionele herziening had kunnen opzetten. In een organisatie kan bijvoorbeeld een typische ontwerp- en publicatieworkflow taken bevatten zoals taken die elke auteur uitvoert met ontwerpinhoud, die automatisch naar de revisoren worden doorgestuurd wanneer de revisie is voltooid en die naar de uitgever worden doorgestuurd om de definitieve uitvoer te genereren. In AEM, kunnen de activiteiten die u op uw inhoud en activa doet in de vorm van een proces worden gecombineerd en aan een AEM werkschema in kaart gebracht. Zie voor meer informatie over workflows in AEM [Workflows beheren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/workflows-administering.html) in AEM documentatie.

Met AEM hulplijnen kunt u de standaardrevisieworkflow aanpassen. U kunt de volgende vier aangepaste revisiegerelateerde processen gebruiken in combinatie met andere workflows voor ontwerpen of publiceren.

- **Revisie maken**: Tijdens dit proces worden de vereiste metagegevens voorbereid voor het maken van een controletaak. Zo wordt bijvoorbeeld revisiemachtigingen toegewezen aan de revisoren, wordt de status van de onderwerpen ingesteld op onderwerpen die worden gecontroleerd, worden de tijdlijnen van de revisie ingesteld enzovoort. Van de vier processen, is dit het enige verplichte proces dat in uw douanewerkschema moet worden omvat. In uw werkstroom kunt u de andere drie processen opnemen of uitsluiten.

- **Revisietaak toewijzen**: Tijdens dit proces wordt de revisietaak gemaakt en wordt het taakbericht naar de aanvrager en revisoren verzonden.

- **Revisie-e-mail verzenden**: Tijdens dit proces wordt de e-mail met de revisie naar de aanvrager en de controleurs verzonden.

- **Taak plannen om revisie te sluiten**: Dit proces zorgt ervoor dat het evaluatieproces wordt voltooid wanneer de deadline wordt bereikt.


Wanneer u een aangepaste revisiewerkstroom maakt, moet u eerst de vereiste metagegevens instellen die nodig zijn voor het revisieproces maken. Hiertoe kunt u een ECMA-script maken. Hieronder ziet u een voorbeeld van het ECMA-script dat de metagegevens toewijst:

```javascript
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

U kunt dit script maken in het dialoogvenster `/etc/workflows/scripts` knooppunt. In de volgende tabel worden de eigenschappen beschreven die door dit ECMA-script worden toegewezen:

| Eigenschap | Type | Beschrijving |
|--------|----|-----------|
| `initiator` | String | Gebruikersnaam van de gebruiker die de revisietaak heeft gestart. |
| `operation` | String | Een statische waarde die is ingesteld als `AEM_REVIEW`. |
| `orgTopics` | String | Pad van de onderwerpen die worden gedeeld voor revisie. Geef meerdere onderwerpen op, gescheiden door komma&#39;s. |
| `payloadJson` | JSON-object | Geef de volgende waarden op: -   `base`: pad van de bovenliggende map met het onderwerp dat ter controle is verzonden. <br> -   `asset`: pad van het onderwerp dat ter controle is verzonden. <br> -   `referrer`: laat het leeg. |
| `deadline` | String | Geef de tijd op in `yyyy-MM-dd'T'HH:mm:ss.SSSXXX` gebruiken. |
| `title` | String | Voer een titel in voor de revisietaak. |
| `description` | String | Voer een beschrijving in voor de revisietaak. |
| `assignee` | String | Gebruikersnaam van de gebruikers naar wie u het onderwerp ter controle wilt verzenden. |
| `status` | Geheel | Een statische waarde ingesteld als 1. |
| `startTime` | Lang | Gebruik de `System.currentTimeMillis()` om de huidige systeemtijd op te halen. |

Nadat u het script hebt gemaakt, roept u het aan voordat u het revisieproces maken in uw workflow oproept. Afhankelijk van uw vereisten kunt u vervolgens de andere revisiewerkstroomprocessen aanroepen.

### De revisiewerkstroom verwijderen uit de zuiveringsconfiguratie

Om de prestaties van de workflow-engine te verbeteren, kunt u regelmatig voltooide workflowexemplaren uit de AEM opslagplaats verwijderen. Als u de standaard AEM configuraties gebruikt, worden alle voltooide workflowinstanties na een bepaalde periode opgeschoond. Dit leidt er ook toe dat alle workflows van de revisie uit de AEM opslagplaats worden verwijderd.

U kunt voorkomen dat revisiewerkstromen automatisch worden gewist door het model \(informatie\) van de revisiewerkstroom te verwijderen uit de configuratie voor automatisch leegmaken. U moet de opdracht **Configuratie van opschonen van de Adobe van Granite-workflow** om de modellen van de revisiewerkstroom te verwijderen uit de lijst voor automatisch leegmaken.

In de **Configuratie van opschonen van de Adobe van Granite-workflow**, zorgt u ervoor dat u ten minste één workflow opsomt die u veilig kunt leegmaken. U kunt bijvoorbeeld de volgende workflows gebruiken die zijn gemaakt met AEM hulplijnen:

- /etc/workflow/models/publishditamap/jcr:content/model
- /etc/workflow/models/post-dita-project-creation-tasks/jcr:content/model

Een workflow toevoegen in het dialoogvenster **Configuratie van opschonen van de Adobe van Granite-workflow** zorgt ervoor dat AEM alleen die workflows leegmaakt die in de configuratie worden vermeld. Zo voorkomt u dat AEM de informatie over de revisiewerkstroom leegmaakt.

Voor meer informatie over het configureren van de **Configuratie van opschonen van de Adobe van Granite-workflow**, zie *Workflowinstanties beheren* in AEM documentatie.

### E-mailsjablonen aanpassen

In een aantal workflows van AEM hulplijnen worden e-mailmeldingen gebruikt. Als u bijvoorbeeld een revisietaak start, wordt een e-mailmelding verzonden naar de revisoren. Als u er echter voor wilt zorgen dat het e-mailbericht wordt verzonden, moet u deze functie in AEM inschakelen. Raadpleeg het artikel als u e-mailmeldingen in AEM wilt inschakelen [E-mail verzenden](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#sending-email) in AEM documentatie.

De AEM bevatten een set e-mailsjablonen die u kunt aanpassen. Voer de volgende stappen uit om deze sjablonen aan te passen:

1. Gebruik Package Manager om te downloaden `/libs/fmdita/mail` bestand.

   >[!NOTE]
   >
   > Breng geen aanpassingen aan in de standaardconfiguratiebestanden in het dialoogvenster ``libs`` knooppunt. U moet een bedekking maken van de ``libs`` knooppunt in de ``apps`` de vereiste bestanden in de ``apps`` alleen knooppunt.

1. De e-mailmap bevat de volgende aanpasbare sjablonen:

   | Naam sjabloonbestand | Beschrijving |
   |-----------------|-----------|
   | closereview.html | Deze e-mailsjabloon wordt gebruikt wanneer een revisietaak wordt gesloten. |
   | createreview.html | Deze e-mailsjabloon wordt gebruikt wanneer een nieuwe revisietaak wordt gemaakt. |
   | reviewapproval.css | Dit CSS-bestand bevat de opmaak van e-mailsjablonen. |


## Workflow voor het genereren na uitvoer aanpassen {#id17A6GI004Y4}

Met AEM hulplijnen kunt u een workflow voor het genereren van producten na de uitvoer opgeven. U kunt sommige naverwerkingstaken op de output uitvoeren die gebruikend de Gidsen van de AEM wordt geproduceerd. U kunt bijvoorbeeld bepaalde CQ-tags toepassen op de gegenereerde AEM Site-uitvoer of bepaalde eigenschappen instellen voor de PDF-uitvoer, of u kunt een e-mailbericht naar een set gebruikers sturen zodra de uitvoer is gegenereerd.

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
> U kunt dit script maken in het dialoogvenster ``/etc/workflows/scripts`` knooppunt.

```javascript
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

Nadat u het script hebt gemaakt, roept u het aangepaste script in uw workflow aan. Afhankelijk van uw vereisten kunt u vervolgens de andere workflowprocessen aanroepen. Nadat u de aangepaste workflow hebt ontworpen, roept u de *Post Generation voltooien* als de laatste stap in het workflowproces. De *Post Generation voltooien* stap zorgt ervoor dat de status van de uitvoergeneratietaak wordt bijgewerkt naar *Voltooid* na voltooiing van het productieproces. Nadat u een aangepaste workflow voor het genereren van na de uitvoer hebt gemaakt, kunt u deze configureren met al uw voorinstellingen voor het genereren van uitvoer. Selecteer de vereiste workflow in het dialoogvenster *Workflow na generatie uitvoeren* eigenschap van de vereiste voorinstelling. Wanneer u een uitvoergeneratietaak uitvoert met behulp van de geconfigureerde uitvoervoorinstelling, verandert de taakstatus \(op het tabblad Uitvoer\) in *Nabewerking*.
