---
title: Hva er nytt eller endret i Project Service Automation Update Release 31, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 31, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945547"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 31. Denne versjonen har et build-nummer på V3.10.52.77 og er generelt tilgjengelig via en egen oppdatering i mai 2021.

## <a name="update-release-31"></a>Update Release 31

### <a name="bug-fixes"></a>Feilrettinger

**Tid og utgift**

Følgende problemer har blitt løst:

- Kommandoknappene for tidsregistreringskontroll på siden **Ressurs som kan reserveres**, var forvirrende.
- Det ble generert et nullreferanseunntak i **Project.SetTrackingFields** under godkjenning av en tidsoppføring.

**Ressursbehandling**

Følgende problemer har blitt løst:

- **Opprett teammedlem** viser ikke metadatainnstillingen for bestillingsoppsett for **Status for registrert standardbestilling** på riktig måte.
- Når du oppgraderer fra PSA 1.X til 3.X, mislykkes oppgraderingsprosessen på **UpgradeResourceRequirements**.


**Salg**

Følgende problemer har blitt løst:

- Faktisk omsetning konverterer beløpene til prosjektvalutaen i sporingsrutenettet.
- Valutastandarden er uklar når du oppretter journallinjer, tilbudslinjer og kontraktlinjer i scenarier der standardvalutaen for en organisasjon er forskjellig fra prosjektvalutaen.
- Spørringen **Venter på korrigering av journalvalidering** filtreres ikke etter prosjekt.
- Resterende salg beregnes feil på et prosjekt.
- Tilbud basert på en kontakt mislykkes når de opprettes uten en prisliste.
- Ingen behandlingsspinner vises når du velger **Bekreft faktura**.
- Ingen behandlingsspinner vises når du velger **Opprett faktura**.
- Hvis du lukker et tilbud som tapt, annulleres ikke bestillingene.







