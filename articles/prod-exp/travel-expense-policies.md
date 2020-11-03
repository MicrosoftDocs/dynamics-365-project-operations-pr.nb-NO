---
title: Konfigurere utgiftspolicyer
description: Du kan konfigurere utgiftspolicyene som dine arbeidere må følge når de angir og sender ut reiseregningsrapporter og reiserekvisisjoner i Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081767"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="a442d-103">Konfigurere utgiftspolicyer</span><span class="sxs-lookup"><span data-stu-id="a442d-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a442d-104">Du kan definere policyer som dine arbeidere må følge når de angir og sender ut reiseregningsrapporter og reiserekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="a442d-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="a442d-105">Ved å implementere utgiftspolicyer kan du administrere utgifter effektivt.</span><span class="sxs-lookup"><span data-stu-id="a442d-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="a442d-106">Du kan for eksempel angi en policy for hotellutgifter i New York, som angir at reiseutgiften ikke kan overskrides USD 250 per natt.</span><span class="sxs-lookup"><span data-stu-id="a442d-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="a442d-107">Hvis en arbeider sender en reiseregning eller en reiserekvisisjon der romprisen overskrider dette beløpet, vil systemet varsle</span><span class="sxs-lookup"><span data-stu-id="a442d-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="a442d-108">arbeideren om at policybeløpet for utgiften er overskredet.</span><span class="sxs-lookup"><span data-stu-id="a442d-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="a442d-109">Du kan konfigurere meldingen som arbeideren skal motta når du</span><span class="sxs-lookup"><span data-stu-id="a442d-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="a442d-110">definener policyen.</span><span class="sxs-lookup"><span data-stu-id="a442d-110">define the policy.</span></span>      
        
<span data-ttu-id="a442d-111">Du kan definere tre typer policyer:</span><span class="sxs-lookup"><span data-stu-id="a442d-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="a442d-112">Advarsel – Gjør det mulig for den ansatte å sende en reiseregningsrapport eller reiserekvisisjon, men utgiften blir merket for alle godkjennere og</span><span class="sxs-lookup"><span data-stu-id="a442d-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="a442d-113">for senere rapportering.</span><span class="sxs-lookup"><span data-stu-id="a442d-113">for later reporting.</span></span>        

- <span data-ttu-id="a442d-114">Feil – Krever at arbeideren reviderer utgiften for å overholde policyen før han/hun sender reiseregningsrapporten eller reiserekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="a442d-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="a442d-115">Begrunnelse – Krever at arbeideren eller en overordnet angir en begrunnelse for å overskride policybeløpet før han/hun sender reiseregningsrapporten eller reiserekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="a442d-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="a442d-116">Policytips</span><span class="sxs-lookup"><span data-stu-id="a442d-116">Policy tips</span></span>
<span data-ttu-id="a442d-117">Her er noen forslag som kan hjelpe deg når du oppretter nye policyer for håndtering av reiseregning og utlegg.</span><span class="sxs-lookup"><span data-stu-id="a442d-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="a442d-118">Policyer er datobaserte, og en policy trer ikke i kraft hvis den opprettes med en dato etter datoen da utgiften oppstod.</span><span class="sxs-lookup"><span data-stu-id="a442d-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="a442d-119">Hvis du for eksempel oppretter en ny policy i dag for å håndheve en maksimal måltidsutgift på $50, sjekkes ikke eksisterende utgifter som er registrert i går, mot denne policyen.</span><span class="sxs-lookup"><span data-stu-id="a442d-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="a442d-120">Når du oppretter en policy for en utgiftskategori som kan spesifiseres, vurderer du å legge til en betingelse for utgiftslinjetypen.</span><span class="sxs-lookup"><span data-stu-id="a442d-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="a442d-121">Noen policyer, for eksempel krav om kvittering, vil kanskje ikke gi mening for spesifiserte linjer, og bør bare brukes på hodelinjen eller en linje uten varer.</span><span class="sxs-lookup"><span data-stu-id="a442d-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="a442d-122">Policyer for utgiftsadministrasjon evalueres mot kildeenheten som standard.</span><span class="sxs-lookup"><span data-stu-id="a442d-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="a442d-123">For konserninterne scenarioer kan du angi at policyen skal evalueres mot målenheten (enhet som låner) i stedet.</span><span class="sxs-lookup"><span data-stu-id="a442d-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="a442d-124">Hvis du vil kjøre policyene mot målenheten, kan du aktivere funksjonen for evaluering av reiseregninger mot juridisk låneenhet i arbeidsområdet **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="a442d-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="a442d-125">Når policyer skal evalueres</span><span class="sxs-lookup"><span data-stu-id="a442d-125">When to evaluate policies</span></span>

<span data-ttu-id="a442d-126">I parametere for reiseregning og utlegg er det et alternativ for å evaluere policyer for reiseregning og utlegg når en linje lagres, eller når en reiseregning sendes.</span><span class="sxs-lookup"><span data-stu-id="a442d-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="a442d-127">Hvis du velger å evaluere når en linje lagres, sørger dette for at brukere får tidligere innsyn i hva de må gjøre for å fullføre reiseregningen samtidig.</span><span class="sxs-lookup"><span data-stu-id="a442d-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="a442d-128">Hvis ikke kan du utsette policyevalueringen og spare tid under innsending til arbeidsflyten hvis valideringen foregår på slutten.</span><span class="sxs-lookup"><span data-stu-id="a442d-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
