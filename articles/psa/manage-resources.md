---
title: Behandle ressurser
description: Dette emnet gir informasjon om hvordan du kan administrere ressurser.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 37377367751592fc533447748b80b124cb6548ad
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151355"
---
# <a name="manage-resources"></a><span data-ttu-id="f9155-103">Behandle ressurser</span><span class="sxs-lookup"><span data-stu-id="f9155-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f9155-104">Dynamics 365 Project Service Automation inkluderer et instrumentbord for ressursledere som gir en visuell oversikt over ressursbehov og -utnyttelse gjennom hele organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="f9155-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="f9155-105">Du kan bruke diagrammene på dette instrumentbordet til å visualisere følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="f9155-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="f9155-106">**Ressursbehov** – diagrammet **Aktive ressursforespørsler** viser ressurser som er sendt.</span><span class="sxs-lookup"><span data-stu-id="f9155-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="f9155-107">Ressursene samles av rolle eller prosjekt.</span><span class="sxs-lookup"><span data-stu-id="f9155-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="f9155-108">**Ressursbehov som ikke er sendt** – diagrammet **Ikke-tilordnet ressursbehov** viser alle ressursbehovene som ikke er sendt.</span><span class="sxs-lookup"><span data-stu-id="f9155-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="f9155-109">Det hjelper ressurs ansvarlige med å vise behov som ikke er fast, og kan sendes via en ressursforespørsel.</span><span class="sxs-lookup"><span data-stu-id="f9155-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="f9155-110">**Fakturerbar utnyttelse for forrige uke** – diagrammet **Utnyttelse etter rolle** viser prosentandelen av organisasjonens faktiske fakturerbare utnyttelse etter rolle mot fakturerbar utnyttelse av rolle for rolle.</span><span class="sxs-lookup"><span data-stu-id="f9155-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9155-111">For å gjøre diagrammet **Utnyttelse etter rolle** tilgjengelig må du opprette en jobb som kjører UpdateRoleUtilization-arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="f9155-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="f9155-112">Denne regelmessige jobben kjører hver sjuende dag for å beregne fakturerbar utnyttelse for de siste sju dagene.</span><span class="sxs-lookup"><span data-stu-id="f9155-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="f9155-113">Resultatene samles etter rolle.</span><span class="sxs-lookup"><span data-stu-id="f9155-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="f9155-114">Administrere prosjektteammedlemmer</span><span class="sxs-lookup"><span data-stu-id="f9155-114">Manage project team members</span></span>

<span data-ttu-id="f9155-115">Prosjektledere kan bruke instrumentbordet for ressursledere til å administrere ressursene på prosjekter.</span><span class="sxs-lookup"><span data-stu-id="f9155-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="f9155-116">De kan for eksempel legge til et teammedlem direkte i et prosjekt og bestille et teammedlem for å oppfylle ressurskravene som ble registrert av en generell ressurs.</span><span class="sxs-lookup"><span data-stu-id="f9155-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="f9155-117">Legge til et teammedlem direkte i et prosjekt</span><span class="sxs-lookup"><span data-stu-id="f9155-117">Add a team member directly to a project</span></span>

<span data-ttu-id="f9155-118">Hvis du vil legge til et teammedlem direkte i et prosjekt, går du til **Prosjekter**-siden og **Team**-kategorien og velger **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f9155-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="f9155-119">Dialogboksen **Hurtigoppretting: Prosjektteammedlem** vises.</span><span class="sxs-lookup"><span data-stu-id="f9155-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="f9155-120">I denne dialogboksen kan du utføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="f9155-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="f9155-121">**Bestille en navngitt ressurs** – velg navnet på ressursen i feltet **Bestillbar ressurs**.</span><span class="sxs-lookup"><span data-stu-id="f9155-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="f9155-122">Velg deretter rollen, angi perioden, og velg en tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="f9155-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="f9155-123">Den navngitte ressursen du har valgt, blir lagt til i prosjektet ved hjelp av den valgte tildelingsmetoden og ressurskalenderen.</span><span class="sxs-lookup"><span data-stu-id="f9155-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="f9155-124">**Legge til en generell ressurs** – la feltet **Bestillbar ressurs** være tomt, og velg deretter rollen, angi perioden, og velg den foretrukne tildelingsmetoden.</span><span class="sxs-lookup"><span data-stu-id="f9155-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="f9155-125">En generell ressurs blir lagt til i teamet som en plassholder for å holde behovsmønsteret som brukes til å bestille navngitte ressurser i teamet.</span><span class="sxs-lookup"><span data-stu-id="f9155-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="f9155-126">Kravet utføres i henhold til prosjektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="f9155-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="f9155-127">**Legge til en navngitt ressurs i teamet uten å ta i bruk ressurskapasitet** – i feltet **Bestillbar ressurs** velger du en ressurs.</span><span class="sxs-lookup"><span data-stu-id="f9155-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="f9155-128">Velg deretter perioden, og velg **Ingen** som tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="f9155-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="f9155-129">Ressursen legges til i teamet, men ressursens kapasitet forbrukes ikke via en bestilling.</span><span class="sxs-lookup"><span data-stu-id="f9155-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="f9155-130">Bestille et teammedlem for å oppfylle ressurskrav for en generell ressurs</span><span class="sxs-lookup"><span data-stu-id="f9155-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="f9155-131">I PSA kan du reservere en generell ressurs i et prosjektteam, og du kan angi rollen, den nødvendige kapasiteten og hvordan denne kapasiteten skal distribueres.</span><span class="sxs-lookup"><span data-stu-id="f9155-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="f9155-132">I ressurskravet kan du angi attributter som er tilknyttet den generelle ressursen.</span><span class="sxs-lookup"><span data-stu-id="f9155-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="f9155-133">Disse attributtene inkluderer nødvendige ferdigheter, den foretrukne organisasjonsenheten og foretrukne ressurser.</span><span class="sxs-lookup"><span data-stu-id="f9155-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="f9155-134">Følg fremgangsmåten nedenfor for å angi nødvendige ferdigheter på en generell ressurs for en utvikler.</span><span class="sxs-lookup"><span data-stu-id="f9155-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="f9155-135">På siden **Prosjekter** i kategorien **Team** velger du **Ny** for å reservere en generell ressurs.</span><span class="sxs-lookup"><span data-stu-id="f9155-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Generell ressurs bestilt i teamet](media/Resource-Management-image9.png)

2. <span data-ttu-id="f9155-137">I visningen **Alle teammedlemmer**, i kolonnen **Ressurskrav** velger du koblingen for å legge til nødvendige ferdigheter for den generelle ressursen.</span><span class="sxs-lookup"><span data-stu-id="f9155-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Kobling til krav](media/Resource-Management-image10.png)

3. <span data-ttu-id="f9155-139">På siden **Ressurskrav** som vises i **Ferdigheter**-rutenettet, velger du ellipsen (**...**) og velger deretter **Legg til nytt kravkjennetegn** for å legge til de nødvendige ferdighetene for utvikleren.</span><span class="sxs-lookup"><span data-stu-id="f9155-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Kommandoen Legg til nytt kravkjennetegn](media/Resource-Management-image11.png)

4. <span data-ttu-id="f9155-141">I dialogboksen **Hurtigoppretting: Kravkjennetegn** som vises, velger du den ønskede ferdigheten i **Kjennetegn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9155-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="f9155-142">I feltet **Rangeringsverdi** velger du deretter kompetansenivået for ferdigheten.</span><span class="sxs-lookup"><span data-stu-id="f9155-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="f9155-143">Til slutt, i feltet **Ressurskrav**, angir du kravet for kilderessurser fra organisasjonsenheter eller navngitte ressurser.</span><span class="sxs-lookup"><span data-stu-id="f9155-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="f9155-144">Velg **Lagre** når du er ferdig.</span><span class="sxs-lookup"><span data-stu-id="f9155-144">When you've finished, select **Save**.</span></span>

    ![Dialogboksen Hurtigoppretting: Kravkjennetegn](media/Resource-Management-image12.png)

5. <span data-ttu-id="f9155-146">På siden **Ressurskrav** velger du **Bestill** for å oppfylle ressurskravet.</span><span class="sxs-lookup"><span data-stu-id="f9155-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Bestill-knappen på siden Ressurskrav](media/Resource-Management-image13.png)

    <span data-ttu-id="f9155-148">Du kan også velge den generelle ressursen i rutenettet **Alle teammedlemmer** og deretter velge **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="f9155-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Bestill-knappen over rutenettet Alle teammedlemmer](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="f9155-150">I dette eksemplet er det 40 obligatoriske timer, men ingen faktisk bestilte timer, fordi generelle ressurser ikke har bestillinger.</span><span class="sxs-lookup"><span data-stu-id="f9155-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="f9155-151">I tillegg er det ingen tildelte timer fordi den generelle ressursen ble lagt til direkte i teamet.</span><span class="sxs-lookup"><span data-stu-id="f9155-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="f9155-152">Den ble ikke lagt til ved hjelp av oppgavetilordning.</span><span class="sxs-lookup"><span data-stu-id="f9155-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="f9155-153">På siden **Planleggingsassistent** kan du filtrere tilgjengelige ressurser etter kravene som er angitt i ressurskravet.</span><span class="sxs-lookup"><span data-stu-id="f9155-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="f9155-154">Ressurser sorteres i henhold til sorteringsparameterne som er angitt på planleggingstavlen.</span><span class="sxs-lookup"><span data-stu-id="f9155-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Siden Planleggingsassistent](media/Resource-Management-image15.png)

    <span data-ttu-id="f9155-156">Her er noen filtre som brukes ofte:</span><span class="sxs-lookup"><span data-stu-id="f9155-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="f9155-157">**Kjennetegn sammen med en rangering** – Filtrer etter ferdigheter, sertifiseringer og andre ressurskvaliteter, i tillegg til vurdering av kompetanse.</span><span class="sxs-lookup"><span data-stu-id="f9155-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="f9155-158">**Roller** – Filtrer etter standardrollene som er tilordnet bestillbare ressurser.</span><span class="sxs-lookup"><span data-stu-id="f9155-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="f9155-159">**Organisasjonsenheter** – Filtrer bestillbare ressurser etter organisasjonsenhetene de er tilordnet til.</span><span class="sxs-lookup"><span data-stu-id="f9155-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="f9155-160">Hvis du ikke er fornøyd med resultatene av det første kravsøket, kan du endre filtervilkårene.</span><span class="sxs-lookup"><span data-stu-id="f9155-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="f9155-161">Utvid ruten **Filtervisning** til venstre, og velg deretter **Søk** for å finne flere ressurser.</span><span class="sxs-lookup"><span data-stu-id="f9155-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Ruten Filtervisning](media/Resource-Management-image16.png)

7. <span data-ttu-id="f9155-163">Hvis du vil endre måten resultatene sorteres på, velger du **Sorter**.</span><span class="sxs-lookup"><span data-stu-id="f9155-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Sorter-kommandoen](media/Resource-Management-image17.png)

8. <span data-ttu-id="f9155-165">Velg ressurser i henhold til behovet som er angitt i kravet, som angitt øverst i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="f9155-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="f9155-166">Du kan fjerne merkingen av celler i rutenettet og la den ressurskapasiteten være åpen.</span><span class="sxs-lookup"><span data-stu-id="f9155-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="f9155-167">Bare én ressurs om gangen kan velges som bestilt.</span><span class="sxs-lookup"><span data-stu-id="f9155-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="f9155-168">Velg **Bestill** for å reservere den valgte ressursen og la planleggingstavlen være åpen, slik at du kan velge flere ressurser.</span><span class="sxs-lookup"><span data-stu-id="f9155-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="f9155-169">Du kan også velge **Bestill og avslutt** for å reservere den valgte ressursen og lukke planleggingstavlen.</span><span class="sxs-lookup"><span data-stu-id="f9155-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Ressurs som skal bestilles](media/Resource-Management-image19.png)

    <span data-ttu-id="f9155-171">Du mottar et varsel om bestilte timer.</span><span class="sxs-lookup"><span data-stu-id="f9155-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="f9155-172">Behovsindikatorene viser hvor mye bestillingskravet er oppfylt, og hvor mye som gjenstår.</span><span class="sxs-lookup"><span data-stu-id="f9155-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="f9155-173">Du kan også se hvor mye av kapasiteten til den valgte ressursen som forbrukes.</span><span class="sxs-lookup"><span data-stu-id="f9155-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="f9155-174">Velg **Utvid** for å vise flere detaljer om ressursbestillinger.</span><span class="sxs-lookup"><span data-stu-id="f9155-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="f9155-175">Gå tilbake til visningen **Alle teammedlemmer**.</span><span class="sxs-lookup"><span data-stu-id="f9155-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="f9155-176">Legg merke til at den generelle ressursen er erstattet med den navngitte ressursen i rutenettet, og 40 timer vises som bestilt for den ressursen.</span><span class="sxs-lookup"><span data-stu-id="f9155-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Oppdatert Alle teammedlemmer-rutenett](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="f9155-178">Ingen tildelte timer vises fordi de ble bestilt direkte i teamet.</span><span class="sxs-lookup"><span data-stu-id="f9155-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="f9155-179">De ble ikke bestilt ved hjelp av oppgavetilordning.</span><span class="sxs-lookup"><span data-stu-id="f9155-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="f9155-180">Tilordne generelle ressurser til oppgaver og generere ressurskrav</span><span class="sxs-lookup"><span data-stu-id="f9155-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="f9155-181">I PSA kan du opprette oppgaver og deretter tilordne generelle ressurser til dem.</span><span class="sxs-lookup"><span data-stu-id="f9155-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="f9155-182">På denne måten kan ressursbehovet representeres av plassholdere når du beregner tidsplanen og de finansielle tallene.</span><span class="sxs-lookup"><span data-stu-id="f9155-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="f9155-183">Deretter kan du generere ressurskrav for de generelle ressursene og fullføre dem.</span><span class="sxs-lookup"><span data-stu-id="f9155-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="f9155-184">På siden **Prosjekter** i kategorien **Tidsplan** velger du **Legg til** for å opprette en oppgave.</span><span class="sxs-lookup"><span data-stu-id="f9155-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Ny oppgave opprettet](media/Resource-Management-image21.png)

2. <span data-ttu-id="f9155-186">I **Ressurser**-feltet velger du **Ressursvelger**-symbolet.</span><span class="sxs-lookup"><span data-stu-id="f9155-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="f9155-187">Ressursvelgeren vises med eksisterende teammedlemmer for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="f9155-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Ressursvelger](media/Resource-Management-image22.png)

3. <span data-ttu-id="f9155-189">Skriv inn navnet på den nye generelle ressursen, og velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="f9155-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Navn på en ny generisk ressurs angitt](media/Resource-Management-image23.png)

4. <span data-ttu-id="f9155-191">I dialogboksen **Hurtigoppretting: Prosjektteammedlem** som vises, velger du rollen for den generelle ressursen i **Rolle**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9155-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="f9155-192">I feltet **Ressursenhet** velger du organisasjonsenheten for den generelle ressursen.</span><span class="sxs-lookup"><span data-stu-id="f9155-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="f9155-193">Velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f9155-193">Then select **Save**.</span></span>

    ![Dialogboksen Hurtigoppretting: Prosjektteammedlem](media/Resource-Management-image24.png)

    <span data-ttu-id="f9155-195">Det generelle teammedlemmet tilordnes nå til oppgaven.</span><span class="sxs-lookup"><span data-stu-id="f9155-195">The generic team member is now assigned to the task.</span></span>

    ![Generelt teammedlem tilordnet til oppgaven](media/Resource-Management-image25.png)

    <span data-ttu-id="f9155-197">I kategorien **Team** vil du se det nye generelle teammedlemmet.</span><span class="sxs-lookup"><span data-stu-id="f9155-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="f9155-198">Legg merke til at det bare har tildelte timer.</span><span class="sxs-lookup"><span data-stu-id="f9155-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="f9155-199">Disse timene er summen av alle oppgaver som er tilordnet det generelle teammedlemmet.</span><span class="sxs-lookup"><span data-stu-id="f9155-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="f9155-200">Det generelle teammedlemmet har ennå ikke nødvendige timer eller et ressurskrav.</span><span class="sxs-lookup"><span data-stu-id="f9155-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Generelt teammedlem i kategorien Team](media/Resource-Management-image26.png)

5. <span data-ttu-id="f9155-202">Du kan nå tilordne det generelle teammedlemmet til andre oppgaver ved hjelp av ressursvelgeren.</span><span class="sxs-lookup"><span data-stu-id="f9155-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Generelt teammedlem i ressursvelgeren](media/Resource-Management-image27.png)

    <span data-ttu-id="f9155-204">Når du er ferdig med å tilordne den generelle ressursen til oppgaver, kan du generere et ressurs krav for den generelle ressursen.</span><span class="sxs-lookup"><span data-stu-id="f9155-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="f9155-205">I kategorien **Team** velger du den generelle ressursen, og deretter velger du **Generer krav**.</span><span class="sxs-lookup"><span data-stu-id="f9155-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Kommandoen Generer krav](media/Resource-Management-image28.png)

    <span data-ttu-id="f9155-207">Når kravet er generert, vil det generelle team medlemmet ha nødvendige timer og en kobling for ressurskravet.</span><span class="sxs-lookup"><span data-stu-id="f9155-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Kobling til ressurskrav](media/Resource-Management-image29.png)

    <span data-ttu-id="f9155-209">Når du har bestilt en navngitt ressurs, fjernes den generelle ressursen fra teamet og erstattes av den navngitte ressursen.</span><span class="sxs-lookup"><span data-stu-id="f9155-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Generell ressurs erstattet av den navngitte ressursen](media/Resource-Management-image30.png)

    <span data-ttu-id="f9155-211">I kategorien **Tidsplan** blir de generelle ressurstilordningene fjernet og erstattet av den navngitte ressursen.</span><span class="sxs-lookup"><span data-stu-id="f9155-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Generell ressurstilordningen erstattet av den navngitte ressursen i kategorien Tidsplan](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="f9155-213">Denne virkemåten inntreffer bare når en navngitt ressurs er fullstendig bestilt for det generelle ressurskravet.</span><span class="sxs-lookup"><span data-stu-id="f9155-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="f9155-214">Når en navngitt ressurs delvis erstatter det generelle ressurskravet eller flere navngitte ressurser erstatter det generelle ressurskravet, forblir den generelle ressursen tilordnet til oppgaven.</span><span class="sxs-lookup"><span data-stu-id="f9155-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="f9155-215">I illustrasjonen nedenfor er en oppgave på 80 timer planlagt med en varighet på fem dager (16 timer per dag over fem dager) og tilordnet til den generelle ressursen som har navnet **Funksjonell**.</span><span class="sxs-lookup"><span data-stu-id="f9155-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Oppgave på 80 timer og fem dager tilordnet den generelle Funksjonell-ressursen](media/Resource-Management-image32.png)

    <span data-ttu-id="f9155-217">Når du genererer kravet, er det for 80 timer i løpet av fem dager.</span><span class="sxs-lookup"><span data-stu-id="f9155-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Krav generert for 80 timer over fem dager](media/Resource-Management-image33.png)

    <span data-ttu-id="f9155-219">Siden tilgjengelige ressurser bare arbeider åtte timer per dag, kreves det to ressurser for å fullføre behovet.</span><span class="sxs-lookup"><span data-stu-id="f9155-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Andre ressurs](media/Resource-Management-image35.png)

    <span data-ttu-id="f9155-221">I kategorien **Team** kan du nå se at den generelle ressursen ikke har noen nødvendige timer, men de tildelte timene vises fremdeles sammen med de to navngitte ressursene som utgjør fullføringen.</span><span class="sxs-lookup"><span data-stu-id="f9155-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![To navngitte ressurser i kategorien Team](media/Resource-Management-image36.png)

    <span data-ttu-id="f9155-223">I kategorien **Tidsplan** forblir den generelle ressursen tilordnet til oppgaven.</span><span class="sxs-lookup"><span data-stu-id="f9155-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Generelle ressurser i kategorien Tidsplan](media/Resource-Management-image37.png)

<span data-ttu-id="f9155-225">PSA tilordner ikke begge ressursene til oppgaven fordi denne funksjonaliteten vil gi en mindre forutsigbar tidsplan.</span><span class="sxs-lookup"><span data-stu-id="f9155-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="f9155-226">I dette enkle eksemplet er det enkelt å dele opp timene likt mellom to ressurser.</span><span class="sxs-lookup"><span data-stu-id="f9155-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="f9155-227">I mer komplekse scenarier som involverer flere oppgaver og flere ressurser, må imidlertid PSA opprette antagelser om hvordan det skal fordele bestillinger som er mottatt for flere ressurser på tvers av flere oppgaver.</span><span class="sxs-lookup"><span data-stu-id="f9155-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="f9155-228">I disse scenariene er prosjektlederen derfor ansvarlig for å analysere flere bestillinger og tilordne dem etter behov.</span><span class="sxs-lookup"><span data-stu-id="f9155-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="f9155-229">For å kunne tildele bestillinger tilordner prosjektlederen oppgavene fra de generelle ressursene til de navngitte ressursene, og deretter brukes **Avstemming**-visningen til å sikre at tildelingen fungerer med bestillinger.</span><span class="sxs-lookup"><span data-stu-id="f9155-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="f9155-230">Redigere et ressurskrav</span><span class="sxs-lookup"><span data-stu-id="f9155-230">Edit a resource requirement</span></span>

<span data-ttu-id="f9155-231">Når et ressurskrav er opprettet, kan det hende at en prosjektleder eller ressursleder vil redigere detaljene for å finjustere søkevilkårene når planleggingstavlen brukes.</span><span class="sxs-lookup"><span data-stu-id="f9155-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="f9155-232">Følg fremgangsmåten nedenfor for å redigere ressurskravet.</span><span class="sxs-lookup"><span data-stu-id="f9155-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="f9155-233">På siden **Prosjekter** i kategorien **Team** velger du koblingen til et krav for en generell ressurs.</span><span class="sxs-lookup"><span data-stu-id="f9155-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="f9155-234">På siden **Ressurskrav** som vises, kan du oppdatere flere attributter.</span><span class="sxs-lookup"><span data-stu-id="f9155-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="f9155-235">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="f9155-235">Here are some examples:</span></span>

    - <span data-ttu-id="f9155-236">Navn</span><span class="sxs-lookup"><span data-stu-id="f9155-236">Name</span></span>
    - <span data-ttu-id="f9155-237">Fra dato</span><span class="sxs-lookup"><span data-stu-id="f9155-237">From Date</span></span>
    - <span data-ttu-id="f9155-238">Til dato</span><span class="sxs-lookup"><span data-stu-id="f9155-238">To Date</span></span>
    - <span data-ttu-id="f9155-239">Varighet</span><span class="sxs-lookup"><span data-stu-id="f9155-239">Duration</span></span>
    - <span data-ttu-id="f9155-240">Ressurstype</span><span class="sxs-lookup"><span data-stu-id="f9155-240">Resource Type</span></span>

<span data-ttu-id="f9155-241">På siden **Ressurskrav** kan prosjektlederen eller ressurslederen også definere følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="f9155-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="f9155-242">Ferdigheter</span><span class="sxs-lookup"><span data-stu-id="f9155-242">Skills</span></span>
- <span data-ttu-id="f9155-243">Roller</span><span class="sxs-lookup"><span data-stu-id="f9155-243">Roles</span></span>
- <span data-ttu-id="f9155-244">Ressurspreferanser</span><span class="sxs-lookup"><span data-stu-id="f9155-244">Resource preferences</span></span>
- <span data-ttu-id="f9155-245">Foretrukket organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="f9155-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="f9155-246">Oppdatere ressursbestillinger etter at de er bestilt på et prosjekt</span><span class="sxs-lookup"><span data-stu-id="f9155-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="f9155-247">Når du har lagt til en generell eller navngitt ressurs i et prosjektteam, kan du endre ressursens bestillinger.</span><span class="sxs-lookup"><span data-stu-id="f9155-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="f9155-248">På **Prosjekter**-siden i kategorien **Team** velger du et teammedlem og velger deretter **Vedlikehold bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="f9155-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Planleggingstavlen åpnet for det valgte teammedlemmet](media/Resource-Management-image40.png)

    <span data-ttu-id="f9155-250">Planleggingstavlen vises med bestillingene til prosjektteammedlemmet.</span><span class="sxs-lookup"><span data-stu-id="f9155-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="f9155-251">Utvid teammedlemmets oppføring for å vise timene som er bestilt mot dette prosjektet, og andre prosjekter som bruker kapasiteten til teammedlemmet.</span><span class="sxs-lookup"><span data-stu-id="f9155-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="f9155-252">Merk og dra bestillingen for å utvide den eller redusere den.</span><span class="sxs-lookup"><span data-stu-id="f9155-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="f9155-253">Dialogboksen **Opprett ressursbestilling** vises, der du kan justere bestillingen.</span><span class="sxs-lookup"><span data-stu-id="f9155-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Dialogboksen Opprett ressursbestilling](media/Resource-Management-image41.png)

3. <span data-ttu-id="f9155-255">Høyreklikk bestillingen.</span><span class="sxs-lookup"><span data-stu-id="f9155-255">Right-click the booking.</span></span> <span data-ttu-id="f9155-256">Du kan deretter bruke hurtigmenyen til å utføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="f9155-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="f9155-257">Endre bestillingsstatusen.</span><span class="sxs-lookup"><span data-stu-id="f9155-257">Change the booking status.</span></span>
    - <span data-ttu-id="f9155-258">Redigere bestillingen.</span><span class="sxs-lookup"><span data-stu-id="f9155-258">Edit the booking.</span></span>
    - <span data-ttu-id="f9155-259">Erstatte en ressurs i prosjektteamet.</span><span class="sxs-lookup"><span data-stu-id="f9155-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="f9155-260">Endre bestillingsstatusen</span><span class="sxs-lookup"><span data-stu-id="f9155-260">Change the booking status</span></span>

<span data-ttu-id="f9155-261">Du kan endre enhver standard eller egendefinert bestillingsstatus.</span><span class="sxs-lookup"><span data-stu-id="f9155-261">You can change any default or custom booking status.</span></span>

![Kommandoen Endre status](media/Resource-Management-image42.png)

<span data-ttu-id="f9155-263">Følgende statuser er inkludert i PSA:</span><span class="sxs-lookup"><span data-stu-id="f9155-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="f9155-264">**Annullert** – denne statusen annullerer en bestillingen av en ressurs og frigjør kapasiteten for ressursen.</span><span class="sxs-lookup"><span data-stu-id="f9155-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="f9155-265">**Forpliktende bestilling** – denne statusen bruker kapasiteten til en ressurs.</span><span class="sxs-lookup"><span data-stu-id="f9155-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="f9155-266">En bestilling har vanligvis denne statusen når du åpner **Vedlikehold bestillinger** fra rutenettet **Alle teammedlemmer** på **Prosjekter**-siden.</span><span class="sxs-lookup"><span data-stu-id="f9155-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="f9155-267">**Ikke-forpliktende bestilling** – denne statusen legger til en ressurs i et team, men forbruker ikke kapasiteten til ressursen.</span><span class="sxs-lookup"><span data-stu-id="f9155-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="f9155-268">Den angir at ressursen er reservert for potensielt arbeid, men fremdeles har kapasitet hvis det er nødvendig for andre jobber.</span><span class="sxs-lookup"><span data-stu-id="f9155-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="f9155-269">Når det gjelder generell ressurstilgjengelighet, har ikke-forpliktende bestillinger en annen status enn forpliktende bestillinger.</span><span class="sxs-lookup"><span data-stu-id="f9155-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="f9155-270">**Foreslått** – denne statusen representerer et forslag for en ressurs fra en ressursleder eller prosjektleder.</span><span class="sxs-lookup"><span data-stu-id="f9155-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="f9155-271">Forslag forbruker ikke kapasiteten til en ressurs, og ressursen blir ikke lagt til i prosjektteamet.</span><span class="sxs-lookup"><span data-stu-id="f9155-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="f9155-272">Hvis du vil ha en forpliktende bestilling av ressursen i teamet, må prosjektlederen godta forslaget.</span><span class="sxs-lookup"><span data-stu-id="f9155-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="f9155-273">Send ressursforespørsler</span><span class="sxs-lookup"><span data-stu-id="f9155-273">Submit resource requests</span></span>

<span data-ttu-id="f9155-274">Ressursforespørsler brukes til å utføre behovet (ressurskravet) som må oppfylles av en ressursleder.</span><span class="sxs-lookup"><span data-stu-id="f9155-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="f9155-275">For en generell ressurs som allerede er i teamet, kan du sende en ressursforespørsel direkte.</span><span class="sxs-lookup"><span data-stu-id="f9155-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="f9155-276">En ressursforespørsel kan gjennomføres på to måter:</span><span class="sxs-lookup"><span data-stu-id="f9155-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="f9155-277">Ressurslederen oppfyller forespørselen direkte.</span><span class="sxs-lookup"><span data-stu-id="f9155-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="f9155-278">I dette tilfellet blir den generelle ressursen erstattet av en forpliktende bestilling som har en navngitt ressurs.</span><span class="sxs-lookup"><span data-stu-id="f9155-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="f9155-279">Ressurslederen foreslår en ressurs til prosjektlederen, og prosjektlederen godkjenner eller forkaster den foreslåtte ressursen.</span><span class="sxs-lookup"><span data-stu-id="f9155-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="f9155-280">Direkte oppfylling av ressursforespørsler</span><span class="sxs-lookup"><span data-stu-id="f9155-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="f9155-281">Når et ressurskrav er generert, kan en prosjektleder sende en ressursforespørsel om en generell ressurs ved å velge ressursen og deretter velge **Send forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="f9155-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Knappen Send forespørsel](media/Resource-Management-image45.png)

<span data-ttu-id="f9155-283">Kommentarer om ressursen kan sendes til ressurslederen ren som oppfyller forespørselen.</span><span class="sxs-lookup"><span data-stu-id="f9155-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="f9155-284">Når forespørselen er sendt, blir **Status**-feltet for teammedlemmet endret til **Sendt**.</span><span class="sxs-lookup"><span data-stu-id="f9155-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Angi valgfrie kommentarer](media/Resource-Management-image46.png)

<span data-ttu-id="f9155-286">Når ressurslederen oppfyller forespørselen, blir det generelle teammedlemmet erstattet av den navngitte ressursen i rutenettet **Alle teammedlemmer**.</span><span class="sxs-lookup"><span data-stu-id="f9155-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Generelt teammedlem erstattet av den navngitte ressursen i rutenettet Alle teammedlemmer](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="f9155-288">Bruke et ressursforslag for ressursforespørsler</span><span class="sxs-lookup"><span data-stu-id="f9155-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="f9155-289">I stedet for å reservere en ressurs direkte på en ressursforespørsel kan en ressursleder foreslå en ressurs til prosjektlederen.</span><span class="sxs-lookup"><span data-stu-id="f9155-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="f9155-290">En ressursleder kan bruke dette alternativet når et identisk treff for kravene ikke er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="f9155-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="f9155-291">Når en ressursleder foreslår en ressurs, ser prosjektlederen at **Status**-feltet for det generelle teammedlemmet blir endret til **Må gjennomgås**.</span><span class="sxs-lookup"><span data-stu-id="f9155-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Statusen for generelt teammedlems endret til Må gjennomgås](media/Resource-Management-image48.png)

<span data-ttu-id="f9155-293">Hvis du vil vise den foreslåtte ressursen sammen med en visualisering av innvirkningen til bestillingen av forslaget, dobbeltklikker du teammedlemmet som har statusen **Må gjennomgås**.</span><span class="sxs-lookup"><span data-stu-id="f9155-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="f9155-294">Velg deretter kategorien **Foreslåtte ressurser**.</span><span class="sxs-lookup"><span data-stu-id="f9155-294">Then select the **Proposed Resources** tab.</span></span>

![Kategorien Foreslåtte ressurser](media/Resource-Management-image49.png)

<span data-ttu-id="f9155-296">Velg **Godta alle forslag** for å godta alle foreslåtte ressurser eller **Avvis alle forslag** for å avvise dem.</span><span class="sxs-lookup"><span data-stu-id="f9155-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="f9155-297">Hvis du godtar de foreslåtte ressursene, blir de forpliktende på prosjektet som teammedlemmer og erstatter de generelle ressursene.</span><span class="sxs-lookup"><span data-stu-id="f9155-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="f9155-298">Du må enten godta eller forkaste alle foreslåtte ressurser.</span><span class="sxs-lookup"><span data-stu-id="f9155-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="f9155-299">Du kan ikke delvis godta eller forkaste dem.</span><span class="sxs-lookup"><span data-stu-id="f9155-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="f9155-300">Erstatte en ressurs i prosjektteamet</span><span class="sxs-lookup"><span data-stu-id="f9155-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="f9155-301">Noen ganger må en prosjektleder erstatte et teammedlem i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="f9155-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="f9155-302">På **Prosjekter**-siden i kategorien **Team** velger du ressursen som trenger erstatning, og velger deretter **Vedlikehold bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="f9155-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="f9155-303">Utvid ressursen for å vise prosjektene den er tilordnet til.</span><span class="sxs-lookup"><span data-stu-id="f9155-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Ressurs utvidet for å vise tilordnede prosjekter](media/Resource-Management-image50.png)

3. <span data-ttu-id="f9155-305">Høyreklikk prosjektet, og velg deretter **Erstatt ressurs**.</span><span class="sxs-lookup"><span data-stu-id="f9155-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="f9155-306">Hvis du vet ressursen du vil erstatte den gjeldende ressursen med, velger du eller skriver inn navnet, og deretter velger du **Tilordne på nytt**.</span><span class="sxs-lookup"><span data-stu-id="f9155-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Angi en erstatningsressurs](media/Resource-Management-image51.png)

    <span data-ttu-id="f9155-308">Du kan også følge disse trinnene hvis du vil søke etter en ressurs:</span><span class="sxs-lookup"><span data-stu-id="f9155-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="f9155-309">Velg **Finn erstatning**.</span><span class="sxs-lookup"><span data-stu-id="f9155-309">Select **Find Substitution**.</span></span>

        ![Søke etter en erstatningsressurs](media/Resource-Management-image52.png)

        <span data-ttu-id="f9155-311">Planleggingsassistente returnerer en liste over tilgjengelige erstatninger.</span><span class="sxs-lookup"><span data-stu-id="f9155-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="f9155-312">I planleggingsassistenten kan du ytterligere filtrere de tilgjengelige ressursene for å finne en passende erstatning.</span><span class="sxs-lookup"><span data-stu-id="f9155-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Liste over tilgjengelige erstatninger](media/Resource-Management-image53.png)

    2. <span data-ttu-id="f9155-314">Hvis du vil erstatte ressursen, velger du ønsket ressurs, og deretter velger du **Erstatt**.</span><span class="sxs-lookup"><span data-stu-id="f9155-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Erstatningsressurs valgt](media/Resource-Management-image54.png)

    <span data-ttu-id="f9155-316">Bestillingene og tildelingene erstattes med den nye ressursen.</span><span class="sxs-lookup"><span data-stu-id="f9155-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Bestillinger og tildelinger erstattet med den nye ressursen](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="f9155-318">Avstemme tilordninger og bestillinger for teammedlemmer</span><span class="sxs-lookup"><span data-stu-id="f9155-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="f9155-319">For teammedlemmer er bestillinger og tildelinger løst sammenkoblet.</span><span class="sxs-lookup"><span data-stu-id="f9155-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="f9155-320">Ressurser kan med andre ord ha tilordninger, men ikke bestillinger, eller de kan ha bestillinger, men ikke tilordninger.</span><span class="sxs-lookup"><span data-stu-id="f9155-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="f9155-321">Ideelt sett bør bestillinger og tilordninger rettes inn mot hverandre, slik at ressurser har forpliktet kapasitet til å utføre oppgavetilordningene.</span><span class="sxs-lookup"><span data-stu-id="f9155-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="f9155-322">Det kan imidlertid hende at bestillinger blir basert på tilgjengelighet, og det kan hende at oppgavetidspunkter endres etter hvert som prosjektet fortsetter.</span><span class="sxs-lookup"><span data-stu-id="f9155-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="f9155-323">Derfor gir den løse koblingen av bestillinger og tildelinger fleksibilitet.</span><span class="sxs-lookup"><span data-stu-id="f9155-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="f9155-324">PSA har en **Avstemming**-kategori som gjør at prosjektledere kan avstemme teammedlemmenes bestillinger og deres tildelinger for prosjektteam.</span><span class="sxs-lookup"><span data-stu-id="f9155-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Kategorien Avstemming](media/Resource-Management-image56.png)

<span data-ttu-id="f9155-326">Kategorien **Avstemming** viser bestillinger og tilordninger nedover til nivået for den individuelle oppgavetilordningen for hvert teammedlem.</span><span class="sxs-lookup"><span data-stu-id="f9155-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="f9155-327">Den viser timer i celler som representerer tidsperioder, fra måneder til dager.</span><span class="sxs-lookup"><span data-stu-id="f9155-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="f9155-328">Kategorien viser også en total nettosum for prosjektet, sammen med en totalsumkolonne.</span><span class="sxs-lookup"><span data-stu-id="f9155-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="f9155-329">For hver ressurs beregner kategorien forskjellen mellom teammedlemmenes bestillinger og en beregnet verdi teammedlemmets oppgavetilordninger.</span><span class="sxs-lookup"><span data-stu-id="f9155-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="f9155-330">Ideelt sett bør denne forskjellen være 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f9155-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="f9155-331">Det bør med andre ord ikke være forskjell mellom bestillinger og tildelinger.</span><span class="sxs-lookup"><span data-stu-id="f9155-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="f9155-332">Forskjellene er fargelagt og skyggelagt for å rette oppmerksomheten mot to betingelser:</span><span class="sxs-lookup"><span data-stu-id="f9155-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="f9155-333">**Få bestillinger** – for få bestillinger inntreffer når en ressurs har flere tildelinger enn bestillinger.</span><span class="sxs-lookup"><span data-stu-id="f9155-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="f9155-334">Ettersom denne kapasiteten ikke er reservert, kan det hende at en prosjektleder vil korrigere denne betingelsen ved å utvide ressursens bestillinger for å dekke underskuddet.</span><span class="sxs-lookup"><span data-stu-id="f9155-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="f9155-335">**Overflødige bestillinger** – Overflødige bestillinger skjer når en ressurs er bestilt til prosjektet, men ikke er tilordnet til aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="f9155-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="f9155-336">Denne tilstanden kan være akseptabel i saker der ressursen ble bestilt til prosjektet før oppgavetilordningen ble utført.</span><span class="sxs-lookup"><span data-stu-id="f9155-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="f9155-337">I andre tilfeller er det imidlertid ikke planlagt at ressursen skal tilordnes til oppgaver.</span><span class="sxs-lookup"><span data-stu-id="f9155-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="f9155-338">I slike tilfeller bør prosjektlederen vurdere å annullere ressursens bestillinger, slik at kapasiteten kan brukes for et annet prosjekt.</span><span class="sxs-lookup"><span data-stu-id="f9155-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="f9155-339">Når du i noen tilfeller viser tid på høyere nivå enn dagnivået (for eksempel månedsnivået), kan det hende du ser en netto differanse på null for en ressurs (med andre ord bestillinger = tildelinger).</span><span class="sxs-lookup"><span data-stu-id="f9155-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="f9155-340">Hvis du imidlertid viser tid på ukenivå, ser du at det er tildelinger på null timer og bestillinger på 40 timer i den første uken, men tildelinger på 40 timer og bestillinger på null timer i den andre uken.</span><span class="sxs-lookup"><span data-stu-id="f9155-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="f9155-341">Totalt er bestillingene og tilordningene avstemte, men de skiller seg fra én uke til den neste.</span><span class="sxs-lookup"><span data-stu-id="f9155-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="f9155-342">Når du viser tid på høyere nivåer, har celler i **Avstemming**-kategorien en indikator som informerer deg om at det er forskjeller på lavere nivåer.</span><span class="sxs-lookup"><span data-stu-id="f9155-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="f9155-343">Ved å dobbeltklikke i en celle kan du zoome inn for å vise forskjellen.</span><span class="sxs-lookup"><span data-stu-id="f9155-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="f9155-344">Du kan deretter høyreklikke for å zoome ut. Ved å velge en ressurs og deretter bruke kontrollen **Neste forskjell** på verktøylinjen i rutenettet kan du gå til den neste forskjellen mellom bestillinger og tildelinger for denne ressursen.</span><span class="sxs-lookup"><span data-stu-id="f9155-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="f9155-345">Deretter kan du bruke kontrollen **Forrige forskjell** til å gå tilbake.</span><span class="sxs-lookup"><span data-stu-id="f9155-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="f9155-346">Du kan også slå av forskjellsindikatoren og virkemåten for navigasjon under **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="f9155-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Forskjellsindikator](media/Resource-Management-image57.png)

<span data-ttu-id="f9155-348">Hvis du har oppgavetildelinger for en ressurs, men ingen bestillinger, går du til **Prosjekter**-siden, i kategorien **Avstemming** og velger **Utvid bestilling**.</span><span class="sxs-lookup"><span data-stu-id="f9155-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="f9155-349">Dialogboksen **Utvid bestilling** vises med bestillingen som er nødvendig for å løse ressursens underskudd.</span><span class="sxs-lookup"><span data-stu-id="f9155-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="f9155-350">Den viser også ressursens eksisterende bestillinger på tvers av alle prosjekter eller andre enheter som kan planlegges.</span><span class="sxs-lookup"><span data-stu-id="f9155-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="f9155-351">Hvis du velger **OK** for å opprette en bestilling for ressursen, uavhengig av om ressursen er tilgjengelig, kan det oppstå overbestilling.</span><span class="sxs-lookup"><span data-stu-id="f9155-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Dialogboksen Utvid bestilling](media/Resource-Management-image58.png)

<span data-ttu-id="f9155-353">Prosjektlederen eller ressurslederen kan deretter bruke planleggingstavlen til å behandle eventuelle situasjoner der en ressurs er overbestilt utover dens kapasitet.</span><span class="sxs-lookup"><span data-stu-id="f9155-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
