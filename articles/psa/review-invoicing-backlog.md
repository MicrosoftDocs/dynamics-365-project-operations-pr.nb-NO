---
title: Se gjennom restansen for fakturering for prosjekter og prosjektkontrakter
description: Dette emnet gir informasjon om hvordan du gjennomgår tids-, utgifts- og produktrestanse, og hvordan du merker dem som klare til fakturering.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081829"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="d7879-103">Se gjennom restansen for fakturering for prosjekter og prosjektkontrakter</span><span class="sxs-lookup"><span data-stu-id="d7879-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d7879-104">Når en transaksjon er klar til få en faktura opprettet og behandlet, skal transaksjonen merkes **Klar for fakturering**.</span><span class="sxs-lookup"><span data-stu-id="d7879-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="d7879-105">Dette emnet beskriver transaksjonstypene som kan opprettes.</span><span class="sxs-lookup"><span data-stu-id="d7879-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="d7879-106">Se gjennom faktureringsrestanse for tid og materiale</span><span class="sxs-lookup"><span data-stu-id="d7879-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="d7879-107">Når en tids- eller utgiftsoppføring sendes og godkjennes for et prosjekt, oppretter PSA en faktisk prosjektverdi.</span><span class="sxs-lookup"><span data-stu-id="d7879-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="d7879-108">Hvis kombinasjonen av prosjektet og transaksjonsklassen tilordnes til en kontraktlinje for et tids-og-materiell-prosjekt, opprettes det to faktiske verdier når oppføringen godkjennes:</span><span class="sxs-lookup"><span data-stu-id="d7879-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="d7879-109">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="d7879-109">Cost actual</span></span> 
- <span data-ttu-id="d7879-110">Ufakturert faktisk salg</span><span class="sxs-lookup"><span data-stu-id="d7879-110">Unbilled sales actual</span></span>

<span data-ttu-id="d7879-111">Ufakturerte faktiske verdier for salg representerer faktureringsrestansen, og faktureringsstatusen må være satt **Klar for fakturering**.</span><span class="sxs-lookup"><span data-stu-id="d7879-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="d7879-112">Når en prosjektfaktura opprettes, blir ufakturerte faktiske verdier for salg merket som **Klar for fakturering** , kopiert over som fakturalinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="d7879-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="d7879-113">Hvis du vil se gjennom faktureringsrestansen for tid og materialer, går du til **Salg** \> **Fakturering** \> **Faktureringsrestanse for Tid og materiale**.</span><span class="sxs-lookup"><span data-stu-id="d7879-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="d7879-114">Velg alle ufakturerte faktiske verdier for salg som er klare for fakturering, og velg deretter **Klar for fakturering**.</span><span class="sxs-lookup"><span data-stu-id="d7879-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="d7879-115">Faktureringsstatusen for disse faktiske verdiene endres til **Klar for fakturering**.</span><span class="sxs-lookup"><span data-stu-id="d7879-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Faktureringsrestanse for Tid og materiale](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="d7879-117">Se gjennom faktureringsrestanse for produkt</span><span class="sxs-lookup"><span data-stu-id="d7879-117">Review the product billing backlog</span></span>

<span data-ttu-id="d7879-118">Når en prosjektkontrakt i PSA har produktbaserte kontraktlinjer, vurderes disse linjene for fakturering hver gang det opprettes en faktura for prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="d7879-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="d7879-119">Alle produkter som har kontraktlinjer som er merket **Klar for fakturering** , kopieres til prosjektfakturaen som prosjektfakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="d7879-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="d7879-120">Hvis du vil se gjennom faktureringsresistansen for produkter, går du til **Salg** \> **Fakturering** \> **Faktureringsrestanse for produkt**.</span><span class="sxs-lookup"><span data-stu-id="d7879-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="d7879-121">Merk av for alle de produktbaserte kontraktlinjene som er klare til fakturering, og velg deretter **Klar for fakturering**.</span><span class="sxs-lookup"><span data-stu-id="d7879-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="d7879-122">Faktureringsstatusen for disse linjene endres til **Klar for fakturering**.</span><span class="sxs-lookup"><span data-stu-id="d7879-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Faktureringsrestanse for produkt](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="d7879-124">Se gjennom faktureringsmilepæler på fastepriskontrakter</span><span class="sxs-lookup"><span data-stu-id="d7879-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="d7879-125">Hver prosjektkontraktlinje som har en fastprisfaktureringsmetode, må definere kontraktmilepæler.</span><span class="sxs-lookup"><span data-stu-id="d7879-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="d7879-126">Disse kontraktmilepælene kan bare faktureres hvis de er merket **Klar for fakturering**.</span><span class="sxs-lookup"><span data-stu-id="d7879-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="d7879-127">Hvis du vil se gjennom faktureringsmilepæler, går du til **Salg** \> **Fakturering** \> **Milepæler for fast pris**.</span><span class="sxs-lookup"><span data-stu-id="d7879-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="d7879-128">Velg milepælene som er klare for fakturering, og velg deretter **Klar for fakturering**.</span><span class="sxs-lookup"><span data-stu-id="d7879-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="d7879-129">Faktureringsstatusen for disse milepælene endres til **Klar for fakturering**.</span><span class="sxs-lookup"><span data-stu-id="d7879-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Milepæler for fast pris](media/FPBacklog.png)
