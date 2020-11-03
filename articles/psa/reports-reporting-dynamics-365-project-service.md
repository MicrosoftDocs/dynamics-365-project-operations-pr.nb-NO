---
title: Hjemmeside for rapportering
description: Dette emnet inneholder informasjon om rapportering i Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 30411818bdc1b370a71148cf79f743413167dab2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081847"
---
# <a name="reporting-home-page"></a><span data-ttu-id="c1770-103">Hjemmeside for rapportering</span><span class="sxs-lookup"><span data-stu-id="c1770-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c1770-104">Microsoft Dynamics 365 Project Service Automation lar prosektbaserte organisasjoner effektivt administrere driften av virksomheten.</span><span class="sxs-lookup"><span data-stu-id="c1770-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="c1770-105">I et hvilket som helst prosjekt må teammedlemmer administrere salgsmuligheten, tilbudet og planlegge arbeidet, tildele ressurser til prosjektene, administrere arbeidet i henhold til planen, fakturere arbeidet og deretter fullføre prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c1770-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="c1770-106">Muligheten til å rapportere om operasjoner er nøkkelen for å avgjøre tilstanden til organisasjonen og å utføre eventuelle korrigerende handlinger som kreves.</span><span class="sxs-lookup"><span data-stu-id="c1770-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="c1770-107">PSA bruker Microsoft Dynamics 365-rapporteringsmetoder og -teknologi for all rapportering.</span><span class="sxs-lookup"><span data-stu-id="c1770-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="c1770-108">Hvis du vil ha mer informasjon om alternativene for rapportering, kan du se [Veiledning for rapportskriving for Dynamics 365 Customer Engagement (on-premises), versjon 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="c1770-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="c1770-109">Rapportveiviser</span><span class="sxs-lookup"><span data-stu-id="c1770-109">Report Wizard</span></span>

<span data-ttu-id="c1770-110">Ved hjelp av rapportveiviseren kan ikke-utviklere opprette enkle rapporter.</span><span class="sxs-lookup"><span data-stu-id="c1770-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="c1770-111">Fordi appen er bygd på en eksisterende plattform, er opplevelsen den samme som opplevelsen som dokumenteres i [Opprette eller redigere en rapport ved hjelp av rapportveiviseren](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="c1770-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="c1770-112">Du må imidlertid bruke de Project Service Automation-spesifikke enhetene.</span><span class="sxs-lookup"><span data-stu-id="c1770-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="c1770-113">Tilpassede rapporter for SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="c1770-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="c1770-114">Hvis virksomheten krever en bestemt rapport som ikke kan opprettes ved hjelp av rapportveiviseren, kan du opprette en egendefinert rapport.</span><span class="sxs-lookup"><span data-stu-id="c1770-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="c1770-115">Microsoft Visual Studio må være installert sammen med de riktige Microsoft SQL Server Data Tools og rapportredigeringsutvidelser.</span><span class="sxs-lookup"><span data-stu-id="c1770-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="c1770-116">Hvis du vil ha mer informasjon om verktøy og versjoner, kan du se [Rapportskrivingsmiljø ved hjelp av SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="c1770-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="c1770-117">Hvis du vil ha informasjon om hvordan du oppretter en egendefinert rapport, kan du se [Opprette en ny rapport ved hjelp av SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="c1770-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="c1770-118">Power BI Insights-apper</span><span class="sxs-lookup"><span data-stu-id="c1770-118">Power BI insights apps</span></span>

<span data-ttu-id="c1770-119">Microsoft Power BI og Dynamics 365 gir deg en effektiv måte å arbeide med dataene på, i form av Insights-apper.</span><span class="sxs-lookup"><span data-stu-id="c1770-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="c1770-120">Hvis du vil ha informasjon om tilgjengeligheten til Insights-apper, kan du se [siden med Power BI Insights-apper](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="c1770-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="c1770-121">Ytterligere ressurser</span><span class="sxs-lookup"><span data-stu-id="c1770-121">Additional resources</span></span>
<span data-ttu-id="c1770-122">Du finner mer informasjon om rapportering i PSA i følgende emner:</span><span class="sxs-lookup"><span data-stu-id="c1770-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="c1770-123">Arbeide med datamodell for Project Service</span><span class="sxs-lookup"><span data-stu-id="c1770-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="c1770-124">Instrumentbord</span><span class="sxs-lookup"><span data-stu-id="c1770-124">Dashboards</span></span>](reports-dashboards.md)

