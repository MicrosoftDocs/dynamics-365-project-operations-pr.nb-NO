---
title: Bestillinger i forhold til tildelinger
description: Dette emnet inneholder informasjon om forskjellene mellom ressursbestillinger og ressurstildelinger.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081469"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="edde0-103">Bestillinger i forhold til tildelinger</span><span class="sxs-lookup"><span data-stu-id="edde0-103">Bookings vs assignments</span></span>

<span data-ttu-id="edde0-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="edde0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="edde0-105">Bestillinger er forpliktende eller ikke-forpliktende tildeling av ressurser i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="edde0-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="edde0-106">Forpliktende bestillinger bruker kapasiteten til en ressurs.</span><span class="sxs-lookup"><span data-stu-id="edde0-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="edde0-107">Tildelinger er tilordningen av ressurser til prosjektoppgaver i prosjektplanen.</span><span class="sxs-lookup"><span data-stu-id="edde0-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="edde0-108">Ressursene kan være enten reelle ressurser eller generelle ressurser.</span><span class="sxs-lookup"><span data-stu-id="edde0-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="edde0-109">Ideelt sett bør bestillinger og tildelinger for reelle ressurser være de samme, fordi de ikke er forskjellige.</span><span class="sxs-lookup"><span data-stu-id="edde0-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="edde0-110">Microsoft Dynamics Project Operations håndhever imidlertid ikke denne avtalen.</span><span class="sxs-lookup"><span data-stu-id="edde0-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="edde0-111">**Avstemming** -visningen viser en prosjektleder steder der bestillingene og tildelingene til en ressurs ikke er de samme.</span><span class="sxs-lookup"><span data-stu-id="edde0-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
