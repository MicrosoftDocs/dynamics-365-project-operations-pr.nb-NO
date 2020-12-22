---
title: Oppdatere programtilleggattributter med nye prisdimensjoner
description: Dette emnet gir informasjon om hvordan du oppdaterer programtilleggattributter for prisdimensjoner.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643230"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="b2354-103">Oppdatere programtilleggattributter med nye prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="b2354-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="b2354-104">Dette emnet gir informasjon om hvordan du oppdaterer programtilleggattributter for prisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="b2354-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="b2354-105">Dette emnet gjelder bare for tilbuds- og kontraktfunksjonene i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b2354-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b2354-106">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="b2354-106">Prerequisites</span></span>
<span data-ttu-id="b2354-107">Før du fullfører trinnene i dette emnet, må du fullføre prosedyrene i følgende emner:</span><span class="sxs-lookup"><span data-stu-id="b2354-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="b2354-108">Opprette egendefinerte felt og enheter</span><span class="sxs-lookup"><span data-stu-id="b2354-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="b2354-109">Legge til egendefinerte felt i prisoppsett og transaksjonsenheter </span><span class="sxs-lookup"><span data-stu-id="b2354-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="b2354-110">[Konfigurere egendefinerte felt som prisdimensjoner](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="b2354-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="b2354-111">Hvis du ikke har fullført disse prosedyrene, kan du fullføre dem og deretter gå tilbake til dette emnet.</span><span class="sxs-lookup"><span data-stu-id="b2354-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="b2354-112">Registrer et programtillegg</span><span class="sxs-lookup"><span data-stu-id="b2354-112">Register a plug-in</span></span>
<span data-ttu-id="b2354-113">Når det blir opprettet en tilbudslinjedetalj på **Tilbudslinje**-siden for en tilbudslinje for prosjektet, oppretter systemet to estimatlinjer.</span><span class="sxs-lookup"><span data-stu-id="b2354-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="b2354-114">Én linje gjelder for kostnadssiden for estimatet, og den andre linjen er for salgssiden.</span><span class="sxs-lookup"><span data-stu-id="b2354-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="b2354-115">Dette er det samme for prosjektkontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="b2354-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="b2354-116">Når du gjør en endring i antallet eller et felt på kostnadssiden, overføres endringen også til salgssiden.</span><span class="sxs-lookup"><span data-stu-id="b2354-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="b2354-117">Dette er mulig fordi PreOperation-programtilleggene på Quotelinedetail og kontraktlinjedetalj-enheter kobler bestemte attributter på kostnadssiden til salgssiden av transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="b2354-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="b2354-118">Hvis du trenger at endringer som er gjort på prisdimensjonsverdiene på salgssiden også blir gjort på kostnadssiden, må du også registrere følgende tilleggsprogrammer på nytt etter at du har gjort endringer i en prisdimensjon.</span><span class="sxs-lookup"><span data-stu-id="b2354-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="b2354-119">Dette er tilleggsprogrammene som skal oppdateres og registreres på nytt:</span><span class="sxs-lookup"><span data-stu-id="b2354-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="b2354-120">PreOperationContractLineDetailUpdate – **Oppdater msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="b2354-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="b2354-121">PreOperationQuoteLineDetailUpdate – **Oppdaterer msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="b2354-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="b2354-122">Fullfør fremgangsmåten nedenfor for å oppdatere og registrere programtilleggene på nytt.</span><span class="sxs-lookup"><span data-stu-id="b2354-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="b2354-123">Åpne **PluginRegistrationTool** og koble til Project Operations Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="b2354-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="b2354-124">Velg **Søk**, og skriv inn de første bokstavene i programtillegget som skal oppdateres.</span><span class="sxs-lookup"><span data-stu-id="b2354-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="b2354-125">Når programtillegget er funnet, velger du den, og deretter velger du **Velg på hovedskjema**.</span><span class="sxs-lookup"><span data-stu-id="b2354-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="b2354-126">Velg **Update msdyn_orderlinetransaction**-trinnet, høyreklikk og velg deretter **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="b2354-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="b2354-127">I **Oppdatering**-dialogbokssiden velger du ellipsen (**...**) i filtreringsattributtene.</span><span class="sxs-lookup"><span data-stu-id="b2354-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="b2354-128">Vinduet for filtreringsattributter åpnes og gir en liste over alle attributtene i enheten og prisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="b2354-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="b2354-129">Velg avmerkingsboksene for prisdimensjonsattributtene.</span><span class="sxs-lookup"><span data-stu-id="b2354-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="b2354-130">Velg **OK** for å lukke siden, og velg deretter **Oppdater trinn**.</span><span class="sxs-lookup"><span data-stu-id="b2354-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="b2354-131">Gjenta trinn 2 til 7 for det andre programtillegget, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="b2354-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="b2354-132">For dette programtillegget må du oppdatere, **Oppdatering av msdyn_quotelinetransaction**-trinnet.</span><span class="sxs-lookup"><span data-stu-id="b2354-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="b2354-133">Lukk **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="b2354-133">Close **PluginRegistrationTool**.</span></span>
