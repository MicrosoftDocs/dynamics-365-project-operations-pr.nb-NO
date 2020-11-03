---
title: Foreta en ikke-forpliktende bestilling på krav
description: Dette emnet gir informasjon om hvordan du foretar en ikke-forpliktende bestilling på krav.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 861e484ea2fc251e0082b4cb0cd5409a45a74057
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081830"
---
# <a name="soft-book-requirements"></a>Foreta en ikke-forpliktende bestilling på krav

Et ressurskrav kan være forpliktende. En forpliktende bestilling oppretter et forslag som bruker kapasiteten til en ressurs. Forslaget sendes deretter tilbake til anmoderen for godkjenning. En ikke-forpliktende bestilling legger foreløpig til en ressurs i et prosjektteam og har en annen status på planleggingstavlen, men den forbruker ikke kapasiteten til ressursen. Hvis du vil legge inn en ikke-forpliktende bestilling på en ressurs fra planleggingtavlen, setter du feltet **Bestillingsstatus** til **Ikke-forpliktende**.

![Bestillingsstatusen settes til Ikke-forpliktende](media/Resource-Management-image77.png)

Når kategorien **Team** er i visning **Navngitte teammedlemmer** , vises ressursen der. Timene som det er foretatt en ikke-forpliktende bestilling på, rapporteres i kolonnen **Timer med ikke-forpliktende bestillinger**.

![Ikke-forpliktende bestilte timer i visningen Navngitte teammedlemmer](media/Resource-Management-image78.png)

Ikke-forpliktende bestilte teammedlemmer kan tilordnes til oppgaver.

![Ikke-forpliktende bestilt teammedlem som er tilordnet en oppgave](media/Resource-Management-image79.png)

I kategorien **Avstemming** vises ingen bestillinger for en ikke-forpliktende ressurs, fordi kategorien **Avstemming** bare vurderer forpliktende bestillinger.

![Ikke-forpliktende bestilt ressurs uten bestillinger i kategorien Avstemming](media/Resource-Management-image80.png)

> [!NOTE]
> Du kan ikke foreta en ikke-forpliktende bestilling av en ressurs fra et krav som ble generert fra et generelt teammedlem.

I planleggingstavlen brukes en annen farge for ikke-forpliktende bestillinger for en ressurs.

![Ikke-forpliktende bestilling fra planleggingstavlen](media/Resource-Management-image81.png)

Hvis du vil konvertere en ikke-forpliktende bestilling til en forpliktende bestilling, høyreklikker du den ikke-forpliktende bestillingen på planleggingstavlen og velger **Endre status** \> **Forpliktende bestilling** \> **Forpliktende**.

![Endre bestillingsstatusen til forpliktende](media/Resource-Management-image82.png)

Bestillingen endres, og statusen endres på planleggingstavlen. Fordi bestillingsstatusen nå er **Forpliktende** , vises ressursen som bestilt, og kapasiteten og tilgjengeligheten blir justert.

Du kan bruke samme metode til å annullere en forpliktende bestilling eller en ikke-forpliktende bestilling fra planleggingstavlen.

Hvis du vil konvertere en ressurs som er ikke-forpliktende, til forpliktende, går du til kategorien **Team** for prosjektet og velger ressursen, og deretter velger du **Bekreft**.

![Bekreft-kommandoen](media/Resource-Management-image83.png)
