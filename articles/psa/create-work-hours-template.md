---
title: Opprette en mal for arbeidstimer
description: Dette emnet beskriver hvordan du oppretter en mal for arbeidstimer i Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981267"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="8dc0a-103">Opprette en mal for arbeidstimer (Project Service)</span><span class="sxs-lookup"><span data-stu-id="8dc0a-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8dc0a-104">Hvis du vil opprette og administrere et prosjekt, må du bruke en kalendermal på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="8dc0a-105">Kalendermalen definerer følgende prosjektattributter:</span><span class="sxs-lookup"><span data-stu-id="8dc0a-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="8dc0a-106">Arbeidstid, inkludert start- og sluttidspunkt</span><span class="sxs-lookup"><span data-stu-id="8dc0a-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="8dc0a-107">Arbeidsdager</span><span class="sxs-lookup"><span data-stu-id="8dc0a-107">Working days</span></span>
- <span data-ttu-id="8dc0a-108">Kalenderunntak, for eksempel fridager</span><span class="sxs-lookup"><span data-stu-id="8dc0a-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="8dc0a-109">Kalendermalen som brukes på et prosjekt, er en kopi av kalendermalen som er definert i organisasjonens innstillinger.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="8dc0a-110">Hvis du endrer kalendermalen, overføres ikke disse endringene til arbeidstiden for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="8dc0a-111">Hvis du vil endre arbeidstiden for prosjektet, må du bruke en ny mal.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="8dc0a-112">Hvis du vil opprette en kalendermal for organisasjonen, er det to viktige krav:</span><span class="sxs-lookup"><span data-stu-id="8dc0a-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="8dc0a-113">Definer ønsket arbeidstid for malen ved hjelp av en ny eller eksisterende ressurs som kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="8dc0a-114">Opprett en ny kalendermal, og knytt malen til ressursen som kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="8dc0a-115">**Definer arbeidstimene for malen**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="8dc0a-116">Gå til **Ressurser** \> **Ressurser**.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="8dc0a-117">Opprett en ny ressurs som skal refereres til i kalendermalen, eller velg en eksisterende ressurs.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="8dc0a-118">Velg kategorien **Arbeidstimer** for ressursen, og fullfør instruksjonene i [Angi arbeidstimer for en ressurs](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) for å konfigurere kalenderreglene.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="8dc0a-119">**Opprett en ny kalendermal**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="8dc0a-120">Gå til **Innstillinger** \> **Kalendermal**.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="8dc0a-121">Velg **Ny**, og skriv inn et navn, en beskrivelse og en malressurs.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="8dc0a-122">Når det refereres til en ressurs i en kalendermal, knyttes en kopi av ressursens kalender til kalendermalen.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="8dc0a-123">Hvis arbeidstimene for den kopierte malen endres, overføres ikke disse endringene til kalendermalen.</span><span class="sxs-lookup"><span data-stu-id="8dc0a-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="8dc0a-124">Se også</span><span class="sxs-lookup"><span data-stu-id="8dc0a-124">See Also</span></span>  
 [<span data-ttu-id="8dc0a-125">Definere ressurser</span><span class="sxs-lookup"><span data-stu-id="8dc0a-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
