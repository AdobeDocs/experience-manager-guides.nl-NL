---
title: Nieuwe aangepaste actieknop toevoegen op de werkbalk Webeditor
description: Leer hoe u een nieuwe aangepaste knop toevoegt op de werkbalk voor spetters en javascript aanroept om deze aan te passen.
exl-id: 34999db6-027a-4d93-944f-b285b4a44288
feature: Web Editor
role: User, Admin
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Nieuwe aangepaste actieknop toevoegen op de werkbalk Webeditor

In dit artikel leren wij hoe een nieuwe douaneknoop in webeditor toolbar toevoegen en javascript roepen om gewenste douaneverrichting uit te voeren.

Het toevoegen van een actioneerbare knoop aan webeditor omvat het volgende stappen:
- Toevoegend de knoop in *ui_config.json* bij de positie waar het nodig is
- De klikgebeurtenis van de knoop in webeditor registreren voor gebruiker om een actie uit te voeren wanneer zij het klikken


## Implementeren door een voorbeeld te nemen

Laten we dit begrijpen met een voorbeeld waarin een auteur een jira-verwijzing wil toevoegen aan een sectie met een onderwerp-proloog. De proloog sectie met ingebedde jira verwijzing-identiteitskaart kan als hieronder kijken:

![ sectie van het Prolog met identiteitskaart JIRA verwijzing ](../../../assets/authoring/webeditor-add-customtoolbarbutton-prolog-sample.png)

Het element &#39;change-request-id&#39; dat de JIRA-id bevat, moet worden opgehaald uit de API (laat bijvoorbeeld gebaseerd op een specifieke JIRA-query die door de toepassing wordt weergegeven). Wanneer de gebruiker de proloog sectie creeert, zou de gebruiker een knoop moeten kunnen klikken en jira verwijzings identiteitskaart van Web-redacteursttoolbar opnemen, iets als:

![ sectie van het Logboek - voeg verwijzing JIRA ](../../../assets/authoring/webeditor-add-customtoolbarbutton-prolog-insertjirareference.png) toe

En wanneer de gebruiker op de knop klikt, moet er een dialoogvenster worden weergegeven waarin de mogelijke opties worden weergegeven en de gebruiker de gewenste JIRA-id kan selecteren, bijvoorbeeld:

![ de sectie van het Prolog voegt de dialoog van identiteitskaart JIRA ](../../../assets/authoring/webeditor-add-customtoolbarbutton-prolog-insertjirareference-dialog.png) toe

die vervolgens de &quot;change-request-id&quot; aan de blog moet toevoegen:

![ sectie van het Prolog met identiteitskaart JIRA verwijzing ](../../../assets/authoring/webeditor-add-customtoolbarbutton-prolog-sample.png)



## Dit implementeren


### Voeg de knoop in webeditor toe door het in *te vormen ui_config.json*

Gebruik de omslagprofielen om *ui_config.json* onder het lusje van de Configuratie van de Redacteur van XML te controleren en de knoopconfiguratie JSON in de gewenste sectie van de &quot;toolbar&quot;groep toe te voegen

```
{
    "on-click":"insertJIRARef",
    "icon":"linkCheck",
    "variant":"quiet",
    "type":"button",
    "title":"Insert JIRA Reference"
}
```

[ gebruik deze verbinding om meer over het profiel van de Omslag te leren en het vormen ui_config.json ](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/videos/advanced-user-guide/editor-configuration.html?lang=en)


### De klikgebeurtenis voor de nieuwe knop afhandelen

     NOTA: De hieronder vermelde stappen zijn beschikbaar als pakket in bijlage in deze post 


- Na het opslaan van het omslagprofiel creeer &quot;cq:ClientLibraryFolder&quot;onder een projectfolder (zou onder *kunnen zijn/apps*) en voeg eigenschappen zoals aangetoond in het hieronder scherm toe:
  ![ de bibliotheekmontages van de Cliënt voor webeditor ](../../../assets/authoring/webeditor-add-customtoolbarbutton-clientlibrarysettings.png)

```
This example uses "coralui3" library to show a dialog as it is used in the Javascript sample we presented.
You may use different library of your choice.
```

- Maak onder deze clientbibliotheekmap twee bestanden, zoals hieronder wordt vermeld:
   - *treedt met voeten.js*: die de code javascript zal hebben om de gebeurtenis on-click voor &quot;insertJIRARef&quot;te behandelen (gebruik in bijlage pakket om de inhoud van dit javascript te krijgen)
   - *js.txt*: die &quot;overrides.js&quot;zal omvatten om dit javascript toe te laten

- Sla de wijzigingen op en u bent klaar om deze te testen.


### Testen

- Webeditor openen
- Van gebruikersvoorkeur kies het omslagprofiel waarin u douane *ui_config.json* toevoegde. Als u het aan het Globale profiel toevoegt, dan gebruikt u waarschijnlijk reeds dat.
- Open een onderwerp, u zult merken dat de toolbar een nieuwe knoop &quot;de Verwijzing van Jira van het Tussenvoegsel&quot;heeft
- Vervolgens kunt u de sectie prolog toevoegen zoals hieronder aan het onderwerp wordt gegeven en vervolgens klikken in de knop Jira-verwijzing invoegen in het prologelement &quot;change-request-reference&quot;

```
<prolog>
    <change-historylist>
        <change-item>
            <change-request-reference>
            </change-request-reference>
            <change-completed></change-completed>
            <change-summary></change-summary>
        </change-item>
    </change-historylist>
</prolog>
```

Zie onderstaande screenshot voor een uitleg van hoe deze eruitziet:

![ Test nieuwe knoop ](../../../assets/authoring/webeditor-add-customtoolbarbutton-testing.png)


### Bijlagen

- Het pakket van clientlibs van de steekproef dat de webeditor cliëntbibliotheek zal installeren die javascript code voor de actie van de toolbarknoop hebben: [ download gebruikend deze verbinding ](../../../assets/authoring/webeditor-addbuttonontoolbar-insertjira-clientlib.zip)
- Steekproef *ui_config.json* dat u aan een omslagprofiel kunt uploaden: [ download steekproef ui_config.json ](../../../assets/authoring/sample_ui_config_Guides4.2-InsertJiraReference.json)

```
Please note this is compatible to AEM 6.5 and AEM Guides version 4.2.
If you are using a different version please add the toolbar button to the ui_config.json manually.
```
