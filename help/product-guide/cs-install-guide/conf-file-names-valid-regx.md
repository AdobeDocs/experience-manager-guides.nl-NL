---
title: Regx configureren voor geldige bestandsnaamtekens
description: Leer hoe u Regx kunt configureren voor geldige bestandsnaamtekens
exl-id: 05e9ca3c-28ff-4f82-8061-3d20307890ff
feature: Filename Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Regx configureren voor geldige bestandsnaamtekens {#id214BD0550E8}

Vanaf AEM Guides 3.8 kunt u als beheerder een lijst met geldige speciale tekens definiëren die zijn toegestaan in bestandsnamen. In eerdere versies mochten gebruikers bestandsnamen definiëren die speciale tekens bevatten, zoals `@` , `$` , `>` en meer. Deze speciale karakters resulteerden in kwesties terwijl het openen van onderwerpen van het dashboard van de kaart DITA of het klikken op de verbinding van onderwerp in TOC, die vaak in resulteerden dat de pagina niet wegens speciale karakters in URL werd geopend.

Gebruikend de configuratie die u toestaat om een regx voor geldige dossier te bepalen - noem karakters, hebt u volledige controle op hoe de dossiers intern in het systeem worden genoemd. U kunt een lijst met speciale tekens definiëren die zijn toegestaan in de bestandsnamen. Standaard bevat de geldige bestandsnaamconfiguratie &quot;`a-z A-Z 0-9 - _`&quot;. Tijdens het creëren van een nieuw dossier, kunt u om het even welk speciaal karakter in de titel van het dossier hebben, maar intern zal het met &quot;`-`&quot;in de dossiernaam worden vervangen. U kunt bijvoorbeeld de bestandstitel &quot;Introduction 1&quot; of &quot;Introduction@1&quot; hebben. De overeenkomstige bestandsnaam die voor beide gevallen wordt gegenereerd, is &quot;Introduction-1&quot;.

Wanneer u een lijst van geldige karakters bepaalt, herinner dat deze karakters &quot;`*/:[\]|#%{}?&<>"/+`&quot;altijd met &quot;`-`&quot;zullen worden vervangen.

Als u de geldige lijst met speciale tekens niet configureert, kan het maken van bestanden onverwachte resultaten opleveren. Om dergelijke fouten te vermijden, wordt sterk geadviseerd om deze configuratieverandering aan te brengen.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\) gegevens op om regex te configureren voor geldige bestandsnaamtekens:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `valid.characters` | De waarde is een regex-patroon. Het moet drie basistekens hebben en de lijst moet met een koppelteken \ (-\) beginnen.<br> **Standaardwaarde**: \[-a-zA-Z0-9\_\] |

>[!NOTE]
>
> Net als in de lijst met geldige bestandsnaamtekens kunt u ook een lijst met geldige bestandsnaamtekens opgeven voor AEM site-uitvoer. Voor meer details, zie [ geldige dossiernamen voor AEM output van de Plaats ](conf-file-names-valid-regx-aem-site-output.md#) vormen.

**Bovenliggend onderwerp:**[ vorm filenames ](conf-file-names.md)
