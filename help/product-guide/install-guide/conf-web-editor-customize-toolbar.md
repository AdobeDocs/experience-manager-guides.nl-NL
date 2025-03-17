---
title: Werkbalk Aanpassen
description: Leer hoe u de werkbalk kunt aanpassen
exl-id: 14a82c7e-5c07-43a8-bd9e-b221d80f6d05
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 5778ed2855287d1010728e689abbe6020ad56574
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 0%

---

# Werkbalk Aanpassen {#id172FB00L0V6}

Standaard wordt de webeditor geleverd met de meest voorkomende redactionele functies die door elke DITA-editor worden vereist. Functies zoals het invoegen van elementen van het type lijst \(genummerd of met opsommingstekens\), kruisverwijzing, inhoudsverwijzing, tabel, alinea en tekenopmaak zijn beschikbaar in de editor. Naast deze basiselementen, kunt u de Redacteur van het Web aanpassen om elementen op te nemen die in uw auteursmilieu worden gebruikt.

>[!NOTE]
>
> Wanneer u van de oude gebruikersinterface naar de nieuwe gebruikersinterface van AEM Guides migreert (van toepassing vanaf de release van AEM Guides 2502 en 5.0), moeten updates naar `ui_config` worden omgezet in flexibelere en modulaire gebruikersinterfaceconfiguraties. Met dit framework kunt u naadloos wijzigingen aanbrengen in de editor_toolbar en andere doelwidget, indien van toepassing. Voor details, mening [ Overzicht van Omzetten UI Config ](https://experienceleague.adobe.com/en/docs/experience-manager-guides-learn/videos/advanced-user-guide/conver-ui-config).

Er zijn twee manieren om de toolbar van de Redacteur van het Web aan te passen:

- Nieuwe functionaliteit toevoegen aan de werkbalk

- Bestaande functies van de werkbalk verwijderen


## Een functie toevoegen aan de werkbalk

Het toevoegen van een functionaliteit aan de Redacteur van het Web impliceert twee primaire taken - toevoegend een pictogram voor de eigenschap in het {*dossier 0} ui\_config.json en toevoegend de achtergrondfunctionaliteit in JavaScript.*

**voeg een pictogram in de toolbar** toe

Voer de volgende stappen uit om een eigenschap aan de toolbar van de Redacteur van het Web toe te voegen:

1. Meld u aan bij AEM en open de CRXDE Lite-modus.

1. Navigeer naar het standaardconfiguratiebestand dat beschikbaar is op de volgende locatie:

   `/libs/fmdita/clientlibs/clientlibs/xmleditor/ui_config.json`

1. Maak een kopie van het standaardconfiguratiebestand op de volgende locatie:

   `/apps/fmdita/xmleditor/ui_config.json`

1. Navigeer naar het `ui_config.json` -bestand in het knooppunt `apps` en open het voor bewerking.

1. Voeg in het bestand `ui_config.json` de definitie van de nieuwe functie toe in de sectie Werkbalken. Doorgaans kunt u een nieuwe werkbalkknoopgroep maken en er een of meer werkbalkknoppen aan toevoegen. U kunt ook een nieuwe werkbalkknop toevoegen binnen een bestaande werkbalkgroep. U moet de volgende gegevens opgeven om een nieuwe werkbalkgroep te maken:

   - **type:**Specify `blockGroup` als `type` waarde. Deze waarde geeft aan dat u een blokgroep maakt die een of meer werkbalkgroepen zou bevatten.

   - **extraclass:** Naam van de klasse of de klassen die met ruimte worden gescheiden.

   - **punten:** specificeer de definitie van alle groepen in de toolbar. Elke groep kan een of meerdere werkbalkpictogrammen bevatten. Als u pictogrammen in een werkbalkgroep wilt definiëren, moet u het kenmerk `type` opnieuw definiëren in de `items` -sectie en de waarde ervan instellen op `buttonGroup` . Geef een of meer klassenamen op in de eigenschap `extraclass` . Geef de functienaam op in de eigenschap `label` . In het volgende fragment uit het bestand `ui_config.json` wordt de definitie van het hoofdwerkbalkblok weergegeven, gevolgd door de definitie `buttonGroup` :

     ```json
     "toolbar": {    
       "type": "blockGroup",    
       "extraclass": 
       "toolbar operations",    
         "items": [      
           {        
             "type": "buttonGroup",        
             "extraclass": "left-controls",        
             "label": "Left Controls",        
             "items": [
     ```

     In de `items` -verzameling moet u de definitie voor een of meer werkbalkpictogrammen opgeven.
U moet de volgende eigenschappen definiëren om een werkbalkpictogram toe te voegen:

   - **type:** specificeer `button` als `type` waarde. Deze waarde geeft aan dat u een werkbalkknop toevoegt.

   - **pictogram:** specificeer de naam van het pictogram van het Koraal dat u in de toolbar wilt gebruiken.

   - **variant:** specificeer `quiet` als `variant` waarde.

   - **titel:** specificeer tooltip voor het pictogram.

   - **on-click:** specificeer de bevelnaam die voor de eigenschap in het dossier van JavaScript wordt bepaald. Als voor uw opdracht invoerparameters zijn vereist, geeft u de opdrachtnaam op als:

     ```JavaScript
     "on-click": {"name": "AUTHOR_INSERT_ELEMENT", "args": "simpletable"}
     ```

   - **tonen of verbergen:** als u het `show` bezit bepaalt, dan specificeer de wijzen waarin het pictogram wordt getoond. Mogelijke waarden zijn - `@isAuthorMode`, `@isSourceMode`, `@isPreviewMode`, `true` \(weergeven in alle modi\) of `false` \(verbergen in alle modi\).

   In plaats van `show` kunt u ook de eigenschap `hide` definiëren. De mogelijke waarden zijn gelijk aan die in de eigenschap `show` , met het enige verschil dat het pictogram niet wordt weergegeven voor de opgegeven modus.

1. Creeer a *clientlib* omslag en voeg uw JavaScript in deze omslag toe.

1. Werk het categoriereigenschap van de *clientlib* omslag bij door het de waarde van *apps.fmdita.xml \_editor.page\_overrides* toe te wijzen.

1. Sparen het {*dossier 0} ui\_config.json en laad de Redacteur van het Web opnieuw.*


**de codesteekproeven van JavaScript**

Deze sectie bevat twee voorbeelden van JavaScript-code die u helpen om aangepaste functionaliteit toe te voegen. In het volgende voorbeeld ziet u het AEM Guides-versienummer wanneer een gebruiker op het pictogram Versie tonen op de werkbalk klikt.

Voeg de volgende code toe aan een JavaScript-bestand:

```JavaScript
/**
* This file contains an example to show AEM Guides version 
* number when a user clicks on the Show Version icon in the toolbar. 
* Step 1. Create a clientlib folder and add save a file with your *JavaScript code into this folder. A code sample is shared below.
* Step 2: Update the categories property of the clientlib folder by *assigning it the value of 
* "apps.fmdita.xml_editor.page_overrides".
* Step 3: Add the feature in the ui_config.json file as shown after the *sample code. Save the ui_config.json file and reload the Web Editor
 */

(function (window) {
  "use strict";

  window.addEventListener('DOMContentLoaded', function () {
    fmxml.ready(function () {
      fmxml.eventHandler.subscribe({
        key: 'user.alert',
        next: function next() {
          alert("AEM Guides version x.x");
        }
      });
    });
  });
})(window);
```

Voeg de functie in het bestand ui\_config.json toe als:

```json
 {
      "type": "button",
      "icon": "alert",
      "title": "About AEM Guides",
      "variant": "quiet",

  "show": "true",
      "on-click": "user.alert"
  } 
```

In het volgende voorbeeld ziet u hoe u de status van een actief bestand in een document kunt wijzigen in &quot;In-Review&quot;.

```JavaScript
/**
* This file contains an example to set the document state of an active *open documen to "In-Review". 
* Step 1. Create a clientlib folder and add save a file with your *JavaScript code into this folder. A code sample is shared below.
* Step 2: Update the categories property of the clientlib folder by *assigning it the value of 
* "apps.fmdita.xml_editor.page_overrides".
* Step 3: Add the feature in the ui_config.json file as shown after the *sample code. Save the ui_config.json file and reload the Web Editor
 */

(function (window) {
  "use strict";

  //Wait for the page has been completely loaded 

  window.addEventListener('DOMContentLoaded', function () {

    //Wait for the xml editor to start
    fmxml.ready(function () {

      //Subscribe to 'user.docstate.to.in-review' event
      fmxml.eventHandler.subscribe({
        key: 'user.docstate.to.in-review',
        next: function next() {
          var docstate = "In-Review"; // New docstate name
          var filePath = fmxml.curEditor.filePath; 
// Get the file path of active open file
          if (filePath) {
            //Call API to change the doc state
            $.ajax({
              type: 'POST',
              url: '/bin/fmdita/states',
              data: {
                paths: filePath,
                operation: "setdocstates",
                docstate: docstate
              }
            }).fail(function (xhr, textStatus, errorThrown) {
              console.error("Cannot update docstate to " + docstate);
            }).success(function (data) {
              console.log('docstate updated to ' + docstate);
            });
          }
        }
      });
    });
  });
})(window);
```

Voeg de functie in het bestand ui\_config.json toe als:

```json
 {
      "type": "button",
      "icon": "actions",
      "title": "Change document state to In-Review",
      "variant": "quiet",
      "show": "true",
      "on-click": "user.docstate.to.in-review"
    } 
```

## Een functie verwijderen uit de werkbalk

Soms wilt u wellicht niet alle functies weergeven die momenteel beschikbaar zijn in de webeditor. In dat geval kunt u de ongewenste functie verwijderen van de werkbalk van de webeditor.

Voer de volgende stappen uit om ongewenste functies van de werkbalk te verwijderen:

1. Meld u aan bij AEM en open de CRXDE Lite-modus.

1. Navigeer naar het standaardconfiguratiebestand dat beschikbaar is op de volgende locatie:

   `/libs/fmdita/clientlibs/clientlibs/xmleditor/ui_config.json`

1. Maak een kopie van het standaardconfiguratiebestand op de volgende locatie:

   `/apps/fmdita/xmleditor/ui_config.json`

1. Navigeer naar het `ui_config.json` -bestand in het knooppunt `apps` en open het voor bewerking.
Het bestand `ui_config.json` heeft drie secties:

- **toolbars:**   Deze sectie bevat de definitie van alle functies die beschikbaar zijn op de werkbalk van de editor, zoals Genummerde lijst invoegen/verwijderen, \(bestand\) Sluiten, Opslaan, Opmerkingen en meer.

- **kortere weg:**   Deze sectie bevat de definitie van toetsenbordkortere weg die aan een bepaalde eigenschap in de redacteur wordt toegewezen.

- **malplaatjes:**   Deze sectie bevat de vooraf gedefinieerde structuur van DITA-elementen die u in uw document kunt gebruiken. Standaard bevat de sjabloonsectie sjabloondefinities voor een alinea, eenvoudige tabel, tabel en tekstelementen. U kunt een sjabloondefinitie maken voor elk element door een geldige XML-structuur toe te voegen voor het gewenste element. Als u bijvoorbeeld een `p` -element wilt toevoegen met elk nieuw `li` -element in een lijst, kunt u de volgende code toevoegen aan het einde van de sjabloonsectie om dit te bereiken:

```HTML
"li": "<li><p></p></li>"
```

1. Verwijder in de sectie Werkbalken het item van de functie die u niet aan uw gebruikers wilt tonen.

1. Sparen het {*dossier 0} ui\_config.json en laad de Redacteur van het Web opnieuw.*


**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
