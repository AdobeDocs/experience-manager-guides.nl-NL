---
title: Inhoud vertalen in AEM Guides
description: Leer hoe u inhoud kunt vertalen
exl-id: 0d3a909c-3499-4ef4-b033-02e412dae959
feature: Translation
role: Admin
level: Experienced
source-git-commit: ea3083542e955a56c27cd833600370a7962c6b8d
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---

# Inhoud vertalen {#id181GB0400UI}

Automatiseer de vertaling van pagina-inhoud, elementen en door de gebruiker gegenereerde inhoud om meertalige websites te maken en te onderhouden. Om vertaalworkflows te automatiseren, integreert u de leveranciers van vertaaldiensten met AEM en creeert projecten voor het vertalen van inhoud in veelvoudige talen. AEM ondersteunt workflows voor het vertalen van mensen en machines.

- Menselijke vertaling: de inhoud wordt naar uw vertaalbureau verzonden en door professionele vertalers vertaald. Wanneer de vertaalde inhoud is voltooid, wordt deze geretourneerd en in AEM geïmporteerd. Wanneer uw vertaalprovider is geïntegreerd met AEM, wordt inhoud automatisch uitgewisseld tussen AEM en de vertaalprovider

- Machinevertaling: de vertaalservice zet uw inhoud direct om


Voor het vertalen van inhoud worden de volgende stappen uitgevoerd:

1. Verbind AEM met uw [&#x200B; leverancier van de vertaaldienst &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-tic.html#ConnectingtoaTranslationServiceProvider) en creeer [&#x200B; configuraties van het kader van de vertaalintegratie &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-tic.html#CreatingaTranslationIntegrationConfiguration).

1. Koppel de pagina&#39;s van uw taalmeester met de [&#x200B; vertaaldienst en kaderconfiguraties &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-tic.html#ConfiguringPagesforTranslation).

1. Identificeer het type van [&#x200B; te vertalen inhoud &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-rules.html).

1. [&#x200B; bereidt de inhoud voor vertaling &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-prep.html) voor door de taalmeester te ontwerpen en de wortelpagina&#39;s van taalexemplaren te creëren.

1. Creeer [&#x200B; vertaalprojecten &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-manage.html) om de inhoud te verzamelen om te vertalen en het vertaalproces voor te bereiden.

1. Gebruik de vertaalprojecten om [&#x200B; het proces van de inhoudsomzetting &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-manage.html) te beheren.


Wanneer uw vertaalservicebureau geen aansluiting voor integratie met AEM biedt, ondersteunt AEM het handmatig exporteren en importeren van vertaalde inhoud in XML-indeling.

>[!TIP]
>
> Zie de *sectie van de Vertaling* in de Beste praktijken gids voor beste praktijken rond het vertalen van inhoud.

## Het tabblad Vertaling op het dashboard voor de DITA-kaart configureren

De optie van het Lusje van de Vertaling van de Huid wordt niet toegelaten door gebrek en u moet dit van configMgr toelaten. Voer de volgende stappen uit om het tabblad Vertaling op het dashboard voor de DITA-kaart te verbergen:

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

## Op componenten gebaseerde vertaalworkflow configureren

Als de schakelaar voor de vertaalverkoper geen inhoud DITA steunt, dan moet de op component-gebaseerde vertaalwerkschema worden toegelaten. Als deze optie is ingeschakeld, wordt de vertaalbare inhoud verzonden als metagegevens over elementen. Deze workflow werkt alleen als de connector ondersteuning biedt voor het vertalen van metagegevens van elementen.

Op basis van de vertaalworkflow die in uw installatie wordt gebruikt, moet de optie voor de vertaalworkflow op basis van componenten als volgt worden geconfigureerd:

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
   > Als u vertaalschakelaar gebruikt, dan zorg ervoor dat u de schakelaar zoals die in *[wordt beschreven vormend het Kader van de Integratie van de Vertaling &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/administering/using/tc-tic.html)* onderwerp in AEM documentatie hebt gevormd.

1. Klik **sparen**.

>[!IMPORTANT]
>
> Nadat u de vertaalconfiguraties hebt ingesteld, dient u de juiste Cloud Configuration in te stellen voor de taalmappen.

## De workflow voor veroudering configureren

>[!IMPORTANT]
> 
> Het wordt aanbevolen de nieuwste vertaalworkflow, die beschikbaar is in AEM Guides 4.6.0 en hoger, te gebruiken voor betere prestaties. Nochtans, als u om het even welke aanpassing in het vertaalproces hebt toegelaten en het door het nieuwe werkschema wordt beïnvloed, denk na terugkerend aan de erfenisvertaalwerkstroom als oplossing.



Standaard is de optie voor de verouderde vertaalworkflow uitgeschakeld. U kunt deze optie configureren door de volgende stappen uit te voeren:

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






<!---

This was added for 2406 CS IG

## Configure the legacy translation workflow 

It is recommended that you use the latest translation workflow, which provides enhanced performance. However, you can configure the legacy translation workflow if necessary.

Based on the translation workflow used in your setup, provide the following (property) details to configure the legacy translation workflow: the component-based translation workflow option should be configured as follows:

1.  Open the Adobe Experience Manager Web Console Configuration page.

    The default URL to access the configuration page is:

    ! Add the syntax of http as given in previous config

    Note: Configure htttp code as given in previous sample
    

1.  Search for and click on the **com.adobe.fmdita.config.ConfigManager** bundle.



1.  Configure the **Run legacy translation workflow** option as per your setup:

    -   If you use the latest translation workflow, then *Disable* \( `false`\) the **Run legacy translation workflow** option. The latest translation workflow is enabled by default. <br> 

    -   If you use the legacy translation, then *Enable \( `true`\)* the **Run legacy translation workflow** option.

1.  Click **Save**.


--->


## Nabewerking van tijdelijke taalkopieën configureren

Wanneer u de vertaalworkflow start, maakt het systeem tijdelijke taalkopieën van de broninhoud. U kunt de nabewerking voor deze tijdelijke bestanden in- of uitschakelen. In de naverwerkingstransactie worden de inkomende en uitgaande referenties van de bestanden opgelost, wordt de documentstatus ingesteld, samen met andere bewerkingen. Als u naverwerking voor deze tijdelijke bestanden inschakelt, kan het voltooien van het vertaalproces langer duren. Daarom wordt aangeraden de optie voor nabewerking uit te schakelen.

De optie voor naverwerken van tijdelijke bestanden is standaard uitgeschakeld. U kunt deze optie configureren door de volgende stappen uit te voeren:

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
