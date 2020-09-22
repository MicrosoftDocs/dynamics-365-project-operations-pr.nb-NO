---
title: Synkronisere prosjektkontrakter og prosjekter direkte fra Project Service Automation til Finance and Operations
description: Dette emnet beskriver malen og de underliggende oppgavene som brukes til å synkronisere prosjektkontrakter og prosjekter direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 57fe4ae8-6ee9-442d-9933-d525b5415db8
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b914a56b306639253a8cd3b7caa754da175b6df2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754066"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronisere prosjektkontrakter og prosjekter direkte fra Project Service Automation til Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet beskriver malen og de underliggende oppgavene som brukes til å synkronisere prosjektkontrakter og prosjekter direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.

> [!NOTE] 
> Hvis du bruker Enterprise Edition 7.3.0, må du installere KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflyt for Project Service Automation til Finance

> [!NOTE]
> Før du kan bruke integrasjonsløsningen Project Service Automation til Finance, må du ha kjennskap til funksjonen for Dynamics 365-dataintegrasjon.

Project Service Automation til Finance-integreringsløsningen bruker funksjonen for dataintegrering til å synkronisere data på tvers av forekomster av Project Service Automation og Finance. Integreringsmalen som er tilgjengelig med funksjonen for dataintegrering, muliggjør dataflyt om prosjektkontrakter, prosjekter, prosjektkontraktlinjer og milepæler for prosjektkontraktlinjer fra Project Service Automation til Finance.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance.

[![Dataflyt for Project Service Automation-integrasjon med Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Maler og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, går du til Microsoft Power Apps og velger **Prosjekter**, og deretter velger du **Nytt prosjekt** i øverste høyre hjørne for å velge offentlige maler.

Følgende maler og underliggende oppgaver brukes til å synkronisere prosjektkontrakter og prosjekter fra Project Service Automation til Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrere med Dynamics 365 Project Service Automation v2.x
- **Navn på malen i dataintegrering:** Prosjekter og kontrakter (PSA til Fin og Ops)
- **Navn på oppgavene i prosjektet:**

    - Prosjektkontrakter PSA til Fin og Ops
    - Prosjekter PSA til Fin og Ops
    - Prosjektkontraktlinjer PSA til Fin og Ops
    - Milepæler for prosjektkontraktlinjer PSA til Fin og Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrere med Dynamics 365 Project Service Automation v3.x
Det er en skjemaendring i Project Service Automation som påvirker malen for milepæl for prosjektkontraktlinjen, og bruk av v2-versjonen av malen kreves for å integrere Project Service Automation v3.x med Dynamics 365.

- **Navn på malen i dataintegrering:** Prosjekter og kontrakter (PSA 3.x til Fin og Ops) – v2
- **Navn på oppgavene i prosjektet:**

    - Prosjektkontrakter PSA til Fin og Ops
    - Prosjekter PSA til Fin og Ops
    - Prosjektkontraktlinjer PSA til Fin og Ops
    - Milepæler for prosjektkontraktlinjer PSA til Fin og Ops

Før synkronisering av prosjektkontrakter og prosjekter kan forekomme, må du synkronisere forretningsforbindelser.

## <a name="entity-set"></a>Enhetssett

| Project Service Automation       | Finans                                                |
|----------------------------------|--------------------------------------------------------|
| Ordrer                           | Integreringsenhet for prosjektkontrakt                |
| Prosjekter                         | Integreringsenhet for prosjekt                         |
| Ordrelinjer                      | Integreringsenhet for prosjektkontraktlinje           |
| Milepæler for prosjektkontraktlinje | Integreringsenhet for milepæl for prosjektkontraktlinje |

## <a name="entity-flow"></a>Enhetsflyt

Prosjektkontrakter administreres i Project Service Automation, og de synkroniseres til Finance som prosjektkontrakter. Som en del av integreringsmalen kan du angi integreringskilden i Finance for prosjektkontrakten.

Tid og materiale-prosjekt og Fast pris-prosjekter administreres i Project Service Automation, og de synkroniseres til Finance som prosjekter. Som en del av malintegrasjonen kan du angi integreringskilden i Finance for prosjektet.

Prosjektkontraktlinjer administreres i Project Service Automation, og de synkroniseres til Finance som faktureringsregler for prosjektkontrakt. Hvis faktureringsmetoden er forskjellig fra standardprosjekttypen, oppdaterer synkroniserigen prosjekttypen for kontraktlinjeprosjektet og prosjektgruppen.

Milepæler for prosjektkontraktlinjer administreres i Project Service Automation, og de synkroniseres til Finance som milepæler for faktureringsregel for prosjektkontrakt.

## <a name="project-service-automation-to-finance-integration-solution"></a>Ingetreringsløsning for Project Service Automation til Finance

Feltet **Prosjektkontrakt-ID** er tilgjengelig på siden **Prosjektkontrakter**. Dette feltet er gjort til en naturlig og unik nøkkel for å støtte integreringen.

Når en ny prosjektkontrakt opprettes, og en **Prosjektkontrakt-ID** ikke allerede finnes, genereres den automatisk ved å bruke en nummerserie. Verdien består av **ORD** som etterfølges av en stigende nummerserie og deretter et suffiks på seks tegn. Her er et eksempel: **ORD-01022-Z4M9Q0**.

Feltet **Prosjektnummer** er tilgjengelig på siden **Prosjekter**. Dette feltet er gjort til en naturlig og unik nøkkel for å støtte integreringen.

Når et nytt prosjekt opprettes og et **Prosjektnummer** ikke allerede finnes, genereres det automatisk ved å bruke en nummerserie. Verdien består av **PRJ** som etterfølges av en stigende nummerserie og deretter et suffiks på seks tegn. Her er et eksempel: **PRJ-01049-CCNID0**.

Når integrasjonsløsningen Project Service Automation til Finance brukes, angir et oppgraderingsskript feltet **Prosjektkontrakt-ID** for eksisterende prosjektkontrakter og feltet **Prosjektnummer** for eksisterende prosjekter i Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Oppsett av forhåndskrav og tilordning

- Før synkronisering av prosjektkontrakter og prosjekter kan forekomme, må du synkronisere forretningsforbindelser.
- I tilkoblingssettet legger du til en integreringnøkkelfelttilordning for **msdyn\_organizationalunits** i **msdyn\_name \[navn\]**. Du må kanskje først legge til et prosjekt i tilkoblingssettet. Hvis du vil ha mer informasjon, kan du se [Integrere data i Common Data Service for apper](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- I tilkoblingssettet legger du til en integreringnøkkelfelttilordning for **msdyn\_projects** til **msdynce\_projectnumber \[prosjektnummer\]**. Du må kanskje først legge til et prosjekt i tilkoblingssettet. Hvis du vil ha mer informasjon, kan du se [Integrere data i Common Data Service for apper](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** for prosjektkontrakter og prosjekter kan oppdateres til en annen verdi eller fjernes fra tilordningen. Standardmalverdien er **Project Service Automation**.
- **PaymentTerms**-tilordningen må oppdateres slik at den gjenspeiler gyldige betalingsbetingelser i Finance. Du kan også fjerne tilordningen fra prosjektoppgaven. Standardverdien for tilordningen inneholder standardverdier for demonstrasjonsdata. Tabellen nedenfor viser verdiene i Project Service Automation.

    | Value | Beskrivelse   |
    |-------|---------------|
    | 1     | 30 dager netto        |
    | 2     | 2 % 10, 30 dager netto |
    | 3     | 45 dager netto        |
    | 4     | 60 dager netto        |

## <a name="power-query"></a>Power Query

Du må bruke Microsoft Power Query for Excel til å filtrere data hvis følgende betingelser er oppfylt:

- Du har salgsordrer i Dynamics 365 Sales.
- Du har flere organisasjonsenheter i Project Service Automation, og disse organisasjonsenhetene blir tilordnet til flere juridiske enheter i Finance.

Hvis du må bruke Power Query, følger du retningslinjene nedenfor:

- Malen for prosjekter og kontrakter (PSA til Fin og Ops) har et standardfilter som inkluderer bare salgsordrer av typen **Arbeidselement (msdyn\_ordertype = 192350001)**. Dette filteret hjelper deg med å garantere at prosjektkontrakter ikke blir opprettet for salgsordrer i Finance. Hvis du oppretter din egen mal, må du legge til dette filteret.
- Du må opprette et Power Query-filter som bare inkluderer kontraktorganisasjonene som skal synkroniseres med den juridiske enheten for integreringstilkoblingssettet. Eksempelvis bør prosjektkontrakter som du har med kontraktorganisasjonsenheten Contoso US, synkroniseres til den juridiske enheten USSI, mens prosjektkontrakter som du har med kontraktorganisasjonsenheten for Contoso Global, skal synkroniseres til den juridiske enheten USMF. Hvis du ikke legger til dette filteret i oppgavetilordningen, blir alle prosjektkontrakter synkronisert til den juridiske enheten som er definert for tilkoblingssettet, uavhengig av organisasjonsenheten for kontrakten.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i dataintegrering

> [!NOTE] 
> Feltene **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**og **AddressZipCode** inkluderes ikke i standardtilordningen for prosjektkontrakter. Du kan legge til tilordningene hvis du krever at disse dataene synkroniseres for prosjektkontrakter.
>
> Feltene **Beskrivelse**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** og **ProjectType** er ikke med i standardtilordningen for prosjekter. Du kan legge til tilordningene hvis du krever at disse dataene synkroniseres for prosjekter.

Illustrasjonene nedenfor viser eksempler på maloppgavetilordningene i dataintegrering. Tilordningen viser feltinformasjonen som blir synkronisert fra Project Service Automation til Finance.

[![Maltilordning](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Maltilordning](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Maltilordning](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Maltilordning](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Milepæltilordning for prosjektkontraktlinje i Prosjekter og kontrakter (PSA 3.x til Dynamics) – v2-malen:

[![Maltilordning](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
