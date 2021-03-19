---
title: Forespørsel om tidsplan for utgifter til føderale tilskudd
description: Dette emnet gir informasjon om tidsplanen for forespørselen om tidsplan for utgifter til føderale tilskudd.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288976"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="72a66-103">Forespørsel om tidsplan for utgifter til føderale tilskudd</span><span class="sxs-lookup"><span data-stu-id="72a66-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72a66-104">I henhold til Office of Management and Budget Circular A-133, er byråer som mottar føderale tilskudd, underlagt revisjonskrav, som også er kjent som enkeltrevisjoner.</span><span class="sxs-lookup"><span data-stu-id="72a66-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="72a66-105">Revisjonsprosessen brukes til å rapportere om inntektene og utgiftene av føderale tilskudd på en regelmessig basis.</span><span class="sxs-lookup"><span data-stu-id="72a66-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="72a66-106">En del av rapporten om enkel revisjon omfatter tidsplanen for utgifter til føderale tilskudd (SEFA).</span><span class="sxs-lookup"><span data-stu-id="72a66-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="72a66-107">Forespørselen om tidsplanen for utgifter til føderale tilskudd inkluderer tittel og nummer for Catalog of Federal Domestic Assistance (CFDA), tilskuddsnummeret, året for tilskuddet, navnet på det føderale byrået som skaffer midlene, og navnet på mellomleddet.</span><span class="sxs-lookup"><span data-stu-id="72a66-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="72a66-108">Forespørselen gjelder for en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="72a66-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="72a66-109">Denne perioden er vanligvis den samme som regnskapsoppgjørsperioden, som er et regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="72a66-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="72a66-110">Forespørselen inkluderer tilskudd som har projeksjonsdatoer i det valgte datointervallet.</span><span class="sxs-lookup"><span data-stu-id="72a66-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="72a66-111">**Tilskuddsbyrå**-kolonnen i forespørselen viser tilskuddskunden eller, for et tilskudd med mellomledd, tilskuddsbyrået.</span><span class="sxs-lookup"><span data-stu-id="72a66-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="72a66-112">For et tilskudd med mellomledd, viser **Mellomledd**-kolonnen tilskuddskunden.</span><span class="sxs-lookup"><span data-stu-id="72a66-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="72a66-113">Hvis tilskuddet ikke er et tilskudd med mellomledd, er **Mellomledd**-kolonnen tom.</span><span class="sxs-lookup"><span data-stu-id="72a66-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="72a66-114">Konfigurere CFDA-klyngene</span><span class="sxs-lookup"><span data-stu-id="72a66-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="72a66-115">Du må konfigurere CFDA-klyngene som kan knyttes til CFDA-numre i forespørselen om tidsplan for utgifter til føderale tilskudd.</span><span class="sxs-lookup"><span data-stu-id="72a66-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="72a66-116">Gå til **Prosjektstyring og regnskap \> Oppsett \> Tilskudd \> Katalog over Federal Domestic Assistance-klynger**.</span><span class="sxs-lookup"><span data-stu-id="72a66-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="72a66-117">Velg **Ny** for å opprette en CFDA-klynge.</span><span class="sxs-lookup"><span data-stu-id="72a66-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="72a66-118">Skriv inn navnet på klyngen.</span><span class="sxs-lookup"><span data-stu-id="72a66-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="72a66-119">Velg **Lagre** for å ta i bruk endringene.</span><span class="sxs-lookup"><span data-stu-id="72a66-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="72a66-120">Konfigurere CFDA-numre</span><span class="sxs-lookup"><span data-stu-id="72a66-120">Set up CFDA numbers</span></span>

<span data-ttu-id="72a66-121">Du må konfigurere CFDA-numrene som kan legges til for tilskudd og inkluderes i forespørselen om tidsplan for utgifter til føderale tilskudd.</span><span class="sxs-lookup"><span data-stu-id="72a66-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="72a66-122">Gå til **Prosjektstyring og regnskap \> Oppsett \> Tilskudd \> Katalog over Federal Domestic Assistance-numre**.</span><span class="sxs-lookup"><span data-stu-id="72a66-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="72a66-123">Velg **Ny** for å opprette et CFDA-nummer.</span><span class="sxs-lookup"><span data-stu-id="72a66-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="72a66-124">Angi CFDA-nummeret i **Nummer**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="72a66-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="72a66-125">Trykk på **Tab**-tasten.</span><span class="sxs-lookup"><span data-stu-id="72a66-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="72a66-126">Angi CFDA-tittelen i **Beskrivelse**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="72a66-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="72a66-127">Trykk på **Tab**-tasten.</span><span class="sxs-lookup"><span data-stu-id="72a66-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="72a66-128">Valgfritt: I feltet **Programklynge** legger du til riktig CFDA-klynge.</span><span class="sxs-lookup"><span data-stu-id="72a66-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="72a66-129">Velg **Lagre** for å ta i bruk endringene.</span><span class="sxs-lookup"><span data-stu-id="72a66-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="72a66-130">Sett opp tilskudd som skal rapporteres for forespørselen om tidsplan for utgifter til føderale tilskudd</span><span class="sxs-lookup"><span data-stu-id="72a66-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="72a66-131">Gå til **Prosjektstyring og regnskap \> Tilskudd \> Tilskudd**, og velg et eksisterende tilskudd.</span><span class="sxs-lookup"><span data-stu-id="72a66-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="72a66-132">På hurtigfanen **Oppsett** i feltet **Katalog over Federal Domestic Assistance**, tilordner du CFFDA-nummeret.</span><span class="sxs-lookup"><span data-stu-id="72a66-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="72a66-133">CFDA-nummeret på tilskuddet avgjør CFDA-klyngen for rapportering.</span><span class="sxs-lookup"><span data-stu-id="72a66-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="72a66-134">På hurtigfanen **Kontaktinformasjon** angir du informasjon om giveren ved å følge disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="72a66-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="72a66-135">Angi kunden som er ansvarlig for tilskuddet, i feltet **Tilskuddskunde**.</span><span class="sxs-lookup"><span data-stu-id="72a66-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="72a66-136">Denne informasjonen er kanskje allerede angitt for et eksisterende tilskudd.</span><span class="sxs-lookup"><span data-stu-id="72a66-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="72a66-137">Angi om tilskuddskunden er giveren.</span><span class="sxs-lookup"><span data-stu-id="72a66-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="72a66-138">Hvis tilskuddskunden er giveren, kan du la avmerkingsboksen **Mellomledd** stå tom.</span><span class="sxs-lookup"><span data-stu-id="72a66-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="72a66-139">Hvis en annen kunde er giveren, og tilskuddskunden er ansvarlig for å bruke og spore pengene, merker du av for **Mellomledd**-boksen.</span><span class="sxs-lookup"><span data-stu-id="72a66-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="72a66-140">Hvis har merket av for **Mellomledd** i forrige trinn, må du angi kunden som tilbydde tilskuddet, i feltet **Giverbyrå**.</span><span class="sxs-lookup"><span data-stu-id="72a66-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="72a66-141">Giverbyrået og tilskuddskunden kan ikke være samme kunde.</span><span class="sxs-lookup"><span data-stu-id="72a66-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="72a66-142">Her er et eksempel på et tilskudd med mellomledd:</span><span class="sxs-lookup"><span data-stu-id="72a66-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="72a66-143">Den føderale føderale regjeringen finansierte et infrastrukturprosjekt for en delstat.</span><span class="sxs-lookup"><span data-stu-id="72a66-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="72a66-144">Den føderale regjeringen ga pengene til delstaten for forbruk.</span><span class="sxs-lookup"><span data-stu-id="72a66-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="72a66-145">I dette tilfellet er det den føderale regjeringen som er giverbyrået, og delstaten som er tilskuddskunden.</span><span class="sxs-lookup"><span data-stu-id="72a66-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="72a66-146">Første gang du aktiverer funksjonen, blir opprinnelige CFDA-numre angitt ved hjelp av eksisterende numre på tilskudd.</span><span class="sxs-lookup"><span data-stu-id="72a66-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="72a66-147">Utelate tilskudd fra SEFA-rapportering basert på tilskuddstypen</span><span class="sxs-lookup"><span data-stu-id="72a66-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="72a66-148">Gå til **Prosjektstyring og regnskap \> Oppsett \> Tilskudd \> Tilskuddstyper**.</span><span class="sxs-lookup"><span data-stu-id="72a66-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="72a66-149">På hurtigfanen **Standardinformasjon** merker du av for **Utelat fra utgiftsplan for føderale tilskudd**.</span><span class="sxs-lookup"><span data-stu-id="72a66-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="72a66-150">Velg **Lagre** for å ta i bruk endringene.</span><span class="sxs-lookup"><span data-stu-id="72a66-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="72a66-151">Kjøre forespørselen om tidsplan for utgifter til føderale tilskudd</span><span class="sxs-lookup"><span data-stu-id="72a66-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="72a66-152">Gå til **Prosjektstyring og regnskap \> Forespørsler og rapporter \> Tilskuddsforespørsel \> Tidsplan for utgifter til føderale tilskudd**.</span><span class="sxs-lookup"><span data-stu-id="72a66-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="72a66-153">Følg fremgangsmåten nedenfor i **Parametere**-delen:</span><span class="sxs-lookup"><span data-stu-id="72a66-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="72a66-154">I **Datointervall**-feltet velger du koden for datointervallet.</span><span class="sxs-lookup"><span data-stu-id="72a66-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="72a66-155">Du kan også definere datointervallet i feltene **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="72a66-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="72a66-156">Valgfritt: Hvis du bare vil ta med fakturerte transaksjoner som inntekt i forespørselen, setter du alternativet **Inkludert bare fakturert inntekt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="72a66-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="72a66-157">Kolonner</span><span class="sxs-lookup"><span data-stu-id="72a66-157">Columns</span></span>

<span data-ttu-id="72a66-158">Forespørselen om tidsplan for utgifter til føderale tilskudd inkluderer følgende kolonner:</span><span class="sxs-lookup"><span data-stu-id="72a66-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="72a66-159">Navn på katalog over Federal Domestic Assistance-klynger</span><span class="sxs-lookup"><span data-stu-id="72a66-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="72a66-160">Giverbyrå</span><span class="sxs-lookup"><span data-stu-id="72a66-160">Grantor agency</span></span>
- <span data-ttu-id="72a66-161">Mellomledd</span><span class="sxs-lookup"><span data-stu-id="72a66-161">Pass-through agency</span></span>
- <span data-ttu-id="72a66-162">Navn på tilskudd</span><span class="sxs-lookup"><span data-stu-id="72a66-162">Grant name</span></span>
- <span data-ttu-id="72a66-163">Tilskudds-ID</span><span class="sxs-lookup"><span data-stu-id="72a66-163">Grant ID</span></span>
- <span data-ttu-id="72a66-164">Tilskuddssøknads-ID</span><span class="sxs-lookup"><span data-stu-id="72a66-164">Grant application ID</span></span>
- <span data-ttu-id="72a66-165">Katalog over Federal Domestic Assistance</span><span class="sxs-lookup"><span data-stu-id="72a66-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="72a66-166">Kvitteringer</span><span class="sxs-lookup"><span data-stu-id="72a66-166">Receipts</span></span>
- <span data-ttu-id="72a66-167">Utgifter</span><span class="sxs-lookup"><span data-stu-id="72a66-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]