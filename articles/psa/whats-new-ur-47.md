---
title: Hva er nytt eller endret i Project Service Automation Update Release 47, V3
description: Denne artikkelen viser funksjoner og rettelser i Microsoft Dynamics 365 Project Service Automation Update Release 47 V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477239"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 47, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikkelen viser funksjoner og rettelser som er nye eller endret i Project Service Automation Update Release 45 V3. Denne versjonen har et build-nummer på V3.10.78.8 og er allment tilgjengelig via en egenoppdatering i juli 2022.

## <a name="update-release-47"></a>Update Release 47

### <a name="bug-fixes"></a>Feilrettinger

Følgende problemer har blitt løst.

**Ressursbehandling**
- En validering ble oppdatert for å sikre at brukere ikke kan utløse et nullreferanseunntak under forsøk på å opprette et prosjektteammedlem uten en **ressurs som kan reserveres**.
