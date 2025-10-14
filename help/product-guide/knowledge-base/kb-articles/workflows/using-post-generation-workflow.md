---
title: Post Generation Workflow
description: Een overzicht van de workflow na de generatie met een voorbeeld
exl-id: e19fdc0b-0ec6-46ce-81ed-e9490d12c029
feature: Workflow Configuration
role: User, Admin
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# AEM Guides-publicaties - Post Generation Workflow

AEM Guides biedt u de flexibiliteit om een workflow voor het genereren van producten na de uitvoer op te geven. U kunt sommige naverwerkingstaken uitvoeren op de uitvoer die met AEM Guides wordt gegenereerd.
U kunt bijvoorbeeld bepaalde eigenschappen instellen voor de uitvoer van de PDF, of u wilt een e-mailbericht verzenden naar een set gebruikers wanneer de uitvoer eenmaal is gegenereerd.


## Wat zijn de stappen om workflows voor Post-generatie te gebruiken?

### Een workflowproces maken

Maak een op Java of ECMA gebaseerd workflowproces dat de bewerking uitvoert op de gegenereerde uitvoer. Bijvoorbeeld, kopieert het kopiëren van sommige meta-gegevens van bron aan de geproduceerde inhoud of het manipuleren van meta-gegevens van de geproduceerde output.
- We nemen bijvoorbeeld een voorbeeld van het maken van een dergelijk proces met behulp van ECMA-script (u kunt het bijgevoegde pakket raadplegen)
- Voor Java gebaseerd werkschemaproces, verwijs sectie &quot;*het werkschema van de post-outputgeneratie*&quot;van [&#x200B; de gids van de Installatie en van de configuratie &#x200B;](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-2/Adobe-Experience-Manager-Guides_UUID_Installation-Configuration-Guide_EN.pdf#page=119) aanpassen


### Een workflowmodel maken

Met het proces van het douanewerkschema dat u in vorige stap creeerde, creeer een werkschemamodel en voeg die processtap aan het toe.
- U moet een verplichte processtap ook toevoegen &quot;*voltooit de Generatie van Post*&quot;als laatste stap van het werkschema.

Verwijs hieronder getoonde model van het steekproefwerkschema:

![&#x200B; het model van het de generatiewerkschema van Post &#x200B;](../assets/workflows/pgwf-workflow-model.png)


### Deze workflow na het genereren gebruiken op een kaart

De Post-workflow voor genereren is een eigenschap die kan worden geconfigureerd voor elke uitvoervoorinstelling in het publicatiemechanisme van AEM Guides. Voorbeeld:

![&#x200B; het generatiewerkschema van Post op Vooraf ingestelde Output &#x200B;](../assets/workflows/pgwf-preset-settings.png)


Ervan uitgaande dat het geselecteerde model al is gemaakt.


### Testen

Nu kunt u de publicatie uitvoeren met deze voorinstelling en de uitvoer van de processtap valideren


## Monster

Voor uw verwijzing, kunt u onder pakket gebruiken en het installeren via pakketmanager om het werkschema van de steekproefpost generatie (*zoals die in screenshots hierboven* wordt bedoeld) te testen

[Een voorbeeldworkflowmodel op basis van ECMA na de generatie](../assets/workflows/sample-pgwf-ecma-test-wfmetadata.zip)
