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
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131715"
---
# <a name="expense-estimates"></a><span data-ttu-id="9e6da-103">Utgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="9e6da-103">Expense estimates</span></span>
<span data-ttu-id="9e6da-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="9e6da-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9e6da-105">Sammen med å definere ressursbaserte estimater tillater Dynamics 365 Project Operations at prosjektledere definerer prosjektbasert utgifter for hvert prosjekt.</span><span class="sxs-lookup"><span data-stu-id="9e6da-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="9e6da-106">Hvert utgiftselement kan tilknyttes en bestemt prosjektoppgave eller utgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="9e6da-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="9e6da-107">Utgiftskategorier defineres vanligvis på organisasjonsnivå.</span><span class="sxs-lookup"><span data-stu-id="9e6da-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="9e6da-108">Priser for hver utgiftskategori defineres vanligvis i følgende hierarki:</span><span class="sxs-lookup"><span data-stu-id="9e6da-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="9e6da-109">Organisasjonen</span><span class="sxs-lookup"><span data-stu-id="9e6da-109">Organization</span></span>
- <span data-ttu-id="9e6da-110">Kunde</span><span class="sxs-lookup"><span data-stu-id="9e6da-110">Customer</span></span>
- <span data-ttu-id="9e6da-111">Tilbud/kontrakt</span><span class="sxs-lookup"><span data-stu-id="9e6da-111">Quote/contract</span></span>

<span data-ttu-id="9e6da-112">Fullfør fremgangsmåten nedenfor for å vise, legge til eller slette en prosjektutgift.</span><span class="sxs-lookup"><span data-stu-id="9e6da-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="9e6da-113">Gå til **Prosjekter**, og velg prosjektet du vil arbeide med.</span><span class="sxs-lookup"><span data-stu-id="9e6da-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="9e6da-114">Velg kategorien **Prosjektestimater**, og vis listen over prosjektutgifter.</span><span class="sxs-lookup"><span data-stu-id="9e6da-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="9e6da-115">Velg **Ny utgift** for å legge til en utgift.</span><span class="sxs-lookup"><span data-stu-id="9e6da-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="9e6da-116">Du kan også velge en utgift som skal slettes, og deretter velge **Slett utgift**.</span><span class="sxs-lookup"><span data-stu-id="9e6da-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="9e6da-117">Følgende attributter defineres for hvert utgiftslinjeelement:</span><span class="sxs-lookup"><span data-stu-id="9e6da-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="9e6da-118">**Kategori**: Felles grupperinger som brukes til å beskrive alle utgifter som er påløpt i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="9e6da-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="9e6da-119">**Startdato**: Datoen da utgiften er beregnet å påløpe.</span><span class="sxs-lookup"><span data-stu-id="9e6da-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="9e6da-120">**Antall**: Det estimerte antallet utgiftselementer for en bestemt kategori.</span><span class="sxs-lookup"><span data-stu-id="9e6da-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="9e6da-121">**Kostpris for enhet**: Enhetsprisen som brukes til å beregne kostnad for utgiften.</span><span class="sxs-lookup"><span data-stu-id="9e6da-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="9e6da-122">**Salgspris for enhet**: Enhetsprisen som brukes til å beregne salgsprisen for utgiften.</span><span class="sxs-lookup"><span data-stu-id="9e6da-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

