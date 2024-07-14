---
title: Tekstfilters configureren
description: Leer hoe u tekstfilters kunt configureren
exl-id: 180e4ab5-5259-4a00-ac3c-bb1d6814ce0d
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Tekstfilters configureren {#id21BPD0FK0XA}

AEM Guides biedt de functie om te zoeken naar tekst in de bestanden die zich op het geselecteerde pad van de AEM opslagplaats bevinden. Met filterzoekopdrachten kunt u bestanden zoeken in het paneel van de gegevensopslagruimte of door bestanden bladeren. Wanneer u werkt in de webeditor, moet u het bladerdialoogvenster voor bestanden gebruiken om elementen in te voegen, zoals een afbeelding, verwijzing of een toetsverwijzing.

Standaard kunt u bepaalde verbeterde filters gebruiken om de bestanden in de AEM te doorzoeken. U kunt alle DITA-bestanden of niet-DITA-bestanden op het geselecteerde pad filteren. U kunt ook zoeken naar specifieke waarden in de kenmerken van DITA-elementen. U kunt ook zoeken naar bestanden die door de opgegeven gebruiker zijn uitgecheckt.

>[!NOTE]
>
> U kunt ook het algemene profiel configureren en meer filters voor zoeken toevoegen.

Voer de volgende stappen uit om de tekstfilters te configureren:

1. Meld u als beheerder aan bij Adobe Experience Manager.
1. Klik op de **verbinding van Adobe Experience Manager** bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **Profielen van de Omslag**.
1. Klik op de **Globale tegel van het Profiel**.
1. Klik op **de Configuratie van de Redacteur van XML**.
1. Klik op **uitgeven** pictogram op de bovenkant.
1. Download het bestand ui\_config.json.
1. Configureer de filters in het bestand. U kunt ook aangepaste filters toevoegen, zoals in het onderstaande voorbeeld wordt getoond:

   In het volgende codefragment wordt getoond hoe u filteropties DITA-bestanden, niet-DITA-bestanden, DITA-elementen en uitgecheckt door bestanden kunt toevoegen. Het bevat ook een aangepast filter - Markeringen.

   ```json
   [
     {
       "title": "DITA files",
       "property": "jcr:content/metadata/dita_class",
       "operation": "like",
       "children": [
         {
           "title": "DITA Topics",
           "value": "- topic/topic",
           "checked": true
         },
         {
           "title": "DITA Maps",
           "value": "- map/map",
           "checked": true
         }
       ]
     },
     {
       "title": "DITA elements",
       "property": "jcr:content/ditameta",
       "widgetId": "dita_filter",
       "operation": "like"
     },
     {
       "title": "Checked out by",
       "property": "jcr:content/cq:drivelock",
       "operation": "like",
       "itemConfig": {
         "component": "textfield",
         "placeholder": "Checked out by"
       },
       "children": [
         {
           "title": "Check out"
         }
       ]
     },
     {
       "title": "Tags",
       "property": "jcr:content/metadata/cq:tags",
       "itemConfig": {
         "component": "textfield",
         "placeholder": "Enter Tag"
       },
       "children": [
         {
           "title": "Tags"
         }
       ]
     }
   ]
   ```

   In het bovenstaande codefragment is het eerste filter voor DITA-bestanden. De filterdefinitie heeft de volgende parameters:

   - **Titel:** de vertoningsnaam van de filter. Deze titel wordt weergegeven als filteroptie in het bladerdialoogvenster van het bestand.

   - **Bezit:** het bezit in de meta-gegevens van het dossier aan te passen. Als u bijvoorbeeld alleen bestanden wilt toestaan die de metagegevens van de klasse dita\_in hun eigenschap hebben, neemt het eigenschapsfilter &quot;jcr:content/metadata/dita\_class&quot; als waarde.

   - **Verrichting** specificeer &quot;bestaat&quot;om voor bestaan van de waarde aan te passen die in de bezitsparameter wordt gespecificeerd

1. Upload het bijgewerkte bestand ui\_config.json dat de toegevoegde filters bevat.

De geconfigureerde filters zijn beschikbaar in het deelvenster Filters.

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
