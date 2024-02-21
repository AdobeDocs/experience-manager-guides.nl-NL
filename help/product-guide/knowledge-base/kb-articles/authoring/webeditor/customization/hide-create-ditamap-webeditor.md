---
title: De optie DitaMap maken verbergen in het contextmenu van de map voor specifieke gebruikers of groepen.
description: Leer hoe u de webbrowser kunt aanpassen door de optie DitaMap te verbergen in het contextmenu voor mappen voor specifieke gebruikers/groepen
source-git-commit: ea8fb646287f68676b6530b4cc5f56e7ba2d9b0c
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---


# &#39;Create DitaMAP&#39; in het contextmenu van mappen in de webbrowser tonen/verbergen

In dit artikel, zullen wij leren hoe te om de Redacteur van het Web van Gidsen aan te passen om de optie &quot;Create DitaMap&quot;in het menu van de omslagcontext op basis van gebruiker/groepstoestemmingen te verbergen of te tonen.
In dit gebruiksgeval wordt deze optie voor alle gebruikers zonder auteur verborgen.

## Voorwaarden

We gebruiken het extensiepakket voor AEM hulplijnen, waarmee u de gebruikersinterface van uw app naar wens kunt aanpassen.
Gelieve dit door te nemen [documentatie](https://github.com/adobe/guides-extension/tree/main) voor meer inzicht in de werking van het Extension Framework van Guides.

Nu gaat u aan de slag en leert u hoe u het contextmenu van de map kunt aanpassen om deze optie te verbergen voor alle gebruikers die geen auteur zijn.

Zoals u onder codefragment kunt zien, is de optie &quot;DitaMap maken&quot; zichtbaar voor een auteur-gebruiker.

![DitaMap maken weergeven, optie](../../../assets/authoring/ditamap-show-author.png)

Laten we nu bekijken hoe we deze optie kunnen verbergen met het Guides Extension Framework.

## Implementatiestappen

De implementatie is onderverdeeld in de volgende onderdelen:

- **Wijzigingen in de controller Folder_options**

  Aan elk contextmenu is een controller-id gekoppeld. Deze controller handelt de gebeurtenisfunctionaliteit voor de verschillende contextmenu-opties af.

  In dit voorbeeld passen we het contextmenu van de map aan om de optie &#39;Create DitaMap&#39; voor niet-auteurs te verbergen. Hiervoor zullen we wijzigingen aanbrengen in het bestand folder_options.ts dat zich onder /src bevindt in de gegevensopslagruimte van het raamwerk voor hulplijnen.

  We gebruiken &quot;viewState&quot; als &quot;REPLACE&quot; om deze optie in het contextmenu te verbergen.
We roepen een nieuwe widget in deze folder_options door sleutel &#39;id&#39; aan.

```typescript
const folderOptions = {
  id: "folder_options",
  contextMenuWidget: "repository_panel",
  view: {
    items: [
      {
        component: "widget",
        id: "customditamap",
        target: {
          key: "displayName",
          value: "DITA Map",
          viewState: VIEW_STATE.REPLACE,
        },
      },
    ],
  },
};
```

- **Een nieuwe widget maken om de logica af te handelen**

  Er is een nieuwe widget gemaakt (customoptions.ts) om de logica te schrijven waarmee deze optie alleen voor niet-auteurgebruikers kan worden verborgen. Om dit te bereiken hebben we de &quot;show&quot;-toets gebruikt, die fungeert als schakeloptie in onze JSON-structuur.

  U kunt uw eigen externe servlet schrijven om de groepdetails te controleren. Op deze manier kunt u ook de opties voor het mapmenu aanpassen voor uw aangepaste groep.
In dit voorbeeld hebben we de OOTB-AEM &#39;rolesapi&#39;-aanroep benut om de gebruikersgegevens op te halen en de reactie in &#39;isAuthor&#39; in te stellen, zoals in bovenstaande fragmenten wordt getoond.

```typescript
const folderOptions = {
  id: "customditamap",
  view: {
    component: "button",
    quiet: true,
    icon: "breakdownAdd",
    label: "DITA Map",
    "on-click": "createNewDitaMap",
    show: "@extraProps.isAuthor",
  },
};
```

Hiermee kunnen we de knop verbergen met het label &#39;Dita Map&#39; op basis van de waarde &#39;show&#39;.

We hebben een controller toegevoegd om het kenmerk &#39;isAuthor&#39; in het model in te stellen. Dit kan met de volgende syntaxis in de controller worden gedaan.

```typescript
this.model.extraProps.set("key", value);
```

Hier is de sleutel &#39;isAuthor&#39; en de waarde is de reactie van de rolesapi vraag.
We hebben ook de gebeurtenis &#39;createNewDitaMap&#39; gedefinieerd om de optie DitaMap maken in te schakelen (voor auteur-gebruikers).

```typescript
controller: {
    init: function () {
      this.model.extraProps.set("isAuthor", false);

      rolesApiResponse.then((result) => {
        console.log(result);
        this.model.extraProps.set(
          "isAuthor",
          result["/content/dam"].roles.authors
        );

        console.log("testresult" + result["/content/dam"].roles.authors);
      });
    },
    createNewDitaMap() {
      repositoryController && repositoryController.next("create_new.map");
    },
  },
```

- **De aangepaste code toevoegen**

  Importeer de bestanden folder_options.ts en customoptions.ts in het bestand index.ts onder /src.

## Testen

- Meld u aan bij AEM met een gebruiker die geen deel uitmaakt van een groep auteurs. De optie DitaMap maken wordt verborgen in het contextmenu van elke map, zoals hieronder wordt weergegeven.
Dit gebruikscase is toegevoegd aan GIT. Zie hieronder de gerelateerde bronnen.

![De optie DitaMap maken verbergen](../../../assets/authoring/ditamap-hide-non-author.png)

### Gerelateerde bronnen

- **Basis gegevensopslagsysteem van Extension Framework** - [GIT](https://github.com/adobe/guides-extension/tree/main)

- **Documentatie** - [over Experience League](../../../../../guides-ui-extensions/aem_guides_framework/basic-customisation.md)

- **Gedocumenteerde gevallen van veelvuldig gebruik** - [over Experience League](../../../../../guides-ui-extensions/aem_guides_framework/jui-framework.md)

- **Openbare opslagplaats met voorbeelden** - [op GIT](https://github.com/adobe/guides-extension/tree/sc-expert-session). Verwijs tak sc-deskundige-zitting

```

```
