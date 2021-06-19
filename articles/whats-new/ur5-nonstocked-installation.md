---
title: Oppdatere Project Operations i Økonomi-miljøet
description: Dette emnet gir informasjon om hvordan du oppdaterer Project Operations i Dynamics 365 Finance-miljøet.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011068"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="2bb53-103">Oppdatere Project Operations i Økonomi-miljøet</span><span class="sxs-lookup"><span data-stu-id="2bb53-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="2bb53-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="2bb53-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="2bb53-105">Dette emnet gir informasjon om hvordan du oppdaterer Dynamics 365 Project Operations i Dynamics 365 Finance-miljøet.</span><span class="sxs-lookup"><span data-stu-id="2bb53-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="2bb53-106">Det er tre prosedyrer som kreves for å oppdatere Project Operations til Update 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="2bb53-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="2bb53-107">Importere pakken til forhåndsvisningsprosjektet</span><span class="sxs-lookup"><span data-stu-id="2bb53-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="2bb53-108">Ta i bruk oppdateringen</span><span class="sxs-lookup"><span data-stu-id="2bb53-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="2bb53-109">Oppdatere Dataverse-miljøet</span><span class="sxs-lookup"><span data-stu-id="2bb53-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="2bb53-110">Importere pakken til LCS-prosjektet</span><span class="sxs-lookup"><span data-stu-id="2bb53-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="2bb53-111">Logg på [Lifecycle Services (LCS)](https://lcs.dynamics.com/) som prosjekteier eller miljøleder.</span><span class="sxs-lookup"><span data-stu-id="2bb53-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="2bb53-112">Fra listen over prosjekter velger du LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="2bb53-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="2bb53-113">På siden **Prosjekt** i gruppen **Miljøer** åpner du miljøet du vil oppdatere.</span><span class="sxs-lookup"><span data-stu-id="2bb53-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="2bb53-114">Bekreft at miljøet kjører.</span><span class="sxs-lookup"><span data-stu-id="2bb53-114">Verify that the environment is running.</span></span> <span data-ttu-id="2bb53-115">Hvis det ikke er startet, starter du miljøet.</span><span class="sxs-lookup"><span data-stu-id="2bb53-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="2bb53-116">I delen **Ny versjon** under **Tilgjengelige oppdateringer** velger du **Vis oppdatering** for 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="2bb53-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Vis oppdatering, knapp](media/view-update.png)

6. <span data-ttu-id="2bb53-118">På siden **Binære oppdateringer** velger du **Lagre pakke**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="2bb53-119">På siden **Se gjennom og lagre oppdateringer** velger du **Lagre pakke**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="2bb53-120">I ruten **Lagre pakke i aktivabibliotek** som åpnes, angir du pakkenavnet og velger deretter **Lagre pakke**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="2bb53-121">Når LCS er ferdig med å lagre pakken, aktiveres **Ferdig**-knappen.</span><span class="sxs-lookup"><span data-stu-id="2bb53-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="2bb53-122">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-122">Select **Done**.</span></span> <span data-ttu-id="2bb53-123">LCS verifiserer pakken.</span><span class="sxs-lookup"><span data-stu-id="2bb53-123">LCS will verify the package.</span></span> <span data-ttu-id="2bb53-124">Verifisering kan ta noen minutter eller opptil én time.</span><span class="sxs-lookup"><span data-stu-id="2bb53-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="2bb53-125">Ta i bruke pakkeoppdateringen</span><span class="sxs-lookup"><span data-stu-id="2bb53-125">Apply the package update</span></span>

1. <span data-ttu-id="2bb53-126">På siden **Miljødetaljer** i LCS velger du **Oppretthold** > **Bruk oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="2bb53-127">Velg pakken du lagret tidligere, fra listen, og velg deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="2bb53-128">Velg **Ja** for å bekrefte at du vil distribuere pakken.</span><span class="sxs-lookup"><span data-stu-id="2bb53-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Dialogboksen Bekreft distribusjon av pakke](media/confirm-package-deployment.png)

4. <span data-ttu-id="2bb53-130">Velg **Ja** for å bekrefte at du vil oppdatere appen.</span><span class="sxs-lookup"><span data-stu-id="2bb53-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Dialogboksen Bekreft oppdatering av app](media/confirm-application-update.png)

<span data-ttu-id="2bb53-132">Distribusjonen og appoppdateringen starter.</span><span class="sxs-lookup"><span data-stu-id="2bb53-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="2bb53-133">På siden **Miljødetaljer** blir miljøstatusen oppdatert til **Betjener** i hjørnet øverst til høyre.</span><span class="sxs-lookup"><span data-stu-id="2bb53-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="2bb53-134">Oppdateringen blir fullført på ca. to timer.</span><span class="sxs-lookup"><span data-stu-id="2bb53-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="2bb53-135">Informasjonen om apputgivelsen oppdateres til **Microsoft Dynamics 365 for Finance and Operations 10.0.15)**, og miljøstatusen oppdateres til **Distribuert**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="2bb53-136">Oppdatere Dataverse-miljøet</span><span class="sxs-lookup"><span data-stu-id="2bb53-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="2bb53-137">Logg på [Power Platform-administrasjonssenteret](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="2bb53-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="2bb53-138">I listen finner og åpner du miljøet du brukte til å installere Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2bb53-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="2bb53-139">På siden **Miljøer** velger du **Ressurs** > **Dynamics 365-apper**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="2bb53-140">I listen finner du **Microsoft Dynamics 365 Project Operations**, og i kolonnen **Status** velger du **Oppdatering er tilgjengelig**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="2bb53-141">Merk av for **Jeg godtar servicebetingelsene**, og velg deretter **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="2bb53-142">Den nyeste versjonen av løsningen blir installert.</span><span class="sxs-lookup"><span data-stu-id="2bb53-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="2bb53-143">Når installasjonen er fullført, har du versjonsnummeret 4.5.0.134 installert.</span><span class="sxs-lookup"><span data-stu-id="2bb53-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="2bb53-144">Konfigurere nye funksjoner</span><span class="sxs-lookup"><span data-stu-id="2bb53-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="2bb53-145">Aktivere tilordning for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="2bb53-145">Enable dual-write mapping</span></span>

<span data-ttu-id="2bb53-146">Når du har fullført oppdateringen av Økonomi- og Dataverse-miljøene, kan du aktivere de nødvendige tilordningene for dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="2bb53-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="2bb53-147">Fullfør følgende prosedyrer for å aktivere tilordninger for dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="2bb53-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="2bb53-148">Oppdatere sikkerhetsinnstillinger i Customer Engagement-miljøet</span><span class="sxs-lookup"><span data-stu-id="2bb53-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="2bb53-149">Oppdatere dataenheter</span><span class="sxs-lookup"><span data-stu-id="2bb53-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="2bb53-150">Oppdatere og kjøre tilordninger for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="2bb53-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="2bb53-151">Oppdatere sikkerhetsinnstillinger i Dataverse-miljøet</span><span class="sxs-lookup"><span data-stu-id="2bb53-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="2bb53-152">Følgende oppdateringer av sikkerhetsrettighetene for enheter nedenfor kreves som en del av oppdateringen til UR5.</span><span class="sxs-lookup"><span data-stu-id="2bb53-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="2bb53-153">I Dataverse-miljøet går du til **Innstillinger**, og i gruppen **System** velger du **Sikkerhet**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Innstillinger for Dataverse-miljø](media/Picture21.png)

2. <span data-ttu-id="2bb53-155">Velg **Sikkerhetsroller**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="2bb53-156">Fra listen over roller velger du **appbruker med dobbeltskriving** og velger kategorien **Egendefinerte enheter**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="2bb53-157">Kontroller at rollen har tillatelsene **Lese** og **Tilføye i** for følgende:</span><span class="sxs-lookup"><span data-stu-id="2bb53-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="2bb53-158">**Valutakurstype**</span><span class="sxs-lookup"><span data-stu-id="2bb53-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="2bb53-159">**Plan over kontoer**</span><span class="sxs-lookup"><span data-stu-id="2bb53-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="2bb53-160">**Regnskapskalender**</span><span class="sxs-lookup"><span data-stu-id="2bb53-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="2bb53-161">**Finans**</span><span class="sxs-lookup"><span data-stu-id="2bb53-161">**Ledger**</span></span>

5. <span data-ttu-id="2bb53-162">Etter at sikkerhetsrollen er oppdatert, går du til **Innstillinger** > **Sikkerhet** > **Team**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="2bb53-163">Kontroller at rollen **appbruker med dobbeltskriving** er brukt på teamet.</span><span class="sxs-lookup"><span data-stu-id="2bb53-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="2bb53-164">Oppdatere dataenheter fra oppdateringen</span><span class="sxs-lookup"><span data-stu-id="2bb53-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="2bb53-165">I økonomimiljøet åpner du arbeidsområdet **Databehandling**, og deretter åpner du siden **Rammeverkparametre**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="2bb53-166">I kategorien **Enhetsinnstillinger** velger du **Oppdater enhetsliste**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="2bb53-167">Velg **Lukk** for å bekrefte oppdatering av enheten.</span><span class="sxs-lookup"><span data-stu-id="2bb53-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="2bb53-168">Det tar omtrent 20 minutter å fullføre denne prosessen.</span><span class="sxs-lookup"><span data-stu-id="2bb53-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="2bb53-169">Du blir varslet når oppdateringen er fullført.</span><span class="sxs-lookup"><span data-stu-id="2bb53-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="2bb53-170">Oppdatere tilordninger for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="2bb53-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="2bb53-171">I arbeidsområdet **Databehandling** velger du **Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="2bb53-172">Velg **Bruk løsninger**, velg begge løsningene fra listen, og velg deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="2bb53-173">På siden **Dobbel skriving** velger du følgende tabelltilordninger, og deretter velger du **Stopp**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="2bb53-174">**Faktiske verdier for Project Operations-integrering (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="2bb53-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="2bb53-175">**Prosjektutgiftskategorier for Project Operations-integrering (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="2bb53-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="2bb53-176">**Faktiske verdier for enhet for prosjektutgiftsrapport for Project Operations-integrering (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="2bb53-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="2bb53-177">På siden **Tabelltilordningsversjon** bruker du en ny versjon av tilordningen for hver av de tre enhetene.</span><span class="sxs-lookup"><span data-stu-id="2bb53-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="2bb53-178">På siden **Dobbel skriving** velger du Kjør for å starte tilordningene på nytt.</span><span class="sxs-lookup"><span data-stu-id="2bb53-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="2bb53-179">Fra listen over tilordninger velger du tilordningen **Finans (msdyn_ledgers)** med alle dens krav, og deretter merker du av for **Første synkronisering**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="2bb53-180">I feltet **Hovedoppføring for første synkronisering** velger du **Finance and Operations-apper** og velger deretter **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Synkronisering av finanstilordning](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]