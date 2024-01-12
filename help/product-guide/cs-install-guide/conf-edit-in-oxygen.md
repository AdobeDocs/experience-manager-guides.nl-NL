---
title: De optie configureren om te bewerken in zuurstof
description: Leer hoe u de optie voor het bewerken van de insteekmodule Zuurstofconnector configureert.
exl-id: 96081a6d-39cf-4697-8b43-6494543ea187
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# De optie configureren om te bewerken in zuurstof

AEM de Gidsen staan de gebruikers ook toe om hun onderwerpen DITA en kaarten DITA in de Oxygeschakelaarstop uit te geven.

Gebruik de instructies die worden gegeven in [Configuratieoverschrijvingen](download-install-additional-config-override.md#) om het configuratiebestand te maken. In het configuratiedossier, verstrek de volgende (bezit) details om het **Bewerken in zuurstof** optie:



| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.editinoxygen` | Boolean \(true/false\). **Standaardwaarde**: false |

>[!NOTE]
>
> Deze configuratie wordt door gebrek onbruikbaar gemaakt en de optie is niet beschikbaar in de Redacteur van het Web.

**Bovenliggend onderwerp:**[ Webeditor aanpassen](conf-web-editor.md)
