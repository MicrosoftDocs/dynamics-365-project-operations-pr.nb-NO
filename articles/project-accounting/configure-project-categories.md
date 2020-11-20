---
title: Konfigurere prosjektkategorier
description: Denne emnet gir informasjon om konfigurering av prosjektkategorier.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131940"
---
# <a name="configure-project-categories"></a><span data-ttu-id="5b8a6-103">Konfigurere prosjektkategorier</span><span class="sxs-lookup"><span data-stu-id="5b8a6-103">Configure project categories</span></span>

<span data-ttu-id="5b8a6-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="5b8a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5b8a6-105">Project Operations tilbyr kraftige funksjoner for kategorisering av omsetning og utgifter på prosjekter.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="5b8a6-106">Kategorier gir mulighet til å rapportere og analysere prosjekttransaksjoner, og å postere til hovedboken.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="5b8a6-107">Følgende diagram illustrerer korrelasjonen mellom transaksjonskategorier, delte kategorier og prosjektkategorier.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="5b8a6-108">Transaksjonskategorier er den grunnleggende grupperingen av prosjekttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="5b8a6-109">I denne grupperingen finnes det et sett med delte kategorier som kan deles på tvers av programmer og moduler.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="5b8a6-110">For å bli enda mer spesifikk er prosjektkategorier det mest detaljerte nivået av kategorier.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="5b8a6-111">Prosjektkategorier er spesifikke for juridisk enhet, modul og program.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korrelasjonen mellom transaksjonskategorier, delte kategorier og prosjektkategorier](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="5b8a6-113">Transaksjonskategorier</span><span class="sxs-lookup"><span data-stu-id="5b8a6-113">Transaction categories</span></span>

<span data-ttu-id="5b8a6-114">Transaksjonskategorier representerer den grunnleggende grupperingen av prosjekttransaksjoner, og er ikke firma- eller transaksjonstypespesifikk.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="5b8a6-115">Ekeli bruker for eksempel kategoriene Design, Reise, Installasjon og Servicetransaksjon til å gruppere prosjekttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="5b8a6-116">Transaksjonskategorier defineres i Project Operations-modulen.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="5b8a6-117">Gå til **Innstillinger** \> **Transaksjonskategorier** for å åpne skjemaet.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="5b8a6-118">Opprett en ny transaksjonskategori enten ved å velge **Ny** eller ved å velge **Importer fra Excel**.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="5b8a6-119">Delta kategorier</span><span class="sxs-lookup"><span data-stu-id="5b8a6-119">Shared categories</span></span>

<span data-ttu-id="5b8a6-120">Dynamics 365 bruker delte kategorier til å kategorisere utgifter i forskjellige programmer, for eksempel Dynamics 365 Finance, Dynamics 365 Supply Chain og Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="5b8a6-121">For hver transaksjonskategori som opprettes, oppretter Project Operations automatisk fire relaterte delte kategorier: timer, utgift, avgifter og vare.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="5b8a6-122">Du kan se gjennom og justere de delte kategoriene ved å gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Kategorier** \> **Delte kategorier**.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="5b8a6-123">Prosjektkategorier</span><span class="sxs-lookup"><span data-stu-id="5b8a6-123">Project categories</span></span>

<span data-ttu-id="5b8a6-124">Prosjektkategorier representerer det mest detaljertenivået av kategorikonfigurasjon, og må konfigureres separat og for hvert selskap av en prosjektregnskapsfører.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="5b8a6-125">Gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Kategorier** \> **Prosjektkategorier**.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="5b8a6-126">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-126">Select **New**.</span></span>
3. <span data-ttu-id="5b8a6-127">Velg **Kategori-ID** for den delte kategorien du opprettet i den forrige delen.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="5b8a6-128">Project Operations tillater bare bruk av de delte kategoriene som er tilknyttet transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="5b8a6-129">Velg en kategorigruppe.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="5b8a6-130">Kategorigrupper</span><span class="sxs-lookup"><span data-stu-id="5b8a6-130">Category groups</span></span>

<span data-ttu-id="5b8a6-131">Kategorigrupper brukes til å dele egenskaper, primært postering av profiler, mellom relaterte prosjektkategorier.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="5b8a6-132">Det må finnes minst én kategorigruppe for hver transaksjonstype, og hver prosjektkategori er tilordnet en gruppe.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="5b8a6-133">Posteringsspesifikasjonene i Project Operations er definert av reglene for prosjektkostnader og omsetning, prosjektkategoriene og kategorigruppene.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="5b8a6-134">Du kan konfigurere kategorigrupper ved å gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Kategorier** \> **Kategorigrupper**.</span><span class="sxs-lookup"><span data-stu-id="5b8a6-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
