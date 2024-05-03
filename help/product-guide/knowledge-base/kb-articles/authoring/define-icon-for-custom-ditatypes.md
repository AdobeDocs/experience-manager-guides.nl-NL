---
title: Pictogram configureren voor aangepaste bewerkingstypen
description: Leer hoe u het pictogram voor aangepaste gegevenstypen definieert, zodat het pictogram op een andere gebruikersinterface wordt weergegeven in AEM
source-git-commit: 40b4c0803c87dbf1d3c2756e7974848100b5e56e
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---

# Het vormen pictogram voor de types van douane dita (onderwerp of kaart)


## Probleemverklaring

Met douaneschema in AEMGidsen wordt gebruikt, kunt u douaneonderwerp of kaarttypes tot stand brengen en met die u de douaneonderwerpen/de kaarten kunt zien tonen geen pictogram in de Web-redacteur of Activa UI. Zie schermafbeelding ter referentie ![screenshot ter referentie](../assets/authoring/custom-ditatype-icon-notshown.png)

Zo om een pictogram aan de types van douaneonderwerp/kaart toe te wijzen moet u het volgende doen:
- Het aangepaste onderwerp-/kaarttype zoeken
- Stijlen schrijven om het gewenste pictogram voor het aangepaste type toe te voegen


We kunnen de bovenstaande stappen implementeren om het pictogram weer te geven in de webeditor (de weergave in de repository) en in de interface Middelen. Hieronder staan de stappen voor beide


## Pictogram weergeven voor aangepast onderwerp/aangepaste kaart in webeditorweergave

*Stap 1 *: Bepaal het ditatype voor het aangepaste dita onderwerp/de ap
- Open de dataweergave in de webeditor > open ontwikkelingsconsole in de browser
- De pictogramruimte naast het vermelde onderwerp/de lijst Inspect
- Controleer de klasse die aan het douaneonderwerp wordt toegewezen
- Zie de schermafbeelding ![Zie de schermafbeelding](../assets/authoring/custom-ditatype-icon-knowditatype.png) voor meer informatie
- Deze klasse wordt gebruikt om pictogrammen toe te wijzen en css voor dit te schrijven

*Stap 2 *: Maak CSS en wijs een pictogram toe aan dit gegevenstype
- Maak een clientbibliotheek onder /apps en laat u een cq:ClientLibraryFolder onder het gewenste pad maken
   - er categorieën &quot;apps.fmdita.xml_editor.page&quot; aan toevoegen
- Maak een map &quot;assets&quot; onder deze map en voeg alle pictogrammen toe die u voor aangepaste gegevenstypen wilt gebruiken
- een CSS-bestand toevoegen onder de map van de clientbibliotheek, bijvoorbeeld &quot;tree-icons.css&quot;
   - volgende code toevoegen

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

- css.txt toevoegen onder de map met clientbibliotheken en verwijzing toevoegen naar &quot;tree-icon.css&quot; (zojuist gemaakt)
- deze wijzigingen opslaan/implementeren

Screenshot vernieuwen ![Screenshot vernieuwen](../assets/authoring/custom-ditatype-icon-define-webeditor-styles.png) voor meer informatie .

En de definitieve output wordt getoond in het schermschot ![weergegeven in schermafbeelding](../assets/authoring/custom-ditatype-icon-webeditor-showstyles.png)


## Pictogram weergeven voor aangepast onderwerp/kaart in interface Middelen

*Stap 1*: het bepalen van het ditatype van het aangepaste dita onderwerp/de kaart
- dit wordt uitgelegd in stap 1 van de voorgaande methoden

*Stap 2*: Maak JavaScript om te definiëren welke pictogrammen voor het aangepaste gegevenstype dita moeten worden geladen voor aangepaste onderwerpen/kaarttypen
- Maak een clientbibliotheek onder /apps en laat u een cq:ClientLibraryFolder onder het gewenste pad maken
   - Voeg de volgende eigenschappen toe:
      - &quot;Categorieën&quot; (multivalue string) als &quot;dam.gui.admin.coral&quot;
      - Waarde voor &#39;afhankelijkheden&#39; (multivalue string) als &#39;libs.fmdita.versioncontrol&#39;
- Een kopie van het bestand &quot;/libs/fmdita/clientlibs/clientlibs/xmleditor/clientlib-dam/topic_type.js&quot; maken naar deze map /apps
   - bewerk het gekopieerde &quot;topic_type.js&quot;en verander/voeg customtopictype onder veranderlijke &quot;typeImageNameMap&quot; toe
   - U kunt het pad van de afbeeldingenmap ook wijzigen door de waarde van de variabele &quot;parentImagePath&quot; te wijzigen in de locatie waar aangepaste pictogrammen worden opgeslagen
- Creeer een dossier genoemd js.txt onder de omslag van de cliëntbibliotheek en voeg verwijzing naar &quot;topic_type.js toe
- opslaan/implementeren van deze wijzigingen Zie schermafbeelding ![Screenshot vernieuwen](../assets/authoring/custom-ditatype-icon-define-assetsui-styles.png) voor meer informatie .

En de definitieve output zal verschijnen zoals aangetoond in het schermschot ![weergegeven in schermafbeelding](../assets/authoring/custom-ditatype-icon-assetsui-showstyles.png)