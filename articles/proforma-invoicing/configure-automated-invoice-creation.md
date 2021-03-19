---
title: Konfigurere automatisk fakturaoppretting
description: Dette emnet gir informasjon om hvordan du konfigurerer systemet til å generere fakturaer automatisk.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0dddd963e79f8ecd91a96a6e684ab79e1b95bd6d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287925"
---
# <a name="configure-automatic-invoice-creation"></a><span data-ttu-id="82d70-103">Konfigurere automatisk fakturaoppretting</span><span class="sxs-lookup"><span data-stu-id="82d70-103">Configure automatic invoice creation</span></span>

<span data-ttu-id="82d70-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="82d70-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="82d70-105">Fullfør fremgangsmåten nedenfor for å konfigurere en automatisk fakturakjøring i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="82d70-105">Complete the following steps to configure an automated invoice run in Dynamics 365 Project operations.</span></span>

1. <span data-ttu-id="82d70-106">Gå til **Innstillinger** > **Satvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="82d70-106">Go to **Settings** > **Batch jobs**.</span></span>
2. <span data-ttu-id="82d70-107">Opprett en satsvis jobb, og gi den navnet **Opprett fakturaer i Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="82d70-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="82d70-108">Navnet på den satsvise jobben må inneholde ordene "opprett fakturaer".</span><span class="sxs-lookup"><span data-stu-id="82d70-108">The name of the batch job must include the words "create invoices."</span></span>
3. <span data-ttu-id="82d70-109">I **Jobbtype**-feltet velger du **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="82d70-109">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="82d70-110">Som standard er **Daglig intervall** og **Er aktiv** satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="82d70-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="82d70-111">Velg **Kjør arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="82d70-111">Select **Run Workflow**.</span></span> <span data-ttu-id="82d70-112">I dialogboksen **Oppslagsoppføring** vises tre arbeidsflyter:</span><span class="sxs-lookup"><span data-stu-id="82d70-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="82d70-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="82d70-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="82d70-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="82d70-114">ProcessRunner</span></span>
    - <span data-ttu-id="82d70-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="82d70-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="82d70-116">Velg **ProcessRunCaller**, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="82d70-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="82d70-117">Velg **OK** i den neste dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="82d70-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="82d70-118">Arbeidsflyten **Hvile** følges av arbeidsflyten **Prosess**.</span><span class="sxs-lookup"><span data-stu-id="82d70-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

  > [!NOTE]
  > <span data-ttu-id="82d70-119">Du kan også velge **ProcessRunner** i trinn 5.</span><span class="sxs-lookup"><span data-stu-id="82d70-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="82d70-120">Når du deretter velger **OK**, etterfølges en **Prosess**-arbeidsflyt av en **Hvile**-arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="82d70-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="82d70-121">Arbeidsflytene **ProcessRunCaller** og **ProcessRunner** oppretter fakturaer.</span><span class="sxs-lookup"><span data-stu-id="82d70-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="82d70-122">**ProcessRunCaller** kaller **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="82d70-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="82d70-123">**ProcessRunner** er arbeids flyten som faktisk oppretter fakturaene.</span><span class="sxs-lookup"><span data-stu-id="82d70-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="82d70-124">Det går gjennom alle kontraktslinjene som fakturaer må opprettes for, og det opprettes fakturaer for disse linjene.</span><span class="sxs-lookup"><span data-stu-id="82d70-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="82d70-125">For å finne ut hvilke kontraktslinjer fakturaer må opprettes for, ser jobben på fakturakjøredatoer for kontraktslinjene.</span><span class="sxs-lookup"><span data-stu-id="82d70-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="82d70-126">Hvis kontraktslinjer som tilhører én kontrakt, har samme fakturakjøringsdato, kombineres transaksjonene til én faktura som har to fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="82d70-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="82d70-127">Hvis det ikke finnes transaksjoner for å opprette fakturaer for, hopper jobben over fakturaopprettelsen.</span><span class="sxs-lookup"><span data-stu-id="82d70-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="82d70-128">Når **ProcessRunner** har kjørt ferdig, kaller den **ProcessRunCaller**, angir sluttidspunktet og lukkes.</span><span class="sxs-lookup"><span data-stu-id="82d70-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="82d70-129">**ProcessRunCaller** starter deretter en tidtaker som kjører i 24 timer, fra det angitte sluttidspunktet.</span><span class="sxs-lookup"><span data-stu-id="82d70-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="82d70-130">Når tidtakeren er ferdig, lukkes **ProcessRunCaller**.</span><span class="sxs-lookup"><span data-stu-id="82d70-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="82d70-131">Den satsvise prosessjobben for oppretting av fakturaer er en gjentakende jobb.</span><span class="sxs-lookup"><span data-stu-id="82d70-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="82d70-132">Hvis denne satsvise prosessen kjører mange ganger, opprettes flere forekomster av jobben, og det fører til feil.</span><span class="sxs-lookup"><span data-stu-id="82d70-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="82d70-133">Derfor bør du starte den satsvise prosessen bare én gang, og du bør bare starte den på nytt hvis den slutter å kjøre.</span><span class="sxs-lookup"><span data-stu-id="82d70-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="82d70-134">Satsvis fakturering kjører bare for prosjektkontraktlinjer som er konfigurert ved hjelp av fakturaplaner.</span><span class="sxs-lookup"><span data-stu-id="82d70-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="82d70-135">En kontraktlinje med en faktureringsmetode for fast pris må ha milepæler konfigurert.</span><span class="sxs-lookup"><span data-stu-id="82d70-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="82d70-136">Det må konfigureres en datobasert fakturaplan for en prosjektkontraktlinje med en faktureringsmetode for tid og materialer.</span><span class="sxs-lookup"><span data-stu-id="82d70-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="82d70-137">Det samme gjelder for en prosjektbasert kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="82d70-137">The same applies to a project-based contract line.</span></span>     


[!INCLUDE[footer-include](../includes/footer-banner.md)]