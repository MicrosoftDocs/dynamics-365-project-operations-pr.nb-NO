---
title: Lukke et tilbud
description: Dette emnet gir informasjon om hvordan du lukker tilbud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2c752ba6395ed4bf025092219350dc245f7428f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277260"
---
# <a name="close-a-quote"></a><span data-ttu-id="695a6-103">Lukke et tilbud</span><span class="sxs-lookup"><span data-stu-id="695a6-103">Close a quote</span></span>

<span data-ttu-id="695a6-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="695a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="695a6-105">Et prosjekttilbud kan lukkes som vunnet eller tapt.</span><span class="sxs-lookup"><span data-stu-id="695a6-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="695a6-106">Siden funksjonene Aktiver og Revider ikke støttes på tilbud i Microsoft Dynamics 365 Project Operations, kan du lukke et utkasttilbud.</span><span class="sxs-lookup"><span data-stu-id="695a6-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="695a6-107">Lukk et tilbud som vunnet</span><span class="sxs-lookup"><span data-stu-id="695a6-107">Close a quote as Won</span></span>

<span data-ttu-id="695a6-108">Hvis du lukker et prosjekttilbud som vunnet, settes statusen for tilbudet til **Lukket**, og statusårsaken settes til **Vunnet**.</span><span class="sxs-lookup"><span data-stu-id="695a6-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="695a6-109">Ved å lukke tilbudet blir det skrivebeskyttet, og det opprettes et prosjektkontraktutkast med all tilbudsinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="695a6-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="695a6-110">Siden et lukket tilbud ikke kan åpnes på nytt, vil en bekreftelsesdialogboks bekrefte endringene før du lukker et tilbud.</span><span class="sxs-lookup"><span data-stu-id="695a6-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="695a6-111">Prosjektkontrakten som opprettes fra et prosjekttilbud, gjøres også tilgjengelig i modulen for prosjektstyring og regnskap i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="695a6-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="695a6-112">Hvis en prosjektkontrakt ikke er tilordnet til et prosjekt på noen av linjene, gjøres denne prosjektkontrakten tilgjengelig som en inaktiv prosjektkontrakt, og den blir aktiv så snart et prosjekt er tilordnet til minst én av kontraktlinjene.</span><span class="sxs-lookup"><span data-stu-id="695a6-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="695a6-113">Hvis tilbudet er knyttet til en salgsmulighet, lukkes eventuelle andre prosjekttilbud på salgsmuligheten automatisk som tapt.</span><span class="sxs-lookup"><span data-stu-id="695a6-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="695a6-114">Økonomisk påvirkning av å lukke et tilbud som vunnet</span><span class="sxs-lookup"><span data-stu-id="695a6-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="695a6-115">Hvis det har vært faktiske verdier for tid registrert i et prosjekt mens det fremdeles er knyttet til et utkasttilbud, registreres bare kostnadene for tiden eller utgiften.</span><span class="sxs-lookup"><span data-stu-id="695a6-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="695a6-116">Når et tilbud er lukket som vunnet, vil programmet refaktorere kostnadene ved å reversere de eldre faktiske kostnadsverdiene og opprette nye faktiske kostnadsverdier på nytt.</span><span class="sxs-lookup"><span data-stu-id="695a6-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="695a6-117">Programmet behandler disse faktiske kostnadsverdiene basert på faktureringsmetoden for den tilknyttede prosjektkontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="695a6-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="695a6-118">Hvis de faktiske kostnadsverdiene refererer til en kontraktlinje for tid og materialer, oppretter systemet automatisk tilsvarende faktiske verdier for ikke-fakturerte salg når tilbudet lukkes og prosjektkontrakten opprettes.</span><span class="sxs-lookup"><span data-stu-id="695a6-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="695a6-119">Hvis de faktiske kostnadsverdiene refererer til en kontraktlinje med fast pris, stoppes den nye behandlingen av de faktiske kostnadsverdiene basert på reglene for delt fakturering for prosjektkontraktkundene.</span><span class="sxs-lookup"><span data-stu-id="695a6-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="695a6-120">Alle etterbehandlede faktiske verdier er tilgjengelige i modulen for prosjektstyring og regnskap, slik at prosjektregnskapsføreren kan se gjennom, oppdatere og postere dem til hovedboken.</span><span class="sxs-lookup"><span data-stu-id="695a6-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="695a6-121">Lukk et tilbud som tapt</span><span class="sxs-lookup"><span data-stu-id="695a6-121">Close a quote as Lost</span></span>

<span data-ttu-id="695a6-122">Hvis du lukker et prosjekttilbud som tapt, settes statusen til **Lukket** og statusårsaken til **Tapt**.</span><span class="sxs-lookup"><span data-stu-id="695a6-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="695a6-123">Hvis du lukker tilbudet, blir det skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="695a6-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="695a6-124">Siden et lukket tilbud ikke kan åpnes på nytt, vil en bekreftelsesdialogboks bekrefte endringene før du lukker et tilbud.</span><span class="sxs-lookup"><span data-stu-id="695a6-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="695a6-125">Hvis prosjekttilbudet som er lukket som tapt, har et prosjekt det er referert til på noen av linjene, blir dette prosjektet også merket som lukket, og eventuelle ressursbestillinger fra den dagen og fremover blir annullert.</span><span class="sxs-lookup"><span data-stu-id="695a6-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="695a6-126">I Project Operations vil lukking av et tilbud som vunnet eller tapt ikke virke inn på statusen for salgsmuligheten, som forblir åpen til den lukkes manuelt.</span><span class="sxs-lookup"><span data-stu-id="695a6-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]