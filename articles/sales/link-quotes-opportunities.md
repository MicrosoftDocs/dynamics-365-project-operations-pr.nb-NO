---
title: Opprett prosjekttilbud fra salgsmuligheter
description: Denne emnet gir informasjon om oppretting av et prosjekttilbud fra en salgsmulighet.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898544"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="a424a-103">Opprett prosjekttilbud fra salgsmuligheter</span><span class="sxs-lookup"><span data-stu-id="a424a-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="a424a-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="a424a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a424a-105">Tilbud kan opprettes fra prosjektmuligheter på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="a424a-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="a424a-106">Fra kategorien **Tilbud** på siden **Prosjektmuligheter**</span><span class="sxs-lookup"><span data-stu-id="a424a-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="a424a-107">Fra flyten Salgsprosess for salgsmulighet</span><span class="sxs-lookup"><span data-stu-id="a424a-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="a424a-108">Ved å oppdatere salgsmulighetsreferansen for et eksisterende tilbud</span><span class="sxs-lookup"><span data-stu-id="a424a-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="a424a-109">Fra kategorien Tilbud på siden Prosjektmuligheter</span><span class="sxs-lookup"><span data-stu-id="a424a-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="a424a-110">Du kan opprette et prosjekttilbud fra en salgsmulighet ved å følge fremgangs måten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a424a-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="a424a-111">Åpne siden **Prosjektmuligheter**, og velg kategorien **Tilbud**.</span><span class="sxs-lookup"><span data-stu-id="a424a-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="a424a-112">I delrutenettet **Tilbud** velger du **+** for å opprette det nye prosjekttilbudet basert på salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="a424a-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="a424a-113">Alle salgsmulighetslinjene og de relaterte prosjektprislistene kopieres til det nye tilbudet fra salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="a424a-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="a424a-114">Fra flyten Salgsprosess for salgsmulighet</span><span class="sxs-lookup"><span data-stu-id="a424a-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="a424a-115">Du kan opprette et tilbud fra flyten Salgsprosess for salgsmulighet ved å følge fremgangs måten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a424a-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="a424a-116">Åpne salgsmuligheten fra flyten Salgsprosess for salgsmulighet.</span><span class="sxs-lookup"><span data-stu-id="a424a-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="a424a-117">Velg fasen **Kvalifiser**.</span><span class="sxs-lookup"><span data-stu-id="a424a-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="a424a-118">Velg **Neste**, og velg deretter **+ Opprett** for å opprette et nytt tilbud.</span><span class="sxs-lookup"><span data-stu-id="a424a-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="a424a-119">Det meste av informasjonen i kategorien **Sammendrag** for dette nye tilbudet hentes som standard fra salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="a424a-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="a424a-120">Angi eventuell nødvendig informasjon som mangler, eller oppdater standardverdiene etter behov i kategorien **Sammendrag**.</span><span class="sxs-lookup"><span data-stu-id="a424a-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="a424a-121">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a424a-121">Select **Save**.</span></span> <span data-ttu-id="a424a-122">Det nye tilbudet opprettes og knyttes til salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="a424a-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="a424a-123">Du kan nå vise tilbudsinformasjonen i kategorien **Tilbud** på siden **Salgsmulighet**.</span><span class="sxs-lookup"><span data-stu-id="a424a-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="a424a-124">Salgsprosessen for salgsmuligheten flyttes til neste fase, **Foreslå**.</span><span class="sxs-lookup"><span data-stu-id="a424a-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="a424a-125">Ved å oppdatere salgsmulighetsreferansen for et eksisterende tilbud</span><span class="sxs-lookup"><span data-stu-id="a424a-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="a424a-126">Et eksisterende tilbud kan kobles til en salgsmulighet.</span><span class="sxs-lookup"><span data-stu-id="a424a-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="a424a-127">Fullfør fremgangsmåten nedenfor for å oppdatere salgsmulighetsinformasjonen for et eksisterende tilbud.</span><span class="sxs-lookup"><span data-stu-id="a424a-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="a424a-128">Åpne siden **Tilbud**, og velg kategorien **Sammendrag**.</span><span class="sxs-lookup"><span data-stu-id="a424a-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="a424a-129">I **Salgsmulighet**-feltet velger du salgsmuligheten du vil knytte til tilbudet.</span><span class="sxs-lookup"><span data-stu-id="a424a-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="a424a-130">Du kan se tilbudet i rutenettet **Tilbud** for salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="a424a-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="a424a-131">Ved hjelp av salgsprosessen for salgsmuligheten kan salgsmuligheten flyttes til neste fase, **Foreslå**.</span><span class="sxs-lookup"><span data-stu-id="a424a-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="a424a-132">Når du flytter en salgsmulighet til denne fasen, kan du velge dette tilbudet fra en liste over tilbud som er knyttet til denne salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="a424a-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="a424a-133">Hvis du velger dette tilbudet, angir du at det skal flyttes fremover.</span><span class="sxs-lookup"><span data-stu-id="a424a-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="a424a-134">Alle de andre tilbudene som er knyttet til salgsmuligheten, vil fremdeles være tilgjengelig eog aktivee til ett av dem er vunnet.</span><span class="sxs-lookup"><span data-stu-id="a424a-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="a424a-135">Du kan flytte salgsprosessen tilbake til den forrige fasen, **Kvalifiser**, og velge et nytt tilbud å flytte fremover med.</span><span class="sxs-lookup"><span data-stu-id="a424a-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
