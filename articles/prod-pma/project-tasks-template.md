---
title: Synkroniser prosjektoppgaver direkte fra Project Service Automation til økonomi og drift
description: Denne artikkelen beskriver malen og den underliggende oppgavene som brukes til å synkronisere prosjektoppgaver direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ed559fcd9e0e666f68e7d9f4f1fca91417fe4970
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028373"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synkroniser prosjektoppgaver direkte fra Project Service Automation til økonomi og drift

[!include[banner](../includes/banner.md)]

Denne artikkelen beskriver malen og den underliggende oppgavene som brukes til å synkronisere prosjektoppgaver direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.

> [!NOTE]
> - Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeoverslag, utgiftsoverslag og låsing av funksjoner er tilgjengelig i versjon 8.0.
> - Hvis du bruker Enterprise Edition 7.3.0 etter at du har installert KB-4132657 og KB-4132660, kan du bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske verdier, og til å konfigurere låsing av funksjoner. Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.
> - Integrering av faktiske data er tilgjengelig i versjon 8.0.1 eller senere.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflyt for Project Service Automation til Finance

Project Service Automation til Finance-integreringsløsningen bruker funksjonen for dataintegrering til å synkronisere data på tvers av forekomster av Project Service Automation og Finance. Integreringsmalen som er tilgjengelig med funksjonen for dataintegrering, muliggjør dataflyt om prosjektoppgaver fra Project Service Automation til Finance.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance.

[![Dataflyt for Project Service Automation-integrasjon med Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Mal og oppgave

Hvis du vil ha tilgang til malen, går du til Microsoft Power Apps og velger **Prosjekter**, og deretter velger du **Nytt prosjekt** i øverste høyre hjørne for å velge offentlige maler.

Følgende mal og underliggende oppgave brukes til å synkronisere prosjektoppgaver fra Project Service Automation til Finance:

- **Navn på malen i dataintegrering:** Prosjektoppgaver (PSA til Fin og Ops)
- **Navn på oppgaven i prosjektet:** Prosjektoppgaver

Før synkronisering av prosjektoppgaver kan forekomme, må du synkronisere prosjektkontrakter og prosjekter.

## <a name="entity-set"></a>Enhetssett

| Project Service Automation | Finans                             |
|----------------------------|-------------------------------------|
| Prosjektoppgaver              | Integreringsenhet for prosjektoppgave |

## <a name="entity-flow"></a>Enhetsflyt

Prosjektoppgaver administreres i Project Service Automation, og de synkroniseres til Finance som prosjektaktiviteter.

## <a name="prerequisites-and-mapping-setup"></a>Oppsett av forhåndskrav og tilordning

Før synkronisering av prosjektoppgaver kan forekomme, må du synkronisere prosjektkontrakter og prosjekter.

## <a name="power-query"></a>Power Query

Du må bruke Microsoft Power Query for Excel til å filtrere data hvis denne betingelsen er oppfylt:

- Du har ressursspesifikke oppføringer i en prosjektoppgave.

Hvis du må bruke Power Query, følger du disse retningslinjene:

- Malen Prosjektoppgaver (PSA til Fin og Ops) har et standardfilter som utelater ressursspesifikke oppføringer fra en prosjektoppgave ved å sette filteret på **IsLineTask** til **Usann**. Hvis du oppretter din egen mal, må du legge til dette filteret.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i dataintegrering

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordningene i dataintegrering. Tilordningen viser feltinformasjonen som blir synkronisert fra Project Service Automation til Finance.

[![Maltilordning.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]