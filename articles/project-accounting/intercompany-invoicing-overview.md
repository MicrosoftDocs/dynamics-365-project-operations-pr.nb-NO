---
title: Oversikt over konsernintern fakturering
description: Dette emnet gir informasjon og eksempler på konsernintern fakturering for prosjekter.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595523"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="30e9e-103">Oversikt over konsernintern fakturering</span><span class="sxs-lookup"><span data-stu-id="30e9e-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="30e9e-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="30e9e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="30e9e-105">Det kan hende at organisasjonen har flere divisjoner, datterselskaper og andre juridiske enheter som overfører produkter og servicer til hverandre for prosjekter.</span><span class="sxs-lookup"><span data-stu-id="30e9e-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="30e9e-106">Den juridiske enheten som tilbyr servicen eller produktet, kalles den *juridiske enheten som låner ut*.</span><span class="sxs-lookup"><span data-stu-id="30e9e-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="30e9e-107">Den juridiske enheten som mottar servicen eller produktet, kalles den *juridiske enheten som låner*.</span><span class="sxs-lookup"><span data-stu-id="30e9e-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="30e9e-108">Illustrasjonen nedenfor viser et typisk scenario der to juridiske enheter, Contoso Robotics USA (den juridiske enheten som låner) og Contoso Robotics UK (den juridiske enheten som låner ut) deler ressurser for å levere et prosjekt for kunden, Brusefoss industrier.</span><span class="sxs-lookup"><span data-stu-id="30e9e-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="30e9e-109">I dette scenarioet er Contoso Robotics USA kontraktert for å levere arbeidet til Brusefoss industrier.</span><span class="sxs-lookup"><span data-stu-id="30e9e-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Konsernintern fakturering](./media/IntercompanyScenario.png) 

<span data-ttu-id="30e9e-111">Dynamics 365 Project Operations bruker følgende flyt til å behandle konserninterne transaksjoner:</span><span class="sxs-lookup"><span data-stu-id="30e9e-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="30e9e-112">Ressurser fra den juridiske enheten som låner ut registrerer konsernintern tids- eller utgiftstransaksjoner ved å postere tid og utgifter opp mot prosjektet i den juridiske enheten som låner.</span><span class="sxs-lookup"><span data-stu-id="30e9e-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="30e9e-113">Tids- og utgiftskostnader registreres i utlånsfirmaet ved hjelp av prislisten over enhetskostnad til firmaet som låner.</span><span class="sxs-lookup"><span data-stu-id="30e9e-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="30e9e-114">Interkonserne ufakturerte salgstransaksjoner registreres i utlånsfirmaet ved hjelp av prislisten over enhetskostnaden til firmaet som låner.</span><span class="sxs-lookup"><span data-stu-id="30e9e-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="30e9e-115">Ufakturert inntekt registreres i firmaet som låner ved hjelp av salgsprislisten for prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="30e9e-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="30e9e-116">Kunden kan faktureres når ufakturert inntekt registreres.</span><span class="sxs-lookup"><span data-stu-id="30e9e-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="30e9e-117">Kunden trenger ikke å vente til konsernintern fakturabehandling er fullført.</span><span class="sxs-lookup"><span data-stu-id="30e9e-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="30e9e-118">Konserninterne kundefakturaer opprettes regelmessig i utlånsfirmaet.</span><span class="sxs-lookup"><span data-stu-id="30e9e-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="30e9e-119">Fakturaene opprettes manuelt eller ved hjelp av en periodisk automatisert prosess.</span><span class="sxs-lookup"><span data-stu-id="30e9e-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="30e9e-120">Én enkelt faktura kan opprettes for hver juridiske enhet som låner, eller separate fakturaer kan opprettes etter prosjekt.</span><span class="sxs-lookup"><span data-stu-id="30e9e-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="30e9e-121">Når den konserninterne kundefakturaen blir postert i den juridiske enheten som låner ut, opprettes den tilsvarende ventende leverandørfakturaen i den juridiske enheten som låner.</span><span class="sxs-lookup"><span data-stu-id="30e9e-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="30e9e-122">Kostnadene i den ventende leverandørfakturaen blir registrert i prosjektets underfinans når fakturaen er postert.</span><span class="sxs-lookup"><span data-stu-id="30e9e-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="30e9e-123">Følgende diagram illustrerer konsernintern fakturering som det relaterer til regnskapshendelser og forventede posteringer til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="30e9e-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Konsernintern flyt](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="30e9e-125">Ytterligere ressurser</span><span class="sxs-lookup"><span data-stu-id="30e9e-125">Additional resources</span></span>

- [<span data-ttu-id="30e9e-126">Konfigurere konsernintern fakturering</span><span class="sxs-lookup"><span data-stu-id="30e9e-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="30e9e-127">Registrere konserninterne transaksjoner</span><span class="sxs-lookup"><span data-stu-id="30e9e-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="30e9e-128">Opprette konserninterne kunde- og leverandørfakturaer</span><span class="sxs-lookup"><span data-stu-id="30e9e-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)
