---
title: Aangepaste DITA-onderwerpsjabloon configureren
description: Leer hoe te om het onderwerpmalplaatje van douaneDITA te vormen
exl-id: 5a2f4897-9697-4c5c-b5be-8fdb3a211948
feature: Template Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Aangepaste DITA-onderwerpsjabloon configureren {#id16A7G0O02TD}

AEM Guides komt met de volgende DITA onderwerpmalplaatjes:

- Onderwerp

- Taak

- Concept

- Referentie

- Verklarende woordenlijst

- Problemen oplossen

- Leeg


U kunt om het even welk van deze malplaatjes gebruiken om onderwerpmalplaatjes volgens uw auteursvereisten tot stand te brengen. De lege DITA-sjabloon bevat geen structuur of elementen zoals de andere sjablonen. U kunt het Lege malplaatje als basis gebruiken, als uw malplaatje hoogst aangepast is en niet gebaseerd op om het even welke regelmatige DITA onderwerpmalplaatjes is.

Om DITA onderwerpmalplaatje aan te passen en het voor creatie te gebruiken, moet u de volgende drie hoofdtaken uitvoeren:

1. *\ (Facultatief \)* [ vorm de weg van de malplaatjeomslag van DITA ](#id191LCF0095Z)

1. [Aangepaste ontwerpsjabloon maken](conf-folder-level.md#id1917D0EG0HJ)

1. Voeg een douanemalplaatje in het globale of omslag-vlakke profiel toe zoals die in [ wordt verklaard creërende malplaatjes ](conf-folder-level.md#id1889D0IL0Y4) sectie vormt


## Aangepast pad voor DITA-sjabloonmap configureren {#id191LCF0095Z}

Met AEM Guides kunt u een map configureren voor het opslaan van uw aangepaste DITA-kaart en -sjablonen. Standaard worden de sjabloonbestanden opgeslagen in de volgende map in DAM:

`/content/dam/dita-templates/`

Om onderwerp en kaartmalplaatjedossiers te beheren, zijn er specifieke omslagen om het onderwerp en kaartmalplaatjes op te slaan. Standaard worden alle onderwerpsjablonen opgeslagen onder `/content/dam/dita-templates/topics`

map. Alle kaartsjablonen worden opgeslagen in de map `/content/dam/dita-templates/maps` .

Als beheerder, kunt u verkiezen om douanekaart of onderwerpmalplaatjes in de standaardomslag tot stand te brengen of uw eigen omslag tot stand te brengen om douanesjablonen op te slaan. Als u de standaardmap wilt gebruiken, kunt u dit proces overslaan.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. In het configuratiedossier, verstrek de volgende \(bezit \) details om een omslag voor uw douaneDITA onderwerpmalplaatjes te vormen:

>[!IMPORTANT]
>
> U kunt dit proces overslaan als u de standaardmap wilt gebruiken om aangepaste sjablonen op te slaan.

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `topic.templates` | Geef een locatie op voor de opslag van aangepaste sjablonen.<br> Als de gespecificeerde plaats in DAM bestaat, dan worden alle standaardkaart en onderwerpmalplaatjes gekopieerd in die omslag. Als de plaats niet bestaat, dan wordt de omslag gecreeerd met alle standaardkaart en onderwerpmalplaatjes. |

**Bovenliggend onderwerp:**&#x200B;[ vorm onderwerp en kaartmalplaatjes ](conf-template-tags.md)
