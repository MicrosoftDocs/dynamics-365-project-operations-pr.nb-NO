---
title: Definere utgiftspolicyer
description: Du kan definere utgiftspolicyer som dine arbeidere må følge når de angir og sender ut reiseregningsrapporter og reiserekvisisjoner.
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
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128430"
---
# <a name="define-expense-policies"></a><span data-ttu-id="94b11-103">Definere utgiftspolicyer</span><span class="sxs-lookup"><span data-stu-id="94b11-103">Define expense policies</span></span>

<span data-ttu-id="94b11-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="94b11-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="94b11-105">Du kan definere policyer som dine arbeidere må følge når de angir og sender ut reiseregningsrapporter og reiserekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="94b11-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="94b11-106">Ved å implementere utgiftspolicyer kan du administrere utgifter effektivt.</span><span class="sxs-lookup"><span data-stu-id="94b11-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="94b11-107">Du kan for eksempel angi en policy for hotellutgifter i New York, som angir at reiseutgiften ikke kan overskrides USD 250 per natt.</span><span class="sxs-lookup"><span data-stu-id="94b11-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="94b11-108">Hvis en arbeider sender en reiseregning eller en reiserekvisisjon der romprisen overskrider dette beløpet, vil systemet varsle</span><span class="sxs-lookup"><span data-stu-id="94b11-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="94b11-109">arbeideren om at policybeløpet for utgiften er overskredet.</span><span class="sxs-lookup"><span data-stu-id="94b11-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="94b11-110">Du kan konfigurere meldingen som arbeideren skal motta når du</span><span class="sxs-lookup"><span data-stu-id="94b11-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="94b11-111">definener policyen.</span><span class="sxs-lookup"><span data-stu-id="94b11-111">define the policy.</span></span>      
        
<span data-ttu-id="94b11-112">Du kan definere tre typer policyer:</span><span class="sxs-lookup"><span data-stu-id="94b11-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="94b11-113">**Advarsel**: Gjør det mulig for den ansatte å sende en reiseregningsrapport eller reiserekvisisjon, men utgiften blir merket for alle godkjennere og</span><span class="sxs-lookup"><span data-stu-id="94b11-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="94b11-114">for senere rapportering.</span><span class="sxs-lookup"><span data-stu-id="94b11-114">for later reporting.</span></span>        

- <span data-ttu-id="94b11-115">**Feil**: Krever at arbeideren reviderer utgiften for å overholde policyen før han/hun sender reiseregningsrapporten eller reiserekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="94b11-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="94b11-116">**Begrunnelse**: Krever at arbeideren eller en overordnet angir en begrunnelse for å overskride policybeløpet før han/hun sender reiseregningsrapporten eller reiserekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="94b11-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="94b11-117">Policytips</span><span class="sxs-lookup"><span data-stu-id="94b11-117">Policy tips</span></span>
<span data-ttu-id="94b11-118">Her er noen forslag som kan hjelpe deg når du oppretter nye policyer for håndtering av reiseregning og utlegg:</span><span class="sxs-lookup"><span data-stu-id="94b11-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="94b11-119">Policyer er datobaserte, noe som betyr at en policy ikke trer i kraft hvis den opprettes med en dato etter datoen da utgiften oppstod.</span><span class="sxs-lookup"><span data-stu-id="94b11-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="94b11-120">Du oppretter for eksempel en ny policy i dag for å angi en maksimal utgift for måltider på USD 50.</span><span class="sxs-lookup"><span data-stu-id="94b11-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="94b11-121">Alle eksisterende utgifter som er angitt fra og med i går, blir ikke kontrollert mot denne policyen.</span><span class="sxs-lookup"><span data-stu-id="94b11-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="94b11-122">Når du oppretter en policy for en utgiftskategori som kan spesifiseres, vurderer du å legge til en betingelse for utgiftslinjetypen.</span><span class="sxs-lookup"><span data-stu-id="94b11-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="94b11-123">Noen policyer, for eksempel å kreve en kvittering, gir kanskje ikke mening for spesifiserte linjer.</span><span class="sxs-lookup"><span data-stu-id="94b11-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="94b11-124">I denne situasjonen brukes policyen bare på hodelinjen eller en ikke-spesifisert linje.</span><span class="sxs-lookup"><span data-stu-id="94b11-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="94b11-125">Policyer for utgiftsadministrasjon evalueres mot kildeenheten som standard.</span><span class="sxs-lookup"><span data-stu-id="94b11-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="94b11-126">For konserninterne scenarioer kan du angi at policyen skal evalueres mot målenheten (enhet som låner) i stedet.</span><span class="sxs-lookup"><span data-stu-id="94b11-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="94b11-127">Hvis du vil kjøre policyene mot målenheten, kan du aktivere funksjonen for **evaluering av reiseregninger mot juridisk låneenhet** i arbeidsområdet for **funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="94b11-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="94b11-128">Når policyer skal evalueres</span><span class="sxs-lookup"><span data-stu-id="94b11-128">When to evaluate policies</span></span>

<span data-ttu-id="94b11-129">I parametere for reiseregning og utlegg kan du velge å evaluere policyer for reiseregning og utlegg når en linje lagres, eller når en reiseregning sendes.</span><span class="sxs-lookup"><span data-stu-id="94b11-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="94b11-130">Hvis du velger å evaluere når en linje lagres, vil brukere ha tidligere innsyn i hva de må gjøre for å fullføre reiseregningen samtidig.</span><span class="sxs-lookup"><span data-stu-id="94b11-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="94b11-131">Hvis ikke kan du utsette policyevalueringen og spare tid ved å validere på slutten, under innsending til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="94b11-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
