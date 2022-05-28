---
title: Økonomiske estimater for utgifter på prosjekter
description: Dette emnet gir informasjon om hvordan du definerer eller beregner prosjektrelaterte utgifter.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c14dc31d666d0e0d026cf9cddfa1e78dee40f717
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589485"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Økonomiske estimater for utgifter på prosjekter
_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations gjør det mulig for prosjektledere å definere prosjektbaserte utgifter for hvert prosjekt eller hver oppgave. Hvert utgiftselement kan knyttes til en bestemt prosjektoppgave. Utgifter kategoriseres i ulike utgiftskategorier, som defineres på organisasjonsnivå. Priser og kostnader for hver utgiftskategori defineres i prislisten. 

Fullfør fremgangsmåten nedenfor for å vise, legge til eller slette en prosjektutgift.

1. Gå til **Prosjekter**, og velg prosjektet du vil arbeide med.
2. Velg kategorien **Prosjektestimater**, og vis listen over prosjektutgifter.
3. Velg **Ny utgift** for å legge til en utgift. Du kan også velge en utgift som skal slettes, og deretter velge **Slett utgift**.

Tabellen nedenfor inneholder informasjon om feltene på **kostnadsestimatlinjen** for et prosjekt. 

| **Felt** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- |
| Oppgave | En liste over oppgavene i prosjektet. Dette inkluderer sammendrags- og bladnodeoppgaver. | Hvis du velger en oppgave for en kostnadsestimatlinje, vil dette påvirke den beregnede utgiftskostnaden og beregnet utgiftssalg for en oppgave. Hvis dette feltet står tomt, spores kostnadsestimatet og oppsummeres bare på prosjektnivå. |
| Kategori | En liste over transaksjonskategorier som har koblede utgiftskategorier i programmet. | Hvis du velger en kategori, blir prisene og kostnadene dyrere på estimatlinjen for utgifter. |
| Startdato | Prognosedatoen for utgiften. | Dette feltet har ingen nedstrøms påvirkning. |
| Enhetsgruppe | Standardverdien i dette feltet kommer fra enhetsgruppen som er angitt som standard i den valgte kategorien. Du kan oppdatere dette feltet for å velge en annen enhetsgruppe. | Dette feltet har ingen nedstrøms påvirkning. |
| Enhet | Verdien i dette feltet er standardenheten for den valgte kategorien. Du kan oppdatere dette feltet for å velge en annen enhet. | Endring av enheten fører til en annen standard enhetspris og -kostnad. |
| Antall | Beløpet for den beregnede utgiften du vil pådra deg. | Dette feltet har ingen nedstrøms påvirkning. |
| Enhetskost | Kostnaden for den valgte kategorien og enhetskombinasjonen som angitt i den aktuelle kostnadsprislisten | Enhetskostnaden vises alltid i kostnadsvalutaen for prosjektet. |
| Enhetspris | Prisen for den valgte kategorien og enhetskombinasjonen som satt opp i den aktuelle salgsprislisten. | Enhetsprisen vises alltid i salgsvalutaen for prosjektet. |
| Totale kostnader | Kostnadsbeløpet som beregnes som antall \* enhetskostnad.| Kostnadsbeløpet vises alltid i kostnadsvalutaen for prosjektet. |
| Totalt salg | Salgsbeløpet som beregnes som antall \* enhetspris. | Salgsbeløpet vises alltid i salgsvalutaen for prosjektet. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
