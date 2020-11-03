---
title: Sikkerhetsmodellen
description: Dette emnet gir information om sikkerhetsmodellen i Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e875d1765b5038e60830d626abb5bcd61749ece1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081505"
---
# <a name="security-model"></a>Sikkerhetsmodell

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Microsoft Dynamics 365 Project Operations inneholder en unik sikkerhetsmodell som gjør det mulig med en rollebasert sikkerhetsmodell for bedrifter som samarbeider med Microsoft Office-grupper. 


## <a name="security-roles"></a>Sikkerhetsroller
Frontfunksjonene i Project Operations inkluderer følgende roller:

| Rolle                          | Beskrivelse                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Practice Manager              | Støtter rapportering på tvers av prosjekter.                                                                                                            | Forretningsenhet              |
| Prosjektgodkjenner              | Godkjenner tid og utgifter mot et prosjekt.                                                                                                                              | Forretningsenhet |
| Faktureringsadministrator for prosjekt | Oppretter fakturaforslaget.                                                                                                                                                 | Forretningsenhet |
| Prosjektleder               | Oppretter prosjektplanen og ber om ressurser.                                                                                                                              | Forretningsenhet |
| Prosjektressurs              | Teammedlemmer som kan bli bestilt og rapportere tid.                                                                                                          | Forretningsenhet|
| Resource Manager              | Alle funksjoner for ressursbehandlings, for eksempel fullføring av ressursforespørsler og bestillinger, er atskilt for å støtte for en hybrid konfigurasjon av Project Manager + Resource Manager og en enkelt og sentralisert Resource Manager-rolle. | Forretningsenhet |


Microsoft Project for Internett inkluderer følgende roller:

| Rolle           | Beskrivelse                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Prosjektbruker   | Samarbeidsbruker i prosjektet som kan opprette sine egne prosjekter og vise alle prosjekter som er delt med dem. | User   |
| Prosjektsystem | Rolle brukt til programkontekst. Kunder bør ikke bruke denne systemrollen.                                    | Global |

## <a name="security-enforcement"></a>Sikkerhetshåndhevelse
Handlinger som utføres på prosjektnivå, utføres i konteksten til brukeren som er logget på. Dette betyr at brukeren må ha tilgang til CDS for å opprette, åpne eller slette et prosjekt. Tilgang i CDS kan gis gjennom enhver av de mulige mekanismene som er inkludert i plattformen. En bruker med et større omfang kan for eksempel få tilgang til prosjektet, eller hvis en eksplisitt handling for prosjektdeling er utført som gir brukeren tilgang.

Det er viktig å vurdere dette når du oppretter prosjekter i Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Moderne gruppesamarbeid med Project Operations
Project for Internett og Project Operations støtter moderne grupper for samarbeid. Brukere som legges til i prosjektet via en gruppe, kan redigere prosjektplanen.

Project for Internett legger til brukere i gruppen automatisk ved tilordning.

Med grupper er det mulig med samarbeid for tillatelsene i prosjektet og støttende samarbeidsartefakter. Diagrammet nedenfor viser hendelsene og tilstandsendringene som skjer under gruppetilordningsprosessen.

Project Operations oppretter ikke en gruppe gjennom implisitt handling. Dette skjer bare gjennom den eksplisitte handlingen ved å trykke grupper.

Søk etter gruppemedlemmer i dialogboksen **Gruppebehandling** er begrenset til de som er angitt som en del av miljøets sikkerhetsgruppe. Hvis du vil ha mer informasjon, kan du se [Styre brukertilgangen til miljøer: sikkerhetsgrupper og lisenser](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Gruppemodus](./media/groupsmode.png)

1. Prosjektet opprettes og eies av brukeren som opprettet det.
2. Prosjekteieren oppdateres til teamet.
3. Eierteamet tilordnes til den angitte eller opprettede Office-gruppen.
4. Den opprinnelige eieren av prosjektet blir lagt til i Office-gruppen.

## <a name="deployment-recommendation"></a>Anbefalinger for distribusjon
Etter hvert som samarbeidsmodellen med Office-grupper utvikler seg, blir det lagt til funksjonalitet for å gi mer detaljert kontroll over tid. Kunder som distribuerer Project Operations i dag, oppfordres til å fokusere på en tradisjonell Microsoft Dynamics 365-sikkerhetsmodell.

Hvis du vil ha mer informasjon, kan du se [Sikkerhet i Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Sikkerhet for Project Operations og Microsoft Dynamics 365 Finance
Project Operations inkluderer følgende roller:

- Prosjektleder
- Prosjektregnskapsfører

Hvis du vil ha mer informasjon om sikkerhet i Finance, kan du se [Rollebasert sikkerhet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


