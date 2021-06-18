---
title: Overstyre salgsprislister for prosjekt
description: Dette emnet gir informasjon om hvordan du oppretter egendefinerte prislister for salg.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: db2ff6acaad6ab4cbcc98d3d5b06b36ed23b758f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995093"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="d1989-103">Overstyre salgsprislister for prosjekt</span><span class="sxs-lookup"><span data-stu-id="d1989-103">Override project sales price lists</span></span>

<span data-ttu-id="d1989-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="d1989-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="d1989-105">Kundespesifikke prosjektprislister</span><span class="sxs-lookup"><span data-stu-id="d1989-105">Customer-specific project price lists</span></span>

<span data-ttu-id="d1989-106">Kundespesifikke prisavtaler kan konfigureres som prosjektprislister på en forretningsforbindelsesoppføring i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d1989-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="d1989-107">Hvis du vil definere en kundespesifikk prosjektprisliste, navigerer du til forretningsforbindelsesoppføringen i **Salg**-området.</span><span class="sxs-lookup"><span data-stu-id="d1989-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="d1989-108">Åpne listesiden **Forretningsforbindelser**.</span><span class="sxs-lookup"><span data-stu-id="d1989-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="d1989-109">Finn og dobbeltklikk en kundeoppføring for å åpne detaljsiden **Forretningsforbindelse**.</span><span class="sxs-lookup"><span data-stu-id="d1989-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="d1989-110">På **Prosjektprislister**-fanen velger du **+ Ny prosjektprisliste**.</span><span class="sxs-lookup"><span data-stu-id="d1989-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="d1989-111">På siden **Ny prosjektprisliste** velger du en prisliste fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="d1989-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="d1989-112">Bare prislister som har konteksten satt til **Salg**, og der valutaen samsvarer med valutaen for forretningsforbindelsen, er inkludert.</span><span class="sxs-lookup"><span data-stu-id="d1989-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="d1989-113">Angi et navn på tilknytningen, og velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d1989-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="d1989-114">En kundespesifikk prosjektprisliste opprettes.</span><span class="sxs-lookup"><span data-stu-id="d1989-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="d1989-115">Denne prislisten blir brukt til å angi standard prosjektpriser i prosjekttilbud eller kontrakter som er opprettet for denne kunden, der datoen for opprettelsen av tilbud eller prosjektkontrakt faller innenfor datogyldigheten for prislisten.</span><span class="sxs-lookup"><span data-stu-id="d1989-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="d1989-116">Egendefinerte priser på prosjekttilbud</span><span class="sxs-lookup"><span data-stu-id="d1989-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="d1989-117">I prosjekttilbud kan du ha prosjektpriser som starter med en standard prisliste som angis som standard fra kunden eller fra prosjektparameterne.</span><span class="sxs-lookup"><span data-stu-id="d1989-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="d1989-118">Når du trenger egendefinerte priser for prosjektrelatert arbeid på et bestemt tilbud, kan du få dette fra den tilknyttede enheten for prosjektprislister.</span><span class="sxs-lookup"><span data-stu-id="d1989-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="d1989-119">Fullfør fremgangsmåten nedenfor for å definere tilbudsspesifikke prosjektpriser.</span><span class="sxs-lookup"><span data-stu-id="d1989-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="d1989-120">Åpne prosjekttilbudet og velg kategorien **Prosjektprislister**.</span><span class="sxs-lookup"><span data-stu-id="d1989-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="d1989-121">I delrutenettet velger du **Opprett egendefinert prising**.</span><span class="sxs-lookup"><span data-stu-id="d1989-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="d1989-122">Alle prosjektprislistene som er knyttet til tilbudet, kopieres til nye prislister.</span><span class="sxs-lookup"><span data-stu-id="d1989-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="d1989-123">Navnene på de nye prislistene gjenspeiler navnet på tilbudet med et dato- og tidsstempel for når disse prislistene ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="d1989-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="d1989-124">Du kan bruke hver av disse prislistene til å gjøre oppdateringer for arbeids- (rollepris) og utgiftspriser (kategoripris).</span><span class="sxs-lookup"><span data-stu-id="d1989-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="d1989-125">Disse prisene gjelder bare for dette prosjekttilbudet.</span><span class="sxs-lookup"><span data-stu-id="d1989-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="d1989-126">Prosjektlister på en prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="d1989-126">Price lists on a project contract</span></span>

<span data-ttu-id="d1989-127">I en prosjektkontrakt blir alltid prosjektprissetting som standard en egendefinert prisliste med navnet på kontrakten og det opprettede dato/klokkeslett-stempelet lagt til i navnet.</span><span class="sxs-lookup"><span data-stu-id="d1989-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="d1989-128">Dette gjelder enten kontrakten ble opprettet da tilbudet ble vunnet, eller hvis kontrakten ble opprettet fra grunnen av.</span><span class="sxs-lookup"><span data-stu-id="d1989-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="d1989-129">Du kan om nødvendig fjerne denne tilordningen til den egendefinerte prislisten og knytte en standard prisliste til prosjektkontrakten i stedet.</span><span class="sxs-lookup"><span data-stu-id="d1989-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="d1989-130">Når du knytter en standard prisliste til prosjektprislistene i tilbud eller kontrakt, vil eventuelle endringer som gjøres i prisene i prislisten, ha innvirkning på alle tilbud og kontrakter som bruker prislisten.</span><span class="sxs-lookup"><span data-stu-id="d1989-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]