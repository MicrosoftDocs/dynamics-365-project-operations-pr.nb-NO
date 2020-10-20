---
title: Oversikt over utgifter
description: Dette emnet gir information om Utgift-funksjonaliteten i Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967378"
---
# <a name="expense-home-page"></a><span data-ttu-id="56286-103">Startside for utgift</span><span class="sxs-lookup"><span data-stu-id="56286-103">Expense home page</span></span>

<span data-ttu-id="56286-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="56286-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="56286-105">Dynamics 365 Project Operations støtte behandling av utgifter.</span><span class="sxs-lookup"><span data-stu-id="56286-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="56286-106">Utgiftsbehandling forekommer med eller uten prosjekter ved å bruke en tilpassbar arbeidsflyt med policyer, transaksjonskategorier og godkjenninger.</span><span class="sxs-lookup"><span data-stu-id="56286-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="56286-107">I Project Operations finnes det to støttede distribusjonsmodeller for utgifter:</span><span class="sxs-lookup"><span data-stu-id="56286-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="56286-108">**Fullstendig**: Fullstendig distribusjon er tilgjengelig for **Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer** eller **Project Operations for produksjonsordrebaserte scenarioer**.</span><span class="sxs-lookup"><span data-stu-id="56286-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="56286-109">**Standard**: Standard distribusjon er tilgjengelig for **Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer** og **Lite-distribusjon – avtale til proformafakturering**.</span><span class="sxs-lookup"><span data-stu-id="56286-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="56286-110">Fullstendig</span><span class="sxs-lookup"><span data-stu-id="56286-110">Full</span></span> 
<span data-ttu-id="56286-111">Fullstendig utgiftsdistribusjon gir en fullstendig håndheving av en policy som inkluderer muligheten til å opprette policyer, for eksempel følgende:</span><span class="sxs-lookup"><span data-stu-id="56286-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="56286-112">Grenser for utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="56286-112">Expense category limits</span></span>
  - <span data-ttu-id="56286-113">Reise</span><span class="sxs-lookup"><span data-stu-id="56286-113">Travel</span></span>
  - <span data-ttu-id="56286-114">Kostgodtgjørelse</span><span class="sxs-lookup"><span data-stu-id="56286-114">Per diem</span></span>
  - <span data-ttu-id="56286-115">Kredittkortimporter</span><span class="sxs-lookup"><span data-stu-id="56286-115">Credit card imports</span></span>
  - <span data-ttu-id="56286-116">Optisk tegngjenkjenning for kvittering</span><span class="sxs-lookup"><span data-stu-id="56286-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="56286-117">Standard</span><span class="sxs-lookup"><span data-stu-id="56286-117">Basic</span></span> 
<span data-ttu-id="56286-118">Et scenario med standard utgiftsdistribusjons tillater bare registrering av grunnleggende utgifter mot et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="56286-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="56286-119">Hvis du vil ha mer informasjon, kan du se [Utgiftsregistrering (Lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="56286-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="56286-120">Fastslå utgiftsdistribusjonen</span><span class="sxs-lookup"><span data-stu-id="56286-120">Determine your Expense deployment</span></span>
<span data-ttu-id="56286-121">For å finne ut om du kjører standard distribusjon av utgiftshåndtering, må du kontrollere at URL-adressen for adressen slutter på **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="56286-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
