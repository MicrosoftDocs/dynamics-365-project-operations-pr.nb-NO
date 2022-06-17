---
title: Nyheter september 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra september 2021.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c7f764b3e8ee3775167ee57b4f034e383899aea3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923384"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter september 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

*Gjelder: Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer*

Denne artikkelen gjelder følgende komponenter og versjoner av Dynamics 365 Project Operations:

   - Project Operations i Microsoft Dataverse-miljø, versjon 4.14.0.99.
   - Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Det finnes ingen oppdateringer for tilordninger av dobbel skriving i Project Operations i denne versjonen. Hvis du vil ha en gjeldende liste og versjoner av tilordninger for dobbel skriving i Project Operations, kan du se [Tilordningsversjoner av dobbel skriving for Project Operations](../environment/resource-dual-write-maps.md).

Kjør alltid den nyeste versjonen av kartet i miljøet, og aktiver alle relaterte tabellkart når du oppdaterer Project Operations Dataverse-løsningen og Finance-løsningsversjonen. Enkelte funksjoner fungerer kanskje ikke på riktig måte hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen på siden **Dobbel skriving** i kolonnen **Versjon**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en medfølgende tabelltilordning, må du bruke endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem med å starte kartet, følger du instruksjonene i delen [Problemer med manglende tabellkolonner i tilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funksjonsområdet** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| Tid og utgifter | 1811407 | Justerte sikkerhetsrollen for prosjektgodkjenner for godkjenning av utgiftsregistrering. |
| Tid og utgifter | 1811438 | Justerte sikkerhetsrollen for prosjektgodkjenner for annullering av tidsoppføringsgodkjenning. |
| Tid og utgifter | 2370126 | Oppdaterte ikonene **Prosjektoppgave** og **Rolle** i enheten **Tidsoppføring**. |
| Tid og utgifter | 2379879 | Korrigerte **Kopier uke**-funksjonen i tidsoppføringen ved bruk av Dynamics 365 for telefon. |
| Fakturering og prising | 2371906 | Totalbeløpet for proformafaktura kan ikke være justerbar i Project Operations for ressursbaserte distribusjoner. |
| Fakturering og prising | 2385802 | Rettet feilen som oppstår med negative faktiske timer når prosjekttotaler oppdateres. |
| Fakturering og prising | 2389675 | Forbedret virkemåte for bekreftelse av proformafaktura. Enheten for langvarige jobber må ta hensyn til aktiviteten som kreves for å skrive bekreftelsesresultater for regnskap. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Reise og utgift | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Beløpene på leverandør- og salgsavgiftstransaksjoner som posteres fra en utgift som ble opprettet fra en kredittkorttransaksjon, er feil. |
| Reise og utgift | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Feil linjer for innbetaling opprettes når betalingskladden genereres. |
| Reise og utgift | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Beløpene på salgsavgiftstransaksjoner som posteres fra en utgift som ble opprettet fra en kredittkorttransaksjon, er feil. |
| Reise og utgift | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Det kan ta lang tid å slette en utgiftslinje. |
| Prosjektregnskap | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Når du har brukt KB 4619395, støttes ikke endring av nummersekvensen til **Kontinuerlig**, og når du legger inn et estimat, oppstår følgende feil: Systemet støtter ikke konfigurasjon av kontinuerlig for nummersekvensen Proj_X. |
| Prosjektregnskap | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Det kan hende at innlegging av en leverandørfaktura mislykkes med følgende feilmelding: «Transaksjonene på leverandørfakturaen balanserer ikke per 17.05.2021. (regnskapsvaluta: 0,00 – rapporteringsvaluta: 0,01)». |
