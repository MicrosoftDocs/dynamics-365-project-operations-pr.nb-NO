---
title: Utviklers merknader til godkjenninger
description: Dette emnet inneholder tilleggsinformasjon fra utvikler om arbeid med godkjenninger.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996803"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="9a82f-103">Utviklers merknader til godkjenninger</span><span class="sxs-lookup"><span data-stu-id="9a82f-103">Developer notes for Approvals</span></span>

<span data-ttu-id="9a82f-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="9a82f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9a82f-105">Dynamics 365 Project Operations inkluderer valideringslogikk som sikrer riktig oppføringsoverføring gjennom godkjenningstrinnene.</span><span class="sxs-lookup"><span data-stu-id="9a82f-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="9a82f-106">Riktig oppføringsoverføringer sikrer følgende:</span><span class="sxs-lookup"><span data-stu-id="9a82f-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="9a82f-107">Alle støtterader opprettes i relaterte tabeller, for eksempel journaler og faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="9a82f-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="9a82f-108">Godkjenneren merkes som en **Prosjektgodkjenner** i prosjektet før du fortsetter.</span><span class="sxs-lookup"><span data-stu-id="9a82f-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]