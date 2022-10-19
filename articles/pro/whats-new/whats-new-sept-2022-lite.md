---
title: Nyheter september 2022 – Project Operations Lite-distribusjon
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Microsoft Dynamics 365 Project Operations Lite-distribusjon fra september 2022.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634865"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Nyheter september 2022 – Project Operations Lite-distribusjon

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.46.0.60

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

| Funksjonsområdet | Funksjonsnavn | Mer informasjon |
| --- | --- | --- |
| Administrasjon av salgsmulighet | **Revisjon og aktivering av tilbud**<br>Project Operations har fullstendig støtte for salgsprosessen. Prosjekttilbud kan aktiveres for å representere en tilstand der tilbudet er skrivebeskyttet og blir gjennomgått. Aktiverte tilbud kan revideres for å opprette nye tilbud som har et trinnvis revisjonsnummer. Aktiverte prosjekttilbud eller tilbudsrevisjoner kan lukkes som vunnet eller tapt. | [Aktiver og revider et prosjekttilbud](/dynamics365/project-operations/sales/activation-and-revision) |
| Fakturering og prising | **Tidssoneagnostisk prisstandard**<br>Project Operations har innført konseptet med en tidssoneagnostisk dato for alle faktiske verdier for prosjekt. Et nytt felt, **Transaksjonsdato**, er nå tilgjengelig på journallinjer og faktiske verdier og brukes til å lagre datoen da transaksjonen forekom, men uten å konvertere denne datoen til Coordinated Universal Time. Denne datoen brukes til nedstrømsprosesser, for eksempel prisstandard og opprettelse av faktura. | <p>[Fastslå kostnadssatser for prosjektbaserte estimater og faktiske verdier](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Fastslå salgspriser for prosjektbaserte estimater og faktiske verdier](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Fakturering og prising | **Datoeffektive prisoverstyringer i Project Operations**<br>Datoeffektive prisoverstyringer gjør at du kan overstyre eller endre bestemte priser i prislisten. | [Datoeffektive prisoverstyringer](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Tid og utgift | **Global godkjenner**<br>Denne funksjonen aktiverer uavhengige programvareleverandører (ISV) og sentralisert godkjenning, uavhengig av statusen for prosjekt- eller teammedlem i prosjektet. | [Sikkerhet og godkjenninger](/dynamics365/project-operations/approvals/approvals-security) |
|Prosjektplanlegging og sporing|**Bruk API-er for prosjektplan til å utføre operasjoner med planleggingsenheter** </br> </br>API-en for redigering av ressurstilordninger gjør det mulig for utviklere å programmatisk angi en oppgavetilordningspersons innsats i alle støttede datointervaller for mer detaljert planlegging av faser i tid.|[Bruk API-er for prosjektplan til å utføre operasjoner med planleggingsenheter](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Kvalitetsoppdateringer

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Fakturering og prising | 2754422 | Materiale- og utgiftsestimater flyter ikke til Dynamics 365 Finance når prosjekter kopieres i Dataverse. |
| Tid og utgift | 2787409 | En ugyldig godkjenner kan godkjenne en tidsoppføring som ikke er knyttet til et prosjekt. |
| Administrasjon av salgsmulighet | 2788907 | Oppdatert feilmelding om unikhetsvalidering for ordrelinjer som inneholder flagg. |
| Tid og utgift | 2842253 | Håndtering av nullunntak for tidsgodkjenning. |
| Fakturering og prising | 2844181 | Mislykket forsøk på å hente korrelasjons-ID-en blokkerer fakturaopprettelse. |
| Fakturering og prising | 2876628 | QLD, CLD – Løsningen for estimering av prisliste skal bruke eldre felter for datointervall i prislisten. |
| Utsetting | 2893222 | Hvis ingen rolle er angitt for en underkontraktlinje, må det gå an å velge denne linjen på et teammedlem for enhver rolle. |
