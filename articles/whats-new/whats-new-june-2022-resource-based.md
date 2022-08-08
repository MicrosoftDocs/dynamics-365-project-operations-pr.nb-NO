---
title: Nyheter juni 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Microsoft Dynamics 365 Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra juni 2022.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031343"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter juni 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.43.0.77 eller 4.43.0.119
- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Tabellen nedenfor viser tilordningene for dobbel skriving som er endret eller lagt til i juni 2022-versjonen av Project Operations.

| Enhetstilordning | Oppdatert versjon | Kommentarer |
| --- | --- | --- |
| Project Operations-integrering, prosjektleverandør fakturaeksportenhet (msdyn_projectvendorinvoices) | 1.0.0.1 | Det gamle feltet er avskrevet og tilordnet til det nye feltet for sporing av leverandørfakturatilstand. |

Kjør alltid den nyeste versjonen av tilordningen i miljøet, og aktiver alle relaterte tabelltilordninger når du oppdaterer versjonen av Project Operations Dataverse-løsningen og Finance-løsningen. Enkelte funksjoner fungerer kanskje ikke riktig hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en bruksklar tabelltilordning, bruker du endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem når du starter tilordningen, følger du instruksjonene i delen [Problemer med manglende tabellkolonner i tilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Utsetting | 2708885 | Rettet feilmeldingen som vises når en bruker oppretter en oppføring for overskrift for bestilling av ressurs som kan reserveres, der ingen ressurs som kan reserveres, er fylt ut. |
| Prosjektplanlegging og sporing | 2629441 | Rettet logikken for utløsing av arbeidsflyt for å forhindre en uendelig løkke når prosjektoppgaver oppdateres. |
| Tid og utgifter | 2641209 | Import av tidsoppføringer fra tilordninger/bestillinger må beholde en ressursreferanse som kan reserveres. |
| Prosjektplanlegging og sporing | 2651148 | Prosjektdokumenttoppteksten må beskyttes.|
| Prosjektplanlegging og sporing | 2653145 | La til valideringer for å sikre at det ikke kan opprettes en prosjektoppføring med ugyldige tegn i navnet. |
| Tid og utgifter | 2654710 | Rettet filtreringen på **Godkjenninger**-siden. |
| Fakturering og prising | 2667805 | La til valideringer for å forhindre at fakturerte faktiske salg opprettes hvis det ikke finnes støttende ufakturerte faktiske salg. |
| Fakturering og prising | 2668378 | La til valideringer for å forhindre at en egendefinert prisdimensjon legges til, med mindre et logisk navn og et feltnavn fylles ut. |
| Utsetting | 2677485 | Oppdaterte målversjonen av tilordningen med dobbel skriving for leverandørfakturalinjer. |
| Tid og utgifter | 2700428 | Forbedret godkjenningslogikken for å sikre at andre godkjenningssett for prosjektet kan behandles selv om et av godkjenningssettene står fast i systemjobber. |

### <a name="project-management-and-accounting-in-finance"></a>Oversikt over prosjektstyring og regnskap i Finans

Hvis du vil ha informasjon om feilrettinger som er inkludert i denne oppdateringen, logger du på Microsoft Dynamics Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
