---
title: Utgiftsestimater
description: Dette emnet gir informasjon om hvordan du definerer eller beregner prosjektrelaterte utgifter.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287070"
---
# <a name="expense-estimates"></a><span data-ttu-id="bff58-103">Utgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="bff58-103">Expense estimates</span></span>
<span data-ttu-id="bff58-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="bff58-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bff58-105">Sammen med definering av ressursbaserte estimater kan prosjektledere definere prosjektbaserte utgifter for hvert prosjekt i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="bff58-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="bff58-106">Hvert utgiftselement kan tilknyttes en bestemt prosjektoppgave eller utgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="bff58-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="bff58-107">Utgiftskategorier defineres vanligvis på organisasjonsnivå.</span><span class="sxs-lookup"><span data-stu-id="bff58-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="bff58-108">Priser for hver utgiftskategori defineres vanligvis i følgende hierarki:</span><span class="sxs-lookup"><span data-stu-id="bff58-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="bff58-109">Organisasjonen</span><span class="sxs-lookup"><span data-stu-id="bff58-109">Organization</span></span>
- <span data-ttu-id="bff58-110">Kunde</span><span class="sxs-lookup"><span data-stu-id="bff58-110">Customer</span></span>
- <span data-ttu-id="bff58-111">Tilbud/kontrakt</span><span class="sxs-lookup"><span data-stu-id="bff58-111">Quote/contract</span></span>

<span data-ttu-id="bff58-112">Fullfør fremgangsmåten nedenfor for å vise, legge til eller slette en prosjektutgift.</span><span class="sxs-lookup"><span data-stu-id="bff58-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="bff58-113">Gå til **Prosjekter**, og velg prosjektet du vil arbeide med.</span><span class="sxs-lookup"><span data-stu-id="bff58-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="bff58-114">Velg kategorien **Prosjektestimater**, og vis listen over prosjektutgifter.</span><span class="sxs-lookup"><span data-stu-id="bff58-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="bff58-115">Velg **Ny utgift** for å legge til en utgift.</span><span class="sxs-lookup"><span data-stu-id="bff58-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="bff58-116">Du kan også velge en utgift som skal slettes, og deretter velge **Slett utgift**.</span><span class="sxs-lookup"><span data-stu-id="bff58-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="bff58-117">Følgende attributter defineres for hvert utgiftslinjeelement:</span><span class="sxs-lookup"><span data-stu-id="bff58-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="bff58-118">**Kategori**: Felles grupperinger som brukes til å beskrive alle utgifter som er påløpt i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="bff58-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="bff58-119">**Startdato**: Datoen da utgiften er beregnet å påløpe.</span><span class="sxs-lookup"><span data-stu-id="bff58-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="bff58-120">**Antall**: Det estimerte antallet utgiftselementer for en bestemt kategori.</span><span class="sxs-lookup"><span data-stu-id="bff58-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="bff58-121">**Kostpris for enhet**: Enhetsprisen som brukes til å beregne kostnad for utgiften.</span><span class="sxs-lookup"><span data-stu-id="bff58-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="bff58-122">**Salgspris for enhet**: Enhetsprisen som brukes til å beregne salgsprisen for utgiften.</span><span class="sxs-lookup"><span data-stu-id="bff58-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]