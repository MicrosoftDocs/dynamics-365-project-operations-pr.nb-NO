---
title: Hva er nytt eller endret i Project Service Automation Update Release 13, V3
description: Dette emnet inneholder informasjon om hva som er nytt i Project Service Automation Update Release 13, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: a4ebc2e6ca3f6be0a05a7240d762d7a8cf92d81b
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949466"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="a1b70-103">Project Service Automation, Update Release 13, V3</span><span class="sxs-lookup"><span data-stu-id="a1b70-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a1b70-104">Vi er glade for å annonsere den nyeste oppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet.</span><span class="sxs-lookup"><span data-stu-id="a1b70-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="a1b70-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="a1b70-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a1b70-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a1b70-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a1b70-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="a1b70-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="a1b70-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a1b70-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a1b70-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 13.</span><span class="sxs-lookup"><span data-stu-id="a1b70-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="a1b70-110">Denne versjonen har buildnummer V3.10.3.18 og er tilgjengelig i henhold til følgende tidsplan:</span><span class="sxs-lookup"><span data-stu-id="a1b70-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="a1b70-111">**Generell tilgjengelighet (egen oppdatering):** november 2019</span><span class="sxs-lookup"><span data-stu-id="a1b70-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="a1b70-112">**Automatisk oppdatering:** desember 2019</span><span class="sxs-lookup"><span data-stu-id="a1b70-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="a1b70-113">Update Release 13</span><span class="sxs-lookup"><span data-stu-id="a1b70-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="a1b70-114">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="a1b70-114">Bug fixes</span></span>

- <span data-ttu-id="a1b70-115">Tid og utgift</span><span class="sxs-lookup"><span data-stu-id="a1b70-115">Time and Expense</span></span>

     - <span data-ttu-id="a1b70-116">Fikset: Søkefunksjonaliteten på siden **Utgiftsgodkjenning** fungerer ikke når det søkes etter utgiftsformål.</span><span class="sxs-lookup"><span data-stu-id="a1b70-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="a1b70-117">Ressursbehandling</span><span class="sxs-lookup"><span data-stu-id="a1b70-117">Resource Management</span></span>

     - <span data-ttu-id="a1b70-118">Fikset: Tallene i avstemmingen er oppdatert til å være høyrejustert.</span><span class="sxs-lookup"><span data-stu-id="a1b70-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="a1b70-119">Fikset: Navngitte ressurser kan ikke tilordnes oppgaver via kategorien **Tidsplan**.</span><span class="sxs-lookup"><span data-stu-id="a1b70-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="a1b70-120">Prosjektledelse</span><span class="sxs-lookup"><span data-stu-id="a1b70-120">Project Management</span></span>

     - <span data-ttu-id="a1b70-121">Fikset: Nullreferanseunntak ved tilordning av teammedlemmer når **TransactionType** mangler oppsettinformasjon for **Enhet** og **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="a1b70-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="a1b70-122">Sales</span><span class="sxs-lookup"><span data-stu-id="a1b70-122">Sales</span></span>

     - <span data-ttu-id="a1b70-123">Fikset: Duplikate transaksjonstypeoppføringer returnerer en feil når rolleprisoppføringer opprettes.</span><span class="sxs-lookup"><span data-stu-id="a1b70-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="a1b70-124">Fikset: Ekstra knapper for **Ny salgsmulighet**, **Tilbud**, **Ordrelinjer** og **Legg til produkt** vises i kommandoer for salgsmuligheter, tilbud, ordreprodukter og prosjektbaserte linjedelrutenettet.</span><span class="sxs-lookup"><span data-stu-id="a1b70-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]