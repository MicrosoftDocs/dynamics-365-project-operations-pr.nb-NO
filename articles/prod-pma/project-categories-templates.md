---
title: Synkronisere prosjektutgiftskategorier mellom Finance and Operations og Project Service Automation
description: Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjektutgiftskategorier mellom Microsoft Dynamics 365 Finance og Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999863"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synkronisere prosjektutgiftskategorier mellom Finance and Operations og Project Service Automation

[!include[banner](../includes/banner.md)]

Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjektutgiftskategorier mellom Dynamics 365 Finance og Dynamics 365 Project Service Automation.

> [!NOTE]
> - Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeoverslag, utgiftsoverslag og låsing av funksjoner er tilgjengelig i versjon 8.0.
> - Integrering av faktiske data er tilgjengelig i versjon 8.0.1 eller senere.
> - Hvis du bruker Enterprise Edition 7.3.0 etter at du har installert KB-4132657 og KB-4132660, kan du bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske verdier, og til å konfigurere låsing av funksjoner. Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Dataflyt for Project Service Automation og Finance

Project Service Automation og Finance-integreringsløsningen bruker funksjonen for dataintegrering til å synkronisere data på tvers av forekomster av Project Service Automation og Finance. Integreringsmalene som er tilgjengelige med funksjonen for dataintegrering, muliggjør dataflyt om prosjektets utgiftstransaksjonskategorier mellom Finance og Project Service Automation.

Hvis prosjektutgiftskategoriene håndteres i Finance, er integreringsflyten først fra Finance til Project Service Automation. Integrerings-IDene for prosjektutgiftskategoriene oppdateres deretter via synkronisering fra Project Service Automation til Finance.

Hvis prosjektutgiftskategoriene håndteres i Project Service Automation, er integreringsflyten først fra Project Service Automation til Finance. Prosjektkategoriene må allerede være konfigurert i Finance før synkronisering fra Project Service Automation. Deretter synkroniserer du fra Finance tilbake til Project Service Automation, og deretter fra Project Service Automation til Finance igjen. På denne måten bidrar du til å sikre at kategoriene er koblet, og at det ikke opprettes noen duplikater.

> [!NOTE]
> Vanligvis er prosjektutgiftskategoriene behandlet i Finance. Hvis de ikke er det, eller hvis det allerede er opprettet utgiftskategorier i Project Service Automation, må du først synkronisere ved hjelp av malen for kategorier for prosjektets utgiftstransaksjoner (PSA til Fin og Ops). Deretter synkroniserer du ved å bruke malen for kategorier for prosjektets utgiftstransaksjoner (Fin og Ops til PSA). Du bør deretter kjøre synkronisering fra Project Service Automation til Finance én gang til.
>
> Hvis du først synkroniserer fra Project Service Automation, må følgende krav oppfylles i Finance før synkroniseringen blir kjørt:
>
> - Den delte kategorien som samsvarer med prosjektkategorien som er angitt i Project Service Automation, må finnes, og den må være aktivert for både **Prosjekt** og **Utgift**.
> - For hver juridiske enhet som må integreres med, må følgende prosjektkategorier finnes:
>
>     - **Prosjektkategori** finnes. 
>     - **Bruk i Utgift** er aktivert.
>     - **Aktiv i journal** er aktivert.
>     - **Transaksjonstype** er satt til **Utgift**.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance.

[![Dataflyt for Project Service Automation-integrasjon med Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Synkronisering av prosjektets utgiftskategorier fra Finance til Project Service Automation

### <a name="template-and-task"></a>Mal og oppgave

Hvis du vil ha tilgang til malen, går du til Microsoft Power Apps og velger **Prosjekter**, og deretter velger du **Nytt prosjekt** i øverste høyre hjørne for å velge offentlige maler.

Følgende mal og underliggende oppgave brukes til å synkronisere kategorier for prosjektutgifter fra Finance til Project Service Automation:

- **Navn på malen i dataintegrering:** Kategorier for prosjektets utgiftstransaksjoner (Fin og Ops til PSA)
- **Navn på oppgaven i prosjektet:** Synkroniser kategorier til PSA

### <a name="entity-set"></a>Enhetssett

| Finans                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Integreringsenhet for kategorier | Transaksjonskategorier     |

### <a name="entity-flow"></a>Enhetsflyt

Kategorier for prosjektutgifter administreres i Finance, og de synkroniseres til Project Service Automation som transaksjonskategorier.

### <a name="power-query"></a>Power Query

Når du synkroniserer med Project Service Automation, må du bruke Microsoft Power Query for Excel for å angi faktureringstype i transaksjonskategorien. Malen Kategorier for prosjektets utgiftstransaksjoner (Fin og Ops til PSA) har en standardkolonne og tilordning. Hvis du oppretter din egen mal, må du legge til en betinget-kolonnen i Power Query. Følg denne fremgangsmåten.

1. Klikk pilen for å åpne tilordningen for oppgaven for prosjektets utgiftskategori i malen Kategorier for prosjektets utgiftstransaksjoner (Fin og Ops til PSA).
2. Klikk **Avansert spørring og filtrering** for å åpne Power Query.
2. Velg **Legg til betinget kolonne**.
3. Angi et navn for den nye kolonnen, for eksempel **Faktureringstype**.
4. Angi følgende betingelse: **hvis KATEGORIID ikke er lik null, så 19235001, ellers null**.
5. Klikk **OK** i kolonnen.
6. Pass på at du tilordner den nye kolonnen på tilordningssiden.

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordningen i dataintegrering. Tilordningen viser feltinformasjonen som blir synkronisert fra Finance til Project Service Automation.

[![Tilordning av prosjektets utgiftskategorier til Project Service Automation-malen](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Synkronisering av prosjektets utgiftskategorier fra Project Service Automation til Finance

### <a name="template-and-task"></a>Mal og oppgave

Følgende mal og underliggende oppgave brukes til å synkronisere kategorier for prosjektutgifter fra Project Service Automation til Finance:

- **Navn på malen i dataintegrering:** Kategorier for prosjektets utgiftstransaksjoner (PSA til Fin og Ops)
- **Navn på oppgaven i prosjektet:** Synkroniser kategorier til Fin Ops

### <a name="entity-set"></a>Enhetssett

| Project Service Automation | Finans                           |
|----------------------------|-----------------------------------|
| Transaksjonskategorier     | Integreringsenhet for kategorier |

### <a name="entity-flow"></a>Enhetsflyt

Kategorier for prosjektutgifter administreres i Finance, og de synkroniseres til Project Service Automation som transaksjonskategorier. Synkroniseringen tilbake til Finance oppdaterer prosjektkategorien i Finance med integrasjons-IDen fra Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Maltilordning i dataintegrering

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordningen i dataintegrering.

> [!NOTE]
> Tilordningen viser feltinformasjonen som blir synkronisert fra Project Service Automation til Finance.

[![Tilordning av mal for Project Service Automation til Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]