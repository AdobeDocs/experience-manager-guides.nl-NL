---
title: De optie Verwijderen verwijderen uit het contextmenu van het bestand in de webbrowser voor specifieke gebruikers
description: Leer hoe u de webbrowser kunt aanpassen door de optie Verwijderen te verwijderen uit het contextmenu van het bestand voor specifieke gebruikers/groepen
exl-id: 31b4dd53-3938-42e1-bbc6-64806d668696
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# De optie Verwijderen verwijderen uit het contextmenu van het bestand in de webbrowser

In dit artikel leert u hoe u de optie Verwijderen verbergt in het contextmenu van bestanden in de AEM Guides-webeditor voor specifieke gebruikers of groepen. Voor andere aanpassingen in de menuopties van de dossiercontext, gelieve het kader van de Uitbreiding van Gidsen te controleren. Meer details kunnen [ hier ](https://github.com/adobe/guides-extension/tree/main) worden gevonden.

Zoals u onder het fragment kunt zien, is de optie Verwijderen beschikbaar voor deze specifieke gebruiker.

![ contextmenu van het Dossier met Schrapping ](../../../assets/authoring/file-contextmenu-Delete.png)

Laten we nu bekijken hoe we de optie Verwijderen kunnen verbergen voor deze gebruiker.

## Implementatiestappen:

- Navigeer naar Gereedschappen > Beveiliging > Rechten van AEM startpagina.
- Kies de groep of de gebruiker in het zoekvak.
- Klik op ACE toevoegen in de rechterbovenhoek.
- Kies het mappad.
- Inclusief rechten &quot;jcr:removeChildNodes&quot; en &quot;jcr:removeNode&quot;.
- Kies Machtigingstype als &#39;weigeren&#39; en klik op Toevoegen zoals hieronder wordt weergegeven.

![ de Toestemming van de Gebruiker ontkent ACE ](../../../assets/authoring/permission-ACE-Delete.png)

![ de controlelijst van de Toegang in toestemmingen ](../../../assets/authoring/delete-acl.png)

### Testen

- Login aan AEM als gebruiker waarvoor ACE is toegevoegd.
- Webeditor openen.
- Ga naar de dataweergave en kies de map waarvoor de ACE&#39;s zijn toegevoegd.
- Open het contextmenu voor bestanden.
- De optie Verwijderen wordt niet weergegeven in het contextmenu.

Het contextmenu voor bestanden ziet er nu als volgt uit:

![ contextmenu van het Dossier zonder Schrapping ](../../../assets/authoring/file-contextmenu-Delete-removed.png)

```
Please note that these steps would also remove 'move' and 'rename' options from the Web Editor as they are also tied to delete process at the backend.
```
