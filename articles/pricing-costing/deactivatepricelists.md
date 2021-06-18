---
title: Deaktiver prislister
description: Dette emnet forklarer hvordan du deaktiverer eller fjerner ubrukte eller gamle prislister.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001348"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="6a53f-103">Deaktiver prislister</span><span class="sxs-lookup"><span data-stu-id="6a53f-103">Deactivate price lists</span></span> 

<span data-ttu-id="6a53f-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="6a53f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6a53f-105">Hvis du vil fjerne gamle eller ubrukte prislister fra Dynamics 365 Project Operations, er det to trinn du må fullføre.</span><span class="sxs-lookup"><span data-stu-id="6a53f-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="6a53f-106">Fjern eller slett prislisten fra bestemte sider.</span><span class="sxs-lookup"><span data-stu-id="6a53f-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="6a53f-107">Deaktiver eller slett prislisten fra de aktive prislistene på **Prislister**-siden.</span><span class="sxs-lookup"><span data-stu-id="6a53f-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="6a53f-108">Du må fullføre begge trinnene for å fjerne en prisliste fullstendig.</span><span class="sxs-lookup"><span data-stu-id="6a53f-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="6a53f-109">Bare å utføre trinn 2, som er å slette eller deaktivere prislisten direkte fra visningen Aktive prislister, er ikke tilstrekkelig.</span><span class="sxs-lookup"><span data-stu-id="6a53f-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="6a53f-110">Du må også slette tilknytningen til denne prislisten fra alle stedene nevnt i trinn 1.</span><span class="sxs-lookup"><span data-stu-id="6a53f-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="6a53f-111">Slett prislisten fra bestemte sider</span><span class="sxs-lookup"><span data-stu-id="6a53f-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="6a53f-112">Hvis du vil slette en prisliste fra Project Operations, går du til følgende sider:</span><span class="sxs-lookup"><span data-stu-id="6a53f-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="6a53f-113">**Prosjektparametere**-siden > **Prislister**-fanen</span><span class="sxs-lookup"><span data-stu-id="6a53f-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="6a53f-114">**Organisasjonsenhet**-siden > **Prislister**-rutenettet</span><span class="sxs-lookup"><span data-stu-id="6a53f-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="6a53f-115">**Konto**-siden > **Prosjektprislister**-rutenettet</span><span class="sxs-lookup"><span data-stu-id="6a53f-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="6a53f-116">**Prosjekttilbud**-siden > **Prosjektprislister**-rutenettet: Dette gjelder for alle aktive prosjekttilbud.</span><span class="sxs-lookup"><span data-stu-id="6a53f-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="6a53f-117">**Prosjektkontrakter**-siden > **Prosjektprislister**-rutenettet: Dette gjelder for alle aktive prosjektkontrakter.</span><span class="sxs-lookup"><span data-stu-id="6a53f-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="6a53f-118">For hver side må du velge prislisten du vil slette, og deretter velge **Slett**.</span><span class="sxs-lookup"><span data-stu-id="6a53f-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="6a53f-119">Slett eller deaktiver prislisten fra Prislister-siden</span><span class="sxs-lookup"><span data-stu-id="6a53f-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="6a53f-120">Hvis du vil slette en prisliste fra de aktive prislistene, går du til **Salg** > **Kunder** > **Prislister**.</span><span class="sxs-lookup"><span data-stu-id="6a53f-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="6a53f-121">Velg prislisten du vil slette, og velg deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="6a53f-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="6a53f-122">Hvis det refereres til prislisten for eksisterende transaksjoner, kan du ikke slette den.</span><span class="sxs-lookup"><span data-stu-id="6a53f-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="6a53f-123">Hvis dette skjer, kan du deaktivere prislisten slik at den ikke vises i noen visninger.</span><span class="sxs-lookup"><span data-stu-id="6a53f-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="6a53f-124">Hvis du vil deaktivere prislisten, velger du prislisten på nytt, og deretter velger du **Deaktiver**.</span><span class="sxs-lookup"><span data-stu-id="6a53f-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
