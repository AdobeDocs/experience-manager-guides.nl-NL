---
title: Een aangepast deelvenster configureren in het linkerdeelvenster
description: Leer hoe u een aangepast deelvenster kunt configureren in het linkerdeelvenster
exl-id: 6cfa64aa-46f3-4235-a4a7-f21e658f0a5a
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# Een aangepast deelvenster configureren in het linkerdeelvenster {#id224JI200Y6F}

Voer de volgende stappen uit om een aangepast paneel binnen het linkerpaneel van de Redacteur van het Web toe te voegen:

1. Creeer a *clientlib* omslag en voeg uw JavaScript en CSS dossier in deze omslag toe.
1. Werk het categoriereigenschap van de *clientlib* omslag bij door het de waarde van *apps.fmdita.xml \_editor.page\_overrides* toe te wijzen.

Voorbeeldcode voor het configureren van een aangepast deelvenster:

```JavaScript
tcx.ready(function () { //Ready will call the callback after editor code is set for events and global variable excess
 
 
    // APP_ADD_AUTHOR_LEFT_TAB event will add a new left tab in the left panel, user can show hide it using editor settings
    tcx.eventHandler.next(tcx.eventHandler.KEYS.APP_ADD_AUTHOR_LEFT_TAB, {
            id: 'my_panel',
            class: 'my-panel-tab',
            icon: 'file', //Any valid Adobe Spectrum icon name https://spectrum.adobe.com/page/icons/
            label: 'My Tab',
            prevTabID: 'repository_panel' //Existing tab ids are 'collection_panel', 'repository_panel', 'map_panel', 'outline_panel', 'conref_panel', 'glossary_panel', 'condition_panel', 'subject_scheme_panel', 'snippet_panel', 'template_panel', 'search_panel'
    })
 
    // APP_PANEL_DID_MOUNT event will be called after user has selected the panel and panel is rendered in the DOM
    tcx.eventHandler.subscribe({
        key: tcx.eventHandler.KEYS.APP_PANEL_DID_MOUNT,
        next: function(opts) {
            // TODO create panel ui inside $el
            let $el = opts.$el //$el is Tab panel content html node
            let id = opts.id //id is tab panel id (my_panel)
            console.log("mounted", opts)
        }
    })
 
  // APP_PANEL_WILL_UNMOUNT will be called before destorying the new left panel
  tcx.eventHandler.subscribe({
        key: tcx.eventHandler.KEYS.APP_PANEL_WILL_UNMOUNT,
        next: function(opts) {
            //TODO do some cleanup
            let id = opts.id //id is tab panel id (my_panel)
            console.log("unmounted", opts)
        }
    })
 
});
```

**Bovenliggend onderwerp:**&#x200B;[ pas de Redacteur van het Web ](conf-web-editor.md) aan
