---
title: Native PDF Publish-functie | Werken met aangepaste wijzigingsbalken
description: Leer hoe u stijlen toepast op wijzigingsbalken.
exl-id: a81ec56c-ccbb-4599-a696-8edef7a73cdd
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Werken met aangepaste wijzigingsbalken

Een wijzigingsbalk is een verticale lijn die nieuwe of herziene inhoud visueel identificeert. AEM Guides staat u toe om een veranderingsbar op de linkerzijde van de veranderde inhoud binnen onderwerpen en ook de veranderde onderwerpen in TOC van de output van de PDF te tonen.

Voor meer details bij het tonen van de veranderingsbar, zie *PDF met de Bar van de Verandering tussen Gepubliceerde Versies* het plaatsen in [&#x200B; Uitvoer van de PDF van Publish &#x200B;](../web-editor/native-pdf-web-editor.md) creëren.

## Gewijzigde inhoud binnen onderwerpen

De veranderingsbar verschijnt op de linkerzijde van de inhoud in de onderwerpen die zijn opgenomen, veranderd of geschrapt.

U kunt de volgende stijlen wijzigen om de gewijzigde inhoud weer te geven en onder de wijzigingsbalken.


>[!NOTE]
>
>Deze stijlen maken deel uit van het `layout.css` -bestand en u kunt ze naar wens bewerken.

U kunt bijvoorbeeld het kleurkenmerk in de `.inserted-block` -stijl gebruiken om te definiëren hoe de ingevoegde inhoud in de gepubliceerde PDF-uitvoer wordt weergegeven.


```css
...
.inserted-block { 
  color: #2ECC40; 
  display: inline; 
  -ro-comment-content: " "; 
  -ro-comment-style: underline; 
  -ro-comment-title: "Inserted"; 
  -ro-comment-date: attr(data-time); 
  -ro-comment-dateformat: "yyyy/dd/MM HH:mm:ss"; 
} 
...
```

Op dezelfde manier kunt u de stijl `.deleted-block` gebruiken om te bepalen hoe uw verwijderde inhoud in de gepubliceerde uitvoer van PDF verschijnt.

```css
...
.deleted-block { 
  display: inline; 
  color: #FF6961; 
  text-decoration: line-through; 
  -ro-comment-content: " "; 
  -ro-comment-style: strikeout; 
  -ro-comment-title: "Deleted"; 
  -ro-comment-date: attr(data-time); 
  -ro-comment-dateformat: "yyyy/dd/MM HH:mm:ss"; 
} 
...
```

Met de stijlen `.inserted-change-bar` en `.deleted-change-bar` kunt u de weergave wijzigen van de wijzigingsbalken die links van de bijgewerkte inhoud worden weergegeven.

U kunt bijvoorbeeld het kenmerk `-ro-change-bar-color` in `.inserted-change-bar` -stijl gebruiken om de ingevoegde wijzigingsbalk in groene kleur weer te geven. U kunt ook het kenmerk `-ro-change-bar-color` in `.deleted-change-bar` -stijl gebruiken om de verwijderde wijzigingsbalk in rode kleur weer te geven.

```css
...
.inserted-change-bar { 
  -ro-change-bar-color: #2ECC40; 
} 

.deleted-change-bar { 
  -ro-change-bar-color: #FF6961; 
  } 
...
```

<img src="./assets/changed-bar-content.png" alt="Inhoud van gewijzigd onderwerp van balk" width="500">

## Gewijzigd onderwerp in de Inhoudsopgave (TOC)

U kunt een veranderingsbar op de linkerzijde van de veranderde onderwerpen in TOC van de output van de PDF ook toevoegen. Met het kenmerk `-ro-change-bar-color` in de stijl `.changed-topic` kunt u een wijzigingsbalk in de kleur van uw keuze toevoegen voor de bijgewerkte onderwerpen in de lijst met inhoudsopgave.

U kunt bijvoorbeeld een wijzigingsbalk met een groene kleur toevoegen.

```css
...
.changed-topic { 
 -ro-change-bar-color: #2ECC40; 
}  
...
```


Dit toont een groene veranderingsbar tegen alle onderwerpen in TOC waar sommige bijgewerkt zijn gedaan. U kunt op het gewijzigde onderwerp in de inhoudsopgave klikken en de gedetailleerde wijzigingen bekijken.

<img src="./assets/changed-bar-TOC.png" alt="Gewijzigde balk" width="500">
