---
title: Opmerkingen bij de release | Problemen met Adobe Experience Manager Guides 5.1.0 Service Pack 1-release opgelost.
description: Meer informatie over de opgeloste problemen vindt u in de 5.1.0 Service Pack 1-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: 575488e1b378c17419add75876a8e7f7423d5116
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Oplossingen voor problemen in de 5.1.0 Service Pack 1-release (oktober 2025)


Dit artikel behandelt de fouten die in diverse gebieden van 5.1.0 Service Pack 1 versie van Adobe Experience Manager Guides worden opgelost.

Leer over [&#x200B; verbeteringsinstructies voor 5.1.0 Service Pack 1 versie &#x200B;](upgrade-instructions-5-1-0-sp1.md).


## Platform

- Als u van niet-UUID naar UUID migreert en een upgrade uitvoert naar de nieuwste versie (5.0+), als u doorverwezen afbeeldingen naar andere mappen verplaatst en vervolgens de DITA-bestanden (waar naar deze afbeeldingen wordt verwezen) terugkeert naar vorige versies, resulteert dit in verbroken verwijzingen naar afbeeldingen. (HIDEN-34315)

## Publiceren

- Wanneer u een DITA-kaart publiceert met een basislijn op AEM Sites (met toewijzing van verouderde componenten), worden ook de structuurelementen met het kenmerk `processing-role = resource-only` gepubliceerd. (GUIDEN-34298)
