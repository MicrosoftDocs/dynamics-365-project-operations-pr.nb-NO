---
title: Synkronisere ressurskapasitet
description: Dette emnet gir informasjon om hvordan du synkroniserer kapasiteten til en ressurs på tvers av kalendere og prosjekter.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081598"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="f7fb1-103">Synkronisere ressurskapasitet</span><span class="sxs-lookup"><span data-stu-id="f7fb1-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7fb1-104">Prosessene for hjelp for ressurssynkronisering garanterer at informasjon for kalenderen og basiskalenderen når frem til planleggingen av prosjektressurser.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="f7fb1-105">Hvis kalenderen endres, gjør prosessene de nødvendige oppdateringene for planleggingen av prosjektressurser.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="f7fb1-106">Prosessene bidrar også til å forbedre ytelsen fordi kalenderens ressursinformasjon er synkronisert på forhånd.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="f7fb1-107">Derfor skjer oppdatering av ressursplanleggingsinformasjonen raskere.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="f7fb1-108">Vi anbefaler at du planlegger prosessene som en bunke i stedet for én om gangen.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="f7fb1-109">Ellers er det en risiko for at noen vil glemme inklusivdatoene da informasjonen sist ble synkronisert.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="f7fb1-110">Hvis du ikke bruker noen datoer, kan det oppstå mellomrom under synkronisering av dato.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendersynkronisering](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="f7fb1-112">Synkroniser opprullering av ressurskapasitet</span><span class="sxs-lookup"><span data-stu-id="f7fb1-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="f7fb1-113">Synkroniseringsprosessen er utformet for å synkronisere all ressurskalenderinformasjon.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="f7fb1-114">Denne informasjonen inkluderer informasjon om basiskalenderen for eventuelle endringer i prosjektets tabellkapasitet for ressurskalender.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="f7fb1-115">Hvis det legges til nye ressurser i prosjektet, bidrar synkroniseringen til å garantere at den oppdaterte kalenderinformasjonen er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="f7fb1-116">Denne synkroniseringen kan gjøres når som helst.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="f7fb1-117">Vi anbefaler at du bruker en bunke.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-117">We recommend that you use a batch.</span></span> <span data-ttu-id="f7fb1-118">Alternativene er tilgjengelige under synkronisering av kapasitetsreservasjoner.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="f7fb1-119">Velg **Prosjektstyring og regnskap** &gt; **Periodisk** &gt; **Kapasitetssynkronisering** &gt; **Synkroniser opprullering av ressurskapasitet**.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="f7fb1-120">Angi alternativene i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="f7fb1-121">Alternativ</span><span class="sxs-lookup"><span data-stu-id="f7fb1-121">Option</span></span>      | <span data-ttu-id="f7fb1-122">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f7fb1-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="f7fb1-123">Periodekode</span><span class="sxs-lookup"><span data-stu-id="f7fb1-123">Period code</span></span> | <span data-ttu-id="f7fb1-124">Du kan også velge datointervallkoden for økonomimodulen for å angi start- og sluttdatoene for synkroniseringsprosessen for opprullering av ressurskapasitet.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="f7fb1-125">Startdato</span><span class="sxs-lookup"><span data-stu-id="f7fb1-125">Start date</span></span>  | <span data-ttu-id="f7fb1-126">Angi startdatoen for synkroniseringsprosessen for opprullering av ressurskapasitet.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="f7fb1-127">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="f7fb1-127">End date</span></span>    | <span data-ttu-id="f7fb1-128">Angi sluttdatoen for synkroniseringsprosessen for opprullering av ressurskapasitet.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="f7fb1-129">[![Synkroniseringsfremdrift](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="f7fb1-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
