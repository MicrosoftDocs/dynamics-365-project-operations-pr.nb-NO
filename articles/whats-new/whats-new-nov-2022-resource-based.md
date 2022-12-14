---
title: Nyheter november 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Microsoft Dynamics 365 Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra november 2022.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831098"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter november 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.58.0.119
- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Det finnes ingen oppdateringer for tilordninger av dobbel skriving i Project Operations i denne versjonen. Hvis du vil ha en gjeldende liste og versjoner av tilordninger for dobbel skriving i Project Operations, kan du se [Tilordningsversjoner av dobbel skriving for Project Operations](../environment/resource-dual-write-maps.md).

Kjør alltid den nyeste versjonen av kartet i miljøet, og aktiver alle relaterte tabellkart når du oppdaterer Project Operations Dataverse-løsningen og Finance-løsningsversjonen. Enkelte funksjoner fungerer kanskje ikke riktig hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en bruksklar tabelltilordning, bruker du endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem når du starter tilordningen, følger du instruksjonene i delen [Problemer med manglende tabellkolonner i tilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Fakturering og prising | 2781818 | Feilmelding om nøkkel som ikke finnes, ved opprettelse av standardpris for logg over materialbruk. |
| Fakturering og prising | 2922373 | Kan ikke koble tilbudslinje til prosjekt som er lukket som tapt tilbud. |
| Fakturering og prising | 2943206 | **Kontraktlinje**-feltet i prosjektenheten skal være valgfritt. |
| Fakturering og prising | 2953182 | Feilmeldingen for korrigeringsfakturaer er forbedret.|
| Fakturering og prising | 2959500 | Kan ikke koble tilbudslinje til en prosjektoppgave som allerede er knyttet til et tapt tilbud.|
| Fakturering og prising | 2959560 | Meldingen «Denne kunden finnes allerede i prosjektkontrakten» ble mottatt ved lukking av tilbud som vunnet i bestemte nasjonale innstillinger. |
| Fakturering og prising | 3031727 | Ressurstilordninger mislykkes med feilmeldingen «Det obligatoriske feltet msdyn_Company mangler». |
| Fakturering og prising | 3036905 | Eiende firma initialiseres aldri ved ProjectTeamMember. |
| Administrasjon av salgsmulighet | 2763519 | Nullreferansefeil i EnsureProjectContractAllowsUpdates. |
| Administrasjon av salgsmulighet | 2783798 | Når du importerer prosjektestimater på en tilbudslinje, mangler oppgavebeskrivelser for utgifts- og materialestimater.|
| Administrasjon av salgsmulighet | 2988635 | Beskrivelsen av feilmeldingen ved sletting av kunde i tilbud er forbedret. |
| Administrasjon av salgsmulighet | 3001191 | Kan ikke opprette tilbud fra salgsmulighet der faktureringsmetoden er angitt som null. |
| Oppgradering | 3012324 | Prosjektkonvertering mislyktes i et prosjekt med kontrolltegn som Tab i navnet. || Prosjektplanlegging og sporing | 2790384 | Tidsavbruddet for ventende OperationSet er for kort. |
| Prosjektplanlegging og sporing | 3044275 | Manglende lokalisering for følgende: missingProjectSchedulerErrorMessage. |
| Prosjektplanlegging og sporing | 3044277 | Rutenettet for Project Recon lastes ikke inn når planleggeren oppheves.|
| Ressursbehandling | 2943153 | Sporing-fanen er oppdatert for å vise to desimalplasser for varighet.|
| Utsetting | 2932774 | Skrivebeskyttet leverandørfakturalinje viser ikke feil på riktig måte. |
| Utsetting | 2939556 | Status for leverandørfakturahode skal ikke settes til Utkast ved sletting av linje hvis den ikke er aktiv. |
| Tid og utgift | 2939998 | Ta i bruk TESA-versjon i ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Oversikt over prosjektstyring og regnskap i Finans

Hvis du vil ha informasjon om feilrettinger som er inkludert i denne oppdateringen, logger du deg på Microsoft Dynamics Lifecycle Services og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
