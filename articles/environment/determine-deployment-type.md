---
title: Distribusjonstyper
description: Dette emnet gir informasjon som hjelper deg med å bestemme riktig distribusjonstype for prosjektoperasjoner for firmaet ditt.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948998"
---
# <a name="deployment-types"></a><span data-ttu-id="2b767-103">Distribusjonstyper</span><span class="sxs-lookup"><span data-stu-id="2b767-103">Deployment types</span></span>

<span data-ttu-id="2b767-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="2b767-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b767-105">Når du har kjøpt lisensen, starter du her for å finne den beste distribusjonsmodellen for Dynamics 365 Project Operations ved å bruke den [veiledede installasjonsflyten](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="2b767-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="2b767-106">Når du har fullført den veiledede installasjonsflyten, blir du dirigert til riktig administrasjonsportal for å fullføre installasjonen.</span><span class="sxs-lookup"><span data-stu-id="2b767-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="2b767-107">Se distribusjonsdetaljene nedenfor for å fullføre installasjonen.</span><span class="sxs-lookup"><span data-stu-id="2b767-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="2b767-108">Eksisterende kunder av Dynamics som bruker Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2b767-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="2b767-109">Prosjekt Operations inkluderer funksjonene som leveres med Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2b767-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="2b767-110">En oppgraderingsbane blir utgitt for disse kundene i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="2b767-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="2b767-111">Eksisterende kunder av Dynamics 365 Finance som bruker prosjektstyring og regnskap</span><span class="sxs-lookup"><span data-stu-id="2b767-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="2b767-112">Eksisterende kunder av Finance som bruker prosjektstyrings og regnskap, kan fortsette å bruke dette som de er.</span><span class="sxs-lookup"><span data-stu-id="2b767-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="2b767-113">Se [Project Operations for lagerførte scenarioer / produksjonsordrescenarioer](#pma).</span><span class="sxs-lookup"><span data-stu-id="2b767-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="2b767-114">Project Operations støtter flere distribusjonsalternativer for å dekke dine behov.</span><span class="sxs-lookup"><span data-stu-id="2b767-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="2b767-115">Enten du er en ny eller eksisterende Dynamics 365-kunde, kan Project Operations støtte dine behov.</span><span class="sxs-lookup"><span data-stu-id="2b767-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="2b767-116">[Spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations) hjelper deg med å finne riktig distribusjon.</span><span class="sxs-lookup"><span data-stu-id="2b767-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="2b767-117">Resultatene leder deg mot én av følgende distribusjonstyper:</span><span class="sxs-lookup"><span data-stu-id="2b767-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="2b767-118">Lite-distribusjon – avtale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="2b767-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="2b767-119">Project Operations for ressursbaserte/ikke-lagerførte scenarioer</span><span class="sxs-lookup"><span data-stu-id="2b767-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="2b767-120">Project Operations for lagerførte scenarioer / produksjonsordrescenarioer</span><span class="sxs-lookup"><span data-stu-id="2b767-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="2b767-121">Project Operations støtter lagerførte scenarioer / produksjonsordrescenarioer og ordre scenarioer og ikke-lagerbaserte/ressursbaserte scenarioer i samme miljø ved hjelp av konfigurasjoner på juridisk enhetsnivå.</span><span class="sxs-lookup"><span data-stu-id="2b767-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="2b767-122">Contoso kan for eksempel dra nytte av funksjoner for lagerbasert/produksjonsordre i amerikanske produksjonsanlegg (juridisk enhet = Contoso Manufacturing United States), og ikke-lagerbaserte/ressursbaserte funksjoner i Contoso Robotics Arms vedlikeholdsanlegg i Storbritannia (juridisk enhet = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="2b767-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="2b767-123"><a name="lite"><a/>Lite-distribusjon – avtale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="2b767-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="2b767-124">Lite-distribusjonen omfatter følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="2b767-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="2b767-125">Prosjektplanlegging ved hjelp av Microsoft Project for Internett</span><span class="sxs-lookup"><span data-stu-id="2b767-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="2b767-126">Flerdimensjonal prising</span><span class="sxs-lookup"><span data-stu-id="2b767-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="2b767-127">Enhetlig ressursstyring</span><span class="sxs-lookup"><span data-stu-id="2b767-127">Unified Resource Management</span></span>
- <span data-ttu-id="2b767-128">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="2b767-128">Time Tracking</span></span>
- <span data-ttu-id="2b767-129">Grunnleggende utgift</span><span class="sxs-lookup"><span data-stu-id="2b767-129">Basic Expense</span></span>
- <span data-ttu-id="2b767-130">Fakturaforslag</span><span class="sxs-lookup"><span data-stu-id="2b767-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="2b767-131">Distribusjonstrinn:</span><span class="sxs-lookup"><span data-stu-id="2b767-131">Deployment steps:</span></span>
<span data-ttu-id="2b767-132">Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="2b767-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="2b767-133">For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](lite-preview-subscription-sign-up.md) og [Klargjøre nytt miljø](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="2b767-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="2b767-134"><a name="integrated"><a/>Project Operations for ressursbaserte/ikke-lagerførte scenarioer</span><span class="sxs-lookup"><span data-stu-id="2b767-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="2b767-135">Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer inkluderer følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="2b767-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="2b767-136">Prosjektplanlegging ved hjelp av Microsoft Project for Internett</span><span class="sxs-lookup"><span data-stu-id="2b767-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="2b767-137">Flerdimensjonal prising</span><span class="sxs-lookup"><span data-stu-id="2b767-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="2b767-138">Enhetlig ressursstyring</span><span class="sxs-lookup"><span data-stu-id="2b767-138">Unified Resource Management</span></span>
- <span data-ttu-id="2b767-139">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="2b767-139">Time Tracking</span></span>
- <span data-ttu-id="2b767-140">Grunnleggende utgift</span><span class="sxs-lookup"><span data-stu-id="2b767-140">Basic Expense</span></span>
- <span data-ttu-id="2b767-141">Fullstendig utgift</span><span class="sxs-lookup"><span data-stu-id="2b767-141">Full Expense</span></span>
- <span data-ttu-id="2b767-142">Mottak av OCR</span><span class="sxs-lookup"><span data-stu-id="2b767-142">Receipt OCR</span></span>
- <span data-ttu-id="2b767-143">Full fakturering</span><span class="sxs-lookup"><span data-stu-id="2b767-143">Full Invoicing</span></span>
- <span data-ttu-id="2b767-144">Inntektsføring</span><span class="sxs-lookup"><span data-stu-id="2b767-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="2b767-145">Distribusjonstrinn:</span><span class="sxs-lookup"><span data-stu-id="2b767-145">Deployment steps:</span></span>
<span data-ttu-id="2b767-146">Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="2b767-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="2b767-147">For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](resource-sign-up-preview-subscription.md) og [Klargjøre nytt miljø](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2b767-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="2b767-148">Project Operations for lagerførte scenarioer / produksjonsordrescenarioer</span><span class="sxs-lookup"><span data-stu-id="2b767-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="2b767-149">Prosjektplanlegging ved hjelp av WBS</span><span class="sxs-lookup"><span data-stu-id="2b767-149">Project planning using WBS</span></span>
- <span data-ttu-id="2b767-150">Ressursbehandling</span><span class="sxs-lookup"><span data-stu-id="2b767-150">Resource Management</span></span>
- <span data-ttu-id="2b767-151">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="2b767-151">Time Tracking</span></span>
- <span data-ttu-id="2b767-152">Fullstendig utgift</span><span class="sxs-lookup"><span data-stu-id="2b767-152">Full Expense</span></span>
- <span data-ttu-id="2b767-153">Mottak av OCR</span><span class="sxs-lookup"><span data-stu-id="2b767-153">Receipt OCR</span></span>
- <span data-ttu-id="2b767-154">Full fakturering</span><span class="sxs-lookup"><span data-stu-id="2b767-154">Full Invoicing</span></span>
- <span data-ttu-id="2b767-155">Inntektsføring</span><span class="sxs-lookup"><span data-stu-id="2b767-155">Revenue Recognition</span></span>
- <span data-ttu-id="2b767-156">Produksjonsordrer</span><span class="sxs-lookup"><span data-stu-id="2b767-156">Production Orders</span></span>
- <span data-ttu-id="2b767-157">Støtte for materiell</span><span class="sxs-lookup"><span data-stu-id="2b767-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="2b767-158">Distribusjonstrinn:</span><span class="sxs-lookup"><span data-stu-id="2b767-158">Deployment steps:</span></span>
<span data-ttu-id="2b767-159">Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="2b767-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="2b767-160">For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) og [Klargjøre nytt miljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2b767-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



