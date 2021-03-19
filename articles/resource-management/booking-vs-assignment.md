---
title: Bestillinger i forhold til tildelinger
description: Dette emnet inneholder informasjon om forskjellene mellom ressursbestillinger og ressurstildelinger.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279915"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="94208-103">Bestillinger i forhold til tildelinger</span><span class="sxs-lookup"><span data-stu-id="94208-103">Bookings vs assignments</span></span>

<span data-ttu-id="94208-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="94208-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="94208-105">Bestillinger er forpliktende eller ikke-forpliktende tildeling av ressurser i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="94208-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="94208-106">Forpliktende bestillinger bruker kapasiteten til en ressurs.</span><span class="sxs-lookup"><span data-stu-id="94208-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="94208-107">Bestillinger representerer organisasjonskonsepter for team, slik at de kan forstå hvordan ressurser skal fordeles på forskjellige prosjekter.</span><span class="sxs-lookup"><span data-stu-id="94208-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="94208-108">Dynamics 365 Project Operations vurderer bestillinger som et konsept på prosjektnivå.</span><span class="sxs-lookup"><span data-stu-id="94208-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="94208-109">I motsetning til bestillinger er tilordninger ressursforpliktelser til prosjektoppgaver i prosjektplanen.</span><span class="sxs-lookup"><span data-stu-id="94208-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="94208-110">Ressursene kan navngis eller være generiske.</span><span class="sxs-lookup"><span data-stu-id="94208-110">The resources can be named or generic.</span></span>  <span data-ttu-id="94208-111">Når et ressurskrav avledes av prosjektoppgavetilordningene, bruker Project Operations innsatsen for ressurstilordningen til å bygge opp ressurskravdetaljene.</span><span class="sxs-lookup"><span data-stu-id="94208-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="94208-112">Ressurstilordningene blir imidlertid ikke opprettholdt.</span><span class="sxs-lookup"><span data-stu-id="94208-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="94208-113">Oppdateringer for bestillinger som er avledet fra ressurskravet, oppdaterer ikke ressurstilordninger.</span><span class="sxs-lookup"><span data-stu-id="94208-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="94208-114">Vanligvis vil summen av bestillinger for en ressurs tilsvare summen av ressursens tilordninger på tvers av én eller flere oppgaver.</span><span class="sxs-lookup"><span data-stu-id="94208-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="94208-115">Project Operations håndhever imidlertid ikke denne avtalen.</span><span class="sxs-lookup"><span data-stu-id="94208-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="94208-116">**Avstemming**-visningen viser en prosjektleder steder der bestillingene og tildelingene til en ressurs ikke er de samme.</span><span class="sxs-lookup"><span data-stu-id="94208-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]