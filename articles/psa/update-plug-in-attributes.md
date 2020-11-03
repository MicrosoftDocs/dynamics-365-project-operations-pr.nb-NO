---
title: Oppdater plugin-attributter slik at de inkluderer nye prisdimensjoner
description: Dette emnet inneholder informasjon om hvordan du oppdaterer plugin-attributter for prisdimensjoner.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: dynamics-365-customerservice
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f215555dd7b29444e00499c0e731624e51057250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081703"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="c7341-103">Oppdater plugin-attributter slik at de inkluderer nye prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="c7341-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="c7341-104">Hvis du ikke bruker tilbuds- og kontraktfunksjonene i Project Service Automation, kan du hoppe over dette emnet.</span><span class="sxs-lookup"><span data-stu-id="c7341-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="c7341-105">Dette emnet forutsetter at du har fullført prosedyrene i emnene [Opprette egendefinerte felt og enheter](create-custom-fields-entities.md), [Legge til egendefinerte felt i prisoppsett og transaksjonsenheter](field-references.md) og [Konfigurere egendefinerte felt som prisdimensjoner](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="c7341-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="c7341-106">Hvis du ikke har utført disse prosedyrene, kan du gå tilbake og fullføre dem og deretter gå tilbake til dette emnet.</span><span class="sxs-lookup"><span data-stu-id="c7341-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="c7341-107">Når det blir opprettet en tilbudslinjedetalj på siden **Tilbudslinje** for en prosjekttilbudslinje, oppretter systemet to estimatlinjer i bakgrunnen – én linje for kostnadssiden for estimatet og én for salgsiden.</span><span class="sxs-lookup"><span data-stu-id="c7341-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="c7341-108">Dette er det samme for prosjektkontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="c7341-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="c7341-109">Når du gjør en endring i antallet eller et felt på kostnadssiden, overføres endringen til salgsiden.</span><span class="sxs-lookup"><span data-stu-id="c7341-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="c7341-110">Dette kan skyldes at følgende plugin-moduler må registreres på nytt etter at du har endret prisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="c7341-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="c7341-111">PreOperationContractLineDetailUpdate – oppdaterer **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="c7341-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="c7341-112">PreOperationQuoteLineDetailUpdate – oppdaterer **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="c7341-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="c7341-113">Fremgangsmåten nedenfor forklarer hvordan du registrerer plugin-modulene.</span><span class="sxs-lookup"><span data-stu-id="c7341-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="c7341-114">Åpne **PluginRegistrationTool** , koble til forekomsten på nettet.</span><span class="sxs-lookup"><span data-stu-id="c7341-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="c7341-115">Klikk **Søk** , og søk etter plugin-modulen som du vil oppdatere.</span><span class="sxs-lookup"><span data-stu-id="c7341-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Skjermbilde av søketreet](media/PRT-1.png)

3. <span data-ttu-id="c7341-117">Når plugin-modulen er funnet, velger du den, og deretter klikker du **Velg i hovedskjema**.</span><span class="sxs-lookup"><span data-stu-id="c7341-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="c7341-118">Velg trinnet i plugin-modulen som skal oppdateres, høyreklikk, og velg deretter **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="c7341-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Skjermbilde av plugin-modulen som skal oppdateres](media/PRT-2.png)
 
5. <span data-ttu-id="c7341-120">I oppdateringsvinduet klikker du på ellipsen ( **...** ) i filtreringsegenskapene.</span><span class="sxs-lookup"><span data-stu-id="c7341-120">In the update window, click the ellipsis ( **...** ) in the filtering attributes.</span></span>

 ![Skjermbilde av konfigurasjonsinformasjon for oppdatering av eksisterende trinn](media/PRT-3.png)
 
6. <span data-ttu-id="c7341-122">Velg avmerkingsboksen for prisattributt.</span><span class="sxs-lookup"><span data-stu-id="c7341-122">Select the pricing attribute check boxes.</span></span>

 ![Skjermbilde med avmerkingsboks for prissettingattributter](media/PRT-4.png)

7. <span data-ttu-id="c7341-124">Klikk **OK** for å lukke siden, og velg deretter **Oppdater trinn**.</span><span class="sxs-lookup"><span data-stu-id="c7341-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Skjermbilde som viser "Oppdater trinn"-knappen](media/PRT-5.png)
 
8. <span data-ttu-id="c7341-126">Gjenta denne prosessen for den andre plugin-modulen, **PreOperationQuoteLineDetail – oppdaterer msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="c7341-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="c7341-127">Lukk registreringsverktøyet for plugin-modul.</span><span class="sxs-lookup"><span data-stu-id="c7341-127">Close the plug-in registration tool.</span></span>

