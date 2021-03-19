---
title: Foreslå prosjektressurser
description: Dette emnet gir informasjon om hvordan du foreslår prosjektressurser.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 2003f6f06912b0c47eb942aae17e509b00e19487
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283020"
---
# <a name="propose-project-resources"></a><span data-ttu-id="37514-103">Foreslå prosjektressurser</span><span class="sxs-lookup"><span data-stu-id="37514-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="37514-104">Ressursledere kan foreslå en ressurs til prosjektlederen ved å bruke en ressursforespørsel.</span><span class="sxs-lookup"><span data-stu-id="37514-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="37514-105">Fra rutenettet med forspørsler eller fra selve forespørselen velger du **Søk etter ressurser**.</span><span class="sxs-lookup"><span data-stu-id="37514-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="37514-106">På siden **Planleggingsassistent** velger du ressursen, og deretter i ruten **Opprett ressursbestilling**, i feltet **Bestillingsstatus**, velger du **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="37514-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Foreslått ressurs valgt](media/Resource-Management-image62.png)

<span data-ttu-id="37514-108">Følgende statusoppdateringer inntreffer:</span><span class="sxs-lookup"><span data-stu-id="37514-108">The following status updates occur:</span></span>

- <span data-ttu-id="37514-109">På siden **Planleggingsassistent** oppdateres statusindikatorene for å indikere at bestillingen er foreslått, ikke forpliktende bestilt.</span><span class="sxs-lookup"><span data-stu-id="37514-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Statusindikatorer for foreslått bestilling på siden Planleggingsassistent](media/Resource-Management-image63.png)

- <span data-ttu-id="37514-111">I ressursforespørselen endres statusen til **Må gjennomgås**.</span><span class="sxs-lookup"><span data-stu-id="37514-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Status for ressursforespørsel endret til Må gjennomgås](media/Resource-Management-image64.png)

- <span data-ttu-id="37514-113">I kategorien **Team** i prosjektet endres verdien for det generelle teammedlemmets **Forespørselsstatus** til **Må gjennomgås**.</span><span class="sxs-lookup"><span data-stu-id="37514-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Generelt teammedlems forespørselsstatus endret til Må gjennomgås i kategorien Team.](media/Resource-Management-image48.png)

<span data-ttu-id="37514-115">Prosjektlederen kan enten godta eller avvise forslaget.</span><span class="sxs-lookup"><span data-stu-id="37514-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="37514-116">Når ressursledere behandler ressursforespørsler, kan de bruke én av følgende metoder:</span><span class="sxs-lookup"><span data-stu-id="37514-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="37514-117">Foreslå flere ressurser for å tilfredsstille behovet hvis det ikke er noen enkelt ressurs tilgjengelig for å oppfylle de nødvendige timene.</span><span class="sxs-lookup"><span data-stu-id="37514-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="37514-118">Foreslåtte timer deles deretter mellom flere ressurser som kan oppfylle de nødvendige timene.</span><span class="sxs-lookup"><span data-stu-id="37514-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="37514-119">I dette scenariet kan ikke timene overlappe.</span><span class="sxs-lookup"><span data-stu-id="37514-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="37514-120">Foreslå færre ressurser enn nødvendig.</span><span class="sxs-lookup"><span data-stu-id="37514-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="37514-121">I dette scenariet er den foreslåtte ressurskapasiteten mindre enn de påkrevde timene som er angitt.</span><span class="sxs-lookup"><span data-stu-id="37514-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="37514-122">Når anmoderen godtar de foreslåtte ressursene, opprettes det derfor et ressurskrav som ikke er fullført, for å fange opp det gjenstående behovet.</span><span class="sxs-lookup"><span data-stu-id="37514-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="37514-123">Bestille flere ressurser for å tilfredsstille behovet hvis det ikke er noen enkelt ressurs tilgjengelig for å utføre arbeidet.</span><span class="sxs-lookup"><span data-stu-id="37514-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="37514-124">Bestille færre ressurser enn nødvendig.</span><span class="sxs-lookup"><span data-stu-id="37514-124">Book fewer resources than are required.</span></span> <span data-ttu-id="37514-125">I dette scenariet er de bestilte timene færre enn de obligatoriske timene.</span><span class="sxs-lookup"><span data-stu-id="37514-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="37514-126">Systemet veileder deg om hvordan du foreslår ressurser i stedet for bestillinger, slik at anmoderen kan kontrollere og holde oversikt over gjenstående behov.</span><span class="sxs-lookup"><span data-stu-id="37514-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="37514-127">Fakturerbar utnyttelse</span><span class="sxs-lookup"><span data-stu-id="37514-127">Billable utilization</span></span>

<span data-ttu-id="37514-128">Ressurser kan ha fakturerbar utnyttelse som mål.</span><span class="sxs-lookup"><span data-stu-id="37514-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="37514-129">Denne målutnyttelsen er definert som et attributt i standardrollen til en ressurs eller angitt i oppføringen for en enkelt bestillbar ressurs.</span><span class="sxs-lookup"><span data-stu-id="37514-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="37514-130">Utnyttelsesberegninger er basert på de faktiske timene ressursene har rapportert ved hjelp av godkjente tidsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="37514-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="37514-131">Følgende formler brukes til å beregne utnyttelse:</span><span class="sxs-lookup"><span data-stu-id="37514-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="37514-132">Fakturerbar utnyttelse = belastbare faktiske timer ÷ ressurskapasitet</span><span class="sxs-lookup"><span data-stu-id="37514-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="37514-133">Ikke-fakturerbar utnyttelse = faktisk tid med faktureringstype-ID = ikke-belastbar, komplementær eller ikke tilgjengelig ÷ ressurskapasitet</span><span class="sxs-lookup"><span data-stu-id="37514-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="37514-134">Intern = faktisk tid uten salgskontrakt ÷ ressurskapasitet</span><span class="sxs-lookup"><span data-stu-id="37514-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="37514-135">Ressurskapasitet = arbeidstimer for ressursen – fravær – ikke-arbeidsdager</span><span class="sxs-lookup"><span data-stu-id="37514-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="37514-136">Du kan finne visningen **Ressursutnyttelse** i **Ressurser**-ruten.</span><span class="sxs-lookup"><span data-stu-id="37514-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Visningen Ressursutnyttelse](media/Resource-Management-image65.png)

<span data-ttu-id="37514-138">Hver celle i rutenettet representerer den fakturerbare utnyttelsesprosenten for ressursen i en periode, for eksempel en dag, uke eller måned.</span><span class="sxs-lookup"><span data-stu-id="37514-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="37514-139">Følgende formler brukes til å fargelegge cellene:</span><span class="sxs-lookup"><span data-stu-id="37514-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="37514-140">**Grønn:** fakturerbar utnyttelse \>= ressursmålutnyttelse</span><span class="sxs-lookup"><span data-stu-id="37514-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="37514-141">**Gul:** målutnyttelse – 20 \<= fakturerbar utnyttelse \< målutnyttelse</span><span class="sxs-lookup"><span data-stu-id="37514-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="37514-142">**Rød:** fakturerbar utnyttelse \< målutnyttelse – 20.</span><span class="sxs-lookup"><span data-stu-id="37514-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="37514-143">Siden visningen **Ressursutnyttelse** er basert på planleggingstavlen, kan du bruke filtreringsfunksjonene på planleggingstavlen til å filtrere resultatene.</span><span class="sxs-lookup"><span data-stu-id="37514-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="37514-144">Rutenettet krever at du angir en målutnyttelse for rollen eller den individuelle ressursen.</span><span class="sxs-lookup"><span data-stu-id="37514-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="37514-145">Du kan sette opp dette ved å gå til **Ressurser** \> **Ressursroller**.</span><span class="sxs-lookup"><span data-stu-id="37514-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="37514-146">I tillegg må en standardrolle tilordnes til hver bestillbare ressurs.</span><span class="sxs-lookup"><span data-stu-id="37514-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="37514-147">Gå til **Ressurser** \> **Ressurser**.</span><span class="sxs-lookup"><span data-stu-id="37514-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="37514-148">I kategorien **Project Service** kontrollerer du at det er definert en ressursrolle, og at **Er standard**-feltet er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="37514-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="37514-149">Du kan legge til flere roller der **Er standard = Nei**.</span><span class="sxs-lookup"><span data-stu-id="37514-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="37514-150">Rollen der **Er standard = Ja** brukes til å evaluere ressursens utnyttelse mot målet for den aktuelle rollen.</span><span class="sxs-lookup"><span data-stu-id="37514-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Standardrolle angitt](media/Resource-Management-image67.png)

<span data-ttu-id="37514-152">I kategorien **Project Service** kan du også angi en individuell målutnyttelse for ressursen.</span><span class="sxs-lookup"><span data-stu-id="37514-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="37514-153">Beregningen av utnyttelsen bruker deretter denne målutnyttelsen til å evaluere ressursens mål i stedet for målet for standardrollen for ressursen.</span><span class="sxs-lookup"><span data-stu-id="37514-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="37514-154">Utnyttelse vises bare for en ressurs hvis ressursen har godkjent, belastbar tid i perioden som vises i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="37514-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="37514-155">Ressurstilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="37514-155">Resource availability</span></span>

<span data-ttu-id="37514-156">Det er svært viktig at ressurslederne kan vise tilgjengeligheten til ressurser og oppdatere bestillinger.</span><span class="sxs-lookup"><span data-stu-id="37514-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="37514-157">I noen tilfeller er det ingen formell etterspørsel (ressursforespørsel), men en ressursleder må reagere på et ikke-planlagt behov som kommer gjennom kanaler, for eksempel en e-postmelding, telefonsamtale eller direkte melding.</span><span class="sxs-lookup"><span data-stu-id="37514-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="37514-158">Ressursledere bruker planleggingstavlen til å oppdatere ressurser og bestillinger.</span><span class="sxs-lookup"><span data-stu-id="37514-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="37514-159">Arbeidstimer for ressursen brukes som grunnlag for beregning av tilgjengeligheten for en ressurs.</span><span class="sxs-lookup"><span data-stu-id="37514-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="37514-160">Ressursbestillinger opptar kapasiteten til ressursene.</span><span class="sxs-lookup"><span data-stu-id="37514-160">Resource bookings consume the capacity of the resources.</span></span>

![Planleggingstavle](media/Resource-Management-image68.png)

<span data-ttu-id="37514-162">Planleggingstavlen bruker farger og skyggelegging til å vise bestillinger, tilgjengelighet og overbestillinger, samt statusen til bestillinger.</span><span class="sxs-lookup"><span data-stu-id="37514-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="37514-163">Ved hjelp av en innstilling for planleggingstavlen kan du vise en forklaring.</span><span class="sxs-lookup"><span data-stu-id="37514-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="37514-164">Hvis en pil mot høyre vises ved siden av en individuell bestillbar ressurs på planleggingstavlen, kan ressursen utvides for å vise detaljer om arbeidet som er bestilt av ressursen.</span><span class="sxs-lookup"><span data-stu-id="37514-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Bestillbar ressurs utvidet på planleggingstavlen](media/Resource-Management-image69.png)

<span data-ttu-id="37514-166">Ettersom Dynamics 365 Project Service Automation bruker Universal Resource Scheduling-motoren, hvis du også har Dynamics 365 Field Service installert, kan du vise detaljene for ressursbestillinger for prosjekter, arbeidsordrer og alle andre enheter du har utvidet planlegging til.</span><span class="sxs-lookup"><span data-stu-id="37514-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Detaljer for ressursbestillinger for prosjekter og arbeidsordrer](media/Resource-Management-image70.png)

<span data-ttu-id="37514-168">Hvis du vil vise flere detaljer om en individuell ressurs, høyreklikker du den for å åpne ressurskortet.</span><span class="sxs-lookup"><span data-stu-id="37514-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Ressurskort](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]