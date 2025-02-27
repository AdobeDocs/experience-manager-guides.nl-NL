---
title: Variabelen gebruiken voor het instellen van de opties Doelpad, Sitenaam of Bestandsnaam
description: Leer hoe u variabelen gebruikt voor het instellen van de opties Pad bestemming, Sitenaam of Bestandsnaam. In AEM Guides ondersteunde variabelen voor 'out-of-the-box'.
feature: Publishing
role: User
hide: true
exl-id: 19d9121f-6b72-445c-a7d9-07f00026b654
source-git-commit: 1426cdaecdd358f06e76908b09330e65997e8452
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Variabelen gebruiken voor het instellen van de opties Doelpad, Sitenaam of Bestandsnaam


Tijdens het genereren van uitvoer in AEM-sites of PDF&#39;s kunt u variabelen gebruiken om de opties Doelpad, AEM-sitenaam of PDF-bestandsnaam te definiëren. U kunt een enkele of een combinatie van variabelen gebruiken om deze opties te definiëren.

In de volgende tabel worden de variabelen weergegeven die uit het vak worden ondersteund:

| Variabele | Uiteindelijke bestemmingspad | Voorbeeld |
| --- | --- | --- |
| `${map_filename}` | Gebruikt de naam van de DITA kaartdossiers om de bestemmingspad tot stand te brengen. | **DITA de naam van het kaartdossier**:<br>`AEMGuides.ditamap`<br><br>**Pad van de Bestemming** gevormd als:<br>`/content/output/sites/${map_filename}`<br><br>**Definitieve outputplaats**:<br>`/content/output/sites/aemGuides/AEMGuides.html` |
| `${map_title}` | Gebruikt de DITA kaarttitel om de bestemmingsweg tot stand te brengen. | **DITA kaartdossier - naam**:<br>`AEMGuides.ditamap`<br><br>**DITA kaartTitel**:<br>`AEMGuides`<br><br>**Pad van de Bestemming** gevormd als:<br>`/content/output/sites/${map_title}`<br><br>**Definitieve outputplaats**:<br>`/content/output/sites/AEMGuides/AEMGuides.html` |
| `${preset_name}` | Gebruikt de naam van de uitvoervoorinstelling om het doelpad te maken. | **Vooraf ingestelde Output Naam**:<br>`AEM Guides PDF Output`<br><br>**DITA naam van het kaartdossier**:<br>`SampleDita.ditamap`<br><br>**Pad van de Bestemming** gevormd als:<br>`/content/output/sites/${preset_name}`<br><br>**Definitieve outputplaats**:<br>`/content/output/sites/AEM Guides PDF Output/SampleDita.html` |
| `${language_code}` | Gebruikt de taalcode waar het kaartdossier wordt gevestigd om de bestemmingspad tot stand te brengen. | **DITA de naam van het kaartdossier**:<br>`SampleDita.ditamap`<br><br>**DITA de weg van het kaartdossier**:<br>`/content/dam/projects/AEM-Guides/en/user-guide/`<br><br>**Pad van de Bestemming** gevormd als:<br>`/content/output/sites/${language_code}`<br><br>**Definitieve outputplaats**:<br>`/content/output/sites/en/SampleDita.html` |
| `${map_parentpath}` | Gebruikt het volledige pad van het kaartbestand om het doelpad te maken.<br><br>**Nota**:Deze variabele kan niet worden gebruikt om de Naam van de Plaats van AEM of het Dossier van PDF te specificeren. | **DITA de naam van het kaartdossier**:<br>`SampleDita.ditamap`<br><br>**DITA de weg van het kaartdossier**:<br>`/content/dam/projects/AEM-Guides/en/user-guide`/<br><br>**Pad van de Bestemming** gevormd als:<br>`/content/output/sites/${map_parentpath}`<br><br>**Definitieve outputplaats**:<br>`/content/output/sites/content/dam/projects/AEM-Guides/en/user-guide/SampleDita.html` |
| `${path_after_langfolder}` | Gebruikt het pad van het kaartbestand na de taalmap om het doelpad te maken.<br><br>**Nota**: Deze variabele kan niet worden gebruikt om de Naam van de Plaats van AEM of het Dossier van PDF te specificeren. | **DITA de naam van het kaartdossier**:<br>`SampleDita.ditamap`<br><br>**DITA de weg van het kaartdossier**:<br>`/content/dam/projects/AEM-Guides/en/user-guide/`<br><br>**Pad van de Bestemming** gevormd als:<br>`/content/output/sites/${path\_after\_langfolder}`<br><br>**Definitieve outputplaats**:<br>`/content/output/sites/user-guide/SampleDita.html` |
| `${system_date}` | Gebruikt de huidige serverdatum om de bestemmingspad tot stand te brengen. | **DITA de naam van het kaartdossier**: <br> `SampleDita.ditamap` <br><br> **Pad van het de kaartdossier DITA:** <br> `/content/dam/projects/AEM-Guides/en/user-guide/` <br><br> **Pad van de Bestemming** gevormd als: <br> `/content/output/sites/${system_date}` <br> <br> **Definitieve outputplaats:** <br> /`content/output/sites/08252023/SampleDita.html` |
| `${system_time}` | Gebruikt de huidige servertijd om de bestemmingspad tot stand te brengen. | **DITA de naam van het kaartdossier:** <br>`SampleDita.ditamap` <br> <br> **DITA de weg van het kaartdossier:** <br>`/content/dam/projects/AEM-Guides/en/user-guide/` <br><Br>**Pad van de Bestemming** gevormd als: <br> `/content/output/sites/${system_time}`<br><br>**Definitieve outputplaats:**<br>`/content/output/sites/055612/SampleDita.html` |

Daarnaast kunt u de metagegevens die voor de DITA-kaart of het bladwijzerbestand zijn gedefinieerd, ook als variabelen gebruiken. De metagegevens vindt u onder het knooppunt `/jcr:content/metadata` van de DITA-kaart of het bladwijzerbestand. Een van de metagegevenseigenschappen die in het knooppunt `/jcr:content/metadata` wordt gedefinieerd, is bijvoorbeeld `dc:title` . U kunt `${dc:title}` opgeven en de titelwaarde wordt gebruikt in de uiteindelijke uitvoer.
**Bovenliggend onderwerp:**[ Productie van de Output ](generate-output.md)
