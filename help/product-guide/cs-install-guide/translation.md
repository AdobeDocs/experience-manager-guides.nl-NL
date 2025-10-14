---
title: Inhoud vertalen
description: Leer hoe u inhoud kunt vertalen
exl-id: 5af78233-343e-47ba-b60c-b7f4789e2406
feature: Translation
role: Admin
level: Experienced
source-git-commit: ea3083542e955a56c27cd833600370a7962c6b8d
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 0%

---

# Inhoud vertalen {#id181GB0400UI}

Automatiseer de vertaling van pagina-inhoud, elementen en door de gebruiker gegenereerde inhoud om meertalige websites te maken en te onderhouden. Om vertaalworkflows te automatiseren, integreert u de leveranciers van vertaaldiensten met AEM en creeert projecten voor het vertalen van inhoud in veelvoudige talen. AEM ondersteunt workflows voor het vertalen van mensen en machines.

- Menselijke vertaling: de inhoud wordt naar uw vertaalbureau verzonden en door professionele vertalers vertaald. Wanneer de vertaalde inhoud is voltooid, wordt deze geretourneerd en in AEM geïmporteerd. Wanneer uw vertaalprovider is geïntegreerd met AEM, wordt inhoud automatisch uitgewisseld tussen AEM en de vertaalprovider

- Machinevertaling: de vertaalservice zet uw inhoud direct om


Voor het vertalen van inhoud worden de volgende stappen uitgevoerd:

1. Verbind AEM met uw [&#x200B; leverancier van de vertaaldienst &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/integration-framework.html?lang=nl-NL) en creeer configuraties van het kader van de vertaalintegratie.

1. Koppel de pagina&#39;s van uw taalmaster aan de vertaalservice en frameworkconfiguraties.

1. Identificeer het type van [&#x200B; te vertalen inhoud &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/rules.html?lang=nl-NL).

1. [&#x200B; bereidt de inhoud voor vertaling &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/preparation.html?lang=nl-NL) voor door de taalmeester te ontwerpen en de wortelpagina&#39;s van taalexemplaren te creëren.

1. Creeer [&#x200B; vertaalprojecten &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/managing-projects.html?lang=nl-NL) om de inhoud te verzamelen om te vertalen en het vertaalproces voor te bereiden.

1. Gebruik de vertaalprojecten om [&#x200B; het proces van de inhoudsomzetting &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/managing-projects.html?lang=nl-NL) te beheren.


Wanneer uw vertaalservicebureau geen aansluiting voor integratie met AEM biedt, ondersteunt AEM het handmatig exporteren en importeren van vertaalde inhoud in XML-indeling.

>[!TIP]
>
> Zie de *Vertaling* sectie in de Beste praktijken gids voor beste praktijken rond het vertalen van inhoud.

## Het tabblad Vertaling op het dashboard voor de DITA-kaart configureren

Voer de volgende stappen uit om het tabblad Vertaling op het dashboard voor de DITA-kaart te verbergen:

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen.
1. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om het tabblad Vertaling op het kaartdashboard te configureren:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|------------|--------------|
   | `com.adobe.fmdita.config.ConfigManager` | `tabs.translation` | Boolean \( true/ false\).<br> **Standaardwaarde**: `true` |

   >[!NOTE]
   >
   > Deze configuratie is standaard ingeschakeld en het tabblad Vertalen is niet beschikbaar op het kaartdashboard.


## Op componenten gebaseerde vertaalworkflow configureren

Als de schakelaar voor de vertaalverkoper geen inhoud DITA steunt, dan moet de op component-gebaseerde vertaalwerkschema worden toegelaten. Als deze optie is ingeschakeld, wordt de vertaalbare inhoud verzonden als metagegevens over elementen. Deze workflow werkt alleen als de connector ondersteuning biedt voor het vertalen van metagegevens van elementen.

Op basis van de vertaalworkflow die in uw installatie wordt gebruikt, moet de optie voor de vertaalworkflow op basis van componenten worden geconfigureerd. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om de workflow voor op componenten gebaseerde omzetting te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `component.translation` | Boolean: <br> -   Als u menselijke vertaling gebruikt, dan *maak* \ ( `false` onbruikbaar \) de **op component-Gebaseerde optie van het Vertaalwerkschema**. <br> -   Als u machinevertaling gebruikt, dan *laat \ ( `true` \)* toe de **op component-Gebaseerde optie van het Vertaalwerkschema**. |



## De workflow voor veroudering configureren

>[!IMPORTANT]
>
> Het wordt aanbevolen de nieuwste vertaalworkflow, die beschikbaar is in AEM Guides 2024.06.0 en hoger, te gebruiken voor betere prestaties. Nochtans, als u om het even welke aanpassing in het vertaalproces hebt toegelaten en het door het nieuwe werkschema wordt beïnvloed, denk na terugkerend aan de erfenisvertaalwerkstroom als oplossing.

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende gegevens (eigenschap) op om de workflow voor veroudering te configureren:


| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `translation.workflow.version.legacy` | Van Boole: <br> - als u het recentste vertaalwerkschema gebruikt, dan *maak* \ ( `false` onbruikbaar \) **de oudere vertaalwerkstroom van de Looppas** optie.  <br> -   Als u de erfenisvertaling gebruikt, dan *laat \ ( `true` \)* toe de **optie van het de erfenisvertaalwerkschema van de Looppas**. <br> **Standaardwaarde**: vals |




>[!NOTE]
>
> Als u vertaalschakelaar gebruikt, dan zorg ervoor dat u de schakelaar zoals die in *[wordt beschreven het Vormen van het Kader van de Integratie van de Vertaling &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/integration-framework.html?lang=nl-NL)* onderwerp in de documentatie van Adobe Experience Manager hebt gevormd.

>[!IMPORTANT]
>
> Nadat u de vertaalconfiguraties hebt ingesteld, dient u de juiste Cloud Configuration in te stellen voor de taalmappen.

## Nabewerking van tijdelijke taalkopieën configureren

Wanneer u de vertaalworkflow start, maakt het systeem tijdelijke taalkopieën van de broninhoud. U kunt de nabewerking voor deze tijdelijke bestanden in- of uitschakelen. In de naverwerkingstransactie worden de inkomende en uitgaande referenties van de bestanden opgelost, wordt de documentstatus ingesteld, samen met andere bewerkingen. Als u naverwerking voor deze tijdelijke bestanden inschakelt, kan het voltooien van het vertaalproces langer duren. Daarom wordt aangeraden de optie voor nabewerking uit te schakelen.

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om de naverwerking van tijdelijke taalkopieën te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `postprocess.temporary.langcopies` | Boolean: <br> -   Als u niet de post-verwerkingsverrichting op de tijdelijke dossiers wilt in werking stellen, dan *maak* \ ( vals \) onbruikbaar de **de taalexemplaren van het na-proces** optie.<br> -   Als u de post-verwerkingsverrichting op de tijdelijke dossiers wilt in werking stellen, dan *laat* \ ( waar \) toe **de taalexemplaren van het na-proces** optie.<br> **Standaardwaarde**: vals |

