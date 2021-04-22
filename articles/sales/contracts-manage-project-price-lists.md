---
title: Administrere prosjektprislister i prosjektkontrakter
description: Dette emnet gir informasjon om behandling av prosjektprislister på prosjektkontrakter.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ffc48782394995781535ae56142dc76afeb9a040
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858575"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="78f36-103">Administrere prosjektprislister i prosjektkontrakter</span><span class="sxs-lookup"><span data-stu-id="78f36-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="78f36-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="78f36-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="78f36-105">Prosjektkontrakter i Dynamics 365 Project Operations er utformet for å støtte flere salgsprislister med gyldighetsdato på en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="78f36-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="78f36-106">In Project Operations er det en ny tilknyttet enhet kalt **Prosjektprislister**.</span><span class="sxs-lookup"><span data-stu-id="78f36-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="78f36-107">Denne enheten har en én-til-mange-relasjon til en prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="78f36-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="78f36-108">Prosjektprislister brukes til å prise tids-, material- og utgiftstransaksjoner for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="78f36-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="78f36-109">Når en kontrakt har en eller flere prosjektprislister, brukes disse prislistene til å prise for tid, materiell, kostnadsestimater og faktiske verdier for prosjekter som er knyttet til kontrakten via kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="78f36-109">When a contract has one or more project price lists, these price lists are used to price for time, material, expense estimates, and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="78f36-110">Når det ikke finnes prosjektprislister på en prosjektkontrakt, vises en advarsel om at det ikke finnes prosjektprislister, og at estimater, faktisk prosjektarbeid, materiale og utgifter som er logget, ikke er priset.</span><span class="sxs-lookup"><span data-stu-id="78f36-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, material, and expenses logged will not be priced.</span></span> <span data-ttu-id="78f36-111">Det vil ikke være pris for salgsverdier.</span><span class="sxs-lookup"><span data-stu-id="78f36-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="78f36-112">Knytte eller oppheve tilknytningen til en prosjektprisliste i en prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="78f36-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a><span data-ttu-id="78f36-113">Opprett eller tilknytt en bestemt prisliste for beregning av prosjektbasert arbeid, materiell og utgifter</span><span class="sxs-lookup"><span data-stu-id="78f36-113">Create or associate a specific price list for estimating project-based work, material, and expenses</span></span>

1. <span data-ttu-id="78f36-114">Velg kategorien **Prosjektprislister** i prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="78f36-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="78f36-115">Velg **+ Legg til ny prosjektprisliste** i delrutenettet.</span><span class="sxs-lookup"><span data-stu-id="78f36-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="78f36-116">Velg en prisliste på glidebryteren **Hurtigoppretting**.</span><span class="sxs-lookup"><span data-stu-id="78f36-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="78f36-117">Rullegardinlisten viser alle prislister som har konteksten satt til **Salg**, der valutaen på prislisten samsvarer med valutaen på kontrakten.</span><span class="sxs-lookup"><span data-stu-id="78f36-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="78f36-118">Skriv inn en beskrivelse for prosjektprislistetilknytningen, velg **Lagre**, og lukk deretter **Hurtigoppretting**-glidebryteren.</span><span class="sxs-lookup"><span data-stu-id="78f36-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="78f36-119">En tilknytning for prosjektprislisten opprettes.</span><span class="sxs-lookup"><span data-stu-id="78f36-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="78f36-120">Gjenta trinn 1–4 for å knytte mer enn én prosjektprisliste til prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="78f36-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="78f36-121">Bare opprett flere prosjektprislister hvis du har ulik gyldighetsdato for hver av de tilknyttede prosjektprislistene.</span><span class="sxs-lookup"><span data-stu-id="78f36-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="78f36-122">Project Operations støtter ikke overlappende gyldighetsdato for prosjektprislistene.</span><span class="sxs-lookup"><span data-stu-id="78f36-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="78f36-123">Hvis det finnes flere prosjektprislister for en transaksjon med en gitt dato, blir prisen på transaksjonen som standard null.</span><span class="sxs-lookup"><span data-stu-id="78f36-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="78f36-124">Fjerne en tilknytning til en prosjektprisliste</span><span class="sxs-lookup"><span data-stu-id="78f36-124">Remove a project price list association</span></span>

- <span data-ttu-id="78f36-125">Velg prosjektprislisten, og velg deretter valget for **slett kontraktprosjektprisliste** i delrutenettet.</span><span class="sxs-lookup"><span data-stu-id="78f36-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="78f36-126">Prislisten fjernes fra prosjektprislistene i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="78f36-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="78f36-127">Selve prislisten blir ikke slettet.</span><span class="sxs-lookup"><span data-stu-id="78f36-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="78f36-128">Bare tilknytningen til kontrakten blir slettet.</span><span class="sxs-lookup"><span data-stu-id="78f36-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="78f36-129">Konfigurere automatisk standardering av prosjektprislister på en kontrakt</span><span class="sxs-lookup"><span data-stu-id="78f36-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="78f36-130">En prosjektprisliste kan angis som standard prosjektprisliste.</span><span class="sxs-lookup"><span data-stu-id="78f36-130">A project price list can be set up as the default project price list.</span></span> <span data-ttu-id="78f36-131">Dette oppsettet sikrer at alle kontraktene i organisasjonen alltid starter med en standard prosjektprisliste for den prisperioden.</span><span class="sxs-lookup"><span data-stu-id="78f36-131">This setup ensures that all contracts in your organization always start with a standard project price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="78f36-132">Konfigurere organisasjonsstandarden for prosjektprislister</span><span class="sxs-lookup"><span data-stu-id="78f36-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="78f36-133">Gå til **Innstillinger** > **Generelt**, og velg deretter **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="78f36-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="78f36-134">På listesiden **Aktive parametere** velger eller dobbeltklikker du oppføringen for å åpne den.</span><span class="sxs-lookup"><span data-stu-id="78f36-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="78f36-135">Når du dobbeltklikker, må du passe på at du ikke klikker på en feltverdi som er en hyperkobling.</span><span class="sxs-lookup"><span data-stu-id="78f36-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="78f36-136">På siden **Aktive parametere** velger du kategorien **Prisliste**. Et delrutenett viser en liste over standard prislister.</span><span class="sxs-lookup"><span data-stu-id="78f36-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="78f36-137">Dette er en liste over standard kostnads- og salgsprislister.</span><span class="sxs-lookup"><span data-stu-id="78f36-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="78f36-138">Det å ha en **Salg**-prisliste tilknyttet her ofr hver hver valuta du selger inn, sikrer at salgsprislisten er standard for alle kontrakter som du oppretter for kunder som utfører transaksjoner i denne valutaen.</span><span class="sxs-lookup"><span data-stu-id="78f36-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="78f36-139">Konfigurere en kundespesifikk prosjektprisliste</span><span class="sxs-lookup"><span data-stu-id="78f36-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="78f36-140">Du kan også sette opp kundespesifikke prosjektprislister når du har forhandlet en hovedprisavtale med kundene.</span><span class="sxs-lookup"><span data-stu-id="78f36-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="78f36-141">Gå til **Salg** > **Kunder**.</span><span class="sxs-lookup"><span data-stu-id="78f36-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="78f36-142">Velg kunden som har spesialprisliste, fra listen over aktive forretningsforbindelser.</span><span class="sxs-lookup"><span data-stu-id="78f36-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="78f36-143">Velg kundeoppføringen for å åpne den, og velg deretter kategorien **Prosjektprislister**. Et delrutenett viser en liste over prosjektprislister som er spesifikke for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="78f36-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="78f36-144">Opprett en ny prislistetilknytning her for å få prosjektprisliste som er spesifikk for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="78f36-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="78f36-145">Egendefinert prissetting for en prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="78f36-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="78f36-146">Når du har angitt organisasjons- og kundespesifikke standard prosjektprislister, blir prosjektkontraktene opprettet automatisk med disse prosjektprislistetilordningene.</span><span class="sxs-lookup"><span data-stu-id="78f36-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="78f36-147">Prosjektprislister i en prosjektkontrakt blir imidlertid alltid kopiert med dato og kontraktnavn lagt til.</span><span class="sxs-lookup"><span data-stu-id="78f36-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="78f36-148">Forretningsforbindelses- og prosjektlederne kan deretter begynne å gjøre endringer i prisene på disse kopiene.</span><span class="sxs-lookup"><span data-stu-id="78f36-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="78f36-149">Disse endrede prisene gjelder bare for denne prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="78f36-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
