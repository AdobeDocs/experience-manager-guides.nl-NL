---
title: Aanbevolen procedures voor het vertalen van inhoud
description: Weet de beste werkwijzen voor het vertalen van inhoud in AEM Guides. Leer hoe u de vertaalservice configureert, een nieuw vertaalproject maakt en de vertaaltaak start.
exl-id: f2a4df86-bba7-434c-b7f9-3587b8a4f9bc
feature: Translation
role: User
source-git-commit: ae36a7fdff6ae147619340aa3a3d2bb6c7774fe0
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Aanbevolen procedures voor het vertalen van inhoud {#id1678G0S702F}

Houd rekening met het volgende punt voor het vertalen van inhoud:

- De map- en bestandsnamen moeten voldoen aan de naamgevingsstandaarden voor bestanden, zoals: er mogen geen spaties, apostrof, accolades, gelijktekens, speciale of niet-ASCII-tekens voorkomen.

- Als u inhoud in verschillende talen vertaalt, moet u omslagen tot stand brengen die aan elke taal beantwoorden. Elk van deze taalomslagen zal de inhoud bevatten die aan die taal beantwoordt. U kunt bijvoorbeeld mappen maken met de taalaanduiding `de` voor Duits, `fr` voor Frans enzovoort. U kunt ook mappen maken met de taal- en regioaanwijzers, zoals `fr-FR` voor Frans, zoals gebruikt in Frankrijk of `fr-CA` voor Frans, zoals gebruikt in Canada.
- In de doeltaal moeten ook de werkelijke landinstellingen worden geselecteerd op basis van de doeltaalmappen op hun exemplaar.
- De cloudconfiguratie moet dezelfde zijn als die van de bronmap en er mag slechts één cloudconfiguratie in één map zijn. U kunt veelvoudige omslagen onder /conf tot stand brengen, als u veelvoudige vertaalschakelaars wilt gebruiken.
- Een map mag niet meer dan 1000 bestanden bevatten.
- Zorg ervoor dat de gebruiker die belast is met het initiëren van het vertaalproces, beschikt over de machtigingen Lezen, Wijzigen, Maken en Verwijderen voor de bronmappen en de doeltaalmappen.
- Aangezien voor het vertalen van inhoud een vertaalproject moet worden gemaakt, moet de gebruiker toegang hebben om een project te maken in Adobe Experience Manager.
- Als u Voorwaardelijke voorinstellingen voor uw kaart wilt gebruiken, moet u deze maken voordat u het vertaalproces start. Omdat Voorwaardelijke voorinstellingen ook in de vertaalde versie van de kaart worden gebundeld, zorgt het creëren van voorinstellingen alvorens het vertaalproces in werking te stellen ervoor dat zij in de vertaalde versie beschikbaar zijn.
- Het proces voor het vertalen van inhoud moet worden gestart vanuit de DITA-kaartconsole en niet vanuit de Adobe Experience Manager Assets-gebruikersinterface.
- De op componenten-gebaseerde DITA-omzettingsworkflow mag niet worden gebruikt als u inhoud via menselijke vertaling vertaalt. Deze optie moet echter worden gebruikt voor machinevertaling.
- De wereldwijd gebruikte inhoud en media die niet hoeven te worden gelokaliseerd, moeten buiten de taalkopieën worden gehouden.
- Alle algemene inhoud die moet worden gelokaliseerd, moet in een gemeenschappelijke omslag onder de taalomslag worden gehouden.

In de volgende afbeelding ziet u een voorbeeld van een mapstructuur in Adobe Experience Manager wanneer u inhoud en drie taalkopieën hebt gebruikt.

![](images/aem-directory_structure.png){width="800" align="left"}

## Vertaalservice configureren

Voer de volgende stappen uit om de te gebruiken service voor het vertalen van mensen of machines te configureren:

1. Selecteer de brontaalmap in de gebruikersinterface van Assets.

1. Open de omslageigenschappen, en ga naar **de Diensten van de Wolk** tabel.

1. In het **lusje van de Diensten van de Wolk**, vorm de vertaaldienst die u wilt gebruiken.

   U kunt op computer gebaseerde of menselijke vertaling configureren.

   Zorg ervoor dat er slechts één configuratie voor vertaalschakelaar in één omslag is. De veelvoudige omslagen kunnen onder /conf worden gecreeerd, als er veelvoudige vertaalschakelaars zijn. Voor de brontaalmap moet een cloudconfiguratie zijn geselecteerd voordat het vertaalproces wordt gestart.

   >[!NOTE]
   >
   > De mening [ Vormend het Kader van de Integratie van de Vertaling ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/integration-framework.html?lang=en) in documentatie van Adobe Experience Manager voor details bij het integreren met de diensten van de derdeconversie.

1. Selecteer **sparen &amp; sluit** om de bijgewerkte omslageigenschappen te bewaren.


## De vertaaltaak starten {#id225IK030OE8}

Voer de volgende stappen uit om de vertaaltaak te starten:

1. In de **console van Projecten**, navigeer aan de projectomslag u voor localisatie creeerde.

1. Selecteer het lokalisatieproject om de detailpagina te openen.

1. Selecteer de pijl op de **tegel van de VertaalBaan**, en selecteer **Begin** van de lijst om het vertaalwerkschema te beginnen.

   >[!NOTE]
   >
   > Als u de vertaalservice Human gebruikt, moet u de inhoud exporteren voor vertaling. Zodra u de vertaalde inhoud hebt, dan moet u het terug in het vertaalproject invoeren.

1. Om het statuut van de vertaalbaan te bekijken, selecteer de ellips bij de bodem van de **tegel van de VertaalBaan**.


Nadat de vertaling voltooit, verandert het statuut van de vertaalbaan in *Klaar aan Overzicht*. Om het vertaalproces te voltooien, moet u de vertaalde exemplaar en activa meta-gegevens van de Taaktegel van de Vertaling in de console van het Project goedkeuren. Als u een nieuw vertaalproject wilt beginnen, mening [ creeer een vertaalproject ](translate-documents-web-editor.md#create-a-translation-project).

>[!NOTE]
>
>- Als u de vertaling voor één of meerdere onderwerpen in een vertaalbaan verwerpt, keert de **Bezig** vertaalstatus van alle verworpen onderwerpen terug naar hun originele status. De status van de bedoelde onderwerpen wordt gecontroleerd en teruggezet volgens de meest recente vertaalstatus. De vertaalbestanden die in de map met de doeltaal zijn gemaakt, worden ook niet verwijderd als de vertaling voor de bestanden is geweigerd.
>- Als u verwerpt, schrapt of annuleert de vertaalbaan voor een onderwerp aanwezig in veelvoudige projecten (voor om het even welke projecten), keert de **Bezig** vertaalstatus van het onderwerp niet terug maar dat project wordt verwijderd uit **Bezig** projectlijst voor dat bepaalde activa.
>- Bovendien, als u annuleert of de vertaalbaan schrapt of het volledige project schrapt, keert de **Bezig** vertaalstatus terug naar hun originele status.

**Bovenliggend onderwerp:**[ het vertaaloverzicht van de Inhoud ](translation.md)
