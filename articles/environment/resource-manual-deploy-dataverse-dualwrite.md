---
title: Distribuer Project Operations Dataverse-appen manuelt med støtte for dobbel skriving
description: Dette emnet forklarer hvordan du distribuerer Project Operations Dataverse-appen manuelt slik at den støtter dobbel skriving.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274020"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="fdced-103">Distribuer Project Operations Dataverse-appen manuelt med støtte for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="fdced-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="fdced-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="fdced-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fdced-105">Dette emnet forklarer hvordan du distribuerer Microsoft Dynamics 365 Project Operations i Microsoft Dataverse slik at den støtter dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="fdced-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="fdced-106">Project Operations registrerer konfigurasjonen av miljøet og legger til ytterligere støtte for dobbel skriving hvis forutsetningene oppfylles.</span><span class="sxs-lookup"><span data-stu-id="fdced-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="fdced-107">Hvis du har fulgt instruksjonene i dette emnet under distribusjon gjennom Microsoft Dynamics Lifecycle Services (LCS), kan du hoppe over distribusjonen av Microsoft Power Platform-integreringen (tidligere kjent som Common Data Service-miljøet).</span><span class="sxs-lookup"><span data-stu-id="fdced-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="fdced-108">Prosessen med å distribuere Project Operations i Dataverse slik at den støtter dobbel skriving har fire hovedtrinn:</span><span class="sxs-lookup"><span data-stu-id="fdced-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="fdced-109">[Opprett et nytt miljø i Dataverse som støtter dobbel skriving](#create).</span><span class="sxs-lookup"><span data-stu-id="fdced-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="fdced-110">[Legg til forutsetninger til dobbel skriving i miljøet](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="fdced-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="fdced-111">[Legg til Project Operations Dataverse-appen](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="fdced-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="fdced-112">[Koble til miljøene](#link).</span><span class="sxs-lookup"><span data-stu-id="fdced-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="fdced-113">Opprett et nytt miljø i Dataverse som støtter dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="fdced-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="fdced-114">Hvis du vil fullføre denne fremgangsmåten, må du logge på som administrator.</span><span class="sxs-lookup"><span data-stu-id="fdced-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="fdced-115">Åpne [Power Platform-administrasjonssenteret](https://admin.powerplatform.com), og logg på som administrator.</span><span class="sxs-lookup"><span data-stu-id="fdced-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="fdced-116">Opprett et nytt miljø og gi det navn.</span><span class="sxs-lookup"><span data-stu-id="fdced-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="fdced-117">Velg miljøtypen.</span><span class="sxs-lookup"><span data-stu-id="fdced-117">Select the environment type.</span></span> <span data-ttu-id="fdced-118">Hvis du registrerte deg for prøveversjonstilbudet, velger du **Prøveversjon (abonnementsbasert)**.</span><span class="sxs-lookup"><span data-stu-id="fdced-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="fdced-119">Bekreft distribusjonsområdet.</span><span class="sxs-lookup"><span data-stu-id="fdced-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="fdced-120">Aktiver alternativet **Opprett en database for dette miljøet**.</span><span class="sxs-lookup"><span data-stu-id="fdced-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="fdced-121">Bekreft språket, og bekreft deretter at valutaen samsvarer med valutaen for Finance and Operations-appene dine.</span><span class="sxs-lookup"><span data-stu-id="fdced-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="fdced-122">Aktiver alternativet **Dynamics 365-apper**, og bekreft at feltet **Automatisk distribusjon av disse appene** er satt til **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="fdced-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="fdced-123">Legg til en sikkerhetsgruppe hvis det kreves en sikkerhetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="fdced-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="fdced-124">Velg **Lagre** for å opprette miljøet.</span><span class="sxs-lookup"><span data-stu-id="fdced-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="fdced-125">Vent til distribusjonen er fullført og miljøet når tilstanden **Klar**.</span><span class="sxs-lookup"><span data-stu-id="fdced-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="fdced-126">Legg til forutsetninger til dobbel skriving i miljøet</span><span class="sxs-lookup"><span data-stu-id="fdced-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="fdced-127">Støtte for dobbel skriving inkluderer flere felter som legges til viktige enheter, for eksempel **Firma**-enheten.</span><span class="sxs-lookup"><span data-stu-id="fdced-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="fdced-128">Hvis du legger til støtte for dobbel skriving i et eksisterende miljø, må du kanskje oppdatere dataene for å aktivere støtten.</span><span class="sxs-lookup"><span data-stu-id="fdced-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="fdced-129">Hvis du vil ha mer informasjon om hvordan du starter opp dataene, kan du se [Bootstrap-firmadata](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="fdced-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="fdced-130">Hvis du vil ha mer informasjon om dobbel skriving, kan du se [Systemkrav for dobbel skriving](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="fdced-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="fdced-131">Fullfør denne fremgangsmåten for å legge til forutsetningene for dobbel skriving i miljøet.</span><span class="sxs-lookup"><span data-stu-id="fdced-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="fdced-132">Åpne miljøet du nettopp opprettet, og gå deretter til **Ressurs** \> **Dynamics 365-apper**.</span><span class="sxs-lookup"><span data-stu-id="fdced-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="fdced-133">Velg **Løsning for dobbel skriving** i applisten, og installer den.</span><span class="sxs-lookup"><span data-stu-id="fdced-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="fdced-134">Vent til installasjonen er fullført.</span><span class="sxs-lookup"><span data-stu-id="fdced-134">Wait until the installation is completed.</span></span> <span data-ttu-id="fdced-135">Velg deretter **Orkestreringsløsning for dobbel skriving** i applisten, og installer den.</span><span class="sxs-lookup"><span data-stu-id="fdced-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="fdced-136">Legg til Project Operations Dataverse-appen</span><span class="sxs-lookup"><span data-stu-id="fdced-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="fdced-137">Du kan bare fullføre denne fremgangsmåten hvis du har fullført de forrige fremgangsmåtene før du installerte Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fdced-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="fdced-138">Under installasjonen analyserer systemet miljøkonfigurasjonen og støtte for dobbel skriving hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="fdced-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="fdced-139">Åpne miljøet du opprettet tidligere, og gå deretter til **Ressurs** \> **Dynamics 365-apper**.</span><span class="sxs-lookup"><span data-stu-id="fdced-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="fdced-140">Velg **Microsoft Dynamics 365 Project Operations** i applisten, og installer den.</span><span class="sxs-lookup"><span data-stu-id="fdced-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="fdced-141">Koble til miljøene</span><span class="sxs-lookup"><span data-stu-id="fdced-141">Link your environments</span></span>

<span data-ttu-id="fdced-142">Når Dataverse-miljøet er distribuert, kan du konfigurere koblingen i Finance and Operations-appene dine.</span><span class="sxs-lookup"><span data-stu-id="fdced-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="fdced-143">Følg fremgangsmåten i [Bruk veiviseren for dobbel skriving til å koble miljøene](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="fdced-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
