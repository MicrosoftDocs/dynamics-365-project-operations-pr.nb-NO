---
title: Hva er nytt eller endret i Project Service Automation Update Release 29, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499683"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 29. Denne versjonen har buildnummeret V3.10.45.98, og er generelt tilgjengelig via en egen oppdatering i februar 2021.

## <a name="update-release-29"></a>Update Release 29

### <a name="bug-fixes"></a>Feilrettinger

**Tid og utgift**

Følgende problemer har blitt løst:

- Brukere kan ikke se arbeidstimer som er logget på dager som ikke er arbeidsdager, i rutenettet for tidsoppføring.
- Godkjente utgiftsoppføringer kan redigeres i rutenettet.

**Prosjektledelse**

Følgende problemer har blitt løst:

- Mangler valideringslogikk for å sikre at arbeidstimer for ressurstilordning ikke kan være negative.
- Den egendefinerte handlingen **AssignResourcesForTask** oppdaterer alle felter i stedet for bare endrede felter.
- Når du kopierer et prosjekt i et miljø med plugin-moduler eller arbeidsflyter som er registrert på **CreateProject**-hendelsen, oppdateres ikke **msdyn_bulkgenerationstatus**-attributtet hvis **CopyWBSToProject** mislykkes.
- Når du utvider prosjektkalenderen, sorteres ikke arbeidsdagene i stigende rekkefølge, noe som fører til at enkelte prosjektoppgaveoppdateringer mislykkes.
- Endring av prosjektlederen i et eksisterende prosjekt utløser logikken for standardisering av organisasjonsenheten.

**Salg**

Følgende problemer har blitt løst:

- Fanen **Kontraktytelse** på **Kontrakt**-siden mislykkes stille under initialiseringen når det ikke finnes kontraktlinjer.
