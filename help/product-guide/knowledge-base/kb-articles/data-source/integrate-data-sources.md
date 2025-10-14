---
title: Architectuur van de integratie van externe gegevensbronnen in AEM Guides
description: Leer over de architectuur van de Externe Integratie van Gegevensbronnen in AEM Guides.
source-git-commit: b0cf652023770eda24ea27ff105ed6dc2cdd1f08
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Integratie van externe gegevensbronnen

Gegevens van externe systemen kunnen eenvoudig in uw Experience Manager Guides-instantie worden geïntegreerd. Door verbinding te maken met externe gegevensbronnen kunt u de functionaliteit en bruikbaarheid van uw contentbeheersysteem aanzienlijk verbeteren.


U kunt gegevens efficiënt verbinden en halen uit externe bronnen gebruikend gegevensintegratie. Met deze functie hoeft u niet afhankelijk te zijn van het IT-team om de gegevens te verkrijgen en deze vervolgens handmatig te kopiëren en plakken of de wijzigingen in het externe systeem voortdurend bij te werken.

Deze functie zorgt voor synchronisatie met de oorspronkelijke bron en maakt het mogelijk de documentatie op harmonieuze wijze bij te werken zonder dat er handmatige kopieer- en plakbewerkingen nodig zijn. Het helpt ook de gegevensconsistentie tussen Experience Manager Guides en de externe gegevensbron te handhaven.

Nadat u de inhoud van externe gegevensbronnen hebt opgehaald, kunt u deze bovendien in DITA-indeling maken en de geïntegreerde inhoud opnieuw gebruiken.


## Gegevensbronintegratieframework

Het integratiekader van een gegevensbron omvat hoofdzakelijk twee belangrijke componenten: de externe gegevensbronnen en hun integratie in Experience Manager Guides-instantie.

### Externe gegevensbronnen

U kunt als volgt verbinding maken met Experience Manager Guides:

- Relationele databases (RDBMS)
   - PostSQL, MySQL, Microsoft SQL Server, MariaDB en SQLite
- Niet-relationele databases
   - MongoDB, Apache Cassandra, Apache CouchDB en Redis
- Product Information Management (PIM) / Product Lifecycle Management (PLM)
   - Pimcore, Salsify, Akeneo en Informatica
- Productbeheersystemen
   - JIRA en Microsoft Azure DevOps Boards (ADO)
- Online Analytical Processing (OLAP) en Analytics Systems

### Integratie in Experience Manager Guides



Via een geverifieerde connector worden gegevens overgebracht van een extern systeem en worden gegevens gegenereerd in Experience Manager Guides.
![Architectuur](assets/konnect-architecture.png)


### Integratie in Experience Manager Guides

Voer de volgende stappen uit om de inhoud in Experience Manager Guides te integreren:

1. **Opstelling de gegevensbronschakelaar**
   - De gegevensbronschakelaar dient als interface om connectiviteit met de externe gegevensbronnen te vestigen. U moet de connector configureren om de verbinding tot stand te brengen en de verificatiemethoden, zoals `Basic Auth` of `API key Auth` , op te nemen. Alle configuratiedetails, met inbegrip van gecodeerde informatie, worden veilig opgeslagen in Adobe Experience Manager.
   - De schakelaarlaag wordt ontworpen om uitbreidbaar te zijn, toestaand u om uw implementaties tot stand te brengen voor het verbinden met diverse systemen die niet uit-van-de-doos door Experience Manager Guides worden verstrekt.

     ![&#x200B; Laag van de Schakelaar &#x200B;](assets/data-source-connector-layer.jpg)
   >[!NOTE]
   >
   > Open de definitiemodule Konnect en implementeer de connectorinterface om een aangepaste connector te maken. Leer meer over hoe te [&#x200B; vormen de schakelaars van de douanegegevensbron &#x200B;](./conf-custom-data-source-connector.md).

1. **pas de malplaatjes van de Snelheid** aan

   - Experience Manager Guides biedt ondersteuning voor Snelheid (https://velocity.apache.org/), een uiterst robuuste sjabloonengine waarmee u de gegevens van JSON-bestanden kunt omzetten in DITA-inhoud. De snelheid biedt de flexibiliteit om door structuren te navigeren JSON met om het even welk niveau van het nesten.
   - In het volgende voorbeeld ziet u hoe u snelheidssjablonen en gegevens van Jira kunt integreren om moeiteloos tabellen of geordende lijsten te genereren.
      - Jira Response

        ```
        {
            "expand": "schema,names",
            "total": 5,
            "hostname": "https://jira.corp.adobe.com",
            "maxResults": "200",
            "issues": [
                {
                    "key": "DXML-12756",
                    "fields": {
                        "description": "Implement the snippet generator in External Data Source integration",
                        "summary": "Implement the snippet generator in External Data Source integration"
                    }
                },
                {
                    "key": "DXML-12755",
                    "fields": {
                        "description": "Implement the topic generator in External Data Source integration",
                        "summary": "Implement the topic generator in External Data Source integration"
                    }
                },
                {
                    "key": "DXML-12745",
                    "fields": {
                        "description": "Implement the ability to register a new connector",
                        "summary": "Implement the ability to register a new connector"
                    }
                }
            ],
            "startAt": 0
        }
        ```

      - Sjablonen

        ![&#x200B; het Sjablonen Motor &#x200B;](assets/data-source-TemplatingEngine.png){width="800" align="left"}
      - Gegevens gegenereerd uit dezelfde gegevensbron maar met verschillende sjablonen

        ![&#x200B; Gegenereerde Gegevens &#x200B;](assets/data-source-templates-topics.png){width="800" align="left"}

1. **produceer inhoud gebruikend de malplaatjes**
   - U kunt de inhoud genereren op basis van de sjablonen die u hebt gemaakt.
   - U kunt verschillende typen inhoud genereren:
      - Fragment: dit is eenmalige bruikbare inhoud. U kunt de gegevens van de schakelaar in het bepaalde malplaatje produceren en dan het inbedden in de gewenste markering.
      - DITA Onderwerp: Produceer diverse onderwerpen om te gebruiken zoals in inhoud is of kan als a *Herbruikbare Component* worden opnieuw gebruikt.
      - DITA Onderwerp + Kaart: U kunt een volledige kaart ook produceren kan met het onderwerp en dan de gegevens voor het publiceren direct gebruiken of het gebruiken als a *Herbruikbare Component* in andere gegevens.


1. **Publish de geïntegreerde inhoud**
   - Publiceren is de OOTB-functie van Experience Manager Guides en u kunt rechtstreeks alle gegevens publiceren die door het externe systeem zijn gegenereerd als PDF- of AEM Site-uitvoer.

>[!MORELIKETHIS]
>
> De volgende documenten verstrekken meer details bij het vormen van de schakelaars en het gebruiken van hen in uw instantie.
> - [&#x200B; vorm een gegevensbronschakelaar &#x200B;](../../../install-guide/conf-data-source-connector-tools.md)
> - [&#x200B; produceer inhoud gebruikend fragmenten of onderwerpen &#x200B;](../../../user-guide/web-editor-content-snippet.md)