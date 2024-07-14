---
title: Filters configureren voor het dialoogvenster Bladeren
description: Leer hoe u filters voor bladeren door bestanden kunt configureren
exl-id: 1ef2cec8-2e77-40c1-9ed2-324048bf65fb
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# Filters configureren voor het dialoogvenster Bladeren {#id20CIL7009GN}

Wanneer u werkt in de webeditor, moet u het bladerdialoogvenster voor bestanden gebruiken om elementen in te voegen, zoals een afbeelding, verwijzing of een toetsverwijzing. Het standaarddialoogvenster voor bladeren naar bestanden biedt geen filteroptie. U kunt uw eigen filters toevoegen waarmee u de vereiste bestanden snel en gemakkelijk kunt openen.

Voer de volgende stappen uit om uw aangepaste filteropties voor bestanden toe te voegen aan het bladerdialoogvenster van het bestand:

1. U kunt als beheerder het configuratiebestand van de gebruikersinterface downloaden door u aan te melden bij Adobe Experience Manager.

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **Profielen van de Omslag**.
1. Klik op de **Globale tegel van het Profiel**.
1. Selecteer het **lusje van de Configuratie van de Redacteur van XML** en klik **uitgeven** pictogram op de bovenkant
1. Klik het **pictogram van de Download** om het ui \_config.json- dossier op uw lokaal systeem te downloaden. Vervolgens kunt u wijzigingen in het bestand aanbrengen en het bestand vervolgens uploaden.
1. Voeg in het `ui_config.json` -bestand de definitie toe van de filters die u wilt toevoegen.

   In het volgende codefragment ziet u hoe u twee filteropties kunt toevoegen: DITA-bestanden en afbeeldingsbestanden.

   ```
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

   titel
:   De weergavenaam van het filter. Deze titel wordt weergegeven als filteroptie in het bladerdialoogvenster van het bestand.

   eigenschap
:   De eigenschap die moet overeenkomen met de metagegevens van het bestand. Als u bijvoorbeeld alleen die bestanden wilt toestaan die de metagegevens `dita_class` in hun eigenschap hebben, gebruikt het eigenschapsfilter &quot; `jcr:content/metadata/dita_class`&quot; als waarde.

   bewerking
:   Geef &quot; `exists`&quot; op, zodat deze overeenkomt met de waarde die in de parameter property is opgegeven.

   Het tweede filter is voor de Dossiers van het Beeld. De parameters zijn vergelijkbaar met het eerste filter, behalve de parameter `value` . De parameter `value` neemt een array van afbeeldingstypen als waarde. Alle bestandstypen die in de parameter value zijn opgegeven, worden doorzocht en weergegeven in het bladerdialoogvenster. Alle andere bestandstypen worden genegeerd.

1. Sparen het {*dossier 0} ui\_config.json en upload het zelfde.* Laad vervolgens de webeditor opnieuw.

   Wanneer u het bladerdialoogvenster start, worden de filteropties weergegeven die in het bestand ui\_config.json zijn geconfigureerd.

   ![](assets/file-browse-custom-filters.png)


**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
