---
title: Hva er nytt eller endret i Project Service Automation Update Release 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643275"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="2f810-102">Project Service Automation, Update Release 26, V3</span><span class="sxs-lookup"><span data-stu-id="2f810-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="2f810-103">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2f810-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2f810-104">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="2f810-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2f810-105">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2f810-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2f810-106">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="2f810-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2f810-107">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2f810-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2f810-108">Dette emnet viser funksjonene og rettinger som er nye eller endrede for Project Service Automation Update Release 26, V3.</span><span class="sxs-lookup"><span data-stu-id="2f810-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="2f810-109">Denne versjonen har et build-nummer for V 3.10.44.59, og er generelt tilgjengelig via en egen oppdatering i desember 2020.</span><span class="sxs-lookup"><span data-stu-id="2f810-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="2f810-110">Update Release 26</span><span class="sxs-lookup"><span data-stu-id="2f810-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="2f810-111">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="2f810-111">Bug fixes</span></span>

<span data-ttu-id="2f810-112">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="2f810-112">**Time and Expense**</span></span>

<span data-ttu-id="2f810-113">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="2f810-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="2f810-114">Brukere kan endre oppgaven i en tidsoppføring som er godkjent/sendt.</span><span class="sxs-lookup"><span data-stu-id="2f810-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="2f810-115">«Objektreferanse er ikke angitt»-feilmelding under lagring av tidsoppføring.</span><span class="sxs-lookup"><span data-stu-id="2f810-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="2f810-116">Tidsoppføringimport fra ressurstildelinger oppretter tidsoppføringer med feil dato/klokkeslett-verdier.</span><span class="sxs-lookup"><span data-stu-id="2f810-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="2f810-117">Når både Project Service Automation- og Field Service-appen er installert, vises **Ny**-knappen to ganger på kommandolinjen for tidsoppføringer i Field Service-appen.</span><span class="sxs-lookup"><span data-stu-id="2f810-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="2f810-118">**Tillat enhet** og **Enhetsgruppe**-celleoppdateringer fungerer nå på **Utgiftsestimat**-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="2f810-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="2f810-119">**Oppdater redigering for tidsoppføring**-skjema inkluderer **Tidslinje**.</span><span class="sxs-lookup"><span data-stu-id="2f810-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="2f810-120">Tidsgodkjenning for tidsoppføringer som ikke er prosjekt, blokkerer systemet ved søk etter en prosjektgodkjennerrolle.</span><span class="sxs-lookup"><span data-stu-id="2f810-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="2f810-121">**Ressursbehandling**</span><span class="sxs-lookup"><span data-stu-id="2f810-121">**Resource Management**</span></span>

<span data-ttu-id="2f810-122">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="2f810-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="2f810-123">Ekstra validering i **PostProjectCreate**-programtillegget for å se etter et primært krav før du oppretter et.</span><span class="sxs-lookup"><span data-stu-id="2f810-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="2f810-124">**Prosjektteammedlem**-hurtigopprettingsskjema genererer et nullreferanseunntak hvis felt fjernes fra skjemaet.</span><span class="sxs-lookup"><span data-stu-id="2f810-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="2f810-125">Generering av krav for 12 timer over 1 år vil mislykkes.</span><span class="sxs-lookup"><span data-stu-id="2f810-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="2f810-126">Forbedret feilmelding om nullreferanseunntak under oppretting av ressurskrav.</span><span class="sxs-lookup"><span data-stu-id="2f810-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="2f810-127">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="2f810-127">**Project Management**</span></span>

<span data-ttu-id="2f810-128">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="2f810-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="2f810-129">Forbedret validering for å løse nullreferanseunntak generert i **PreProjectUpdate**-programtillegget.</span><span class="sxs-lookup"><span data-stu-id="2f810-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="2f810-130">Prosjekter som publiseres av Microsoft Project-tilleggsprogrammet, sletter oppgaver som ikke er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="2f810-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="2f810-131">Ekstra ny validering når en prosjektreferanse for en oppgave er ugyldig på grunn av nullreferanseunntak i **PreValidateProjectTaskUpdate**-programtillegget.</span><span class="sxs-lookup"><span data-stu-id="2f810-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="2f810-132">Teammedlem-rutenettet viser ikke forskjellige tildelinger på teammedlemsoppføringen.</span><span class="sxs-lookup"><span data-stu-id="2f810-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="2f810-133">Ekstra ny validering og feilmeldinger som skyldes nullreferanseunntak i **PreProjectTaskDelete**-programtillegget.</span><span class="sxs-lookup"><span data-stu-id="2f810-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="2f810-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="2f810-134">**Sales**</span></span>

<span data-ttu-id="2f810-135">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="2f810-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="2f810-136">Når du velger en prosjektbasert linje i tilbud eller kontrakt, skal **Forslag**-knappen kun være synlig når du velger en produktbasert linje som er tilknyttet et eksisterende produkt.</span><span class="sxs-lookup"><span data-stu-id="2f810-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="2f810-137">Dele **Create_Product**-rettighet fra **Create_ProjectContracts**-rettighet.</span><span class="sxs-lookup"><span data-stu-id="2f810-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="2f810-138">Sletting av en fakturalinje forårsaker nullreferansefeil på **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="2f810-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
