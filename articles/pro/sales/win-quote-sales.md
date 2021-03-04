---
title: Lukke et tilbud – Lite
description: Dette emnet gir informasjon om hvordan du lukker et tilbud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764876"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="169c7-103">Lukke et tilbud – Lite</span><span class="sxs-lookup"><span data-stu-id="169c7-103">Close a quote - lite</span></span>

<span data-ttu-id="169c7-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="169c7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="169c7-105">Et prosjekttilbud kan lukkes som vunnet eller tapt.</span><span class="sxs-lookup"><span data-stu-id="169c7-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="169c7-106">Et tilbudsutkast kan lukkes fordi operasjonene Aktiver og Revider tilbud ikke støttes i Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="169c7-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="169c7-107">Lukk et tilbud som vunnet</span><span class="sxs-lookup"><span data-stu-id="169c7-107">Close a quote as Won</span></span>

<span data-ttu-id="169c7-108">Når du lukker et prosjekttilbud som Vunnet, settes statusen til Lukket, og statusårsak er Vunnet.</span><span class="sxs-lookup"><span data-stu-id="169c7-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="169c7-109">Ved å lukke tilbudet blir prosjekttilbudet skrivebeskyttet, og det opprettes et prosjektkontraktutkast som inneholder tilbudsinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="169c7-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="169c7-110">Et lukket tilbud kan ikke åpnes på nytt, og derfor bekreftes endringene i en bekreftelsesdialogboks.</span><span class="sxs-lookup"><span data-stu-id="169c7-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="169c7-111">Hvis tilbudet er knyttet til en salgsmulighet, lukkes eventuelle andre prosjekttilbud på salgsmuligheten automatisk som tapt.</span><span class="sxs-lookup"><span data-stu-id="169c7-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="169c7-112">Økonomisk påvirkning av å lukke et tilbud som vunnet</span><span class="sxs-lookup"><span data-stu-id="169c7-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="169c7-113">Hvis det finnes faktiske data for tid på et prosjekt mens det fremdeles er knyttet til et tilbudsutkast, registreres bare kostnadene for tids- eller utgiftene.</span><span class="sxs-lookup"><span data-stu-id="169c7-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="169c7-114">Når et tilbud er lukket som vunnet, vil programmet refaktorere kostnadene ved å reversere de eldre faktiske kostnadsverdiene og opprette nye faktiske kostnadsverdier på nytt.</span><span class="sxs-lookup"><span data-stu-id="169c7-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="169c7-115">Programmet behandler disse faktiske kostnadsverdiene basert på faktureringsmetoden for den tilknyttede prosjektkontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="169c7-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="169c7-116">Hvis de faktiske kostnadene refererer til en tids- og materialkontraktlinje, opprettes tilsvarende faktiske salg for når tilbudet lukkes og prosjektkontrakten opprettes.</span><span class="sxs-lookup"><span data-stu-id="169c7-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="169c7-117">Hvis de faktiske kostnadene refererer til en kontraktlinje med fast pris, slutter programmet å reprosessere de faktiske kostnadene som er basert på de delte faktureringsreglene for prosjektkontraktkundene.</span><span class="sxs-lookup"><span data-stu-id="169c7-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="169c7-118">Lukk et tilbud som tapt:</span><span class="sxs-lookup"><span data-stu-id="169c7-118">Closing a quote as lost:</span></span>

<span data-ttu-id="169c7-119">Når du lukker et prosjekttilbud som Tapt, settes statusen til Lukket, og statusårsak er Tapt.</span><span class="sxs-lookup"><span data-stu-id="169c7-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="169c7-120">Hvis du lukker tilbudet, blir prosjekttilbudet skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="169c7-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="169c7-121">Siden et lukket tilbud ikke kan åpnes på nytt, vil en bekreftelsesdialogboks bekrefte endringene før du lukker et tilbud.</span><span class="sxs-lookup"><span data-stu-id="169c7-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="169c7-122">Hvis prosjekttilbudet som lukkes som Tapt, refererer til et prosjekt på noen av linjene, blir det prosjektet også merket som Lukket.</span><span class="sxs-lookup"><span data-stu-id="169c7-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="169c7-123">Eventuelle ressursbestillinger fra den dagen og fremover annulleres.</span><span class="sxs-lookup"><span data-stu-id="169c7-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="169c7-124">I Project Operations vil lukking av et tilbud som vunnet eller tapt ikke virke inn på statusen for salgsmuligheten, som forblir åpen til den lukkes manuelt.</span><span class="sxs-lookup"><span data-stu-id="169c7-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
