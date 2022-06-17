---
title: Hva er nytt eller endret i Project Service Automation Update Release 39, V3
description: Denne artikkelen viser funksjoner og rettelser i Microsoft Dynamics 365 Project Service Automation Update Release 39 V3.
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922464"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikkelen viser funksjoner og rettelser som er nye eller endret i Project Service Automation Update Release 39 V3. Denne versjonen har buildnummer V3.10.60.170 og er vanligvis tilgjengelig via en egen oppdatering i januar 2022.

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
