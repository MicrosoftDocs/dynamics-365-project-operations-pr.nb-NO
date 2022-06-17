---
title: Hva er nytt eller endret i Project Service Automation Update Release 40, V3
description: Denne artikkelen viser funksjoner og rettelser i Microsoft Dynamics 365 Project Service Automation Update Release 40 V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912804"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikkelen viser funksjoner og rettelser som er nye eller endret i Project Service Automation Update Release 40 V3. Denne versjonen har buildnummeret V3.10.61.61, og er generelt tilgjengelig via en egen oppdatering i februar 2022.

## <a name="update-release-40"></a>Update Release 40

### <a name="features"></a>Funksjoner
Fase 1 av oppgraderingen fra Project Service Automation til Project Operations – Lite frigis til alle kunder i februar 2022. For å finne ut om du er kvalifisert kan du se [Oppgrader fra Project Service Automation til Project Operations](upgrade-project-operations-non-stocked.md). Hvis appen ikke vises i forekomsten din i Power Platform-administrasjonssenteret, må du kontakte kundestøtte og be om at lanseringen aktiveres for dine miljøer. Forespørselen må inneholde en liste over miljø-ID-er der lanseringen må aktiveres.

### <a name="bug-fixes"></a>Feilrettinger

Følgende problemer har blitt løst.

**Tid og utgift**
- En notatoppføring mangler når en tidsoppføring er avvist eller annullert. 

**Salg**

- Når du oppdaterer kostnads- eller salgsestimater ved hjelp av standard programtillegg, har du fått feilaktig tillatelse til å sende JSON-nyttelaster som ikke er gyldige utenfor brukergrensesnittet.
- Når du oppdaterer tilbudslinjer ved hjelp av hurtigvisningen, kan du aktivere tilbud.
