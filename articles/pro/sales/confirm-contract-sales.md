---
title: Bekrefte en prosjektkontrakt
description: Dette emnet gir informasjon om hvordan du bekrefter en kontrakt i Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003688"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="659a3-103">Bekrefte en prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="659a3-103">Confirm a project contract</span></span>

<span data-ttu-id="659a3-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="659a3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="659a3-105">En prosjektkontrakt i Dynamics 365 Project Operations kan være aktiv med årsaken **Bekreftet** eller lukket med årsaken **Tapt**.</span><span class="sxs-lookup"><span data-stu-id="659a3-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="659a3-106">Når du bekrefter en prosjektkontrakt, oppdateres statusen fra **Utkast** til **Aktiv**, og statusårsaken er **Bekreftet**.</span><span class="sxs-lookup"><span data-stu-id="659a3-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="659a3-107">En aktiv eller lukket kontrakt kan ikke redigeres eller åpnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="659a3-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="659a3-108">Økonomisk innvirkning av å bekrefte en prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="659a3-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="659a3-109">Når en prosjektkontrakt er bekreftet, vil programmet kostnadene på nytt ved å reversere de eldre faktiske kostnadsverdiene og opprette nye faktiske kostnadsverdier.</span><span class="sxs-lookup"><span data-stu-id="659a3-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="659a3-110">Disse nye faktiske kostnadsverdiene behandles deretter basert på faktureringsmetoden for den tilknyttede prosjektkontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="659a3-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="659a3-111">Hvis de faktiske kostnadsverdiene refererer til en kontraktlinje av typen Tid og materiale, oppretter programmet automatisk de tilsvarende ufakturerte faktiske salgsverdiene på nytt.</span><span class="sxs-lookup"><span data-stu-id="659a3-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="659a3-112">Hvis de faktiske kostnadsverdiene refererer til en kontraktlinje med fast pris, slutter programmet å behandle de faktiske kostnadene på nytt.</span><span class="sxs-lookup"><span data-stu-id="659a3-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="659a3-113">Grenser som ikke må overskrides, oppsett av belastbarhet og priser og kostnadsberegning for de faktiske verdiene evalueres og oppdateres deretter som en del av bekreftelsesprosessen.</span><span class="sxs-lookup"><span data-stu-id="659a3-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="659a3-114">Lukke en prosjektkontrakt som tapt</span><span class="sxs-lookup"><span data-stu-id="659a3-114">Close a project contract as lost</span></span>

<span data-ttu-id="659a3-115">Når du lukker en prosjektkontrakt som tapt, oppdateres kontraktstatusen til **Lukket**, og statusårsaken er **Tapt**.</span><span class="sxs-lookup"><span data-stu-id="659a3-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="659a3-116">Prosjektkontrakten blir skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="659a3-116">The project contract becomes read-only.</span></span> <span data-ttu-id="659a3-117">Det finnes en bekreftelsesdialogboks før endringene fullføres, fordi du ikke kan åpne en lukket prosjektkontrakt på nytt.</span><span class="sxs-lookup"><span data-stu-id="659a3-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="659a3-118">Hvis prosjektkontrakten som er lukket som tapt, refererer til et prosjekt på sine linjer, blir dette prosjektet også merket som lukket.</span><span class="sxs-lookup"><span data-stu-id="659a3-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="659a3-119">Eventuelle ressursbestillinger fra den dagen og fremover annulleres.</span><span class="sxs-lookup"><span data-stu-id="659a3-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="659a3-120">Eventuelle ikke-fakturerte faktiske salgsverdier i prosjektkontrakten som ikke allerede er på en faktura, blir tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="659a3-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="659a3-121">Hvis du lukker en prosjektkontrakt som tapt, påvirker ikke dette statusen for den tilknyttede salgsmuligheten i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="659a3-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="659a3-122">Salgsmuligheten forblir åpen og må lukkes manuelt.</span><span class="sxs-lookup"><span data-stu-id="659a3-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]