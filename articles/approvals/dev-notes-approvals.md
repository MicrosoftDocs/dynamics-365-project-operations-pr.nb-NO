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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483960"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="a2a1d-103">Utviklers merknader til godkjenninger</span><span class="sxs-lookup"><span data-stu-id="a2a1d-103">Developer notes for Approvals</span></span>

<span data-ttu-id="a2a1d-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="a2a1d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a2a1d-105">Dynamics 365 Project Operations inkluderer valideringslogikk som sikrer riktig oppføringsoverføring gjennom godkjenningstrinnene.</span><span class="sxs-lookup"><span data-stu-id="a2a1d-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="a2a1d-106">Riktig oppføringsoverføringer sikrer følgende:</span><span class="sxs-lookup"><span data-stu-id="a2a1d-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="a2a1d-107">Alle støtterader opprettes i relaterte tabeller, for eksempel journaler og faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="a2a1d-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="a2a1d-108">Godkjenneren merkes som en **Prosjektgodkjenner** i prosjektet før du fortsetter.</span><span class="sxs-lookup"><span data-stu-id="a2a1d-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
