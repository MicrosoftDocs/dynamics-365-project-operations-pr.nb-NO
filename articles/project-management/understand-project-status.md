---
title: Forstå prosjektstatus
description: Dette emnet inneholder informasjon om statusen som er tilordnet prosjekter i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ad8c012b93bc65595dca33df1770562916c557e0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993428"
---
# <a name="understand-project-status"></a><span data-ttu-id="648ce-103">Forstå prosjektstatus</span><span class="sxs-lookup"><span data-stu-id="648ce-103">Understand project status</span></span>

<span data-ttu-id="648ce-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="648ce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="648ce-105">Delen **Status** på siden **Prosjektenhet** inneholder et sammendrag over tilstanden til et prosjekt basert på kostnad og innsats.</span><span class="sxs-lookup"><span data-stu-id="648ce-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="648ce-106">Statussammendragsfelt</span><span class="sxs-lookup"><span data-stu-id="648ce-106">Status summary fields</span></span>

- <span data-ttu-id="648ce-107">Feltet **Generell prosjektstatus** er et redigerbart felt som viser den generelle statusen til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="648ce-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="648ce-108">Dette feltet bruker fargekoding, for eksempel grønn, gul og rød, for å vise økende risikoer.</span><span class="sxs-lookup"><span data-stu-id="648ce-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="648ce-109">Med **Kommentarer**-feltet kan prosjektlederen angi spesifikke kommentarer om statusen.</span><span class="sxs-lookup"><span data-stu-id="648ce-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="648ce-110">Feltet **Statusen oppdatert** kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="648ce-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="648ce-111">Verdien i dette feltet er et tidsstempel som angir når statusen sist ble oppdatert.</span><span class="sxs-lookup"><span data-stu-id="648ce-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="648ce-112">Feltene **Tidsplanytelse** og **Kostnadsytelse** angis fra sporingsrutenettet.</span><span class="sxs-lookup"><span data-stu-id="648ce-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="648ce-113">Når tidsplan- og kostnadsavviket for rotnoden i visningen **Innsatssporing** er positive, oppdateres disse feltene til **Foran**.</span><span class="sxs-lookup"><span data-stu-id="648ce-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="648ce-114">Når tidsplan- og kostnadsavviket for rotnoden er negativt, angis disse feltene til **Bak**.</span><span class="sxs-lookup"><span data-stu-id="648ce-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]