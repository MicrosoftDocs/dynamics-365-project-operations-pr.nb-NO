---
title: Nyheter mars 2021 – Project Operations Lite-distribusjon
description: Dette emnet gir informasjon om kvalitetsoppdateringene som er tilgjengelige i mars 2021-versjonen av Project Operations Lite-distribusjon.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500026"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="51056-103">Nyheter mars 2021 – Project Operations Lite-distribusjon</span><span class="sxs-lookup"><span data-stu-id="51056-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="51056-104">_Gjelder: Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="51056-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="51056-105">Dette emnet gjelder for følgende Dynamics 365 Project Operations-komponenter og versjoner:</span><span class="sxs-lookup"><span data-stu-id="51056-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="51056-106">Project Operations på Dataverse-miljø versjon 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="51056-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="51056-107">Kvalitetsoppdateringer</span><span class="sxs-lookup"><span data-stu-id="51056-107">Quality updates</span></span>

| <span data-ttu-id="51056-108">**Funksjonsområdet**</span><span class="sxs-lookup"><span data-stu-id="51056-108">**Feature area**</span></span> | <span data-ttu-id="51056-109">**Referansenummer**</span><span class="sxs-lookup"><span data-stu-id="51056-109">**Reference number**</span></span> | <span data-ttu-id="51056-110">**Kvalitetsoppdatering**</span><span class="sxs-lookup"><span data-stu-id="51056-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="51056-111">Fakturering og prising</span><span class="sxs-lookup"><span data-stu-id="51056-111">Billing and pricing</span></span> | <span data-ttu-id="51056-112">2133873</span><span class="sxs-lookup"><span data-stu-id="51056-112">2133873</span></span> | <span data-ttu-id="51056-113">Løste visningen av valutasymbolet **Enhetssalgspris** i rutenettet **Utgiftsestimater**.</span><span class="sxs-lookup"><span data-stu-id="51056-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="51056-114">Fakturering og prising</span><span class="sxs-lookup"><span data-stu-id="51056-114">Billing and pricing</span></span> | <span data-ttu-id="51056-115">2174616</span><span class="sxs-lookup"><span data-stu-id="51056-115">2174616</span></span> | <span data-ttu-id="51056-116">Når et tilbud blir vunnet, refereres det til den egendefinerte prislisten for kontrakten på kontraktlinjedetaljer som kopieres fra tilbudet.</span><span class="sxs-lookup"><span data-stu-id="51056-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="51056-117">Administrasjon av salgsmulighet</span><span class="sxs-lookup"><span data-stu-id="51056-117">Opportunity Management</span></span> | <span data-ttu-id="51056-118">2167475</span><span class="sxs-lookup"><span data-stu-id="51056-118">2167475</span></span> | <span data-ttu-id="51056-119">Løste avgiftsbeløp i rettelsesfakturaen som opprinnelig var en ufakturert faktisk oppføring.</span><span class="sxs-lookup"><span data-stu-id="51056-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="51056-120">Administrasjon av salgsmulighet</span><span class="sxs-lookup"><span data-stu-id="51056-120">Opportunity Management</span></span> | <span data-ttu-id="51056-121">2176285</span><span class="sxs-lookup"><span data-stu-id="51056-121">2176285</span></span> | <span data-ttu-id="51056-122">Avgiftsbeløp må ikke kopieres fra detaljer om salgskontrakt/tilbudslinje til detaljer om kostnadskontrakt/tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="51056-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="51056-123">Administrasjon av salgsmulighet</span><span class="sxs-lookup"><span data-stu-id="51056-123">Opportunity Management</span></span> | <span data-ttu-id="51056-124">2188079</span><span class="sxs-lookup"><span data-stu-id="51056-124">2188079</span></span> | <span data-ttu-id="51056-125">Delt faktureringsregel må ikke opprettes for kontrakter som ikke er arbeidsbaserte.</span><span class="sxs-lookup"><span data-stu-id="51056-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="51056-126">Planlegging og sporing</span><span class="sxs-lookup"><span data-stu-id="51056-126">Planning and Tracking</span></span> | <span data-ttu-id="51056-127">2138853</span><span class="sxs-lookup"><span data-stu-id="51056-127">2138853</span></span> | <span data-ttu-id="51056-128">Prosjektkopieringsfunksjon er oppdatert for å sikre at kostnadsestimatlinjer som refererer til oppgaver, kopieres til målprosjektet.</span><span class="sxs-lookup"><span data-stu-id="51056-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="51056-129">Planlegging og sporing</span><span class="sxs-lookup"><span data-stu-id="51056-129">Planning and Tracking</span></span> | <span data-ttu-id="51056-130">2173259</span><span class="sxs-lookup"><span data-stu-id="51056-130">2173259</span></span> | <span data-ttu-id="51056-131">Prosjektkopieringsfunksjon er oppdatert for å sikre at den ikke viser feilmeldingen **Kopierer WBS** i bestemte scenarioer.</span><span class="sxs-lookup"><span data-stu-id="51056-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="51056-132">Tid og utgift</span><span class="sxs-lookup"><span data-stu-id="51056-132">Time and Expense</span></span> | <span data-ttu-id="51056-133">2148910</span><span class="sxs-lookup"><span data-stu-id="51056-133">2148910</span></span> | <span data-ttu-id="51056-134">Løste visningsproblem med siden **Rediger oppføring** i rutenettet **Tidsoppføring**.</span><span class="sxs-lookup"><span data-stu-id="51056-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="51056-135">Tid og utgift</span><span class="sxs-lookup"><span data-stu-id="51056-135">Time and Expense</span></span> | <span data-ttu-id="51056-136">2159798</span><span class="sxs-lookup"><span data-stu-id="51056-136">2159798</span></span> | <span data-ttu-id="51056-137">Innsnevret kontroller for å sikre at godkjente utgiftsoppføringer ikke kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="51056-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


