---
title: AEM Guides verwijderen
description: Leer hoe u AEM Guides kunt verwijderen
exl-id: 6c6b9692-cdec-426f-bc3b-f09d0091da39
feature: Installation
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# AEM Guides verwijderen {#id21BHG0C0SXA}

U kunt AEM Guides verwijderen met CRX Package Manager. Tijdens het verwijderen wordt de inhoud van de opslagplaats teruggezet naar de momentopname die vlak voor de installatie van het pakket is gemaakt.

Voer de volgende stappen uit om AEM Guides te verwijderen:

1. Meld u aan bij uw AEM en navigeer naar CRX Package Manager. De standaard-URL voor toegang tot pakketbeheer is:

   ```http
   http://<server name>:<port>/crx/packmgr/index.jsp
   ```

1. Zoek naar het pakket com.adobe.fmdita.
1. Klik op het pakket om het uit te vouwen.
1. Klik **Meer** om dropdown te openen.
1. Klik **desinstalleer** en wacht op uninstall om te voltooien.
1. Als u dit pakket niet meer nodig hebt, klik **Schrapping** na het verwijderen van het pakket.

## Na verwijderen

Voer de volgende stappen uit om de resterende bestanden op te schonen nadat u deze hebt verwijderd:

1. Maak de scriptcache leeg met:

   ```http
   http://<host>:<port>/system/console/scriptcache
   ```

1. U kunt de cache ongeldig maken met:

   ```http
   http://<host>:<port>/libs/granite/ui/content/dumplibs.rebuild.html?back=true
   ```

1. Klik **ongeldig het Geheime voorgeheugen**.
1. Maak de cache van de browser leeg.

**Bovenliggend onderwerp:**[ Download en installeer ](download-install.md)
