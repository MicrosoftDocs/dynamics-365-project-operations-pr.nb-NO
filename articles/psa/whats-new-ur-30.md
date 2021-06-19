---
title: Hva er nytt eller endret i Project Service Automation Update Release 30, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 30, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010438"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="9a55f-103">Hva er nytt eller endret i Project Service Automation Update Release 30, V3</span><span class="sxs-lookup"><span data-stu-id="9a55f-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9a55f-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9a55f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9a55f-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="9a55f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9a55f-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9a55f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9a55f-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="9a55f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9a55f-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="9a55f-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="9a55f-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 30.</span><span class="sxs-lookup"><span data-stu-id="9a55f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="9a55f-110">Denne versjonen har et build-nummer på V3.10.51.61 og er generelt tilgjengelig via en egen oppdatering i april 2021.</span><span class="sxs-lookup"><span data-stu-id="9a55f-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="9a55f-111">Update Release 30</span><span class="sxs-lookup"><span data-stu-id="9a55f-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9a55f-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="9a55f-112">Bug fixes</span></span>

<span data-ttu-id="9a55f-113">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="9a55f-113">**Time and Expense**</span></span>

<span data-ttu-id="9a55f-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="9a55f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9a55f-115">Det oppstår en feil når du oppretter og lagrer en tidsoppføring på **Hurtigoppretting**-siden hvis **Rolle**-feltet er fjernet.</span><span class="sxs-lookup"><span data-stu-id="9a55f-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="9a55f-116">Tidsregistrering-filteret bruker feil filteroperator.</span><span class="sxs-lookup"><span data-stu-id="9a55f-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="9a55f-117">Kopierte timeregistreringer vises ikke automatisk når du velger **Kopier uke** på tidsregistreringskontrollen.</span><span class="sxs-lookup"><span data-stu-id="9a55f-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="9a55f-118">**Ressursbehandling**</span><span class="sxs-lookup"><span data-stu-id="9a55f-118">**Resource Management**</span></span>

<span data-ttu-id="9a55f-119">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="9a55f-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="9a55f-120">Når du utvider en bestilling, er bestillingsstatusen som er tilordnet den forpliktende bestillingen, feil.</span><span class="sxs-lookup"><span data-stu-id="9a55f-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="9a55f-121">Hvis du utvider en bestilling, respekteres bestillingsstatusen definert som **Utført** i metadataene for bestillingsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="9a55f-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="9a55f-122">Når en gyldig bestillingsstatus ikke er angitt, er ikke feilmeldingen riktig lokalisert.</span><span class="sxs-lookup"><span data-stu-id="9a55f-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="9a55f-123">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="9a55f-123">**Project Management**</span></span>

<span data-ttu-id="9a55f-124">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="9a55f-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="9a55f-125">Prosjekter kan ikke opprettes i én valuta og inkludere relaterte oppgaver i en annen valuta.</span><span class="sxs-lookup"><span data-stu-id="9a55f-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="9a55f-126">**Salg**</span><span class="sxs-lookup"><span data-stu-id="9a55f-126">**Sales**</span></span>

<span data-ttu-id="9a55f-127">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="9a55f-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="9a55f-128">Når en prisliste kopieres, oppdateres ikke prisene.</span><span class="sxs-lookup"><span data-stu-id="9a55f-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="9a55f-129">Lukking av et tilbud som vunnet mislykkes når kostnadsdetaljene har en verdi for opprinnelse.</span><span class="sxs-lookup"><span data-stu-id="9a55f-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="9a55f-130">I enheten **Prosjektoppgave** har **Estimert kostnad** fått endret navnet til **Planlagt kostnad (standardvaluta)**.</span><span class="sxs-lookup"><span data-stu-id="9a55f-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="9a55f-131">Det genereres et nullreferanseunntak når fakturaer opprettes eller slettes.</span><span class="sxs-lookup"><span data-stu-id="9a55f-131">A null reference exception is generated when invoices are created or deleted.</span></span>
