---
title: Hva er nytt eller endret i Project Service Automation Update Release 22, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 22, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 5694aa27afe7618cfca6b27444393634a9686600
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006568"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="c30cd-103">Project Service Automation, Update Release 22, V3</span><span class="sxs-lookup"><span data-stu-id="c30cd-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c30cd-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c30cd-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c30cd-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="c30cd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c30cd-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c30cd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c30cd-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="c30cd-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c30cd-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c30cd-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c30cd-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 22.</span><span class="sxs-lookup"><span data-stu-id="c30cd-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="c30cd-110">Denne versjonen har et build-nummer på V 3.10.33.48 og er generelt tilgjengelig via en egen oppdatering i juni 2020.</span><span class="sxs-lookup"><span data-stu-id="c30cd-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="c30cd-111">Update Release 22</span><span class="sxs-lookup"><span data-stu-id="c30cd-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c30cd-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="c30cd-112">Bug fixes</span></span>



<span data-ttu-id="c30cd-113">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="c30cd-113">**Time and Expense**</span></span>

<span data-ttu-id="c30cd-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="c30cd-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c30cd-115">**Tidsoppføringer** legges ikke til automatisk i tidsplanen for tidsoppføringer etter importen.</span><span class="sxs-lookup"><span data-stu-id="c30cd-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="c30cd-116">Datovelgerrutenettet for **Tidsoppføring** gjenkjenner ikke brukerens regionale innstillinger.</span><span class="sxs-lookup"><span data-stu-id="c30cd-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="c30cd-117">**Ressursbehandling**</span><span class="sxs-lookup"><span data-stu-id="c30cd-117">**Resource Management**</span></span>

<span data-ttu-id="c30cd-118">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="c30cd-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="c30cd-119">I manuell modus gjenkjennes ikke endringer i **Ressurstilordning**-konturer ved generering av **Ressurskrav**.</span><span class="sxs-lookup"><span data-stu-id="c30cd-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="c30cd-120">**Ressursforespørsler** støtter ikke egendefinerte forespørselsstatuser.</span><span class="sxs-lookup"><span data-stu-id="c30cd-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="c30cd-121">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="c30cd-121">**Project Management**</span></span>

<span data-ttu-id="c30cd-122">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="c30cd-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="c30cd-123">Bruk av dobbeltklikking på EstimateGridControl analyserer ikke nederlandske formatnumre riktig.</span><span class="sxs-lookup"><span data-stu-id="c30cd-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="c30cd-124">Tildelte timer oppdateres ikke riktig når tilordninger endres ved hjelp av Microsoft Project-klienttilleggsprogrammet for stasjonære datamaskiner.</span><span class="sxs-lookup"><span data-stu-id="c30cd-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="c30cd-125">Rutenettet for Prosjektsporing og Estimater viser feil salgsvalutakode når kontraktvaluta er forskjellig fra kundevalutaen, og organisasjonen er konfigurert til å vise valutakoder i stedet for valutasymboler.</span><span class="sxs-lookup"><span data-stu-id="c30cd-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="c30cd-126">Sluttdatoen for et teammedlem vil legge til én dag hvis tidsplanen for arbeidstimer er 24 timer per dag.</span><span class="sxs-lookup"><span data-stu-id="c30cd-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="c30cd-127">Når du legger til en transaksjonskategori i en oppgave i prosjektplanen, utløses ikke automatisk lagring.</span><span class="sxs-lookup"><span data-stu-id="c30cd-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="c30cd-128">Følgende feil vises når du legger til et teammedlem i prosjektmalen: "Ressurskrav kan ikke knyttes til prosjektmaler".</span><span class="sxs-lookup"><span data-stu-id="c30cd-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="c30cd-129">Skript på båndregel "msdyn.Approval.CanApproveOrReject" viser en tidsavbruddsfeil.</span><span class="sxs-lookup"><span data-stu-id="c30cd-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="c30cd-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="c30cd-130">**Sales**</span></span>

<span data-ttu-id="c30cd-131">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="c30cd-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="c30cd-132">Valideringsfeilmelding vises ikke når en kostprisliste er valgt i prislisteoppslag i skjema/enhet for ny prosjektprisliste for tilbud.</span><span class="sxs-lookup"><span data-stu-id="c30cd-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="c30cd-133">Hvis du lukker tilbudet som vunnet, går det ikke videre til den opprettede kontrakten hvis en BPF som er knyttet til tilbudet, er i det siste trinnet.</span><span class="sxs-lookup"><span data-stu-id="c30cd-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="c30cd-134">Tilbakeføring av **Ufakturert salg** er koblet til opprinnelig kostnad når en tidsoppføring blir tilbakekalt.</span><span class="sxs-lookup"><span data-stu-id="c30cd-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="c30cd-135">Når du har valgt **Bekreft**-knappen, endres ikke fakturastatusen til **Bekreftet** med mindre fakturaen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="c30cd-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]