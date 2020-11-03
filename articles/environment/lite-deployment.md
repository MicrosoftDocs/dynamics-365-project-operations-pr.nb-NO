---
title: Project Operations Lite-distribusjon – avtale til proformafakturering
description: Dette emnet gir informasjon om hvordan du installerer Lite-distribusjon i Project Operations – avtale til proformafakturering.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081484"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="3a44d-103">Project Operations Lite-distribusjon – avtale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="3a44d-103">Deploy Project Operations Lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="3a44d-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="3a44d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3a44d-105">Project Operations støtter flere distribusjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="3a44d-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="3a44d-106">Hvis du vil finne den beste distribusjonsmodellen, kan du se [Distribusjonstyper](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="3a44d-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="3a44d-107">Denne distribusjonen, Lite-distribusjon – avtale til proformafakturering, fører til en **distribusjon av Project Operations bare med Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="3a44d-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="3a44d-108">Installer Project Operations i et nytt CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="3a44d-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="3a44d-109">Installer i et eksisterende CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="3a44d-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="3a44d-110">Installer Project Operations i et nytt CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="3a44d-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="3a44d-111">Som [global eller Power Platform-administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-lisens oppretter du et nytt CDS-miljø i [administrasjonssenteret for Power Platform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="3a44d-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="3a44d-112">Kontroller at **CDS-database** og **Dynamics 365-apper** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="3a44d-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="3a44d-113">Hvis du vil ha mer informasjon, kan du se [Opprette og administrere miljøer i Power Platform-administrasjonssenteret](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="3a44d-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="3a44d-114">Velg **Microsoft Dynamics 365 Project Operations** fra distribusjonslisten over Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="3a44d-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="3a44d-115">Installer Project Operations i et eksisterende CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="3a44d-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="3a44d-116">Som [global eller Power Platform-administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-lisens finner du miljøet i [administrasjonssenteret for Power Platform](https://admin.powerplatform.com) der du ønsker å installere Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3a44d-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="3a44d-117">Installer **Microsoft Dynamics 365 Project Operations** fra distribusjonslisten over Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="3a44d-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="3a44d-118">Hvis du vil ha mer informasjon, kan du se [Administrere Dynamics 365-apper](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="3a44d-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


