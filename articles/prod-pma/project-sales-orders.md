---
title: Prosjektsalgsordrer for tids og materialprosjekter
description: Dette emnet forklarer hvordan du oppretter prosjektbaserte salgsordrer for tids- og materialprosjekter.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009673"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="7fe5c-103">Prosjektsalgsordrer for tids og materialprosjekter</span><span class="sxs-lookup"><span data-stu-id="7fe5c-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7fe5c-104">Dette emnet beskriver hvordan du oppretter en salgsordre for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="7fe5c-105">Salgsordrer kan bare opprettes for prosjekter av typen **tid og materiale**.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="7fe5c-106">Hvis et tid og materiale-prosjekt har flere finansieringskilder i prosjektkontrakten, må du aktivere parameteren **Tillat salgsordrer for prosjekter med flere finansieringskilder** på siden **Parametere for prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="7fe5c-107">Støtte for prosjektsalgsordrer som har flere finansieringskilder, er tilgjengelig fra programutgivelse 10.0.2 og nyere.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="7fe5c-108">Parameteren for å aktivere støtten for prosjektsalgsordrer med flere finansieringskilder, blir fjernet i april 2020-utgivelsesbølgen, og etter dette vil funksjonaliteten alltid være aktivert.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="7fe5c-109">Du kan opprette prosjektbaserte salgsordrer på to måter:</span><span class="sxs-lookup"><span data-stu-id="7fe5c-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="7fe5c-110">Gå til selve prosjektet.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-110">Go to the project itself.</span></span> <span data-ttu-id="7fe5c-111">I handlingsruten velger du **Behandle > Vareoppgaver > Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="7fe5c-112">Prosjektinformasjonen settes som standard til salgsordren fra prosjektet.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="7fe5c-113">Hvis prosjektkontrakten har mer enn én finansieringskilde, må du velge finansieringskilden for å angi kunden for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="7fe5c-114">Hvis det bare er én finansieringskilde for prosjektet, blir kunden angitt automatisk.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="7fe5c-115">Gå til listesiden **Alle salgsordrer**, og opprett en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="7fe5c-116">Du må velge prosjektet for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="7fe5c-117">Etter at du har valgt prosjektet, blir kunden angitt fra finansieringskilden, eller du må velge finansieringskilden hvis prosjektkontrakten har flere finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="7fe5c-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]