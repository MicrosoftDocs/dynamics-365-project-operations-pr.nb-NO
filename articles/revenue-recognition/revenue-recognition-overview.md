---
title: Oversikt over inntektsføring
description: Dette emnet gir informasjon om inntektsføring i Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368038"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="6d592-103">Oversikt over inntektsføring</span><span class="sxs-lookup"><span data-stu-id="6d592-103">Revenue recognition overview</span></span>

<span data-ttu-id="6d592-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="6d592-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6d592-105">I Dynamics 365 Project Operations kan det være forskjellige prinsipper for inntektsføring, basert på den valgte faktureringsmetoden for et prosjekt eller en del av prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6d592-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="6d592-106">Dette emnet gir informasjon om inntektsføring i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6d592-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="6d592-107">Transaksjoner beregnet ved hjelp av faktureringsmetode for tid og materialer</span><span class="sxs-lookup"><span data-stu-id="6d592-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="6d592-108">Kostnads- og inntektsføring er tilkoblet.</span><span class="sxs-lookup"><span data-stu-id="6d592-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="6d592-109">Transaksjonskostnader og ufakturerte salg posteres ved hjelp av [Integreringsjournal for Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="6d592-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="6d592-110">Prosjektkostnads- og inntektsprofil avgjør om ufakturerte salgstransaksjoner blir postert til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="6d592-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="6d592-111">Hvis **Avsett inntekt** er valgt, bruker systemet **VIA-salgsverdi** og **Påløpte inntekter – salgsverdi**-kontoene under postering.</span><span class="sxs-lookup"><span data-stu-id="6d592-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="6d592-112">Nedenfor er et eksempel på denne metoden.</span><span class="sxs-lookup"><span data-stu-id="6d592-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="6d592-113">Transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="6d592-113">Transaction type</span></span> | <span data-ttu-id="6d592-114">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="6d592-114">Debit/Credit</span></span> | <span data-ttu-id="6d592-115">Mengde</span><span class="sxs-lookup"><span data-stu-id="6d592-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="6d592-116">VIA – Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="6d592-116">WIP Sales value</span></span> | <span data-ttu-id="6d592-117">Debet</span><span class="sxs-lookup"><span data-stu-id="6d592-117">Debit</span></span> | <span data-ttu-id="6d592-118">100</span><span class="sxs-lookup"><span data-stu-id="6d592-118">100</span></span> |
  | <span data-ttu-id="6d592-119">Påløpt inntekt – Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="6d592-119">Accrued revenue sales value</span></span> | <span data-ttu-id="6d592-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="6d592-120">Credit</span></span> | <span data-ttu-id="6d592-121">100</span><span class="sxs-lookup"><span data-stu-id="6d592-121">100</span></span> |

- <span data-ttu-id="6d592-122">Inntekt gjenkjennes gjennom fakturering.</span><span class="sxs-lookup"><span data-stu-id="6d592-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="6d592-123">Systemet bruker **Fakturert inntekt**-kontoen under postering.</span><span class="sxs-lookup"><span data-stu-id="6d592-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="6d592-124">Nedenfor er et eksempel på denne metoden.</span><span class="sxs-lookup"><span data-stu-id="6d592-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="6d592-125">Transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="6d592-125">Transaction type</span></span> | <span data-ttu-id="6d592-126">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="6d592-126">Debit/Credit</span></span> | <span data-ttu-id="6d592-127">Mengde</span><span class="sxs-lookup"><span data-stu-id="6d592-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="6d592-128">Kundesaldo</span><span class="sxs-lookup"><span data-stu-id="6d592-128">Customer balance</span></span> | <span data-ttu-id="6d592-129">Debet</span><span class="sxs-lookup"><span data-stu-id="6d592-129">Debit</span></span> | <span data-ttu-id="6d592-130">120</span><span class="sxs-lookup"><span data-stu-id="6d592-130">120</span></span> |
  | <span data-ttu-id="6d592-131">Skyldig merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="6d592-131">Sales tax payable</span></span> | <span data-ttu-id="6d592-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="6d592-132">Credit</span></span> | <span data-ttu-id="6d592-133">20</span><span class="sxs-lookup"><span data-stu-id="6d592-133">20</span></span> |
  | <span data-ttu-id="6d592-134">Fakturert inntekt</span><span class="sxs-lookup"><span data-stu-id="6d592-134">Invoiced Revenue</span></span> | <span data-ttu-id="6d592-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="6d592-135">Credit</span></span> | <span data-ttu-id="6d592-136">100</span><span class="sxs-lookup"><span data-stu-id="6d592-136">100</span></span> |

- <span data-ttu-id="6d592-137">Hvis inntekten var påløpt da det ufakturerte salget ble postert, tilbakefører systemet den påløpte inntekten ved fakturering.</span><span class="sxs-lookup"><span data-stu-id="6d592-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="6d592-138">Transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="6d592-138">Transaction type</span></span> | <span data-ttu-id="6d592-139">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="6d592-139">Debit/Credit</span></span> | <span data-ttu-id="6d592-140">Mengde</span><span class="sxs-lookup"><span data-stu-id="6d592-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="6d592-141">VIA – Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="6d592-141">WIP Sales value</span></span> | <span data-ttu-id="6d592-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="6d592-142">Credit</span></span> | <span data-ttu-id="6d592-143">100</span><span class="sxs-lookup"><span data-stu-id="6d592-143">100</span></span> |
  | <span data-ttu-id="6d592-144">Påløpt inntekt – Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="6d592-144">Accrued revenue sales value</span></span> | <span data-ttu-id="6d592-145">Debet</span><span class="sxs-lookup"><span data-stu-id="6d592-145">Debit</span></span> | <span data-ttu-id="6d592-146">100</span><span class="sxs-lookup"><span data-stu-id="6d592-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="6d592-147">Transaksjoner beregnet ved bruk av faktureringsmetode for fastpris</span><span class="sxs-lookup"><span data-stu-id="6d592-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="6d592-148">Kostnads- og inntektsføring er separate.</span><span class="sxs-lookup"><span data-stu-id="6d592-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="6d592-149">Transaksjonskostnader posteres ved hjelp av [Integreringsjournalen for Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="6d592-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="6d592-150">Ufakturerte salgstransaksjoner opprettes ikke.</span><span class="sxs-lookup"><span data-stu-id="6d592-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="6d592-151">Inntekt kan gjenkjennes under fakturering hvis prosjektkostnads- og inntektsprofilen har **Prinsipp brukt til beregninger for prosjektfullføring** satt til **Ingen VIA**.</span><span class="sxs-lookup"><span data-stu-id="6d592-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="6d592-152">Bruk bare denne metoden for kortsiktige, enkle prosjekter.</span><span class="sxs-lookup"><span data-stu-id="6d592-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="6d592-153">Inntekt kan gjenkjennes ved hjelp av inntektsestimat for fastpris, med enten **Fullført kontrakt** eller **Inntektsføring for fullføringsprosent**-metoden.</span><span class="sxs-lookup"><span data-stu-id="6d592-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d592-154">Ytterligere ressurser</span><span class="sxs-lookup"><span data-stu-id="6d592-154">Additional resources</span></span>
[<span data-ttu-id="6d592-155">Konfigurer regnskap for fakturerbare prosjekter</span><span class="sxs-lookup"><span data-stu-id="6d592-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="6d592-156">Inntektsestimat for fastprisprosjekter</span><span class="sxs-lookup"><span data-stu-id="6d592-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="6d592-157">Administrer inntektsestimater</span><span class="sxs-lookup"><span data-stu-id="6d592-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="6d592-158">Metoder for ferdigstillingskostnad</span><span class="sxs-lookup"><span data-stu-id="6d592-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]