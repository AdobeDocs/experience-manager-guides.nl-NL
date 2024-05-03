---
title: Pictogram configureren voor aangepaste bewerkingstypen
description: Leer hoe u het pictogram voor aangepaste gegevenstypen definieert, zodat het pictogram op een andere gebruikersinterface wordt weergegeven in AEM
source-git-commit: ce2f5e4ab6b05fbce7b8384ff59091ebf9bab7be
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Het vormen pictogram voor de types van douane dita (onderwerp of kaart)


## Probleemverklaring

Met douaneschema in AEMGidsen wordt gebruikt, kunt u douaneonderwerp of kaarttypes tot stand brengen en met die u de douaneonderwerpen/de kaarten kunt zien tonen geen pictogram in de Web-redacteur of Activa UI. Zie schermafbeelding ter referentie  ../assets/authoring/custom-ditatype-icon-notshown.png)

Zo om een pictogram aan de types van douaneonderwerp/kaart toe te wijzen moet u het volgende doen:
- Het aangepaste onderwerp-/kaarttype zoeken
- Stijlen schrijven om het gewenste pictogram voor het aangepaste type toe te voegen


We kunnen de bovenstaande stappen implementeren om het pictogram weer te geven in de webeditor (de weergave in de repository) en in de interface Middelen. Hieronder staan de stappen voor beide


## Pictogram weergeven voor aangepast onderwerp/aangepaste kaart in webeditorweergave

Stap 1: Bepaal het ditatype voor het aangepaste dita onderwerp/de ap - open de bewaargegevensmening in Web-editor > open ontwikkelaarsconsole op browser - Inspect de pictogramruimte naast het vermelde onderwerp/de kaart - controleer de klasse die aan het douaneonderwerp wordt toegewezen - zie het screenshot  (../assets/authoring/custom-ditatype-icon-knowditatype.png) voor meer informatie - We gebruiken deze klasse om pictogrammen toe te wijzen en css voor dit type schrijven

Stap 2: CSS maken en pictogram aan dit gegevenstype toewijzen - Een clientbibliotheek maken onder /apps, hiermee kunt u een cq:ClientLibraryFolder maken onder het gewenste pad - categorieën &quot;apps.fmdita.xml_editor.page&quot; toevoegen - een map &quot;assets&quot; onder deze map maken en alle pictogrammen toevoegen die u voor aangepaste ditatypen wilt gebruiken - een css-bestand toevoegen onder de clientbibliotheekmap, bijvoorbeeld &quot;tree-icons&quot;.css&quot; - voeg de volgende code aan het toe

```
            .tree-item-icon {
                &.custommaptype {
                    background-image: url('assets/custommap.svg')
                }
                &.customtopictype {
                    background-image: url('assets/customtopic.svg')
                }
            }
```

    - css.txt onder de omslag van de cliëntbibliotheek toevoegen en verwijzing toevoegen aan &quot;tree-icon.css enkel gecreeerd
    - deze wijzigingen opslaan/implementeren
Screenshot vernieuwen  (../assets/authoring/custom-ditatype-icon-define-webeditor-styles.png) voor meer informatie.

En de definitieve output wordt getoond in het schermschot  ../assets/authoring/custom-ditatype-icon-webeditor-showstyles.png)


## Pictogram weergeven voor aangepast onderwerp/kaart in interface Middelen

Stap 1: het bepalen van het ditatype van het aangepaste dita onderwerp/de kaart - dit wordt verklaard in de vorige methodes&#39; Stap 1

Stap 2: Maak JavaScript om te definiëren welke pictogrammen moeten worden geladen voor het aangepaste dita-type voor aangepaste onderwerper-/kaarttypen - maak een clientbibliotheek onder /apps, laat u een cq:ClientLibraryFolder onder het gewenste pad maken - voeg er de volgende eigenschappen aan toe: - waarde &quot;categorieën&quot;(multivalue string) als &quot;dam.gui.admin.coral&quot; - waarde &quot;afhankelijkheden&quot;(multivalue string) als &quot;libs.fmbs dita.versioncontrol&quot; - Maak een kopie van het bestand &quot;/libs/fmdita/clientlibs/clientlibs/xmleditor/clientlib-dam/topic_type.js&quot; naar deze directory /apps - bewerk het gekopieerde &quot;topic_type.js&quot; en wijzig/voeg het aangepaste type toe onder de variabele &quot;typeImageNameMap&quot; - U kunt ook het pad van de afbeeldingenmap wijzigen door de waarde van de variabele &quot;parentImagePath&quot; te wijzigen naar de locatie waar aangepaste pictogrammen zijn opgeslagen - Een bestand maken met de naam js.txt onder de map voor de clientbibliotheek en verwijzing naar &quot;topic_type.js&quot; - bewaar/stel deze veranderingen op het schermschot van verwijzingen  (../assets/authoring/custom-ditatype-icon-define-assetsui-styles.png) voor meer informatie.

En de definitieve output zal verschijnen zoals aangetoond in het schermschot  ../assets/authoring/custom-ditatype-icon-assetsui-showstyles.png)