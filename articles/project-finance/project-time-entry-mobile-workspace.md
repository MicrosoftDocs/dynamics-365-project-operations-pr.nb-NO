---
title: Mobilt arbeidsområde for tidsoppføring for prosjekt
description: Dette emnet gir informasjon om det mobile arbeidsområdet for tidsoppføring for prosjekt. Dette arbeidsområdet gjør det mulig for brukere å skrive inn og spare tid på et prosjekt ved hjelp av den mobile enheten.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754128"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="f66f1-104">Mobilt arbeidsområde for tidsoppføring for prosjekt</span><span class="sxs-lookup"><span data-stu-id="f66f1-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f66f1-105">Dette emnet gir informasjon om det mobile arbeidsområdet for **Tidsoppføring for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="f66f1-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="f66f1-106">Dette arbeidsområdet gjør det mulig for brukere å skrive inn og spare tid på et prosjekt ved hjelp av den mobile enheten.</span><span class="sxs-lookup"><span data-stu-id="f66f1-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="f66f1-107">Dette mobile arbeidsområdet er ment å skulle brukes med en Dynamics 365 Unified OPS-mobilapp.</span><span class="sxs-lookup"><span data-stu-id="f66f1-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="f66f1-108">Oversikt</span><span class="sxs-lookup"><span data-stu-id="f66f1-108">Overview</span></span>
<span data-ttu-id="f66f1-109">Som en del av det daglige arbeidet er prosjektressurser ofte på stedet eller på reise.</span><span class="sxs-lookup"><span data-stu-id="f66f1-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="f66f1-110">Med det mobile arbeidsområdet **Tidsoppføring for prosjekt** kan brukere angi fakturerbar eller ikke-fakturerbar tid mot et prosjekt på den mobile enheten de velger.</span><span class="sxs-lookup"><span data-stu-id="f66f1-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="f66f1-111">Derfor kan prosjektressurser registrere tidsoppføringer når som helst og hvor som helst.</span><span class="sxs-lookup"><span data-stu-id="f66f1-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="f66f1-112">De kan også vise tidsoppføringer som allerede er registrert.</span><span class="sxs-lookup"><span data-stu-id="f66f1-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="f66f1-113">I det mobile arbeidsområdet **Tidsoppføring for prosjekt** kan brukere utføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="f66f1-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="f66f1-114">For en valgt dato angir du hvor mange timer du har brukt på en bestemt oppgave.</span><span class="sxs-lookup"><span data-stu-id="f66f1-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="f66f1-115">Søk etter prosjektnavn eller kunde for å finne prosjektet du vil registrere tid for.</span><span class="sxs-lookup"><span data-stu-id="f66f1-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="f66f1-116">Angi kategorien og aktiviteten for tiden du brukte.</span><span class="sxs-lookup"><span data-stu-id="f66f1-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="f66f1-117">Registrere tiden som fakturerbar eller ikke-fakturerbar for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="f66f1-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="f66f1-118">Angi eventuelt eksterne eller interne kommentarer.</span><span class="sxs-lookup"><span data-stu-id="f66f1-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f66f1-119">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="f66f1-119">Prerequisites</span></span>
<span data-ttu-id="f66f1-120">Forhåndskravene varierer basert på versjonen av Microsoft Dynamics 365 som er distribuert for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="f66f1-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="f66f1-121">Forhåndskrav hvis du bruker Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="f66f1-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="f66f1-122">Hvis Finance er distribuert for organisasjonen, må systemetadministrator publisere det mobile arbeidsområdet **Tidsoppføring for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="f66f1-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="f66f1-123">Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="f66f1-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="f66f1-124">Forhåndskrav hvis du bruker versjon 1611 med plattformoppdatering 3 eller senere</span><span class="sxs-lookup"><span data-stu-id="f66f1-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="f66f1-125">Hvis versjon 1611 med plattformoppdatering 3 eller senere er distribuert for organisasjonen, må følgende forhåndskrav fullføres av systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="f66f1-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f66f1-126">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="f66f1-126">Prerequisite</span></span></th>
<th><span data-ttu-id="f66f1-127">Rolle</span><span class="sxs-lookup"><span data-stu-id="f66f1-127">Role</span></span></th>
<th><span data-ttu-id="f66f1-128">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f66f1-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="f66f1-129">Implementer KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="f66f1-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="f66f1-130">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="f66f1-130">System administrator</span></span></td>
<td><span data-ttu-id="f66f1-131">KB 4018050 er en X++-oppdatering eller hurtigreparasjon for metadata som inneholder det mobile arbeidsområdet <strong>Tidsoppføring for prosjekt</strong>.</span><span class="sxs-lookup"><span data-stu-id="f66f1-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="f66f1-132">For å implementere KB 4018050 må systemadministrator følge fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="f66f1-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="f66f1-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="f66f1-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="f66f1-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installer hurtigreparasjon for metadata</a>.</span><span class="sxs-lookup"><span data-stu-id="f66f1-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="f66f1-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opprett en distribuerbar pakke</a> som inneholder <strong>ApplicationSuite</strong> - og <strong>ProjectMobile</strong> -modellene, og last deretter opp den distribuerbare pakken til LCS.</span><span class="sxs-lookup"><span data-stu-id="f66f1-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="f66f1-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Ta i bruk den distribuerbare pakken</a>.</span><span class="sxs-lookup"><span data-stu-id="f66f1-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f66f1-137">Publiser arbeidsområdet for <strong>Tidsoppføring for prosjekt</strong>.</span><span class="sxs-lookup"><span data-stu-id="f66f1-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="f66f1-138">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="f66f1-138">System administrator</span></span></td>
<td><span data-ttu-id="f66f1-139">Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a>.</span><span class="sxs-lookup"><span data-stu-id="f66f1-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="f66f1-140">Laste ned og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="f66f1-140">Download and install the mobile app</span></span>

<span data-ttu-id="f66f1-141">Last ned og installer Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="f66f1-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="f66f1-142">For Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="f66f1-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="f66f1-143">For iPhone</span><span class="sxs-lookup"><span data-stu-id="f66f1-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="f66f1-144">Logge på mobilappen</span><span class="sxs-lookup"><span data-stu-id="f66f1-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="f66f1-145">Start appen på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="f66f1-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="f66f1-146">Angi Dynamics 365-URL-en din.</span><span class="sxs-lookup"><span data-stu-id="f66f1-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="f66f1-147">Første gang du logger deg på, blir du bedt om å oppgi brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="f66f1-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="f66f1-148">Angi legitimasjonen din.</span><span class="sxs-lookup"><span data-stu-id="f66f1-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="f66f1-149">Etter at du har logget på, vises de tilgjengelige arbeidsområdene for firmaet.</span><span class="sxs-lookup"><span data-stu-id="f66f1-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="f66f1-150">Vær oppmerksom på at hvis systemetadministrator publiserer et nytt arbeidsområde senere, må du oppdatere listen over mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="f66f1-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="f66f1-151">[![Dra for å oppdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="f66f1-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="f66f1-152">Registrer tid ved hjelp av det mobile arbeidsområdet Tidsoppføring for prosjekt</span><span class="sxs-lookup"><span data-stu-id="f66f1-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="f66f1-153">På den mobile enheten velger du arbeidsområdet **Tidsoppføring for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="f66f1-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="f66f1-154">Velg **Tidsoppføring**.</span><span class="sxs-lookup"><span data-stu-id="f66f1-154">Select **Time entry**.</span></span> <span data-ttu-id="f66f1-155">Kalenderdatoene for inneværende uke vises.</span><span class="sxs-lookup"><span data-stu-id="f66f1-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="f66f1-156">For en valgt dato velger du **Handlinger** &gt; **Ny oppføring**.</span><span class="sxs-lookup"><span data-stu-id="f66f1-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="f66f1-157">Angi antall timer du vil registrere.</span><span class="sxs-lookup"><span data-stu-id="f66f1-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="f66f1-158">Velg prosjektet for tidsoppføringen.</span><span class="sxs-lookup"><span data-stu-id="f66f1-158">Select the project for the time entry.</span></span> <span data-ttu-id="f66f1-159">En liste viser prosjektene som lastes inn i appen for bruk i frakoblet modus.</span><span class="sxs-lookup"><span data-stu-id="f66f1-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="f66f1-160">Som standard lastes 50 elementer inn, men en utvikler kan endre dette antallet.</span><span class="sxs-lookup"><span data-stu-id="f66f1-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f66f1-161">Hvis du vil ha mer informasjon, kan du se [Mobile-plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)</span><span class="sxs-lookup"><span data-stu-id="f66f1-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="f66f1-162">Hvis prosjektet ikke finnes i listen, velger du **Søk**.</span><span class="sxs-lookup"><span data-stu-id="f66f1-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="f66f1-163">Søk etter navn, eller bytt for å søke etter prosjektnavn eller kunde.</span><span class="sxs-lookup"><span data-stu-id="f66f1-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="f66f1-164">Velg en kategori.</span><span class="sxs-lookup"><span data-stu-id="f66f1-164">Select a category.</span></span> <span data-ttu-id="f66f1-165">En liste viser kategorier som lastes inn i appen for bruk i frakoblet modus.</span><span class="sxs-lookup"><span data-stu-id="f66f1-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="f66f1-166">Som standard lastes 50 elementer inn, men en utvikler kan endre dette antallet.</span><span class="sxs-lookup"><span data-stu-id="f66f1-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f66f1-167">Hvis du vil ha mer informasjon, kan du se [Mobile-plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)</span><span class="sxs-lookup"><span data-stu-id="f66f1-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="f66f1-168">Hvis kategorien din ikke finnes i listen, velger du **Søk**.</span><span class="sxs-lookup"><span data-stu-id="f66f1-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="f66f1-169">Søk etter kategori, eller bytt for å søke etter kategorinavn.</span><span class="sxs-lookup"><span data-stu-id="f66f1-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="f66f1-170">Velg en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="f66f1-170">Select an activity.</span></span> <span data-ttu-id="f66f1-171">En liste viser aktiviteter som lastes inn i appen for bruk i frakoblet modus.</span><span class="sxs-lookup"><span data-stu-id="f66f1-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="f66f1-172">Som standard lastes 50 elementer inn, men en utvikler kan endre dette antallet.</span><span class="sxs-lookup"><span data-stu-id="f66f1-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f66f1-173">Hvis du vil ha mer informasjon, kan du se [Mobile-plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)</span><span class="sxs-lookup"><span data-stu-id="f66f1-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="f66f1-174">Hvis aktiviteten din ikke finnes i listen, velger du **Søk**.</span><span class="sxs-lookup"><span data-stu-id="f66f1-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="f66f1-175">Søk etter aktivitetsnummer, eller bytt for å søke etter formål.</span><span class="sxs-lookup"><span data-stu-id="f66f1-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="f66f1-176">Velg linjeegenskapen.</span><span class="sxs-lookup"><span data-stu-id="f66f1-176">Select the line property.</span></span>
12. <span data-ttu-id="f66f1-177">Valgfritt: Angi eventuelt eksterne og interne kommentarer.</span><span class="sxs-lookup"><span data-stu-id="f66f1-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="f66f1-178">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="f66f1-178">Select **Done**.</span></span>
