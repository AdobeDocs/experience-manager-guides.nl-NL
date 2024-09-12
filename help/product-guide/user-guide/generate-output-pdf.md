---
title: PDF genereren
description: Leer hoe u een PDF-voorinstelling maakt in de webeditor en het kaartdashboard. PDF-uitvoervoorinstelling configureren in AEM Guides.
exl-id: f12c91fd-3f95-478e-a9cd-68d037206ee8
feature: Publishing
role: User
source-git-commit: c2a97a134b9e7367689778a2a1e1f4bbead9860b
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 0%

---

# PDF {#id205BE600HAH}

U kunt de voorinstelling PDF op twee manieren maken:

**van de Redacteur van het Web:** in het paneel van de Bewaarplaats, open het DITA kaartdossier in de Mening van de Kaart, dan in het lusje van de Output, selecteer + pictogram om tot een outputvoorinstelling te leiden, en selecteer dan PDF van het type drop-down in Add vooraf ingestelde dialoog.

>[!NOTE]
>
> U kunt de methode kiezen om PDF te produceren gebruikend DITA-OT, Inheemse PDF, of FMPS \(als uw systeembeheerder het \) heeft gevormd.

In de redacteur van het Web zijn de configuraties georganiseerd onder Algemene en Geavanceerde lusjes:

**Algemeen**

Het **Algemene** lusje bevat de volgende configuraties:

- Uitvoerpad
- Argumenten DITA-OT-opdrachtregel
- Transformatienaam
- Bestandsnaam PDF
- Voorwaarden toepassen met \(als de voorwaarden voor een kaart zijn gedefinieerd\)
- Basislijn gebruiken \(als een basislijn is gemaakt voor een kaart\)
- Workflow na generatie

**Geavanceerd**

Het tabblad Geavanceerd bevat de volgende configuraties:

- Versiering inschakelen
- Tijdelijke bestanden behouden

Voor details, verwijs naar [ PDF configuratie ](#id231KIM004X1).

**van het kaartdashboard**

Als u uitvoervoorinstellingen voor PDF wilt openen, klikt u op een DITA-toewijzingsbestand in de Assets-interface en klikt u vervolgens op Voorinstellingen uitvoer. Klik vervolgens op de optie PDF. In het dashboard van de Kaart, geeft de klik **** op de bovenkant uit om de diverse configuraties bij te werken, en klikt dan **sparen**.

**PDF configuratie**

De volgende opties zijn beschikbaar voor de Uitvoer van PDF:

| PDF-opties | Beschrijving |
| --- | --- |
| Uitvoertype | Het type uitvoer dat u wilt genereren. Als u PDF-uitvoer wilt genereren, kiest u de optie PDF. |
| Naam instellen | Geef een beschrijvende naam voor de PDF-uitvoerinstellingen die u maakt. Bijvoorbeeld, kunt u _Interne klantenoutput_ of _eind-gebruikers output_ specificeren. |
| Argumenten DITA-OT-opdrachtregel | Geef de aanvullende argumenten op die u tijdens het genereren van uitvoer wilt laten verwerken door DITA-OT. Voor details over de bevel-lijn argumenten die in DITA-OT worden gesteund, zie [ documentatie DITA-OT ](https://www.dita-ot.org/). |
| Voorwaarden toepassen met | Selecteer één van de volgende opties:<br><br>* **toegepaste niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>* **DITAVal dossier**: Selecteer DITAVal dossier(s) om gepersonaliseerde inhoud te produceren. U kunt meerdere DITAVal-bestanden selecteren via het dialoogvenster Bladeren of door een bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVal-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVal-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch verwijderd van het kaartdashboard. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad te zien in de AEM opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVal-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype hebt geselecteerd. FrameMaker Publishing Server ondersteunt geen meerdere DITAVAL-bestanden.<br>* **Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. De optie is zichtbaar als u een voorwaarde hebt toegevoegd op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Om meer over vooraf ingestelde voorwaarde te weten, zie [ Voorinstellingen van het Gebruik ](generate-output-use-condition-presets.md#id1825FL004PN). |
| PDF genereren met | Selecteer DITA-OT om de PDF te genereren. |
| Workflow na generatie uitvoeren | Wanneer u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Werkstroom na generatie weergegeven met alle werkstromen die in AEM zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid.<br><br>**Nota**: Voor meer informatie over het creëren van een douanewerkschema van de post-output generatie, zie het werkschema van de post-output generatie aanpassen in installeer en vorm Adobe Experience Manager Guides as a Cloud Service. |
| Transformatienaam | Geef het type uitvoer op dat u wilt genereren. Dit is vereist als u uitvoer wilt genereren met uw eigen aangepaste plug-in, die is geïntegreerd in de DITA-OT-plug-in. Als u bijvoorbeeld XHTML-uitvoer wilt genereren, geeft u `xhtml` op. Voor een lijst van transformaties beschikbaar in DITA-OT, zie [ transformaties DITA-OT (outputformaten) ](http://www.dita-ot.org/2.3/user-guide/AvailableTransforms.html) in de Gids van de Gebruiker van OASIS DITA-OT. |
| Bestandsnaam | Geef de bestandsnaam op waarmee u de PDF wilt opslaan.<br><br> u kunt variabelen ook gebruiken terwijl het plaatsen van de Naam van het Dossier van de PDF. Voor meer details over het gebruiken van variabelen, zie [ variabelen van het Gebruik voor het plaatsen van de Weg van de Bestemming, de Naam van de Plaats, of de opties van de Naam van het Dossier ](generate-output-use-variables.md#id18BUG70K05Z).<br><br>**Nota**: Als u geen dossier verstrekt - noem, dan wordt de titel van de kaart DITA gebruikt om het definitieve dossier van de PDF te produceren. Als de kaart geen titel heeft, dan wordt de het dossiernaam van de kaart DITA gebruikt aan naam de definitieve PDF. De bestandsnaam wordt ontsmet volgens de regels die in het systeem zijn geconfigureerd voor het verwerken van elk ongeldig teken. |
| Doelpad | Het pad in uw AEM opslagplaats waar de PDF is opgeslagen.<br><br> u kunt variabelen ook gebruiken terwijl het plaatsen van de Weg van de Bestemming. Voor meer details over het gebruiken van variabelen, zie [ variabelen van het Gebruik voor het plaatsen van de Weg van de Bestemming, de Naam van de Plaats, of de opties van de Naam van het Dossier ](generate-output-use-variables.md#id18BUG70K05Z). |
| Tijdelijke bestanden behouden | Selecteer deze optie om de tijdelijke bestanden te behouden die door DITA-OT worden gegenereerd. Als er fouten optreden bij het genereren van uitvoer via DITA-OT, selecteert u deze optie om de tijdelijke bestanden te behouden. U kunt die dossiers dan gebruiken om de fouten van de outputgeneratie problemen op te lossen.<br> <br> Na het produceren van de output, selecteer het **tijdelijke dossiers van de Download** ![ pictogram van de download tijdelijke dossiers ](images/download-temp-files-icon.png) om de omslag te downloaden van het PIT die de tijdelijke dossiers bevat. <br><br> **Nota**: Als de dossiereigenschappen tijdens generatie worden toegevoegd, omvatten de output tijdelijke dossiers ook a *metadata.xml* dossier die die eigenschappen bevatten. |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br> zie [ Werk met Basislijn ](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer detail. |
| Bestandseigenschappen | Selecteer de eigenschappen die u als metagegevens wilt verwerken. Deze eigenschappen worden ingesteld op de pagina Eigenschappen van de DITA-kaart of het bladwijzerbestand. De eigenschappen u van de dropdown lijst selecteert verschijnen onder het **gebied van de Eigenschappen van het Dossier 0} {.** Selecteer het kruispictogram naast de eigenschap om deze te verwijderen. <br><br> Nota: U kunt de meta-gegevens tot de output ook overgaan gebruikend DITA-OT het publiceren. Voor meer details zie, [ pas op de meta-gegevens aan de output over gebruikend DITA-OT ](pass-metadata-dita-ot.md#id21BJ00QD0XA). |

**Bovenliggend onderwerp:**[ Begrijpend de output stelt ](generate-output-understand-presets.md) vooraf in
