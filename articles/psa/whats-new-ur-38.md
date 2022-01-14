---
title: Hva er nytt eller endret i Project Service Automation Update Release 38, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelige i Microsoft Dynamics 365 Project Service Automation-oppdateringsutgivelsen 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901493"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og rettinger som er nye eller endrede for Project Service Automation Update Release 38, V3. Denne versjonen har et build-nummer for V3.10.59.117 og er generelt tilgjengelig via en egen oppdatering i desember 2021.

## <a name="update-release-38"></a>Update Release 38

### <a name="bug-fixes"></a>Feilrettinger

Følgende problemer har blitt løst.

**Tid og utgift**

- Det forekommer et unntak når lengden av logger for godkjenningssett overskrider 100 000 oppføringer.
- Brukere har ikke tilgang til rutenettet for **Tidsregistrering** fra hovedsiden for **Tidsoppføring**.
- Dialogboksen **Import av tidsoppføring** viser ikke tekst når ingen elementer er kvalifisert for import.
- Brukere kan opprette godkjenningssett der feltet **Målstatus** er satt til **Ukjent**.

**Prosjektledelse**

- Profiler vises ikke på riktig måte i ressurstilordninger for UTC(+09:30) og UTC(+10:00) når sommertid starter.
- Feltet **Tilleggskolonne** for arbeidsnedbrytningsstrukturer er skjult i enkelte nasjonale nasjonale data.
- Datovelgeren for kalenderkontrollen i rutenettet **Prosjektoppgave** er ikke riktig lokalisert for kinesisk.

**Salg**

- Verdiene **Kontraktytelse** og **Faktiske kostnader for prosjekt** samsvarer ikke når reserveringsbare ressurser som har forskjellige kontraktsenheter og valutaer, sender inn tidsoppføringer.
- En egendefinert arbeidsflyt for automatisk å bekrefte fakturaer mislykkes når fakturaene importeres som en administrert løsning. Følgende melding vises: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Melding: Ugyldig fakturastatus".
- Når **Rot** velges som oppsummeringsalternativ, og prosjektet har estimater fra en sammensetning av transaksjonsklasser (for eksempel en kombinasjon av tids-, utgifts- og materialestimater), oppsummeres systemet på tvers av transaksjonsklasser som én enkelt avgiftslinje.
- I scenarier der en utgiftslinje legges til før en kontraktlinje tilknyttes et prosjekt, angis ikke riktig pris som en standardverdi i feltet **Oppdater pris**-feltet.
- Negative salgsbeløp er ikke tillatt for **Prosjekt**- og **Oppgave**-enheter.
