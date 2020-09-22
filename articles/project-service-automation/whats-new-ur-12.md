---
title: Hva er nytt i Project Service Automation Update Release 12, V3
description: Dette emnet inneholder informasjon om hva som er nytt i Project Service Automation Update Release 12, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754116"
---
# <a name="project-service-automation-v3-update-release-12"></a><span data-ttu-id="c7478-103">Project Service Automation V3, Update Release 12</span><span class="sxs-lookup"><span data-stu-id="c7478-103">Project Service Automation V3, Update Release 12</span></span>
<span data-ttu-id="c7478-104">Vi er glade for å annonsere den nyeste oppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet.</span><span class="sxs-lookup"><span data-stu-id="c7478-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="c7478-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="c7478-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c7478-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c7478-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c7478-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="c7478-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="c7478-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c7478-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c7478-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 12.</span><span class="sxs-lookup"><span data-stu-id="c7478-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="c7478-110">Denne versjonen har buildnummer V3.10.2.34 og er vanligvis tilgjengelig via en egen oppdatering i oktober 2019.</span><span class="sxs-lookup"><span data-stu-id="c7478-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="c7478-111">Update Release 12</span><span class="sxs-lookup"><span data-stu-id="c7478-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c7478-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="c7478-112">Bug fixes</span></span>

- <span data-ttu-id="c7478-113">Tid og utgift</span><span class="sxs-lookup"><span data-stu-id="c7478-113">Time and Expense</span></span>

    - <span data-ttu-id="c7478-114">Fikset: Timeregistreringsfeilmeldinger er oppdatert med mer relevant kontekst.</span><span class="sxs-lookup"><span data-stu-id="c7478-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="c7478-115">Fikset: Rutenett for tidsoppføring og tidsplan viser riktig loddrett rullefelt når det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="c7478-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="c7478-116">Fikset: Innsendte utgifts- og tidsoppføringer kan godkjennes.</span><span class="sxs-lookup"><span data-stu-id="c7478-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="c7478-117">Fikset: Dialogmelding for bekreftelse av annullering av bekreftelse er korrigert for å vise statusen til godkjenningen når den endres fra **Godkjent** til **Sendt**.</span><span class="sxs-lookup"><span data-stu-id="c7478-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="c7478-118">Fikset: Feltene **Pris**, **Enhet** og **Antall** er nå låst på utgiftsoppføringen etter at den er godkjent.</span><span class="sxs-lookup"><span data-stu-id="c7478-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="c7478-119">Prosjektledelse</span><span class="sxs-lookup"><span data-stu-id="c7478-119">Project Management</span></span>

    - <span data-ttu-id="c7478-120">Fikset: **Ny**-handling på hovedskjemaet for **Teammedlem** er fjernet.</span><span class="sxs-lookup"><span data-stu-id="c7478-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="c7478-121">Fikset: Ressurstilordningene er oppdatert for å ta høyde for unøyaktige avrundingsfeil, noe som fører til endring av sluttdatoen for oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c7478-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="c7478-122">Fikset: I oppgaverutenettet blir relevante feil på serversiden vist for brukeren.</span><span class="sxs-lookup"><span data-stu-id="c7478-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="c7478-123">Fikset: Navnet på teammedlemmet gjengis nå i personvelgeren for oppgave i stedet for posisjonsnavnet.</span><span class="sxs-lookup"><span data-stu-id="c7478-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="c7478-124">Ressursbehandling</span><span class="sxs-lookup"><span data-stu-id="c7478-124">Resource Management</span></span>

    - <span data-ttu-id="c7478-125">Fikset: Detaljer for ressurskrav for prosjekter som er opprettet fra en mal, bruker nå prosjektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="c7478-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="c7478-126">Fikset: Kompetanse og ferdigheter går nå som standard fra rollehoveddata til ressurskravene som er opprettet for rollen.</span><span class="sxs-lookup"><span data-stu-id="c7478-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="c7478-127">Sales</span><span class="sxs-lookup"><span data-stu-id="c7478-127">Sales</span></span>

    - <span data-ttu-id="c7478-128">Fikset: Duplikate objekt-IDer ble funnet i hovedskjemaet for **Kontrakt**.</span><span class="sxs-lookup"><span data-stu-id="c7478-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="c7478-129">Fikset: Logikken er oppdatert slik at kategorien **Tilbudsanalyse** blir synlig og viser metadataoppsettet for kategorien.</span><span class="sxs-lookup"><span data-stu-id="c7478-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="c7478-130">Fikset: Regnskapsdato på den faktiske oppføringen kommer nå fra datoen for tids-/utgiftsoppføring og ikke fra godkjenningsdatoen.</span><span class="sxs-lookup"><span data-stu-id="c7478-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
