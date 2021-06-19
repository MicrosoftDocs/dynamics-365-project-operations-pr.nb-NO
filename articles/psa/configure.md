---
title: Konfigurere Project Service Automation
description: Fremgangsmåte for konfigurasjon av Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ef1724bb92e62ae21472e133fff0978c4faeeffa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002856"
---
# <a name="configure-project-service"></a><span data-ttu-id="c3c97-103">Konfigurere Project Service</span><span class="sxs-lookup"><span data-stu-id="c3c97-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c3c97-104">Før du kan bruke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-automatiseringsfunksjonene i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] til å administrere forretningsforbindelser, prosjekter og ressurser, må du fullføre noen konfigurasjonstrinn for å sikre at [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-løsningen samsvarer med organisasjonens behov.</span><span class="sxs-lookup"><span data-stu-id="c3c97-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="c3c97-105">Disse trinnene omfatter følgende:</span><span class="sxs-lookup"><span data-stu-id="c3c97-105">These steps include:</span></span>  
  
-   <span data-ttu-id="c3c97-106">[Definere tidsenheter](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="c3c97-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="c3c97-107">Konfigurer tidsenhetene i produktkatalogen som du vil bruke som grunnlag for planlegging og fakturering av prosjektene.</span><span class="sxs-lookup"><span data-stu-id="c3c97-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="c3c97-108">[Sette opp valutaer og valutakurser](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="c3c97-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="c3c97-109">Definer valutaene som skal brukes for prosjektene.</span><span class="sxs-lookup"><span data-stu-id="c3c97-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="c3c97-110">[Opprette organisasjonsenheter](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="c3c97-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="c3c97-111">Definer gruppene som firmaet bruker til å dele inn virksomheten, etter geografi, forretningsfunksjon eller andre logiske inndelinger.</span><span class="sxs-lookup"><span data-stu-id="c3c97-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="c3c97-112">[Sette opp fakturafrekvenser](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="c3c97-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="c3c97-113">Definer tidsperioder som du vil bruke for å fakturere kundene.</span><span class="sxs-lookup"><span data-stu-id="c3c97-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="c3c97-114">[Konfigurere transaksjonskategorier](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="c3c97-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="c3c97-115">Angi transaksjonskategorier som konsulentenes fakturerbare og ikke-fakturerbare utgifter kan belastes.</span><span class="sxs-lookup"><span data-stu-id="c3c97-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="c3c97-116">[Konfigurere utgiftskategorier](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="c3c97-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="c3c97-117">Angi kategoriene som konsulentenes fakturerbare og ikke-fakturerbare utgifter kan belastes.</span><span class="sxs-lookup"><span data-stu-id="c3c97-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="c3c97-118">[Opprette produktkatalogelementer](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="c3c97-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="c3c97-119">Legg til produktene du selger, for eksempel programvarelisenser, i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="c3c97-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="c3c97-120">[Opprette en prisliste](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="c3c97-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="c3c97-121">Konfigurer forskjellige prislister, avhengig av hvor mye du vil belaste kundene for hver rolle som prosjektet deres krever.</span><span class="sxs-lookup"><span data-stu-id="c3c97-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="c3c97-122">[Definere ressurser](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="c3c97-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="c3c97-123">Legg til ferdigheter, kompetanse, ressursroller og annen ressursinformasjon som du trenger i prosjektene.</span><span class="sxs-lookup"><span data-stu-id="c3c97-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c3c97-124">Se også</span><span class="sxs-lookup"><span data-stu-id="c3c97-124">See Also</span></span>  
 <span data-ttu-id="c3c97-125">[Oversikt over Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="c3c97-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="c3c97-126">[Konfigurere Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="c3c97-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="c3c97-127">[Veiledning for kontoadministrator](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="c3c97-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="c3c97-128">[Prosjektlederhåndbok](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="c3c97-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="c3c97-129">[Håndbok for ressursansvarlig](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="c3c97-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="c3c97-130">Håndbok for tid, utgifter og samarbeid</span><span class="sxs-lookup"><span data-stu-id="c3c97-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]