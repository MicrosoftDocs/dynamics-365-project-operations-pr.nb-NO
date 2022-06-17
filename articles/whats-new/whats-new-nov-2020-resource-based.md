---
title: Nyheter november 2020 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra november 2020.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b98c968a040c14f4d11c350885e2cbb984596c48
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923430"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter november 2020 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Denne artikkelen gjelder følgende komponenter og versjoner av Dynamics 365 Project Operations:

- Project Operations på CDS-miljø versjon 4.4.0.70
- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Oppdateringer til Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

### <a name="project-operations-on-cds"></a>Project Operations på CDS

| Funksjonsområdet                 | Referansenummer | Kvalitetsoppdatering                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Administrasjon av salgsmuligheter       | 2036993          | Estimatlinje og kontraktlinjer for ressurstilordning oppdateres på vinnende tilbud når tilbudslinjetypen er **Alle oppgaver**.                                                 |
| Fakturering og prising          | 2070392          | Prosjektkontraktlinjer på fakturaen øker hver gang **Oppdater fakturatransaksjoner** velges.                                                                         |
| Prosjektplanlegging             | 2043336          | Kan ikke slette en oppføring for prosjektteammedlem.                                                                                                                                  |
| Prosjektplanlegging             | 2046013          | Inkonsekvent virkemåte for estimatmerkers kolonner under lasting i forhold til endring av tidsfasetype.                                                                                   |
| Prosjektplanlegging             | 2046647          | Start- og sluttidspunktene avviker med en time når ressurskrav blir generert fra prosjektgruppemedlemmer.                                                                      |
| Prosjektplanlegging             | 2053879          | (I henhold til de forestående CDS-fasene) PublishUnassignedAssignments bryter et forsøk på å lagre en oppgave ved feilen om at verdien som er sent til ConditionOperator.In, er tom.                       |
| Prosjektplanlegging             | 2055501          | Hvis du lar **Prosjektets startdato** stå tom, fører det til en feil i tidsplanen.                                                                                                      |
| Prosjektplanlegging             | 2066817          | Kan ikke opprette en generisk ressurs ved hjelp av personvelgeren i kategorien **Oppgaver**.                                                                                                   |
| Prosjektplanlegging             | 2067034          | Knappen **Vis detaljer** er ikke tilgjengelig på siden **Detaljer for oppgave**.                                                                                                       |
| Ressursstyring          | 2046667          | Generiske teammedlemmer slettes ikke selv etter at alle ressurser er fullført.                                                                                                    |
| Hurtigregistrering av tid og utgifter | 2047499          | **Ny**-knappen på siden Tidsoppføring åpner siden **Ny e-postsignatur**.                                                                                               |
| Hurtigregistrering av tid og utgifter | 2059859          | Uventet popup-vindu åpnes når du oppretter en utgiftsoppføring.                                                                                                                         |
| Andre                        | 2044181          | (Avinstallerer bestilling) Under forsøk på å avinstallere msdyn_ProjectServiceCore_Patch og msdyn for Project Service-kjerneløsninger vises feilmelding om at "oppføringen ikke er tilgjengelig".  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

| Funksjonsområdet        | Referansenummer | Kvalitetsoppdatering                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inntektsføring | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Den estimerte fullføringsprosenten for prosjektet er feil når kontrakten bruker en fremmed valuta og prosenten for fullført arbeid for den ferdige metoden.                     |
| Inntektsføring | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Kan ikke postere estimater med fullføringsmetoden for **Faktisk kostnad**.                                                                                                    |
| Inntektsføring | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Eliminering mislykkes på grunn av en feil ved utbalansering av bilag når firmavalutaen og transaksjonsvalutaen er forskjellig.                                              |
| Utgiftshåndtering  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | For brukere som ikke er administrator, vises ikke oppslagsverdiene for utgiftslinjekolonner som **Prosjekt-ID** og **Utgiftskategori** på riktig måte i datakontaktrammen. |
| Utgiftshåndtering  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Linjeegenskapsstandard vises ikke for utgiftskategorier.                                                                                                         |
| Utgiftshåndtering  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Utgiftsintegrering må inkludere linjeegenskapen fra utgiftsrapporten.                                                                                             |
| Fakturering           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Kan ikke bokføre prosjektfakturaforslag på grunn av en feilmelding som sier at kombinasjonen av FD ikke ble validert.                                                    |
| Fakturering           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Kan ikke vise transaksjoner fra detaljsiden for **faktura**.                                                                                                              |
| Fakturering           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Fakturaforslagslinjer kan slettes.                                                                                                                                  |
| Prosjektregnskap  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | **Prognose**-menyelementer vises ikke på listesiden **Prosjekter**.                                                                                                   |
| Prosjektregnskap  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Kan ikke åpne **Prosjektoppgave**   > **Transaksjoner og prognose**.                                                                                                       |
| Prosjektregnskap  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Justering av regnskap** er ikke aktivert for fakturerte prosjekttransaksjoner.                                                                                                  |
| Prosjektregnskap  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Regnskapsdetaljer er ikke inkludert i **ProjCDSActualsImport**-tabellen når **Interering**-journalen er postert.                                                  |
| Prosjektregnskap  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Oppføringen for prosjektprognose dobles når du fjerner og deretter legger til en ressurstilordning på nytt.                                                                            |
| Prosjektregnskap  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Hvis du velger en prosjekt-ID-kobling, åpnes ikke URL-adressen for CDS-dypkobling.                                                                                                         |
| Prosjektregnskap  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Kan ikke oppdatere startdatoen for en oppgave i CDS.                                                                                                                           |
| Prosjektregnskap  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Hvis du aktiverer funksjonen, er det ikke mulig å finne flere kontraktlinjer uten CDS-integrering.                                                                                   |

### <a name="regulatory-updates"></a>Forskriftsmessige oppdateringer
Hvis du vil ha informasjon om forskriftsmessige oppdateringer for økonomi- og driftsapper, kan du se [Forskriftsmessige oppdateringer](/dynamics365/finance/localizations/regulatory-updates). Du kan også logge på LCS og vise de planlagte forskriftsmessige oppdateringene ved hjelp av verktøyet for problemsøk. Problemsøk lar deg søke etter land, type funksjon og utgave.


[!INCLUDE[footer-include](../includes/footer-banner.md)]