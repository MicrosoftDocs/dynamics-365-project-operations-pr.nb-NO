---
title: Nyheter mars 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra mars 2021.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fbdcb01117c39f879f80319b01d278c91a56e8f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932952"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter mars 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Denne artikkelen gjelder følgende komponenter og versjoner av Dynamics 365 Project Operations:

- Project Operations på Dataverse-miljø versjon 4.8.0.91 
- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.16 

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse


| **Funksjonsområdet** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| Fakturering og prising | 2133873 | Løste visningen av valutasymbolet **Enhetssalgspris** i rutenettet **Utgiftsestimater**. |
| Fakturering og prising | 2174616 | Når et tilbud blir vunnet, refereres det til den egendefinerte prislisten for kontrakten på kontraktlinjedetaljer som kopieres fra tilbudet. |
| Administrasjon av salgsmulighet | 2167475 | Løste avgiftsbeløp i rettelsesfakturaen som opprinnelig var en ufakturert faktisk oppføring. |
| Administrasjon av salgsmulighet | 2176285 | Avgiftsbeløp må ikke kopieres fra detaljer om salgskontrakt/tilbudslinje til detaljer om kostnadskontrakt/tilbudslinje. |
| Administrasjon av salgsmulighet | 2188079 | Delt faktureringsregel må ikke opprettes for kontrakter som ikke er arbeidsbaserte. |
| Planlegging og sporing | 2125274 | Attributtet **Prosjekt med dobbel skrivetilordning** for **prosjektstartdatotilordning** er oppdatert fra **msdyn\_taskearlieststart** til **msdyn\_actualstart**. |
| Planlegging og sporing | 2138853 | Prosjektkopieringsfunksjon er oppdatert for å sikre at kostnadsestimatlinjer som refererer til oppgaver, kopieres til målprosjektet. |
| Planlegging og sporing | 2154306 | Løste problemer med sletting av utgiftsestimater i Project Operations for ressursbaserte scenarioer. |
| Planlegging og sporing | 2173259 | Prosjektkopieringsfunksjon er oppdatert for å sikre at den ikke viser feilmeldingen **Kopierer WBS** i bestemte scenarioer. |
| Tid og utgift | 2148910 | Løste visningsproblem med siden **Rediger oppføring** i rutenettet **Tidsoppføring**. |
| Tid og utgift | 2159798 | Innsnevret kontroller for å sikre at godkjente utgiftsoppføringer ikke kan redigeres. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

Se [Nyheter januar 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer](whats-new-jan-2021-resource-based.md) for mer informasjon.

## <a name="regulatory-updates"></a>Forskriftsmessige oppdateringer

Hvis du vil ha informasjon om forskriftsmessige oppdateringer for økonomi- og driftsapper, kan du se [Forskriftsmessige oppdateringer](/dynamics365/finance/localizations/regulatory-updates). En annen måte å lære om regelverksoppdateringer på, er å logge på LCS og vise de planlagte forskriftsoppdateringene ved hjelp av problemsøkeverktøyet. Problemsøk lar deg søke etter land, type funksjon og utgave.


[!INCLUDE[footer-include](../includes/footer-banner.md)]