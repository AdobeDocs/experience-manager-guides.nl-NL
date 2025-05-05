---
title: Bestaande DITA-inhoud uploaden
description: Leer hoe u bestaande DITA-inhoud kunt uploaden
exl-id: 2b385eef-00a7-4c25-9e78-367a0c9e44ba
feature: Migration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Bestaande DITA-inhoud uploaden {#id176FF000JUI}

U hebt waarschijnlijk een opslagplaats voor bestaande DITA-inhoud die u met de AEM Guides wilt gebruiken. Voor dergelijke bestaande inhoud, kunt u om het even welke gesteunde methodes gebruiken die in [ worden verklaard digitale activa aan Adobe Experience Manager as a Cloud Service Assets ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html) toevoegen.

## Patroon UUID-bestandsnaam configureren

Wanneer u inhoud importeert, is het niet nodig dat de bestandsnamen worden gebaseerd op de UUID. In een systeem dat op UUID-Gebaseerde dossiernamen gebruikt, is het verplicht dat alle dossiers worden bedoeld gebruikend hun UUIDs eerder dan hun originele dossiernamen. Als een geïmporteerd bestand geen op UUID gebaseerde bestandsnamen heeft, kunt u het systeem zo configureren dat een UUID wordt toegevoegd aan de eigenschap file. Deze UUID wordt vervolgens gebruikt om te verwijzen naar bestanden waarin UUID niet wordt gebruikt voor het benoemen van de bestanden.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\) gegevens op om het patroon van de UUID-bestandsnaam te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `uuid.regex` | String specifying the regex for UID filename pattern. <br> Als een bestand het opgegeven patroon niet volgt, wordt een UUID toegevoegd aan de eigenschap van het bestand en worden alle verwijzingen naar het bestand bijgewerkt met de UUID die aan het bestand is toegewezen. <br> **Standaardwaarde**: `"^GUID-(?<id>.*)"` |

## Krullopdrachten gebruiken

U kunt ook curl-opdrachten gebruiken om een map in DAM te maken, bestanden te uploaden en metagegevens toe te voegen aan de geüploade inhoud.

**creeer een omslag**

Voer de volgende opdracht uit om een map in AEM opslagplaats te maken:

```
curl --user <username>:<password> --data jcr:primaryType=sling:Folder "<server folder path>"
```

Geef de volgende parameters op om een map te maken:

- `<username>:<passowrd>`: Geef de gebruikersnaam en het wachtwoord op voor toegang tot de AEM. Deze gebruiker moet over de rechten voor het maken van mappen beschikken.

- `jcr:primaryType=sling:Folder`: Specificeer deze parameter *zoals* is om een middel van het omslagtype tot stand te brengen.

- `<server folder path>`: Volledig mappad inclusief de naam van de nieuwe map die u wilt maken in de AEM. Als u bijvoorbeeld het pad opgeeft als `http://192.168.1.1:4502/content/dam/projects/AEM-Guides` , wordt de map `AEM-Guides` gemaakt in de map `projects` in DAM.


**upload een dossier**

Voer de volgende opdracht uit om een bestand te uploaden in de AEM opslagplaats:

```
curl --user <username>:<password> -T "<local file path>" "<server folder path>"
```

Geef de volgende parameters op om een bestand te uploaden:

- `<username>:<passowrd>`: Geef de gebruikersnaam en het wachtwoord op voor toegang tot de AEM. Deze gebruiker moet schrijfrechten hebben op de `server folder path` .

- ``local file path``: volledig bestandspad op uw lokale systeem dat u wilt uploaden.

- `<server folder path>`: Voltooi het mappad op de AEM server waar u het bestand wilt uploaden.


**voeg meta-gegevens** toe

Voer de volgende opdracht uit om metagegevens toe te voegen aan een bestand:

```
curl --user <username>:<password> -F<attribute name>=<value> <metadata node path>
```

Geef de volgende parameters op om metagegevensinformatie toe te voegen:

- `<username>:<passowrd>`: Geef de gebruikersnaam en het wachtwoord op voor toegang tot de AEM. Deze gebruiker moet schrijfrechten hebben op de ``metadata node path`` .

- ``-F<attribute name>=<value>``: `<attribute name>` is de naam van het metagegevenskenmerk, zoals `audience` en `<value>` zou kunnen zijn `internal` . U kunt meerdere naam-waardeparen voor kenmerken opgeven, gescheiden door spatie.

- `<metadata node path>`: volledig mappad, inclusief bestandsnaam en het bijbehorende metagegevensknooppunt. Als u bijvoorbeeld het pad opgeeft als `http://192.168.1.1:4502/content/dam/projects/AEM-Guides/intro.xml/jcr:content/metadata` , wordt de opgegeven metagegevens ingesteld in het `intro.xml` -bestand.


**Bovenliggend onderwerp:**&#x200B;[ Migreer bestaande inhoud ](migrate-content.md)
