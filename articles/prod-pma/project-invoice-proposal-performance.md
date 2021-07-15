---
title: Ytelse for prosjektfakturaforslag
description: Dette emnet inneholder informasjon om ytelsesforbedringer av prosjektfakturaforslag.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269802"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="4345e-103">Ytelse for prosjektfakturaforslag</span><span class="sxs-lookup"><span data-stu-id="4345e-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4345e-104">Når du oppretter et nytt fakturaforslag, kan det oppstå ytelsesproblemer etter hvert som antall prosjekter og delprosjekter øker.</span><span class="sxs-lookup"><span data-stu-id="4345e-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="4345e-105">For å forbedre ytelsen er en funksjon tilgjengelig som reduserer tiden du trenger for å opprette et nytt fakturaforslag for posterte prosjekttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="4345e-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="4345e-106">Aktiver ytelsesforbedringen for prosjektfakturaforslag</span><span class="sxs-lookup"><span data-stu-id="4345e-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="4345e-107">Fullfør fremgangsmåten nedenfor for å aktivere funksjonen for ytelsesforbedring av prosjektfakturaforslaget.</span><span class="sxs-lookup"><span data-stu-id="4345e-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="4345e-108">Gå til **Funksjonsbehandling** > **Alle**.</span><span class="sxs-lookup"><span data-stu-id="4345e-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="4345e-109">Finn **Ytelsesforbedring for prosjektfakturaforslag** i funksjonslisten.</span><span class="sxs-lookup"><span data-stu-id="4345e-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="4345e-110">Velg **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="4345e-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="4345e-111">Oppdater nettleseren, og opprett deretter et nytt fakturaforslag.</span><span class="sxs-lookup"><span data-stu-id="4345e-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="4345e-112">Deaktiver ytelsesforbedringen for prosjektfakturaforslag</span><span class="sxs-lookup"><span data-stu-id="4345e-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="4345e-113">Fullfør fremgangsmåten nedenfor for å deaktivere funksjonen for ytelsesforbedring av prosjektfakturaforslaget.</span><span class="sxs-lookup"><span data-stu-id="4345e-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="4345e-114">Gå til **Funksjonsbehandling** > **Alle**.</span><span class="sxs-lookup"><span data-stu-id="4345e-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="4345e-115">Finn **Ytelsesforbedring for prosjektfakturaforslag** i funksjonslisten.</span><span class="sxs-lookup"><span data-stu-id="4345e-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="4345e-116">Velg **Deaktiver**.</span><span class="sxs-lookup"><span data-stu-id="4345e-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="4345e-117">Oppdater nettleseren din.</span><span class="sxs-lookup"><span data-stu-id="4345e-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="4345e-118">Ytelse for fakturaforslag kan ikke brukes når faktureringsregler er aktivert.</span><span class="sxs-lookup"><span data-stu-id="4345e-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="4345e-119">I løpet av den satsvise prosessen for å opprette fakturaforslag deler antall delaktiviteter oppgavene til et maksimumsantall basert på antall kontrakter med fakturerbare transaksjoner, uavhengig av hva du har angitt.</span><span class="sxs-lookup"><span data-stu-id="4345e-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="4345e-120">Hvis du for eksempel angir **3** for antall delaktiviteter for oppretting av fakturaforslaget satsvis, og det bare er to kontrakter med fakturerbare transaksjoner, opprettes det bare to delaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="4345e-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
