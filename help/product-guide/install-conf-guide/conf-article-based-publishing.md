---
title: Pakketten installeren voor publiceren op basis van artikel
description: Leer hoe u pakketten installeert voor publicaties op basis van artikelen
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Pakketten installeren voor publiceren op basis van artikel {#id21BNL02052Z}

AEM Guides biedt een krachtige publicatiefunctie die is gebaseerd op artikelen en die is geïntegreerd met de webeditor. Gebruikend deze eigenschap, kunt u één of meerdere onderwerpen gelijktijdig publiceren. Nadat u een kaart hebt geopend in de Kaarteditor, kunt u naar het tabblad Uitvoer navigeren om een voorinstelling te maken en vervolgens een of meer onderwerpen kiezen om de uitvoer te genereren. U kunt de op artikel-gebaseerde het publiceren eigenschap gebruiken om output van één of meerdere onderwerpen stapsgewijs te produceren of uw inhoud aan een kennisbasisplatform op een artikel-door-artikel wijze te publiceren. Voor meer details zie, *Op artikel-gebaseerde het publiceren van de sectie van de Redacteur van het Web* in de gids van de Gebruiker.

Op de volgende tabbladen vindt u instructies voor het maken van een AEM-site voor het publiceren van op artikelen gebaseerde uitvoer op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Download **het Pakket van de Inhoud van de Componenten van XML Documentation voor Cloud Service** van uw [ Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/general.html).
1. Open AEM Package Manager. De standaard-URL voor toegang tot pakketbeheer is: `https://<hostname>/crx/packmgr/index.jsp`
1. Upload XML Documentation Components Content Package voor Cloud Service en installeer deze.
1. Download het `Knowledge-base-template-for-article-based-publishing-for-cloud-service.zip` dossier van uw [ Portaal van de Distributie van de Software van Adobe ](https://experience.adobe.com/#/downloads/content/software-distribution/en/general.html).
1. Van de Globale Navigatie, uitgezochte **Plaatsen**.
1. Binnen Plaatsen UI, creeer **** knoop op de top-juiste hoek.
1. Selecteer **Plaats van malplaatje** van **creeer** dropdown.
1. Klik de **knoop van de Invoer** en selecteer dan `Knowledge-base-template-for-article-based-publishing-for-cloud-service.zip` die op uw systeem wordt gedownload. Als de sitesjabloon eenmaal is geïmporteerd, wordt deze onderaan weergegeven.

   >[!NOTE]
   >
   > U hoeft het ZIP-bestand alleen voor de eerste keer te importeren. Nadat de sitesjabloon is geïmporteerd, is deze beschikbaar in de lijst.

   Selecteer **het malplaatje van de Kennisbank voor op artikel-gebaseerde het publiceren** om de plaats van AEM tot stand te brengen en **daarna** op de hoogste juiste hoek te klikken.

1. Ga de **titel van de Plaats** en de **naam van de Plaats** in en klik **creeer** op de hoogste juiste hoek. Er wordt een AEM-site gemaakt met de Tragopan-sitesjabloon. \(Tragopan-site is een voorbeeld van een AEM-site met sjablonen voor een categorie, sectie en artikelpagina.\)

   >[!NOTE]
   >
   > U kunt meerdere AEM-sites maken met dezelfde sjabloon.


U kunt de AEM-site gebruiken om uw artikel te publiceren met behulp van de uitvoervoorinstellingen in de webeditor.

>[!TAB  Op locatie ]

Als u op artikelen gebaseerde publicaties wilt inschakelen, downloadt en installeert u de volgende pakketten van uw Adobe Software Distribution Portal. Installeer deze om een Tragopan-site te maken. \(Tragopan-site is een voorbeeld van een AEM-site met sjablonen voor een categorie, sectie en artikelpagina.\) Werk de Tragopan-site bij om de uitvoer van de AEM-site te genereren met behulp van de uitvoervoorinstellingen van de webeditor.

- Kennisbasissjabloon voor op artikelen gebaseerde publicaties
- Componentpakket voor op artikel gebaseerde publicaties

>[!ENDTABS]


**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](customize-overview.md) aan
