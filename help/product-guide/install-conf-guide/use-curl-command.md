---
title: Krullopdrachten gebruiken
description: Leer hoe u curl-opdrachten kunt gebruiken voor de geüploade inhoud in Experience Manager Guides.
feature: Migration
role: Admin
level: Experienced
source-git-commit: 834959a6a0e22cd5d2b2c5d0e57ceb6d45c0c666
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Krullopdrachten gebruiken

U kunt ook curl-opdrachten gebruiken om een map in DAM te maken, bestanden te uploaden en metagegevens toe te voegen aan de geüploade inhoud.

## Een map maken

Voer de volgende opdracht uit om een map te maken in de AEM-opslagplaats:

```curl
curl --user <username>:<password> --data jcr:primaryType=sling:Folder "<server folder path>"
```

Geef de volgende parameters op om een map te maken:

- `<username>:<passowrd>`: Geef de gebruikersnaam en het wachtwoord op voor toegang tot de AEM-opslagplaats. Deze gebruiker moet over de rechten voor het maken van mappen beschikken.

- `jcr:primaryType=sling:Folder`: Specificeer deze parameter *zoals* is om een middel van het omslagtype tot stand te brengen.

- `<server folder path>`: Volledig mappad inclusief de naam van de nieuwe map die u wilt maken in de AEM-opslagplaats. Als u bijvoorbeeld het pad opgeeft als `http://192.168.1.1:4502/content/dam/projects/AEM-Guides` , wordt de map `AEM-Guides` gemaakt in de map `projects` in DAM.


## Een bestand uploaden

Voer de volgende opdracht uit om een bestand te uploaden in de AEM-opslagplaats:

```curl
curl --user <username>:<password> -T "<local file path>" "<server folder path>"
```

Geef de volgende parameters op om een bestand te uploaden:

- `<username>:<passowrd>`: Geef de gebruikersnaam en het wachtwoord op voor toegang tot de AEM-opslagplaats. Deze gebruiker moet schrijfrechten hebben op de `server folder path` .

- ``local file path``: volledig bestandspad op uw lokale systeem dat u wilt uploaden.

- `<server folder path>`: Voltooi het mappad op de AEM-server waar u het bestand wilt uploaden.


## Metagegevens toevoegen

Voer de volgende opdracht uit om metagegevens toe te voegen aan een bestand:

```curl
curl --user <username>:<password> -F<attribute name>=<value> <metadata node path>
```

Geef de volgende parameters op om metagegevensinformatie toe te voegen:

- `<username>:<passowrd>`: Geef de gebruikersnaam en het wachtwoord op voor toegang tot de AEM-opslagplaats. Deze gebruiker moet schrijfrechten hebben op de ``metadata node path`` .

- ``-F<attribute name>=<value>``: `<attribute name>` is de naam van het metagegevenskenmerk, zoals `audience` en `<value>` zou kunnen zijn `internal` . U kunt meerdere naam-waardeparen voor kenmerken opgeven, gescheiden door spatie.

- `<metadata node path>`: volledig mappad, inclusief bestandsnaam en het bijbehorende metagegevensknooppunt. Als u bijvoorbeeld het pad opgeeft als `http://192.168.1.1:4502/content/dam/projects/AEM-Guides/intro.xml/jcr:content/metadata` , wordt de opgegeven metagegevens ingesteld in het `intro.xml` -bestand.