---
title: Nyheter juli 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Microsoft Dynamics 365 Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra juli 2022.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183923"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter juli 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.44.0.22
- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Det finnes ingen oppdateringer for tilordninger av dobbel skriving i Project Operations i denne versjonen. Hvis du vil ha en gjeldende liste og versjoner av tilordninger for dobbel skriving i Project Operations, kan du se [Tilordningsversjoner av dobbel skriving for Project Operations](../environment/resource-dual-write-maps.md).

Kjør alltid den nyeste versjonen av tilordningen i miljøet, og aktiver alle relaterte tabelltilordninger når du oppdaterer versjonen av Project Operations Dataverse-løsningen og Finance-løsningen. Enkelte funksjoner fungerer kanskje ikke riktig hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en bruksklar tabelltilordning, bruker du endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem når du starter tilordningen, følger du instruksjonene i delen [Problemer med manglende tabellkolonner i tilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Distribusjon og konfigurasjon | 2761472 | Installasjonsfeil for Project Operations håndteres. |
| Fakturering og prising | 2746940 | Navnet på underkontraktlinjen må ha en maksimumslengde på 100 tegn. |
| Fakturering og prising | 2739162 | Kunder må kunne se båndknapper i den faktiske rutenettvisningen. |
| Prosjektplanlegging og sporing | 2730318 | Oppdatert validering for tegn som ikke støttes i prosjektemnet. |
| Fakturering og prising | 2705361 | Faktiske verdier for fakturert salg for milepæl må inkluderes i prosjektsporingsfelt. |
| Fakturering og prising | 2675880 | Forhindre at et prosjekt kobles til en kontraktlinje som ikke er arbeidsbasert. |
| Fakturering og prising | 2664396 | Hvis en tilbudsprisliste lagres uten et tilbud, må det finnes en feil som angir at tilbudet ikke kan være tomt. |
| Fakturering og prising | 2184019 | Kategorien **Oppgavebasert fakturering** skal ikke vises for prosjekter som ikke har støttekontrakt eller tilbud. |

### <a name="project-management-and-accounting-in-finance"></a>Oversikt over prosjektstyring og regnskap i Finans

Hvis du vil ha informasjon om feilrettinger som er inkludert i denne oppdateringen, logger du på Microsoft Dynamics Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funksjoner som er aktivert som standard i den neste versjonen

Denne tabellen viser funksjonene som er aktivert som standard i versjon 10.0.29. De fleste funksjoner som er aktivert automatisk, kan slås av i [Funksjonsbehandling](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). I fremtiden kan det hende at enkelte funksjoner som har blitt slått på automatisk, blir fjernet fra Funksjonsbehandling og blir obligatoriske. Denne endringen sikrer at kunder bruker gjeldende funksjonalitet, slik at forbedringer kan bygge på den gjeldende funksjonaliteten etter hvert som de legges til. Funksjoner aktiveres aldri automatisk på mindre enn ett år hvis de ikke er avgjørende.

| Funksjonsnavn | Aktiveringsdato | Funksjon lagt til | Funksjonstilstand | Modul |
| --- | --- | --- |--- |--- |
| Aktivere justering av timetransaksjon basert på endring i tildeling av finansieringsregel | 16. september 2022 | 7. oktober 2020 | Aktivert som standard | Prosjektstyring og regnskap |
| Funksjon for tilbakeføring av forskuddsfaktura for prosjektordre | 16. september 2022 | 6. oktober 2021 | Aktivert som standard | Prosjektstyring og regnskap |
| Slette fakturaforslagslinjer når Project Operations for ressursbaserte/ikke-lagerbeholdte scenarier | 16. september 2022 | 6. oktober 2021 | Aktivert som standard | Prosjektstyring og regnskap |
| Justere regnskap for en postert prosjekttransaksjon | 16. september 2022 | 10. mai 2020 | Aktivert som standard | Prosjektstyring og regnskap |
| Aktiver standard regnskapsoppsett for prosjekt | 16. september 2022 | 19. februar 2020 | Aktivert som standard | Prosjektstyring og regnskap |
| Aktiver flere kontraktlinjer for et prosjekt | 16. september 2022 | 29. juni 2020 | Aktivert som standard | Prosjektstyring og regnskap |
| Skrivebeskytte prosjekttimekladder skrivebeskyttet hvis gjeldende godkjenningsstatus ikke tillater redigering | 16. september 2022 | 6. oktober 2021 | Aktivert som standard | Prosjektstyring og regnskap |
| Aktiver synkroniseringssalgslinjer fra innkjøpslinjer når innkjøpslinjer oppdateres, og parameteren for administrasjon av endring av innkjøpsordre er aktivert | 16. september 2022 | 7. oktober 2020 | Aktivert som standard | Prosjektstyring og regnskap |
| Aktiver Project Operations i Dynamics 365 Customer Engagement | 16. september 2022 | 29. juni 2020 | Aktivert som standard | Prosjektstyring og regnskap |
| Funksjon for korrigering av prosjekttransaksjon | 16. september 2022 | 13. juli 2020 | Aktivert som standard | Prosjektstyring og regnskap |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funksjoner som blir obligatoriske i den kommende versjonen

Denne tabellen viser funksjonene som er obligatoriske fra versjon 10.0.29 og fremover.

| Funksjonsnavn | Aktiveringsdato | Funksjon lagt til | Funksjonstilstand | Modul |
| --- | --- | --- | --- | --- |
| Beregn den innlagte verdien i finansieringskilde uten å runde av valutakursen | 16. september 2022 | 14. juni 2020 | Obligatorisk | Prosjektstyring og regnskap |
| Aktiver prosjektjusteringspostering med samme finanskonto som den opprinnelige transaksjonen | 16. september 2022 | 14. juni 2020 | Obligatorisk | Prosjektstyring og regnskap |
| Detalj om beregnet beløp for prosjektkontrakt | 16. september 2022 | 31. august 2019 | Obligatorisk | Prosjektstyring og regnskap |
| Aktivere sortering etter ressurs under oppretting av prosjektfakturaforslag | 16. september 2022 | 31. august 2019 | Obligatorisk | Prosjektstyring og regnskap |
