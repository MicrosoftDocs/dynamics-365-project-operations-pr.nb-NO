---
title: Oppdatere estimat for kostnad
description: Dette emnet gir informasjon om oppdatering av projeksjonen av innsats for et prosjekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081803"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="714df-103">Oppdatere estimat for kostnad</span><span class="sxs-lookup"><span data-stu-id="714df-103">Update estimate at completion</span></span>

<span data-ttu-id="714df-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="714df-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="714df-105">Det er vanlig at en prosjektleder kan revidere de opprinnelige beregningene på en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="714df-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="714df-106">Reprojisering av prosjekter er en prosjektleders oppfatning av estimater, gitt gjeldende status for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="714df-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="714df-107">Vi anbefaler imidlertid ikke at prosjektledere endrer tallene i den opprinnelige planen, fordi den opprinnelige planen for prosjektet er den etablerte sannhetskilden for prosjektets tidsplan og kostnadsestimat, som alle interessenter i prosjektet har godtatt.</span><span class="sxs-lookup"><span data-stu-id="714df-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="714df-108">Det er to måter en prosjektleder kan reprojisere innsats på aktiviteter:</span><span class="sxs-lookup"><span data-stu-id="714df-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="714df-109">Overstyr standard anslagstid med ny beregning av gjenstående gjenstående innsats for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="714df-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="714df-110">Overstyr standard fremdriftsprosent med ny beregning av den virkelige fremdriften for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="714df-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="714df-111">Hver av disse metodene forårsaker en ny beregning av aktivitetens ETC, EAC og fremdriftsprosent samt beregnet innsatsavvik for en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="714df-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="714df-112">EAC, ETC- og fremdriftsprosenten på aktivitetssammendragene beregnes på nytt, og det lages en ny projisering av innsatsavvik.</span><span class="sxs-lookup"><span data-stu-id="714df-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
