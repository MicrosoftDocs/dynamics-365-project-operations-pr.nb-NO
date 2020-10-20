---
title: Lukk tilbud
description: Dette emnet gir informasjon om hvordan du lukker et tilbud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896203"
---
# <a name="close-quotes"></a><span data-ttu-id="f08ef-103">Lukk tilbud</span><span class="sxs-lookup"><span data-stu-id="f08ef-103">Close quotes</span></span> 

<span data-ttu-id="f08ef-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="f08ef-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f08ef-105">Et prosjekttilbud kan lukkes som vunnet eller tapt.</span><span class="sxs-lookup"><span data-stu-id="f08ef-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="f08ef-106">Operasjonene Aktiver og Revider i tilbud støttes ikke i Microsoft Dynamics 365 Project Operations, slik at et utkasttilbud kan lukkes.</span><span class="sxs-lookup"><span data-stu-id="f08ef-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="f08ef-107">Lukk et tilbud som vunnet</span><span class="sxs-lookup"><span data-stu-id="f08ef-107">Close a quote as Won</span></span>

<span data-ttu-id="f08ef-108">Hvis du lukker et prosjekttilbud som vunnet, lukkes tilbudet med statusen satt til Lukket, og statusårsaken satt til Vunnet.</span><span class="sxs-lookup"><span data-stu-id="f08ef-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="f08ef-109">Ved å lukke tilbudet blir prosjekttilbudet skrivebeskyttet, og det opprettes et prosjektkontraktutkast som inneholder tilbudsinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="f08ef-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="f08ef-110">Siden et lukket tilbud ikke kan åpnes på nytt, vises det en bekreftelsesdialogboks før endringene blir utført, siden endringene kan ikke gjøres om.</span><span class="sxs-lookup"><span data-stu-id="f08ef-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="f08ef-111">Hvis tilbudet er knyttet til en salgsmulighet, lukkes eventuelle andre prosjekttilbud på salgsmuligheten automatisk som tapt.</span><span class="sxs-lookup"><span data-stu-id="f08ef-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="f08ef-112">Økonomisk påvirkning av å lukke et tilbud som vunnet</span><span class="sxs-lookup"><span data-stu-id="f08ef-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="f08ef-113">Hvis det har vært faktiske verdier for tid registrert i et prosjekt mens det fremdeles er knyttet til et utkasttilbud, registreres bare kostnadene for tiden eller utgiften.</span><span class="sxs-lookup"><span data-stu-id="f08ef-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="f08ef-114">Når et tilbud er lukket som vunnet, vil programmet refaktorere kostnadene ved å reversere de eldre faktiske kostnadsverdiene og opprette nye faktiske kostnadsverdier på nytt.</span><span class="sxs-lookup"><span data-stu-id="f08ef-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="f08ef-115">Programmet behandler disse faktiske kostnadsverdiene basert på faktureringsmetoden for den tilknyttede prosjektkontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="f08ef-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="f08ef-116">Hvis de faktiske kostnadsverdiene refererer til en kontraktlinje for tid og materialer, oppretter systemet automatisk tilsvarende faktiske verdier for ikke-fakturerte salg når tilbudet lukkes og prosjektkontrakten opprettes.</span><span class="sxs-lookup"><span data-stu-id="f08ef-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="f08ef-117">Hvis de faktiske kostnadsverdiene refererer til en kontraktlinje med fast pris, stoppes den nye behandlingen av de faktiske kostnadsverdiene basert på reglene for delt fakturering for prosjektkontraktkundene.</span><span class="sxs-lookup"><span data-stu-id="f08ef-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="f08ef-118">Lukk et tilbud som tapt:</span><span class="sxs-lookup"><span data-stu-id="f08ef-118">Closing a quote as lost:</span></span>

<span data-ttu-id="f08ef-119">Hvis du lukker et prosjekttilbud som tapt, settes statusen til Lukket og statusårsaken til Tapt.</span><span class="sxs-lookup"><span data-stu-id="f08ef-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="f08ef-120">Hvis du lukker tilbudet, blir prosjekttilbudet skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="f08ef-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="f08ef-121">Siden et lukket tilbud ikke kan åpnes på nytt, vil en bekreftelsesdialogboks bekrefte endringene før du lukker et tilbud.</span><span class="sxs-lookup"><span data-stu-id="f08ef-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="f08ef-122">Hvis prosjekttilbudet som er lukket som tapt, har et prosjekt det er referert til på noen av linjene, blir dette prosjektet også merket som lukket, og eventuelle ressursbestillinger fra den dagen og fremover blir annullert.</span><span class="sxs-lookup"><span data-stu-id="f08ef-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="f08ef-123">I Project Operations vil lukking av et tilbud som vunnet eller tapt ikke virke inn på statusen for salgsmuligheten, som forblir åpen til den lukkes manuelt.</span><span class="sxs-lookup"><span data-stu-id="f08ef-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
