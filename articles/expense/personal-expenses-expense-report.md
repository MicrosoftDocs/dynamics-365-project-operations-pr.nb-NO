---
title: Arbeide med personlige utgifter i en utgiftsrapport
description: Dette emnet inneholder informasjon om hvordan du arbeider med personlige utgifter som påløper for ansatte når de reiser i forretningsformål.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025696"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="653a7-103">Arbeide med personlige utgifter i en utgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="653a7-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="653a7-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="653a7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="653a7-105">I løpet av forretningsreiser kan en ansatt kreve personlige utgifter for bedriftens kredittkort.</span><span class="sxs-lookup"><span data-stu-id="653a7-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="653a7-106">Hvis en prosess ikke er definert for håndtering av personlige utgifter, kan godkjenningsprosessen for utgiftsrapport bli avbrutt når en ansatt sender sin spesifiserte utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="653a7-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="653a7-107">Du kan bruke to metoder for å arbeide med personlige utgifter for en ansatt:</span><span class="sxs-lookup"><span data-stu-id="653a7-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="653a7-108">**Betalt av ansatt**: Organisasjonen betaler ikke personlige utgifter som vises på fakturaen for firmaets kredittkort.</span><span class="sxs-lookup"><span data-stu-id="653a7-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="653a7-109">I stedet betaler den ansatte kredittkortleverandøren direkte for utgiftene.</span><span class="sxs-lookup"><span data-stu-id="653a7-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="653a7-110">**Betalt av firma**: Organisasjonen betaler hele regningen for bedriftskredittkortet, og deretter belaster arbeiderens konto for de personlige utgiftene.</span><span class="sxs-lookup"><span data-stu-id="653a7-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="653a7-111">Du kan velge metoden organisasjonen bruker, på siden **Parametere for utgiftshåndtering**.</span><span class="sxs-lookup"><span data-stu-id="653a7-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="653a7-112">Aktiver funksjon for delt utgift når personlig beløpsfelt har verdi definert</span><span class="sxs-lookup"><span data-stu-id="653a7-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="653a7-113">Funksjonen **Aktiver funksjon for delt utgift når personlig beløpsfelt har verdi definert**, gjelder bare utgiftsrapporter som er godkjent ved hjelp av en arbeidsflyt på linjenivå.</span><span class="sxs-lookup"><span data-stu-id="653a7-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="653a7-114">Rapporter godkjennes ved å gå til **Behandle kostnadsrapporter** > **Kostnadsrapporter tilordnet til meg** > **Åpne utgiftsrapport**.</span><span class="sxs-lookup"><span data-stu-id="653a7-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="653a7-115">Hvis du vil aktivere denne funksjonen, går du til **Arbeidsområder** > **Funksjonsbehandling**, velger **Aktiver funksjon for delt utgift når personlig beløpsfelt har verdi definert**, og deretter velger du **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="653a7-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="653a7-116">Når funksjonen er aktivert, genererer utgiftslinjer som bruker denne funksjonaliteten, to linjer når rapporten sendes.</span><span class="sxs-lookup"><span data-stu-id="653a7-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="653a7-117">To linjer genereres, slik at godkjenneren kan godkjenne hver linje separat.</span><span class="sxs-lookup"><span data-stu-id="653a7-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
