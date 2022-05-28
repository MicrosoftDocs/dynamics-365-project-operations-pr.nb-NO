---
title: Hva er nytt eller endret i Project Service Automation Update Release 36, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelige i Microsoft Dynamics 365 Project Service Automation-oppdateringsutgivelsen 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 108c75598dc7dd3dd0cdb9ce68e30423d051a4cf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586678"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og rettinger som er nye eller endrede for Project Service Automation Update Release 36, V3. Denne versjonen har buildnummer V3.10.57.152 og er vanligvis tilgjengelig via en egen oppdatering i oktober 2021.

## <a name="update-release-36"></a>Update Release 36

### <a name="bug-fixes"></a>Feilrettinger

Følgende problemer har blitt løst.

**Generelt**
- Feltnavnet **Standard arbeidstidsmal** oversettes feil på siden **Prosjektparametere**.
- Asynkrone programtillegg håndterer ikke unntak som er relatert til **SharedVariableService**, på riktig måte.

**Tid og utgift**
- Når det mangler journallinjer eller brukeren ikke har de riktige rettighetene til å lese journallinjer, oppstår det en feil når prosjektgodkjenninger annulleres.
- Brukere kan ikke annullere en godkjenning når en utgifts- eller tidsoppføring har mer enn én tilknyttet prosjektgodkjenning.
- **Fravær** og **Ferie** oversettes feil for det kinesiske språket i et oppslag på hurtigopprettingssiden **Tidsoppføring**.

**Ressursstyring**
- Brukeren kan ikke søke etter ressurser i **Planleggingsassistent** når visningsmodusen er satt til **Dag**, **Uke** eller **Måned**.
- Generelle ressurser kan ikke ha tomme posisjonsnavn. 
- Hvis du lukker en kontrakt som tapt, annulleres ikke fremtidige bestillinger.

**Salg**
- Når et miljø har et stort volum produkter, reduseres ytelsen i rutenettet **Materialestimat**.
- Når du oppretter et prosjekt fra en mal, brukes ikke prosjektvalutaen som standard i den respektive prosjektlederens kontraktsenhet.
- Faktiske beløp samsvarer ikke alltid med det som gjenspeiles i forfall for prosjektet, eller beløpene blir negative i bestemte tilbakekallingsscenarioer.
- Det oppstår en feil når du knytter et prosjekt opprettet fra prosjektmalen til en kontraktlinje.
- Brukere kan slette en kontraktlinje med milepælene **Klar for fakturering** og **Faktura opprettet**. Dette skal ikke være tillatt.
- Når estimater importeres fra et prosjekt, angis avgiftsnivået for tilbudslinjen på feil måte når oppgavebasert fakturering er aktivert for tilbudslinjen.
- Når du legger til en faktureringsmilepæl med fast pris, vises ikke milepælen i delskjemaet for milepælen før siden oppdateres.
- Det genereres et nullreferanseunntak når du oppretter en prosjektkontrakt med et tilbudsnavn som er null.
- Manuelle oppgaver i manuell modus der prosjektvalutaen er forskjellig fra valutaen for ressursen, fører til feil prisestimater.
- Brukere kan ikke tilbakekalle en transaksjon som er korrigert med en korrigering av en korrigeringsfaktura.
- Deaktiverte transaksjonskategorier vises i rutenettet **Kostnadsestimater**.



