---
title: Reiserekvisisjoner
description: Dette emnet inneholder informasjon om reiserekvisisjoner.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081489"
---
# <a name="travel-requisitions"></a><span data-ttu-id="66dbc-103">Reiserekvisisjoner</span><span class="sxs-lookup"><span data-stu-id="66dbc-103">Travel requisitions</span></span>

<span data-ttu-id="66dbc-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="66dbc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="66dbc-105">En reiserekvisisjon gir en oversikt over utgiftene som vil påløpe for reiseformål.</span><span class="sxs-lookup"><span data-stu-id="66dbc-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="66dbc-106">En reiserekvisisjon sendes inn til gjennomgang og kan brukes til å autorisere utgifter.</span><span class="sxs-lookup"><span data-stu-id="66dbc-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="66dbc-107">Du kan bli bedt om å sende en reiserekvisisjon før du påløper noen som helst utgift som skal belastes organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="66dbc-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="66dbc-108">Dette kravet gjelder uansett om du betaler utgifter med et kredittkort som tilhører bedriften, bruker kontanter som du har mottatt fra forskudd, eller betaler utgifter av egen lomme som skal refunderes av organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="66dbc-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="66dbc-109">Reiserekvisisjoner og policyer kan brukes til å administrere organisasjonens utgifter.</span><span class="sxs-lookup"><span data-stu-id="66dbc-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="66dbc-110">Hvis for eksempel organisasjonen din arbeider med et fastprisprosjekt som krever reise, må reiseutgiftene for prosjektets teammedlemmer være innenfor prosjektbudsjettet.</span><span class="sxs-lookup"><span data-stu-id="66dbc-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="66dbc-111">Ved å kreve at reiseutgifter godkjennes før de påløper, kan organisasjonen bidra til å sikre at prosjektet holder seg innenfor budsjettet.</span><span class="sxs-lookup"><span data-stu-id="66dbc-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="66dbc-112">Konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="66dbc-112">Configuration</span></span> 

<span data-ttu-id="66dbc-113">Reiserekvisisjoner kan konfigureres som "obligatorisk" ved å aktivere parameteren "Forhåndsautorisasjon av reise er obligatorisk" i parametere for utgiftshåndtering.</span><span class="sxs-lookup"><span data-stu-id="66dbc-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="66dbc-114">Opprette og sende en reiserekvisisjon</span><span class="sxs-lookup"><span data-stu-id="66dbc-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="66dbc-115">Gå til **Mine utgifter: Reiserekvisisjon** , og velg **Ny reiserekvisisjon**.</span><span class="sxs-lookup"><span data-stu-id="66dbc-115">Go to **My expenses: Travel Requisition** , and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="66dbc-116">Angi et formål og et mål for rekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="66dbc-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="66dbc-117">Skriv inn eventuell tilleggsinformasjon i feltet **Reisebeskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="66dbc-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="66dbc-118">For hver av de forventede utgiftene, for eksempel flyreiser, måltider eller bilutleie, oppretter du et utgiftslinjeelement.</span><span class="sxs-lookup"><span data-stu-id="66dbc-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="66dbc-119">Inkluder estimert dato, estimert beløp og valuta for hver utgift.</span><span class="sxs-lookup"><span data-stu-id="66dbc-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="66dbc-120">Når du er ferdig med å legge til de forventede utgiftene, velger du **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="66dbc-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="66dbc-121">Når du er klar til å sende inn reise rekvisisjonen, velger du **Arbeidsflyt** > **Send**.</span><span class="sxs-lookup"><span data-stu-id="66dbc-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="66dbc-122">Du kan vise godkjente reiserekvisisjoner under **Mine utgifter: Reiserekvisisjon**.</span><span class="sxs-lookup"><span data-stu-id="66dbc-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="66dbc-123">Vise tilgjengelige reiserekvisisjoner</span><span class="sxs-lookup"><span data-stu-id="66dbc-123">View available travel requisitions</span></span>

<span data-ttu-id="66dbc-124">Du kan vise alle reiserekvisisjonene dine under **Mine utgifter: Reiserekvisisjoner**.</span><span class="sxs-lookup"><span data-stu-id="66dbc-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="66dbc-125">Godkjenn reiserekvisisjoner</span><span class="sxs-lookup"><span data-stu-id="66dbc-125">Approve travel requisitions</span></span>

<span data-ttu-id="66dbc-126">Velg reiserekvisisjonen du vil godkjenne, og velg deretter **Arbeidsflyt** > **Godkjenn**.</span><span class="sxs-lookup"><span data-stu-id="66dbc-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="66dbc-127">Send inn en reiseregning ved hjelp av den godkjente reiserekvisisjonen</span><span class="sxs-lookup"><span data-stu-id="66dbc-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="66dbc-128">Opprett en ny reiseregning, og i hodet i reiseregningen, og fra listen over godkjente reiserekvisisjoner, velger du **Tilordne til reiserekvisisjon**.</span><span class="sxs-lookup"><span data-stu-id="66dbc-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="66dbc-129">Feltet **Beløp for reiserekvisisjon** oppdateres automatisk i hodet i reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="66dbc-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="66dbc-130">Legg til hver utgift som er påløpt for reisen.</span><span class="sxs-lookup"><span data-stu-id="66dbc-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="66dbc-131">Hvis feltet **Forhåndsgodkjent** er aktivert, oppdateres det avstemte beløpet og det godkjente beløpet for den spesifikke utgiftskategorien.</span><span class="sxs-lookup"><span data-stu-id="66dbc-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="66dbc-132">Når du tilordner en reiseregning til en godkjent reiserekvisisjon, kan ikke transaksjonsbeløpet være større enn det godkjente beløpet.</span><span class="sxs-lookup"><span data-stu-id="66dbc-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
