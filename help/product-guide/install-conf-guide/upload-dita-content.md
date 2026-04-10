---
title: Bestaande DITA-inhoud uploaden
description: Leer hoe u bestaande DITA-inhoud in Experience Manager Guides kunt uploaden met WebDAV en FrameMaker
feature: Migration
role: Admin
level: Experienced
source-git-commit: 834959a6a0e22cd5d2b2c5d0e57ceb6d45c0c666
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 0%

---

# Bestaande DITA-inhoud uploaden met WebDAV en FrameMaker for On-Premise

U hebt waarschijnlijk een opslagplaats voor bestaande DITA-inhoud die u met AEM Guides wilt gebruiken. Voor dergelijke bestaande inhoud kunt u de volgende methoden gebruiken om uw inhoud in bulk te uploaden naar de AEM-opslagplaats.

- [Een WebDAV-hulpprogramma gebruiken](#use-a-webdav-tool)
- [FrameMaker gebruiken](#use-framemaker)

## Een WebDAV-hulpprogramma gebruiken

Als u uw onderwerpen en kaarten in een andere redacteur ontwerpt DITA, kunt u om het even welk hulpmiddel gebruiken WebDAV om uw dossiers te uploaden. De procedure die in deze sectie wordt gegeven gebruikt WinSCP als hulpmiddel WebDAV om inhoud te uploaden.

Voer de volgende stappen uit om WinSCP te gebruiken om dossiers te uploaden:

1. Download en installeer WinSCP op uw computer.

1. Start de WinSCP-app.

   Het dialoogvenster Aanmelden wordt weergegeven.

1. Voor de Login dialoog, specificeer een Nieuwe Plaats die door WebDAV als **Protocol van het Dossier** te kiezen en andere verbindingsdetails zoals te verstrekken:

   - de URL waar uw AEM-server wordt gehost,

   - het poortnummer `\(default is 4502\)` en

   - de gebruikersnaam en het wachtwoord voor toegang tot uw AEM-server.

1. Selecteer **Login**.

   Bij een geslaagde verbinding wordt de inhoud van AEM Assets weergegeven in de WinSCP-gebruikersinterface. U kunt gemakkelijk doorbladeren, tot stand brengen, bijwerken, of schrapping inhoud gebruikend WinSCP dossierontdekkingsreiziger.

## Inhoud uploaden met UUID met een WebDav-gereedschap {#id201MI0I04Y4}

U kunt de volgende methoden gebruiken om uw inhoud te uploaden met UUID:

- Sleep inhoud van uw lokale systeem.
- Gebruik **creeer** \> **&#x200B;**&#x200B;werkschema van Dossiers van de UI van Assets van AEM.
- Gebruik een gereedschap zoals WinSCP.

In het geval dat u een hulpmiddel zoals WinSCP gebruikt, kunt u de actie bepalen om op een dubbel dossier uit te voeren door het **oude dossier van de Beweging met Zelfde UUID aan Nieuwe Omslag** optie in configMgr te plaatsen. Met deze optie wordt gedefinieerd welke actie wordt uitgevoerd op een bestand dat op een andere locatie in de AEM-opslagplaats beschikbaar is. Deze instelling is beschikbaar in de `*com.adobe.fmdita.config.ConfigManager*` -bundel in configMgr.

Door gebrek wordt het **oude dossier van de Beweging met Zelfde UUID aan Nieuwe Omslag** optie aangezet. Dit houdt in dat wanneer het bestand dat wordt geüpload aanwezig is in een andere map in de opslagplaats, het bestaande bestand wordt verplaatst naar de huidige locatie en wordt overschreven door het bestand dat wordt geüpload. Als u deze optie niet selecteert, wordt het bestand op de bestaande locatie overschreven.

**extra nota&#39;s bij het werken met op UUID-Gebaseerde dossiers**:

Bij het verplaatsen of kopiëren van inhoud in de AEM-opslagplaats moeten de volgende punten in overweging worden genomen:

- Wanneer een of meer bestanden van de ene naar de andere locatie worden gekopieerd, wordt een nieuwe UUID gegenereerd voor bestanden zonder UUID. Deze UUID wordt toegevoegd aan de metagegevens van het bestand.

- Als een bestand een conflict heeft of een duplicaat heeft, wordt een unieke bestandsnaam gegenereerd voor het nieuwe bestand dat wordt gekopieerd of verplaatst.

- Geen twee bestanden kunnen dezelfde UUID hebben. Er wordt een unieke UID toegewezen aan alle nieuwe bestanden.


Bij het verplaatsen of kopiëren van inhoud van uw lokale systeem naar de AEM-opslagplaats moet rekening worden gehouden met de volgende punten:

- Als een bestand door twee verschillende gebruikers tegelijk wordt geüpload, wordt het eerdere bestand overschreven door het bestand dat later wordt verwerkt. Een dergelijke praktijk komt echter zelden voor en moet worden vermeden.

- Wanneer u inhoud uitcheckt in de AEM-opslagplaats en wijzigingen aanbrengt in uw lokale systeem, dient u ervoor te zorgen dat de bestandsnaam niet wordt gewijzigd op het moment dat het bestand wordt geüpload.

## FrameMaker gebruiken

Adobe FrameMaker wordt geleverd met een krachtige AEM-aansluiting waarmee u uw bestaande DITA en andere FrameMaker-documenten `\(.book and .fm\)` eenvoudig kunt uploaden naar AEM. U kunt verschillende functies voor het uploaden van bestanden gebruiken, zoals het uploaden van één bestand, het uploaden van een volledige map met of zonder afhankelijkheden \(zoals inhoudsverwijzingen, kruisverwijzingen en afbeeldingen\).

Voer de volgende stappen uit om FrameMaker AEM Connector te gebruiken om inhoud te uploaden:

1. Start FrameMaker.

1. Open de **dialoog van de Manager van de Verbinding**.

   ![](assets/fm-aem-connector.png){width="550" align="left"}

1. Voer de volgende gegevens in om verbinding te maken met de AEM-opslagplaats:

   - **Naam**: Ga een beschrijvende naam in om de verbinding aan uw server van AEM te identificeren.
   - **Server**: Ga URL en havenaantal van uw server van AEM in.

   - **Naam van de Gebruiker**/ **Wachtwoord**: Ga de gebruikersnaam en het wachtwoord in om tot de server van AEM toegang te hebben.

1. Selecteer **verbinden**.

   Zodra de verbinding tot stand is gebracht, wordt Assets van de AEM-opslagplaats weergegeven in het venster Repository Manager.

   ![](assets/fm-repo-manager.png){width="550" align="left"}

   Als u met de rechtermuisknop op een bestand of map klikt, kunt u gerelateerde bewerkingen uitvoeren. Als u bijvoorbeeld met de rechtermuisknop op een map klikt, hebt u opties om een bestand te uploaden, een bestand met afhankelijkheden te uploaden, een volledige map te uploaden enzovoort.






**Bovenliggend onderwerp:**&#x200B;[&#x200B; Migreer bestaande inhoud &#x200B;](migrate-content.md)
