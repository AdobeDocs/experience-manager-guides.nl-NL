---
title: Bestaande DITA-inhoud uploaden
description: Leer hoe u bestaande DITA-inhoud kunt uploaden
exl-id: 1dde8a29-301f-461e-b598-2a8cab61bf3d
feature: Migration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 0%

---

# Bestaande DITA-inhoud uploaden {#id176FF000JUI}

U hebt waarschijnlijk een opslagplaats voor bestaande DITA-inhoud die u met AEM Guides wilt gebruiken. Voor dergelijke bestaande inhoud kunt u de volgende methoden gebruiken om uw inhoud in bulk te uploaden naar de AEM opslagplaats.

## Een WebDAV-hulpprogramma gebruiken

Als u uw onderwerpen en kaarten in een andere redacteur ontwerpt DITA, kunt u om het even welk hulpmiddel gebruiken WebDAV om uw dossiers te uploaden. De procedure die in deze sectie wordt gegeven gebruikt WinSCP als hulpmiddel WebDAV om inhoud te uploaden.

Voer de volgende stappen uit om WinSCP te gebruiken om dossiers te uploaden:

1. Download en installeer WinSCP op uw computer.

1. Start de WinSCP-app.

   Het dialoogvenster Aanmelden wordt weergegeven.

1. Voor de Login dialoog, specificeer een Nieuwe Plaats die door WebDAV als **Protocol van het Dossier** te kiezen en andere verbindingsdetails zoals te verstrekken:

   - de URL waar uw AEM server wordt gehost,

   - het poortnummer \(standaardwaarde is 4502\), en

   - de gebruikersnaam en het wachtwoord om toegang te krijgen tot uw AEM.

1. Klik **Login**.

   Bij een geslaagde verbinding wordt de inhoud van AEM Assets weergegeven in de WinSCP-gebruikersinterface. U kunt gemakkelijk doorbladeren, tot stand brengen, bijwerken, of schrapping inhoud gebruikend WinSCP dossierontdekkingsreiziger.


## FrameMaker gebruiken

Adobe FrameMaker wordt geleverd met een krachtige AEM-aansluiting waarmee u uw bestaande DITA en andere FrameMaker documenten \(.book en .fm\) eenvoudig kunt uploaden naar AEM. U kunt verschillende functies voor het uploaden van bestanden gebruiken, zoals het uploaden van één bestand, het uploaden van een volledige map met of zonder afhankelijkheden \(zoals inhoudsverwijzingen, kruisverwijzingen en afbeeldingen\).

Voer de volgende stappen uit om de Verbinding van de FrameMaker AEM te gebruiken om inhoud te uploaden:

1. Start de FrameMaker.

1. Open de **dialoog van de Manager van de Verbinding**.

   ![](assets/fm-aem-connector.png){width="550" align="left"}

1. Voer de volgende gegevens in om verbinding te maken met de AEM opslagplaats:

   - **Naam**: Ga een beschrijvende naam in om de verbinding aan uw AEM server te identificeren.
   - **Server**: Ga URL en havenaantal van uw AEM server in.

   - **Naam van de Gebruiker**/ **Wachtwoord**: Ga de gebruikersnaam en het wachtwoord in om tot de AEM server toegang te hebben.

1. Klik **verbinden**.

   Zodra de verbinding tot stand is gebracht, wordt Assets van de AEM weergegeven in het venster Repository Manager.

   ![](assets/fm-repo-manager.png){width="550" align="left"}

   Als u met de rechtermuisknop op een bestand of map klikt, kunt u gerelateerde bewerkingen uitvoeren. Als u bijvoorbeeld met de rechtermuisknop op een map klikt, hebt u opties om een bestand te uploaden, een bestand met afhankelijkheden te uploaden, een volledige map te uploaden enzovoort.


## Patroon UUID-bestandsnaam configureren

Wanneer u inhoud importeert, is het niet nodig dat de bestandsnamen worden gebaseerd op de UUID. In een systeem dat op UUID-Gebaseerde dossiernamen gebruikt, is het verplicht dat alle dossiers worden bedoeld gebruikend hun UUIDs eerder dan hun originele dossiernamen. Als een geïmporteerd bestand geen op UUID gebaseerde bestandsnamen heeft, kunt u het systeem zo configureren dat een UUID wordt toegevoegd aan de eigenschap file. Deze UUID wordt vervolgens gebruikt om te verwijzen naar bestanden waarin UUID niet wordt gebruikt voor het benoemen van de bestanden.

Voer de volgende stappen uit om bestandsnamen te controleren op basis van een UUID-patroon en UUID toe te wijzen aan bestanden waaraan geen UUID is toegewezen:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op *com.adobe.fmdita.config.ConfigManager* bundel.

1. In het **bezit van de Patronen van Filename 0&rbrace; UUID &lbrace;, specificeer een patroon om de namen van het ingevoerde dossier te controleren.**

   Als een bestand het opgegeven patroon niet volgt, wordt een UUID toegevoegd aan de eigenschap van het bestand en worden alle verwijzingen naar het bestand bijgewerkt met de UUID die aan het bestand is toegewezen.

1. Klik **sparen**.


## Inhoud uploaden met UUID met een WebDav-gereedschap {#id201MI0I04Y4}

U kunt de volgende methoden gebruiken om uw inhoud te uploaden met UUID:

- Sleep inhoud van uw lokale systeem.
- Gebruik **creeer** \> **3&rbrace; werkschema van Dossiers van AEM Assets UI van.**
- Gebruik een gereedschap zoals WinSCP.

In het geval dat u een hulpmiddel zoals WinSCP gebruikt, kunt u de actie bepalen om op een dubbel dossier uit te voeren door het **oude dossier van de Beweging met Zelfde UUID aan Nieuwe Omslag** optie in configMgr te plaatsen. Met deze optie wordt gedefinieerd welke actie wordt uitgevoerd op een bestand dat op een andere locatie in de AEM opslagplaats beschikbaar is. Dit het plaatsen is beschikbaar in *com.adobe.fmdita.config.ConfigManager* bundel in configMgr.

Door gebrek wordt het **oude dossier van de Beweging met Zelfde UUID aan Nieuwe Omslag** optie aangezet. Dit houdt in dat wanneer het bestand dat wordt geüpload aanwezig is in een andere map in de opslagplaats, het bestaande bestand wordt verplaatst naar de huidige locatie en wordt overschreven door het bestand dat wordt geüpload. Als u deze optie niet selecteert, wordt het bestand op de bestaande locatie overschreven.

**extra nota&#39;s bij het werken met op UUID-Gebaseerde dossiers**:

De volgende punten moeten in overweging worden genomen bij het verplaatsen of kopiëren van inhoud binnen de AEM opslagplaats:

- Wanneer een of meer bestanden van de ene naar de andere locatie worden gekopieerd, wordt een nieuwe UUID gegenereerd voor bestanden zonder UUID. Deze UUID wordt toegevoegd aan de metagegevens van het bestand.

- Als een bestand een conflict heeft of een duplicaat heeft, wordt een unieke bestandsnaam gegenereerd voor het nieuwe bestand dat wordt gekopieerd of verplaatst.

- Geen twee bestanden kunnen dezelfde UUID hebben. Er wordt een unieke UID toegewezen aan alle nieuwe bestanden.


De volgende punten moeten in overweging worden genomen bij het verplaatsen of kopiëren van inhoud van uw lokale systeem naar de AEM opslagplaats:

- Als een bestand door twee verschillende gebruikers tegelijk wordt geüpload, wordt het eerdere bestand overschreven door het bestand dat later wordt verwerkt. Een dergelijke praktijk komt echter zelden voor en moet worden vermeden.

- Wanneer u inhoud uitcheckt in de AEM opslagplaats en wijzigingen aanbrengt in uw lokale systeem, moet u ervoor zorgen dat de bestandsnaam niet wordt gewijzigd op het moment dat het bestand wordt geüpload.


## Krullopdrachten gebruiken

U kunt ook curl-opdrachten gebruiken om een map in DAM te maken, bestanden te uploaden en metagegevens toe te voegen aan de geüploade inhoud.

**creeer een omslag**

Voer de volgende opdracht uit om een map in AEM opslagplaats te maken:

```curl
curl --user <username>:<password> --data jcr:primaryType=sling:Folder "<server folder path>"
```

Geef de volgende parameters op om een map te maken:

- `<username>:<passowrd>`: Geef de gebruikersnaam en het wachtwoord op voor toegang tot de AEM. Deze gebruiker moet over de rechten voor het maken van mappen beschikken.

- `jcr:primaryType=sling:Folder`: Specificeer deze parameter *zoals* is om een middel van het omslagtype tot stand te brengen.

- `<server folder path>`: Volledig mappad inclusief de naam van de nieuwe map die u wilt maken in de AEM. Als u bijvoorbeeld het pad opgeeft als `http://192.168.1.1:4502/content/dam/projects/AEM-Guides` , wordt de map `AEM-Guides` gemaakt in de map `projects` in DAM.


**upload een dossier**

Voer de volgende opdracht uit om een bestand te uploaden in de AEM opslagplaats:

```curl
curl --user <username>:<password> -T "<local file path>" "<server folder path>"
```

Geef de volgende parameters op om een bestand te uploaden:

- `<username>:<passowrd>`: Geef de gebruikersnaam en het wachtwoord op voor toegang tot de AEM. Deze gebruiker moet schrijfrechten hebben op de `server folder path` .

- ``local file path``: volledig bestandspad op uw lokale systeem dat u wilt uploaden.

- `<server folder path>`: Voltooi het mappad op de AEM server waar u het bestand wilt uploaden.


**voeg meta-gegevens** toe

Voer de volgende opdracht uit om metagegevens toe te voegen aan een bestand:

```curl
curl --user <username>:<password> -F<attribute name>=<value> <metadata node path>
```

Geef de volgende parameters op om metagegevensinformatie toe te voegen:

- `<username>:<passowrd>`: Geef de gebruikersnaam en het wachtwoord op voor toegang tot de AEM. Deze gebruiker moet schrijfrechten hebben op de ``metadata node path`` .

- ``-F<attribute name>=<value>``: `<attribute name>` is de naam van het metagegevenskenmerk, zoals `audience` en `<value>` zou kunnen zijn `internal` . U kunt meerdere naam-waardeparen voor kenmerken opgeven, gescheiden door spatie.

- `<metadata node path>`: volledig mappad, inclusief bestandsnaam en het bijbehorende metagegevensknooppunt. Als u bijvoorbeeld het pad opgeeft als `http://192.168.1.1:4502/content/dam/projects/AEM-Guides/intro.xml/jcr:content/metadata` , wordt de opgegeven metagegevens ingesteld in het `intro.xml` -bestand.


**Bovenliggend onderwerp:**&#x200B;[ Migreer bestaande inhoud ](migrate-content.md)
