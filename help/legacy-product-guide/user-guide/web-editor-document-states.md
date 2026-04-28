---
title: Documentstatus
description: Leer de typen documentstatussen in AEM Guides. Weet hoe u de documentstatus kunt wijzigen of weergeven en de documentstatus in DDLC kunt gebruiken.
feature: Authoring, Features of Web Editor, Document State
role: User
hide: true
exl-id: f8367f84-dd46-4140-8748-c3bda0cf933a
source-git-commit: a70b3ce942b3e69445ad1d7ba6c8f7542e0ff176
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# Documentstatus {#id1821HC00URO}

Om de gereedheid van de documenten te beheren, biedt AEM Guides de eigenschap documentstatus om de huidige status van het document aan te geven. Met documentstatussen kunt u snel nagaan of een document nieuw is, in de revisie of de voltooide status van de revisie.

## Typen documentstatussen

Voor een document kunnen alle documentstatussen zijn gedefinieerd in het profiel Documentstatus. Een document kan bijvoorbeeld een van de volgende documentstatussen hebben:

- Concept - Geeft aan dat het document wordt gemaakt en opgeslagen met nieuwe wijzigingen.
- In-Review - Geeft aan dat een revisiewerkstroom is gestart voor het document.
- Gereviseerd - Geeft aan dat het document is gereviseerd door de bedoelde gebruikers.

Deze statussen worden handmatig of automatisch ingesteld volgens de profielinstellingen van de documentstatussen. Bijvoorbeeld, als het profiel van de Staat van het Document met beginstaat als Ontwerp wordt gevormd, en de staat In-Overzicht wordt bepaald voor documenten onder overzicht. Dan, wanneer u een document creeert, wordt de documentstaat geplaatst aan *Ontwerp*. Als u een revisietaak start, wordt de status van het document gewijzigd in In-Review.

U kunt de documentstatus voor een of meerdere documenten ook handmatig wijzigen. Als u echter de documentstatus voor meerdere documenten wilt wijzigen, wordt de toegestane status bepaald door de algemene staten die zijn toegestaan voor de geselecteerde documenten. Stel dat u de documentstatussen hebt gedefinieerd als Concept, In-Review, Reviewed en Ready to Publish, in dezelfde volgorde. Voor document one.dita wordt de staat geplaatst aan *Ontwerp* en op document two.dita, wordt de staat geplaatst aan Gereviseerde. Wanneer u zowel—one.dita als two.dita selecteert, dan zal de toegestane documentstaat *klaar zijn om* te publiceren. Aangezien two.dita in *Gereviseerde* staat is, is de volgende mogelijke staat voor two.dita slechts *klaar om* te publiceren, die wordt getoond wanneer beide documenten worden geselecteerd.

>[!NOTE]
>
> Een document kan slechts in één frame tegelijk bestaan.

## Documentstatus wijzigen

Voer de volgende stappen uit om de status van een document te wijzigen:

1. In the Assets UI, select one ore more document for which you want to change the document state.
1. In the main toolbar, click **Properties**.
1. Select the new state from the **Document State** drop-down. You can select only those document states that are allowed in the State Transition section of the Document State profile.

   >[!NOTE]
   >
   >Administrators can see all document states and change the document to any possible state.

1. Klik **sparen &amp; Sluiten**.

## View document state

The card view of the Assets UI shows the current state along with the creation date and size of the respective DITA topic or DITA map.

![](images/document_state.png){width="800" align="left"}

## Use document states in DDLC

Document states play an important role in managing the lifecycle of documents in DDLC. If your organization strictly follows the DDLC, then having a mechanism to control editing documents based on their state becomes an essential feature. For example, you can allow editing documents when they are in *Draft* or *In-review* states. However, once a document is reviewed and is ready to publish, then there should be a way to prevent further modification of documents.

AEM Guides provides document approval workflow, which helps you to control the lifecycle of your document development process. Once a document is ready to publish or has reached the penultimate state, you can mark it as approved. Once a document is approved, AEM Guides creates a new version of the document and makes it read-only. You can then move the document for publishing or create a baseline for further processing.

To start a new release form the documents that are marked as approved, an author has to start a new release. Starting a new release changes the document state to *Draft* again. By changing the document state to *Draft*, the document is again made editable and you can continue working on the next release.

To use the document approval feature, perform the following steps:

>[!NOTE]
>
> The approval workflow feature must be enabled by your administrator. For more details, see *Enable approval workflow* section in the Install and configure Adobe Experience Manager Guides as a Cloud Service.

1. In the Web Editor, open the document that you to mark for approval.

1. Click the **Mark Approved**![](images/mark_approve_icon.svg) icon.

1. Als het document de status heeft die als goedgekeurd moet worden gemarkeerd, wordt het volgende dialoogvenster weergegeven:

   ![](images/mark-approved-correct-state.png){width="300" align="left"}

   Als uw document niet als goedgekeurd kan worden gemerkt, dan wordt het volgende bericht getoond:

   ![](images/mark-approved-incorrect-state.png){width="300" align="left"}

1. Als uw document klaar is om zoals goedgekeurd te worden gemerkt, dan selecteer een etiket van de drop-down lijst en klik **goedkeuren**.

   >[!NOTE]
   >
   > Als uw beheerder geen vooraf gedefinieerde lijst met labels heeft geconfigureerd, wordt u een tekstveld met een vrije vorm getoond waarin u een label kunt invoeren.

1. Zodra het document met succes zoals goedgekeurd wordt gemerkt, dan wordt a **Voorproef** van het document getoond op de read-only wijze.

   ![](images/approved-doc-read-only.png){width="650" align="left"}

   >[!NOTE]
   >
   > In de modus Voorbeeld worden alle bewerkingsopties verwijderd van de werkbalk. Bovendien zijn de weergave Auteur en Source van het document ook verwijderd uit de bovenste navigatie.


Als een document is gemarkeerd als goedgekeurd, kan het niet meer worden bewerkt. Als u het document voor de volgende versie wilt gebruiken, dan moet u het terug naar de *staat van het Ontwerp* brengen. Om de documentstaat van een goedgekeurd document terug naar *Laag* wijze te veranderen, voer de volgende stappen uit:

1. In een goedgekeurd document, klik het **Begin een Nieuw pictogram van de Versie** ![](images/approved-restart-draft-mode-icon.svg).

   Het bericht Nieuwe release starten wordt weergegeven.

1. Klik **bevestigen**.

   De staat van het document wordt veranderd in Ontwerp en het document wordt geopend in de Redacteur van het Web op uitgeeft wijze.


**Bovenliggend onderwerp:**[ Werk met de Redacteur van het Web ](web-editor.md)
