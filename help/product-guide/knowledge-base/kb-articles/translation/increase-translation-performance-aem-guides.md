---
title: Verhoog de vertaalprestaties voor uw DITA-bestanden in AEM hulplijnen
description: Best practices, tips en trucs om de prestaties van DITA-vertaalprojecten in AEM Guides te verbeteren
feature: Translation
role: User, Admin
author: Pulkit Nagpal (punagpal)
exl-id: d7e4f3ae-2143-4767-b7ab-c89f5e5eef59
source-git-commit: 18fe3cbb1439d489d243d98a546ef1095104a863
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# Aanbevolen procedures voor vertaling in AEM Guides

De prestaties voor uw vertaalproject kunnen dalen naarmate de vertaalactiviteit op het systeem in de loop der tijd toeneemt.

Elk vertaalproject produceert veelvoudige gebruikersgroepen voor toegang, die tot een toename van het aantal gebruikersgroepen binnen het systeem leiden. Naarmate het aantal gebruikersgroepen toeneemt, kunnen CRUD-bewerkingen met betrekking tot gebruikersmachtigingen geleidelijk worden vertraagd, wat mogelijk van invloed is op de algemene AEM. Als vertaalprojecten na voltooiing actief blijven, kan dit bovendien een negatief effect hebben op de prestaties van vertaalsynchronisatie tussen AEM en de vertaalleverancier.

**na de hieronder geschetste beste praktijken zal helpen een efficiënt milieu handhaven.**

## Als u werkt met een oudere versie van versie 4.6 (on-prem) of 2404 (cloud):

- Markeer alle projecten als &quot;Inactief&quot; zodra de vertaling is voltooid en goedgekeurd. Het project blijft beschikbaar voor revisie en wordt eenvoudig als inactief gemarkeerd.
   - Als u deze stappen uitvoert, blijven de algemene vertaalprestaties in goede gezondheid behouden.

     ![ Inactief vertaalproject ](../assets/translation/translation-project-image1.png)

- Voor oudere projecten moet de map die als inactief is gemarkeerd, worden verwijderd. Deze map moet worden goedgekeurd en gecontroleerd.
   - Als u deze stappen uitvoert, blijven de algemene vertaalprestaties in goede gezondheid behouden doordat tijdelijke vertaalbestanden en gebruikersgroepen die bij deze projectmap horen, worden opgeschoond.

     ![ Vertaalproject en -map verwijderen ](../assets/translation/translation-project-image2.png)


## Als u aan bent, bouwt u 4.6 of 2404 of later:

U kunt dezelfde stappen blijven volgen als hierboven vermeld. Vanaf versie 4.6/2404 introduceert AEM Guides een editor-instelling waarmee beheerders de automatische verwijdering van vertaalprojecten kunnen uitschakelen.

Verwijs: [ schrapt of maakt automatisch een voltooid vertaalproject ](https://experienceleague.adobe.com/en/docs/experience-manager-guides/using/user-guide/author-content/create-preview-topics/author-content-aem-guides/work-with-web-editor/translate-documents-web-editor#automatically-delete-or-disable-a-completed-translation-project) onbruikbaar

![ Geautomatiseerde montages om vertaalproject in AEM Guides te schrappen en onbruikbaar te maken ](../assets/translation/translation-project-image3.png)
