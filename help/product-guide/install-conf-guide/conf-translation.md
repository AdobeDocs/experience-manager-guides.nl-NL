---
title: Inhoud vertalen
description: Leer hoe u inhoud kunt vertalen
feature: Translation
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '1368'
ht-degree: 0%

---

# Inhoud vertalen {#id181GB0400UI}

Automatiseer de vertaling van pagina-inhoud, elementen en door de gebruiker gegenereerde inhoud om meertalige websites te maken en te onderhouden. Om vertaalworkflows te automatiseren, integreert u de leveranciers van vertaaldiensten met AEM en creeert u projecten voor het vertalen van inhoud in veelvoudige talen. AEM ondersteunt workflows voor het vertalen van mensen en machines.

- Menselijke vertaling: de inhoud wordt naar uw vertaalbureau verzonden en door professionele vertalers vertaald. Wanneer de vertaalde inhoud is voltooid, wordt deze geretourneerd en in AEM geïmporteerd. Wanneer uw vertaalprovider is geïntegreerd met AEM, wordt inhoud automatisch uitgewisseld tussen AEM en de vertaalprovider

- Machinevertaling: de vertaalservice zet uw inhoud direct om


Op de volgende tabbladen vindt u instructies voor het vertalen van inhoud op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Verbind AEM met uw [&#x200B; leverancier van de vertaaldienst &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/integration-framework.html?lang=nl-NL) en creeer configuraties van het kader van de vertaalintegratie.

1. Koppel de pagina&#39;s van uw taalmaster aan de vertaalservice en frameworkconfiguraties.

1. Identificeer het type van [&#x200B; te vertalen inhoud &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/rules.html?lang=nl-NL).

1. [&#x200B; bereidt de inhoud voor vertaling &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/preparation.html?lang=nl-NL) voor door de taalmeester te ontwerpen en de wortelpagina&#39;s van taalexemplaren te creëren.

1. Creeer [&#x200B; vertaalprojecten &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/managing-projects.html?lang=nl-NL) om de inhoud te verzamelen om te vertalen en het vertaalproces voor te bereiden.

1. Gebruik de vertaalprojecten om [&#x200B; het proces van de inhoudsomzetting &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/managing-projects.html?lang=nl-NL) te beheren.


>[!TAB  Op locatie ]

1. Verbind AEM met uw [&#x200B; leverancier van de vertaaldienst &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-tic.html#ConnectingtoaTranslationServiceProvider) en creeer [&#x200B; configuraties van het kader van de vertaalintegratie &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-tic.html#CreatingaTranslationIntegrationConfiguration).

1. Koppel de pagina&#39;s van uw taalmeester met de [&#x200B; vertaaldienst en kaderconfiguraties &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-tic.html#ConfiguringPagesforTranslation).

1. Identificeer het type van [&#x200B; te vertalen inhoud &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-rules.html).

1. [&#x200B; bereidt de inhoud voor vertaling &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-prep.html) voor door de taalmeester te ontwerpen en de wortelpagina&#39;s van taalexemplaren te creëren.

1. Creeer [&#x200B; vertaalprojecten &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-manage.html) om de inhoud te verzamelen om te vertalen en het vertaalproces voor te bereiden.

1. Gebruik de vertaalprojecten om [&#x200B; het proces van de inhoudsomzetting &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-manage.html) te beheren.

>[!ENDTABS]

Als uw vertaalservicebureau geen aansluiting voor integratie met AEM biedt, biedt AEM ondersteuning voor het handmatig exporteren en importeren van vertaalde inhoud in XML-indeling.

>[!TIP]
>
> Zie de *Vertaling* sectie in de Beste praktijken gids voor beste praktijken rond het vertalen van inhoud.

## Het tabblad Vertaling op het dashboard voor de DITA-kaart configureren

Op de volgende tabbladen vindt u instructies voor het verbergen van het tabblad Vertaling op het dashboard voor de DITA-kaart op basis van uw Experience Manager Guides-instellingen: Cloud Service of Op locatie.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen.
1. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om het tabblad Vertaling op het kaartdashboard te configureren:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|------------|--------------|
   | `com.adobe.fmdita.config.ConfigManager` | `tabs.translation` | Boolean \( true/ false\).<br> **Standaardwaarde**: `true` |

   >[!NOTE]
   >
   > Deze configuratie is standaard ingeschakeld en het tabblad Vertalen is niet beschikbaar op het kaartdashboard.


>[!TAB  Op locatie ]

De optie van het Lusje van de Vertaling van de Huid wordt niet toegelaten door gebrek en u moet dit van configMgr toelaten.


1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Selecteer de **optie van het Lusje van de Vertaling van de Huid**, om het vertaallusje op het kaartdashboard te verbergen.

   >[!NOTE]
   >
   > Deze eigenschap is standaard uitgeschakeld en het tabblad Vertalen is beschikbaar op het kaartdashboard.

1. Klik **sparen**.

>[!ENDTABS]


## Op componenten gebaseerde vertaalworkflow configureren

Als de schakelaar voor de vertaalverkoper geen inhoud DITA steunt, dan moet de op component-gebaseerde vertaalwerkschema worden toegelaten. Als deze optie is ingeschakeld, wordt de vertaalbare inhoud verzonden als metagegevens over elementen. Deze workflow werkt alleen als de connector ondersteuning biedt voor het vertalen van metagegevens van elementen.

Op de volgende tabbladen vindt u instructies voor de vertaalworkflow op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Op basis van de vertaalworkflow die in uw installatie wordt gebruikt, moet de optie voor de vertaalworkflow op basis van componenten worden geconfigureerd. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om de workflow voor op componenten gebaseerde omzetting te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `component.translation` | Boolean: <br> -   Als u menselijke vertaling gebruikt, dan *maak* \ ( `false` onbruikbaar \) de **op component-Gebaseerde optie van het Vertaalwerkschema**. <br> -   Als u machinevertaling gebruikt, dan *laat \ ( `true` \)* toe de **op component-Gebaseerde optie van het Vertaalwerkschema**. |

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Vorm de **Component-Gebaseerde optie van het Werkschema van de Vertaling DITA** zoals per uw opstelling:

   - Als u menselijke vertaling gebruikt, dan *maak* **op component-Gebaseerde optie van het Vertaalwerkschema** onbruikbaar.

   - Als u machinevertaling gebruikt, dan *laat* toe de **op component-Gebaseerde optie van het Vertaalwerkschema**.

   >[!NOTE]
   >
   > Als u vertaalschakelaar gebruikt, dan zorg ervoor dat u de schakelaar zoals die in *[wordt beschreven het Vormen van het Kader van de Integratie van de Vertaling &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-tic.html)* onderwerp in de documentatie van AEM hebt gevormd.

1. Klik **sparen**.

>[!IMPORTANT]
>
> Nadat u de vertaalconfiguraties hebt ingesteld, dient u de juiste Cloud Configuration in te stellen voor de taalmappen.

>[!ENDTABS]


## De workflow voor veroudering configureren

Op de volgende tabbladen vindt u instructies voor het configureren van deze optie op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

>[!IMPORTANT]
>
> Het wordt aanbevolen de nieuwste vertaalworkflow, die beschikbaar is in AEM Guides 2024.06.0 en hoger, te gebruiken voor betere prestaties. Nochtans, als u om het even welke aanpassing in het vertaalproces hebt toegelaten en het door het nieuwe werkschema wordt beïnvloed, denk na terugkerend aan de erfenisvertaalwerkstroom als oplossing.

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende gegevens (eigenschap) op om de workflow voor veroudering te configureren:


| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `translation.workflow.version.legacy` | Van Boole: <br> - als u het recentste vertaalwerkschema gebruikt, dan *maak* \ ( `false` onbruikbaar \) **de oudere vertaalwerkstroom van de Looppas** optie.  <br> -   Als u de erfenisvertaling gebruikt, dan *laat \ ( `true` \)* toe de **optie van het de erfenisvertaalwerkschema van de Looppas**. <br> **Standaardwaarde**: vals |


>[!NOTE]
>
> Als u vertaalschakelaar gebruikt, dan zorg ervoor dat u de schakelaar zoals die in *[wordt beschreven het Vormen van het Kader van de Integratie van de Vertaling &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/integration-framework.html?lang=nl-NL)* onderwerp in de documentatie van Adobe Experience Manager hebt gevormd.

>[!IMPORTANT]
>
> Nadat u de vertaalconfiguraties hebt ingesteld, dient u de juiste Cloud Configuration in te stellen voor de taalmappen.

>[!TAB  Op locatie ]

>[!IMPORTANT]
> 
> Het wordt aanbevolen de nieuwste vertaalworkflow, die beschikbaar is in AEM Guides 4.6.0 en hoger, te gebruiken voor betere prestaties. Nochtans, als u om het even welke aanpassing in het vertaalproces hebt toegelaten en het door het nieuwe werkschema wordt beïnvloed, denk na terugkerend aan de erfenisvertaalwerkstroom als oplossing. Standaard is de optie voor de verouderde vertaalworkflow uitgeschakeld.

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Configureer de workflowoptie voor veroudering van verouderde vertalingen volgens uw instellingen:

   - (*Gebrek*) als u het recentste vertaalwerkschema wilt gebruiken, dan maak de **optie van het de vertaalwerkschema van de Looppas erfenis** onbruikbaar.
   - Als u het erfenisvertaalwerkschema wilt gebruiken, dan laat de **optie van het de erfenisvertaalwerkschema van de Looppas** toe.

1. Klik **sparen**.

>[!ENDTABS]

## Nabewerking van tijdelijke taalkopieën configureren

Wanneer u de vertaalworkflow start, maakt het systeem tijdelijke taalkopieën van de broninhoud. U kunt de nabewerking voor deze tijdelijke bestanden in- of uitschakelen. In de naverwerkingstransactie worden de inkomende en uitgaande referenties van de bestanden opgelost, wordt de documentstatus ingesteld, samen met andere bewerkingen. Als u naverwerking voor deze tijdelijke bestanden inschakelt, kan het voltooien van het vertaalproces langer duren. Daarom wordt aangeraden de optie voor nabewerking uit te schakelen.

Op de volgende tabbladen vindt u instructies voor het configureren van deze optie op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om de naverwerking van tijdelijke taalkopieën te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `postprocess.temporary.langcopies` | Boolean: <br> -   Als u niet de post-verwerkingsverrichting op de tijdelijke dossiers wilt in werking stellen, dan *maak* \ ( vals \) onbruikbaar de **de taalexemplaren van het na-proces** optie.<br> -   Als u de post-verwerkingsverrichting op de tijdelijke dossiers wilt in werking stellen, dan *laat* \ ( waar \) toe **de taalexemplaren van het na-proces** optie.<br> **Standaardwaarde**: vals |

>[!TAB  Op locatie ]

>[!NOTE]
>
> De optie voor naverwerken van tijdelijke bestanden is standaard uitgeschakeld.

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Vorm de **post-procestaal taalexemplaren** optie zoals per uw opstelling:

   - \ (*Gebrek* \) als u niet de post-verwerkingsverrichting op de tijdelijke dossiers wilt in werking stellen, dan **&#x200B; onbruikbaar maken &#x200B;** na-procestaalexemplaren** optie.

   - Als u de post-verwerkingsverrichting op de tijdelijke dossiers wilt in werking stellen, dan *laat* de **na-procestaalexemplaren** optie toe.

1. Klik **sparen**.

>[!ENDTABS]