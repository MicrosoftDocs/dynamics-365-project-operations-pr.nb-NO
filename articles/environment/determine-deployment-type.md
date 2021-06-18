---
title: Fastslå distribusjonstypen
description: Dette emnet gir informasjon som hjelper deg med å bestemme riktig distribusjonstype for prosjektoperasjoner for firmaet ditt.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ad700a84edd6c39609bc5b4f09ca74af3059a0dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997118"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="96042-103">Fastslå distribusjonstypen</span><span class="sxs-lookup"><span data-stu-id="96042-103">Determine your deployment type</span></span>

<span data-ttu-id="96042-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="96042-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="96042-105">Når du har kjøpt lisensen, starter du her for å finne den beste distribusjonsmodellen for Dynamics 365 Project Operations ved å bruke [flyten for veiledet installasjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="96042-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="96042-106">Når du har fullført den veiledede installasjonsflyten, blir du dirigert til riktig administrasjonsportal for å fullføre installasjonen.</span><span class="sxs-lookup"><span data-stu-id="96042-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="96042-107">Se distribusjonsdetaljene for å fullføre installasjonen.</span><span class="sxs-lookup"><span data-stu-id="96042-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="96042-108">Eksisterende kunder av Dynamics som bruker Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="96042-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="96042-109">Prosjekt Operations inkluderer funksjonene som leveres med Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="96042-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="96042-110">En oppgraderingsbane blir utgitt for disse kundene i 2021-lanseringsbølge 1.</span><span class="sxs-lookup"><span data-stu-id="96042-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="96042-111">Eksisterende kunder av Dynamics 365 Finance som bruker prosjektstyring og regnskap</span><span class="sxs-lookup"><span data-stu-id="96042-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="96042-112">Eksisterende kunder av Finance som bruker Prosjektstyring og regnskap-funksjonaliteten, kan fortsette å bruke den som den er.</span><span class="sxs-lookup"><span data-stu-id="96042-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="96042-113">Se [Project Operations for lagerførte scenarioer / produksjonsordrescenarioer](#pma).</span><span class="sxs-lookup"><span data-stu-id="96042-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="96042-114">Distribusjonsområder</span><span class="sxs-lookup"><span data-stu-id="96042-114">Deployment regions</span></span>
<span data-ttu-id="96042-115">Hvis du vil finne ut hvilke områder som støtter Project Operations-distribusjon, kan du se [Geografisk tilgjengelighet for Dynamics 365 og Power Platform-rapport](https://dynamics.microsoft.com/en-us/geographic-availability/).</span><span class="sxs-lookup"><span data-stu-id="96042-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="96042-116">Velg **Vis rapport** og utvid **Dynamics 365 > Operations-apper > Dynamics 365 Project Operations** for å vise de støttede områdene.</span><span class="sxs-lookup"><span data-stu-id="96042-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="96042-117">Distribusjonstyper</span><span class="sxs-lookup"><span data-stu-id="96042-117">Deployment types</span></span>
<span data-ttu-id="96042-118">Project Operations støtter flere distribusjonsalternativer for å dekke dine behov.</span><span class="sxs-lookup"><span data-stu-id="96042-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="96042-119">Enten du er en ny eller eksisterende Dynamics 365-kunde, kan Project Operations støtte dine behov.</span><span class="sxs-lookup"><span data-stu-id="96042-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="96042-120">[Spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations) hjelper deg med å finne riktig distribusjon.</span><span class="sxs-lookup"><span data-stu-id="96042-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="96042-121">Resultatene leder deg mot én av følgende distribusjonstyper:</span><span class="sxs-lookup"><span data-stu-id="96042-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="96042-122">Lite-distribusjon – avtale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="96042-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="96042-123">Project Operations for ressursbaserte/ikke-lagerførte scenarioer</span><span class="sxs-lookup"><span data-stu-id="96042-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="96042-124">Project Operations for lagerførte scenarioer / produksjonsordrescenarioer</span><span class="sxs-lookup"><span data-stu-id="96042-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="96042-125">Project Operations støtter lagerførte scenarioer / produksjonsordrescenarioer og ordre scenarioer og ikke-lagerbaserte/ressursbaserte scenarioer i samme miljø ved hjelp av konfigurasjoner på juridisk enhetsnivå.</span><span class="sxs-lookup"><span data-stu-id="96042-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="96042-126">Contoso kan for eksempel bruke kapasiteten for lagerbeholdning/produksjon i produksjonsfasilitetene i USA (juridisk enhet = Contoso Manufacturing i USA).</span><span class="sxs-lookup"><span data-stu-id="96042-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="96042-127">Contoso kan bruke de ikke-lagerbeholdte/ressursbaserte funksjonene i Contosos anlegg for service av robotarmer i Storbritannia (juridisk enhet = Contoso Robotics i Storbritannia).</span><span class="sxs-lookup"><span data-stu-id="96042-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="96042-128">Lite-distribusjon – avtale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="96042-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="96042-129">Lite-distribusjonen omfatter følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="96042-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="96042-130">Salgsprosess for prosjekter som utvider Dynamics 365 Sales-programerfaringer</span><span class="sxs-lookup"><span data-stu-id="96042-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="96042-131">Prosjektplanlegging ved hjelp av Microsoft Project for Internett</span><span class="sxs-lookup"><span data-stu-id="96042-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="96042-132">Flerdimensjonal prising</span><span class="sxs-lookup"><span data-stu-id="96042-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="96042-133">Enhetlig ressursstyring</span><span class="sxs-lookup"><span data-stu-id="96042-133">Unified resource management</span></span>
- <span data-ttu-id="96042-134">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="96042-134">Time tracking</span></span>
- <span data-ttu-id="96042-135">Grunnleggende utgift</span><span class="sxs-lookup"><span data-stu-id="96042-135">Basic expense</span></span>
- <span data-ttu-id="96042-136">Proforma fakturering for prosjektleders gjennomgang og redigeringer</span><span class="sxs-lookup"><span data-stu-id="96042-136">Proforma invoicing for Project manager's review and edits</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="96042-137">Trinn for distribusjon</span><span class="sxs-lookup"><span data-stu-id="96042-137">Deployment steps</span></span>
<span data-ttu-id="96042-138">Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="96042-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="96042-139">For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](lite-preview-subscription-sign-up.md) og [Klargjøre nytt miljø](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="96042-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="96042-140">Project Operations for ressursbaserte/ikke-lagerførte scenarioer</span><span class="sxs-lookup"><span data-stu-id="96042-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="96042-141">Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer inkluderer følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="96042-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="96042-142">Salgsprosess for prosjekter som utvider Dynamics 365 Sales-programmet</span><span class="sxs-lookup"><span data-stu-id="96042-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="96042-143">Prosjektplanlegging ved hjelp av Microsoft Project for Internett</span><span class="sxs-lookup"><span data-stu-id="96042-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="96042-144">Flerdimensjonal prising</span><span class="sxs-lookup"><span data-stu-id="96042-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="96042-145">Enhetlig ressursstyring</span><span class="sxs-lookup"><span data-stu-id="96042-145">Unified resource management</span></span>
- <span data-ttu-id="96042-146">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="96042-146">Time tracking</span></span>
- <span data-ttu-id="96042-147">Grunnleggende utgift</span><span class="sxs-lookup"><span data-stu-id="96042-147">Basic expense</span></span>
- <span data-ttu-id="96042-148">Fullstendig utgift</span><span class="sxs-lookup"><span data-stu-id="96042-148">Full expense</span></span>
- <span data-ttu-id="96042-149">Mottak av OCR</span><span class="sxs-lookup"><span data-stu-id="96042-149">Receipt OCR</span></span>
- <span data-ttu-id="96042-150">Proforma og kunderettet fakturering</span><span class="sxs-lookup"><span data-stu-id="96042-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="96042-151">Inntektsføring for prosjekter</span><span class="sxs-lookup"><span data-stu-id="96042-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="96042-152">Trinn for distribusjon</span><span class="sxs-lookup"><span data-stu-id="96042-152">Deployment steps</span></span>
<span data-ttu-id="96042-153">Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="96042-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="96042-154">For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](resource-sign-up-preview-subscription.md) og [Klargjøre nytt miljø](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="96042-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="96042-155">Project Operations for lagerførte scenarioer / produksjonsordrescenarioer</span><span class="sxs-lookup"><span data-stu-id="96042-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="96042-156">Prosjektplanlegging ved hjelp av WBS</span><span class="sxs-lookup"><span data-stu-id="96042-156">Project planning using WBS</span></span>
- <span data-ttu-id="96042-157">Ressursstyring</span><span class="sxs-lookup"><span data-stu-id="96042-157">Resource management</span></span>
- <span data-ttu-id="96042-158">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="96042-158">Time tracking</span></span>
- <span data-ttu-id="96042-159">Fullstendig utgift</span><span class="sxs-lookup"><span data-stu-id="96042-159">Full expense</span></span>
- <span data-ttu-id="96042-160">Mottak av OCR</span><span class="sxs-lookup"><span data-stu-id="96042-160">Receipt OCR</span></span>
- <span data-ttu-id="96042-161">Full fakturering</span><span class="sxs-lookup"><span data-stu-id="96042-161">Full invoicing</span></span>
- <span data-ttu-id="96042-162">Inntektsføring</span><span class="sxs-lookup"><span data-stu-id="96042-162">Revenue recognition</span></span>
- <span data-ttu-id="96042-163">Produksjonsordrer</span><span class="sxs-lookup"><span data-stu-id="96042-163">Production orders</span></span>
- <span data-ttu-id="96042-164">Støtte for lagerførte materialer med beholdning</span><span class="sxs-lookup"><span data-stu-id="96042-164">Stocked materials support with inventory</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="96042-165">Trinn for distribusjon</span><span class="sxs-lookup"><span data-stu-id="96042-165">Deployment steps</span></span>
<span data-ttu-id="96042-166">Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="96042-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="96042-167">For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) og [Klargjøre nytt miljø](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="96042-167">For this deployment, see [Sign-up for preview subscriptions](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) and [Provision new environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]