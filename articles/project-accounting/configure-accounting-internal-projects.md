---
title: Konfigurere regnskap for interne prosjekter
description: Dette emnet gir informasjon om hvordan du konfigurerer regnskapspraksiser for interne prosjekter i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287610"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="cdc43-103">Konfigurere regnskap for interne prosjekter</span><span class="sxs-lookup"><span data-stu-id="cdc43-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="cdc43-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="cdc43-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cdc43-105">Interne prosjekter gjør det mulig for selskaper å spore kostnader relatert til aktiviteter som ikke blir fakturert til en kunde.</span><span class="sxs-lookup"><span data-stu-id="cdc43-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="cdc43-106">Eksempler på interne prosjekter er:</span><span class="sxs-lookup"><span data-stu-id="cdc43-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="cdc43-107">Utvikling av et produkt, for eksempel en mobilapp, og sporing av kostnadene som er knyttet til utviklingen.</span><span class="sxs-lookup"><span data-stu-id="cdc43-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="cdc43-108">Behandle tid og utgifter før salg.</span><span class="sxs-lookup"><span data-stu-id="cdc43-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="cdc43-109">Dette interne prosjektet før salg kan konverteres til et fakturerbart prosjekt senere hvis tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="cdc43-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="cdc43-110">Prosjekter som ikke er knyttet til en kontrakt i Dynamics 365 Project Operations, behandles som interne.</span><span class="sxs-lookup"><span data-stu-id="cdc43-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="cdc43-111">Prosjektkostnads- og omsetningsprofiler brukes ikke til å fastsette regnskapsregler for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="cdc43-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="cdc43-112">Interne prosjektkostnader bokføres alltid ved hjelp av resultatprinsipper.</span><span class="sxs-lookup"><span data-stu-id="cdc43-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="cdc43-113">Hovedbokkontoer for inn bokføringer defineres på siden **Finansposteringsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="cdc43-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="cdc43-114">Tidstransaksjoner bokføres ved å debitere **Kostnad**-kontoen og kreditere **Lønnstildeling**-kontoen.</span><span class="sxs-lookup"><span data-stu-id="cdc43-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="cdc43-115">Utgiftstransaksjoner bokføres ved å debitere **Kostnad**-kontoen og kreditere kontoen **Forskyvningskonto for utgift**.</span><span class="sxs-lookup"><span data-stu-id="cdc43-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="cdc43-116">Når transaksjoner er bokført til prosjektet, tilbakefører systemet alle akkumulerte transaksjoner og oppretter nye fakturerbare transaksjoner hvis prosjektet er tilknyttet en prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="cdc43-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="cdc43-117">De fakturerbare transaksjonene følger regnskapsreglene som er definert i den respektive kostnads- og omsetningsprofilen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="cdc43-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]