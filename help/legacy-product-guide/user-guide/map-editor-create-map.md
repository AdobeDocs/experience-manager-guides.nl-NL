---
title: Een kaart maken
description: Maak een kaart met de Kaarteditor in AEM Guides. Zoek de stappen om een kaartdossier tot stand te brengen dat op een kaartmalplaatje wordt gebaseerd.
feature: Authoring, Map Editor
role: User
hide: true
exl-id: 981ecaeb-9b1f-4c7a-8336-7746a739bedc
source-git-commit: ea597cd14469f21e197c700542b9be7c373aef14
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Een kaart maken {#id176FEN0D05Z}

AEM Guides biedt twee out-of-the-box kaartsjablonen: DITA-kaart en Bookmap. U kunt ook uw eigen kaartsjablonen maken en deze delen met uw auteurs om kaartbestanden te maken.

Voer de volgende stappen uit om een kaartbestand te maken:

1. Navigeer in de gebruikersinterface van Assets naar de locatie waar u het kaartbestand wilt maken.

1. Klik **creëren** \> **Kaart DITA**.

1. Voor de pagina van de Vervaging, selecteer het type van kaartmalplaatjes u **daarna** wilt gebruiken en klikken.

   >[!NOTE]
   >
   > De manier waarop de onderwerpen in een kaartdossier worden bedoeld hangt van het kaartmalplaatje af. Bijvoorbeeld, als u het malplaatje van de Kaart selecteert, dan worden de onderwerpverwijzingen \ (`topicref` \) gebruikt om naar onderwerpen te verwijzen. In het geval van een Bookmap, worden de onderwerpverwijzingen gecreeerd gebruikend het `chapter` element in DITA.

   ![](images/map-template.png){width="650" align="left"}

1. Voor de pagina van Eigenschappen, specificeer de kaart **Titel**.

1. \ (Facultatief \) specificeer het dossier **Naam**.

   Als uw beheerder automatische bestandsnaam heeft geconfigureerd op basis van de UUID-instelling, ziet u geen optie om de bestandsnaam op te geven. Er wordt automatisch een op UUID gebaseerde bestandsnaam toegewezen aan het bestand.

   Als de optie voor het benoemen van bestanden beschikbaar is, wordt ook de naam automatisch voorgesteld op basis van de titel van uw kaart. Als u de naam van het kaartbestand handmatig wilt opgeven, moet u ervoor zorgen dat de bestandsnaam geen spaties, apostrof of accolades bevat en eindigt met `.ditamap` .

1. Klik **creëren**.

   Het bericht Kaart gemaakt wordt weergegeven.

   Elk nieuw kaartdossier dat u van Assets UI **creeert** \> **Kaart DITA** of de Redacteur van het Web wordt toegewezen een unieke kaartidentiteitskaart Bovendien wordt de nieuwe kaart opgeslagen als de meest recente werkkopie in DAM. Totdat u een revisie van een pas gemaakte kaart opslaat, ziet u geen versienummer in de Versiegeschiedenis. Als u de kaart opent om te bewerken, wordt de versie-informatie weergegeven in de rechterbovenhoek van het tabblad van het kaartbestand:

   ![](images/first-version-map-none.png){width="650" align="left"}

   De versieinformatie voor een pas gecreëerde kaart wordt getoond als *niets*. Wanneer u een nieuwe versie opslaat, krijgt deze een versienummer toegewezen als 1.0. Voor meer informatie over het bewaren van een nieuwe versie, zie [&#x200B; sparen als Nieuwe Versie &#x200B;](web-editor-features.md#save-as-new-version-id209ME400GXA).

   U kunt de kaart openen om te bewerken in de geconfigureerde kaarteditor, of het kaartbestand opslaan in de AEM-opslagplaats.

   >[!NOTE]
   >
   > Om de Geavanceerde Redacteur van de Kaart te gebruiken, heb toegang tot het kaartdossier in de Redacteur van het Web. Als uw beheerder de Geavanceerde Redacteur van de Kaart als standaardredacteur in de kaartdossiers heeft gevormd, dan wordt het kaartdossier geopend direct in de Geavanceerde Redacteur van de Kaart voor het uitgeven. Zie *plaats de Geavanceerde Redacteur van de Kaart als standaard* sectie in installeer en vorm Adobe Experience Manager Guides as a Cloud Service.


**Bovenliggend onderwerp:**&#x200B;[&#x200B; Werk met de Redacteur van de Kaart &#x200B;](map-editor.md)
