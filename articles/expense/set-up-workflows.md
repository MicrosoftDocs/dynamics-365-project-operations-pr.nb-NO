---
title: Konfigurere arbeidsflyter for reiseregning og utlegg
description: Du kan sette opp en arbeidsflytprosess som brukes til å gjennomgå og godkjenne reise- og utgiftsdokumenter.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e54fca67427e8f3d0e7050563a751b5be354356c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276045"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="4890f-103">Konfigurere arbeidsflyter for reiseregning og utlegg</span><span class="sxs-lookup"><span data-stu-id="4890f-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="4890f-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="4890f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4890f-105">Du kan sette opp en arbeidsflytprosess for å gjennomgå og godkjenne reise- og utgiftsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="4890f-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="4890f-106">Du kan definere arbeidsflyter for reiseregninger, reiserekvisisjoner og forespørsler om forskudd.</span><span class="sxs-lookup"><span data-stu-id="4890f-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="4890f-107">En arbeidsflyt representerer en forretningsprosess og definerer hvordan et dokument flyter gjennom systemet.</span><span class="sxs-lookup"><span data-stu-id="4890f-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="4890f-108">Arbeidsflyten angir også hvem som må fullføre en oppgave eller godkjenne et dokument.</span><span class="sxs-lookup"><span data-stu-id="4890f-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="4890f-109">Det er flere fordeler ved å bruke arbeidsflytsystemet i organisasjonen:</span><span class="sxs-lookup"><span data-stu-id="4890f-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="4890f-110">**Konsistente prosesser**: Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter.</span><span class="sxs-lookup"><span data-stu-id="4890f-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="4890f-111">Ved å bruke arbeidsflytsystemet bidrar du til å sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="4890f-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="4890f-112">**Prosess-synlighet**: Du kan spore måledata for status, logg og ytelse for en bestemt arbeidsflytforekomst.</span><span class="sxs-lookup"><span data-stu-id="4890f-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="4890f-113">Dette gjør det mulig for deg å fastsette om endringer skal utføres i arbeidsflyten for å forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="4890f-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="4890f-114">**Sentralisert arbeidsliste**: Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og godkjenningene som er tilordnet dem.</span><span class="sxs-lookup"><span data-stu-id="4890f-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="4890f-115">Arbeidsflyttyper</span><span class="sxs-lookup"><span data-stu-id="4890f-115">Workflow types</span></span>

<span data-ttu-id="4890f-116">Tabellen nedenfor viser hvilke typer arbeidsflyter du kan opprette i **Reiseregning og utlegg**.</span><span class="sxs-lookup"><span data-stu-id="4890f-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="4890f-117"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="4890f-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="4890f-118"><strong>Bruk denne typen til å</strong></span><span class="sxs-lookup"><span data-stu-id="4890f-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="4890f-119"><strong>Automatisk goodkjenning av reiseregninger</strong></span><span class="sxs-lookup"><span data-stu-id="4890f-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="4890f-120">Opprette arbeidsflyter for godkjenning av reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="4890f-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="4890f-121"><strong>Automatisk bokføring av reiseregning</strong></span><span class="sxs-lookup"><span data-stu-id="4890f-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="4890f-122">Opprette arbeidsflyter for automatisk bokføring av reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="4890f-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="4890f-123"><strong>Utgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="4890f-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="4890f-124">Opprette arbeidsflyter for godkjenning av linjeelementer i reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="4890f-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="4890f-125"><strong>Automatisk postering av utgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="4890f-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="4890f-126">Opprette arbeidsflyter for automatisk postering av linjeelementer i reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="4890f-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="4890f-127"><strong>Reiserekvisisjon</strong></span><span class="sxs-lookup"><span data-stu-id="4890f-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="4890f-128">Opprette arbeidsflyter for godkjenning av reiserekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="4890f-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="4890f-129"><strong>Forespørsel om kontantforskudd</strong></span><span class="sxs-lookup"><span data-stu-id="4890f-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="4890f-130">Opprette arbeidsflyter for godkjenning av forespørsler om kontantforskudd.</span><span class="sxs-lookup"><span data-stu-id="4890f-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="4890f-131"><strong>Mva-fradrag</strong></span><span class="sxs-lookup"><span data-stu-id="4890f-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="4890f-132">Opprette arbeidsflyter for godkjenning av Mva-fradrag.</span><span class="sxs-lookup"><span data-stu-id="4890f-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]