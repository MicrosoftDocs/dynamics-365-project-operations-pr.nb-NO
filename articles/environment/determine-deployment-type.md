---
title: Fastslå distribusjonstypen
description: Dette emnet gir informasjon som hjelper deg med å bestemme riktig distribusjonstype for prosjektoperasjoner for firmaet ditt.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401230"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="91c8b-103">Fastslå distribusjonstypen</span><span class="sxs-lookup"><span data-stu-id="91c8b-103">Determine your deployment type</span></span>

<span data-ttu-id="91c8b-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="91c8b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91c8b-105">Når du har kjøpt lisensen, starter du her for å finne den beste distribusjonsmodellen for Dynamics 365 Project Operations ved å bruke den [veiledede installasjonsflyten](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="91c8b-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="91c8b-106">Når du har fullført den veiledede installasjonsflyten, blir du dirigert til riktig administrasjonsportal for å fullføre installasjonen.</span><span class="sxs-lookup"><span data-stu-id="91c8b-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="91c8b-107">Se distribusjonsdetaljene for å fullføre installasjonen.</span><span class="sxs-lookup"><span data-stu-id="91c8b-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="91c8b-108">Eksisterende kunder av Dynamics som bruker Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="91c8b-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="91c8b-109">Prosjekt Operations inkluderer funksjonene som leveres med Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="91c8b-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="91c8b-110">En oppgraderingsbane blir utgitt for disse kundene i 2021-lanseringsbølge 1.</span><span class="sxs-lookup"><span data-stu-id="91c8b-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="91c8b-111">Eksisterende kunder av Dynamics 365 Finance som bruker prosjektstyring og regnskap</span><span class="sxs-lookup"><span data-stu-id="91c8b-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="91c8b-112">Eksisterende kunder av Finance som bruker Prosjektstyring og regnskap-funksjonaliteten, kan fortsette å bruke den som den er.</span><span class="sxs-lookup"><span data-stu-id="91c8b-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="91c8b-113">Se [Project Operations for lagerførte scenarioer / produksjonsordrescenarioer](#pma).</span><span class="sxs-lookup"><span data-stu-id="91c8b-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="91c8b-114">Distribusjonstyper</span><span class="sxs-lookup"><span data-stu-id="91c8b-114">Deployment types</span></span>
<span data-ttu-id="91c8b-115">Project Operations støtter flere distribusjonsalternativer for å dekke dine behov.</span><span class="sxs-lookup"><span data-stu-id="91c8b-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="91c8b-116">Enten du er en ny eller eksisterende Dynamics 365-kunde, kan Project Operations støtte dine behov.</span><span class="sxs-lookup"><span data-stu-id="91c8b-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="91c8b-117">[Spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations) hjelper deg med å finne riktig distribusjon.</span><span class="sxs-lookup"><span data-stu-id="91c8b-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="91c8b-118">Resultatene leder deg mot én av følgende distribusjonstyper:</span><span class="sxs-lookup"><span data-stu-id="91c8b-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="91c8b-119">Lite-distribusjon – avtale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="91c8b-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="91c8b-120">Project Operations for ressursbaserte/ikke-lagerførte scenarioer</span><span class="sxs-lookup"><span data-stu-id="91c8b-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="91c8b-121">Project Operations for lagerførte scenarioer / produksjonsordrescenarioer</span><span class="sxs-lookup"><span data-stu-id="91c8b-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="91c8b-122">Project Operations støtter lagerførte scenarioer / produksjonsordrescenarioer og ordre scenarioer og ikke-lagerbaserte/ressursbaserte scenarioer i samme miljø ved hjelp av konfigurasjoner på juridisk enhetsnivå.</span><span class="sxs-lookup"><span data-stu-id="91c8b-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="91c8b-123">Contoso kan for eksempel bruke funksjonene for lagerført/produksjonsordre på produksjonsanlegget i USA (juridisk enhet = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="91c8b-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="91c8b-124">Contoso bruke funksjonene for ikke-lagerflrt/ressursbasert i Contoso Robotics Arms serviceanlegget i UK (juridisk enhet = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="91c8b-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="91c8b-125">Lite-distribusjon – avtale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="91c8b-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="91c8b-126">Lite-distribusjonen omfatter følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="91c8b-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="91c8b-127">Salgsprosess for prosjekter som utvider Dynamics 365 Sales-programerfaringer</span><span class="sxs-lookup"><span data-stu-id="91c8b-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="91c8b-128">Prosjektplanlegging ved hjelp av Microsoft Project for Internett</span><span class="sxs-lookup"><span data-stu-id="91c8b-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="91c8b-129">Flerdimensjonal prising</span><span class="sxs-lookup"><span data-stu-id="91c8b-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="91c8b-130">Enhetlig ressursstyring</span><span class="sxs-lookup"><span data-stu-id="91c8b-130">Unified resource management</span></span>
- <span data-ttu-id="91c8b-131">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="91c8b-131">Time tracking</span></span>
- <span data-ttu-id="91c8b-132">Grunnleggende utgift</span><span class="sxs-lookup"><span data-stu-id="91c8b-132">Basic expense</span></span>
- <span data-ttu-id="91c8b-133">Proforma og kunderettet fakturering</span><span class="sxs-lookup"><span data-stu-id="91c8b-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="91c8b-134">Trinn for distribusjon</span><span class="sxs-lookup"><span data-stu-id="91c8b-134">Deployment steps</span></span>
<span data-ttu-id="91c8b-135">Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="91c8b-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="91c8b-136">For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](lite-preview-subscription-sign-up.md) og [Klargjøre nytt miljø](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="91c8b-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="91c8b-137">Project Operations for ressursbaserte/ikke-lagerførte scenarioer</span><span class="sxs-lookup"><span data-stu-id="91c8b-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="91c8b-138">Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer inkluderer følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="91c8b-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="91c8b-139">Salgsprosess for prosjekter som utvider Dynamics 365 Sales-programmet</span><span class="sxs-lookup"><span data-stu-id="91c8b-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="91c8b-140">Prosjektplanlegging ved hjelp av Microsoft Project for Internett</span><span class="sxs-lookup"><span data-stu-id="91c8b-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="91c8b-141">Flerdimensjonal prising</span><span class="sxs-lookup"><span data-stu-id="91c8b-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="91c8b-142">Enhetlig ressursstyring</span><span class="sxs-lookup"><span data-stu-id="91c8b-142">Unified resource management</span></span>
- <span data-ttu-id="91c8b-143">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="91c8b-143">Time tracking</span></span>
- <span data-ttu-id="91c8b-144">Grunnleggende utgift</span><span class="sxs-lookup"><span data-stu-id="91c8b-144">Basic expense</span></span>
- <span data-ttu-id="91c8b-145">Fullstendig utgift</span><span class="sxs-lookup"><span data-stu-id="91c8b-145">Full expense</span></span>
- <span data-ttu-id="91c8b-146">Mottak av OCR</span><span class="sxs-lookup"><span data-stu-id="91c8b-146">Receipt OCR</span></span>
- <span data-ttu-id="91c8b-147">Proforma og kunderettet fakturering</span><span class="sxs-lookup"><span data-stu-id="91c8b-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="91c8b-148">Inntektsføring for prosjekter</span><span class="sxs-lookup"><span data-stu-id="91c8b-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="91c8b-149">Trinn for distribusjon</span><span class="sxs-lookup"><span data-stu-id="91c8b-149">Deployment steps</span></span>
<span data-ttu-id="91c8b-150">Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="91c8b-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="91c8b-151">For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](resource-sign-up-preview-subscription.md) og [Klargjøre nytt miljø](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="91c8b-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="91c8b-152">Project Operations for lagerførte scenarioer / produksjonsordrescenarioer</span><span class="sxs-lookup"><span data-stu-id="91c8b-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="91c8b-153">Prosjektplanlegging ved hjelp av WBS</span><span class="sxs-lookup"><span data-stu-id="91c8b-153">Project planning using WBS</span></span>
- <span data-ttu-id="91c8b-154">Ressursbehandling</span><span class="sxs-lookup"><span data-stu-id="91c8b-154">Resource Management</span></span>
- <span data-ttu-id="91c8b-155">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="91c8b-155">Time Tracking</span></span>
- <span data-ttu-id="91c8b-156">Fullstendig utgift</span><span class="sxs-lookup"><span data-stu-id="91c8b-156">Full Expense</span></span>
- <span data-ttu-id="91c8b-157">Mottak av OCR</span><span class="sxs-lookup"><span data-stu-id="91c8b-157">Receipt OCR</span></span>
- <span data-ttu-id="91c8b-158">Full fakturering</span><span class="sxs-lookup"><span data-stu-id="91c8b-158">Full Invoicing</span></span>
- <span data-ttu-id="91c8b-159">Inntektsføring</span><span class="sxs-lookup"><span data-stu-id="91c8b-159">Revenue Recognition</span></span>
- <span data-ttu-id="91c8b-160">Produksjonsordrer</span><span class="sxs-lookup"><span data-stu-id="91c8b-160">Production Orders</span></span>
- <span data-ttu-id="91c8b-161">Støtte for materiell</span><span class="sxs-lookup"><span data-stu-id="91c8b-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="91c8b-162">Trinn for distribusjon</span><span class="sxs-lookup"><span data-stu-id="91c8b-162">Deployment steps</span></span>
<span data-ttu-id="91c8b-163">Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="91c8b-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="91c8b-164">For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) og [Klargjøre nytt miljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="91c8b-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

