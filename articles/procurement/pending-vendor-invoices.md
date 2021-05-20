---
title: Kjøpe ikke lagerførte materialer ved hjelp av en ventende leverandørfaktura
description: Dette emnet forklarer hvordan du registrerer ventende leverandørfakturaer.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880670"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="a0c68-103">Kjøpe ikke lagerførte materialer ved hjelp av en ventende leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="a0c68-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="a0c68-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="a0c68-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a0c68-105">Når et selskap anskaffer ikke-lagerført materiell for et prosjekt, kan kostnadene umiddelbart registreres mot prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a0c68-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="a0c68-106">For eksempel utfører Contoso Robotics US et prosjekt for fornyelse av utstyr og trenger programvarelisenser.</span><span class="sxs-lookup"><span data-stu-id="a0c68-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="a0c68-107">Disse lisensene anskaffes fra en tredjepartsleverandør.</span><span class="sxs-lookup"><span data-stu-id="a0c68-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="a0c68-108">Når du bruker Dynamics 365 Finance, registrerer assistenten for leverandørgjeld et ventende leverandørfakturadokument og attributterer lisenskostnadene direkte mot prosjektet for fornyelse av utstyr.</span><span class="sxs-lookup"><span data-stu-id="a0c68-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="a0c68-109">Før du bruker funksjonaliteten som er beskrevet i dette emnet, må du se gjennom og bruke de nødvendige konfigurasjonene.</span><span class="sxs-lookup"><span data-stu-id="a0c68-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="a0c68-110">Hvis du vil ha mer informasjon, kan du se [Aktivere ikke-lagerførte materialer og ventende leverandørfakturaer](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="a0c68-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="a0c68-111">Poster en prosjektrelatert ventende leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="a0c68-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="a0c68-112">Ventende leverandørfakturaer kan registreres på siden **Ventende leverandørfakturaer** (**Leverandørgjeld** > **Fakturaer** > **Ventende leverandørfakturaer**).</span><span class="sxs-lookup"><span data-stu-id="a0c68-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="a0c68-113">Fullfør følgende trinn for å postere en prosjektrelatert ventende leverandørfaktura:</span><span class="sxs-lookup"><span data-stu-id="a0c68-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="a0c68-114">Gå til **Leverandørgjeld** > **Fakturaer** og velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a0c68-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="a0c68-115">I **Fakturakonto**-feltet velger du en leverandør i **Nummer**-feltet og angir leverandørfaktura-IDen.</span><span class="sxs-lookup"><span data-stu-id="a0c68-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="a0c68-116">Legg til en linje i leverandørfakturaen, og velg varen som ikke er på lager fra leverandøren i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a0c68-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="a0c68-117">Leverandørfakturalinjer som er basert på en innkjøpskategori, kan ikke registreres mot prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a0c68-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="a0c68-118">Legg til innkjøpmengden.</span><span class="sxs-lookup"><span data-stu-id="a0c68-118">Add the quantity purchased.</span></span> <span data-ttu-id="a0c68-119">Enhetsprisen fylles ut i systemet basert på konfigurasjonen av varepris som ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="a0c68-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="a0c68-120">Kontroller totalbeløpet og andre nødvendige detaljer på linjen.</span><span class="sxs-lookup"><span data-stu-id="a0c68-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="a0c68-121">Velg IDen for prosjektet som varen skal registreres til, i kategorien **Prosjekt** i linjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="a0c68-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="a0c68-122">Du kan eventuelt velge aktivitetsnummeret og oppdatere prosjektkategorien og linjeegenskapen.</span><span class="sxs-lookup"><span data-stu-id="a0c68-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="a0c68-123">Poster ventende leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="a0c68-123">Post pending vendor invoice.</span></span> <span data-ttu-id="a0c68-124">Når fakturaen posteres, registrerer systemet følgende:</span><span class="sxs-lookup"><span data-stu-id="a0c68-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="a0c68-125">Leverandørsaldobeløpet.</span><span class="sxs-lookup"><span data-stu-id="a0c68-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="a0c68-126">Salgsavgiftsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="a0c68-126">The sales tax amount.</span></span>
    - <span data-ttu-id="a0c68-127">Kostnadene mot prosjektet registreres på integrasjonskontoen for innkjøp.</span><span class="sxs-lookup"><span data-stu-id="a0c68-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="a0c68-128">Den faktiske transaksjonen for prosjekt i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a0c68-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="a0c68-129">Denne transaksjonen behandles videre ved hjelp av [journalen for Project Operations-integrering](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="a0c68-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="a0c68-130">Når du legger inn denne journalen, flyttes beløpet fra integrasjonskontoen for innkjøp til prosjektkostnadskontoen.</span><span class="sxs-lookup"><span data-stu-id="a0c68-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
