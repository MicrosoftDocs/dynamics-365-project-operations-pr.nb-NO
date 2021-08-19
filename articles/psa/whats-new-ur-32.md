---
title: Hva er nytt eller endret i Project Service Automation Update Release 32, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994873"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 32. Denne versjonen har buildnummeret V3.10.53.108 og er vanligvis tilgjengelig via en egenoppdatering i juni 2021.

## <a name="update-release-32"></a>Update Release 32

### <a name="bug-fixes"></a>Feilrettinger

#### <a name="general"></a>Generelt

- Når en større oppgradering mislykkes, bør bare hovedinngangspunktene i programmet blokkeres for å sikre at delte enheter fremdeles er tilgjengelige.

#### <a name="time-and-expense"></a>Tid og utgift

Følgende problemer har blitt løst:

- **TimeEntriesImportFromResourceAssignment** vedlikeholder ikke start- og sluttidspunktene for omfangsdelen for ressurstilordningen.
- Når du velger **Åpne oppføring** i rutenettet for **Tidsoppføring**, kan det hende du ikke kan velge andre skjemaer.
- Når du importerer tilordninger til tidsoppføringer, kan klientkodespørringen generere en lang URL-adresse som mislykkes i spørringen.
- Når en verdi er slettet fra en celle i rutenettet for **Tidsoppføring**, blir ikke fokuset værende i rutenettet.
- **Avvis**-knappen er fjernet fra visningen **Behandling av godkjenninger** for moderne godkjenninger.
- Stabiliteten og ytelsen til massegodkjenning av tidsregistrering påvirkes av vranglåser, og det oppstår en feil under behandling av tilpassinger som er relatert til **Tidsoppføring**-enheten.

#### <a name="project-planning"></a>Prosjektplanlegging

- Det genereres et nullreferanseunntak når du oppdaterer et prosjekt som har en nullverdi i feltet **Kontraktenhet**.
- **Oppdater totalsummer for prosjektet** feilberegner gjenstående kostnad og gjenstående salg for et prosjekt.
- Overflødige prisberegninger påvirker ytelsen som er relatert til oppdateringer for ressurstilordninger.

#### <a name="resource-management"></a>Ressursbehandling

Følgende problem er løst:

- Når kalenderkapasiteten for en ressurs som kan reserves, er mer enn 1, gjenkjenner Project Service Automation feilaktig kapasiteten som 0 (null). Derfor oppstår en uendelig løkkei tidsplanvisningen.

#### <a name="sales"></a>Salg

Følgende problemer har blitt løst:

- Når det opprettes en journallinje som har en egendefinert transaksjonstype, oppstår følgende nullreferanseunntak: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Roller og kategorier som er deaktivert før et tilbud er kopiert, må ikke legges til belastbare roller og kategorier for det nylig kopierte tilbud.
- Dokumentdatoen og regnskapsdatoen er ikke justert med startdatoen som er angitt på en fakturalinjedetalj som opprettes direkte på et fakturautkast.
- Nullreferanseunntak genereres i scenarier som er relatert til inaktivering av roller og kategorier før et tilbud kopieres.
- Handlingen **Oppdater priser** på **Prosjekter**-siden oppdaterer ikke kostnadsestimater og materielle estimater.
