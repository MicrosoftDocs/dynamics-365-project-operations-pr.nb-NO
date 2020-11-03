---
title: Opprette en manuell proformafaktura
description: Dette emnet gir informasjon om hvordan du oppretter en manuell proformafaktura i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2020
ms.locfileid: "4081849"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="be99d-103">Opprette en manuell proformafaktura</span><span class="sxs-lookup"><span data-stu-id="be99d-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="be99d-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="be99d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="be99d-105">I Dynamics 365 Project Operations kan proformafakturaer opprettes manuelt etter behov.</span><span class="sxs-lookup"><span data-stu-id="be99d-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="be99d-106">Du kan manuelt opprette en proformafaktura fra listesiden **Prosjektkontrakter** eller fra detaljsiden **Prosjektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="be99d-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="be99d-107">Listesiden Prosjektkontrakter</span><span class="sxs-lookup"><span data-stu-id="be99d-107">Project Contracts list page</span></span>

<span data-ttu-id="be99d-108">Fra listesiden **Prosjektkontrakter** velger du én eller flere prosjektkontrakter, og opprett deretter fakturaer for alle de valgte oppføringene.</span><span class="sxs-lookup"><span data-stu-id="be99d-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="be99d-109">Systemet kontrollerer hvilke av de valgte prosjektkontraktene som er har en **Klar for fakturering** -restanse datert før dagens dato.</span><span class="sxs-lookup"><span data-stu-id="be99d-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="be99d-110">Fra disse kontraktene oppretter systemet utkast til proformafakturaer.</span><span class="sxs-lookup"><span data-stu-id="be99d-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="be99d-111">Hvis en prosjektkontrakt har flere kunder, kan det hende at det opprettes én faktura per kunde og flere fakturaer per prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="be99d-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="be99d-112">Alle de opprettede prosjektfakturaene er tilgjengelige på **Faktura** -siden i **Fakturering** -delen i **Salg** -området.</span><span class="sxs-lookup"><span data-stu-id="be99d-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="be99d-113">Detaljsiden Prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="be99d-113">Project Contract details page</span></span>

<span data-ttu-id="be99d-114">En proforafaktura kan også opprettes fra detaljsiden **Prosjektkontrakt** , som oppretter fakturaen for den bestemte prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="be99d-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="be99d-115">Systemet verifiserer at prosjektkontrakten har en **Klar for fakturering** -restanse som er datert før dagens dato.</span><span class="sxs-lookup"><span data-stu-id="be99d-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="be99d-116">Fra disse kontraktene oppretter systemet utkast til proformafakturaer basert på antall kunder på hver kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="be99d-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="be99d-117">Når det er opprettet én enkelt proformafaktura, åpnes **Faktura** -siden.</span><span class="sxs-lookup"><span data-stu-id="be99d-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="be99d-118">Hvis det finnes flere fakturaer som er opprettet for den aktuelle prosjektkontrakten åpnes listesiden **Fakturaer** for å vise alle fakturaene som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="be99d-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
