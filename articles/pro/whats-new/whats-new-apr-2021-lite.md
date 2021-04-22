---
title: Nyheter april 2021 – Project Operations Lite-distribusjon
description: Dette emnet inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i april 2021-versjonen av Project Operations Lite-distribusjonen.
author: sigitac
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd6fbe8d75fbe9157a97d2edd38d40a97395c924
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868050"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Nyheter april 2021 – Project Operations Lite-distribusjon

_Gjelder: Lite-distribusjon – avtale til proformafakturering_

Dette emnet gjelder for følgende Dynamics 365 Project Operations-komponenter og versjoner:

  - Project Operations på Dataverse-miljø versjon 4.9.0.221 

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

Følgende funksjoner er inkludert i denne versjonen:

- Ikke-lagerført materiell for prosjekter. Viktige funksjoner omfatter følgende:
  - Estimering og prising av ikke-lagerført materiell i salgssyklusen for et prosjekt. For mer informasjon, se [Konfigurere kostnads- og salgspriser for katalogprodukter – Lite](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Sporing av bruken av ikke-lagerført materiell under prosjektlevering. For mer informasjon, se [Registrer materialbruk på prosjekter og prosjektoppgaver](../../material/material-usage-log.md).
  - Fakturering av kostnader for ikke-lagerført materiell som er brukt. For mer informasjon, se [Administrere faktureringsrestansen – Lite](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Nye API-er i Dynamics 365 Dataverse tillater oppretting, oppdatering og sletting med **planleggingsenheter**. For mere informasjon, se [Bruke API-er for tidsplan til å utføre operasjoner med planleggingsenheter](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Kvalitetsoppdateringer

| **Funksjonsområdet** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| Fakturering og prising | 2224568 | Lagt til logikk for å aktivere tilpassinger som involverer aktivering av plugin-modulen for fakturabekreftelse. |
| Fakturering og prising | 2101098 | Forbedret logikken for standardfelt til proformafaktura: **Fakturaadresse**, **Fakturanavn** og **Betalingsbetingelser** angis nå som standard fra den tilsvarende kundeoppføringen i prosjektkontrakten. |
| Fakturering og prising | 2021413 | Oppdaterte feltene **Faktisk kostnad** og **Salg** i **Oppgave**-enheten for å inkludere salgsverdier fra ufakturerte og fakturerte utgifter for oppgaver. |
| Fakturering og prising | 2182110 | Når du kopierer en prosjektkontrakt, genereres kontraktlinje-ID-en på nytt i målprosjektkontrakten for å sikre at den er unik. |
| Administrasjon av salgsmulighet | 2186741 | Valideringer som er lagt til for å sikre at **Opprinnelse**-feltet og **Transaksjonstype** ikke kan oppdateres for eksisterende tilbudslinjedetaljer. |
| Administrasjon av salgsmulighet | 2191353 | Milepæler kan ikke opprettes på en kontraktlinje for tid og materialer. |
| Administrasjon av salgsmulighet | 2216956 | Løste problemer med **Oppdater priser**. |
| Planlegging og sporing | 2182979 | Forbedret prosjektkopieringsfunksjonen for å sikre at utgiftsestimatlinjene kopieres fra det opprinnelige prosjektet. |
| Planlegging og sporing | 2184144 | Forbedret prosjektkopieringsfunksjonen for å sikre at navnet på ressursposisjonen kopieres fra det opprinnelige prosjektet. |
| Planlegging og sporing | 2184799 | Prosjektkopiering: Strammet inn kontrollen for å sikre at den estimerte startdatoen ikke kan endres under kopiering. |
| Planlegging og sporing | 2185134 | Prosjektkopiering: Estimert startdato for målprosjektet er satt til dagens dato. |
| Planlegging og sporing | 2196373 | Prosjektkopiering: Kontroller at prosjektleder- og teammedlemsoppføringer ikke dupliseres i prosjektteamet. |
| Planlegging og sporing | 2211833 | Prosjektkopiering: Ressurstilordninger kopieres fra kildeprosjektoppgaven til målprosjektet. |
| Planlegging og sporing | 2186541 | Løste problemer i **Estimater**-rutenettet ved gruppering etter ressurs. |
| Planlegging og sporing | 2166906 | Transaksjonskategorien fra en oppgave må kopieres til enheten **Ressurstilordning**. |
| Ressursbehandling | 2125362 | Løste problemer med oppretting av et generelt teammedlem ved hjelp av en timesbasert tildelingsmetode. |
| Tid og utgift | 2113603 | Løste det tilpassingsrelaterte problemet med å fjerne attributter fra **Tidsregistrering**-siden. Systemet kontrollerer nå om attributtet finnes på siden før det får tilgang til dem ved hjelp av et skript. |
| Tid og utgift | 2204377 | Kopierte timeregistreringer må vises automatisk når du velger **Kopier uke** i tidsoppføringen. |
| Tid og utgift | 2209059 | **Status**-feltet kan redigeres for tidsoppføringer i Dynamics 365 Field Service. |
