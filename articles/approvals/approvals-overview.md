---
title: Oversikt over godkjenninger
description: Dette emnet gir information om å arbeide med godkjenninger i Project Operations.
author: stsporen
manager: Annbe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b2da22e10cf6c40a2c84bcd32437b2830f830d07
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852511"
---
# <a name="approvals-overview"></a><span data-ttu-id="82c11-103">Oversikt over godkjenninger</span><span class="sxs-lookup"><span data-stu-id="82c11-103">Approvals overview</span></span>

<span data-ttu-id="82c11-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="82c11-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="82c11-105">Innsendinger av tids-, utgifts- og materialbruk flyttes gjennom en arbeidsflyt for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="82c11-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="82c11-106">Når oppføringene er godkjent, registreres transaksjoner i faktisk verdier, eller tiden bestilles i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="82c11-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="82c11-107">Godkjenningsarbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="82c11-107">Approvals workflow</span></span>
<span data-ttu-id="82c11-108">Når du oppretter og sender en oppføring for tids-, utgifts- eller materialbruk, opprettes det en godkjenningsoppføring.</span><span class="sxs-lookup"><span data-stu-id="82c11-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="82c11-109">Prosjektgodkjenneren eller -lederen ser gjennom og godkjenner oppføringen.</span><span class="sxs-lookup"><span data-stu-id="82c11-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="82c11-110">Hvis oppføringen er relatert til et prosjekt, opprettes de faktiske dataene når den er godkjent.</span><span class="sxs-lookup"><span data-stu-id="82c11-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="82c11-111">På denne måten kan kostnad og fakturering spores.</span><span class="sxs-lookup"><span data-stu-id="82c11-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="82c11-112">Godkjenne en oppføring</span><span class="sxs-lookup"><span data-stu-id="82c11-112">Approve an entry</span></span>
<span data-ttu-id="82c11-113">**Godkjenninger**-siden gjør det mulig å veksle mellom ulike visninger, slik at du kan vise de ulike godkjenningstypene.</span><span class="sxs-lookup"><span data-stu-id="82c11-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="82c11-114">Gå til **Godkjenninger**-siden, og velg **Utgifter**, **Tid**, **Materialbruk** eller **Tilbakekallinger**.</span><span class="sxs-lookup"><span data-stu-id="82c11-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="82c11-115">Gå gjennom hver godkjenning, og velg de du vil godkjenne.</span><span class="sxs-lookup"><span data-stu-id="82c11-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="82c11-116">Velg **Godkjenn** for å godkjenne de valgte oppføringene.</span><span class="sxs-lookup"><span data-stu-id="82c11-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="82c11-117">Systemet behandler disse oppføringene og oppretter faktiske data.</span><span class="sxs-lookup"><span data-stu-id="82c11-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="82c11-118">Avvise en oppføring</span><span class="sxs-lookup"><span data-stu-id="82c11-118">Reject an entry</span></span>
<span data-ttu-id="82c11-119">Som prosjektgodkjenner kan det hende du må sende en oppføring tilbake til en bruker for korrigering.</span><span class="sxs-lookup"><span data-stu-id="82c11-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="82c11-120">Gå til **Godkjenninger**-siden, og velg oppføringen som skal avvises.</span><span class="sxs-lookup"><span data-stu-id="82c11-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="82c11-121">Velg **Avvis**.</span><span class="sxs-lookup"><span data-stu-id="82c11-121">Select **Reject**.</span></span>
3. <span data-ttu-id="82c11-122">Du kan eventuelt legge til en kommentar i dialogboksen **Avvisningskommentarer** for å informere brukeren om hvorfor oppføringen blir avvist.</span><span class="sxs-lookup"><span data-stu-id="82c11-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="82c11-123">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="82c11-123">Select **OK**.</span></span> <span data-ttu-id="82c11-124">Oppføringen returneres til brukeren.</span><span class="sxs-lookup"><span data-stu-id="82c11-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="82c11-125">Avbryt godkjenning</span><span class="sxs-lookup"><span data-stu-id="82c11-125">Cancel approval</span></span>
<span data-ttu-id="82c11-126">I noen tilfeller kan det hende du må annullere en tidligere godkjent oppføring.</span><span class="sxs-lookup"><span data-stu-id="82c11-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="82c11-127">Annullering av en tidligere godkjent oppføring vil ha økonomisk innvirkning.</span><span class="sxs-lookup"><span data-stu-id="82c11-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="82c11-128">Godkjenning av tilbakekallingsforespørsler</span><span class="sxs-lookup"><span data-stu-id="82c11-128">Approving recall requests</span></span>
<span data-ttu-id="82c11-129">I noen tilfeller kan det hende at en konsulent må tilbakekalle en tidligere godkjent oppføring.</span><span class="sxs-lookup"><span data-stu-id="82c11-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="82c11-130">Annullering av en tidligere godkjent oppføring vil ha økonomisk innvirkning.</span><span class="sxs-lookup"><span data-stu-id="82c11-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="82c11-131">Prosjektgodkjenneren må godkjenne tilbakekallingen for å kunne reversere transaksjonen i Faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="82c11-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="82c11-132">Angi prosjektgodkjennere</span><span class="sxs-lookup"><span data-stu-id="82c11-132">Specify Project approvers</span></span>
<span data-ttu-id="82c11-133">Hvert prosjekt har flere prosjektteammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="82c11-133">Each project has a number of project team members.</span></span> <span data-ttu-id="82c11-134">Du kan angi hvilke teammedlemmer som også er prosjektgodkjennere.</span><span class="sxs-lookup"><span data-stu-id="82c11-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="82c11-135">Gå til **Prosjekter**-siden, og åpne prosjektet fra listen.</span><span class="sxs-lookup"><span data-stu-id="82c11-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="82c11-136">På **Team**-fanen velger du teammedlemmet som skal være en prosjektgodkjenner, og deretter velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="82c11-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="82c11-137">Sett feltet **Prosjektgodkjenner** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="82c11-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="82c11-138">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="82c11-138">Select **Save**.</span></span>
5. <span data-ttu-id="82c11-139">Gjenta trinn 2 til 4 hvis du vil legge til flere prosjektgodkjennere.</span><span class="sxs-lookup"><span data-stu-id="82c11-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="82c11-140">Konfigurere brukerens overordnede</span><span class="sxs-lookup"><span data-stu-id="82c11-140">Configure the user's manager</span></span>

1. <span data-ttu-id="82c11-141">Gå til **Innstillinger** > **Sikkerhet** > **Brukere**.</span><span class="sxs-lookup"><span data-stu-id="82c11-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="82c11-142">Velg brukeren som du tilordner en overordnet til, og velg lederen fra listen i området **Organisasjonsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="82c11-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="82c11-143">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="82c11-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
