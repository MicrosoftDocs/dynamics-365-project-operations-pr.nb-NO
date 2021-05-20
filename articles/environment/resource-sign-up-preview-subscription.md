---
title: Registrer deg for forhåndsversjonsabonnementer på Project Operations for ressursbaserte/ikke-lagerførte scenarioer
description: Dette emnet gir informasjon om hvordan du abonnerer på og distribuerer Project Operations for ressursbaserte/ikke-lagerførte scenarioer.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 917ead8ff6d9d3ef8374f8ccde608b6cebd50c8c
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948476"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="081b4-103">Registrer deg for forhåndsversjonsabonnementer på Project Operations for ressursbaserte/ikke-lagerførte scenarioer</span><span class="sxs-lookup"><span data-stu-id="081b4-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="081b4-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="081b4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="081b4-105">Dette emnet forklarer hvordan du abonnerer på tilbudet om forhåndsversjon/partner og distribuerer Project Operations-miljøer for ressursbaserte/ikke-lagerførte scenarioer.</span><span class="sxs-lookup"><span data-stu-id="081b4-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="081b4-106">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="081b4-106">Prerequisites</span></span>

- <span data-ttu-id="081b4-107">Du vil motta en e-post som inviterer deg til å delta i forhåndsversjonen.</span><span class="sxs-lookup"><span data-stu-id="081b4-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="081b4-108">Du kan be om en forhåndsversjon på [Project Operations-nettstsedet](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="081b4-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="081b4-109">Brukeren som distribuerer forhåndsversjonen, må ha globale administratorrettigheter for Azure-leieren.</span><span class="sxs-lookup"><span data-stu-id="081b4-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="081b4-110">Distribusjon av et Finance-miljø krever et gyldig Azure-abonnement som blir fakturert per miljø.</span><span class="sxs-lookup"><span data-stu-id="081b4-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="081b4-111">Du kan bruke organisasjonens eksisterende abonnement eller bruke en [Azure-prøveversjon](https://azure.microsoft.com/en-us/free/) for å komme i gang.</span><span class="sxs-lookup"><span data-stu-id="081b4-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="081b4-112">CDS-miljøet tilbys gratis i en begrenset periode på 30 dager.</span><span class="sxs-lookup"><span data-stu-id="081b4-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="081b4-113">Abonner</span><span class="sxs-lookup"><span data-stu-id="081b4-113">Subscribe</span></span>

<span data-ttu-id="081b4-114">Når [forespørselen din om forhåndsversjon](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) er godkjent, får du tre tilbud fra Microsoft via e-post.</span><span class="sxs-lookup"><span data-stu-id="081b4-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="081b4-115">Med disse tilbudene kan du distribuere forhåndsversjonen av Project Operations:</span><span class="sxs-lookup"><span data-stu-id="081b4-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="081b4-116">Dynamics 365 Project Operations (CRM) – forhåndsversjon</span><span class="sxs-lookup"><span data-stu-id="081b4-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="081b4-117">Office 365 Project Operations – forhåndsversjon</span><span class="sxs-lookup"><span data-stu-id="081b4-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="081b4-118">Dynamics 365 Finance – forhåndsversjon</span><span class="sxs-lookup"><span data-stu-id="081b4-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="081b4-119">Bare én person, leieradministratoren, i en organisasjon trenger å utføre denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="081b4-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="081b4-120">Hvis det ikke er du som er abonnent for denne versjonen, må du vente til organisasjonen har registrert seg og du har mottatt brukerlegitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="081b4-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="081b4-121">Dynamics 365 Project Operations (CRM) – forhåndsversjon</span><span class="sxs-lookup"><span data-stu-id="081b4-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="081b4-122">Før du begynner, må du forsikre deg om at du er logget på en nettleser med brukerarbeidskontoen i leieren der du vil ha forhåndsversjonen av Project Operations.</span><span class="sxs-lookup"><span data-stu-id="081b4-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="081b4-123">Løs inn den første tilbudskoden **Dynamics 365 Project Operations (CRM) – forhåndsversjon** ved å lime den inn i URL-adressen i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="081b4-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Løs inn tilbud](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="081b4-125">Bekreft ordren.</span><span class="sxs-lookup"><span data-stu-id="081b4-125">Confirm your order.</span></span>

![Bekreft ordren](./media/17ConfirmOrderNew.png)

<span data-ttu-id="081b4-127">Du ser en bekreftelse på at tilbudet ble løst inn.</span><span class="sxs-lookup"><span data-stu-id="081b4-127">You will see confirmation offer was successfully redeemed.</span></span>

![Bekreftelse](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="081b4-129">Office 365 Project Operations – forhåndsversjon</span><span class="sxs-lookup"><span data-stu-id="081b4-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="081b4-130">Gjenta de samme trinnene som med den første tilbudskoden.</span><span class="sxs-lookup"><span data-stu-id="081b4-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="081b4-131">Pass på at du legger til den andre tilbudskoden ved hjelp av den samme brukerkontoen som ble brukt med første tilbudskode.</span><span class="sxs-lookup"><span data-stu-id="081b4-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="081b4-132">Dynamics 365 Finance – forhåndsversjon</span><span class="sxs-lookup"><span data-stu-id="081b4-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="081b4-133">Gjenta de samme trinnene med det siste tilbudet fra e-postmeldingen.</span><span class="sxs-lookup"><span data-stu-id="081b4-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="081b4-134">Tilordne lisenser</span><span class="sxs-lookup"><span data-stu-id="081b4-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="081b4-135">Du må ha administrativ tilgang til organisasjonens Microsoft 365-portal for å kunne utføre følgende trinn.</span><span class="sxs-lookup"><span data-stu-id="081b4-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="081b4-136">Gå til [administrasjonssenteret for Microsoft 365](https://portal.office.com/) for å tilordne lisensene til brukerne dine.</span><span class="sxs-lookup"><span data-stu-id="081b4-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Startsiden for administrasjonssenteret](./media/14AdminPortal.png)

2. <span data-ttu-id="081b4-138">På siden **Aktive brukere** velger du brukerne du vil tilordne en lisens til.</span><span class="sxs-lookup"><span data-stu-id="081b4-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Tilordne lisenser](./media/15AssignLicenses.png)

3. <span data-ttu-id="081b4-140">Bekreft at **Dynamics 365 Project Operations (CRM) Forhåndsvisning**- og **Office 365 Project Operations – Forhåndsvisning**-lisensen er valgt, og velg **Lagre endringer**.</span><span class="sxs-lookup"><span data-stu-id="081b4-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="081b4-141">Prøvetilbudet på Finance trenger ikke tilordnes til en bruker.</span><span class="sxs-lookup"><span data-stu-id="081b4-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="081b4-142">Start et nytt prosjekt i LCS</span><span class="sxs-lookup"><span data-stu-id="081b4-142">Start a new project in LCS</span></span>

<span data-ttu-id="081b4-143">Opprett et nytt LCS-prosjekt slik det er beskrevet i emnet [Start et nytt prosjekt i LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="081b4-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="081b4-144">Legg til et Azure-abonnement i et LCS Project</span><span class="sxs-lookup"><span data-stu-id="081b4-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="081b4-145">For å fullføre denne oppgaven må du følge fremgangsmåten i emnet [Legg til et Azure-abonnement i et LCS-prosjekt](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="081b4-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="081b4-146">Distribuer Finance-demonstrasjonsmiljø med Project Operations for scenarioer for ressursbaserte/ikke-lagerførte scenarioer</span><span class="sxs-lookup"><span data-stu-id="081b4-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="081b4-147">Følg veiledningen i emnet [Klargjør et nytt miljø](resource-provision-new-environment.md) for å fullføre distribusjonen.</span><span class="sxs-lookup"><span data-stu-id="081b4-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="081b4-148">Bruk distribusjonstypen [demonstrasjonsmiljø](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) for forhåndsversjonen.</span><span class="sxs-lookup"><span data-stu-id="081b4-148">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="081b4-149">Installer CDS-oppsett og konfigurasjonsdata</span><span class="sxs-lookup"><span data-stu-id="081b4-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="081b4-150">Installer CDS-oppsett og konfigurasjonsdata slik det er beskrevet i emnet [Konfigurer og bruk konfigurasjonsdata i Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="081b4-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="081b4-151">Utfør dette trinnet bare etter at demomiljøet i Finance er distribuert, og når demodataene i FO er klare.</span><span class="sxs-lookup"><span data-stu-id="081b4-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]