---
title: AEM standaardwoordenboek aanpassen
description: Leer hoe u AEM standaardwoordenboek kunt aanpassen
exl-id: 8bfd3ea7-0be8-4e7a-b389-5face043200b
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# AEM standaardwoordenboek aanpassen {#id209SD8000WU}

De Redacteur van het Web kan worden gevormd om AEM spellingcontrole of browser spellingcontrole te gebruiken. Als u ervoor kiest om te werken met AEM spellingcontrole, hebt u de flexibiliteit om uw lijst met aangepaste woorden te definiëren. Deze aangepaste woorden worden vervolgens toegevoegd aan het AEM en deze woorden worden niet gemarkeerd als onjuist in de webeditor.

Voer de volgende stappen uit om uw lijst van douanewoorden tot stand te brengen, die in AEM woordenboek wordt toegevoegd:

1. Meld u aan bij AEM en open de modus CRXDE Lite.

1. Navigeer naar het volgende knooppunt:

   /apps/fmdita/config

1. Maak een nieuw bestand met de naam user\_dictionary.txt.

1. Open het bestand en voeg een lijst toe met woorden die u in het aangepaste woordenboek wilt definiëren.

   In de volgende schermafbeelding ziet u een lijst met aangepaste woorden die aan het bestand user\_dictionary.txt is toegevoegd:

   ![](assets/custom-words-list-dictionary.png){width="650" align="left"}

1. Sla het bestand op en sluit het.


Auteurs moeten hun Web Editor-sessie opnieuw starten om de lijst met aangepaste woorden in AEM woordenboek bij te werken.

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
