---
title: Konfigurere Project Service Automation
description: Fremgangsmåte for konfigurasjon av Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754099"
---
# <a name="configure-project-service"></a><span data-ttu-id="1d537-103">Konfigurere Project Service</span><span class="sxs-lookup"><span data-stu-id="1d537-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1d537-104">Før du kan bruke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-automatiseringsfunksjonene i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] til å administrere forretningsforbindelser, prosjekter og ressurser, må du fullføre noen konfigurasjonstrinn for å sikre at [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-løsningen samsvarer med organisasjonens behov.</span><span class="sxs-lookup"><span data-stu-id="1d537-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="1d537-105">Disse trinnene omfatter følgende:</span><span class="sxs-lookup"><span data-stu-id="1d537-105">These steps include:</span></span>  
  
-   <span data-ttu-id="1d537-106">[Definere tidsenheter](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="1d537-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="1d537-107">Konfigurer tidsenhetene i produktkatalogen som du vil bruke som grunnlag for planlegging og fakturering av prosjektene.</span><span class="sxs-lookup"><span data-stu-id="1d537-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="1d537-108">[Sette opp valutaer og valutakurser](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="1d537-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="1d537-109">Definer valutaene som skal brukes for prosjektene.</span><span class="sxs-lookup"><span data-stu-id="1d537-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="1d537-110">[Opprette organisasjonsenheter](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="1d537-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="1d537-111">Definer gruppene som firmaet bruker til å dele inn virksomheten, etter geografi, forretningsfunksjon eller andre logiske inndelinger.</span><span class="sxs-lookup"><span data-stu-id="1d537-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="1d537-112">[Sette opp fakturafrekvenser](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="1d537-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="1d537-113">Definer tidsperioder som du vil bruke for å fakturere kundene.</span><span class="sxs-lookup"><span data-stu-id="1d537-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="1d537-114">[Konfigurere transaksjonskategorier](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="1d537-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="1d537-115">Angi transaksjonskategorier som konsulentenes fakturerbare og ikke-fakturerbare utgifter kan belastes.</span><span class="sxs-lookup"><span data-stu-id="1d537-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="1d537-116">[Konfigurere utgiftskategorier](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="1d537-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="1d537-117">Angi kategoriene som konsulentenes fakturerbare og ikke-fakturerbare utgifter kan belastes.</span><span class="sxs-lookup"><span data-stu-id="1d537-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="1d537-118">[Opprette produktkatalogelementer](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="1d537-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="1d537-119">Legg til produktene du selger, for eksempel programvarelisenser, i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="1d537-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="1d537-120">[Opprette en prisliste](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="1d537-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="1d537-121">Konfigurer forskjellige prislister, avhengig av hvor mye du vil belaste kundene for hver rolle som prosjektet deres krever.</span><span class="sxs-lookup"><span data-stu-id="1d537-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="1d537-122">[Definere ressurser](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="1d537-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="1d537-123">Legg til ferdigheter, kompetanse, ressursroller og annen ressursinformasjon som du trenger i prosjektene.</span><span class="sxs-lookup"><span data-stu-id="1d537-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1d537-124">Se også</span><span class="sxs-lookup"><span data-stu-id="1d537-124">See Also</span></span>  
 <span data-ttu-id="1d537-125">[Oversikt over Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="1d537-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="1d537-126">[Konfigurere Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="1d537-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="1d537-127">[Veiledning for kontoadministrator](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="1d537-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="1d537-128">[Prosjektlederhåndbok](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="1d537-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="1d537-129">[Håndbok for ressursansvarlig](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="1d537-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="1d537-130">Håndbok for tid, utgifter og samarbeid</span><span class="sxs-lookup"><span data-stu-id="1d537-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
