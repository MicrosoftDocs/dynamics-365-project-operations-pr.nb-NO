---
title: Korrigerte fakturaer
description: Dette emnet inneholder informasjon om korrigerte fakturaer.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898093"
---
# <a name="corrected-invoices"></a><span data-ttu-id="e366a-103">Korrigerte fakturaer</span><span class="sxs-lookup"><span data-stu-id="e366a-103">Corrected invoices</span></span>

<span data-ttu-id="e366a-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="e366a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e366a-105">Bekreftede fakturaer kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="e366a-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="e366a-106">Når du redigerer en bekreftet faktura, opprettes det et korrigert fakturautkast.</span><span class="sxs-lookup"><span data-stu-id="e366a-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="e366a-107">Fordi det antas at du vil tilbakeføre alle transaksjonene og antallene fra den opprinnelige fakturaen, inneholder denne korrigerte fakturaen alle transaksjonene fra den opprinnelige fakturaen, og alle antallene i den er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e366a-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="e366a-108">Hvis noen av transaksjonene ikke krever rettelser, kan du fjerne dem fra det korrigerte fakturautkastet.</span><span class="sxs-lookup"><span data-stu-id="e366a-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="e366a-109">Hvis du vil tilbakeføre eller bare returnere et delvis antall, kan du redigere Antall-feltet i linjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="e366a-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="e366a-110">Hvis du åpner fakturalinjedetaljene, kan du se det opprinnelige fakturaantallet.</span><span class="sxs-lookup"><span data-stu-id="e366a-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="e366a-111">Du kan deretter redigere det gjeldende fakturaantallet slik at det blir mindre enn eller større enn det opprinnelige fakturaantallet.</span><span class="sxs-lookup"><span data-stu-id="e366a-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="e366a-112">Når du bekrefter en korrigert faktura, tilbakeføres det opprinnelige faktiske fakturerte salget, og et nytt faktisk fakturert salg opprettes.</span><span class="sxs-lookup"><span data-stu-id="e366a-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="e366a-113">Hvis antallet ble redusert, vil forskjellen føre til at et nytt, ikke-fakturert faktisk salg også opprettes.</span><span class="sxs-lookup"><span data-stu-id="e366a-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="e366a-114">Hvis det opprinnelige fakturerte salget for eksempel var på åtte timer, og den korrigerte fakturalinjedetaljen har et redusert antall på seks timer, tilbakeføres den opprinnelige, fakturerte salgslinjen, og det opprettes to nye faktiske verdier:</span><span class="sxs-lookup"><span data-stu-id="e366a-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="e366a-115">Et fakturert faktisk salg på seks timer.</span><span class="sxs-lookup"><span data-stu-id="e366a-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="e366a-116">Et ikke-fakturert faktisk salg for de resterende to timene.</span><span class="sxs-lookup"><span data-stu-id="e366a-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="e366a-117">Denne transaksjonen kan enten faktureres senere eller merkes som ikke-belastbar, avhengig av forhandlingene med kunden.</span><span class="sxs-lookup"><span data-stu-id="e366a-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
