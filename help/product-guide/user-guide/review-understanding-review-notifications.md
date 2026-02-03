---
title: Herzieningsmeldingen
description: Leer meer over verschillende typen revisiemeldingen en hoe deze worden geactiveerd tijdens de verschillende fasen van de revisiewerkstroom in Experience Manager Guides.
feature: Reviewing
role: User
exl-id: dc452e7d-a317-4168-8015-9fa4a06666ea
source-git-commit: 16688221c35e0b24c51cbff27953a93892cd0944
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# Herzieningsmeldingen

>[!IMPORTANT]
>
> De nieuwe functies die in dit artikel worden beschreven, zijn standaard ingeschakeld met de release van 2508 Experience Manager Guides als Cloud Services. Revisies die vóór de migratie zijn gemaakt, worden niet beïnvloed en blijven gebruikmaken van de eerdere workflow. Als u de bestaande functies zonder deze updates wilt blijven gebruiken, neemt u contact op met het team voor succes van de klant om de nieuwe functies uit te schakelen.

Experience Manager Guides stroomlijnt de samenwerking tussen auteurs en revisoren via een gestructureerde revisieworkflow. Als onderdeel van deze workflow spelen meldingen een sleutelrol bij het informeren van alle deelnemers aan een revisietaak en het reageren op wijzigingen.

Wanneer een aan een revisie gerelateerde actie wordt uitgevoerd, zoals taaktoewijzing, voltooiing, of terugkoppelen updates, wordt automatisch een bericht verzonden naar de betrokken gebruikers van de overzichtstaak om hun directe aandacht te vestigen. Deze meldingen worden in twee indelingen verzonden:

- **de berichten van AEM**: Weergegeven binnen de interface van AEM.
- **E-mailberichten**: Verzonden rechtstreeks naar inbox van de gebruiker.

In de onderstaande tabel vindt u een overzicht van de verschillende typen revisiemeldingen, de acties die deze activeren en de manier waarop deze worden weergegeven in verschillende indelingen:


## Meldingsindelingen controleren met samplewaarden

| **actie van het Overzicht** | **titel van het Bericht (AEM)** | **tekst van het Bericht (AEM)** | **E-mailonderwerp** | **Tekst van het e-mailbericht** | **Ontvanger** |
|-----------------------------|--------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------|------------------------------------------------------------------------------------------------|-----------------------------|
| Taak controleren is gemaakt | Toegewezen taak van het overzicht: **Overzicht van de Homepage** | Toegewezen door **Auteur** | Toegewezen taak van het overzicht: **Overzicht van de Homepage** | **Auteur** heeft tot een overzichtTaak **Overzicht van de Homepage** in project **WebDocs Revamp** met datum **15 Aug 2025** geleid. U bent toegewezen als revisor. | **Recensent** |
| Feedback verzonden | Het overzicht koppelt voor **Overzicht van de Homepage** wordt ontvangen | Terugkoppeling van **Recensent** | Het overzicht koppelt voor **Overzicht van de Homepage** wordt ontvangen | **Recensent** heeft voorgelegd terugkoppelt voor taak **Overzicht van de Homepage** in project **WebDocs Revamp**. Gelieve te herzien en noodzakelijke updates ver vóór vervaldatum **15 Aug 2025** te maken. | **Auteur** of **Initiator van taak** |
| Herbeoordeling aangevraagd | Heronderzoek verzocht om **Overzicht van de Homepage** | Gevraagd door **Auteur** | Heronderzoek verzocht voor **Overzicht van de Homepage** door **Auteur** | **de Auteur** heeft het document voor taak **Overzicht van de Homepage** bijgewerkt dat op uw wordt gebaseerd terugkoppelt en verzoekt om een herbeoordeling. Gelieve te herzien ruim vóór vervaldatum **15 aug 2025**. | **Recensent** |
| Revisie gesloten | De taak van het overzicht sloot: **Overzicht van de Homepage** | Gesloten door **Auteur** | De taak van het overzicht sloot: **Overzicht van de Homepage** | Het overzicht van de overzichtstaak **Overzicht van de Homepage** onder project **WebDocs Revamp** is gesloten door **Auteur**. | **Auteur** of **Initiator van taak**, **Recensent** |
| Revisor niet toegewezen | Niet toegewezen van het Overzicht van de overzichtstaak **Homepage** | Niet toegewezen door **Auteur** | Niet toegewezen van het Overzicht van de overzichtstaak **Homepage** | U bent niet toegewezen van het overzicht taak **Overzicht van de Homepage** onder project **WebDocs Revamp** door **Auteur**. | **Recensent** |
| Tagverwijzing | Vermeldenseerd in de commentaar van de overzichtstaak voor **Overzicht van de Homepage** | Vernoemd door **Auteur** | Vermeldenseerd in de commentaar van de overzichtstaak voor **Overzicht van de Homepage** | U bent vermeld in een commentaar op taak **Overzicht van de Homepage** onder **WebDocs Revamp** door **Auteur**. **uittreksel van de Commentaar:** *&quot;Gelieve te werken de kopstructuur bij om toegankelijkheidsrichtlijnen te volgen.&quot;* | **Vermelde gebruiker** |
| Inhoud bijgewerkt tijdens revisie | Onderwerp dat in overzicht wordt bijgewerkt taak **Overzicht van de Homepage** | Bijgewerkt door **Auteur** | Onderwerp dat in overzicht wordt bijgewerkt taak **Overzicht van de Homepage** | **Auteur** heeft de onderwerpversies voor het overzicht van de taak **Overzicht van de Homepage** bijgewerkt. Gelieve te herzien ruim vóór vervaldatum **15 aug 2025**. | **Recensent** |
| Onderwerpen die zijn toegevoegd, verwijderd of bijgewerkt terwijl een revisietaak bezig is met revisoren | De onderwerpen die in overzichtTaak **Overzicht van de Homepage** worden bijgewerkt | Bijgewerkt door **Auteur** | De onderwerpen die in overzichtTaak **Overzicht van de Homepage** worden bijgewerkt | **Auteur** heeft de onderwerpversies voor het overzicht van de taak **Overzicht van de Homepage** bijgewerkt. Gelieve te herzien ruim vóór vervaldatum **15 aug 2025**. | **Recensent** |


In de bovengenoemde lijst, vertegenwoordigt de **tekst in vette** steekproefwaarden en door vooraf bepaalde variabelen gedreven die in berichten kunnen worden gebruikt.


Bijvoorbeeld:

- **Overzicht van de Homepage** is een naam van de steekproeftaak.
- **Priya** (Auteur) en **John** (Recensent) zijn namen van steekproefgebruikers.
- **WebDocs Revamp** is een naam van het steekproefproject.
- **15 Aug 2025** is een steekproef vervaldatum.

Als een taak opmerkingen bevat, wordt bovendien een commentaarfragment (een deel van de volledige opmerking) opgenomen in het e-mailbericht. Het fragment wordt in de volgende gevallen weergegeven:

- Wanneer u een opmerking van tags hebt voorzien, wordt een fragment van de gelabelde opmerking weergegeven in het e-mailbericht.
- Wanneer een opmerking op taakniveau wordt toegevoegd aan een revisietaak waarvan u deel uitmaakt, wordt een fragment van die opmerking weergegeven in het e-mailbericht.

Voor een volledige lijst van vooraf bepaalde variabelen en de aanpassing van het overzichtsbericht, vormt de mening [&#x200B; en past werkschema&#39;s &#x200B;](../cs-install-guide/customize-workflows.md#customize-email-and-aem-notification-templates) aan.




**Bovenliggend onderwerp:**&#x200B;[&#x200B; Inleiding aan overzicht &#x200B;](review.md)
