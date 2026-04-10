---
title: Standaard AEM-woordenboek aanpassen
description: Meer informatie over het standaardwoordenboek voor AEM aanpassen
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Standaard AEM-woordenboek aanpassen {#id209SD8000WU}

De webeditor kan zo worden geconfigureerd dat spellingcontrole van AEM of de spellingcontrole van de browser wordt gebruikt. Als u ervoor kiest om met de spellingcontrole van AEM te werken, dan hebt u de flexibiliteit om uw lijst met aangepaste woorden te definiëren. Deze aangepaste woorden worden vervolgens toegevoegd aan het AEM-woordenboek en deze woorden worden niet gemarkeerd als onjuist in de webeditor.

Op de volgende tabbladen vindt u instructies voor het maken van uw lijst met aangepaste woorden. Deze lijst wordt toegevoegd in het AEM-woordenboek op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Maak het bestand user\_dictionary.txt met een lijst met woorden die u in het aangepaste woordenboek wilt definiëren.

   >[!NOTE]
   >
   > Elk aangepast woord moet op een nieuwe regel worden gedefinieerd.

1. Sla het bestand op de volgende locatie op in uw Cloud Manager Git-opslagplaats:

   /apps/fmdita/config

1. Sla het bestand op.

   Leg de wijzigingen vast en voer de Cloud Manager \(CI/CD\)-pijplijn uit om configuratiewijzigingen te implementeren.


Auteurs moeten hun Web Editor-sessie opnieuw starten om de lijst met aangepaste woorden in het AEM-woordenboek bij te werken.

>[!TAB  Op locatie ]

1. Meld u aan bij AEM en open de CRXDE Lite-modus.

1. Navigeer naar het volgende knooppunt:

   /apps/fmdita/config

1. Maak een nieuw bestand met de naam user\_dictionary.txt.

1. Open het bestand en voeg een lijst toe met woorden die u in het aangepaste woordenboek wilt definiëren.

   In de volgende schermafbeelding ziet u een lijst met aangepaste woorden die aan het bestand user\_dictionary.txt is toegevoegd:

   ![](assets/custom-words-list-dictionary.png){width="650" align="left"}

1. Sla het bestand op en sluit het.


Auteurs moeten hun Web Editor-sessie opnieuw starten om de lijst met aangepaste woorden in het AEM-woordenboek bij te werken.

>[!ENDTABS]

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](customize-overview.md) aan
