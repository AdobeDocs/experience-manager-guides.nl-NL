---
title: Weergave van op UUID gebaseerde koppelingen configureren
description: Leer hoe u weergave van UUID-koppelingen kunt configureren
exl-id: 2ae6a27f-983b-4aa0-be29-166899aeb4ff
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Weergave van op UUID gebaseerde koppelingen configureren {#id2035G20M0QN}

Wanneer u een koppeling maakt met de optie Referentie invoegen of Inhoud hergebruiken invoegen in de webeditor, wordt de koppeling standaard gemaakt met de UUID van de inhoud waarnaar wordt verwezen. De **Koppeling** eigenschap \(in deelvenster Eigenschappen\) van de inhoud waarnaar wordt verwezen, kan worden geconfigureerd om het relatieve bestandspad van de inhoud waarnaar wordt verwezen of de UUID weer te geven. Standaard wordt de UUID van de inhoud waarnaar wordt verwezen, weergegeven in het deelvenster Eigenschappen.

Gebruik de instructies die worden gegeven in [Configuratieoverschrijvingen](download-install-additional-config-override.md#) om het configuratiebestand te maken. In het configuratiedossier, verstrek de volgende \(bezit \) details om de relatieve weg of UUID van de referenced inhoud in de Redacteur van het Web te tonen:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.uuid` | Boolean \(true/false\). Als u het relatieve pad van de gekoppelde inhoud wilt weergeven, stelt u deze eigenschap in op false. <br> **Standaardwaarde**: true |

**Bovenliggend onderwerp:**[ Webeditor aanpassen](conf-web-editor.md)
