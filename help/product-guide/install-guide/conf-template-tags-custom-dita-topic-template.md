---
title: Aangepaste DITA-onderwerpsjabloon configureren
description: Leer hoe te om het onderwerpmalplaatje van douaneDITA te vormen
exl-id: a9b2c479-7bf6-4c62-addd-fdfe74dc1f69
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Aangepaste DITA-onderwerpsjabloon configureren {#id16A7G0O02TD}

De AEM Gidsen komt met de volgende DITA onderwerpmalplaatjes:

- Onderwerp

- Taak

- Concept

- Referentie

- Verklarende woordenlijst

- Problemen oplossen

- Leeg


U kunt om het even welk van deze malplaatjes gebruiken om onderwerpmalplaatjes volgens uw auteursvereisten tot stand te brengen. De lege DITA-sjabloon bevat geen structuur of elementen zoals de andere sjablonen. U kunt het Lege malplaatje als basis gebruiken, als uw malplaatje hoogst aangepast is en niet gebaseerd op om het even welke regelmatige DITA onderwerpmalplaatjes is.

Om DITA onderwerpmalplaatje aan te passen en het voor creatie te gebruiken, moet u de volgende drie hoofdtaken uitvoeren:

1. *\(Optioneel\)* [Aangepast pad voor DITA-sjabloonmap configureren](#id191LCF0095Z)

1. [Aangepaste ontwerpsjabloon maken](conf-folder-level.md#id1917D0EG0HJ)

1. Een aangepaste sjabloon toevoegen aan het algemene profiel of aan het mapprofiel, zoals wordt uitgelegd in het dialoogvenster [Ontwerpsjablonen configureren](conf-folder-level.md#id1889D0IL0Y4) sectie


## Aangepast pad voor DITA-sjabloonmap configureren {#id191LCF0095Z}

AEM de Gidsen staat u toe om een omslag te vormen om uw aangepaste kaart DITA en malplaatjes op te slaan. Standaard worden de sjabloonbestanden opgeslagen in de volgende map in DAM:

`/content/dam/dita-templates/`

Om onderwerp en kaartmalplaatjedossiers te beheren, zijn er specifieke omslagen om het onderwerp en kaartmalplaatjes op te slaan. Door gebrek, worden alle onderwerpmalplaatjes opgeslagen onder `/content/dam/dita-templates/topics`

map. Alle kaartsjablonen worden onder de `/content/dam/dita-templates/maps` map.

Als beheerder, kunt u verkiezen om douanekaart of onderwerpmalplaatjes in de standaardomslag tot stand te brengen of uw eigen omslag tot stand te brengen om douanesjablonen op te slaan. Als u de standaardmap wilt gebruiken, kunt u dit proces overslaan.

Voer de volgende stappen uit om een map voor uw aangepaste DITA-onderwerpsjablonen te configureren:

>[!IMPORTANT]
>
> U kunt dit proces overslaan als u de standaardmap wilt gebruiken om aangepaste sjablonen op te slaan.

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Zoeken naar en klikken op de knop *com.adobe.fmdita.config.ConfigManager* bundel.

1. In de **Sjabloonlocatie** eigenschap, geeft u een locatie op waar aangepaste sjablonen moeten worden opgeslagen.

1. Klikken **Opslaan**.


Als de gespecificeerde plaats in DAM bestaat, dan worden alle standaardkaart en onderwerpmalplaatjes gekopieerd in die omslag. Als de plaats niet bestaat, dan wordt de omslag gecreeerd met alle standaardkaart en onderwerpmalplaatjes.

**Bovenliggend onderwerp:**[ Onderwerp- en kaartsjablonen configureren](conf-template-tags.md)
