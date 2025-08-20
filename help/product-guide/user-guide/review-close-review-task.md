---
title: Nieuwe revisie aanvragen of een revisietaak als auteur sluiten
description: Meer informatie over de workflow voor het sluiten van een revisietaak of het opnieuw aanvragen van een revisie als auteur in Experience Manager Guides.
feature: Reviewing
role: User
source-git-commit: b7648fe1d36de3c243ca5a55f42a41f7523056ce
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# Nieuwe revisie aanvragen of een revisietaak als auteur sluiten

>[!IMPORTANT]
>
> De nieuwe functies die in dit artikel worden beschreven, zijn standaard ingeschakeld met de release van 2508 Experience Manager Guides als Cloud Services. Revisies die vóór de migratie zijn gemaakt, worden niet beïnvloed en blijven gebruikmaken van de eerdere workflow. Als u de bestaande functies zonder deze updates wilt blijven gebruiken, neemt u contact op met het team voor succes van de klant om de nieuwe functies uit te schakelen.

Wanneer een overzichtstaak wordt duidelijk zoals voltooid door een Recensent, wordt een bericht teweeggebracht aan de taakinitiatiefnemer, toelatend hen om tot de taak en verwante commentaren op taakniveau toegang te hebben en te herzien.

Als initiatiefnemer van de overzichtstaak, kunt u dan beslissen hoe te te te werk te gaan gebaseerd op terugkoppelt. De beschikbare opties zijn:

- Nieuwe beoordeling aanvragen
- De revisietaak sluiten

## Nieuwe revisie aanvragen of een revisietaak sluiten

Voer de volgende stappen uit om een revisie aan te vragen of een revisietaak te sluiten:

1. Open de revisietaak in de Editor.
2. In het paneel van het Overzicht, selecteer de overzichtstaak van de **Actieve taken** lijst.

   >[!NOTE]
   >
   > U kunt de taak ook in het taakdashboard openen voor een uitgebreidere weergave. Om dit te doen, selecteer **Open in taakdashboard** van het menu van Opties van om het even welke actieve overzichtstaak. Dit opent de taakdetails in de console van Projecten.

   ![](images/task-dashboard-selection-author-view.png)
3. Selecteer de **commentaren van de Taak** dialoog om tot de commentaren van het taakniveau toegang te hebben en te herzien die door de Recensent worden toegevoegd.

   ![](images/task-comments-selection-author-view.png).

   De **commentaren van de Taak** dialoog wordt getoond op het recht.

   ![](images/task-comments-dialog-editor.png){width="350" align="left"}.
4. Selecteer **de taak van de Update** om verdere actie op de geselecteerde overzichtstaak te voeren.
5. In de **taak van de Update** dialoog, kies één van de volgende acties:

   - **verzoek een herbeoordeling**: Initieert een andere ronde van overzicht. U kunt een andere versie van het onderwerp voor overzicht selecteren. Door gebrek, wordt de recentste (of laatste-uitgegeven) versie van het onderwerp of kaartdossier die voor overzicht wordt verzonden geselecteerd. Revisoren die de vorige revisie hebben voltooid, ontvangen een melding om feedback te geven over de bijgewerkte versie. Andere Revisoren, die de overzichtstaak niet als volledig hebben gemerkt, worden op de hoogte gebracht over de onderwerpupdate.

   - **dicht overzicht**: Sluit de overzichtstaak. De **taak van de Update** knoop aanwezig bij de bodem van het paneel van het Overzicht verandert in **Gesloten** en een bericht wordt verzonden naar alle gebruikers betrokken bij de overzichtstaak die op zijn sluiting wijzen.

   Voor meer details op hoe de heroverwegingsberichten teweegbrengen, mening [ het Begrip van heroverwegingsberichten ](./review-understanding-review-notifications.md).

   ![](images/update-task-dialog.png).

6. Selecteer **bevestigen**.


Als Auteur of initiatiefnemer van een overzichtstaak, wanneer u de taak sluit, wordt de **taak van de Update** knoop huidig bij de bodem van het paneel van het Overzicht veranderd in **Gesloten**, die op de taak wijzen niet meer actief is.

![](images/review-task-status-closed-review-panel.png){width="350" align="left"}

Ook, blijft de **taak van de Update** knoop huidig in het paneel van het Overzicht gehandicapt voor de andere gebruikers van de overzichtstaak. Bijvoorbeeld, als één van de recensenten van een overzichtstaak, als u de taak in de Redacteur opent, zal de de taakknoop van de Update met een bericht **worden onbruikbaar gemaakt u hebt geen toestemming om op deze taak** te handelen. Alleen de aanvrager van een revisietaak heeft toestemming om de taak bij te werken vanuit de Editor.

![](images/update-task-button-disabled.png){width="350" align="left"}