---
title: Hva er nytt eller endret i Project Service Automation Update Release 41, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelige i Microsoft Dynamics 365 Project Service Automation-oppdateringsutgivelsen 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580928"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og rettinger som er nye eller endrede for Project Service Automation Update Release 41, V3. Denne versjonen har buildnummer V3.10.62.162 og er generelt tilgjengelig via en egen oppdatering fra mars 2022.

## <a name="update-release-41"></a>Update Release 41

### <a name="bug-fixes"></a>Feilrettinger

Følgende problemer har blitt løst.

**Prosjektledelse**
- Når du prøver å opprette et prosjekt fra en mal som er basert på et prosjekt opprettet fra tillegget for stasjonær datamaskin, vises følgende feilmelding: "Feltvalidering av ressurstilordningens planlagte arbeid: Sluttdatoen for hvert tidsutsnitt for ressurstilordninger kan ikke være tidligere enn startdatoen."

**Tid og utgift**
- Når du prøver å slette en tidsoppføring, vises følgende feilmelding: "Det oppstod en uventet feil fra ISV-kode."

**Salg**
- Når du oppretter en faktura for en milepæl med fast pris, blir ikke feltene **Beskrivelse** og **Ekstern beskrivelse** fylt ut. 
