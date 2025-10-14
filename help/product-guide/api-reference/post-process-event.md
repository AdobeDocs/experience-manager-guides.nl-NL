---
title: Gebeurtenishandler voor nabewerking
description: Meer informatie over de gebeurtenishandler Nabewerking
exl-id: 3b105ff5-02d4-40e3-a713-206a7fcf18b2
feature: Post-Processing Event Handler
role: Developer
level: Experienced
source-git-commit: 8e57d4048f4aa13d7f77f25082d4e7aa329ee355
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Gebeurtenishandler voor nabewerking {#id175UB30E05Z}

## UUID en Cloud Service

Adobe Experience Manager Guides maakt de gebeurtenis `com/adobe/guides/postprocess/complete` beschikbaar die wordt gebruikt om naverwerkingen uit te voeren. Deze gebeurtenis wordt geactiveerd wanneer een bewerking op een DITA-bestand wordt uitgevoerd. De volgende bewerkingen op een DITA-bestand activeren deze gebeurtenis:

- Uploaden
- Maken
- Wijzigen

>[!NOTE]
>
> De gebeurtenis na verwerking wordt geactiveerd door de markering `fire.processing.events` in te schakelen. Dit is een configuratieparameter in `fmdita config manager` . Als deze optie is ingesteld op true, worden gebeurtenissen (com/adobe/guides/postprocess/complete) geactiveerd om de voltooiing van de naverwerking te volgen. De standaardwaarde is false (uitgeschakeld).

U moet een Adobe Experience Manager-gebeurtenishandler maken om de eigenschappen te lezen die beschikbaar zijn in deze gebeurtenis en verdere verwerking uit te voeren.

De gebeurtenisdetails worden hieronder uitgelegd:

**naam van de Gebeurtenis**:

```
com/adobe/guides/postprocess/complete 
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| `path` | String | Het pad van het bestand dat deze gebeurtenis heeft geactiveerd. Dit is doorgaans het bestand waarop een bewerking is uitgevoerd. |
| `eventType` | String | Het type gebeurtenis, dat wil zeggen CREATE of MODIFY. |
| `status` | String | De geretourneerde status voor de uitgevoerde bewerking. De mogelijke opties zijn: - <br> - SUCCESS: de naverwerkingbewerking is voltooid. <br> - MISLUKT: de naverwerkingbewerking is mislukt als gevolg van een fout. |
| `errorMsg` | String | Het foutbericht in het geval van een fout met de naverwerkingshandeling. |
| `uuid` | String | De UUID van het bestand dat deze gebeurtenis heeft geactiveerd. Dit is doorgaans het bestand waarop een bewerking is uitgevoerd. |

**de Listener van de Gebeurtenis van de Steekproef**


```
@Component(service = EventHandler.class,
        immediate = true,
        property = {
                EventConstants.EVENT_TOPIC + "=" + "com/adobe/guides/postprocess/complete",
        })
public class PostProcessCompleteEventHandler implements EventHandler {

    protected final Logger log = LoggerFactory.getLogger(this.getClass());

    @Override
    public void handleEvent(final Event event) {
        Set<String> propertyNames = new HashSet<>(Arrays.asList(event.getPropertyNames()));
        Map<String, String> properties = new HashMap<>();
        properties.put("path", (String) event.getProperty("path"));
        properties.put("eventType", (String) event.getProperty("eventType"));
        properties.put("status", (String) event.getProperty("status"));
        if(propertyNames.contains("errorMsg")) {
            properties.put("errorMsg", (String) event.getProperty("errorMsg"));
        }
        if (propertyNames.contains("uuid")) {
            properties.put("uuid", (String) event.getProperty("uuid"));
        }
        String eventTopic = event.getTopic();
        log.debug("eventTopic {}", eventTopic);
        for(Map.Entry entry:properties.entrySet()) {
            log.debug(entry.getKey() + " : " + entry.getValue());
        }
    }
}
```

## Niet-UID


Adobe Experience Manager Guides stelt de gebeurtenis com/adobe/fmdita/postprocess/complete beschikbaar die wordt gebruikt om naverwerkingen uit te voeren. Deze gebeurtenis wordt geactiveerd wanneer een bewerking op een DITA-bestand wordt uitgevoerd. De volgende bewerkingen op een DITA-bestand activeren deze gebeurtenis:

>[!NOTE]
>
> Deze gebeurtenis wordt niet geactiveerd voor het verwijderen in AEM 6.1.

- Uploaden
- Maken
- Wijziging
- Verwijderen

U moet een Adobe Experience Manager-gebeurtenishandler maken om de eigenschappen te lezen die beschikbaar zijn in deze gebeurtenis en verdere verwerking uit te voeren.

De gebeurtenisdetails worden hieronder uitgelegd:

**naam van de Gebeurtenis**:

```
com/adobe/fmdita/postprocess/complete 
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| `path` | String | Het pad van het bestand dat deze gebeurtenis heeft geactiveerd. Dit is doorgaans het bestand waarop een bewerking is uitgevoerd. |
| `status` | String | De geretourneerde status voor de uitgevoerde bewerking. De mogelijke opties zijn: - <br> - SUCCESS: de naverwerkingbewerking is voltooid. <br> - IS VOLTOOID MET FOUTEN: de naverwerkingsbewerking is voltooid, maar met enkele fouten. <br> - MISLUKT: de naverwerkingbewerking is mislukt als gevolg van een fout. |
| `message` | String | Als de status IS VOLTOOID MET FOUTEN of MISLUKT, bevat deze parameter de details over de fout of de oorzaak van de fout. |
| `operation` | String | De nabewerking die op het bestand is uitgevoerd. De mogelijke opties zijn:<br> - Toevoeging <br> - Bijwerken <br> - Verwijderen |
