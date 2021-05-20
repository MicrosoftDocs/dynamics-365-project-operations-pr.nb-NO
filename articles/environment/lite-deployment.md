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
ms.openlocfilehash: 2470d573f4537cb22de4dbd98caff148cbe0bda3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950276"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="a9a68-103">Distribuere Project Operations – Lite</span><span class="sxs-lookup"><span data-stu-id="a9a68-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="a9a68-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="a9a68-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a9a68-105">Project Operations støtter flere distribusjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="a9a68-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="a9a68-106">Hvis du vil finne den beste distribusjonsmodellen, kan du se [Distribusjonstyper](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="a9a68-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="a9a68-107">Denne distribusjonen, Lite-distribusjon – avtale til proformafakturering, fører til en **distribusjon av Project Operations bare med Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="a9a68-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="a9a68-108">Installer Project Operations i et nytt CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="a9a68-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="a9a68-109">Installer i et eksisterende CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="a9a68-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="a9a68-110">Installer Project Operations i et nytt CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="a9a68-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="a9a68-111">Som [global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-lisens oppretter du et nytt CDS-miljø i [administrasjonssenteret for Power Platform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="a9a68-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="a9a68-112">Kontroller at **CDS-database** og **Dynamics 365-apper** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="a9a68-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="a9a68-113">Hvis du vil ha mer informasjon, kan du se [Opprette og administrere miljøer i Power Platform-administrasjonssenteret](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="a9a68-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="a9a68-114">Velg **Microsoft Dynamics 365 Project Operations** fra distribusjonslisten over Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="a9a68-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="a9a68-115">Installer Project Operations i et eksisterende CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="a9a68-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="a9a68-116">Som [global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-lisens finner du miljøet i [administrasjonssenteret for Power Platform](https://admin.powerplatform.com) der du ønsker å installere Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a9a68-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="a9a68-117">Installer **Microsoft Dynamics 365 Project Operations** fra distribusjonslisten over Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="a9a68-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="a9a68-118">Hvis du vil ha mer informasjon, kan du se [Administrere Dynamics 365-apper](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="a9a68-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]