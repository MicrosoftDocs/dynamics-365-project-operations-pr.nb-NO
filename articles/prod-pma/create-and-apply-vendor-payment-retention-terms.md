---
title: Opprette og bruke tilbakeholdelsesbetingelser for leverandørbetaling
description: Dette emnet gir informasjon om hvordan du setter opp og vedlikeholder tilbakeholdelsesbetingelser for leverandørbetalinger.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081757"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="9666a-103">Opprette og bruke tilbakeholdelsesbetingelser for leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="9666a-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="9666a-104">Det er nyttig å konfigurere tilbakeholdelsesbetingelser for leverandørbetalinger for et prosjekt når organisasjonen vil beholde en del av betalingene til en leverandør.</span><span class="sxs-lookup"><span data-stu-id="9666a-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="9666a-105">Dette kan for eksempel være når du vil holde tilbake betalingen til en leverandør til de leverte produktene oppfyller forventningene dine.</span><span class="sxs-lookup"><span data-stu-id="9666a-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="9666a-106">Du kan angi tilbakeholdelsesbetingelser for leverandørbetalinger når du forhandler om en leverandørkontrakt.</span><span class="sxs-lookup"><span data-stu-id="9666a-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="9666a-107">Opprette tilbakeholdelsesbetingelser for leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="9666a-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="9666a-108">Du kan angi prosentandelen av leverandørbetalingen for tilbakeholding og prosentandelen av de tidligere tilbakeholdte beløpene som skal frigis.</span><span class="sxs-lookup"><span data-stu-id="9666a-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="9666a-109">Beløpene tilbakeholdes automatisk på leverandørfakturaer til kontrakten når den angitte fullføringsstatusen.</span><span class="sxs-lookup"><span data-stu-id="9666a-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="9666a-110">Når du har angitt tilbakeholdelsesvilkårene, kan du bruke dem på alle prosjekter for den aktuelle leverandøren.</span><span class="sxs-lookup"><span data-stu-id="9666a-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="9666a-111">Bruk fremgangsmåten nedenfor for å konfigurere og vedlikeholde tilbakeholdingsbetingelser for leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="9666a-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="9666a-112">Gå til **Prosjektstyring og regnskap** > **Tilbakeholding** > **Tilbakeholdelsesbetingelser for leverandørbetaling**.</span><span class="sxs-lookup"><span data-stu-id="9666a-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="9666a-113">Velg **Ny** for å legge til en ny tilbakeholdingsbetingelse for en leverandør.</span><span class="sxs-lookup"><span data-stu-id="9666a-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="9666a-114">Verdien for **Regel-ID** for den nye betingelsen angis automatisk.</span><span class="sxs-lookup"><span data-stu-id="9666a-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="9666a-115">Skriv inn en kort beskrivelse i **Beskrivelse** -feltet, og gå til hurtigfanen **Betingelser** og velg **Legg til linje** for å angi betingelsesverdier for følgende:</span><span class="sxs-lookup"><span data-stu-id="9666a-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="9666a-116">**Prosentandel av leverte enheter** : Angi en fullføringsprosent for betingelsen.</span><span class="sxs-lookup"><span data-stu-id="9666a-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="9666a-117">Beløpene tilbakeholdes automatisk på leverandørfakturaer til prosjektets fullføringsfase er lik den angitte prosentandelen.</span><span class="sxs-lookup"><span data-stu-id="9666a-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="9666a-118">Hvis du for eksempel angir 50,00, beholdes beløpene til prosjektet er 50 prosent fullført.</span><span class="sxs-lookup"><span data-stu-id="9666a-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="9666a-119">**Prosentandel som skal tilbakeholdes** : Angi en prosentandel av leverandørfakturabeløpet som skal tilbakeholdes.</span><span class="sxs-lookup"><span data-stu-id="9666a-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="9666a-120">Hvis du for eksempel angir 10,00, tilbakeholdes 10 prosent av beløpet på en leverandørfaktura til prosjektet når fullføringsprosenten som angitt i feltet **Prosentandel av leverte enheter**.</span><span class="sxs-lookup"><span data-stu-id="9666a-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="9666a-121">**Prosentandel som skal frigis** : Velg **Legg til linje** for å angi en prosentandel av eventuelle tidligere tilbakeholdte beløp som skal frigis for det valgte fullføringsnivået for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="9666a-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="9666a-122">Hvis du har mer enn én milepæl for ulike nivåer av prosjektfullføring, angir du en egen betingelseslinje for tilbakeholdelse for leverandører for hver tilbakeholdelsesregel.</span><span class="sxs-lookup"><span data-stu-id="9666a-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="9666a-123">Hver linje kan angi en annen tilbakeholdingsprosent og en annen frigivelsesprosent for hvert angitte prosjektfullføringsnivå.</span><span class="sxs-lookup"><span data-stu-id="9666a-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="9666a-124">Når du har opprettet tilbakeholdelsesvilkår for en leverandør, kan du bruke vilkårene på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="9666a-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="9666a-125">Bruke tilbakeholdelsesbetingelser for en leverandør på et prosjekt</span><span class="sxs-lookup"><span data-stu-id="9666a-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="9666a-126">Gå til **Prosjektstyring og regnskap** > **Prosjekter** > **Alle prosjekter** , og åpne et prosjekt fra prosjektlistesiden.</span><span class="sxs-lookup"><span data-stu-id="9666a-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="9666a-127">På hurtigfanen **Leverandøravtaler** velger du **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="9666a-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="9666a-128">Velg ett av følgende alternativer i feltet **Kontokode** :</span><span class="sxs-lookup"><span data-stu-id="9666a-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="9666a-129">**Tabell** : Tilbakeholdelsesbetingelsene for leverandører gjelder for én enkelt leverandør.</span><span class="sxs-lookup"><span data-stu-id="9666a-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="9666a-130">**Gruppe** : Tilbakeholdelsesbetingelsene for leverandører gjelder for alle leverandører i en leverandørgruppe.</span><span class="sxs-lookup"><span data-stu-id="9666a-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="9666a-131">**Alle** : Tilbakeholdelsesbetingelsene for leverandører gjelder for alle leverandører.</span><span class="sxs-lookup"><span data-stu-id="9666a-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="9666a-132">I feltet the **Leverandør/Leverandørgruppe** velger du leverandøren eller leverandørgruppen som tilbakeholdelsesbetingelsene for leverandører gjelder for.</span><span class="sxs-lookup"><span data-stu-id="9666a-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="9666a-133">Hvis du valgte **Alle** i forrige trinn, er dette feltet ikke tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="9666a-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="9666a-134">I feltet **Tilbakeholdelsesbetingelser for leverandører** velger du tilbakeholdelsesbetingelsene som du opprettet i den forrige prosedyren.</span><span class="sxs-lookup"><span data-stu-id="9666a-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="9666a-135">Hvis prosjektet også har PWP-betingelser (betal når betalt) satt opp for leverandøren, angir du terskelprosenten for prosjektet i feltet **PWP-terskelprosent**.</span><span class="sxs-lookup"><span data-stu-id="9666a-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="9666a-136">Tilbakeholdelsesbetingelsene for leverandører vises også i bestillinger som du oppretter for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="9666a-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
