---
title: Hvorfor settes pris som standard til null i faktiske tidskostnader?
description: Feilsøke hvorfor en pris settes som standard til 0 i faktiske tidskostnader.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146270"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="ac0cc-103">Hvorfor settes pris som standard til null i faktiske tidskostnader?</span><span class="sxs-lookup"><span data-stu-id="ac0cc-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ac0cc-104">Disse vanlige spørsmålene gjelder for faktiske verdier der transaksjonsklassen er satt til Tid og transaksjonstypen er Kostnad.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="ac0cc-105">Følgende tre kontroller hjelper deg med å feilsøke hvorfor prisen settes som standard til 0 i faktiske tidskostnader.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="ac0cc-106">Kontroll 1: Identifiser kostnadsprislisten for prosjektet</span><span class="sxs-lookup"><span data-stu-id="ac0cc-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="ac0cc-107">Finn prosjektet fra prosjektfeltet for de faktiske verdiene og gå deretter til prosjektsiden.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="ac0cc-108">Klikk på koblingen for kontraktsenhet i feltet.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="ac0cc-109">På siden Kontraktsenhet kan du se om kontraktsenheten har en prisliste i rutenettet Kostprislister.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="ac0cc-110">Hvis det er mer enn én prisliste, har du fastslått problemet.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="ac0cc-111">Project Service støtter bare én prisliste per organisasjonsenhet.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="ac0cc-112">Fjern alle prislister fra denne enheten til det er bare én prisliste vedlagt i rutenettet Kostprislister for organisasjonsenheten.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="ac0cc-113">Hvis det ikke er noen prislister tilknyttet organisasjonsenheten, noter valutaen for organisasjonsenheten.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="ac0cc-114">Gå til Project Service og deretter Parametere, og åpne kategorien Prislister. Kontroller om det finnes prislister med kontekst satt til Kostnad og valuta som samsvarer med organisasjonsenhetens valuta.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="ac0cc-115">Hvis det ikke finnes prislister som samsvarer med kriteriene, har du fastslått problemet.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="ac0cc-116">Kontroller at du har minst én prisliste der konteksten er satt til Kostnad og der valutaen samsvarer med organisasjonsenhetens valuta.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="ac0cc-117">Hvis det er mer enn én prisliste som samsvarer med kriteriene, fortsetter du å lese dette dokumentet for å gjøre flere kontroller.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="ac0cc-118">Kontroll 2: Er noen av prislistene som er identifisert ovenfor, gyldige for den bestemte datoen til de faktiske tidskostnadene?</span><span class="sxs-lookup"><span data-stu-id="ac0cc-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="ac0cc-119">For at Project Service skal vurdere en prisliste for standardpris, må denne prislisten være gjeldende for datoen på de faktiske tidskostnadene.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="ac0cc-120">Kontroller følgende for å se om prislisten(e) identifisert ovenfor er gjeldende:</span><span class="sxs-lookup"><span data-stu-id="ac0cc-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="ac0cc-121">Kontroller om start- og sluttdatoer i kategorien Generelt for prislistene som er tilknyttet, ikke er tomme.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="ac0cc-122">Hvis start- og sluttdatoene i prislistene identifisert ovenfor er tomme, vil du ha fastslått problemet.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="ac0cc-123">Noter startdatofeltet for de faktiske tidskostnadene og kontroller om noen av prislistene som er identifisert, er gjeldende for denne datoen.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="ac0cc-124">For eksempel bør datoen for faktiske tidskostnader være innenfor startdatoen og sluttdatoen i prislisten.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="ac0cc-125">Hvis det ikke er en prisliste som omfatter denne datoen i de faktiske tidskostnadene, har du fastslått problemet.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="ac0cc-126">Endre start- og sluttdatoer for prislisten for å sikre at prislisten dekker datoen for faktiske tidskostnader.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="ac0cc-127">Hvis det er mer enn én prisliste som omfatter datoen i de faktiske tidskostnadene, har du fastslått problemet.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="ac0cc-128">Du kan løse dette ved å redigere start- og sluttdatoene i prislisten(e) slik at det bare er én prisliste som omfatter datoen for de faktiske tidskostnadene.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="ac0cc-129">Hvis det er bare én prisliste som omfatter datoen for de faktiske tidskostnadene, kan du gå til neste kontroll i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="ac0cc-130">Når du har gjort de nødvendige korrigeringene, oppretter du en tidsoppføring på nytt, godkjenner den, og kontrollerer at de faktiske tidskostnadene viser en gyldig pris.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="ac0cc-131">Kontroll 3: Finnes det en pris i prislisten for prisdimensjonene i de faktiske tidskostnadene?</span><span class="sxs-lookup"><span data-stu-id="ac0cc-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="ac0cc-132">Hvis du har fullført kontroll 1 og 2, skal du nå ha bare én prisliste som gjelder for datoen for de faktiske tidskostnadene.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="ac0cc-133">Åpne prislisten og gå til kategorien Rollepriser. Kontroller at det er en rad i rutenettet for prisdimensjonene i de faktiske tidskostnadene.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="ac0cc-134">Hvis det ikke er noen rad i rutenettet Rollepriser for prisdimensjonene i de faktiske tidskostnadene, har du fastslått problemet.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="ac0cc-135">Opprett en rad i rutenettet Rollepriser for prisdimensjonene i de faktiske tidskostnadene.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="ac0cc-136">Når du har gjort dette, oppretter du en tidsoppføring på nytt, godkjenner den, og kontrollerer at de faktiske tidskostnadene viser en gyldig pris.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="ac0cc-137">Hvis du fremdeles ikke ser en gyldig pris i de faktiske tidskostnadene når du har gjort de tre kontrollene ovenfor, logger du en støtteforespørsel.</span><span class="sxs-lookup"><span data-stu-id="ac0cc-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



