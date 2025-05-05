---
title: '@navtitle-kenmerk standaard opnemen'
description: Leer hoe u standaard @navtitle-kenmerk kunt opnemen
exl-id: 38711c0c-efa8-461a-92e1-ecfcdcdd36d3
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# @navtitle-kenmerk standaard opnemen {#id2115BC0J0XA}

U kunt verschillende soorten verwijzingsdossiers in een kaart toevoegen, bijvoorbeeld onderwerp, verwijzing, taak, \(sub\) kaarten, etc. De meeste van deze bestanden ondersteunen het kenmerk `@navtitle` . Niet veel auteurs gebruiken het echter consistent. Als u het gebruik van het kenmerk `@navtitle` wilt afdwingen in alle bestanden waarnaar wordt verwezen in een kaart, kunt u dit doen met een eenvoudige configuratie.

Als deze optie is ingeschakeld, wordt het kenmerk `@navtitle` automatisch toegevoegd aan de eigenschappen van elk referentiebestand dat u in een kaart toevoegt. De `@navtitle` krijgt ook de waarde van het `title` -element van de inhoud waarnaar wordt verwezen.

Ga als volgt te werk om `@navtitle` -kenmerk standaard op te nemen in de eigenschappen van referentiebestanden:

1. U kunt als beheerder het configuratiebestand van de gebruikersinterface downloaden door u aan te melden bij Adobe Experience Manager.

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **Profielen van de Omslag**.
1. Klik op de **Globale tegel van het Profiel**.
1. Selecteer het **lusje van de Configuratie van de Redacteur van XML** en klik **uitgeven** pictogram op de bovenkant
1. Klik het **pictogram van de Download** om het ui \_config.json- dossier op uw lokaal systeem te downloaden.
1. U kunt deze wijziging doorvoeren op algemeen niveau of op een mapniveau. Afhankelijk van waar u deze wijziging wilt aanbrengen, moet u het respectievelijke bestand ui\_config.json downloaden. Voor meer informatie over het downloaden ui\_config.json- dossier, zie [ vormen en de Redacteur van het Web van XML aanpassen ](conf-folder-level.md#id2065G300O5Z).

1. Zoek naar de `ditaAttributes` definitie.

   De standaarddefinitie van `ditaAttributes` is:

   ```
   "ditaAttributes": {
                           "attributes": [],
                           "constraint": false,
                           "required": {}
                           },
   ```

1. Wijzig de parameter `required` als:

   ```
   "required": {"navtitle": true}
   ```

1. Sla het bestand op.

1. Upload het bestand in het bijbehorende profiel \(Algemeen of Map\).


Met deze configuratie bevat elk referentiebestand dat u toevoegt aan een kaart standaard het kenmerk `@navtitle` .

**Bovenliggend onderwerp:**&#x200B;[ pas de Redacteur van het Web ](conf-web-editor.md) aan
