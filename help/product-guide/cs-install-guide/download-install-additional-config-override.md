---
title: Configuratieoverschrijvingen
description: Leer hoe te om met voeten te treden van de Configuratie
exl-id: dc5f81f7-5b0a-4d12-a944-ba66b0239d5c
feature: Installation
role: Admin
level: Experienced
source-git-commit: e4b213b5f0efda18fb24f100f3ee8237947890bf
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Configuratieoverschrijvingen {#id216IFC003XA}

Voor het maken van om het even welke configuratieupdates, zou de volgende generische benadering moeten worden gebruikt:

1. Open de Cloud Manager Git-opslagplaats.

1. Maak een nieuw JSON-bestand op de volgende locatie:

   src/main/content/jcr\_root/apps/fmditaCustom/config/

1. Geef het bestand een naam in de volgende indeling:

   $\{PID\}.cfg.json

   Hier, is PID procesidentiteitskaart van de configuratie.

1. Voeg eigenschappen in het JSON-bestand toe in de volgende indeling:

   ```
   {
      "aem.adminuname": "updatedUserjson",
      "valid.characters": "[-a-zA-Z0-9_@$]",
      "dita.serialization": true
   }
   ```

1. Leg de wijzigingen vast en voer de Cloud Manager-pijplijn uit om de bijgewerkte configuratie te implementeren.

## De gebruikersinterface van Experience Manager Guides configureren

De 2025.02.0-release van Adobe Experience Manager Guides biedt een vernieuwde interface en verbeterde functies om u te helpen sneller en efficiënter dan ooit te werken. Dit omvat een geheel nieuwe homepage, een schonere en meer georganiseerde redacteurstoolbar, specifieke kaartconsole, en verbeterde eigenschappen.

Om een vlotte overgang te verzekeren en verstoringen te minimaliseren, verstrekt Experience Manager Guides een configuratieoptie die u toestaat terug naar oude UI (en vice versa) te schakelen zoals nodig.

>[!IMPORTANT]
>
> Deze configuratieoptie om tussen nieuwe en oude UI te schakelen werd gesteund tot de versie van 2025.4.0. Met versie 2025.6.0, wordt dit het plaatsen afgekeurd en kan niet meer worden gebruikt om aan oude UI terug te keren.

Voer de volgende stappen uit om de gebruikersinterface van Experience Manager Guides te configureren:

1. Open Adobe Experience Manager en selecteer vervolgens het programma dat de omgeving bevat die u wilt configureren.
2. Schakelaar aan de **Milieu&#39;s** tabel.
3. Selecteer de omgevingsnaam die u wilt configureren. Dit zou u aan de **pagina van de Informatie van het Milieu** moeten navigeren.
4. Schakelaar aan de **Configuratie** tabel.
5. Selecteer **toevoegen/bijwerken**.
6. Voeg de UI configuratiedetails toe. Zorg ervoor dat u dezelfde naam en configuratie gebruikt als in de volgende schermafbeelding.

   ![](assets/enable-penultimate-ui.png){width="800" align="left"}

   Het plaatsen van de waarde aan **waar** behoudt oude UI, terwijl **vals** nieuwe UI activeert.



**Bovenliggend onderwerp:**&#x200B;[&#x200B; Download en installeer &#x200B;](download-install.md)
