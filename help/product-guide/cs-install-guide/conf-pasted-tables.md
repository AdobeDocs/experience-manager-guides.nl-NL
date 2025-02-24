---
title: Webeditor aanpassen
description: Leer hoe u de weergave van geplakte tabellen in de Editor kunt aanpassen
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: d03ac6ba3ec8e5c52c31a3239e2043bbae79622e
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Weergave van geplakte tabellen configureren

Gebruikend de secundaire toolbar in de Redacteur, kunt u een eenvoudige lijst bij de huidige of volgende geldige plaats van een onderwerp opnemen. U kunt een lijst van Microsoft Word of Excel ook kopiëren en het kleven direct in een onderwerpdossier.

Beheerders kunnen configureren hoe gekopieerde tabellen worden weergegeven. Dergelijke gekopieerde tabellen worden standaard weergegeven als `simpletable` in de editor. U kunt deze instelling echter wijzigen om gekopieerde tabellen als `tgroup` weer te geven door de instelling Configuratie XML Editor bij te werken.

>[!NOTE]
>
> Als u een tabel met samengevoegde rijen of kolommen kopieert, wordt de tabel als een normale tabel `trgoup` geplakt en niet `simpletable` ongeacht de tabelinstelling die in de configuratie van de XML-editor is geconfigureerd.

Voer de volgende stappen uit om de standaardtabelindeling bij te werken:

1. Open de pagina van de Navigaties van Adobe Experience Manager en selecteer **Hulpmiddelen** op de linkerzijde.
2. In het paneel van Hulpmiddelen, uitgezochte **Gidsen** van de lijst van hulpmiddelen.
3. Selecteer **Profielen van de Omslag**, en selecteer dan het profiel waar u lijst het plaatsen wilt bijwerken.
4. Navigeer aan de **Configuratie van de Redacteur van XML** tabel.
5. Selecteer **uitgeven** pictogram op de bovenkant.
6. Selecteer het **pictogram van de Download** om het `ui_config.json` dossier op uw lokaal systeem te downloaden.
7. Werk in het `ui_config.json` -bestand de instelling `simpletable` bij zoals hieronder wordt weergegeven:

   ```
   "htmlToDitaMapping":{ "table": {
   "name" : "tgroup",
   "wrapTag" : {
       "dita" : "table",
       "html" : "div"
   }
   } },
   ```


Sla het bestand op en upload het wanneer het is bijgewerkt.

