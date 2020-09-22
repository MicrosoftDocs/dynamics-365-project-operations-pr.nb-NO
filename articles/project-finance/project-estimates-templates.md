---
title: Synkronisere prosjektestimater direkte fra Project Service Automation til Finance and Operations
description: Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere estimater for prosjekttimer og prosjektutgifter direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: KimANelson
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
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754104"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="7b360-103">Synkronisere prosjektestimater direkte fra Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7b360-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7b360-104">Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere estimater for prosjekttimer og prosjektutgifter direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7b360-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="7b360-105">Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeoverslag, utgiftsoverslag og låsing av funksjoner er tilgjengelig i versjon 8.0.</span><span class="sxs-lookup"><span data-stu-id="7b360-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="7b360-106">Integrering av faktiske data er tilgjengelig i versjon 8.0.1 eller senere.</span><span class="sxs-lookup"><span data-stu-id="7b360-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="7b360-107">Dataflyt for Project Service Automation til Finance</span><span class="sxs-lookup"><span data-stu-id="7b360-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="7b360-108">Project Service Automation til Finance-integreringsløsningen bruker funksjonen for dataintegrering til å synkronisere data på tvers av forekomster av Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="7b360-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="7b360-109">Integreringsmalene som er tilgjengelige med funksjonen for dataintegrering, muliggjør dataflyt om estimater for prosjekttimer og prosjektutgifter fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="7b360-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7b360-110">Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="7b360-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="7b360-111">[![Dataflyt for Project Service Automation-integrasjon med Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="7b360-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="7b360-112">Estimater for prosjekttimer</span><span class="sxs-lookup"><span data-stu-id="7b360-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="7b360-113">Mal og oppgaver</span><span class="sxs-lookup"><span data-stu-id="7b360-113">Template and tasks</span></span>

<span data-ttu-id="7b360-114">Hvis du vil ha tilgang til de tilgjengelige malene, går du til Microsoft Power Apps og velger **Prosjekter**, og deretter velger du **Nytt prosjekt** i øverste høyre hjørne for å velge offentlige maler.</span><span class="sxs-lookup"><span data-stu-id="7b360-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="7b360-115">Følgende mal og underliggende oppgaver brukes til å synkronisere estimater for prosjekttime fra Project Service Automation til Finance:</span><span class="sxs-lookup"><span data-stu-id="7b360-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="7b360-116">**Navn på malen i dataintegrering:** Estimater for prosjekttime (PSA til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="7b360-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="7b360-117">**Navn på oppgavene i prosjektet:**</span><span class="sxs-lookup"><span data-stu-id="7b360-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="7b360-118">Transaksjonsrelasjoner</span><span class="sxs-lookup"><span data-stu-id="7b360-118">Transaction relationships</span></span>
    - <span data-ttu-id="7b360-119">Utgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="7b360-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="7b360-120">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="7b360-120">Entity set</span></span>

| <span data-ttu-id="7b360-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7b360-121">Project Service Automation</span></span> | <span data-ttu-id="7b360-122">Finans</span><span class="sxs-lookup"><span data-stu-id="7b360-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="7b360-123">Prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="7b360-123">Project tasks</span></span>              | <span data-ttu-id="7b360-124">Integreringsenhet for estimater for prosjekttime</span><span class="sxs-lookup"><span data-stu-id="7b360-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="7b360-125">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="7b360-125">Entity flow</span></span>

<span data-ttu-id="7b360-126">Estimater for prosjekttime administreres i Project Service Automation, og de synkroniseres til Finance som prosjekttimeprognoser.</span><span class="sxs-lookup"><span data-stu-id="7b360-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7b360-127">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="7b360-127">Prerequisites</span></span>

<span data-ttu-id="7b360-128">Før synkronisering av estimater for prosjekttime kan skje, må du synkronisere prosjekter, prosjektoppgaver og prosjektets utgiftstransaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="7b360-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="7b360-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="7b360-129">Power Query</span></span>

<span data-ttu-id="7b360-130">I malen for estimat av prosjekttime må du bruke Microsoft Power Query for Excel til å utføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="7b360-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="7b360-131">Angi standard prognosemodell-ID som skal brukes når integreringen oppretter nye timeprognoser.</span><span class="sxs-lookup"><span data-stu-id="7b360-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="7b360-132">Filtrer ut alle ressursspesifikke oppføringer i oppgaven som ikke kan integreres i timeprognoser.</span><span class="sxs-lookup"><span data-stu-id="7b360-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="7b360-133">Filtrer ut tomme rader for transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="7b360-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="7b360-134">Hvis du ikke fullfører denne oppgaven, kan det føre til feil timeprognoser.</span><span class="sxs-lookup"><span data-stu-id="7b360-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="7b360-135">Angi standard prognosemodell-ID</span><span class="sxs-lookup"><span data-stu-id="7b360-135">Set the default forecast model ID</span></span>

<span data-ttu-id="7b360-136">Hvis du vil oppdatere standard prognosemodell-ID i malen, klikker du **Tilordne**-pilen for å åpne tilordningen.</span><span class="sxs-lookup"><span data-stu-id="7b360-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7b360-137">Deretter velger du koblingen **Avansert spørring og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="7b360-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="7b360-138">Hvis du bruker standardmalen for estimater for prosjekttime (PSA til Fin og OPS), velger du **Innsatt betingelse** i listen **Brukte trinn**.</span><span class="sxs-lookup"><span data-stu-id="7b360-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="7b360-139">I **Funksjon**-oppføringen erstatter du **O\_prognose** med navnet på prognosemodell-ID-en som skal brukes med integrasjonen.</span><span class="sxs-lookup"><span data-stu-id="7b360-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="7b360-140">Standardmalen har en prognosemodell-ID fra demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="7b360-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="7b360-141">Hvis du oppretter en ny mal, må du legge til denne kolonnen.</span><span class="sxs-lookup"><span data-stu-id="7b360-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="7b360-142">Velg **Legg til betinget kolonne** i Power Query, og skriv inn et navn for den nye kolonnen, for eksempel **Modell-ID**.</span><span class="sxs-lookup"><span data-stu-id="7b360-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="7b360-143">Angi betingelsen for kolonnen, der du, hvis prosjektoppgave ikke er null, skal \<angi prognosemodell-ID-en\>. Ellers null.</span><span class="sxs-lookup"><span data-stu-id="7b360-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="7b360-144">Filtrere ut ressursspesifikke oppføringer</span><span class="sxs-lookup"><span data-stu-id="7b360-144">Filter out resource-specific records</span></span>

<span data-ttu-id="7b360-145">Malen Estimater for prosjekttimer (PSA til Fin og OPS) har et standardfilter som fjerner eventuelle ressursspesifikke oppføringer.</span><span class="sxs-lookup"><span data-stu-id="7b360-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="7b360-146">Hvis du oppretter din egen mal, må du legge til dette filteret.</span><span class="sxs-lookup"><span data-stu-id="7b360-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="7b360-147">Velg koblingen **Avansert spørring og filtrering** for å filtrere etter kolonnen **msdyn\_islinetask**, slik at bare **Usann** oppføringer tas med.</span><span class="sxs-lookup"><span data-stu-id="7b360-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="7b360-148">Filtrer ut tomme rader for transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="7b360-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="7b360-149">Du må legge til et filter for å fjerne alle rader som har tomme transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="7b360-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="7b360-150">Denne oppgaven er obligatorisk, uansett om du bruker standardmalen eller oppretter en egen mal.</span><span class="sxs-lookup"><span data-stu-id="7b360-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="7b360-151">Dette filteret fjerner alle sammendragsrader fra Project Service Automation som kan føre til at timeprognoser i Finance blir feil.</span><span class="sxs-lookup"><span data-stu-id="7b360-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="7b360-152">Velg **Avansert spørring og filtrering**-koblingen for å filtrere ut null-oppføringer i kolonnen **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="7b360-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7b360-153">Maltilordning i dataintegrering</span><span class="sxs-lookup"><span data-stu-id="7b360-153">Template mapping in Data integration</span></span>

<span data-ttu-id="7b360-154">Illustrasjonen nedenfor viser et eksempel på maloppgavetilordningen i dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="7b360-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="7b360-155">Tilordningen viser feltinformasjonen som blir synkronisert fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="7b360-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7b360-156">[![Maltilordning](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7b360-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="7b360-157">Prosjektets utgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="7b360-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="7b360-158">Mal og oppgaver</span><span class="sxs-lookup"><span data-stu-id="7b360-158">Template and tasks</span></span>

<span data-ttu-id="7b360-159">Følgende mal og underliggende oppgaver brukes til å synkronisere estimater for prosjektutgifter fra Project Service Automation til Finance:</span><span class="sxs-lookup"><span data-stu-id="7b360-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="7b360-160">**Navn på malen i dataintegrering:** Estimater for prosjektutgifter (PSA til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="7b360-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="7b360-161">**Navn på oppgavene i prosjektet:**</span><span class="sxs-lookup"><span data-stu-id="7b360-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="7b360-162">Transaksjonsrelasjoner</span><span class="sxs-lookup"><span data-stu-id="7b360-162">Transaction relationships</span></span> 
    - <span data-ttu-id="7b360-163">Utgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="7b360-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="7b360-164">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="7b360-164">Entity set</span></span>

| <span data-ttu-id="7b360-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7b360-165">Project Service Automation</span></span> | <span data-ttu-id="7b360-166">Finans</span><span class="sxs-lookup"><span data-stu-id="7b360-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="7b360-167">Transaksjonstilkoblinger</span><span class="sxs-lookup"><span data-stu-id="7b360-167">Transaction Connections</span></span>    | <span data-ttu-id="7b360-168">Integreringsenhet for prosjekttransaksjonsrelasjoner</span><span class="sxs-lookup"><span data-stu-id="7b360-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="7b360-169">Estimatlinjer</span><span class="sxs-lookup"><span data-stu-id="7b360-169">Estimate Lines</span></span>             | <span data-ttu-id="7b360-170">Integreringsenhet for estimater for prosjektutgifter</span><span class="sxs-lookup"><span data-stu-id="7b360-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="7b360-171">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="7b360-171">Entity flow</span></span>

<span data-ttu-id="7b360-172">Estimater for prosjektutgifter administreres i Project Service Automation, og de synkroniseres til Finance som prognoser for prosjektutgifter.</span><span class="sxs-lookup"><span data-stu-id="7b360-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7b360-173">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="7b360-173">Prerequisites</span></span>

<span data-ttu-id="7b360-174">Før synkronisering av estimater for prosjektutgifter kan skje, må du synkronisere prosjekter, prosjektoppgaver og prosjektets utgiftstransaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="7b360-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="7b360-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="7b360-175">Power Query</span></span>

<span data-ttu-id="7b360-176">I malen for estimat av prosjektutgifter må du bruke Power Query til å utføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="7b360-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="7b360-177">Filter for å inkludere bare linjeposter for utgiftsestimater.</span><span class="sxs-lookup"><span data-stu-id="7b360-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="7b360-178">Angi standard prognosemodell-ID som skal brukes når integreringen oppretter nye timeprognoser.</span><span class="sxs-lookup"><span data-stu-id="7b360-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="7b360-179">Transformer faktureringstypene.</span><span class="sxs-lookup"><span data-stu-id="7b360-179">Transform the billing types.</span></span>
- <span data-ttu-id="7b360-180">Transformer transaksjonstypene.</span><span class="sxs-lookup"><span data-stu-id="7b360-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="7b360-181">Filter for å inkludere bare linjer for utgiftsestimater.</span><span class="sxs-lookup"><span data-stu-id="7b360-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="7b360-182">Malen for estimater for prosjektutgifter (PSA til fin og OPS) har et standardfilter som bare inkluderer utgiftslinjer i integrasjonen.</span><span class="sxs-lookup"><span data-stu-id="7b360-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="7b360-183">Hvis du oppretter din egen mal, må du legge til dette filteret.</span><span class="sxs-lookup"><span data-stu-id="7b360-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="7b360-184">Velg oppgaven **Transaksjonsrelasjoner**, og klikk deretter **Tilordne**-pilen for å åpne tilordningen.</span><span class="sxs-lookup"><span data-stu-id="7b360-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7b360-185">Velg koblingen **Avansert spørring og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="7b360-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="7b360-186">Filtrer kolonnen **msdyn\_transactiontype1**, slik at den bare inkluderer **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="7b360-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="7b360-187">Angi standard prognosemodell-ID</span><span class="sxs-lookup"><span data-stu-id="7b360-187">Set the default forecast model ID</span></span>

<span data-ttu-id="7b360-188">Hvis du vil oppdatere standard prognosemodell-ID i malen, velger du oppgaven **Utgiftsestimater**, og deretter klikker du **Tilordne**-pilen for å åpne tilordningen.</span><span class="sxs-lookup"><span data-stu-id="7b360-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7b360-189">Velg koblingen **Avansert spørring og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="7b360-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="7b360-190">Hvis du bruker standardmalen for estimater for prosjektutgifter (PSA til Fin og OPS) i Power Query, velger du først **Innsatt betingelse** fra delen **Brukte trinn**.</span><span class="sxs-lookup"><span data-stu-id="7b360-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="7b360-191">I **Funksjon**-oppføringen erstatter du **O\_prognose** med navnet på prognosemodell-ID-en som skal brukes med integrasjonen.</span><span class="sxs-lookup"><span data-stu-id="7b360-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="7b360-192">Standardmalen har en prognosemodell-ID fra demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="7b360-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="7b360-193">Hvis du oppretter en ny mal, må du legge til denne kolonnen.</span><span class="sxs-lookup"><span data-stu-id="7b360-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="7b360-194">Velg **Legg til betinget kolonne** i Power Query, og skriv inn et navn for den nye kolonnen, for eksempel **Modell-ID**.</span><span class="sxs-lookup"><span data-stu-id="7b360-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="7b360-195">Angi betingelsen for kolonnen, der du, hvis estimatlinje-ID ikke er null, skal \<angi prognosemodell-ID-en\>. Ellers null.</span><span class="sxs-lookup"><span data-stu-id="7b360-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="7b360-196">Transformer faktureringstypene</span><span class="sxs-lookup"><span data-stu-id="7b360-196">Transform the billing types</span></span>

<span data-ttu-id="7b360-197">Malen for estimater for prosjektutgifter (PSA til Fin og OPS) inkluderer en betinget kolonne som brukes til å transformere faktureringstypene som er mottatt fra Project Service Automation under integreringen.</span><span class="sxs-lookup"><span data-stu-id="7b360-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="7b360-198">Hvis du oppretter din egen mal, må du legge til denne betinget-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="7b360-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="7b360-199">Velg **Avanserte spørring og filtrering**-koblingen, og velg deretter **Legg til betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="7b360-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="7b360-200">Angi et navn for den nye kolonnen, for eksempel **Faktureringstype**.</span><span class="sxs-lookup"><span data-stu-id="7b360-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="7b360-201">Skriv deretter inn følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="7b360-201">Then enter the following condition:</span></span>

<span data-ttu-id="7b360-202">Hvis **msdyn\_billingtype** = 192350000, er den **Ikke-belastbar**</span><span class="sxs-lookup"><span data-stu-id="7b360-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="7b360-203">Hvis **msdyn\_billingtype** = 192350001, er den **Belastbar**</span><span class="sxs-lookup"><span data-stu-id="7b360-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="7b360-204">Hvis **msdyn\_billingtype** = 192350002, er den **Komplementær**</span><span class="sxs-lookup"><span data-stu-id="7b360-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="7b360-205">Hvis ikke **Ikke tilgjengelig**</span><span class="sxs-lookup"><span data-stu-id="7b360-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="7b360-206">Transformer transaksjonstypene</span><span class="sxs-lookup"><span data-stu-id="7b360-206">Transform the transaction types</span></span>

<span data-ttu-id="7b360-207">Malen for estimater for prosjektutgifter (PSA til Fin og OPS) inkluderer en betinget kolonne som brukes til å transformere transaksjonstypene som er mottatt fra Project Service Automation under integreringen.</span><span class="sxs-lookup"><span data-stu-id="7b360-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="7b360-208">Hvis du oppretter din egen mal, må du legge til denne betinget-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="7b360-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="7b360-209">Velg **Avanserte spørring og filtrering**-koblingen, og velg deretter **Legg til betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="7b360-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="7b360-210">Angi et navn for den nye kolonnen, for eksempel **Transaksjonstype**.</span><span class="sxs-lookup"><span data-stu-id="7b360-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="7b360-211">Skriv deretter inn følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="7b360-211">Then enter the following condition:</span></span>

<span data-ttu-id="7b360-212">Hvis **msdyn\_transactiontypecode** = 192350000, er det **Kostnad**</span><span class="sxs-lookup"><span data-stu-id="7b360-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="7b360-213">Hvis **msdyn\_transactiontypecode** = 192350005, er det **Salg**</span><span class="sxs-lookup"><span data-stu-id="7b360-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="7b360-214">Hvis ikke er det **Null**</span><span class="sxs-lookup"><span data-stu-id="7b360-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7b360-215">Maltilordning i dataintegrering</span><span class="sxs-lookup"><span data-stu-id="7b360-215">Template mapping in Data integration</span></span>

<span data-ttu-id="7b360-216">Illustrasjonene nedenfor viser eksempler på maloppgavetilordningene i dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="7b360-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="7b360-217">Tilordningen viser feltinformasjonen som blir synkronisert fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="7b360-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7b360-218">[![Maltilordning](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7b360-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="7b360-219">[![Maltilordning](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7b360-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
