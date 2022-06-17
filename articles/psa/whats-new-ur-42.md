---
title: Hva er nytt eller endret i Project Service Automation Update Release 42, V3
description: Denne artikkelen viser funksjoner og rettelser i Microsoft Dynamics 365 Project Service Automation Update Release 42 V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912727"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikkelen viser funksjoner og rettelser som er nye eller endret i Project Service Automation Update Release 42 V3. Denne versjonen har et build-nummer på V3.10.73.61 og er generelt tilgjengelig via en egen oppdatering i april 2022.

## <a name="update-release-42"></a>Update Release 42

### <a name="bug-fixes"></a>Feilrettinger

Følgende problemer har blitt løst.

**Tid og utgift**

- Når en timeliste er avvist, blir brukeren som avviste den, feil identifisert som **System**.
- Når tidsoppføringer importeres, mangler **Ressurskategori**-verdien.
- Prosjektgodkjennere kan godkjenne innsendte prosjekter når tillatelsene ikke er spesifikt angitt til **Kan godkjenne**.

**Salg**

- Når faktiske kostnader loggføres på oppgaver som ikke er på rotnivå, aggregeres de faktiske kostnadene på feil måte.
