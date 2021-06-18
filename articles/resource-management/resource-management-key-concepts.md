---
title: Nøkkelkonsepter for ressursstyring
description: Dette emnet gir information om ressursstyringsfunksjonene i Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6362daab7e2e01c7b7b2c2b801fe7e258b21ef16
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000988"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="fc843-103">Nøkkelkonsepter for ressursstyring</span><span class="sxs-lookup"><span data-stu-id="fc843-103">Resource management key concepts</span></span>

<span data-ttu-id="fc843-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="fc843-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fc843-105">Ressurser er det viktigste aktivaet i en tjenestebasert organisasjon.</span><span class="sxs-lookup"><span data-stu-id="fc843-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="fc843-106">Muligheten til å finne de riktige ressursene til rett tid, bestille disse ressursene på prosjekter og sørge for at ressurser blir brukt, hjelper organisasjoner med å oppfylle omsetningsmål og kundetilfredshetsmål.</span><span class="sxs-lookup"><span data-stu-id="fc843-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="fc843-107">Du kan bruke prosjektbemanningsfunksjonaliteten i Dynamics 365 Project Operations til å gjøre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="fc843-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="fc843-108">Danne prosjektteam ved å bestille tilgjengelige og kvalifiserte ressurser.</span><span class="sxs-lookup"><span data-stu-id="fc843-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="fc843-109">Opprette generelle teammedlemsoppføringer og definere rollene og ressursorganisasjonsenheten.</span><span class="sxs-lookup"><span data-stu-id="fc843-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="fc843-110">Generere ressurskrav for generelle teammedlemmer fra oppgavetilordningene.</span><span class="sxs-lookup"><span data-stu-id="fc843-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="fc843-111">Samsvare ferdigheter ved å identifisere ferdighetene som er definert i ressursbehovet, mot tilgjengelig ressurskompetanse.</span><span class="sxs-lookup"><span data-stu-id="fc843-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="fc843-112">Erstatte ressurser.</span><span class="sxs-lookup"><span data-stu-id="fc843-112">Substitute resources.</span></span>
- <span data-ttu-id="fc843-113">Rette inn prosjektplantilordninger og ressursbestillinger.</span><span class="sxs-lookup"><span data-stu-id="fc843-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="fc843-114">Avstemme ulikheter i bestillinger og tilordninger.</span><span class="sxs-lookup"><span data-stu-id="fc843-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="fc843-115">Endre ressursbestillinger som svar på fraværsstatus.</span><span class="sxs-lookup"><span data-stu-id="fc843-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="fc843-116">Samarbeide mellom prosjektledere og ressursledere.</span><span class="sxs-lookup"><span data-stu-id="fc843-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="fc843-117">Vise historikken for ressursutnyttelsen mot et mål, inkludert en analyse av hvordan ressursens tid ble brukt.</span><span class="sxs-lookup"><span data-stu-id="fc843-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="fc843-118">Vedlikeholde kompetanse og ferdigheter.</span><span class="sxs-lookup"><span data-stu-id="fc843-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="fc843-119">Du kan bemanne prosjektet med et team med generelle eller navngitte ressurser i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fc843-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="fc843-120">Du kan bruke forskjellige metoder til å legge til og tilordne teammedlemmer og til å administrere bestillinger og tilordninger.</span><span class="sxs-lookup"><span data-stu-id="fc843-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]