---
title: Hva er nytt eller endret i Project Service Automation Update Release 37, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelige i Microsoft Dynamics 365 Project Service Automation-oppdateringsutgivelsen 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727617"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og rettinger som er nye eller endrede for Project Service Automation Update Release 37, V3. Denne versjonen har buildnummeret V3.10.58.120 og er allment tilgjengelig via en egenoppdatering i november 2021.

## <a name="update-release-37"></a>Update Release 37

### <a name="bug-fixes"></a>Feilrettinger

Følgende problemer har blitt løst.

**Tid og utgift**
- Brukere kan ikke slette en tidsoppføring ved å tømme cellen.
- Visningen **Mine mislykkede godkjenninger** inneholder bare prosjektgodkjenninger med statusen **Sendt**.

**Prosjektledelse**
- Brukere får en nullreferanseunntaksfeil når de åpner et prosjekt i tilleggsprogrammet for stasjonær Microsoft-datamaskin hvis prosjektteammedlemmets stillingsnavn er tomt.
- Det finnes ingen **Lagre**-knapp på **Prosjektoppgave**-siden, så brukere ikke kan lagre endringer i oppgaveoppføringer.
- Brukere kan ikke slette et prosjekt som har en oppgave tilknyttet et tilbud med statusen **Vunnet**.

**Salg**
- **Valuta**-feltet på **Prosjekt**-siden er oppdatert slik at det samsvarer med valutaen for den gjeldende malen.
- Kostnaden beregnes feil på oppgaver som har flere valutaer.
