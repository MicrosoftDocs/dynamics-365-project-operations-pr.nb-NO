---
title: Bestillinger i forhold til tildelinger
description: Dette emnet inneholder informasjon om forskjellene mellom ressursbestillinger og ressurstildelinger.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012778"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="ab179-103">Bestillinger i forhold til tildelinger</span><span class="sxs-lookup"><span data-stu-id="ab179-103">Bookings vs assignments</span></span>

<span data-ttu-id="ab179-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="ab179-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ab179-105">Bestillinger er forpliktende eller ikke-forpliktende tildeling av ressurser i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="ab179-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="ab179-106">Forpliktende bestillinger bruker kapasiteten til en ressurs.</span><span class="sxs-lookup"><span data-stu-id="ab179-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="ab179-107">Bestillinger representerer organisasjonskonsepter for team, slik at de kan forstå hvordan ressurser skal fordeles på forskjellige prosjekter.</span><span class="sxs-lookup"><span data-stu-id="ab179-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="ab179-108">Dynamics 365 Project Operations vurderer bestillinger som et konsept på prosjektnivå.</span><span class="sxs-lookup"><span data-stu-id="ab179-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="ab179-109">I motsetning til bestillinger er tilordninger ressursforpliktelser til prosjektoppgaver i prosjektplanen.</span><span class="sxs-lookup"><span data-stu-id="ab179-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="ab179-110">Ressursene kan navngis eller være generiske.</span><span class="sxs-lookup"><span data-stu-id="ab179-110">The resources can be named or generic.</span></span>  <span data-ttu-id="ab179-111">Når et ressurskrav avledes av prosjektoppgavetilordningene, bruker Project Operations innsatsen for ressurstilordningen til å bygge opp ressurskravdetaljene.</span><span class="sxs-lookup"><span data-stu-id="ab179-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="ab179-112">Ressurstilordningene blir imidlertid ikke opprettholdt.</span><span class="sxs-lookup"><span data-stu-id="ab179-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="ab179-113">Oppdateringer for bestillinger som er avledet fra ressurskravet, oppdaterer ikke ressurstilordninger.</span><span class="sxs-lookup"><span data-stu-id="ab179-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="ab179-114">Vanligvis vil summen av bestillinger for en ressurs tilsvare summen av ressursens tilordninger på tvers av én eller flere oppgaver.</span><span class="sxs-lookup"><span data-stu-id="ab179-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="ab179-115">Project Operations håndhever imidlertid ikke denne avtalen.</span><span class="sxs-lookup"><span data-stu-id="ab179-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="ab179-116">**Avstemming**-visningen viser en prosjektleder steder der bestillingene og tildelingene til en ressurs ikke er de samme.</span><span class="sxs-lookup"><span data-stu-id="ab179-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]