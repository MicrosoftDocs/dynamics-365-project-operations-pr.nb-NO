---
title: Opprette en mal for arbeidstimer
description: Dette emnet beskriver hvordan du oppretter en mal for arbeidstimer i Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997208"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="79cbd-103">Opprette en mal for arbeidstimer (Project Service)</span><span class="sxs-lookup"><span data-stu-id="79cbd-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="79cbd-104">Hvis du vil opprette og administrere et prosjekt, må du bruke en kalendermal på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="79cbd-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="79cbd-105">Kalendermalen definerer følgende prosjektattributter:</span><span class="sxs-lookup"><span data-stu-id="79cbd-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="79cbd-106">Arbeidstid, inkludert start- og sluttidspunkt</span><span class="sxs-lookup"><span data-stu-id="79cbd-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="79cbd-107">Arbeidsdager</span><span class="sxs-lookup"><span data-stu-id="79cbd-107">Working days</span></span>
- <span data-ttu-id="79cbd-108">Kalenderunntak, for eksempel fridager</span><span class="sxs-lookup"><span data-stu-id="79cbd-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="79cbd-109">Kalendermalen som brukes på et prosjekt, er en kopi av kalendermalen som er definert i organisasjonens innstillinger.</span><span class="sxs-lookup"><span data-stu-id="79cbd-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="79cbd-110">Hvis du endrer kalendermalen, overføres ikke disse endringene til arbeidstiden for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="79cbd-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="79cbd-111">Hvis du vil endre arbeidstiden for prosjektet, må du bruke en ny mal.</span><span class="sxs-lookup"><span data-stu-id="79cbd-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="79cbd-112">Hvis du vil opprette en kalendermal for organisasjonen, er det to viktige krav:</span><span class="sxs-lookup"><span data-stu-id="79cbd-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="79cbd-113">Definer ønsket arbeidstid for malen ved hjelp av en ny eller eksisterende ressurs som kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="79cbd-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="79cbd-114">Opprett en ny kalendermal, og knytt malen til ressursen som kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="79cbd-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="79cbd-115">**Definer arbeidstimene for malen**</span><span class="sxs-lookup"><span data-stu-id="79cbd-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="79cbd-116">Gå til **Ressurser** \> **Ressurser**.</span><span class="sxs-lookup"><span data-stu-id="79cbd-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="79cbd-117">Opprett en ny ressurs som skal refereres til i kalendermalen, eller velg en eksisterende ressurs.</span><span class="sxs-lookup"><span data-stu-id="79cbd-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="79cbd-118">Velg kategorien **Arbeidstimer** for ressursen, og fullfør instruksjonene i [Angi arbeidstimer for en ressurs](/dynamics365/field-service/set-work-hours-resource.md) for å konfigurere kalenderreglene.</span><span class="sxs-lookup"><span data-stu-id="79cbd-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="79cbd-119">**Opprett en ny kalendermal**</span><span class="sxs-lookup"><span data-stu-id="79cbd-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="79cbd-120">Gå til **Innstillinger** \> **Kalendermal**.</span><span class="sxs-lookup"><span data-stu-id="79cbd-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="79cbd-121">Velg **Ny**, og skriv inn et navn, en beskrivelse og en malressurs.</span><span class="sxs-lookup"><span data-stu-id="79cbd-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="79cbd-122">Når det refereres til en ressurs i en kalendermal, knyttes en kopi av ressursens kalender til kalendermalen.</span><span class="sxs-lookup"><span data-stu-id="79cbd-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="79cbd-123">Hvis arbeidstimene for den kopierte malen endres, overføres ikke disse endringene til kalendermalen.</span><span class="sxs-lookup"><span data-stu-id="79cbd-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="79cbd-124">Se også</span><span class="sxs-lookup"><span data-stu-id="79cbd-124">See Also</span></span>  
 [<span data-ttu-id="79cbd-125">Definere ressurser</span><span class="sxs-lookup"><span data-stu-id="79cbd-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
