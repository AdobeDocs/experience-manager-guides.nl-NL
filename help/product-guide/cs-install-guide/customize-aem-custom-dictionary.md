---
title: Standaard AEM-woordenboek aanpassen
description: Meer informatie over het standaardwoordenboek voor AEM aanpassen
exl-id: ecffcd14-6728-4938-a209-5c4b12af6fbb
feature: Web Editor Configuration
role: Admin
level: Experienced
hidefromtoc: true
source-git-commit: 564ee1731be2378744ffd2ed54a2fd423901a0b3
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# Standaard AEM-woordenboek aanpassen {#id209SD8000WU}

De webeditor kan zo worden geconfigureerd dat spellingcontrole van AEM of de spellingcontrole van de browser wordt gebruikt. Als u ervoor kiest om met de spellingcontrole van AEM te werken, dan hebt u de flexibiliteit om uw lijst met aangepaste woorden te definiëren. Deze aangepaste woorden worden vervolgens toegevoegd aan het AEM-woordenboek en deze woorden worden niet gemarkeerd als onjuist in de webeditor.

Voer de volgende stappen uit om uw lijst met aangepaste woorden te maken, die wordt toegevoegd in het AEM-woordenboek:

1. Maak het bestand user\_dictionary.txt met een lijst met woorden die u in het aangepaste woordenboek wilt definiëren.

   >[!NOTE]
   >
   > Elk aangepast woord moet op een nieuwe regel worden gedefinieerd.

1. Sla het bestand op de volgende locatie op in uw Cloud Manager Git-opslagplaats:

   /apps/fmdita/config

1. Sla het bestand op.

   Leg de wijzigingen vast en voer de Cloud Manager \(CI/CD\)-pijplijn uit om configuratiewijzigingen te implementeren.


Auteurs moeten hun Web Editor-sessie opnieuw starten om de lijst met aangepaste woorden in het AEM-woordenboek bij te werken.

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
