---
title: Hva er nytt eller endret i Project Service Automation Update Release 17, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 17, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bb93208217972639f91b39b7b6705d9897373ef7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126812"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="e8a84-103">Project Service Automation, Update Release 17, V3</span><span class="sxs-lookup"><span data-stu-id="e8a84-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="e8a84-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e8a84-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e8a84-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="e8a84-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="e8a84-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e8a84-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e8a84-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="e8a84-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="e8a84-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e8a84-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e8a84-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for PSA V3, Update Release 17.</span><span class="sxs-lookup"><span data-stu-id="e8a84-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="e8a84-110">Denne versjonen har buildnummer V3.10.6.34 og er generelt tilgjengelig via en egen oppdatering fra mars 2020.</span><span class="sxs-lookup"><span data-stu-id="e8a84-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="e8a84-111">Update Release 17</span><span class="sxs-lookup"><span data-stu-id="e8a84-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e8a84-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="e8a84-112">Bug fixes</span></span>

<span data-ttu-id="e8a84-113">**Generelt**</span><span class="sxs-lookup"><span data-stu-id="e8a84-113">**General**</span></span>

- <span data-ttu-id="e8a84-114">Løst: Oppdatert Project Service Automation for å håndheve teammedlemmers lisenser (prosjektressurshuben vil inkludere tjenesteplanmetadata 3.x for teammedlem)</span><span class="sxs-lookup"><span data-stu-id="e8a84-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="e8a84-115">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="e8a84-115">**Time and Expense**</span></span>

- <span data-ttu-id="e8a84-116">Fast: Det er ikke mulig å endre et utgiftsestimat til null (0) fra en annen pris enn null.</span><span class="sxs-lookup"><span data-stu-id="e8a84-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="e8a84-117">Endringen ignoreres.</span><span class="sxs-lookup"><span data-stu-id="e8a84-117">The change is ignored.</span></span>

<span data-ttu-id="e8a84-118">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="e8a84-118">**Project Management**</span></span>

- <span data-ttu-id="e8a84-119">Løst: En kontroll for nullverdier i stillingsnavnet for et teammedlem er lagt til.</span><span class="sxs-lookup"><span data-stu-id="e8a84-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="e8a84-120">Løst: Feltet **msdyn_userresourceid** for enheten **msdyn_resourceassignment** er avskrevet.</span><span class="sxs-lookup"><span data-stu-id="e8a84-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="e8a84-121">Løst: Oppgradering fra 2.x til 3.x håndterer nå tomme innsatsprofiler på oppgavetilordninger.</span><span class="sxs-lookup"><span data-stu-id="e8a84-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="e8a84-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="e8a84-122">**Sales**</span></span>

- <span data-ttu-id="e8a84-123">Løst: **Invoice.PreValidateInvoiceUpdate** behandler nå scenarioet for å tilordne oppføringseiere på nytt på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="e8a84-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="e8a84-124">Løst: Når transaksjonsklassen er **Tidspunkt**, er **UnitGroup** ikke redigerbart for alle enheter, inkludert **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** og **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="e8a84-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="e8a84-125">Imidlertid er **Enhet** ikke-redigerbart kun for **JournalLine** og **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="e8a84-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


