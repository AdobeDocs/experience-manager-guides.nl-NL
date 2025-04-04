---
title: Filters configureren voor het dialoogvenster Bladeren
description: Leer hoe u filters voor bladeren door bestanden kunt configureren
exl-id: 1ef09820-3b18-4762-b177-4d40926e21f0
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# Filters configureren voor het dialoogvenster Bladeren {#id20CIL7009GN}

Wanneer u werkt in de webeditor, moet u het bladerdialoogvenster voor bestanden gebruiken om elementen in te voegen, zoals een afbeelding, verwijzing of een toetsverwijzing. Het standaarddialoogvenster voor bladeren naar bestanden biedt geen filteroptie. U kunt uw eigen filters toevoegen waarmee u de vereiste bestanden snel en gemakkelijk kunt openen.

Voer de volgende stappen uit om uw aangepaste filteropties voor bestanden toe te voegen aan het bladerdialoogvenster van het bestand:

1. Meld u aan bij AEM en open de modus CRXDE Lite.

1. Navigeer naar het standaardconfiguratiebestand dat beschikbaar is op de volgende locatie:

   `/libs/fmdita/clientlibs/clientlibs/xmleditor/ui_config.json`

1. Maak een kopie van het standaardconfiguratiebestand op de volgende locatie:

   `/apps/fmdita/xmleditor/ui_config.json`

1. Navigeer naar het `ui_config.json` -bestand in het knooppunt `apps` en open het voor bewerking.

1. Voeg in het `ui_config.json` -bestand de definitie toe van de filters die u wilt toevoegen.

   In het volgende codefragment ziet u hoe u twee filteropties kunt toevoegen: DITA-bestanden en afbeeldingsbestanden.

   ```json
   "browseFilters": [
       {
         "title": "DITA Files",
         "property": "jcr:content/metadata/dita_class",
         "operation": "exists"
       },
       {
         "title": "Image Files",
         "property": "jcr:content/metadata/dc:format",
         "value": [        
           "image/jpeg",
           "image/gif",
           "image/png"
         ]
       }
   ]
   ```

   In het bovenstaande codefragment is het eerste filter voor DITA-bestanden. De filterdefinitie heeft de volgende parameters:

   - **titel:**   De weergavenaam van het filter. Deze titel wordt weergegeven als filteroptie in het bladerdialoogvenster van het bestand.

   - **bezit:**   De eigenschap die moet overeenkomen met de metagegevens van het bestand. Bijvoorbeeld, om slechts die dossiers toe te staan die `dita_class` meta-gegevens in hun bezit hebben, neemt de bezitsfilter &quot; `jcr:content/metadata/dita_class`&quot;als zijn waarde.

   - **verrichting:**   Specificeer &quot;`exists`&quot;om voor bestaan van de waarde aan te passen die in de bezitsparameter wordt gespecificeerd.

   Het tweede filter is voor de Dossiers van het Beeld. De parameters zijn vergelijkbaar met het eerste filter, behalve de parameter `value` . De parameter `value` neemt een array van afbeeldingstypen als waarde. Alle bestandstypen die in de parameter value zijn opgegeven, worden doorzocht en weergegeven in het bladerdialoogvenster. Alle andere bestandstypen worden genegeerd.

1. Sparen het {*dossier 0} ui\_config.json en laad de Redacteur van het Web opnieuw.*

   Wanneer u het bladerdialoogvenster start, worden de filteropties weergegeven die in het bestand ui\_config.json zijn geconfigureerd.

   ![](assets/file-browse-custom-filters.png){width="300" align="left"}
