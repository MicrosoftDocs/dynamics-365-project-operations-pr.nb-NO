---
title: Nyheter februar 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra februar 2021.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1fe1e59a0a3674752fe62525349a50f00e11089b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029634"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter februar 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Denne artikkelen gjelder følgende komponenter og versjoner av Dynamics 365 Project Operations:

- Project Operations i Dataverse-miljø 4.7.0.95
- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.16 

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funksjonsområde** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| **Fakturering og prising** | 2053736 | Fakturalinjedetaljer er nå tilgjengelige ved å gå til **Faktura** > **Relatert informasjon**. |
| **Fakturering og prising** | 2122613 | Handlingene **Aktiver** og **Deaktiver** ble fjernet fra tilknytningsenhetene for **Prisliste**. |
| **Fakturering og prising** | 2128606 | Løste problemet med **ullReferenceException** i programtillegget **GetEstimatesForProject**. |
| **Distribusjon og konfigurasjon** | 2139346 | Løste problemet med import av uadministrert **Dynamics365ProjectOperationsDualWrite**-løsning. |
| **Distribusjon og konfigurasjon** | 2140569 | Prosjektløsningen må ikke installeres i Dataverse Teams-miljøene. |
| **Distribusjon og konfigurasjon** | 2086991 | Begrenset tilpassing av lokalisering av webressurser. |
| **Administrasjon av salgsmulighet** | 2136794 | Vis den riktige feilmeldingen når prosessen **Bekreft faktura** eller **Merk faktura som betalt** mislykkes. |
| **Administrasjon av salgsmulighet** | 2139330 | Endring av prosjektlederen i et prosjekt kan ikke tilbakestille det eiende firmaet tilbake til standardverdien. |
| **Administrasjon av salgsmulighet** | 2146376 | Korrigert avgiftsbeløp i en ikke-belastbar faktisk verdi opprettes fra fakturabekreftelsen. |
| **Prosjektplanlegging og sporing** | 2099879 | Distribusjonen i Dataverse-miljøet må opprette en standard transaksjonskategori med en statisk ID og ikke generere én tilfeldig per miljø. |
| **Prosjektplanlegging og sporing** | 2128577 | Løste brukerrettighetene for prosjektservice for å oppdatere transaksjonskategorien for en ressurstilordning. |
| **Prosjektplanlegging og sporing** | 2164035 | Løste problemer med funksjonen **Kopier prosjekt**. |
| **Tidsoppføring** | 2129161 | Begrensninger for inntasting brukes for å sikre at brukere ikke kan endre og oppdatere en tidsoppføring som er sendt eller godkjent. |
| **Tidsoppføring** | 2103572 | Tidsgodkjenning for ikke-prosjekttidsoppføringer kan ikke se etter prosjektgodkjennelsesrolle. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance 

Hvis du vil ha mer informasjon om prosjektstyring og regnskap i Dynamics 365 Finance, kan du se [Nyheter januar 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Forskriftsmessige oppdateringer

Hvis du vil ha informasjon om forskriftsmessige oppdateringer for økonomi- og driftsapper, kan du se [Forskriftsmessige oppdateringer](/dynamics365/finance/localizations/regulatory-updates). En annen måte å lære om regelverksoppdateringer på, er å logge på Lifecycle Services (LCS) og vise de planlagte forskriftsoppdateringene ved hjelp av problemsøkverktøyet. Problemsøk lar deg søke etter land, type funksjon og utgave.


[!INCLUDE[footer-include](../includes/footer-banner.md)]