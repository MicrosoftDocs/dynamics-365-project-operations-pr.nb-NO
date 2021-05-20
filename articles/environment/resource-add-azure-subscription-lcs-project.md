---
title: Legg til et Azure-abonnement i et LCS Project
description: Dette emnet gir informasjon om hvordan du kobler Azure-abonnementet til et LCS-prosjekt.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880550"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="3ddd5-103">Legg til et Azure-abonnement i et LCS Project</span><span class="sxs-lookup"><span data-stu-id="3ddd5-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="3ddd5-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="3ddd5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3ddd5-105">Skydriftede miljøer må distribueres ved hjelp av et eksisterende Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="3ddd5-106">Dette emnet forklarer hvordan du kobler det eksisterende Azure-abonnementet ditt til et LCS-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="3ddd5-107">Gi admin-tillatelse</span><span class="sxs-lookup"><span data-stu-id="3ddd5-107">Grant admin consent</span></span>

1. <span data-ttu-id="3ddd5-108">I LCS-prosjektet, i **Miljøer**-delen velger du **Microsoft Azure-innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Innstillinger for Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="3ddd5-110">På siden **Prosjektinnstillinger** i kategorien **Azure-kontakter** velger du **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="3ddd5-111">Dette gjør det mulig å distribuere miljøer til dette prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-111">This allows environments to be deployed to this project.</span></span>

![Azure-koblinger](./media/2AzureConnectors.png)

3. <span data-ttu-id="3ddd5-113">Velg **Autoriser** på nytt for å gi administratorsamtykke.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-113">Select **Authorize** again to provide admin consent.</span></span>

![Gi admin-tillatelse](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="3ddd5-115">Godta tillatelsesforespørselen.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-115">Accept the permissions request.</span></span>

![Godta tillatelsesforespørsel](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="3ddd5-117">Autorisasjonen er nå fullført.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-117">The authorization is now complete.</span></span> 

![Autorisasjon vellykket](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="3ddd5-119">Gi Dynamics Deployment Services tilgang til Azure-abonnementet</span><span class="sxs-lookup"><span data-stu-id="3ddd5-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="3ddd5-120">Gå til [Microsoft Azure-fakturering](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade), og velg abonnementet ditt.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="3ddd5-121">Dynamics Deployment Services må ha tilgang til dette abonnementet for å kunne distribuere miljøer.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Azure-abonnementsdetaljer](./media/6AzureSubscription.png)

2. <span data-ttu-id="3ddd5-123">Velg **Tilgangskontroll (IAM)** i navigasjonsruten, og velg deretter **Legg til rolletildeling**.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="3ddd5-124">På glidebryteren til høyre velger du **Bidragsyterroller**, og finn og velg **Dynamics Deployment Services** i listen som vises.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="3ddd5-125">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-125">Select **Save**.</span></span>

![Abonnementstilgang](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="3ddd5-127">Legg til en abonnementskontakt i et LCS Project</span><span class="sxs-lookup"><span data-stu-id="3ddd5-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="3ddd5-128">I LCS-prosjektet, på siden **Microsoft Azure-innstillinger**, velger du **Legg til** for å legge til en ny kontakt.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="3ddd5-129">Skriv inn Azure abonnements-ID-en din.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="3ddd5-130">Du finner Azure-abonnements-ID-en i [Azure-portalen](https://ms.portal.azure.com/), under **Innstillinger** nederst til venstre på skjermen.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="3ddd5-131">I feltet **Konfigurer for å bruke Azure Resource Manager** velger du **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="3ddd5-132">Kontroller at Azure-abonnementets AAD-leierdomene samsvarer med det domeneeiende Azure-abonnementet du bruker, og velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="3ddd5-133">På skjermen **Microsoft Azure-oppsett** velger du **Neste** for å bekrefte.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="3ddd5-134">Hvis det vises en feil i skjermbildet, må du gå tilbake til delen [Gi Dynamics Deployment Services tilgang til Azure-abonnementet](#provide) i dette emnet og må kontrollere at du har fullført alle trinnene.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="3ddd5-135">Last ned Azure Management-sertifikatet til en lokal mappe på datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="3ddd5-136">Be administrator for Azure-abonnementet ditt om å laste opp sertifikatet til Azure Management-portalen ved å velge abonnementet og gå til **Innstillinger** > **Administrasjonssertifikater**.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="3ddd5-137">Dette sertifikatet gjør det mulig for LCS å kommunisere med Azure på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="3ddd5-138">Du kan hoppe over dette trinnet hvis brukeren har tilgang til abonnementet.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="3ddd5-139">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-139">Select  **Next**.</span></span>
8. <span data-ttu-id="3ddd5-140">Velg Azure-området du skal distribuere i, og velg et datasenter som er nær stedet der du vil bruke dette systemet.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="3ddd5-141">Velg **Koble til**.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-141">Select  **Connect**.</span></span>

<span data-ttu-id="3ddd5-142">Du har koblet til Azure-abonnementet.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="3ddd5-143">Du kan nå distribuere skydriftede Dynamics 365 Finance-miljøer.</span><span class="sxs-lookup"><span data-stu-id="3ddd5-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
