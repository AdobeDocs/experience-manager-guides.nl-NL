---
title: Workflow na generatie
description: Een overzicht van de workflow na de generatie met een voorbeeld
exl-id: e19fdc0b-0ec6-46ce-81ed-e9490d12c029
source-git-commit: eb3fe92d36bc58a11e47f786a10d5938e2ed0184
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Publiceren van hulplijnen AEM - workflow na generatie

Met AEM hulplijnen kunt u een workflow voor het genereren van producten na de uitvoer opgeven. U kunt sommige naverwerkingstaken op de output uitvoeren die gebruikend AEM Gidsen wordt geproduceerd.
U kunt bijvoorbeeld bepaalde eigenschappen instellen voor de uitvoer van de PDF, of u wilt een e-mailbericht verzenden naar een set gebruikers wanneer de uitvoer eenmaal is gegenereerd.


## Wat zijn de stappen om werkstromen na de generatie te gebruiken

### Een workflowproces maken

Maak een op Java of ECMA gebaseerd workflowproces dat de bewerking uitvoert op de gegenereerde uitvoer. Bijvoorbeeld, kopieert het kopiëren van sommige meta-gegevens van bron aan de geproduceerde inhoud of het manipuleren van meta-gegevens van de geproduceerde output.
- We nemen bijvoorbeeld een voorbeeld van het maken van een dergelijk proces met behulp van ECMA-script (u kunt het bijgevoegde pakket raadplegen)
- Raadpleeg de sectie &quot;*Workflow voor het genereren na uitvoer aanpassen*&quot; van [Installatie- en configuratiehandleiding](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-2/Adobe-Experience-Manager-Guides_UUID_Installation-Configuration-Guide_EN.pdf#page=119)


### Een workflowmodel maken

Met het proces van het douanewerkschema dat u in vorige stap creeerde, creeer een werkschemamodel en voeg die processtap aan het toe.
- U moet ook een verplichte processtap toevoegen &quot;*Post Generation voltooien*&quot; als de laatste stap van de workflow.

Verwijs hieronder getoonde model van het steekproefwerkschema:

![Workflowmodel na generatie](../assets/workflows/pgwf-workflow-model.png)


### Deze workflow na het genereren gebruiken op een kaart

De workflow na het genereren is een eigenschap die kan worden geconfigureerd voor elke uitvoervoorinstelling in AEM publicatiemechanisme voor hulplijnen. Voorbeeld:

![Workflow na het genereren op uitvoervoorinstelling](../assets/workflows/pgwf-preset-settings.png)


Ervan uitgaande dat het geselecteerde model al is gemaakt.


### Testen

Nu kunt u de publicatie uitvoeren met deze voorinstelling en de uitvoer van de processtap valideren


## Monster

Ter referentie kunt u het onderstaande pakket gebruiken en installeren via pakketbeheer om de workflow na de generatie te testen (*zoals vermeld in bovenstaande screenshots*)

[Een voorbeeldworkflowmodel op basis van ECMA na de generatie](../assets/workflows/sample-pgwf-ecma-test-wfmetadata.zip)
