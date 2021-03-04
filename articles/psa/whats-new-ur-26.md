---
title: Hva er nytt eller endret i Project Service Automation Update Release 26, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143570"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="cfa8a-103">Project Service Automation, Update Release 26, V3</span><span class="sxs-lookup"><span data-stu-id="cfa8a-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cfa8a-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cfa8a-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cfa8a-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cfa8a-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cfa8a-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cfa8a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cfa8a-109">Dette emnet viser funksjonene og rettinger som er nye eller endrede for Project Service Automation Update Release 26, V3.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="cfa8a-110">Denne versjonen har et build-nummer for V 3.10.44.59, og er generelt tilgjengelig via en egen oppdatering i desember 2020.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="cfa8a-111">Update Release 26</span><span class="sxs-lookup"><span data-stu-id="cfa8a-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cfa8a-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="cfa8a-112">Bug fixes</span></span>

<span data-ttu-id="cfa8a-113">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="cfa8a-113">**Time and Expense**</span></span>

<span data-ttu-id="cfa8a-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="cfa8a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cfa8a-115">Brukere kan endre oppgaven i en tidsoppføring som er godkjent/sendt.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="cfa8a-116">«Objektreferanse er ikke angitt»-feilmelding under lagring av tidsoppføring.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="cfa8a-117">Tidsoppføringimport fra ressurstildelinger oppretter tidsoppføringer med feil dato/klokkeslett-verdier.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="cfa8a-118">Når både Project Service Automation- og Field Service-appen er installert, vises **Ny**-knappen to ganger på kommandolinjen for tidsoppføringer i Field Service-appen.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="cfa8a-119">**Tillat enhet** og **Enhetsgruppe**-celleoppdateringer fungerer nå på **Utgiftsestimat**-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="cfa8a-120">**Oppdater redigering for tidsoppføring**-skjema inkluderer **Tidslinje**.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="cfa8a-121">Tidsgodkjenning for tidsoppføringer som ikke er prosjekt, blokkerer systemet ved søk etter en prosjektgodkjennerrolle.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="cfa8a-122">**Ressursbehandling**</span><span class="sxs-lookup"><span data-stu-id="cfa8a-122">**Resource Management**</span></span>

<span data-ttu-id="cfa8a-123">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="cfa8a-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="cfa8a-124">Ekstra validering i **PostProjectCreate**-programtillegget for å se etter et primært krav før du oppretter et.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="cfa8a-125">**Prosjektteammedlem**-hurtigopprettingsskjema genererer et nullreferanseunntak hvis felt fjernes fra skjemaet.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="cfa8a-126">Generering av krav for 12 timer over 1 år vil mislykkes.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="cfa8a-127">Forbedret feilmelding om nullreferanseunntak under oppretting av ressurskrav.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="cfa8a-128">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="cfa8a-128">**Project Management**</span></span>

<span data-ttu-id="cfa8a-129">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="cfa8a-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="cfa8a-130">Forbedret validering for å løse nullreferanseunntak generert i **PreProjectUpdate**-programtillegget.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="cfa8a-131">Prosjekter som publiseres av Microsoft Project-tilleggsprogrammet, sletter oppgaver som ikke er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="cfa8a-132">Ekstra ny validering når en prosjektreferanse for en oppgave er ugyldig på grunn av nullreferanseunntak i **PreValidateProjectTaskUpdate**-programtillegget.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="cfa8a-133">Teammedlem-rutenettet viser ikke forskjellige tildelinger på teammedlemsoppføringen.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="cfa8a-134">Ekstra ny validering og feilmeldinger som skyldes nullreferanseunntak i **PreProjectTaskDelete**-programtillegget.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="cfa8a-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cfa8a-135">**Sales**</span></span>

<span data-ttu-id="cfa8a-136">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="cfa8a-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="cfa8a-137">Når du velger en prosjektbasert linje i tilbud eller kontrakt, skal **Forslag**-knappen kun være synlig når du velger en produktbasert linje som er tilknyttet et eksisterende produkt.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="cfa8a-138">Dele **Create_Product**-rettighet fra **Create_ProjectContracts**-rettighet.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="cfa8a-139">Sletting av en fakturalinje forårsaker nullreferansefeil på **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="cfa8a-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
