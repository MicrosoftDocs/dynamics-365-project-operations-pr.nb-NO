---
title: Hva er nytt eller endret i Project Service Automation Update Release 20, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 20, V3
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081569"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation, Update Release 20, V3

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 20. Denne versjonen har et build-nummer på V 3.10.31.37 og er generelt tilgjengelig via en egen oppdatering i juni 2020.

## <a name="update-release-20"></a>Update Release 20

### <a name="bug-fixes"></a>Feilrettinger

**Prosjektledelse**

Følgende problemer har blitt løst:

- Import av prosjektteammedlemmer med en tildelingsmetode som krever timer, fører til en uklar feilmelding når de angitte timene er null.
- Brukere får en feilaktig feilmelding når maksimalt antall tegn er angitt i **Beskrivelse** -feltet for en prosjektoppgave.
- Siden for **nedlasting av Microsoft Dynamics 365 Project Service Automation-tillegg** omdirigeres til den engelske nedlastingssiden når brukerens språkinnstillinger er satt til japansk.
- Når det oppstår en serverfeil, blir synkroniseringsetiketten i **Planlegg** -fanen i **Prosjekter** -skjema noen ganger forblir.
- Overflødige oppgaveoppdateringer blir sendt til serveren når en oppgave blir endret.

**Sales**

Følgende problemer har blitt løst:

- På **Kontrakt** -skjemaet oppretter dobbeltklikking **Opprett faktura** to fakturaer for én enkelt oppføring av faktiske verdier.
- I Internet Explorer 11 kan ikke brukere opprette utgiftsoppføringer.
- Tilbakeføring av kostnader og tilbakeføring av ufakturerte faktiske verdier blir ikke koblet sammen.
- **Oppdater faktiske verdier** -knappen på **Prosjekt** -skjemaet oppdaterer ikke **Faktiske timer for oppgaven**.
- **PreValidateProjectTeamMemberCreate** -plugin-modulen kan opprette dupliserte generiske ressurser som kan reserveres, når attributtet **msdyn_isgenericresourceprojectscoped** er satt til **Usann**.
- **Rekalkulerer** fjerne belastbare kostnader for produktbasert tilbudslinjedetaljer og kontraktlinjedetaljer.
- I bestemte scenarier viser **PostEstimateLineUpdate** -plugin-modulen en unntaksfeil med null referanse.
- Tidsfasevarighet i **Diagram for lønnsomhetsanalyse** samsvarer ikke med varigheten for kostnadene i detaljen for tilbudslinjen for fastpris i tilbudet.
- Enhet og enhetsgruppeverdier bruker ikke riktige standardinnstillinger for utgiftskategorier i skjemaene **Kontraktlinjedetaljer** og **Tilbudslinjedetaljer**.
- **Kostpris for organisasjonsenhet** -lister tillater overlapping i ikrafttredelsesdato.
- Brukere har ikke tillatelse til å endre **Organisasjonsenhet** når ordretypen ikke er arbeidsbasert fordi den vil føre til en unntaksfeil med nullreferanse.
- Når du prøver å navigere fra skjemaet **Tilbudslinjedetaljer** tilbake til **Tilbud** -fanen, oppdateres skjemaet og viser **Sammendrag** -fanen.