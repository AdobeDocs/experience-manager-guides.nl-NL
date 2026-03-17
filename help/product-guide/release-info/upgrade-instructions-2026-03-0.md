---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides, release 2026.03.0
description: Leer meer over de compatibiliteitsmatrix en hoe u een upgrade uitvoert naar de release van 2026.03.0 van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: 91befea8c232cd487762ea71f522004e5ca63ee0
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# Upgrade-instructies voor de release van 2026.03.0

Dit artikel behandelt de upgrade-instructies en de compatibiliteitsmatrix voor de release 2026.03.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de versie 2026.03.0 ](whats-new-2026-03-0.md) nieuw is.

Voor de lijst van kwesties die in deze versie worden bevestigd, mening [ Vaste kwesties in de 2026.03.0 versie ](fixed-issues-2026-03-0.md).

## Compatibiliteitsmatrix

In deze sectie wordt de compatibiliteitsmatrix voor de softwaretoepassingen vermeld die worden ondersteund door de release 2026.03.0 van Experience Manager Guides as a Cloud Service.

### FrameMaker en FrameMaker Publishing Server

| Experience Manager Guides als Cloud Release | FMPS | FrameMaker | Zuurstofauteur |
| --- | --- | --- | --- |
| 2026,03,0 | Niet compatibel | 2022 of hoger | 26,1 |


### Zuurstofaansluiting

| Experience Manager Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2026,03,0 | 3,8-uuid 1 | 3,8-uuid 1 | 2,3 | 2,3 |


### Sjabloonversie van AEM-site

| Versie van componenten | Site-versie |
|---|---|
| guides-components.all-1.4.0 | aemg-sites-template-1.3.0 |

### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package voor Cloud Service | guides-components.all-1.4.0 | aem-site-template-dxml-1.0.17 |

## Upgrade naar 2026.03.0-release

Experience Manager Guides wordt automatisch bijgewerkt na de upgrade naar de nieuwste versie van Experience Manager as a Cloud Service.

>[!IMPORTANT]
>
> Deze versie bevat updates voor de instellingen van het mapprofiel (ui_config.json). Als u aangepaste instellingen gebruikt, moet u een back-up van deze instellingen maken voordat u de upgrade uitvoert. Nadat u de update hebt uitgevoerd, kunt u de instellingen controleren en aanpassen en deze aanpassen aan de wijzigingen die u in de nieuwste versie hebt aangebracht.

Controleer en valideer uw opstellingsconfiguraties om te bevestigen zij correct worden uitgevoerd. Als u om het even welke veranderingen van de douaneconfiguratie hebt geïntroduceerd, mening [ Extra configuratie voor de bevordering van Cloud Service ](../cs-install-guide/additional-config-for-cloud-service.md) voor om het even welke extra procedures van toepassing op de versie u van bevordert.

