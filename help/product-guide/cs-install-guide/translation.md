---
title: Inhoud vertalen
description: Leer hoe u inhoud kunt vertalen
exl-id: 5af78233-343e-47ba-b60c-b7f4789e2406
feature: Translation
role: Admin
level: Experienced
source-git-commit: bcb61127f5f69ac39860a90eac2e1a56ecd1de31
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Inhoud vertalen {#id181GB0400UI}

Automatiseer de vertaling van pagina-inhoud, elementen en door de gebruiker gegenereerde inhoud om meertalige websites te maken en te onderhouden. Om vertaalworkflows te automatiseren, integreert u de leveranciers van vertaaldiensten met AEM en creeert projecten voor het vertalen van inhoud in veelvoudige talen. AEM ondersteunt workflows voor het vertalen van mensen en machines.

- Menselijke vertaling: de inhoud wordt naar uw vertaalbureau verzonden en door professionele vertalers vertaald. Wanneer de vertaalde inhoud is voltooid, wordt deze geretourneerd en in AEM geïmporteerd. Wanneer uw vertaalprovider is geïntegreerd met AEM, wordt inhoud automatisch uitgewisseld tussen AEM en de vertaalprovider

- Machinevertaling: de vertaalservice zet uw inhoud direct om


Voor het vertalen van inhoud worden de volgende stappen uitgevoerd:

1. Verbind AEM met uw [ leverancier van de vertaaldienst ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/integration-framework.html?lang=en) en creeer configuraties van het kader van de vertaalintegratie.

1. Koppel de pagina&#39;s van uw taalmaster aan de vertaalservice en frameworkconfiguraties.

1. Identificeer het type van [ te vertalen inhoud ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/rules.html?lang=en).

1. [ bereidt de inhoud voor vertaling ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/preparation.html?lang=en) voor door de taalmeester te ontwerpen en de wortelpagina&#39;s van taalexemplaren te creëren.

1. Creeer [ vertaalprojecten ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/managing-projects.html?lang=en) om de inhoud te verzamelen om te vertalen en het vertaalproces voor te bereiden.

1. Gebruik de vertaalprojecten om [ het proces van de inhoudsomzetting ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/managing-projects.html?lang=en) te beheren.


Wanneer uw vertaalservicebureau geen aansluiting voor integratie met AEM biedt, ondersteunt AEM het handmatig exporteren en importeren van vertaalde inhoud in XML-indeling.

>[!TIP]
>
> Zie de *Vertaling* sectie in de Beste praktijken gids voor beste praktijken rond het vertalen van inhoud.

## Het tabblad Vertaling op het dashboard voor de DITA-kaart configureren

Voer de volgende stappen uit om het tabblad Vertaling op het dashboard voor de DITA-kaart te verbergen:

1. Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen.
1. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om het tabblad Vertaling op het kaartdashboard te configureren:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|------------|--------------|
   | `com.adobe.fmdita.config.ConfigManager` | `tabs.translation` | Boolean \( true/ false\).<br> **Standaardwaarde**: `true` |

   >[!NOTE]
   >
   > Deze configuratie is standaard ingeschakeld en het tabblad Vertalen is niet beschikbaar op het kaartdashboard.


## Op componenten gebaseerde vertaalworkflow configureren

Als de schakelaar voor de vertaalverkoper geen inhoud DITA steunt, dan moet de op component-gebaseerde vertaalwerkschema worden toegelaten. Als deze optie is ingeschakeld, wordt de vertaalbare inhoud verzonden als metagegevens over elementen. Deze workflow werkt alleen als de connector ondersteuning biedt voor het vertalen van metagegevens van elementen.

Op basis van de vertaalworkflow die in uw installatie wordt gebruikt, moet de optie voor de vertaalworkflow op basis van componenten worden geconfigureerd. Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om de workflow voor op componenten gebaseerde omzetting te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `component.translation` | Boolean: <br> -   Als u menselijke vertaling gebruikt, dan *maak* \ ( `false` onbruikbaar \) de **op component-Gebaseerde optie van het Vertaalwerkschema**. <br> -   Als u machinevertaling gebruikt, dan *laat \ ( `true` \)* toe de **op component-Gebaseerde optie van het Vertaalwerkschema**. |



## De workflow voor veroudering configureren

U wordt aangeraden de nieuwste workflow voor vertaling te gebruiken, die betere prestaties biedt. Als u echter de verouderde vertaalworkflow wilt gebruiken, kunt u deze configureren.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende gegevens (eigenschap) op om de workflow voor veroudering te configureren:




| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `translation.workflow.version.legacy` | Van Boole: <br> - als u het recentste vertaalwerkschema gebruikt, dan *maak* \ ( `false` onbruikbaar \) **de oudere vertaalwerkstroom van de Looppas** optie. De meest recente vertaalworkflow is standaard ingeschakeld. <br> -   Als u de erfenisvertaling gebruikt, dan *laat \ ( `true` \)* toe de **optie van het de erfenisvertaalwerkschema van de Looppas**. |



>[!NOTE]
>
> Als u vertaalschakelaar gebruikt, dan zorg ervoor dat u de schakelaar zoals die in *[wordt beschreven het Vormen van het Kader van de Integratie van de Vertaling ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/integration-framework.html?lang=en)* onderwerp in de documentatie van Adobe Experience Manager hebt gevormd.

>[!IMPORTANT]
>
> Nadat u de vertaalconfiguraties hebt ingesteld, dient u de juiste Cloud Configuration in te stellen voor de taalmappen.

## Nabewerking van tijdelijke taalkopieën configureren

Wanneer u de vertaalworkflow start, maakt het systeem tijdelijke taalkopieën van de broninhoud. U kunt de nabewerking voor deze tijdelijke bestanden in- of uitschakelen. In de naverwerkingstransactie worden de inkomende en uitgaande referenties van de bestanden opgelost, wordt de documentstatus ingesteld, samen met andere bewerkingen. Als u naverwerking voor deze tijdelijke bestanden inschakelt, kan het voltooien van het vertaalproces langer duren. Daarom wordt aangeraden de optie voor nabewerking uit te schakelen.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om de naverwerking van tijdelijke taalkopieën te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `postprocess.temporary.langcopies` | Boolean: <br> -   Als u niet de post-verwerkingsverrichting op de tijdelijke dossiers wilt in werking stellen, dan *maak* \ ( vals \) onbruikbaar de **Post-procestaalexemplaren** optie.<br> -   Als u de post-verwerkingsverrichting op de tijdelijke dossiers wilt in werking stellen, dan *laat* \ ( waar \) toe de **Post-procestaalexemplaren** optie.<br> **Standaardwaarde**: vals |

