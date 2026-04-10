---
title: Standaard AEM-woordenboek aanpassen
description: Meer informatie over het standaardwoordenboek voor AEM aanpassen
exl-id: 8bfd3ea7-0be8-4e7a-b389-5face043200b
feature: Web Editor Configuration
role: Admin
level: Experienced
hidefromtoc: true
source-git-commit: 3aadc59f5034828cf319992b7acb32d5a88eaf93
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Standaard AEM-woordenboek aanpassen {#id209SD8000WU}

De webeditor kan zo worden geconfigureerd dat spellingcontrole van AEM of de spellingcontrole van de browser wordt gebruikt. Als u ervoor kiest om met de spellingcontrole van AEM te werken, dan hebt u de flexibiliteit om uw lijst met aangepaste woorden te definiëren. Deze aangepaste woorden worden vervolgens toegevoegd aan het AEM-woordenboek en deze woorden worden niet gemarkeerd als onjuist in de webeditor.

Voer de volgende stappen uit om uw lijst met aangepaste woorden te maken, die wordt toegevoegd in het AEM-woordenboek:

1. Meld u aan bij AEM en open de CRXDE Lite-modus.

1. Navigeer naar het volgende knooppunt:

   /apps/fmdita/config

1. Maak een nieuw bestand met de naam user\_dictionary.txt.

1. Open het bestand en voeg een lijst toe met woorden die u in het aangepaste woordenboek wilt definiëren.

   In de volgende schermafbeelding ziet u een lijst met aangepaste woorden die aan het bestand user\_dictionary.txt is toegevoegd:

   ![](assets/custom-words-list-dictionary.png){width="650" align="left"}

1. Sla het bestand op en sluit het.


Auteurs moeten hun Web Editor-sessie opnieuw starten om de lijst met aangepaste woorden in het AEM-woordenboek bij te werken.

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
