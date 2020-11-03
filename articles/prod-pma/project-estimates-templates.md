---
title: Synkronisere prosjektestimater direkte fra Project Service Automation til Finance and Operations
description: Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere estimater for prosjekttimer og prosjektutgifter direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081748"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronisere prosjektestimater direkte fra Project Service Automation til Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere estimater for prosjekttimer og prosjektutgifter direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.

> [!NOTE]
> - Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeoverslag, utgiftsoverslag og låsing av funksjoner er tilgjengelig i versjon 8.0.
> - Integrering av faktiske data er tilgjengelig i versjon 8.0.1 eller senere.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflyt for Project Service Automation til Finance

Project Service Automation til Finance-integreringsløsningen bruker funksjonen for dataintegrering til å synkronisere data på tvers av forekomster av Project Service Automation og Finance. Integreringsmalene som er tilgjengelige med funksjonen for dataintegrering, muliggjør dataflyt om estimater for prosjekttimer og prosjektutgifter fra Project Service Automation til Finance.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance.

[![Dataflyt for Project Service Automation-integrasjon med Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Estimater for prosjekttimer

### <a name="template-and-tasks"></a>Mal og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, går du til Microsoft Power Apps og velger **Prosjekter** , og deretter velger du **Nytt prosjekt** i øverste høyre hjørne for å velge offentlige maler.

Følgende mal og underliggende oppgaver brukes til å synkronisere estimater for prosjekttime fra Project Service Automation til Finance:

- **Navn på malen i dataintegrering:** Estimater for prosjekttime (PSA til Fin og Ops)
- **Navn på oppgavene i prosjektet:**

    - Transaksjonsrelasjoner
    - Utgiftsestimater

### <a name="entity-set"></a>Enhetssett

| Project Service Automation | Finans                                       |
|----------------------------|-----------------------------------------------|
| Prosjektoppgaver              | Integreringsenhet for estimater for prosjekttime |

### <a name="entity-flow"></a>Enhetsflyt

Estimater for prosjekttime administreres i Project Service Automation, og de synkroniseres til Finance som prosjekttimeprognoser.

### <a name="prerequisites"></a>Forutsetninger

Før synkronisering av estimater for prosjekttime kan skje, må du synkronisere prosjekter, prosjektoppgaver og prosjektets utgiftstransaksjonskategorier.

### <a name="power-query"></a>Power Query

I malen for estimat av prosjekttime må du bruke Microsoft Power Query for Excel til å utføre disse oppgavene:

- Angi standard prognosemodell-ID som skal brukes når integreringen oppretter nye timeprognoser.
- Filtrer ut alle ressursspesifikke oppføringer i oppgaven som ikke kan integreres i timeprognoser.
- Filtrer ut tomme rader for transaksjonskategorier. Hvis du ikke fullfører denne oppgaven, kan det føre til feil timeprognoser.

#### <a name="set-the-default-forecast-model-id"></a>Angi standard prognosemodell-ID

Hvis du vil oppdatere standard prognosemodell-ID i malen, klikker du **Tilordne** -pilen for å åpne tilordningen. Deretter velger du koblingen **Avansert spørring og filtrering**.

- Hvis du bruker standardmalen for estimater for prosjekttime (PSA til Fin og OPS), velger du **Innsatt betingelse** i listen **Brukte trinn**. I **Funksjon** -oppføringen erstatter du **O\_prognose** med navnet på prognosemodell-ID-en som skal brukes med integrasjonen. Standardmalen har en prognosemodell-ID fra demonstrasjonsdataene.
- Hvis du oppretter en ny mal, må du legge til denne kolonnen. Velg **Legg til betinget kolonne** i Power Query, og skriv inn et navn for den nye kolonnen, for eksempel **Modell-ID**. Angi betingelsen for kolonnen, der hvis prosjektoppgaven ikke er null, så \<enter the forecast model ID\>. Ellers null.

#### <a name="filter-out-resource-specific-records"></a>Filtrere ut ressursspesifikke oppføringer

Malen Estimater for prosjekttimer (PSA til Fin og OPS) har et standardfilter som fjerner eventuelle ressursspesifikke oppføringer. Hvis du oppretter din egen mal, må du legge til dette filteret. Velg koblingen **Avansert spørring og filtrering** for å filtrere etter kolonnen **msdyn\_islinetask** , slik at bare **Usann** oppføringer tas med.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrer ut tomme rader for transaksjonskategorier.

Du må legge til et filter for å fjerne alle rader som har tomme transaksjonskategorier. Denne oppgaven er obligatorisk, uansett om du bruker standardmalen eller oppretter en egen mal. Dette filteret fjerner alle sammendragsrader fra Project Service Automation som kan føre til at timeprognoser i Finance blir feil. Velg **Avansert spørring og filtrering** -koblingen for å filtrere ut null-oppføringer i kolonnen **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Maltilordning i dataintegrering

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordningen i dataintegrering. Tilordningen viser feltinformasjonen som blir synkronisert fra Project Service Automation til Finance.

[![Tilordning av maloppgave i dataintegrering](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Prosjektets utgiftsestimater

### <a name="template-and-tasks"></a>Mal og oppgaver

Følgende mal og underliggende oppgaver brukes til å synkronisere estimater for prosjektutgifter fra Project Service Automation til Finance:

- **Navn på malen i dataintegrering:** Estimater for prosjektutgifter (PSA til Fin og Ops)
- **Navn på oppgavene i prosjektet:**

    - Transaksjonsrelasjoner 
    - Utgiftsestimater

### <a name="entity-set"></a>Enhetssett

| Project Service Automation | Finans                                                  |
|----------------------------|----------------------------------------------------------|
| Transaksjonstilkoblinger    | Integreringsenhet for prosjekttransaksjonsrelasjoner |
| Estimatlinjer             | Integreringsenhet for estimater for prosjektutgifter         |

### <a name="entity-flow"></a>Enhetsflyt

Estimater for prosjektutgifter administreres i Project Service Automation, og de synkroniseres til Finance som prognoser for prosjektutgifter.

### <a name="prerequisites"></a>Forutsetninger

Før synkronisering av estimater for prosjektutgifter kan skje, må du synkronisere prosjekter, prosjektoppgaver og prosjektets utgiftstransaksjonskategorier.

### <a name="power-query"></a>Power Query

I malen for estimat av prosjektutgifter må du bruke Power Query til å utføre disse oppgavene:

- Filter for å inkludere bare linjeposter for utgiftsestimater.
- Angi standard prognosemodell-ID som skal brukes når integreringen oppretter nye timeprognoser.
- Transformer faktureringstypene.
- Transformer transaksjonstypene.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filter for å inkludere bare linjer for utgiftsestimater.

Malen for estimater for prosjektutgifter (PSA til fin og OPS) har et standardfilter som bare inkluderer utgiftslinjer i integrasjonen. Hvis du oppretter din egen mal, må du legge til dette filteret. Velg oppgaven **Transaksjonsrelasjoner** , og klikk deretter **Tilordne** -pilen for å åpne tilordningen. Velg koblingen **Avansert spørring og filtrering**. Filtrer kolonnen **msdyn\_transactiontype1** , slik at den bare inkluderer **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Angi standard prognosemodell-ID

Hvis du vil oppdatere standard prognosemodell-ID i malen, velger du oppgaven **Utgiftsestimater** , og deretter klikker du **Tilordne** -pilen for å åpne tilordningen. Velg koblingen **Avansert spørring og filtrering**.

- Hvis du bruker standardmalen for estimater for prosjektutgifter (PSA til Fin og OPS) i Power Query, velger du først **Innsatt betingelse** fra delen **Brukte trinn**. I **Funksjon** -oppføringen erstatter du **O\_prognose** med navnet på prognosemodell-ID-en som skal brukes med integrasjonen. Standardmalen har en prognosemodell-ID fra demonstrasjonsdataene.
- Hvis du oppretter en ny mal, må du legge til denne kolonnen. Velg **Legg til betinget kolonne** i Power Query, og skriv inn et navn for den nye kolonnen, for eksempel **Modell-ID**. Angi betingelsen for kolonnen, der hvis ID-en for estimatlinjen ikke er null, så \<enter the forecast model ID\>. Ellers null.

#### <a name="transform-the-billing-types"></a>Transformer faktureringstypene

Malen for estimater for prosjektutgifter (PSA til Fin og OPS) inkluderer en betinget kolonne som brukes til å transformere faktureringstypene som er mottatt fra Project Service Automation under integreringen. Hvis du oppretter din egen mal, må du legge til denne betinget-kolonnen. Velg **Avanserte spørring og filtrering** -koblingen, og velg deretter **Legg til betinget kolonne**. Angi et navn for den nye kolonnen, for eksempel **Faktureringstype**. Skriv deretter inn følgende betingelse:

Hvis **msdyn\_billingtype** = 192350000, er den **Ikke-belastbar**  
Hvis **msdyn\_billingtype** = 192350001, er den **Belastbar**  
Hvis **msdyn\_billingtype** = 192350002, er den **Komplementær**  
Hvis ikke **Ikke tilgjengelig**

#### <a name="transform-the-transaction-types"></a>Transformer transaksjonstypene

Malen for estimater for prosjektutgifter (PSA til Fin og OPS) inkluderer en betinget kolonne som brukes til å transformere transaksjonstypene som er mottatt fra Project Service Automation under integreringen. Hvis du oppretter din egen mal, må du legge til denne betinget-kolonnen. Velg **Avanserte spørring og filtrering** -koblingen, og velg deretter **Legg til betinget kolonne**. Angi et navn for den nye kolonnen, for eksempel **Transaksjonstype**. Skriv deretter inn følgende betingelse:

Hvis **msdyn\_transactiontypecode** = 192350000, er det **Kostnad**  
Hvis **msdyn\_transactiontypecode** = 192350005, er det **Salg**  
Hvis ikke er det **Null**

### <a name="template-mapping-in-data-integration"></a>Maltilordning i dataintegrering

Illustrasjonene nedenfor viser eksempler på maloppgavetilordningene i dataintegrering. Tilordningen viser feltinformasjonen som blir synkronisert fra Project Service Automation til Finance.

[![Maltilordning for utgiftsestimattransaksjoner](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Maltilordning for utgiftsestimater](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
