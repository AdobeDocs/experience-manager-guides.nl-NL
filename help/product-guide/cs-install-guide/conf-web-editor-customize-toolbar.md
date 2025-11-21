---
title: Werkbalk Aanpassen
description: Leer hoe u de werkbalk kunt aanpassen
exl-id: ba82af48-9357-4f29-90ce-6793366ab432
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '989'
ht-degree: 0%

---

# Werkbalk Aanpassen {#id172FB00L0V6}

Standaard wordt de webeditor geleverd met de meest voorkomende redactionele functies die door elke DITA-editor worden vereist. Functies zoals het invoegen van elementen van het type lijst \(genummerd of met opsommingstekens\), kruisverwijzing, inhoudsverwijzing, tabel, alinea en tekenopmaak zijn beschikbaar in de editor. Naast deze basiselementen, kunt u de Redacteur van het Web aanpassen om elementen op te nemen die in uw auteursmilieu worden gebruikt.

>[!NOTE]
>
> Wanneer u van de oude gebruikersinterface naar de nieuwe gebruikersinterface van AEM Guides migreert (van toepassing vanaf de release van AEM Guides 2502 en 5.0), moeten updates naar `ui_config` worden omgezet in flexibelere en modulaire gebruikersinterfaceconfiguraties. Met dit framework kunt u naadloos wijzigingen aanbrengen in de editor_toolbar en andere doelwidget, indien van toepassing. Voor details, mening [&#x200B; Overzicht van Omzetten UI Config &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-guides-learn/videos/advanced-user-guide/conver-ui-config).

Er zijn twee manieren om de toolbar van de Redacteur van het Web aan te passen:

- Nieuwe functionaliteit toevoegen aan de werkbalk
- Bestaande functies van de werkbalk verwijderen


## Een functie toevoegen aan de werkbalk

Het toevoegen van een functionaliteit aan de Redacteur van het Web impliceert twee primaire taken - toevoegend een pictogram voor de eigenschap in het {*dossier 0} ui\_config.json en toevoegend de achtergrondfunctionaliteit in JavaScript.*

Voer de volgende stappen uit om een eigenschap aan de toolbar van de Redacteur van het Web toe te voegen:

1. U kunt als beheerder het configuratiebestand van de gebruikersinterface downloaden door u aan te melden bij Adobe Experience Manager.

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **Profielen van de Omslag**.
1. Klik op de **Globale tegel van het Profiel**.
1. Selecteer het **lusje van de Configuratie van de Redacteur van XML** en klik **uitgeven** pictogram op de bovenkant
1. Klik het **pictogram van de Download** om het ui \_config.json- dossier op uw lokaal systeem te downloaden. Vervolgens kunt u wijzigingen in het bestand aanbrengen en het bestand vervolgens uploaden.
1. Voeg in het bestand `ui_config.json` de definitie van de nieuwe functie toe in de sectie Werkbalken. Sla het bestand op en upload het.

   Doorgaans kunt u een nieuwe werkbalkknoopgroep maken en er een of meer werkbalkknoppen aan toevoegen. U kunt ook een nieuwe werkbalkknop toevoegen binnen een bestaande werkbalkgroep. U moet de volgende gegevens opgeven om een nieuwe werkbalkgroep te maken:

   **type**:   Geef `blockGroup` op als de `type` -waarde. Deze waarde geeft aan dat u een blokgroep maakt die een of meer werkbalkgroepen zou bevatten.

   **extraclass**:   Naam van de klasse of klassen, gescheiden door spatie.

   **punten**:   Geef de definitie van alle groepen op de werkbalk op. Elke groep kan een of meerdere werkbalkpictogrammen bevatten. Als u pictogrammen in een werkbalkgroep wilt definiëren, moet u het kenmerk `type` opnieuw definiëren in de `items` -sectie en de waarde ervan instellen op `buttonGroup` . Geef een of meer klassenamen op in de eigenschap `extraclass` . Geef de functienaam op in de eigenschap `label` . In het volgende fragment uit het bestand `ui_config.json` wordt de definitie van het hoofdwerkbalkblok weergegeven, gevolgd door de definitie `buttonGroup` :

   ```
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

   **type**:   Geef `button` op als de `type` -waarde. Deze waarde geeft aan dat u een werkbalkknop toevoegt.

   **pictogram**:   Geef de naam op van het koraalpictogram dat u wilt gebruiken op de werkbalk.

   **variant**:   Geef `quiet` op als de `variant` -waarde.

   **titel**:   Geef de knopinfo voor het pictogram op.

   **on-click**:   Geef de opdrachtnaam op die voor de functie in het JavaScript-bestand is gedefinieerd. Als voor uw opdracht invoerparameters zijn vereist, geeft u de opdrachtnaam op als:

   ```Javascript
   "on-click": {"name": "AUTHOR_INSERT_ELEMENT", "args": "simpletable"}
   ```

   **toon of verberg**:   Als u de eigenschap `show` definieert, geeft u de modi op waarin het pictogram wordt weergegeven. Mogelijke waarden zijn - `@isAuthorMode`, `@isSourceMode`, `@isPreviewMode`, `true` \(weergeven in alle modi\) of `false` \(verbergen in alle modi\).

   In plaats van `show` kunt u ook de eigenschap `hide` definiëren. De mogelijke waarden zijn gelijk aan die in de eigenschap `show` , met het enige verschil dat het pictogram niet wordt weergegeven voor de opgegeven modus.

   In het volgende voorbeeld ziet u het AEM Guides-versienummer wanneer de gebruiker op het pictogram Versie tonen op de werkbalk klikt.

   Voeg de volgende code toe aan een JavaScript-bestand:

   ```Javascript
   $(document).ready(setTimeout(function() {
                           fmxml.commandHandler.subscribe({
                           key: 'user.alert',
                           next: function() {
                           alert("AEM Guides version x.x")
                           }
                           })
                           }, 1000))
   ```

   Voeg de eigenschap in het {*dossier 0} toe ui \_config.json als:*

   ```Javascript
   "type": "button",
   "icon": "alert","variant": "quiet","title": "About AEM Guides","show": "true","on-click": "user.alert"
   ```

1. Creeer a *clientlib* omslag en voeg uw JavaScript in deze omslag toe.

1. Werk het categoriereigenschap van de *clientlib* omslag bij door het de waarde van *apps.fmdita.xml \_editor.page\_overrides* toe te wijzen.

1. Sparen het {*dossier 0} ui\_config.json en laad de Redacteur van het Web opnieuw.*


## Een functie verwijderen uit de werkbalk

Soms wilt u wellicht niet alle functies weergeven die momenteel beschikbaar zijn in de webeditor. In dat geval kunt u de ongewenste functie verwijderen van de werkbalk van de webeditor.

Voer de volgende stappen uit om ongewenste functies van de werkbalk te verwijderen:

1. U kunt als beheerder het configuratiebestand van de gebruikersinterface downloaden door u aan te melden bij Adobe Experience Manager.

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **Profielen van de Omslag**.
1. Klik op de **Globale tegel van het Profiel**.
1. Selecteer het **lusje van de Configuratie van de Redacteur van XML** en klik **uitgeven** pictogram op de bovenkant
1. Klik het **pictogram van de Download** om het ui \_config.json- dossier op uw lokaal systeem te downloaden. Vervolgens kunt u wijzigingen in het bestand aanbrengen en het bestand vervolgens uploaden.

   Het bestand `ui_config.json` heeft drie secties:

   1. **toolbars**:   Deze sectie bevat de definitie van alle functies die beschikbaar zijn op de werkbalk van de editor, zoals Genummerde lijst invoegen/verwijderen, \(bestand\) Sluiten, Opslaan, Opmerkingen en meer.

   1. **kortere weg**:   Deze sectie bevat de definitie van toetsenbordkortere weg die aan een bepaalde eigenschap in de redacteur wordt toegewezen.

   1. **malplaatjes**:   Deze sectie bevat de vooraf gedefinieerde structuur van DITA-elementen die u in uw document kunt gebruiken. Standaard bevat de sjabloonsectie sjabloondefinities voor een alinea, eenvoudige tabel, tabel en tekstelementen. U kunt een sjabloondefinitie maken voor elk element door een geldige XML-structuur toe te voegen voor het gewenste element. Als u bijvoorbeeld een `p` -element wilt toevoegen met elk nieuw `li` -element in een lijst, kunt u de volgende code toevoegen aan het einde van de sjabloonsectie om dit te bereiken:

   ```css
   "li": "<li><p></p></li>"
   ```

1. Verwijder in de sectie Werkbalken het item van de functie die u niet aan uw gebruikers wilt tonen.

1. Sparen het {*dossier 0} ui\_config.json en laad de Redacteur van het Web opnieuw.*


**Bovenliggend onderwerp:**&#x200B;[&#x200B; pas de Redacteur van het Web &#x200B;](conf-web-editor.md) aan
