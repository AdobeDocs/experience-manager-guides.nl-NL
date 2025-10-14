---
title: Weergave van op UUID gebaseerde koppelingen configureren
description: Leer hoe u weergave van UUID-koppelingen kunt configureren
exl-id: ab1b0ecf-cb50-4fcd-b36e-d16a8c396054
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Weergave van op UUID gebaseerde koppelingen configureren {#id2035G20M0QN}

Wanneer u een koppeling maakt met de optie Referentie invoegen of Inhoud hergebruiken invoegen in de webeditor, wordt de koppeling standaard gemaakt met de UUID van de inhoud waarnaar wordt verwezen. Het **bezit van de Verbinding** \ (in het paneel van Eigenschappen \) van de referenced inhoud kan worden gevormd om de relatieve dossierweg van de referenced inhoud of UUID te tonen. Deze vertoning wordt gecontroleerd door **laat optie UUIDs** in configMgr toe. De optie is standaard ingeschakeld, wat betekent dat de UUID van de inhoud waarnaar wordt verwezen, wordt weergegeven in het deelvenster Eigenschappen.

Voer de volgende stappen uit om de relatieve weg of UUID van de referenced inhoud in de Redacteur van het Web te tonen:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. In de *montages 0&rbrace; XmlEditorConfig,**laat**&#x200B;optie UUIDs toe wordt toegelaten door gebrek.* Dit impliceert dat UUID van de referenced inhoud in het **bezit van de Verbinding** in het paneel van Eigenschappen wordt getoond.

   Als u de relatieve weg van de verbonden inhoud wilt tonen, dan schrap **toelaten UIDs** optie.

1. Klik **sparen**.


**Bovenliggend onderwerp:**&#x200B;[&#x200B; pas de Redacteur van het Web &#x200B;](conf-web-editor.md) aan
