---
title: Opprette en prisliste
description: Slik oppretter du en prisliste i Project Service
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 32f0cc66d1caa08bd24eb232338444df0388de3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006073"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="0ac80-103">Opprette en prisliste (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0ac80-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0ac80-104">Prislister gir en mal som kontoadministratorene kan bruke for oppretting av tilbud og prosjekter, og for fastsettelse av kostnadene for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="0ac80-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="0ac80-105">De inneholder et linjeelementliste over roller og utgifter, og prisen du vil ta for hver.</span><span class="sxs-lookup"><span data-stu-id="0ac80-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="0ac80-106">Du kan opprette flere prislister, slik at du kan ha separate prisstrukturer for ulike områder du selger produktene i, eller for ulike salgskanaler.</span><span class="sxs-lookup"><span data-stu-id="0ac80-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="0ac80-107">Det er en god idé å opprette minst én prisliste for hver valuta du har tenkt å fakturere kundene i.</span><span class="sxs-lookup"><span data-stu-id="0ac80-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="0ac80-108">Hvis du vil opprette økonomiske estimater for arbeid som skal leveres, kontrollerer du at alle prosjekter har en støttekostnads- og salgsprisliste.</span><span class="sxs-lookup"><span data-stu-id="0ac80-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="0ac80-109">Definer en standardkostnads- og salgsprisliste som gjelder for alle prosjekter som opprettes i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="0ac80-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="0ac80-110">Prislister er avhengige av roller og utgiftskategorier, så før du oppretter en prisliste, må du passe på at du allerede har konfigurert rollene og utgiftskategoriene du vil bruke under oppretting av prislisten.</span><span class="sxs-lookup"><span data-stu-id="0ac80-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="0ac80-111">Gå til **Project Service > Prislister**.</span><span class="sxs-lookup"><span data-stu-id="0ac80-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="0ac80-112">Klikk **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0ac80-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="0ac80-113">I **Kontekst** velger du om denne prislisten er for **Kostnad**, **Kjøp** eller **Salg**.</span><span class="sxs-lookup"><span data-stu-id="0ac80-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="0ac80-114">I **Navnet** skriver du inn et navn for prislisten.</span><span class="sxs-lookup"><span data-stu-id="0ac80-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="0ac80-115">I **Valuta** velger du valutaen du vil bruke for fakturering eller etterkalkulering.</span><span class="sxs-lookup"><span data-stu-id="0ac80-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="0ac80-116">I **Tidsenhet** angir du tidsperioden prisen gjelder for, for eksempel dag eller time.</span><span class="sxs-lookup"><span data-stu-id="0ac80-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="0ac80-117">Fyll ut **Startdato**, **Sluttdato** og **Beskrivelse** etter behov.</span><span class="sxs-lookup"><span data-stu-id="0ac80-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="0ac80-118">Klikk **Lagre** for å opprette oppføringen slik at du kan fortsette å redigere den.</span><span class="sxs-lookup"><span data-stu-id="0ac80-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="0ac80-119">Hvis du vil legge til en rollepris i prislisten, klikker du **+** under **Rollepriser**.</span><span class="sxs-lookup"><span data-stu-id="0ac80-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="0ac80-120">I **Rollepris**-ruten fyller du ut detaljene, og klikker deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="0ac80-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="0ac80-121">Fortsett å legge til rollepriser etter behov.</span><span class="sxs-lookup"><span data-stu-id="0ac80-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="0ac80-122">Når du er ferdig, klikker du **Lagre** nederst til høyre på skjermen.</span><span class="sxs-lookup"><span data-stu-id="0ac80-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="0ac80-123">Hvis du vil legge til en utgiftskategori i prislisten, klikker du **+** under **Kategoripriser**.</span><span class="sxs-lookup"><span data-stu-id="0ac80-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="0ac80-124">I **Pris for transaksjonskategorier**-ruten fyller du ut detaljene, og klikker deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="0ac80-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="0ac80-125">Fortsett å legge til kategoripriser etter behov.</span><span class="sxs-lookup"><span data-stu-id="0ac80-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="0ac80-126">Når du er ferdig, klikker du **Lagre** nederst til høyre på skjermen.</span><span class="sxs-lookup"><span data-stu-id="0ac80-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="0ac80-127">Hvis du vil legge til prislisteelementer i prislisten, klikker du **+** under **Prislisteelementer**.</span><span class="sxs-lookup"><span data-stu-id="0ac80-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="0ac80-128">I **Prislisteelement**-ruten fyller du ut detaljene, og klikker deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="0ac80-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="0ac80-129">Fortsett å legge til prislisteelementer etter behov.</span><span class="sxs-lookup"><span data-stu-id="0ac80-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="0ac80-130">Når du er ferdig, klikker du **Lagre** nederst til høyre på skjermen.</span><span class="sxs-lookup"><span data-stu-id="0ac80-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="0ac80-131">Hvis du vil legge til distriktsrelasjoner i prislisten, klikker du **+** under **Distriktsrelasjoner**.</span><span class="sxs-lookup"><span data-stu-id="0ac80-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="0ac80-132">I **Ny tilkobling**-vinduet fyller du ut detaljene, og klikker deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="0ac80-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="0ac80-133">Fortsett å legge til distriktsrelasjoner etter behov.</span><span class="sxs-lookup"><span data-stu-id="0ac80-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="0ac80-134">Når du er ferdig, klikker du **Lagre** nederst til høyre på skjermen.</span><span class="sxs-lookup"><span data-stu-id="0ac80-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0ac80-135">Se også</span><span class="sxs-lookup"><span data-stu-id="0ac80-135">See Also</span></span>  
 [<span data-ttu-id="0ac80-136">Konfigurere Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0ac80-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]