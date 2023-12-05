---
title: Werkbalk Aanpassen
description: Leer hoe u de werkbalk kunt aanpassen
exl-id: ba82af48-9357-4f29-90ce-6793366ab432
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---

# Werkbalk Aanpassen {#id172FB00L0V6}

Standaard wordt de webeditor geleverd met de meest voorkomende redactionele functies die door elke DITA-editor worden vereist. Functies zoals het invoegen van elementen van het type lijst \(genummerd of met opsommingstekens\), kruisverwijzing, inhoudsverwijzing, tabel, alinea en tekenopmaak zijn beschikbaar in de editor. Naast deze basiselementen, kunt u de Redacteur van het Web aanpassen om elementen op te nemen die in uw auteursmilieu worden gebruikt.

Er zijn twee manieren om de toolbar van de Redacteur van het Web aan te passen:

- Nieuwe functionaliteit toevoegen aan de werkbalk

- Bestaande functies van de werkbalk verwijderen


## Een functie toevoegen aan de werkbalk

Het toevoegen van een functionaliteit aan de Redacteur van het Web impliceert twee primaire taken - toevoegend een pictogram voor de eigenschap in *ui\_config.json* en de achtergrondfunctionaliteit in JavaScript toevoegen.

Voer de volgende stappen uit om een eigenschap aan de toolbar van de Redacteur van het Web toe te voegen:

1. U kunt als beheerder het configuratiebestand van de gebruikersinterface downloaden door u aan te melden bij Adobe Experience Manager.

1. Klik op de Adobe Experience Manager-koppeling bovenaan en kies **Gereedschappen**.
1. Selecteren **Hulplijnen** in de lijst met gereedschappen en klik op de knop **Mapprofielen**.
1. Klik op de knop **Globaal profiel** tegel.
1. Selecteer de **XML Editor-configuratie** en klik op **Bewerken** pictogram bovenaan
1. Klik op de knop **Downloaden** pictogram om het bestand ui\_config.json op uw lokale systeem te downloaden. Vervolgens kunt u wijzigingen in het bestand aanbrengen en het bestand vervolgens uploaden.
1. In de `ui_config.json` , voegt u de definitie van de nieuwe functie toe in de sectie Werkbalken. Sla het bestand op en upload het.

   Doorgaans kunt u een nieuwe werkbalkknoopgroep maken en er een of meer werkbalkknoppen aan toevoegen. U kunt ook een nieuwe werkbalkknop toevoegen binnen een bestaande werkbalkgroep. U moet de volgende gegevens opgeven om een nieuwe werkbalkgroep te maken:

   **type**: Opgeven `blockGroup` als de `type` waarde. Deze waarde geeft aan dat u een blokgroep maakt die een of meer werkbalkgroepen zou bevatten.

   **extractiemateriaal**: Naam van de klasse of klassen, gescheiden door spatie.

   **items**: Geef de definitie van alle groepen op de werkbalk op. Elke groep kan een of meerdere werkbalkpictogrammen bevatten. Als u pictogrammen in een werkbalkgroep wilt definiëren, moet u opnieuw de `type` attribuut binnen `items`en stel de waarde in op `buttonGroup`. Geef een of meer klassenamen op in het dialoogvenster `extraclass` eigenschap. Geef de functienaam op in het dialoogvenster `label` eigenschap. Het volgende fragment uit het `ui_config.json` het bestand bevat de definitie van het hoofdwerkbalkblok, gevolgd door `buttonGroup` definitie:

       &quot;
       &quot;toolbar&quot;: {
       &quot;type&quot;: &quot;blockGroup&quot;,
       &quot;extractiemateriaal&quot;:
       &quot;werkbalkbewerkingen&quot;,
       &quot;items&quot;: [
       {
       &quot;type&quot;: &quot;buttonGroup&quot;,
       &quot;extraclass&quot;: &quot;left-controls&quot;;
       &quot;label&quot;: &quot;Left Controls&quot;,
       &quot;items&quot;: [
       &quot;
   
   Binnen de `items` verzameling, moet u de definitie voor een of meer werkbalkpictogrammen opgeven.

   U moet de volgende eigenschappen definiëren om een werkbalkpictogram toe te voegen:

   **type**: Opgeven `button` als de `type` waarde. Deze waarde geeft aan dat u een werkbalkknop toevoegt.

   **pictogram**: Geef de naam op van het koraalpictogram dat u wilt gebruiken op de werkbalk.

   **variant**: Opgeven `quiet` als de `variant` waarde.

   **titel**: Geef de knopinfo voor het pictogram op.

   **klikken**: Geef de opdrachtnaam op die voor de functie in het JavaScript-bestand is gedefinieerd. Als voor uw opdracht invoerparameters zijn vereist, geeft u de opdrachtnaam op als:

       &quot;Javascript
       &quot;on-click&quot;: {&quot;name&quot;: &quot;AUTHOR_INSERT_ELEMENT&quot;, &quot;args&quot;: &quot;simpletable&quot;}
       &quot;
   
   **tonen of verbergen**: Als u de opdracht `show` en geeft u vervolgens de modi op waarin het pictogram wordt weergegeven. Mogelijke waarden zijn: `@isAuthorMode`, `@isSourceMode`, `@isPreviewMode`, `true` \(weergeven in alle modi\), of `false` \(in alle modi verbergen\).

   In plaats van `show`kunt u ook de `hide` eigenschap. De mogelijke waarden zijn gelijk aan die in `show` eigenschap met het enige verschil dat het pictogram niet wordt weergegeven voor de opgegeven modus.

   In het volgende voorbeeld ziet u AEM het versienummer van hulplijnen wanneer de gebruiker op het pictogram Versie tonen op de werkbalk klikt.

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

   Voeg de functie toe in het dialoogvenster *ui\_config.json* bestand als:

   ```Javascript
   "type": "button",
   "icon": "alert","variant": "quiet","title": "About AEM Guides","show": "true","on-click": "user.alert"
   ```

1. Een *clientlib* en voeg uw JavaScript toe aan deze map.

1. Werk het categoriebezit van bij *clientlib* door deze toe te wijzen aan de waarde van *apps.fmdita.xml\_editor.page\_overrides*.

1. Sla de *ui\_config.json* bestand en laad de webeditor opnieuw.


## Een functie verwijderen uit de werkbalk

Soms wilt u wellicht niet alle functies weergeven die momenteel beschikbaar zijn in de webeditor. In dat geval kunt u de ongewenste functie verwijderen van de werkbalk van de webeditor.

Voer de volgende stappen uit om ongewenste functies van de werkbalk te verwijderen:

1. U kunt als beheerder het configuratiebestand van de gebruikersinterface downloaden door u aan te melden bij Adobe Experience Manager.

1. Klik op de Adobe Experience Manager-koppeling bovenaan en kies **Gereedschappen**.
1. Selecteren **Hulplijnen** in de lijst met gereedschappen en klik op de knop **Mapprofielen**.
1. Klik op de knop **Globaal profiel** tegel.
1. Selecteer de **XML Editor-configuratie** en klik op **Bewerken** pictogram bovenaan
1. Klik op de knop **Downloaden** pictogram om het bestand ui\_config.json op uw lokale systeem te downloaden. Vervolgens kunt u wijzigingen in het bestand aanbrengen en het bestand vervolgens uploaden.

   De `ui_config.json` bestand heeft drie secties:

   1. **werkbalken**: Deze sectie bevat de definitie van alle functies die beschikbaar zijn op de werkbalk van de editor, zoals Genummerde lijst invoegen/verwijderen, \(bestand\) Sluiten, Opslaan, Opmerkingen en meer.

   1. **sneltoetsen**: Deze sectie bevat de definitie van sneltoetsen die zijn toegewezen aan een bepaalde functie in de editor.

   1. **sjablonen**: Deze sectie bevat de vooraf gedefinieerde structuur van DITA-elementen die u in uw document kunt gebruiken. Standaard bevat de sjabloonsectie sjabloondefinities voor een alinea, eenvoudige tabel, tabel en tekstelementen. U kunt een sjabloondefinitie maken voor elk element door een geldige XML-structuur toe te voegen voor het gewenste element. Als u bijvoorbeeld een `p` element met elke nieuwe `li` in een lijst kunt u de volgende code toevoegen aan het einde van de sjabloonsectie om dit te bereiken:

   ```css
   "li": "<li><p></p></li>"
   ```

1. Verwijder in de sectie Werkbalken het item van de functie die u niet aan uw gebruikers wilt tonen.

1. Sla de *ui\_config.json* bestand en laad de webeditor opnieuw.


**Bovenliggend onderwerp:**[ Webeditor aanpassen](conf-web-editor.md)
