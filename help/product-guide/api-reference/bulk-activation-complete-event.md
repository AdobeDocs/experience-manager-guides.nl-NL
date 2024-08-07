---
title: Bulkactivering voltooid, gebeurtenishandler
description: Meer informatie over de volledige gebeurtenishandler voor bulkactivering
feature: Bulk Activation Event Handler
role: Developer
level: Experienced
exl-id: 08b153d7-3d13-4804-9e3e-38790dbea1f3
source-git-commit: 9b8971bf7065a94a2e42669094249c822c555718
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Bulkactivering voltooid, gebeurtenishandler

Experience Manager Guides maakt de gebeurtenis `com/adobe/fmdita/replication/complete` beschikbaar die wordt gebruikt om bewerkingen uit te voeren nadat een bulkactiveringsproces is voltooid. Deze gebeurtenis wordt geactiveerd wanneer een bulkactiveringsproces wordt voltooid. Als u bijvoorbeeld de bulkactivering van een AEM sitevoorinstelling van een kaart uitvoert, wordt deze gebeurtenis aangeroepen nadat het activeringsproces is beëindigd.

U moet een AEM gebeurtenishandler maken om de eigenschappen te lezen die beschikbaar zijn in deze gebeurtenis en verdere verwerking uit te voeren.

De gebeurtenisdetails worden hieronder uitgelegd:

**naam van de Gebeurtenis**:

```
com/adobe/fmdita/replication/complete 
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| `path` | String | Het pad van het bestand dat deze gebeurtenis heeft geactiveerd. <br> Bijvoorbeeld `/content/output/sites/ditamap1-ditamap` . <br> Het is een lijst met paden die als een JSON-array zijn geserialiseerd. |
| `messageType` | String | Het type van een bericht. <br> Mogelijke optie: `REPLICATION` |
| `action` | String | Dit is de uitgevoerde actie. <br> Mogelijke optie: `BulkReplicate` |
| `user` | String | De gebruiker die de bewerking heeft gestart. |
| `result` | String | Het resultaat van de activering van het selectievakje Bulk. Het is een JSON-object met serienummering: <br>`{"success":boolean,"code":integer,"message":"" }` |
| `agentId` | String | AgentId die in de replicatie wordt gebruikt. Bijvoorbeeld `"publish"` . |
| `importMode` | String | Importmodus die wordt gebruikt bij activering. De mogelijke opties zijn: <br>`REPLACE, MERGE, UPDATE`. |


**de Listener van de Gebeurtenis van de Steekproef**:

```XML
@Component(service = EventHandler.class,
        immediate = true,
        property = {
                EventConstants.EVENT_TOPIC + "=" + "com/adobe/fmdita/replication/complete",
        })
 
public class SampleEventHandler implements EventHandler {
 
    protected final Logger log = LoggerFactory.getLogger(this.getClass());
 
    @Override
    public void handleEvent(final Event event) {
        Map<String, String> properties = new HashMap<>();
        properties.put("paths", (String) event.getProperty("paths"));
        properties.put("messageType", (String) event.getProperty("messageType"));
        properties.put("action", (String) event.getProperty("action"));
        properties.put("result", (String) event.getProperty("result"));
        properties.put("user", (String) event.getProperty("user"));
        properties.put("agentId", (String) event.getProperty("agentId"));
        properties.put("importMode", (String) event.getProperty("importMode"));
 
        String eventTopic = event.getTopic();
        log.debug("eventTopic {}", eventTopic);
        for(Map.Entry entry:properties.entrySet()) {
            log.debug(entry.getKey() + " : " + entry.getValue());
        }
 
    }
}
```
