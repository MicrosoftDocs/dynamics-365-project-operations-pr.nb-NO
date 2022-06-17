---
title: Nyheter november 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra november 2021.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932906"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter november 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

*Gjelder: Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer*

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.22

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

Følgende funksjoner er inkludert i denne versjonen:

- API-er (programmeringsgrensesnitt) for prosjektplanlegging har nå støtte for å opprette og slette prosjektsamlinger.

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Det finnes ingen oppdateringer for tilordninger av dobbel skriving i Project Operations i denne versjonen. Hvis du vil ha en gjeldende liste og versjoner av tilordninger for dobbel skriving i Project Operations, kan du se [Tilordningsversjoner av dobbel skriving for Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Kjør alltid den nyeste versjonen av tilordningen i miljøet, og aktiver alle relaterte tabelltilordninger når du oppdaterer versjonen av Project Operations Dataverse-løsningen og Finance-løsningen. Enkelte funksjoner fungerer kanskje ikke riktig hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en bruksklar tabelltilordning, bruker du endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem når du starter tilordningen, følger du instruksjonene i delen [Problemer med manglende tabellkolonner i tilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-in-dataverse"></a>Project Operations i Dataverse

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Fakturering og prising | 2240080 | Feltet **Betalingsbetingelser** kan ikke dupliseres på proformafakturaen. |
| Fakturering og prising | 2358236 | Fakturakorreksjon må tillate korreksjoner som har nullprislinjer. |
| Ressursbehandling | 2410072 | Tillat konfigurasjon av en ressurs som er tilordnet til oppgaven som en prosjektleder. |
| Fakturering og prising | 2430234 | Løste et problem med beregning av kostnadsytelse. |
| Tid og utgift | 2436978 | La tid angis i formatet tt:mm. |
| Fakturering og prising | 2448623 | La prislister oppdateres etter at de er knyttet til en organisasjonsenhet. |
| Tid og utgift | 2460396 | Gjør at en tidsoppføring kan slettes ved å tømme cellen. |
| Fakturering og prising | 2467386 | Gjør at et prosjekt som har en oppgave, kan slettes, selv når oppgaven er knyttet til et vunnet tilbud. |
| Tid og utgift | 2461744 | Visningen **Mine mislykkede godkjenninger** inneholder bare prosjektgodkjenninger i fasen **Sendt**. |
| Tid og utgift | 2464082 | Fjern koblingen fra prosjektgodkjenninger til godkjenningssettet når det er samsvar med en målstatus. |
| Tid og utgift | 2468108 | Planlegg-jobben skal ikke angi statusen **Behandler** for godkjenningssettet. |
| Tid og utgift | 2471503 | Slett godkjenningssett som er sju dager gamle. |
| Fakturering og prising | 2480687 | Referansen til tilbudslinjen må ikke fjernes når en milepæl for tilbudslinje opprettes. |

### <a name="project-management-and-accounting-in-finance"></a>Oversikt over prosjektstyring og regnskap i Finans

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Prosjektstyring og regnskap | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Tilbakeholdte leverandørbeløp i prosjektutgiftstransaksjoner vises ikke i transaksjonslisten. |
| Prosjektstyring og regnskap | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Den konserninterne leverandørfakturaen ødelegges når integrering av leverandørfaktura er aktivert. |
| Prosjektstyring og regnskap | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Betalingsbetingelsene på prosjektfakturaer fungerer ikke som forventet. |
| Prosjektstyring og regnskap | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Når det tilbakeholdte leverandørbeløpet frigis, får bilagsposteringen tilleggslinjer som er feil. |
| Prosjektstyring og regnskap | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Når journalen for Project Operations-integrering posteres, mislykkes den på grunn av manglende dimensjoner for en konto det ikke posteres til. |
| Prosjektstyring og regnskap | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Prosjekt**-fanen kan ikke redigeres i en ventende leverandørfaktura når innkjøpskategorien er tilordnet til varen. |
| Prosjektstyring og regnskap | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigasjonsruten mangler hvis du ikke er logget på Project Operations Dataverse. |
| Prosjektstyring og regnskap | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Når du posterer omsetning fra en prosjektfaktura i et tilfelle med brukt honorar, oppstår det et problem fordi transaksjonene i bilaget ikke er i balanse. |
| Prosjektstyring og regnskap | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Hvis du oppretter et estimat etter at du har postert et fakturaforslag, blokkeres rettelseslinjer fra import. |
| Prosjektstyring og regnskap | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Endring av en fullstendig fakturert milepæloppføring skal ikke være mulig. |
| Reise og utgift | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Alle utgiftsrapporter vises når du søker etter en kategori i mobilappen for utgifter. |
| Reise og utgift | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Det posteres feil beløp i leverandørtransaksjoner og salgsavgiftstransaksjoner fra en utgift som opprettes fra en kredittkorttransaksjon. |
| Reise og utgift | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Det vises en irrelevant advarsel når du oppdaterer siden **Utgiftsrapport**. |
| Reise og utgift | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Feil midlertidig godkjenner brukes når du sletter en midlertidig godkjenner og deretter sender inn en utgiftsrapport på nytt via arbeidsflyten. |
| Reise og utgift | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Det oppstår en posteringsfeil som er knyttet til konfigurasjon av reisegodtgjørelse. |
