---
title: Periodetyper
description: Dette emnet gir informasjon om hvordan du konfigurerer periodetyper for inntektsestimat.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531509"
---
# <a name="period-types"></a><span data-ttu-id="7122e-103">Periodetyper</span><span class="sxs-lookup"><span data-stu-id="7122e-103">Period types</span></span>

<span data-ttu-id="7122e-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="7122e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7122e-105">En periodetype definerer hvor ofte inntekten på et prosjekt estimeres.</span><span class="sxs-lookup"><span data-stu-id="7122e-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="7122e-106">Dette emnet gir informasjon om hvordan du konfigurerer periodetyper for inntektsestimat.</span><span class="sxs-lookup"><span data-stu-id="7122e-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="7122e-107">Opprette og arbeide med periodetyper</span><span class="sxs-lookup"><span data-stu-id="7122e-107">Create and work with period types</span></span>
<span data-ttu-id="7122e-108">Fullfør fremgangsmåten nedenfor for å opprette og arbeide med periodetyper:</span><span class="sxs-lookup"><span data-stu-id="7122e-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="7122e-109">I Dynamics 365 Finance-miljøet går du til Gå til **Prosjektstyring og regnskap** > **Oppsett** > **Estimater** > **Periodetyper**.</span><span class="sxs-lookup"><span data-stu-id="7122e-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="7122e-110">Hvis du vil opprette en ny periodetype, velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7122e-110">Select **New** to create new period type.</span></span> <span data-ttu-id="7122e-111">Angi et navn og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7122e-111">Enter a name and description.</span></span>
3. <span data-ttu-id="7122e-112">Angi en verdi i feltet **Hyppighet**:</span><span class="sxs-lookup"><span data-stu-id="7122e-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="7122e-113">Hvis du velger **Uke**, **Annenhver uke**, **Halvmånedlig**, **Måned**, **Dag**, **Kvartal** eller **År**, brukes kalenderen til å generere periodene.</span><span class="sxs-lookup"><span data-stu-id="7122e-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="7122e-114">Hvis du velger **Finansperiode**, brukes finansperioder fra Økonomimodul-konfigurasjonen til å generere perioder.</span><span class="sxs-lookup"><span data-stu-id="7122e-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="7122e-115">Hvis du velger **Ubegrenset**, kan du angi egendefinerte perioder.</span><span class="sxs-lookup"><span data-stu-id="7122e-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="7122e-116">Velg oppføring for periodetype, og velg deretter **Generer perioder** for å opprette perioder for periodetypen.</span><span class="sxs-lookup"><span data-stu-id="7122e-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="7122e-117">Avhengig av periodefrekvensen du valgte, kan det hende at du har mulighet til å spesifisere en startdato eller antall perioder som skal genereres.</span><span class="sxs-lookup"><span data-stu-id="7122e-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="7122e-118">Velg **Perioder** for å gjennomgå genererte perioder.</span><span class="sxs-lookup"><span data-stu-id="7122e-118">Select **Periods** to review generated periods.</span></span>

