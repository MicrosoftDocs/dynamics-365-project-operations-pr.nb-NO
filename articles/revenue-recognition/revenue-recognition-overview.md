---
title: Oversikt over inntektsføring
description: Dette emnet gir informasjon om inntektsføring i Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013768"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="20d28-103">Oversikt over inntektsføring</span><span class="sxs-lookup"><span data-stu-id="20d28-103">Revenue recognition overview</span></span>

<span data-ttu-id="20d28-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="20d28-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="20d28-105">I Dynamics 365 Project Operations kan det være forskjellige prinsipper for inntektsføring, basert på den valgte faktureringsmetoden for et prosjekt eller en del av prosjektet.</span><span class="sxs-lookup"><span data-stu-id="20d28-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="20d28-106">Dette emnet gir informasjon om inntektsføring i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="20d28-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="20d28-107">Transaksjoner beregnet ved hjelp av faktureringsmetode for tid og materialer</span><span class="sxs-lookup"><span data-stu-id="20d28-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="20d28-108">Kostnads- og inntektsføring er tilkoblet.</span><span class="sxs-lookup"><span data-stu-id="20d28-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="20d28-109">Transaksjonskostnader og ufakturerte salg posteres ved hjelp av [Integreringsjournal for Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="20d28-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="20d28-110">Prosjektkostnads- og inntektsprofil avgjør om ufakturerte salgstransaksjoner blir postert til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="20d28-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="20d28-111">Hvis **Avsett inntekt** er valgt, bruker systemet **VIA-salgsverdi** og **Påløpte inntekter – salgsverdi**-kontoene under postering.</span><span class="sxs-lookup"><span data-stu-id="20d28-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="20d28-112">Nedenfor er et eksempel på denne metoden.</span><span class="sxs-lookup"><span data-stu-id="20d28-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="20d28-113">Transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="20d28-113">Transaction type</span></span> | <span data-ttu-id="20d28-114">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="20d28-114">Debit/Credit</span></span> | <span data-ttu-id="20d28-115">Mengde</span><span class="sxs-lookup"><span data-stu-id="20d28-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="20d28-116">VIA – Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="20d28-116">WIP Sales value</span></span> | <span data-ttu-id="20d28-117">Debet</span><span class="sxs-lookup"><span data-stu-id="20d28-117">Debit</span></span> | <span data-ttu-id="20d28-118">100</span><span class="sxs-lookup"><span data-stu-id="20d28-118">100</span></span> |
  | <span data-ttu-id="20d28-119">Påløpt inntekt – Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="20d28-119">Accrued revenue sales value</span></span> | <span data-ttu-id="20d28-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="20d28-120">Credit</span></span> | <span data-ttu-id="20d28-121">100</span><span class="sxs-lookup"><span data-stu-id="20d28-121">100</span></span> |

- <span data-ttu-id="20d28-122">Inntekt gjenkjennes gjennom fakturering.</span><span class="sxs-lookup"><span data-stu-id="20d28-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="20d28-123">Systemet bruker **Fakturert inntekt**-kontoen under postering.</span><span class="sxs-lookup"><span data-stu-id="20d28-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="20d28-124">Nedenfor er et eksempel på denne metoden.</span><span class="sxs-lookup"><span data-stu-id="20d28-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="20d28-125">Transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="20d28-125">Transaction type</span></span> | <span data-ttu-id="20d28-126">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="20d28-126">Debit/Credit</span></span> | <span data-ttu-id="20d28-127">Mengde</span><span class="sxs-lookup"><span data-stu-id="20d28-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="20d28-128">Kundesaldo</span><span class="sxs-lookup"><span data-stu-id="20d28-128">Customer balance</span></span> | <span data-ttu-id="20d28-129">Debet</span><span class="sxs-lookup"><span data-stu-id="20d28-129">Debit</span></span> | <span data-ttu-id="20d28-130">120</span><span class="sxs-lookup"><span data-stu-id="20d28-130">120</span></span> |
  | <span data-ttu-id="20d28-131">Skyldig merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="20d28-131">Sales tax payable</span></span> | <span data-ttu-id="20d28-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="20d28-132">Credit</span></span> | <span data-ttu-id="20d28-133">20</span><span class="sxs-lookup"><span data-stu-id="20d28-133">20</span></span> |
  | <span data-ttu-id="20d28-134">Fakturert inntekt</span><span class="sxs-lookup"><span data-stu-id="20d28-134">Invoiced Revenue</span></span> | <span data-ttu-id="20d28-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="20d28-135">Credit</span></span> | <span data-ttu-id="20d28-136">100</span><span class="sxs-lookup"><span data-stu-id="20d28-136">100</span></span> |

- <span data-ttu-id="20d28-137">Hvis inntekten var påløpt da det ufakturerte salget ble postert, tilbakefører systemet den påløpte inntekten ved fakturering.</span><span class="sxs-lookup"><span data-stu-id="20d28-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="20d28-138">Transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="20d28-138">Transaction type</span></span> | <span data-ttu-id="20d28-139">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="20d28-139">Debit/Credit</span></span> | <span data-ttu-id="20d28-140">Mengde</span><span class="sxs-lookup"><span data-stu-id="20d28-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="20d28-141">VIA – Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="20d28-141">WIP Sales value</span></span> | <span data-ttu-id="20d28-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="20d28-142">Credit</span></span> | <span data-ttu-id="20d28-143">100</span><span class="sxs-lookup"><span data-stu-id="20d28-143">100</span></span> |
  | <span data-ttu-id="20d28-144">Påløpt inntekt – Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="20d28-144">Accrued revenue sales value</span></span> | <span data-ttu-id="20d28-145">Debet</span><span class="sxs-lookup"><span data-stu-id="20d28-145">Debit</span></span> | <span data-ttu-id="20d28-146">100</span><span class="sxs-lookup"><span data-stu-id="20d28-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="20d28-147">Transaksjoner beregnet ved bruk av faktureringsmetode for fastpris</span><span class="sxs-lookup"><span data-stu-id="20d28-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="20d28-148">Kostnads- og inntektsføring er separate.</span><span class="sxs-lookup"><span data-stu-id="20d28-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="20d28-149">Transaksjonskostnader posteres ved hjelp av [Integreringsjournalen for Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="20d28-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="20d28-150">Ufakturerte salgstransaksjoner opprettes ikke.</span><span class="sxs-lookup"><span data-stu-id="20d28-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="20d28-151">Inntekt kan gjenkjennes under fakturering hvis prosjektkostnads- og inntektsprofilen har **Prinsipp brukt til beregninger for prosjektfullføring** satt til **Ingen VIA**.</span><span class="sxs-lookup"><span data-stu-id="20d28-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="20d28-152">Bruk bare denne metoden for kortsiktige, enkle prosjekter.</span><span class="sxs-lookup"><span data-stu-id="20d28-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="20d28-153">Inntekt kan gjenkjennes ved hjelp av inntektsestimat for fastpris, med enten **Fullført kontrakt** eller **Inntektsføring for fullføringsprosent**-metoden.</span><span class="sxs-lookup"><span data-stu-id="20d28-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20d28-154">Ytterligere ressurser</span><span class="sxs-lookup"><span data-stu-id="20d28-154">Additional resources</span></span>
[<span data-ttu-id="20d28-155">Konfigurer regnskap for fakturerbare prosjekter</span><span class="sxs-lookup"><span data-stu-id="20d28-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="20d28-156">Inntektsestimat for fastprisprosjekter</span><span class="sxs-lookup"><span data-stu-id="20d28-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="20d28-157">Administrer inntektsestimater</span><span class="sxs-lookup"><span data-stu-id="20d28-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="20d28-158">Metoder for ferdigstillingskostnad</span><span class="sxs-lookup"><span data-stu-id="20d28-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]