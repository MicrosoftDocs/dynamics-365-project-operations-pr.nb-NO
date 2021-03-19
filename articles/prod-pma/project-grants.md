---
title: Prosjektstøtte
description: Dette emnet forklarer hvordan du oppretter eller endrer et tilskudd.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
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
ms.openlocfilehash: dfd91e859244cc03b9b358b057bded79eeea0182
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289381"
---
# <a name="project-grants"></a><span data-ttu-id="eba9a-103">Prosjektstøtte</span><span class="sxs-lookup"><span data-stu-id="eba9a-103">Project grants</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eba9a-104">Et tilskudd er en pengegave for et bestemt formål eller prosjekt.</span><span class="sxs-lookup"><span data-stu-id="eba9a-104">A grant is a gift of money for a specific purpose or project.</span></span> <span data-ttu-id="eba9a-105">Det finnes vanligvis begrensninger for hvordan et tilskudd kan brukes.</span><span class="sxs-lookup"><span data-stu-id="eba9a-105">Usually, there are restrictions on how a grant can be spent.</span></span> <span data-ttu-id="eba9a-106">I Prosjektstyring og regnskap kan du angi og spore tilskudd og definere relasjoner til prosjekter og prosjektkontrakter.</span><span class="sxs-lookup"><span data-stu-id="eba9a-106">In Project management and accounting, you can enter and track grants, and define their relationships to projects and project contracts.</span></span> <span data-ttu-id="eba9a-107">Du kan for eksempel utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="eba9a-107">For example, you can perform the following tasks:</span></span>

- <span data-ttu-id="eba9a-108">Du kan knytte tilskudd til prosjekter og finansieringskilder via koblinger til sidene **Prosjekt** og **Prosjektkontraktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="eba9a-108">Associate grants with projects and funding sources through links to the **Project** and **Project contract details** pages.</span></span>
- <span data-ttu-id="eba9a-109">Angi og spore endringer i et tilskudd når det går fra én status til en annen.</span><span class="sxs-lookup"><span data-stu-id="eba9a-109">Enter and track changes to a grant as it moves from one status to another.</span></span>
- <span data-ttu-id="eba9a-110">Angi og spore kostnader, ønskede beløp og tildelte beløp.</span><span class="sxs-lookup"><span data-stu-id="eba9a-110">Enter and track costs, requested amounts, and awarded amounts.</span></span>
- <span data-ttu-id="eba9a-111">Opprett hovedtilskudd, og knytt undertilskudd til dem.</span><span class="sxs-lookup"><span data-stu-id="eba9a-111">Create master grants, and associate subgrants with them.</span></span>

<span data-ttu-id="eba9a-112">Du kan opprette et tilskudd ved å angi alle detaljene i en ny oppføring, eller du kan kopiere detaljene fra et eksisterende tilskudd og deretter oppdatere dem.</span><span class="sxs-lookup"><span data-stu-id="eba9a-112">You can create a grant by entering all the details in a new record, or you can copy the details from an existing grant and then update them.</span></span>

## <a name="create-a-new-grant"></a><span data-ttu-id="eba9a-113">Opprett et nytt tilskudd</span><span class="sxs-lookup"><span data-stu-id="eba9a-113">Create a new grant</span></span>

1. <span data-ttu-id="eba9a-114">Gå til **Prosjektstyring og regnskap** \> **Tilskudd** \> **Tilskudd**.</span><span class="sxs-lookup"><span data-stu-id="eba9a-114">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="eba9a-115">Velg **Nytt** \> **Tilskudd**.</span><span class="sxs-lookup"><span data-stu-id="eba9a-115">Select **New** \> **Grant**.</span></span>
3. <span data-ttu-id="eba9a-116">På siden med tilskuddsdetaljer, på hurtigfanen **Generelt**, i feltet **Tilskudds-ID**, angir du en alfanumerisk identifikator for tilskuddet.</span><span class="sxs-lookup"><span data-stu-id="eba9a-116">On the grant details page, on the **General** FastTab, in the **Grant ID** field, enter an alphanumeric identifier for the grant.</span></span>
4. <span data-ttu-id="eba9a-117">Skriv inn et navn på tilskuddet i feltet **Navn på tilskudd**.</span><span class="sxs-lookup"><span data-stu-id="eba9a-117">In the **Grant name** field, enter a name for the grant.</span></span>
5. <span data-ttu-id="eba9a-118">I **Beskrivelse**-feltet legger du til detaljer om det nye tilskuddet.</span><span class="sxs-lookup"><span data-stu-id="eba9a-118">In the **Description** field, add details about the new grant.</span></span>

    <span data-ttu-id="eba9a-119">De fleste av de andre feltene på siden er valgfrie, og du kan angi så lite eller så mye informasjon som du ønsker.</span><span class="sxs-lookup"><span data-stu-id="eba9a-119">Most of the other fields on the page are optional, and you can enter as little or as much information as you want.</span></span>

    <span data-ttu-id="eba9a-120">Følgende liste beskriver informasjonen som er angitt på hver hurtigfane på siden med tilskuddsdetaljer:</span><span class="sxs-lookup"><span data-stu-id="eba9a-120">The following list describes the information that is specified on each FastTab of the grant details page:</span></span>

    - <span data-ttu-id="eba9a-121">**Generelt** – Angi navnet på tilskuddet, status, beskrivelse, formål og beløp.</span><span class="sxs-lookup"><span data-stu-id="eba9a-121">**General** – Enter the grant name, status, description, purpose, and amount.</span></span>
    - <span data-ttu-id="eba9a-122">**Kontaktinformasjon** – Angi detaljer om ansatte, avdelingen som håndterer tilskuddet, og tilskuddskunden eller organisasjonskilden for tilskuddet.</span><span class="sxs-lookup"><span data-stu-id="eba9a-122">**Contact information** – Enter details about staff members, the department that manages the grant, and the grant customer or organization source of the grant.</span></span> <span data-ttu-id="eba9a-123">Du kan også angi om organisasjonen er et mellomledd som mottar tilskuddet og deretter sender det til en annen mottaker.</span><span class="sxs-lookup"><span data-stu-id="eba9a-123">You can also indicate whether your organization is a pass-through entity that receives the grant and then passes it on to another recipient.</span></span> <span data-ttu-id="eba9a-124">Velg **Legg til** for å legge til kontaktinformasjon, for eksempel telefonnumre og e-postadresser, for organisasjonen som gir tilskuddet.</span><span class="sxs-lookup"><span data-stu-id="eba9a-124">Select **Add** to add contact information such as telephone numbers and email addresses for the organization that provides the grant.</span></span>
    - <span data-ttu-id="eba9a-125">**Datoer og tidsfrister** – Angi datoer som er relatert til tilskuddet og tilskuddsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="eba9a-125">**Dates and deadlines** – Enter dates that are related to the grant and the grant application.</span></span> <span data-ttu-id="eba9a-126">Eksempler inkluderer søknadens forfallsdato, sendedatoen og datoen for når tilskuddet er godkjent eller avvist.</span><span class="sxs-lookup"><span data-stu-id="eba9a-126">Examples include the application due date, the submission date, and the date when the grant is approved or rejected.</span></span>
    - <span data-ttu-id="eba9a-127">**Tilknyttede prosjekter og prosjektkontrakter** – Du kan angi informasjon på denne hurtigfanen bare hvis **Tilskuddsstatus**-feltet på hurtigfanen **Generelt** er angitt til **Aktiv** eller **Tildelt**.</span><span class="sxs-lookup"><span data-stu-id="eba9a-127">**Associated projects and project contracts** – You can enter information on this FastTab only if the **Grant status** field on the **General** FastTab is set to **Active** or **Awarded**.</span></span> <span data-ttu-id="eba9a-128">Velg blant følgende alternativer for å fullføre den relaterte oppgaven:</span><span class="sxs-lookup"><span data-stu-id="eba9a-128">Select among the following options to complete the related task:</span></span>

        - <span data-ttu-id="eba9a-129">**Legg til finansieringskilde** – Legg til en ny finansieringskilde for tilskuddet.</span><span class="sxs-lookup"><span data-stu-id="eba9a-129">**Add funding source** – Add a new funding source for the grant.</span></span> <span data-ttu-id="eba9a-130">Du kan skrive inn alle detaljene nå, eller du kan bruke standardinformasjonen og deretter oppdatere den senere.</span><span class="sxs-lookup"><span data-stu-id="eba9a-130">You can enter all the details now, or you can use default information and then update it later.</span></span>
        - <span data-ttu-id="eba9a-131">**Legg til prosjektkontrakt** – Legg til eller oppdater informasjon om prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="eba9a-131">**Add project contract** – Add or update project contract information.</span></span>
        - <span data-ttu-id="eba9a-132">**Legg til prosjekt** – Legg til eller oppdater prosjektdetaljer.</span><span class="sxs-lookup"><span data-stu-id="eba9a-132">**Add project** – Add or update project details.</span></span>

    - <span data-ttu-id="eba9a-133">**Oppsett** – Angi detaljer om matchende midler hvis denne informasjonen er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="eba9a-133">**Setup** – Enter details about matching funds, if this information is required.</span></span> <span data-ttu-id="eba9a-134">Mange organisasjoner som tildeler tilskudd, krever at mottakerne bruker et bestemt beløp av sine egne penger eller ressurser, slik at de matcher beløpet som er tildelt tilskuddet.</span><span class="sxs-lookup"><span data-stu-id="eba9a-134">Many organizations that award grants require that recipients spend a specific amount of their own money or resources, to match the amount that is awarded in the grant.</span></span> <span data-ttu-id="eba9a-135">I feltet **Lokalt prosjekt eller sporings-ID** kan du angi en identifikator som er forskjellig fra prosjektidentifikatoren.</span><span class="sxs-lookup"><span data-stu-id="eba9a-135">In the **Local project or tracking ID** field, you can enter an identifier that differs from the project identifier.</span></span>

        > [!NOTE]
        > <span data-ttu-id="eba9a-136">Hvis en del av tilskuddet skal tildeles en annen organisasjon, setter du alternativet **Underordnet tilskuddsgiver** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="eba9a-136">If part of the grant will be awarded to a different organization, set the **Subgrantor** option to **Yes**.</span></span> <span data-ttu-id="eba9a-137">For tilskudd som tildeles i USA, kan du angi om et tilskudd skal tildeles under et delstatsmandat eller et føderalt mandat.</span><span class="sxs-lookup"><span data-stu-id="eba9a-137">For grants that are awarded in the United States, you can specify whether a grant will be awarded under a state mandate or a federal mandate.</span></span>

    - <span data-ttu-id="eba9a-138">**Nedtegningsdetaljer** – Legg til eller oppdater informasjon om hvor ofte tilskuddsmidler kan trekkes tilbake, faktureres eller brukes.</span><span class="sxs-lookup"><span data-stu-id="eba9a-138">**Drawdown details** – Add or update information about how often grant funds can be withdrawn, billed for, or spent.</span></span>

## <a name="create-a-new-grant-from-a-copy"></a><span data-ttu-id="eba9a-139">Opprette et nytt tilskudd fra en kopi</span><span class="sxs-lookup"><span data-stu-id="eba9a-139">Create a new grant from a copy</span></span>

1. <span data-ttu-id="eba9a-140">Gå til **Prosjektstyring og regnskap** \> **Tilskudd** \> **Tilskudd**.</span><span class="sxs-lookup"><span data-stu-id="eba9a-140">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="eba9a-141">Velg **Ny** \> **Kopier fra tilskudd**.</span><span class="sxs-lookup"><span data-stu-id="eba9a-141">Select **New** \> **Copy from grant**.</span></span>
3. <span data-ttu-id="eba9a-142">Angi en alfanumerisk identifikator og et navn for det nye tilskuddet, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba9a-142">Enter an alphanumeric identifier and a name for the new grant, and then select **OK**.</span></span>
4. <span data-ttu-id="eba9a-143">Gå gjennom detaljene for det kopierte tilskuddet på siden med tilskuddsdetaljer, og gjør de nødvendige endringene.</span><span class="sxs-lookup"><span data-stu-id="eba9a-143">On the grant details page, review the details of the copied grant, and make any changes that are required.</span></span> <span data-ttu-id="eba9a-144">De fleste feltene på siden er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="eba9a-144">Most of the fields on the page are optional.</span></span>

## <a name="view-or-modify-grant-details"></a><span data-ttu-id="eba9a-145">Vise eller endre tilskuddsdetaljer</span><span class="sxs-lookup"><span data-stu-id="eba9a-145">View or modify grant details</span></span>

1. <span data-ttu-id="eba9a-146">Gå til **Prosjektstyring og regnskap** \> **Tilskudd** \> **Tilskudd**.</span><span class="sxs-lookup"><span data-stu-id="eba9a-146">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="eba9a-147">Velg tilskuddet du vil endre.</span><span class="sxs-lookup"><span data-stu-id="eba9a-147">Select the grant to modify.</span></span>
3. <span data-ttu-id="eba9a-148">I handlingsruten i kategorien **Tilskudd** i gruppen **Vedlikehold** velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="eba9a-148">On the Action Pane, on the **Grant** tab, in the **Maintain** group, select **Edit**.</span></span>
4. <span data-ttu-id="eba9a-149">Se gjennom tilskuddsdetaljene, og gjør de nødvendige endringene.</span><span class="sxs-lookup"><span data-stu-id="eba9a-149">Review the grant details, and make any changes that are required.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]