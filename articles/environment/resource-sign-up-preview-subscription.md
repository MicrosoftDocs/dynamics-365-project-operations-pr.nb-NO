---
title: Registrer deg for forhåndsversjonsabonnementer på Project Operations for ressursbaserte/ikke-lagerførte scenarioer
description: Dette emnet gir informasjon om hvordan du abonnerer på og distribuerer Project Operations for ressursbaserte/ikke-lagerførte scenarioer.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949002"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="eb37d-103">Registrer deg for forhåndsversjonsabonnementer på Project Operations for ressursbaserte/ikke-lagerførte scenarioer</span><span class="sxs-lookup"><span data-stu-id="eb37d-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="eb37d-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="eb37d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="eb37d-105">Dette emnet forklarer hvordan du abonnerer på tilbudet om forhåndsversjon/partner og distribuerer Project Operations-miljøer for ressursbaserte/ikke-lagerførte scenarioer.</span><span class="sxs-lookup"><span data-stu-id="eb37d-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eb37d-106">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="eb37d-106">Prerequisites</span></span>

- <span data-ttu-id="eb37d-107">Du vil motta en e-post som inviterer deg til å delta i forhåndsversjonen.</span><span class="sxs-lookup"><span data-stu-id="eb37d-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="eb37d-108">Du kan be om en forhåndsversjon på [Project Operations-nettstsedet](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="eb37d-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="eb37d-109">Brukeren som distribuerer forhåndsversjonen, må ha globale administratorrettigheter for Azure-leieren.</span><span class="sxs-lookup"><span data-stu-id="eb37d-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="eb37d-110">Distribusjon av et Finance-miljø krever et gyldig Azure-abonnement som blir fakturert per miljø.</span><span class="sxs-lookup"><span data-stu-id="eb37d-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="eb37d-111">Du kan bruke organisasjonens eksisterende abonnement eller bruke en [Azure-prøveversjon](https://azure.microsoft.com/en-us/free/) for å komme i gang.</span><span class="sxs-lookup"><span data-stu-id="eb37d-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="eb37d-112">CDS-miljøet tilbys gratis i en begrenset periode på 30 dager.</span><span class="sxs-lookup"><span data-stu-id="eb37d-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="eb37d-113">Abonner</span><span class="sxs-lookup"><span data-stu-id="eb37d-113">Subscribe</span></span>

<span data-ttu-id="eb37d-114">Når [forespørselen din om forhåndsversjon](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) er godkjent, får du to tilbud fra Microsoft via e-post.</span><span class="sxs-lookup"><span data-stu-id="eb37d-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="eb37d-115">Med disse tilbudene kan du distribuere forhåndsversjonen av Project Operations:</span><span class="sxs-lookup"><span data-stu-id="eb37d-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="eb37d-116">Dynamics 365 Project Operations – forhåndsversjon</span><span class="sxs-lookup"><span data-stu-id="eb37d-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="eb37d-117">Dynamics 365 for Finance and Operations – forhåndsversjon.</span><span class="sxs-lookup"><span data-stu-id="eb37d-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb37d-118">Bare én person, leieradministratoren, i en organisasjon trenger å utføre denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="eb37d-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="eb37d-119">Hvis det ikke er du som er abonnent for denne versjonen, må du vente til organisasjonen har registrert seg og du har mottatt brukerlegitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="eb37d-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="eb37d-120">Dynamics 365 Project Operations – forhåndsversjon</span><span class="sxs-lookup"><span data-stu-id="eb37d-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="eb37d-121">Løs inn det første tilbudet, **prøveversjonen av Dynamics 365 Project Operations**, med URL-adressen fra e-postmeldingen.</span><span class="sxs-lookup"><span data-stu-id="eb37d-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Første tilbud](./media/1FirstOffer.png)

2. <span data-ttu-id="eb37d-123">Kontroller at du er logget på som brukeren som tilhører organisasjonen, og som skal abonnere på tjenesten.</span><span class="sxs-lookup"><span data-stu-id="eb37d-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="eb37d-124">Fortsett med å løse inn tilbudet.</span><span class="sxs-lookup"><span data-stu-id="eb37d-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="eb37d-125">Velg **Ja, Legg det til på kontoen min**.</span><span class="sxs-lookup"><span data-stu-id="eb37d-125">Select **Yes, add it to my account**.</span></span>

![Løs inn tilbud](./media/2RedeemFirstOffer.png)

![Bekreft tilbud](./media/3ConfirmFirstOffer.png)

![Tilbud løst inn](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="eb37d-129">Dynamics 365 Finance – forhåndsversjon</span><span class="sxs-lookup"><span data-stu-id="eb37d-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="eb37d-130">Gjenta de samme trinnene med det andre tilbudet fra e-postmeldingen.</span><span class="sxs-lookup"><span data-stu-id="eb37d-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="eb37d-131">Tilordne lisenser</span><span class="sxs-lookup"><span data-stu-id="eb37d-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb37d-132">Du må ha administrativ tilgang til organisasjonens Office 365-portal for å kunne utføre følgende trinn.</span><span class="sxs-lookup"><span data-stu-id="eb37d-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="eb37d-133">Gå til [administrasjonssenteret for Microsoft 365](https://portal.office.com/) for å tilordne lisenser til brukerne dine.</span><span class="sxs-lookup"><span data-stu-id="eb37d-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Administrasjonsportal for Office](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="eb37d-135">På siden **Aktive brukere** velger du brukerne du vil tilordne en lisens til.</span><span class="sxs-lookup"><span data-stu-id="eb37d-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Tilordne lisenser](./media/6AssignLicenses.png)

3. <span data-ttu-id="eb37d-137">Kontroller at Project Operations-lisensen er valgt, og velg **Lagre endringer**.</span><span class="sxs-lookup"><span data-stu-id="eb37d-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="eb37d-138">Prøvetilbudet på Finance trenger ikke tilordnes til en bruker.</span><span class="sxs-lookup"><span data-stu-id="eb37d-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="eb37d-139">Start et nytt prosjekt i LCS</span><span class="sxs-lookup"><span data-stu-id="eb37d-139">Start a new project in LCS</span></span>

<span data-ttu-id="eb37d-140">Opprett et nytt LCS-prosjekt slik det er beskrevet i emnet [Start et nytt prosjekt i LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="eb37d-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="eb37d-141">Legg til et Azure-abonnement i et LCS Project</span><span class="sxs-lookup"><span data-stu-id="eb37d-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="eb37d-142">For å fullføre denne oppgaven må du følge fremgangsmåten i emnet [Legg til et Azure-abonnement i et LCS-prosjekt](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="eb37d-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="eb37d-143">Distribuer Finance-demonstrasjonsmiljø med Project Operations for scenarioer for ressursbaserte/ikke-lagerførte scenarioer</span><span class="sxs-lookup"><span data-stu-id="eb37d-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="eb37d-144">Følg veiledningen i emnet [Klargjør et nytt miljø](resource-provision-new-environment.md) for å fullføre distribusjonen.</span><span class="sxs-lookup"><span data-stu-id="eb37d-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="eb37d-145">Bruk distribusjonstypen [demonstrasjonsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) for forhåndsversjonen.</span><span class="sxs-lookup"><span data-stu-id="eb37d-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="eb37d-146">Installer CDS-oppsett og konfigurasjonsdata</span><span class="sxs-lookup"><span data-stu-id="eb37d-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="eb37d-147">Installer CDS-oppsett og konfigurasjonsdata slik det er beskrevet i emnet [Konfigurer og bruk konfigurasjonsdata i Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="eb37d-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

