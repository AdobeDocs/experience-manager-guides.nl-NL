---
title: Een gegevensbronaansluiting configureren
description: Leer hoe te om een gegevensbronschakelaar te vormen
exl-id: 6e01098b-53fe-41e0-bffe-9ad056d4a9b3
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Een gegevensbronaansluiting configureren

AEM Guides biedt kant-en-klare connectors voor JIRA-, SQL- (MySQL, PostgreSQL, Microsoft SQL Server, SQLite, MariaDB, H2DB), AdobeCommerce- en Elasticsearch-databases. U kunt andere schakelaars ook toevoegen door de standaardinterfaces uit te breiden. De volgende configuratie helpt u om de diverse gegevensbronnen gemakkelijk toe te voegen. Zodra toegevoegd, kunt u de gegevensbronnen in de Redacteur van het Web bekijken.

Voer de volgende stappen uit om een gegevensbronschakelaar te vormen en dan het van de Redacteur van het Web te gebruiken:

## Een connector configureren

U kunt een out-of-the-box schakelaar vormen door een JSON dossier te uploaden. U kunt de volgende dossiers van de steekproefopstelling aan opstellingsschakelaars voor JIRA, SQL (MySQL, PostgreSQL, de Server van Microsoft SQL, SQLite, MariaDB, H2DB), de gegevensbestanden van AdobeCommerce, en Elasticsearch gebruiken.

Een voorbeeldinstellingenbestand voor de basisverificatie van Jira met gebruikersnaam en wachtwoord:

```
{
    "connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.rest.JiraConnector",
    "configName": "Jira",
    "templateFolders": ["/content/dam/dita-templates/konnect/jira"],
    "connectionConfig": {
        "configClazz": "com.adobe.guides.konnect.definitions.ootb.config.rest.BasicAuthUserNamePasswordRestConfig",
        "configData": {
            "username": "jirausername",
            "password": "jirapassword",
            "url": "https://jira.corp.adobe.com/rest/api/latest/search"
        }
    }
}
```

Sla het bestand bijvoorbeeld op als `jira.json` .

Een voorbeeldinstellingenbestand voor de basisverificatie van Jira met token:

```
{
    "connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.rest.JiraConnector",
    "configName": "Jira",
    "templateFolders": ["/content/dam/dita-templates/konnect/jira"],
    "connectionConfig": {
        "configClazz": "com.adobe.guides.konnect.definitions.ootb.config.rest.BasicAuthTokenRestConfig",
        "configData": {
            "token": "jiraauthtoken",
            "url": "https://jira.corp.adobe.com/rest/api/latest/search"
        }
    }
}
```

Sla het bestand bijvoorbeeld op als `jira.json` .

Een voorbeeldinstellingenbestand voor de basisverificatie van Jira met het token dat het trefwoord &quot;Basic&quot; bevat:

```
{
    "connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.rest.JiraConnector",
    "configName": "Jira",
    "templateFolders": ["/content/dam/dita-templates/konnect/jira"],
    "connectionConfig": {
        "configClazz": "com.adobe.guides.konnect.definitions.ootb.config.rest.BasicAuthTokenRestConfig",
        "configData": {
            "token": "Basic jiraauthtoken",
            "url": "https://jira.corp.adobe.com/rest/api/latest/search"
        }
    }
}
```

Sla het bestand bijvoorbeeld op als `jira.json` .

Een voorbeeldinstellingenbestand voor de basisverificatie van MySql:

```
{
    "connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.sql.MySqlConnector",
    "configName": "MySQL",
    "templateFolders": ["/content/dam/dita-templates/konnect/sql"],
    "connectionConfig": {
        "configClazz": "com.adobe.guides.konnect.definitions.ootb.config.sql.UserPassSqlConfig",
        "configData": {
            "username": "admin",
            "password": "admin",
            "driver": "com.mysql.jdbc.Driver",
            "connectionString": "jdbc:mysql://host.corp.adobe.com:3306/plm"
        }
    }
}
```

Sla het bestand bijvoorbeeld op als `mysql.json` .

Een voorbeeldinstellingenbestand voor de basisverificatie van PostgreSQL:

```
{
    "connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.sql.PostgreSqlConnector",
    "configName": "PostgreSQL",
    "templateFolders": ["/content/dam/dita-templates/konnect/sql"],
    "connectionConfig": {
        "configClazz": "com.adobe.guides.konnect.definitions.ootb.config.sql.UserPassSqlConfig",
        "configData": {
            "username": "admin",
            "password": "admin",
            "driver": "org.postgresql.Driver",
            "connectionString": "jdbc:postgresql://host:port/database"
        }
    }
}
```

Sla het bestand bijvoorbeeld op als `postgres.json` .

Een voorbeeld van een installatiebestand voor de basisverificatie van Microsoft SQL Server:

```
{
    "connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.sql.MsSqlServerConnector",
    "configName": "MSSQLServer",
    "templateFolders": ["/content/dam/dita-templates/konnect/sql"],
    "connectionConfig": {
        "configClazz": "com.adobe.guides.konnect.definitions.ootb.config.sql.UserPassSqlConfig",
        "configData": {
            "username": "admin",
            "password": "admin",
            "driver": "com.microsoft.sqlserver.jdbc.SQLServerDriver",
            "connectionString": "jdbc:sqlserver://10.10.10.10\\SQLEXPRESS01:1433;database=TutorialDB;encrypt=false;trustServerCertificate=true"
        }
    }
}
```

Sla het bestand bijvoorbeeld op als `mssqlserver.json` .

Een voorbeeldinstellingenbestand voor de basisverificatie van SQLite:

```
{
    "connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.sql.SqliteConnector",
    "configName": "SQLiteServer",
    "templateFolders": ["/content/dam/dita-templates/konnect/sql"],
    "connectionConfig": {
        "configClazz": "com.adobe.guides.konnect.definitions.ootb.config.sql.UserPassSqlConfig",
        "configData": {
            "username": "admin",
            "password": "admin",
            "driver": "org.sqlite.JDBC",
            "connectionString": "jdbc:sqlite:sample.db"
        }
    }
}
```

Sla het bestand bijvoorbeeld op als `sqqlite.json` .



Een voorbeeldinstellingsbestand voor H2DB:

```
{
    "connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.sql.H2DBConnector",
    "configName": "H2DBConnector",
    "templateFolders": ["/content/dam/dita-templates/konnect/sql"],
    "connectionConfig": {
        "configClazz": "com.adobe.guides.konnect.definitions.ootb.config.sql.UserPassSqlConfig",
        "configData": {
            "username": "admin",
            "password": "admin",
            "driver": "org.h2.Driver",
            "connectionString": "jdbc:h2:file:D:/h2db/db"
        }
    }
}
```

Sla het bestand bijvoorbeeld op als `sqqlite.json` .



Een voorbeeldinstellingsbestand voor de basisverificatie van MariaDb:

```
{
    "connectorClazz": "com.adobe.guides.sample.konnect.connector.MariaDBConnector",
    "configName": "SampleMariaDbConnector",
    "templateFolders": ["/content/dam/dita-templates/konnect/sql"],
    "connectionConfig": {
        "configClazz": "com.adobe.guides.konnect.definitions.ootb.config.sql.UserPassSqlConfig",
        "configData": {
            "username": "admin",
            "password": "admin",
            "driver": "org.mariadb.jdbc.Driver",
            "connectionString": "jdbc:mariadb://no1010042073107.corp.adobe.com:3308/mysql"
        }
    }
}
```

Sla het bestand bijvoorbeeld op als `mariadb.json` .


Een voorbeeldinstellingenbestand voor basisverificatie van Elasticsearch:

```
{
    "connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.rest.ElasticsearchConnector",
    "configName": "SampleES",
    "templateFolders": ["/content/dam/dita-templates/konnect/sql"],
    "connectionConfig": {
        "configClazz": "com.adobe.guides.konnect.definitions.ootb.config.rest.BasicAuthUserNamePasswordRestConfig",
        "configData": {
            "username": "admin",
            "password": "admin",        
            "url": "https://testsearch-1370045986.us-east-1.bonsaisearch.net:443"   }
    }
}
```

Sla het bestand bijvoorbeeld op als `ES.json` .

De vraag voor Elastic Onderzoek zou de index en de vraag moeten omvatten:

```
{
"index": "kibana_sample_data_ecommerce",
"queryString":{
    "query": {
        "match_all": {}
    }
}
}
```



Een voorbeeldinstellingenbestand voor AdobeCommerce NoAuth:

```
{
    "connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.graphql.AdobeCommerceConnector",
    "configName": "SampleCommerce",
    "templateFolders": ["/content/dam/dita-templates/konnect"],
    "connectionConfig": {   "configClazz": "com.adobe.guides.konnect.definitions.ootb.config.rest.NoAuthRestConfig",
   "configData": {
               "url": "http://host/graphql"   
        }
    }
}
```

Sla het bestand bijvoorbeeld op als `commerce.json` .

### Een verbindingsconfiguratie aanpassen

Met AEM Guides kunt u bepaalde waarden in het configuratiebestand aanpassen aan de behoeften van de gebruiker.

| Eigenschapnaam | Beschrijving |
|---|---|
| configName | De gebruiker kan een configuratienaam specificeren helpen de schakelaar identificeren |
| templateFolders | Lijst met mappen waaruit sjablonen worden opgehaald |

Andere gebieden worden aangepast gebaseerd op de config klasse die wordt geselecteerd om de Schakelaar in werking te stellen.

## Het bestand uploaden naar een locatie in AEM

Upload het bestand naar een locatie in AEM Assets.

Bijvoorbeeld: `/content/dam/jira.json`

## Configuratie maken met REST API

U kunt de configuratie registreren met REST API. Voor meer details, bekijk *REST API om een sectie van de gegevensbronschakelaar* in de API Verwijzing voor Adobe Experience Manager Guides te registreren.

Zodra u de gegevensbron hebt gevormd, is de schakelaar vermeld onder het paneel van Gegevensbronnen in de Redacteur van het Web. U kunt dan met de gegevensbron verbinden en een inhoudsfragment opnemen in uw onderwerpen. Voor meer details, neemt de mening [ een inhoudsfragment van uw gegevensbron ](../user-guide/web-editor-content-snippet.md) op.
