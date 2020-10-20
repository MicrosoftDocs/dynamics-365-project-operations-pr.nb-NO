---
title: Oversikt over godkjenninger
description: Dette emnet gir information om å arbeide med godkjenninger i Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961178"
---
# <a name="approvals-overview"></a><span data-ttu-id="6dad2-103">Oversikt over godkjenninger</span><span class="sxs-lookup"><span data-stu-id="6dad2-103">Approvals overview</span></span>

<span data-ttu-id="6dad2-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="6dad2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6dad2-105">Tids- og utgiftsoppføringer går gjennom en godkjenningsarbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="6dad2-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="6dad2-106">Når oppføringene er godkjent, registreres transaksjoner i faktisk verdier, eller tiden bestilles i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="6dad2-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="6dad2-107">Godkjenningsarbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="6dad2-107">Approvals workflow</span></span>
<span data-ttu-id="6dad2-108">Når du oppretter og sender en tids- eller utgiftsoppføring, opprettes det en godkjenningsoppføring.</span><span class="sxs-lookup"><span data-stu-id="6dad2-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="6dad2-109">Prosjektgodkjenneren eller lederen din ser gjennom og godkjenner oppføringen.</span><span class="sxs-lookup"><span data-stu-id="6dad2-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="6dad2-110">Hvis oppføringen er relatert til et prosjekt blir de faktiske verdiene opprettet når den er godkjent.</span><span class="sxs-lookup"><span data-stu-id="6dad2-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="6dad2-111">På denne måten kan kostnad og fakturering spores.</span><span class="sxs-lookup"><span data-stu-id="6dad2-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="6dad2-112">Godkjenne en oppføring</span><span class="sxs-lookup"><span data-stu-id="6dad2-112">Approve an entry</span></span>
<span data-ttu-id="6dad2-113">På skjemaet **Godkjenninger** kan du bytte mellom forskjellige visninger, slik at du kan vise de forskjellige godkjenningstypene.</span><span class="sxs-lookup"><span data-stu-id="6dad2-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="6dad2-114">Gå til **Godkjenninger**-skjemaet, og velg **Utgifter**, **Tid** eller **Tilbakekallinger**.</span><span class="sxs-lookup"><span data-stu-id="6dad2-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="6dad2-115">Gå gjennom hver godkjenning, og velg de du vil godkjenne.</span><span class="sxs-lookup"><span data-stu-id="6dad2-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="6dad2-116">Velg **Godkjenn** for å godkjenne de valgte oppføringene.</span><span class="sxs-lookup"><span data-stu-id="6dad2-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="6dad2-117">Systemet behandler disse oppføringene og oppretter faktiske verdier eller en bestilling.</span><span class="sxs-lookup"><span data-stu-id="6dad2-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="6dad2-118">Avvise en oppføring</span><span class="sxs-lookup"><span data-stu-id="6dad2-118">Reject an entry</span></span>
<span data-ttu-id="6dad2-119">Som prosjektgodkjenner kan det hende du må sende en oppføring tilbake til en bruker for korrigering.</span><span class="sxs-lookup"><span data-stu-id="6dad2-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="6dad2-120">Gå til **Godkjenninger**-skjemaet, og velg oppføringen du vil avvise.</span><span class="sxs-lookup"><span data-stu-id="6dad2-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="6dad2-121">Velg **Avvis**.</span><span class="sxs-lookup"><span data-stu-id="6dad2-121">Select **Reject**.</span></span>
3. <span data-ttu-id="6dad2-122">Valgfritt – Legg til en kommentar i dialogboksen **Avvisningskommentarer** for å informere brukeren hvorfor oppføringen blir avvist.</span><span class="sxs-lookup"><span data-stu-id="6dad2-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="6dad2-123">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dad2-123">Select **OK**.</span></span> <span data-ttu-id="6dad2-124">Oppføringen returneres til brukeren.</span><span class="sxs-lookup"><span data-stu-id="6dad2-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="6dad2-125">Tilbakekall oppføringer</span><span class="sxs-lookup"><span data-stu-id="6dad2-125">Recall entries</span></span>
<span data-ttu-id="6dad2-126">Det kan hende du må kalle tilbake en oppføring som er sendt.</span><span class="sxs-lookup"><span data-stu-id="6dad2-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="6dad2-127">Hvis oppføringen ikke er godkjent, returneres den umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="6dad2-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="6dad2-128">En godkjent oppføring har imidlertid kanskje en materialinnvirkning.</span><span class="sxs-lookup"><span data-stu-id="6dad2-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="6dad2-129">Prosjektgodkjenneren må godkjenne tilbakekallingen for å kunne reversere transaksjonen i faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="6dad2-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="6dad2-130">Angi prosjektgodkjennere</span><span class="sxs-lookup"><span data-stu-id="6dad2-130">Specify Project approvers</span></span>
<span data-ttu-id="6dad2-131">Hvert prosjekt har flere prosjektteammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="6dad2-131">Each project has a number of project team members.</span></span> <span data-ttu-id="6dad2-132">Du kan angi hvilke teammedlemmer som også er prosjektgodkjennere.</span><span class="sxs-lookup"><span data-stu-id="6dad2-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="6dad2-133">Gå til **Prosjekter**-skjemaet, og åpne prosjektet fra listen.</span><span class="sxs-lookup"><span data-stu-id="6dad2-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="6dad2-134">På **Team**-fanen velger du teammedlemmet som skal være en prosjektgodkjenner, og deretter velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="6dad2-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="6dad2-135">Sett feltet **Prosjektgodkjenner** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6dad2-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="6dad2-136">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6dad2-136">Select **Save**.</span></span>
5. <span data-ttu-id="6dad2-137">Gjenta trinn 2 til 4 hvis du vil legge til flere prosjektgodkjennere.</span><span class="sxs-lookup"><span data-stu-id="6dad2-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="6dad2-138">Konfigurere brukerens overordnede</span><span class="sxs-lookup"><span data-stu-id="6dad2-138">Configure the user's manager</span></span>

1. <span data-ttu-id="6dad2-139">Gå til **Innstillinger** > **Sikkerhet** > **Brukere**.</span><span class="sxs-lookup"><span data-stu-id="6dad2-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="6dad2-140">Velg brukeren som du tilordner en overordnet til, og velg lederen fra listen i området **Organisasjonsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="6dad2-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="6dad2-141">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6dad2-141">Select **Save**.</span></span>


