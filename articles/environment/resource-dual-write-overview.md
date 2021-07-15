---
title: Integrering av dobbel skriving for Project Operations
description: Dette emnet gir en oversikt over integrering av dobbel skriving for Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368443"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="4c75a-103">Oversikt over integrering av dobbel skriving for Project Operations</span><span class="sxs-lookup"><span data-stu-id="4c75a-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="4c75a-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="4c75a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4c75a-105">Project Operations bruker [funksjoner for dobbel skriving](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) til å synkronisere data på tvers av Microsoft Dataverse og Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="4c75a-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="4c75a-106">Illustrasjonen nedenfor viser hvordan data synkroniseres som en del av denne integrasjonen mellom Dataverse og Finance.</span><span class="sxs-lookup"><span data-stu-id="4c75a-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Oversikt over dataflyter for Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="4c75a-108">Project Operations i Dataverse gi et moderne brukergrensesnitt (UI) og enkel utvidelse med ingen kode / lav kode ved hjelp av Power Platform-funksjoner.</span><span class="sxs-lookup"><span data-stu-id="4c75a-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="4c75a-109">Prosjektledere, ressursledere, prosjektteammedlemmer og andre personer på kontoret utfører aktivitetene sine i Project Operations på Dataverse.</span><span class="sxs-lookup"><span data-stu-id="4c75a-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="4c75a-110">Project Operations i Finance gir støtte for prosjektregnskap og inntektsføring.</span><span class="sxs-lookup"><span data-stu-id="4c75a-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="4c75a-111">Project Operations kobles inn i det økonomiske rammeverket i Finance for beregning av salgsavgift, valutakurser, rapportering av finansielle dimensjoner og mer.</span><span class="sxs-lookup"><span data-stu-id="4c75a-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="4c75a-112">Opplevelsene til prosjektregnskapsføreren er for det meste basert i Finans.</span><span class="sxs-lookup"><span data-stu-id="4c75a-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="4c75a-113">Integrering av Project Operations består av følgende komponentintegrering:</span><span class="sxs-lookup"><span data-stu-id="4c75a-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="4c75a-114">Integrering av Project Operations-oppsett og -konfigurasjonsdata</span><span class="sxs-lookup"><span data-stu-id="4c75a-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="4c75a-115">Prosjektestimater og faktiske verdier</span><span class="sxs-lookup"><span data-stu-id="4c75a-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="4c75a-116">Prosjektfakturaer</span><span class="sxs-lookup"><span data-stu-id="4c75a-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="4c75a-117">Utgiftshåndtering</span><span class="sxs-lookup"><span data-stu-id="4c75a-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="4c75a-118">Leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="4c75a-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
