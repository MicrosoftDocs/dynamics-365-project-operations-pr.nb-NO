---
title: Fastslå distribusjonstypen
description: Dette emnet gir informasjon som hjelper deg med å bestemme riktig distribusjonstype for prosjektoperasjoner for firmaet ditt.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081624"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="12c26-103">Fastslå distribusjonstypen</span><span class="sxs-lookup"><span data-stu-id="12c26-103">Determine your deployment type</span></span>

<span data-ttu-id="12c26-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="12c26-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12c26-105">Når du har kjøpt lisensen, starter du her for å finne den beste distribusjonsmodellen for Dynamics 365 Project Operations ved å bruke den [veiledede installasjonsflyten](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="12c26-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="12c26-106">Når du har fullført den veiledede installasjonsflyten, blir du dirigert til riktig administrasjonsportal for å fullføre installasjonen.</span><span class="sxs-lookup"><span data-stu-id="12c26-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="12c26-107">Se distribusjonsdetaljene for å fullføre installasjonen.</span><span class="sxs-lookup"><span data-stu-id="12c26-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="12c26-108">Eksisterende kunder av Dynamics som bruker Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="12c26-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="12c26-109">Prosjekt Operations inkluderer funksjonene som leveres med Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="12c26-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="12c26-110">En oppgraderingsbane blir utgitt for disse kundene i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="12c26-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="12c26-111">Eksisterende kunder av Dynamics 365 Finance som bruker prosjektstyring og regnskap</span><span class="sxs-lookup"><span data-stu-id="12c26-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="12c26-112">Eksisterende kunder av Finance som bruker prosjektstyrings og regnskap, kan fortsette å bruke dette som de er.</span><span class="sxs-lookup"><span data-stu-id="12c26-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="12c26-113">Se [Project Operations for lagerførte scenarioer / produksjonsordrescenarioer](#pma).</span><span class="sxs-lookup"><span data-stu-id="12c26-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="12c26-114">Distribusjonstyper</span><span class="sxs-lookup"><span data-stu-id="12c26-114">Deployment types</span></span>
<span data-ttu-id="12c26-115">Project Operations støtter flere distribusjonsalternativer for å dekke dine behov.</span><span class="sxs-lookup"><span data-stu-id="12c26-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="12c26-116">Enten du er en ny eller eksisterende Dynamics 365-kunde, kan Project Operations støtte dine behov.</span><span class="sxs-lookup"><span data-stu-id="12c26-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="12c26-117">[Spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations) hjelper deg med å finne riktig distribusjon.</span><span class="sxs-lookup"><span data-stu-id="12c26-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="12c26-118">Resultatene leder deg mot én av følgende distribusjonstyper:</span><span class="sxs-lookup"><span data-stu-id="12c26-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="12c26-119">Lite-distribusjon – avtale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="12c26-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="12c26-120">Project Operations for ressursbaserte/ikke-lagerførte scenarioer</span><span class="sxs-lookup"><span data-stu-id="12c26-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="12c26-121">Project Operations for lagerførte scenarioer / produksjonsordrescenarioer</span><span class="sxs-lookup"><span data-stu-id="12c26-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="12c26-122">Project Operations støtter lagerførte scenarioer / produksjonsordrescenarioer og ordre scenarioer og ikke-lagerbaserte/ressursbaserte scenarioer i samme miljø ved hjelp av konfigurasjoner på juridisk enhetsnivå.</span><span class="sxs-lookup"><span data-stu-id="12c26-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="12c26-123">Contoso kan for eksempel bruke funksjonene for lagerført/produksjonsordre på produksjonsanlegget i USA (juridisk enhet = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="12c26-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="12c26-124">Contoso bruke funksjonene for ikke-lagerflrt/ressursbasert i Contoso Robotics Arms serviceanlegget i UK (juridisk enhet = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="12c26-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="12c26-125">Lite-distribusjon – avtale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="12c26-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="12c26-126">Lite-distribusjonen omfatter følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="12c26-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="12c26-127">Prosjektplanlegging ved hjelp av Microsoft Project for Internett</span><span class="sxs-lookup"><span data-stu-id="12c26-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="12c26-128">Flerdimensjonal prising</span><span class="sxs-lookup"><span data-stu-id="12c26-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="12c26-129">Enhetlig ressursstyring</span><span class="sxs-lookup"><span data-stu-id="12c26-129">Unified Resource Management</span></span>
- <span data-ttu-id="12c26-130">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="12c26-130">Time Tracking</span></span>
- <span data-ttu-id="12c26-131">Grunnleggende utgift</span><span class="sxs-lookup"><span data-stu-id="12c26-131">Basic Expense</span></span>
- <span data-ttu-id="12c26-132">Fakturaforslag</span><span class="sxs-lookup"><span data-stu-id="12c26-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="12c26-133">Trinn for distribusjon</span><span class="sxs-lookup"><span data-stu-id="12c26-133">Deployment steps</span></span>
<span data-ttu-id="12c26-134">Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="12c26-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="12c26-135">For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](lite-preview-subscription-sign-up.md) og [Klargjøre nytt miljø](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="12c26-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="12c26-136">Project Operations for ressursbaserte/ikke-lagerførte scenarioer</span><span class="sxs-lookup"><span data-stu-id="12c26-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="12c26-137">Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer inkluderer følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="12c26-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="12c26-138">Prosjektplanlegging ved hjelp av Microsoft Project for Internett</span><span class="sxs-lookup"><span data-stu-id="12c26-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="12c26-139">Flerdimensjonal prising</span><span class="sxs-lookup"><span data-stu-id="12c26-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="12c26-140">Enhetlig ressursstyring</span><span class="sxs-lookup"><span data-stu-id="12c26-140">Unified Resource Management</span></span>
- <span data-ttu-id="12c26-141">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="12c26-141">Time Tracking</span></span>
- <span data-ttu-id="12c26-142">Grunnleggende utgift</span><span class="sxs-lookup"><span data-stu-id="12c26-142">Basic Expense</span></span>
- <span data-ttu-id="12c26-143">Fullstendig utgift</span><span class="sxs-lookup"><span data-stu-id="12c26-143">Full Expense</span></span>
- <span data-ttu-id="12c26-144">Mottak av OCR</span><span class="sxs-lookup"><span data-stu-id="12c26-144">Receipt OCR</span></span>
- <span data-ttu-id="12c26-145">Full fakturering</span><span class="sxs-lookup"><span data-stu-id="12c26-145">Full Invoicing</span></span>
- <span data-ttu-id="12c26-146">Inntektsføring</span><span class="sxs-lookup"><span data-stu-id="12c26-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="12c26-147">Trinn for distribusjon</span><span class="sxs-lookup"><span data-stu-id="12c26-147">Deployment steps</span></span>
<span data-ttu-id="12c26-148">Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="12c26-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="12c26-149">For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](resource-sign-up-preview-subscription.md) og [Klargjøre nytt miljø](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="12c26-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="12c26-150">Project Operations for lagerførte scenarioer / produksjonsordrescenarioer</span><span class="sxs-lookup"><span data-stu-id="12c26-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="12c26-151">Prosjektplanlegging ved hjelp av WBS</span><span class="sxs-lookup"><span data-stu-id="12c26-151">Project planning using WBS</span></span>
- <span data-ttu-id="12c26-152">Ressursbehandling</span><span class="sxs-lookup"><span data-stu-id="12c26-152">Resource Management</span></span>
- <span data-ttu-id="12c26-153">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="12c26-153">Time Tracking</span></span>
- <span data-ttu-id="12c26-154">Fullstendig utgift</span><span class="sxs-lookup"><span data-stu-id="12c26-154">Full Expense</span></span>
- <span data-ttu-id="12c26-155">Mottak av OCR</span><span class="sxs-lookup"><span data-stu-id="12c26-155">Receipt OCR</span></span>
- <span data-ttu-id="12c26-156">Full fakturering</span><span class="sxs-lookup"><span data-stu-id="12c26-156">Full Invoicing</span></span>
- <span data-ttu-id="12c26-157">Inntektsføring</span><span class="sxs-lookup"><span data-stu-id="12c26-157">Revenue Recognition</span></span>
- <span data-ttu-id="12c26-158">Produksjonsordrer</span><span class="sxs-lookup"><span data-stu-id="12c26-158">Production Orders</span></span>
- <span data-ttu-id="12c26-159">Støtte for materiell</span><span class="sxs-lookup"><span data-stu-id="12c26-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="12c26-160">Trinn for distribusjon</span><span class="sxs-lookup"><span data-stu-id="12c26-160">Deployment steps</span></span>
<span data-ttu-id="12c26-161">Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="12c26-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="12c26-162">For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) og [Klargjøre nytt miljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="12c26-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

