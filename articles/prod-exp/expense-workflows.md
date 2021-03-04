---
title: Konfigurere arbeidsflyter for utgiftshåndtering
description: Du kan sette opp en arbeidsflytprosess for å gjennomgå og godkjenne reise- og utgiftsdokumenter.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f3235d12499c68a52f9d1c7e118e7bc91dc3a0a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960529"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="0f42c-103">Konfigurere arbeidsflyter for utgiftshåndtering</span><span class="sxs-lookup"><span data-stu-id="0f42c-103">Set up Expense management workflows</span></span>

<span data-ttu-id="0f42c-104">Du kan sette opp en arbeidsflytprosess som brukes til å gjennomgå og godkjenne reise- og utgiftsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="0f42c-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="0f42c-105">Dokumentene som arbeidsflyter kan defineres for, inkluderer reiseregninger, reiserekvisisjoner og forespørsler om forskudd.</span><span class="sxs-lookup"><span data-stu-id="0f42c-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="0f42c-106">En arbeidsflyt representerer en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="0f42c-106">A workflow represents a business process.</span></span> <span data-ttu-id="0f42c-107">Den definerer hvordan et dokument flyter gjennom systemet, og viser hvem som må fullføre en oppgave eller godkjenne et dokument.</span><span class="sxs-lookup"><span data-stu-id="0f42c-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="0f42c-108">Det er flere fordeler ved å bruke arbeidsflytsystemet i organisasjonen:</span><span class="sxs-lookup"><span data-stu-id="0f42c-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="0f42c-109">**Konsistente prosesser** – Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter.</span><span class="sxs-lookup"><span data-stu-id="0f42c-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="0f42c-110">Ved å bruke arbeidsflytsystemet bidrar du til å sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="0f42c-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="0f42c-111">Prosess-synlighet – Du kan spore måledata for status, logg og ytelse for en bestemt arbeidsflytforekomst.</span><span class="sxs-lookup"><span data-stu-id="0f42c-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="0f42c-112">Dette gjør det mulig for deg å fastsette om endringer skal utføres i arbeidsflyten for å forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="0f42c-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="0f42c-113">Sentralisert arbeidsliste – Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og godkjenningene som er tilordnet dem.</span><span class="sxs-lookup"><span data-stu-id="0f42c-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="0f42c-114">**Typene arbeidsflyter du kan opprette**</span><span class="sxs-lookup"><span data-stu-id="0f42c-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="0f42c-115">Tabellen nedenfor viser hvilke typer arbeidsflyter du kan opprette i **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="0f42c-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="0f42c-116"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="0f42c-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="0f42c-117"><strong>Bruk denne typen til å</strong></span><span class="sxs-lookup"><span data-stu-id="0f42c-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="0f42c-118"><strong>Utgiftsrapport</strong></span><span class="sxs-lookup"><span data-stu-id="0f42c-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="0f42c-119">Opprette arbeidsflyter for godkjenning av reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="0f42c-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="0f42c-120"><strong>Automatisk bokføring av reiseregning</strong></span><span class="sxs-lookup"><span data-stu-id="0f42c-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="0f42c-121">Opprette arbeidsflyter for automatisk bokføring av reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="0f42c-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="0f42c-122"><strong>Utgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="0f42c-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="0f42c-123">Opprette arbeidsflyter for godkjenning av linjeelementer i reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="0f42c-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="0f42c-124"><strong>Automatisk postering av utgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="0f42c-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="0f42c-125">Opprette arbeidsflyter for automatisk postering av linjeelementer i reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="0f42c-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="0f42c-126"><strong>Reiserekvisisjon</strong></span><span class="sxs-lookup"><span data-stu-id="0f42c-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="0f42c-127">Opprette arbeidsflyter for godkjenning av reiserekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="0f42c-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="0f42c-128"><strong>Forespørsel om kontantforskudd</strong></span><span class="sxs-lookup"><span data-stu-id="0f42c-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="0f42c-129">Opprette arbeidsflyter for godkjenning av forespørsler om kontantforskudd.</span><span class="sxs-lookup"><span data-stu-id="0f42c-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="0f42c-130"><strong>Mva-fradrag</strong></span><span class="sxs-lookup"><span data-stu-id="0f42c-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="0f42c-131">Opprette arbeidsflyter for godkjenning av Mva-fradrag.</span><span class="sxs-lookup"><span data-stu-id="0f42c-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

