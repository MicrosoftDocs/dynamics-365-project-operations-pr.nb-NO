---
title: Godkjenningssett
description: Dette emnet inneholder informasjon om godkjenningssett, forespørsler og delsettene for disse operasjonene.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116883"
---
# <a name="approval-sets"></a><span data-ttu-id="81d97-103">Godkjenningssett</span><span class="sxs-lookup"><span data-stu-id="81d97-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="81d97-104">Godkjenningssett grupperer godkjenningsforespørsler sammen i mindre delsett av operasjoner.</span><span class="sxs-lookup"><span data-stu-id="81d97-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="81d97-105">Denne grupperingen tillater at godkjenninger kan behandles i prosjektrekkefølge og tillater nytt forsøk og sekvensering.</span><span class="sxs-lookup"><span data-stu-id="81d97-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="81d97-106">Gruppering forbedrer påliteligheten og sporbarheten ved godkjenningsbehandling for store godkjenningsvolumer.</span><span class="sxs-lookup"><span data-stu-id="81d97-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="81d97-107">Godkjenningssett angir den totale behandlingstilstanden for de relaterte oppføringene.</span><span class="sxs-lookup"><span data-stu-id="81d97-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="81d97-108">Når en godkjenningsoppføring behandles ved hjelp av et godkjenningssett, flyttes oppføringen fra **Sendt** til **Godkjent**, og koblingen fra godkjenningssettet oppheves.</span><span class="sxs-lookup"><span data-stu-id="81d97-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="81d97-109">Hvis en oppføring mislykkes når den sendes til godkjenning, beholdes statusen **Sendt**, og godkjenningssettet merkes som mislykket.</span><span class="sxs-lookup"><span data-stu-id="81d97-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="81d97-110">Godkjenningssettet logger feilmeldingen om feilen.</span><span class="sxs-lookup"><span data-stu-id="81d97-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="81d97-111">Behandle godkjenninger og godkjenningssett</span><span class="sxs-lookup"><span data-stu-id="81d97-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="81d97-112">Godkjenninger som ligger i kø for behandling, vises i visningen **Godkjenninger under behandling**.</span><span class="sxs-lookup"><span data-stu-id="81d97-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="81d97-113">Systemet prøver å behandle alle oppføringene flere ganger asynkront, inkludert å prøve en godkjenning på nytt hvis tidligere forsøk mislyktes.</span><span class="sxs-lookup"><span data-stu-id="81d97-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="81d97-114">Feltet for **godkjenningssett for levetid** registrerer antall forsøk som gjenstår for å behandle settet før det er merket som mislykket.</span><span class="sxs-lookup"><span data-stu-id="81d97-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="81d97-115">Mislykkede godkjenninger og godkjenningssett</span><span class="sxs-lookup"><span data-stu-id="81d97-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="81d97-116">Visningen **Mislykkede godkjenninger** viser alle godkjenninger som krever brukerinngripen.</span><span class="sxs-lookup"><span data-stu-id="81d97-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="81d97-117">Åpne de tilknyttede godkjenningssettloggene for å identifisere årsaken til feilen.</span><span class="sxs-lookup"><span data-stu-id="81d97-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="81d97-118">Når du velger **Prøv på nytt**, legges levetidsantallet til, og godkjenningssettet flyttes tilbake til statusen **Behandling** og prøver å behandle de gjenstående oppføringene.</span><span class="sxs-lookup"><span data-stu-id="81d97-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="81d97-119">Konfigurere godkjenningssett</span><span class="sxs-lookup"><span data-stu-id="81d97-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="81d97-120">Aktiver funksjonen Godkjenningssett</span><span class="sxs-lookup"><span data-stu-id="81d97-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="81d97-121">Før du aktiverer funksjonen Godkjenningssett, kontrollerer du at det ikke er noen godkjenninger som blir behandlet.</span><span class="sxs-lookup"><span data-stu-id="81d97-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="81d97-122">Gå til siden **Prosjektparametere**, og velg **Funksjonskontroll** > **Aktiver moderne godkjenninger**.</span><span class="sxs-lookup"><span data-stu-id="81d97-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="81d97-123">Deaktiver funksjonen Godkjenningssett</span><span class="sxs-lookup"><span data-stu-id="81d97-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="81d97-124">Før du deaktiverer funksjonen Godkjenningssett, kontrollerer du at det ikke er noen godkjenninger som blir behandlet.</span><span class="sxs-lookup"><span data-stu-id="81d97-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="81d97-125">Gå til siden **Prosjektparametere**, og velg **Funksjonskontroll** > **Deaktiver moderne godkjenninger**.</span><span class="sxs-lookup"><span data-stu-id="81d97-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="81d97-126">Konfigurere den asynkrone terskelen</span><span class="sxs-lookup"><span data-stu-id="81d97-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="81d97-127">Når det opprettes godkjenningssett, flyttes behandlingen til bakgrunnen når det valgte antallet oppføringer til godkjenning overskrider det angitte terskelen.</span><span class="sxs-lookup"><span data-stu-id="81d97-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="81d97-128">Bruk feltet **Asynkron terskel** for å konfigurere når godkjenningsbehandling skal kjøres synkront eller asynkront.</span><span class="sxs-lookup"><span data-stu-id="81d97-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="81d97-129">Gyldige verdier er:</span><span class="sxs-lookup"><span data-stu-id="81d97-129">Valid values are:</span></span>

  - <span data-ttu-id="81d97-130">Null: Alle forespørsler må behandles asynkront.</span><span class="sxs-lookup"><span data-stu-id="81d97-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="81d97-131">Tall som er større enn null: Godkjenninger behandles asynkront bare når det sendte antallet godkjenninger overskrider denne verdien.</span><span class="sxs-lookup"><span data-stu-id="81d97-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
