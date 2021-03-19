---
title: Oversikt over utgifter
description: Dette emnet gir information om Utgift-funksjonaliteten i Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c4e2f441e1c4b1bcba5bca292b8075b4334a004d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276585"
---
# <a name="expense-home-page"></a><span data-ttu-id="6f8b5-103">Startside for utgift</span><span class="sxs-lookup"><span data-stu-id="6f8b5-103">Expense home page</span></span>

<span data-ttu-id="6f8b5-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="6f8b5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6f8b5-105">Dynamics 365 Project Operations støtter muligheten til å behandle utgifter.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="6f8b5-106">Utgiftsbehandling forekommer med eller uten prosjekter ved å bruke en tilpassbar arbeidsflyt med policyer, transaksjonskategorier og godkjenninger.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="6f8b5-107">I Project Operations finnes det to støttede distribusjonsmodeller for utgifter:</span><span class="sxs-lookup"><span data-stu-id="6f8b5-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="6f8b5-108">**Fullstendig**: Fullstendig distribusjon er tilgjengelig for **Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer** eller **Project Operations for produksjonsordrebaserte scenarioer**.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="6f8b5-109">**Standard**: Standard distribusjon er tilgjengelig for **Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer** og **Lite-distribusjon – avtale til proformafakturering**.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="6f8b5-110">Fullstendig</span><span class="sxs-lookup"><span data-stu-id="6f8b5-110">Full</span></span> 
<span data-ttu-id="6f8b5-111">Full utgiftsdistribusjon gir en fullstendig håndhevelse av policyen som inkluderer muligheten til å opprette policyer, for eksempel følgende:</span><span class="sxs-lookup"><span data-stu-id="6f8b5-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="6f8b5-112">Grenser for utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="6f8b5-112">Expense category limits</span></span>
  - <span data-ttu-id="6f8b5-113">Reise</span><span class="sxs-lookup"><span data-stu-id="6f8b5-113">Travel</span></span>
  - <span data-ttu-id="6f8b5-114">Kostgodtgjørelse</span><span class="sxs-lookup"><span data-stu-id="6f8b5-114">Per diem</span></span>
  - <span data-ttu-id="6f8b5-115">Kredittkortimporter</span><span class="sxs-lookup"><span data-stu-id="6f8b5-115">Credit card imports</span></span>
  - <span data-ttu-id="6f8b5-116">Optisk tegngjenkjenning for kvittering</span><span class="sxs-lookup"><span data-stu-id="6f8b5-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="6f8b5-117">Standard</span><span class="sxs-lookup"><span data-stu-id="6f8b5-117">Basic</span></span> 
<span data-ttu-id="6f8b5-118">Et scenario med standard utgiftsdistribusjons tillater bare registrering av grunnleggende utgifter mot et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="6f8b5-119">Hvis du vil ha mer informasjon, kan du se [Utgiftsregistrering (Lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="6f8b5-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="6f8b5-120">Fastslå utgiftsdistribusjonen</span><span class="sxs-lookup"><span data-stu-id="6f8b5-120">Determine your Expense deployment</span></span>
<span data-ttu-id="6f8b5-121">For å finne ut om du kjører standard distribusjon av utgiftshåndtering, må du kontrollere at URL-adressen for adressen slutter på **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]