---
title: Oppdatere et prosjekt
description: Dette emnet gir informasjon om oppdatering av prosjekter i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131445"
---
# <a name="update-a-project"></a><span data-ttu-id="c75cd-103">Oppdatere et prosjekt</span><span class="sxs-lookup"><span data-stu-id="c75cd-103">Update a project</span></span>

<span data-ttu-id="c75cd-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="c75cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c75cd-105">Nedenfor vises et sammendrag av feltene som kan oppdateres i et prosjekt etter at det er opprettet, og eventuelle gjeldende implikasjoner av oppdateringene.</span><span class="sxs-lookup"><span data-stu-id="c75cd-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="c75cd-106">Felt for prosjektdetaljer</span><span class="sxs-lookup"><span data-stu-id="c75cd-106">Project detail fields</span></span>

- <span data-ttu-id="c75cd-107">**Navn**: Tittelen på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c75cd-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="c75cd-108">**Beskrivelse**: En oversikt over prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c75cd-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="c75cd-109">**Kunde**: Firmaet som prosjektet skal leveres til.</span><span class="sxs-lookup"><span data-stu-id="c75cd-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="c75cd-110">**Kalendermal**: Arbeidstiden til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c75cd-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="c75cd-111">Når feltet endres, beregnes hele tidsplanen på nytt.</span><span class="sxs-lookup"><span data-stu-id="c75cd-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="c75cd-112">**Valuta**: Valutaen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c75cd-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="c75cd-113">Standardverdien i dette feltet er basert på valutaen som er definert i kontraktenheten.</span><span class="sxs-lookup"><span data-stu-id="c75cd-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="c75cd-114">Når kontraktenheten oppdateres, oppdateres også feltet.</span><span class="sxs-lookup"><span data-stu-id="c75cd-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="c75cd-115">**Kontraktenhet**: Organisasjonsenheten som representerer firmagruppen eller divisjonen som er primært ansvarlig for å vinne salget og administrere levering av arbeid og tjenester til kunden.</span><span class="sxs-lookup"><span data-stu-id="c75cd-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="c75cd-116">**Prosjektleder**: Prosjektteammedlemmet som har autoriteten til å se gjennom og godkjenne tidsoppføringer og utgifter.</span><span class="sxs-lookup"><span data-stu-id="c75cd-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="c75cd-117">Estimatfelt</span><span class="sxs-lookup"><span data-stu-id="c75cd-117">Estimate fields</span></span>

- <span data-ttu-id="c75cd-118">**Estimer startdato**: Datoen når prosjektet skal starte.</span><span class="sxs-lookup"><span data-stu-id="c75cd-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="c75cd-119">Når dette feltet oppdateres, flyttes eventuelle oppgaver i prosjektet proporsjonalt med den nye startdatoen.</span><span class="sxs-lookup"><span data-stu-id="c75cd-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="c75cd-120">**Sluttdato**: Datoen prosjektet er planlagt å avsluttes.</span><span class="sxs-lookup"><span data-stu-id="c75cd-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="c75cd-121">**Innsats**: Den beregnede arbeidsinnsatsen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c75cd-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="c75cd-122">Når det legges til oppgaver i prosjektet, kan ikke dette feltet lenger redigeres.</span><span class="sxs-lookup"><span data-stu-id="c75cd-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="c75cd-123">**Estimert arbeidskostnad**: Den estimerte arbeidskostnaden for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c75cd-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="c75cd-124">Når det legges til arbeidskostnader i prosjektet, kan ikke dette feltet lenger redigeres.</span><span class="sxs-lookup"><span data-stu-id="c75cd-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="c75cd-125">**Estimerte utgifter**: De estimerte utgiftene for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c75cd-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="c75cd-126">Når det legges til utgifter i prosjektet, kan ikke dette feltet lenger redigeres.</span><span class="sxs-lookup"><span data-stu-id="c75cd-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="c75cd-127">Felt for faktiske verdier for prosjekt</span><span class="sxs-lookup"><span data-stu-id="c75cd-127">Project actual fields</span></span>
- <span data-ttu-id="c75cd-128">**Faktisk start**: Datoen da prosjektet startet.</span><span class="sxs-lookup"><span data-stu-id="c75cd-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="c75cd-129">**Faktisk slutt**: Oppdateres når et prosjekt er fullført.</span><span class="sxs-lookup"><span data-stu-id="c75cd-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="c75cd-130">Felt for prosjektstatus</span><span class="sxs-lookup"><span data-stu-id="c75cd-130">Project status fields</span></span>

- <span data-ttu-id="c75cd-131">**Generell prosjektstatus**: Den generelle prosjekttilstanden oppgitt av prosjektlederen.</span><span class="sxs-lookup"><span data-stu-id="c75cd-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="c75cd-132">**Kommentarer**: Informasjon om gjeldende tilstand for prosjektet fra prosjektlederen.</span><span class="sxs-lookup"><span data-stu-id="c75cd-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

