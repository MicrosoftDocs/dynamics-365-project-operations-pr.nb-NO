---
title: Definer prosjektkalendere
description: Dette emnet gir informasjon om hvordan du bruker en kalendermal på et prosjekt til å følge opp prosjektplanen.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981312"
---
# <a name="define-project-calendars"></a><span data-ttu-id="5ef52-103">Definer prosjektkalendere</span><span class="sxs-lookup"><span data-stu-id="5ef52-103">Define project calendars</span></span>

<span data-ttu-id="5ef52-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="5ef52-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5ef52-105">Hvis du vil opprette og administrere et prosjekt, må du bruke en kalendermal på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="5ef52-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="5ef52-106">Kalendermalen definerer følgende prosjektattributter:</span><span class="sxs-lookup"><span data-stu-id="5ef52-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="5ef52-107">Arbeidstid, inkludert start- og sluttidspunkt</span><span class="sxs-lookup"><span data-stu-id="5ef52-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="5ef52-108">Arbeidsdager</span><span class="sxs-lookup"><span data-stu-id="5ef52-108">Working days</span></span>
- <span data-ttu-id="5ef52-109">Kalenderunntak, for eksempel fridager</span><span class="sxs-lookup"><span data-stu-id="5ef52-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="5ef52-110">Kalendermalen som brukes på et prosjekt, er en kopi av kalendermalen som er definert i organisasjonens innstillinger.</span><span class="sxs-lookup"><span data-stu-id="5ef52-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="5ef52-111">Hvis du endrer kalendermalen, overføres ikke disse endringene til arbeidstiden for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="5ef52-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="5ef52-112">Hvis du vil endre arbeidstiden for prosjektet, må du bruke en ny mal.</span><span class="sxs-lookup"><span data-stu-id="5ef52-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="5ef52-113">Hvis du vil opprette en kalendermal for organisasjonen, er det to viktige krav:</span><span class="sxs-lookup"><span data-stu-id="5ef52-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="5ef52-114">Definer ønsket arbeidstid for malen ved hjelp av en ny eller eksisterende ressurs som kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="5ef52-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="5ef52-115">Opprett en ny kalendermal, og knytt malen til ressursen som kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="5ef52-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="5ef52-116">**Definer arbeidstimene for malen**</span><span class="sxs-lookup"><span data-stu-id="5ef52-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="5ef52-117">Gå til **Ressurser** \> **Ressurser**.</span><span class="sxs-lookup"><span data-stu-id="5ef52-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="5ef52-118">Opprett en ny ressurs som skal refereres til i kalendermalen, eller velg en eksisterende ressurs.</span><span class="sxs-lookup"><span data-stu-id="5ef52-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="5ef52-119">Velg kategorien **Arbeidstimer** for ressursen, og fullfør instruksjonene i [Angi arbeidstimer for en ressurs](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) for å konfigurere kalenderreglene.</span><span class="sxs-lookup"><span data-stu-id="5ef52-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="5ef52-120">**Opprett en ny kalendermal**</span><span class="sxs-lookup"><span data-stu-id="5ef52-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="5ef52-121">Gå til **Innstillinger** \> **Kalendermal**.</span><span class="sxs-lookup"><span data-stu-id="5ef52-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="5ef52-122">Velg **Ny**, og skriv inn et navn, en beskrivelse og en malressurs.</span><span class="sxs-lookup"><span data-stu-id="5ef52-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="5ef52-123">Når det refereres til en ressurs i en kalendermal, knyttes en kopi av ressursens kalender til kalendermalen.</span><span class="sxs-lookup"><span data-stu-id="5ef52-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="5ef52-124">Hvis arbeidstimene for den kopierte malen endres, overføres ikke disse endringene til kalendermalen.</span><span class="sxs-lookup"><span data-stu-id="5ef52-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="5ef52-125">Du kan nå knytte arbeidsmalen til en prosjektkKalendermal.</span><span class="sxs-lookup"><span data-stu-id="5ef52-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

