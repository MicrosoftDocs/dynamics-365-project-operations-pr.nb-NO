---
title: Hva er nytt eller endret i Project Service Automation Update Release 29, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 29, V3.
author: ruhercul
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010483"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 29. Denne versjonen har buildnummeret V3.10.47.7, og er generelt tilgjengelig via en egen oppdatering i februar 2021.

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