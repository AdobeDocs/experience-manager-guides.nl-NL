---
title: Contextmenu's
description: Contextmenu's aanpassen
role: User, Admin
exl-id: 25aa76dd-ef05-41ed-b980-14bbc1626059
source-git-commit: 492f72768e0de74a91eb7acc9db8264e21bfc810
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# Contextmenu&#39;s aanpassen

De volgende contextmenu&#39;s kunnen worden aangepast:

- `file_options`
controllers:
   - Kaartweergave: `ditamap_viewer_controller`
   - Deelvenster Opslagplaats: `repository_panel_controller`
   - Deelvenster Favorieten: `collection_tree_controller`
   - Referentiekoppelingen voor bestandseigenschappen: `file_references_links_controller`
   - Zoekdeelvenster voor opslagplaats: `repository_search_controller`
   - Deelvenster Onderwerpschema: `subject_scheme_tree_controller`

- `folder_options`
controllers:
   - Deelvenster Opslagplaats: `repository_panel_controller`
   - Deelvenster Favorieten: `collection_tree_controller`

- `collection_options`
controllers:
   - Deelvenster Favorieten: `collection_tree_controller`

- `map_view_options`
controllers:
   - Kaartweergave: `ditamap_viewer_controller`

- `baseline_panel_menu`
controllers:
   - Deelvenster Basislijn: `baseline_panel`

- `preset_item_menu`
controllers:
   - Deelvenster Voorinstellingen: `preset_panel`

U kunt ook uw eigen contextmenu maken door een nieuwe unieke id te definiëren.

Aan elk contextmenu is nu een `controller id` gekoppeld. Deze controller handelt de functionaliteit `on-event` voor de verschillende opties in contextmenu&#39;s af

Laten we een voorbeeld nemen om te begrijpen

```js title=customise_context_menu.js"
const loadDitaFile = (filePath, uuid) =>{
  return $.ajax({
    type: 'POST',
    url: '/bin/referencelistener',
    data: {
        operation: 'getdita',
        path: filePath,
        type: uuid ? 'UUID' : 'PATH',
        cache: false,
    },
  })
}

const fileOptions = {
    id: "file_options",
    contextMenuWidget: "repository_panel",
    view: {
            items: [
                {
                    component: "div",
                    target: {
                        key:"displayName",value: "Delete",                    
                        viewState: VIEW_STATE.REPLACE
                    }
                },
                {
                    component: "div",
                    target: {
                        key:"displayName",value: "Edit",                    
                        viewState: VIEW_STATE.REPLACE
                    }
                },
                {
                    "displayName": "Download",
                    "data": {
                      "eventid": "downloadFile"
                    },
                    "icon": "downloadFromCloud",
                    "class": "menu-separator",         
                    target: {
                        key:"displayName",value: "Duplicate",                    
                        viewState: VIEW_STATE.REPLACE
                    }
                },
            ]

    },

    controller: {
        downloadFile(){
            const path  = this.getValue('selectedItems')[0].path
            loadDitaFile(path).then((file) => {
              function download_file(name, contents) {
                const mime_type = "text/plain";
        
                const blob = new Blob([contents], {type: mime_type});
        
                const dlink = document.createElement('a');
                dlink.download = name;
                dlink.href = window.URL.createObjectURL(blob);
                dlink.onclick = function() {
                    // revokeObjectURL needs a delay to work properly
                    const that = this;
                    setTimeout(function() {
                        window.URL.revokeObjectURL(that.href);
                    }, 1500);
                };
        
                dlink.click();
                dlink.remove();
            }
            download_file(path,file.xml)
            });
          }
    }
}
```

Laten we nu begrijpen wat deze code doet.

1. `id` wordt gebruikt om het contextmenu te identificeren dat wij willen aanpassen.
2. `contextMenuWidget` wordt gebruikt om de `widget id` of `component` te definiëren die het contextmenu aanroept en de `events` afhandelt.

De rest blijft hetzelfde, waarbij `view` wordt gebruikt om de items te definiëren, `target` aangeeft waar de optie moet worden vervangen, toegevoegd of toegevoegd en de `contextMenuWidget` -controller de `on-click` -gebeurtenissen afhandelt.
