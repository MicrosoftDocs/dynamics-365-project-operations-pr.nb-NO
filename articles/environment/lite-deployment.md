---
title: Distribuere Project Operations – Lite
description: Dette emnet gir informasjon om hvordan du installerer Lite-distribusjon i Project Operations – avtale til proformafakturering.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d4ef905f875ac8af7b2d70c3e64506558bdea1ed
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642195"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="a9cb9-103">Distribuere Project Operations – Lite</span><span class="sxs-lookup"><span data-stu-id="a9cb9-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="a9cb9-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="a9cb9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a9cb9-105">Project Operations støtter flere distribusjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="a9cb9-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="a9cb9-106">Hvis du vil finne den beste distribusjonsmodellen, kan du se [Distribusjonstyper](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb9-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="a9cb9-107">Denne distribusjonen, Lite-distribusjon – avtale til proformafakturering, fører til en **distribusjon av Project Operations bare med Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="a9cb9-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="a9cb9-108">Installer Project Operations i et nytt CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="a9cb9-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="a9cb9-109">Installer i et eksisterende CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="a9cb9-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="a9cb9-110">Installer Project Operations i et nytt CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="a9cb9-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="a9cb9-111">Som [global eller Power Platform-administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-lisens oppretter du et nytt CDS-miljø i [administrasjonssenteret for Power Platform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="a9cb9-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="a9cb9-112">Kontroller at **CDS-database** og **Dynamics 365-apper** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="a9cb9-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="a9cb9-113">Hvis du vil ha mer informasjon, kan du se [Opprette og administrere miljøer i Power Platform-administrasjonssenteret](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="a9cb9-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="a9cb9-114">Velg **Microsoft Dynamics 365 Project Operations** fra distribusjonslisten over Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="a9cb9-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="a9cb9-115">Installer Project Operations i et eksisterende CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="a9cb9-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="a9cb9-116">Som [global eller Power Platform-administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-lisens finner du miljøet i [administrasjonssenteret for Power Platform](https://admin.powerplatform.com) der du ønsker å installere Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a9cb9-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="a9cb9-117">Installer **Microsoft Dynamics 365 Project Operations** fra distribusjonslisten over Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="a9cb9-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="a9cb9-118">Hvis du vil ha mer informasjon, kan du se [Administrere Dynamics 365-apper](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="a9cb9-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


