---
title: Utviklers merknader til godkjenninger
description: Dette emnet inneholder tilleggsinformasjon fra utvikler om arbeid med godkjenninger.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290281"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="8b332-103">Utviklers merknader til godkjenninger</span><span class="sxs-lookup"><span data-stu-id="8b332-103">Developer notes for Approvals</span></span>

<span data-ttu-id="8b332-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="8b332-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8b332-105">Dynamics 365 Project Operations inkluderer valideringslogikk som sikrer riktig oppføringsoverføring gjennom godkjenningstrinnene.</span><span class="sxs-lookup"><span data-stu-id="8b332-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="8b332-106">Riktig oppføringsoverføringer sikrer følgende:</span><span class="sxs-lookup"><span data-stu-id="8b332-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="8b332-107">Alle støtterader opprettes i relaterte tabeller, for eksempel journaler og faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="8b332-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="8b332-108">Godkjenneren merkes som en **Prosjektgodkjenner** i prosjektet før du fortsetter.</span><span class="sxs-lookup"><span data-stu-id="8b332-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]