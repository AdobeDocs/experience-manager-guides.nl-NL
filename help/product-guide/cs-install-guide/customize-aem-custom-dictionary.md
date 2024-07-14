---
title: AEM standaardwoordenboek aanpassen
description: Leer hoe u AEM standaardwoordenboek kunt aanpassen
exl-id: ecffcd14-6728-4938-a209-5c4b12af6fbb
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# AEM standaardwoordenboek aanpassen {#id209SD8000WU}

De Redacteur van het Web kan worden gevormd om AEM spellingcontrole of browser spellingcontrole te gebruiken. Als u ervoor kiest om te werken met AEM spellingcontrole, hebt u de flexibiliteit om uw lijst met aangepaste woorden te definiëren. Deze aangepaste woorden worden vervolgens toegevoegd aan het AEM en deze woorden worden niet gemarkeerd als onjuist in de webeditor.

Voer de volgende stappen uit om uw lijst van douanewoorden tot stand te brengen, die in AEM woordenboek wordt toegevoegd:

1. Maak het bestand user\_dictionary.txt met een lijst met woorden die u in het aangepaste woordenboek wilt definiëren.

   >[!NOTE]
   >
   > Elk aangepast woord moet op een nieuwe regel worden gedefinieerd.

1. Sla het bestand op de volgende locatie op in uw Cloud Manager Git-opslagplaats:

   /apps/fmdita/config

1. Sla het bestand op.

   Leg de wijzigingen vast en voer de Cloud Manager \(CI/CD\)-pijplijn uit om configuratiewijzigingen te implementeren.


Auteurs moeten hun Web Editor-sessie opnieuw starten om de lijst met aangepaste woorden in AEM woordenboek bij te werken.

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
