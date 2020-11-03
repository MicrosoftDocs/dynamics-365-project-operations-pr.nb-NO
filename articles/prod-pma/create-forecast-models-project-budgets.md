---
title: Opprette prognosemodeller for prosjektbudsjetter
description: Dette emnet beskriver hvordan du oppretter en prognosemodell for gjenstående budsjetter.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081756"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="d4356-103">Opprette prognosemodeller for prosjektbudsjetter</span><span class="sxs-lookup"><span data-stu-id="d4356-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4356-104">Dette emnet beskriver hvordan du oppretter en prognosemodell for gjenstående budsjetter.</span><span class="sxs-lookup"><span data-stu-id="d4356-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="d4356-105">Et prosjekt som er underlagt budsjettkontroll, bruker to typer budsjetter: opprinnelig og gjenstående.</span><span class="sxs-lookup"><span data-stu-id="d4356-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="d4356-106">Når du oppretter et prosjektbudsjett, må du angi de opprinnelige og gjenværende budsjettprognosemodellene som ble opprettet på siden **Prognosemodeller**.</span><span class="sxs-lookup"><span data-stu-id="d4356-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="d4356-107">Prosjektbudsjetter som er basert på de angitte modellene, blir opprettet når du vedtar prosjektbudsjettet.</span><span class="sxs-lookup"><span data-stu-id="d4356-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="d4356-108">En prognosemodell som brukes for budsjettkontroll, kan ikke ha en undermodell eller brukes som undermodell.</span><span class="sxs-lookup"><span data-stu-id="d4356-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="d4356-109">Velg **Prosjektstyring og regnskap** > **Oppsett** > **Prognoser**  > **Prognosemodeller**.</span><span class="sxs-lookup"><span data-stu-id="d4356-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="d4356-110">Velg **Ny** for å opprette en ny prognosemodell, og skriv deretter inn et ID-nummer for modellen og navnet på den nye modellen.</span><span class="sxs-lookup"><span data-stu-id="d4356-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="d4356-111">Sett **Stoppet** -alternativet til **Ja** for å forhindre eventuelle endringer i prognoselinjer for prognosemodellen.</span><span class="sxs-lookup"><span data-stu-id="d4356-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="d4356-112">Hvis prognoselinjene som modellen er knyttet til, må generere kontantstrømprognoser i hovedboken, må du sette **Inkluder i kontantstrømprognoser** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d4356-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="d4356-113">Hvis du vil bruke prosjektdatoen som fakturadato, setter du **Fakturadato for prognose** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d4356-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="d4356-114">I **Budsjettype** -feltet velger du én av følgende modelltyper:</span><span class="sxs-lookup"><span data-stu-id="d4356-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="d4356-115">**Opprinnelig budsjett** : Bruk de opprinnelige budsjettbeløpene som ble vedtatt da det opprinnelige budsjettet ble opprettet og godkjent.</span><span class="sxs-lookup"><span data-stu-id="d4356-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="d4356-116">**Gjenstående budsjett** : Bruk de gjenstående budsjettbeløpene i løpet av prosjektets levetid.</span><span class="sxs-lookup"><span data-stu-id="d4356-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="d4356-117">Saldoene i denne prognosemodellen reduseres med faktiske transaksjoner, og økes eller reduseres etter budsjettendringer.</span><span class="sxs-lookup"><span data-stu-id="d4356-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="d4356-118">**Viderefør** : Bruk budsjettbeløpene for videreføring for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d4356-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="d4356-119">Videreføring er en valgfri prosess som kan kjøres for å overføre ubrukte budsjettbeløp fra ett regnskapsår til et annet.</span><span class="sxs-lookup"><span data-stu-id="d4356-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="d4356-120">Angi følgende alternativer etter behov:</span><span class="sxs-lookup"><span data-stu-id="d4356-120">Set the following options as required:</span></span>

   - <span data-ttu-id="d4356-121">Aktiver **Fakturadato for prognose** hvis du vil bruke prosjektdatoen som fakturadato.</span><span class="sxs-lookup"><span data-stu-id="d4356-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="d4356-122">Aktiver **Prognose med VIA** for prognoser basert på varer i arbeid (VIA), og velg deretter type VIA.</span><span class="sxs-lookup"><span data-stu-id="d4356-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="d4356-123">Du kan beholde standard **Budsjettype** som **Ingen** eller angi en ny type.</span><span class="sxs-lookup"><span data-stu-id="d4356-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="d4356-124">Budsjettypen kan ikke endres etter at du har endret en oppføring.</span><span class="sxs-lookup"><span data-stu-id="d4356-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="d4356-125">Hvis du endrer standard budsjettype, blir alle andre alternativer utilgjengelig for oppdateringer, og du kan ikke bruke denne prognosemodellen på nytt.</span><span class="sxs-lookup"><span data-stu-id="d4356-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

