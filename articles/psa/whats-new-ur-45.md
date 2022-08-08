---
title: Hva er nytt eller endret i Project Service Automation Update Release 45, V3
description: Denne artikkelen viser funksjoner og rettelser i Microsoft Dynamics 365 Project Service Automation Update Release 45 V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169162"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikkelen viser funksjoner og rettelser som er nye eller endret i Project Service Automation Update Release 45 V3. Denne versjonen har et build-nummer på V3.10.76.168 og er allment tilgjengelig via en egenoppdatering i juli 2022.

## <a name="update-release-45"></a>Update Release 45

### <a name="bug-fixes"></a>Feilrettinger

Følgende problemer har blitt løst.

**Salg**

- Brukere kan ikke opprette fakturaer etter at de har prøvd å opprette en faktura uten ufakturert salg hvis de også viser samme forekomst av siden og ikke oppdaterer den.

**Tid og utgift**

- Når Moderne godkjenninger er aktivert og en tilbakekalt prosjektgodkjenning er godkjent, blir oppføringstrinnet feil oppdatert til **Tilbakekallingsforespørsel godkjent**.
- Når Moderne godkjenninger er aktivert og Skyflyter er inaktive, er ikke godkjenningsprosessen vellykket, og sending eller godkjenning av brukere blir ikke varslet.
