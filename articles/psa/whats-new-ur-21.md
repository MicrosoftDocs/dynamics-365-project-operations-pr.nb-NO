---
title: Hva er nytt eller endret i Project Service Automation Update Release 21, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 21, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: ad44f6747486222cc1f48c7b645f2525d382dca3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949061"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="b1264-103">Project Service Automation, Update Release 21, V3</span><span class="sxs-lookup"><span data-stu-id="b1264-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b1264-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b1264-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b1264-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="b1264-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b1264-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b1264-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b1264-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="b1264-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b1264-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b1264-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b1264-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 21.</span><span class="sxs-lookup"><span data-stu-id="b1264-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="b1264-110">Denne versjonen har et build-nummer på V 3.10.32.50 og er generelt tilgjengelig via en egen oppdatering i juni 2020.</span><span class="sxs-lookup"><span data-stu-id="b1264-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="b1264-111">Update Release 21</span><span class="sxs-lookup"><span data-stu-id="b1264-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b1264-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="b1264-112">Bug fixes</span></span>

<span data-ttu-id="b1264-113">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="b1264-113">**Time and Expense**</span></span>

<span data-ttu-id="b1264-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="b1264-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b1264-115">Når du bruker **Rutenett for tidsoppføring**-kontrollen på instrumentbordet, bruker ikke rutenettet full bredde på beholderen i instrumentbordrutenettet.</span><span class="sxs-lookup"><span data-stu-id="b1264-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="b1264-116">Når det gjelder spesifikke tidssoner, viser ikke **Tidsoppføring**-rutenettkontrollen visningsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="b1264-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="b1264-117">Tidsoppføringer som er etter 9:00 PM, vises på feil dag.</span><span class="sxs-lookup"><span data-stu-id="b1264-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="b1264-118">Brukere kan ikke sende utgifter hvis utgiftskategorien for **utgiftskvittering kreves** ikke har noen verdi.</span><span class="sxs-lookup"><span data-stu-id="b1264-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="b1264-119">**Ressursbehandling**</span><span class="sxs-lookup"><span data-stu-id="b1264-119">**Resource Management**</span></span>

<span data-ttu-id="b1264-120">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="b1264-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="b1264-121">Inaktive bestillinger vises i **Avstemming**-visningen.</span><span class="sxs-lookup"><span data-stu-id="b1264-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="b1264-122">Generell ressursfullføring mangler validering for å sikre at det finnes en gyldig bestillingsstatus.</span><span class="sxs-lookup"><span data-stu-id="b1264-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="b1264-123">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="b1264-123">**Project Management**</span></span>

<span data-ttu-id="b1264-124">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="b1264-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="b1264-125">**Prosjekt**-skjemarutenettene (**Ressurstilordning**, **Oppgave**, **Avstemming**-visning, **Utgiftsestimater**) forblir redigerbare selv når et prosjekt ikke er aktivt.</span><span class="sxs-lookup"><span data-stu-id="b1264-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="b1264-126">Dupliserte kunder kan ikke flettes med kunder som er koblet til bekreftede prosjektkontrakter.</span><span class="sxs-lookup"><span data-stu-id="b1264-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="b1264-127">Når en ressurs som ikke har en gyldig kalender, blir lagt til, returnerer ikke systemet en brukervennlig feilmelding.</span><span class="sxs-lookup"><span data-stu-id="b1264-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="b1264-128">Knappen **Legg til oppgave** i oppgaverutenettet er aktivert når prosjektet er koblet til **Microsoft Project-tillegget**.</span><span class="sxs-lookup"><span data-stu-id="b1264-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="b1264-129">Innsatsen vokser ukontrollerbart når en oppgave med en kategori tilordnes en ressurs med en rolle som det er definert en kostnadspris for.</span><span class="sxs-lookup"><span data-stu-id="b1264-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="b1264-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="b1264-130">**Sales**</span></span>

<span data-ttu-id="b1264-131">Følgende forbedringer er gjort:</span><span class="sxs-lookup"><span data-stu-id="b1264-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="b1264-132">**Fakturafrekvens** og **Startdato for fakturering** er flyttet til kategorien **Fakturaplan**.</span><span class="sxs-lookup"><span data-stu-id="b1264-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="b1264-133">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="b1264-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="b1264-134">**Total salgspris** er null (0) for **Kategori** selv om **Rolle** har en total salgspris som ikke er null.</span><span class="sxs-lookup"><span data-stu-id="b1264-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="b1264-135">Kunder kan ikke endre verdien i **Fakturastatus**-feltet til **Klar for fakturering** når en annen tilpasset prosess oppdaterer et ekstra felt.</span><span class="sxs-lookup"><span data-stu-id="b1264-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="b1264-136">Knappen for **oppdatering av fakturalinjer** kan opprette flere dupliserte linjer hvis den velges gjentatte ganger.</span><span class="sxs-lookup"><span data-stu-id="b1264-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="b1264-137">Knappen **Oppdater priser** fungerer ikke i delrutenettet **Rollepriser** i skjemaet **Hurtigvisning**.</span><span class="sxs-lookup"><span data-stu-id="b1264-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="b1264-138">**Salgsprislisteoppløsning**-logikken håndterer tidssoner på feil måte, noe som resulterer i feil valg av prislister.</span><span class="sxs-lookup"><span data-stu-id="b1264-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="b1264-139">En prosjekts **Total faktisk kostnad** kan avvike med en brøkdel når én enkelt tidsoppføring er godkjent.</span><span class="sxs-lookup"><span data-stu-id="b1264-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="b1264-140">Logikken for **prisløsning** gir ikke en brukervennlig feilmelding hvis **innhentet rollepris** ikke har verdier i feltene **Primærenhet** og **Pris i primærenhet**.</span><span class="sxs-lookup"><span data-stu-id="b1264-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]