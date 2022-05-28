---
title: Hva er nytt eller endret i Project Service Automation Update Release 39, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelige i Microsoft Dynamics 365 Project Service Automation-oppdateringsutgivelsen 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: 1d198f9ad9144f5cc2f533fa9603e1f1a181c8b6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588748"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og rettinger som er nye eller endrede for Project Service Automation Update Release 39, V3. Denne versjonen har buildnummer V3.10.60.170 og er vanligvis tilgjengelig via en egen oppdatering i januar 2022.

## <a name="update-release-39"></a>Update Release 39

### <a name="bug-fixes"></a>Feilrettinger

Følgende problemer har blitt løst.

**Generelt**

- Det er gjort flere forbedringer i områdekartet for arabisk oversettelse.

**Prosjektledelse**

- Det oppstår en feil når du endrer prosjektlederen i et prosjekt til en bruker som allerede er teammedlem på prosjektet.

**Salg**

- Eieren av **Prisliste for prosjektkontrakter** er feil når prislisten opprettes automatisk. 
- Datogyldigheten for en prisliste overholdes ikke når prislisten brukes på prosjektparameteren.
- Det kan hende at kontraktsenheten ikke har riktig standardverdi når du redigerer to separate tilbud.
