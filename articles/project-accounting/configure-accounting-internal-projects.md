---
title: Konfigurere regnskap for interne prosjekter
description: Dette emnet gir informasjon om hvordan du konfigurerer regnskapspraksiser for interne prosjekter i Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012868"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="19b2f-103">Konfigurere regnskap for interne prosjekter</span><span class="sxs-lookup"><span data-stu-id="19b2f-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="19b2f-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="19b2f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="19b2f-105">Interne prosjekter gjør det mulig for selskaper å spore kostnader relatert til aktiviteter som ikke blir fakturert til en kunde.</span><span class="sxs-lookup"><span data-stu-id="19b2f-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="19b2f-106">Eksempler på interne prosjekter er:</span><span class="sxs-lookup"><span data-stu-id="19b2f-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="19b2f-107">Utvikling av et produkt, for eksempel en mobilapp, og sporing av kostnadene som er knyttet til utviklingen.</span><span class="sxs-lookup"><span data-stu-id="19b2f-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="19b2f-108">Behandle tid og utgifter før salg.</span><span class="sxs-lookup"><span data-stu-id="19b2f-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="19b2f-109">Dette interne prosjektet før salg kan konverteres til et fakturerbart prosjekt senere hvis tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="19b2f-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="19b2f-110">Prosjekter som ikke er knyttet til en kontrakt i Dynamics 365 Project Operations, behandles som interne.</span><span class="sxs-lookup"><span data-stu-id="19b2f-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="19b2f-111">Prosjektkostnads- og omsetningsprofiler brukes ikke til å fastsette regnskapsregler for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="19b2f-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="19b2f-112">Interne prosjektkostnader bokføres alltid ved hjelp av resultatprinsipper.</span><span class="sxs-lookup"><span data-stu-id="19b2f-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="19b2f-113">Hovedbokkontoer for inn bokføringer defineres på siden **Finansposteringsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="19b2f-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="19b2f-114">Tidstransaksjoner bokføres ved å debitere **Kostnad**-kontoen og kreditere **Lønnstildeling**-kontoen.</span><span class="sxs-lookup"><span data-stu-id="19b2f-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="19b2f-115">Utgiftstransaksjoner bokføres ved å debitere **Kostnad**-kontoen og kreditere kontoen **Forskyvningskonto for utgift**.</span><span class="sxs-lookup"><span data-stu-id="19b2f-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="19b2f-116">Varetransaksjoner posteres ved å debitere kontoen **Kostnad** og kreditere kontoen **Kostnad – Vare**.</span><span class="sxs-lookup"><span data-stu-id="19b2f-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="19b2f-117">Når transaksjoner er bokført til prosjektet, tilbakefører systemet alle akkumulerte transaksjoner og oppretter nye fakturerbare transaksjoner hvis prosjektet er tilknyttet en prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="19b2f-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="19b2f-118">De fakturerbare transaksjonene følger regnskapsreglene som er definert i den respektive kostnads- og omsetningsprofilen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="19b2f-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
