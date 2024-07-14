---
title: '@navtitle-kenmerk standaard opnemen'
description: Leer hoe u standaard @navtitle-kenmerk kunt opnemen
exl-id: 3def20dc-dd24-4526-ae36-45708249d34a
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# @navtitle-kenmerk standaard opnemen {#id2115BC0J0XA}

U kunt verschillende soorten verwijzingsdossiers in een kaart toevoegen, bijvoorbeeld onderwerp, verwijzing, taak, \(sub\) kaarten, etc. De meeste van deze bestanden ondersteunen het kenmerk `@navtitle` . Niet veel auteurs gebruiken het echter consistent. Als u het gebruik van het kenmerk `@navtitle` wilt afdwingen in alle bestanden waarnaar wordt verwezen in een kaart, kunt u dit doen met een eenvoudige configuratie.

Als deze optie is ingeschakeld, wordt het kenmerk `@navtitle` automatisch toegevoegd aan de eigenschappen van elk referentiebestand dat u in een kaart toevoegt. De `@navtitle` krijgt ook de waarde van het `title` -element van de inhoud waarnaar wordt verwezen.

Ga als volgt te werk om `@navtitle` -kenmerk standaard op te nemen in de eigenschappen van referentiebestanden:

1. Download het bestand ui\_config.json.

   U kunt deze wijziging doorvoeren op algemeen niveau of op een mapniveau. Afhankelijk van waar u deze wijziging wilt aanbrengen, moet u het respectievelijke bestand ui\_config.json downloaden. Voor meer informatie over het downloaden ui\_config.json- dossier, zie [ vormen en de Redacteur van het Web van XML aanpassen ](conf-folder-level.md#id2065G300O5Z).

1. Zoek naar de `ditaAttributes` definitie.

   De standaarddefinitie van `ditaAttributes` is:

   ```json
   "ditaAttributes": {
   "attributes": [],
   "constraint": false,
   "required": {}
   },
   ```

1. Wijzig de parameter `required` als:

   ```json
   "required": {"navtitle": true}
   ```

1. Sla het bestand op.

1. Upload het bestand in het bijbehorende profiel \(Algemeen of Map\).


Met deze configuratie bevat elk referentiebestand dat u toevoegt aan een kaart standaard het kenmerk `@navtitle` .
