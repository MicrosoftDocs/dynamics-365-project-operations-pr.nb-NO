---
title: Hva er nytt eller endret i Project Service Automation Update Release 43, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelige i Microsoft Dynamics 365 Project Service Automation-oppdateringsutgivelsen 43, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710034"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 43, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og rettinger som er nye eller endrede for Project Service Automation Update Release 43, V3. Denne versjonen har et build-nummer på V3.10.74.200 og er generelt tilgjengelig via en egen oppdatering i mai 2022.

## <a name="update-release-43"></a>Update Release 43

### <a name="bug-fixes"></a>Feilrettinger

Følgende problemer har blitt løst.


**Tid og utgift**

- Når du importerer tidsoppføringer fra bestillinger eller ressurstilordninger, beholdes ikke referansen til den relaterte ressursen som kan reserveres.
- Når rutenettet for tidsoppføringer er utvidet til fullskjermmodus, fungerer ikke navigering med tabulatortasten i rutenettet.
- Når du sender inn en tidsoppføring som er opprettet av en annen bruker, blir feltet **Sendt av** fylt ut på feil måte med brukeren som opprettet tidsarket.
