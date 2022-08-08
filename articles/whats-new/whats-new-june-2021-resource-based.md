---
title: Nyheter juni 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra juni 2021.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028258"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter juni 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Denne artikkelen gjelder følgende komponenter og versjoner av Dynamics 365 Project Operations:

- Project Operations i Dynamics 365 Dataverse-miljø, versjon 4.11.0.156 eller 4.11.0.164.
- Prosjektstyring og regnskap i økonomi- og driftsapper, versjon 10.0.19.

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

Følgende funksjoner er inkludert i denne versjonen:

- Mulighet til å slette [prosjektfakturaforslagslinjer for justeringsscenarioer](../invoicing/correct-project-invoice-proposals.md).
- Vareutgiftslinjer gjenspeiler navn på underkategorier i utgiftsrapporten [Nyskapte utgiftsrapporter – Nye funksjoner](../expense/expense-reports-reimagined.md#new-features).
- Betalingsmåte er tilgjengelig i den nye utgiftsruten når du oppretter en ny utgift.
- Allmenn tilgjengelighet for API-er for prosjektplan. Denne nye funksjonaliteten gjør det mulig for kunder å utføre operasjoner for oppretting, oppdatering og sletting programmatisk i prosjektoppgaver, ressurstilordninger, oppgaveavhengigheter og oppføringer for prosjektteammedlemmer. Hvis du vil ha mer informasjon, kan du se [Bruk API-er for prosjektplan til å utføre operasjoner med planleggingsenheter](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Det finnes ingen oppdateringer for tilordninger av dobbel skriving i Project Operations i denne versjonen. 

Hvis du vil ha en gjeldende liste og versjoner av tilordninger for dobbel skriving i Project Operations, kan du se [Tilordningsversjoner av dobbel skriving for Project Operations](../environment/resource-dual-write-maps.md).

Kjør alltid den nyeste versjonen av tilordningen i miljøet, og aktiver alle relaterte tabelltilordninger når du oppdaterer versjonen av Project Operations Dataverse-løsningen og løsningen for økonomi- og driftsapper. Enkelte funksjoner fungerer kanskje ikke på riktig måte hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen på siden **Dobbel skriving** i kolonnen **Versjon**. Aktiver en ny versjon av tilordningen ved å velge **Versjoner av tabelltilordningen**, velge den nyeste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en medfølgende tabelltilordning, må du bruke endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem med å starte kartet, følger du instruksjonene i delen [Problem med manglende tabellkolonner på kart](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funksjonsområdet** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| Fakturering og prising | 2281417 | Løste problemet med hensyn til feilen i den automatiske fakturaopprettelseshandlingen gjennom fakturaplanen. |
| Fakturering og prising | 2287835 | Forbedret fakturabekreftelsesytelse. |
| Administrasjon av salgsmulighet | 2222555 | Materialestimaters belastbarhet må kopieres riktig til tilbudslinjedetaljer ved bruk av **Importer fra prosjektberegningen**. |
| Administrasjon av salgsmulighet | 2223427 | Tilpasninger er nå tillatt for handlingen **GenerateRetainersFromRetainerScheduleOptions**. |
| Administrasjon av salgsmulighet | 2277528 | Verdiberegning for fast faktureringsmilepæl for prosjektkontraktlinjer med flere kunder. |
| Prosjektplanlegging og sporing | 2226110 | Løste det periodisk problemet med funksjonen **Generer krav** i rutenettet **Prosjektteam**. |
| Prosjektplanlegging og sporing | 2208109 | Brukere kan ikke opprette et prosjekt i en valuta med relaterte oppgaver i en annen valuta. |
| Prosjektplanlegging og sporing | 2258228 | Listen over felter som kan endres med **planleggingsenheter** ved hjelp av API for tidsplan, er oppdatert. |
| Prosjektplanlegging og sporing | 2293989 | Riktige språk og regionale innstillinger må sendes til rutenettet **Prosjektoppgaver**. |
| Ressursbehandling | 2220493 | Løste brukeropplevelsen i rutenettet **Oppgave** ved raskt merking av en ressursforespørsel som fullført. |
| Ressursbehandling | 2330496 | Løste innlastingsproblemene for **planleggingstavlen**. (Kvalitetsoppdatering er tilgjengelig i versjon 4.11.0.164) |
| Tid og utgift | 2194431 | Rutenettet **Tidsoppføring** må overholde starten av uken slik det er angitt i **systeminnstillingene**. |
| Tid og utgift | 2277311 | Når du har slettet verdien i en celle i rutenettet **Tidsoppføring**, beholdes markøren i rutenettet. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Prosjektstyring og regnskap | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Skjemanotater** og **Skjemaoppsett** vises ikke under **oppsettet av prosjektstyring** i juridiske enheter i Finance som er integrert med Project Operations. |
| Prosjektstyring og regnskap | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Standardbeskrivelsen for mva. er tom når **posterinstypen** = **merverdiavgift** for prosjektfakturabilag. |
| Prosjektstyring og regnskap | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Doble transaksjoner posteres når oppgavebasert fakturering brukes i Dataverse med Project Operations-integrering. |
| Prosjektstyring og regnskap | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Prosentandelen som er fullført i omsetningsgjenkjenning, er feil ved bruk av Project Operations-integrering. |
| Prosjektstyring og regnskap | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Omsetningsavsetningen dobles på en ventende leverandørfaktura i et integrert scenario for Project Operations. |
| Prosjektstyring og regnskap | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Kan ikke postere integreringsjournalen når regelen for omsetningsprofilen er satt til **Gruppeoppsett**. |
| Prosjektstyring og regnskap | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | En kjøpsfaktura kan ikke posteres for prosjektbestillinger som har linjer med flere målenheter. |
| Prosjektstyring og regnskap | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Standard finansdimensjon på et prosjekt kan ikke oppdateres ved hjelp av dataenheten Prosjekter **V2**. |
| Prosjektstyring og regnskap | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Det tar for lang tid å fullføre den satsvise prosessen for oppretting av prosjektestimater. |
| Prosjektstyring og regnskap | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Sletting av en kontrakt sletter også adressen som er tilknyttet kunden. |
| Reise og utgift | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Arbeidsflytbetingelsen for godkjenning av utgiftsrapport evalueres ikke på riktig måte. |
| Reise og utgift | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Policyen for utgiftsrapport evaluerer ikke prosjekt-ID-en riktig. |
| Reise og utgift | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Handlingen, **Deles til personlig for konserninterne utgiftstransaksjoner** fungerer ikke som den skal. |
| Reise og utgift | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Justeringer i utgiftsrapportlinje slettes utilsiktet når visse reiserekvisisjoner slettes. Dette skjer når recID for utgiftsrapporten og reiserekvisisjonen er den samme. |
| Reise og utgift | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Det oppstår et problem i Utgift-mobilappen når feltet **Prosjekt-ID** kreves i policyer for utgiftsrapport. |
| Reise og utgift | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Konserninterne utgifter som er knyttet til et prosjekt, kan ikke redigeres. I stedet vises følgende feilmelding: Objektreferansen er ikke angitt til en forekomst av et objekt. |
| Reise og utgift | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Etter at utgiftsrapporten er postert, vises feil valuta og beløp i bankdelfinans. |
| Reise og utgift | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Det er gjort forbedringer i funksjonen *Slett kredittkorttransaksjoner*.  |
| Reise og utgift | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Merverdiavgift inkludert i en utgiftsrapport beregnes ikke konsekvent når en annen rapporteringsvaluta er angitt i en juridisk enhet. |
| Reise og utgift | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Ytelsen påvirkes når du legger til en ny kontant reiseutgift. |
| Reise og utgift | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Utgiftspolicyregelene utløses ikke i en utgiftsrapport. |
| Reise og utgift | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Opplasting av en ny delt kategori ved hjelp av Data Management Framework fjerner alle underkategorier for alle delte kategorier. |
| Reise og utgift | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Når du oppretter en utgiftslinje og deretter velger en kategori, oppstår følgende feilmelding: Kombinasjonen av DOM for mva-gruppe og STD for mva-gruppe for vare er ikke gyldig. |
| Reise og utgift | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Det er synkroniseringsproblemer i Utgift-mobilappen. |
