---
title: Opprette en manuell proformafaktura – Lite
description: Dette emnet gir informasjon om hvordan du oppretter en manuell proformafaktura i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274200"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="99fdd-103">Opprette en manuell proformafaktura – Lite</span><span class="sxs-lookup"><span data-stu-id="99fdd-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="99fdd-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="99fdd-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="99fdd-105">I Dynamics 365 Project Operations kan proformafakturaer opprettes manuelt etter behov.</span><span class="sxs-lookup"><span data-stu-id="99fdd-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="99fdd-106">Du kan manuelt opprette en proformafaktura fra listesiden **Prosjektkontrakter** eller fra detaljsiden **Prosjektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="99fdd-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="99fdd-107">Listesiden Prosjektkontrakter</span><span class="sxs-lookup"><span data-stu-id="99fdd-107">Project Contracts list page</span></span>

<span data-ttu-id="99fdd-108">Fra listesiden **Prosjektkontrakter** velger du én eller flere prosjektkontrakter, og opprett deretter fakturaer for alle de valgte oppføringene.</span><span class="sxs-lookup"><span data-stu-id="99fdd-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="99fdd-109">Systemet kontrollerer hvilke av de valgte prosjektkontraktene som er har en **Klar for fakturering**-restanse datert før dagens dato.</span><span class="sxs-lookup"><span data-stu-id="99fdd-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="99fdd-110">Fra disse kontraktene oppretter systemet utkast til proformafakturaer.</span><span class="sxs-lookup"><span data-stu-id="99fdd-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="99fdd-111">Hvis en prosjektkontrakt har flere kunder, kan det hende at det opprettes én faktura per kunde og flere fakturaer per prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="99fdd-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="99fdd-112">Alle de opprettede prosjektfakturaene er tilgjengelige på **Faktura**-siden i **Fakturering**-delen i **Salg**-området.</span><span class="sxs-lookup"><span data-stu-id="99fdd-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="99fdd-113">Detaljsiden Prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="99fdd-113">Project Contract details page</span></span>

<span data-ttu-id="99fdd-114">En proformafaktura kan også opprettes fra detaljsiden **Prosjektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="99fdd-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="99fdd-115">Systemet verifiserer at prosjektkontrakten har en **Klar for fakturering**-restanse datert før dagens dato.</span><span class="sxs-lookup"><span data-stu-id="99fdd-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="99fdd-116">Fra disse kontraktene oppretter systemet utkast til proformafakturaer basert på antall kunder på hver kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="99fdd-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="99fdd-117">Når det er opprettet én enkelt proformafaktura, åpnes **Faktura**-siden.</span><span class="sxs-lookup"><span data-stu-id="99fdd-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="99fdd-118">Hvis det opprettes flere fakturaer for den prosjektkontrakten, åpnes listesiden **Fakturaer** for å vise alle opprettede fakturaer.</span><span class="sxs-lookup"><span data-stu-id="99fdd-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]