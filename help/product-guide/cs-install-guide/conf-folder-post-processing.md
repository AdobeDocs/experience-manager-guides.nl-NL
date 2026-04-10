---
title: Bestandsnamen configureren
description: Leer hoe u naverwerking voor een naar Adobe Experience Manager Assets geüploade map kunt uitschakelen
feature: Filename Configuration
role: Admin
level: Experienced
exl-id: 42722c6f-1b1c-4a7e-89ef-a373623eb774
hidefromtoc: true
source-git-commit: 564ee1731be2378744ffd2ed54a2fd423901a0b3
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# Nabewerking voor een map uitschakelen

Standaard worden alle geüploade elementen verwerkt met behulp van de DAM Update Asset-workflow. Experience Manager Guides voert als onderdeel van deze workflow een extra verwerking uit, ook wel postprocessing genoemd. Dit helpt ook bij het genereren van de UUID&#39;s

Terwijl het uploaden van uw dossiers en omslagen aan de *Adobe Experience Manager Assets* server, kunt u postprocessing en de generatie van UUIDs ook onbruikbaar maken.

Gebruik de instructies in [ met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. In het configuratiedossier, verstrek de volgende (bezit) details om postprocessing op een bepaalde weg onbruikbaar te maken of de naverwerking voor een omslag te negeren:

>[!NOTE]
>
> U kunt reguliere expressies (regex) ook gebruiken om regels te definiëren die van toepassing zijn op meerdere mappen of een volledige maphiërarchie. Voor meer details, bekijk het [ gebruik regex om post-verwerkende ](#use-regex-to-enable-or-disable-post-processing) sectie toe te laten of onbruikbaar te maken.

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `ignored.post.processing.paths` | Tekenreekswaarde voor het instellen van een standaard NODE_OPTIONS (multigetaxeerde eigenschap, tekenreeksen met een pad dat `/` aan het einde of regex weglaat) <br> **Standaardwaarde**: `/content/dam/projects/translation_output` |

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `enabled.post.processing.paths` | Tekenreekswaarde voor het instellen van een standaard NODE_OPTIONS (multigetaxeerde eigenschap, tekenreeksen met een pad dat `/` aan het einde of regex weglaat) <br> **Standaardwaarde**: `/content/dam` |

## Regels om nabewerking in of uit te schakelen

Standaard wordt nabewerking uitgevoerd voor elk mappad onder de Experience Manager DAM-map. Configuraties worden toegepast op elke map volgens de volgende regels:

* Als het bovenliggende element wordt genegeerd voor nabewerking maar de onderliggende map is ingeschakeld, worden het onderliggende item en alle opvolgers ervan als ingeschakeld beschouwd.
* Als de ouder voor postprocessing wordt toegelaten maar het kind wordt genegeerd, dan worden het kind en al zijn opvolgers beschouwd als genegeerd.
* Als hetzelfde mappad voorkomt in configuraties `ignored.post.processing.paths` en `enabled.post.processing.paths` , wordt het beschouwd als genegeerd voor nabewerking.

## Regex gebruiken om nabewerking in of uit te schakelen

In plaats van afzonderlijke mappaden op te geven, kunt u reguliere expressies (regex) gebruiken om regels te definiëren die van toepassing zijn op meerdere mappen of volledige maphiërarchieën.

Regex-patronen worden tijdens de nabewerking geëvalueerd op basis van het volledige middelenpad.

Wanneer reguliere expressies (regex) worden gebruikt om genegeerde en ingeschakelde naverwerkingspaden te configureren, evalueert AEM Guides beide configuraties op basis van het middelenpad. Als een weg zowel negeert regel als regel toelaat, negeer regels altijd belangrijkheid.

De volgende voorbeelden illustreren hoe op regex-Gebaseerd negeert en regels toelaat worden geëvalueerd.

## Regex-evaluatiescenario&#39;s voor naverwerking

### Bovenliggende hiërarchie negeren, specifieke map inschakelen

**negeren regex**

`regex:/content/dam/lang-test/.*`

**laat regex** toe

`regex:/content/dam/lang-test/.*/parent1`

In het bovenstaande voorbeeld wordt nabewerking uitgeschakeld voor `/content/dam/lang-test/en/parent1` .

Hoewel de weg toelaat regex aanpast, wordt het reeds aangepast door negex. Regels negeren hebben voorrang, dus naverwerking is niet ingeschakeld.

### Specifieke map negeren, bredere hiërarchie inschakelen

**negeren regex**

`regex:/content/dam/lang-test/.*/parent1`

**laat regex** toe

`regex:/content/dam/lang-test/.*`

In het bovenstaande voorbeeld wordt naverwerking uitgeschakeld voor `/content/dam/lang-test/en/parent1` en ingeschakeld voor `/content/dam/lang-test/en/parent2` .

Het pad `parent1` wordt expliciet genegeerd en blijft uitgeschakeld. Andere omslagen die slechts aanpassen toelaten regex worden verwerkt.

### Bovenliggende map negeren, onderliggende map inschakelen

**negeren regex**

`regex:/content/dam/lang-test/.*/parent1`

**laat regex** toe

`regex:/content/dam/lang-test/.*/parent1/child1`

In het bovenstaande voorbeeld wordt naverwerking uitgeschakeld voor `/content/dam/lang-test/en/parent1` en `/content/dam/lang-test/en/parent1/child2` en ingeschakeld voor `/content/dam/lang-test/en/parent1/child1` .

De onderliggende map die expliciet door regex wordt ingeschakeld, wordt verwerkt. Andere onderliggende mappen blijven uitgeschakeld omdat het bovenliggende pad overeenkomt met de ignore regex.

### Specifieke onderliggende map negeren, bovenliggende hiërarchie inschakelen

**negeren regex**

`regex:/content/dam/lang-test/.*/parent1/child1`

**laat regex** toe

`regex:/content/dam/lang-test/.*/parent1`

In het bovenstaande voorbeeld wordt naverwerking uitgeschakeld voor `/content/dam/lang-test/en/parent1/child1` en ingeschakeld voor `/content/dam/lang-test/en/parent1` en `/content/dam/lang-test/en/parent1/child2` .

Alleen de expliciet genegeerde onderliggende map wordt overgeslagen. De bovenliggende map en andere onderliggende mappen worden verwerkt omdat ze overeenkomen met de enable regex en niet overeenkomen met de ignore regex.

