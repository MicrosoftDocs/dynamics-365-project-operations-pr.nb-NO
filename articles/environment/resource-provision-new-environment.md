---
title: Klargjør et nytt miljø
description: Dette emnet gir informasjon om hvordan du klargjør et nytt Project Operations-miljø.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ee9e4c31d1972e3a75ad214071b31527f0ca826
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950546"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="84843-103">Klargjør et nytt miljø</span><span class="sxs-lookup"><span data-stu-id="84843-103">Provision a new environment</span></span>

<span data-ttu-id="84843-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="84843-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="84843-105">Dette emnet gir informasjon om hvordan du klargjør et nytt Dynamics 365 Project Operations-miljø for ressursbaserte/ikke-lagerbaserte scenarioer.</span><span class="sxs-lookup"><span data-stu-id="84843-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="84843-106">Aktiver automatisk klargjøring av Project Operations i et LCS-prosjekt</span><span class="sxs-lookup"><span data-stu-id="84843-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="84843-107">Bruk fremgangsmåten nedenfor for å aktivere den automatiserte klargjøringsflyten for Project Operations for LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="84843-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="84843-108">Gå til [LCS](https://lcs.dynamics.com/v2), og velg flisen **Behandling av evalueringsfunksjonalitet**.</span><span class="sxs-lookup"><span data-stu-id="84843-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="84843-109">I listen **Evalueringsfunksjonalitet** velger du **Project Operations-funksjonen** og deretter **Evalueringsfunksjonalitet aktivert** for å aktivere Project Operations.</span><span class="sxs-lookup"><span data-stu-id="84843-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="84843-110">Dette trinnet utføres bare én gang per LCS-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="84843-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="84843-111">Klargjør et Project Operations-miljø</span><span class="sxs-lookup"><span data-stu-id="84843-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="84843-112">Åpne en ny Dynamics 365 Finance-distribusjon med et [demonstrasjonsmiljø](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) eller et [sandkasse-/produksjonsmiljø](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="84843-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="84843-113">Gå gjennom veiviseren for **klargjøring av miljø**.</span><span class="sxs-lookup"><span data-stu-id="84843-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="84843-114">Kontroller at den valgte programversjon er 10.0.13 eller høyere.</span><span class="sxs-lookup"><span data-stu-id="84843-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="84843-115">Du klargjør Project Operations ved å gå til **Avanserte innstillinger** og velge **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="84843-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="84843-116">Aktiver **Common Data Service-innstillingen** ved å velge **Ja**, og skriv deretter inn informasjon i de obligatoriske feltene:</span><span class="sxs-lookup"><span data-stu-id="84843-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="84843-117">Navn</span><span class="sxs-lookup"><span data-stu-id="84843-117">Name</span></span>
  - <span data-ttu-id="84843-118">Område</span><span class="sxs-lookup"><span data-stu-id="84843-118">Region</span></span>
  - <span data-ttu-id="84843-119">Language</span><span class="sxs-lookup"><span data-stu-id="84843-119">Language</span></span>
  - <span data-ttu-id="84843-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="84843-120">Currency</span></span>
 
5. <span data-ttu-id="84843-121">I feltet **Common Data Service-mal** velger du **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="84843-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="84843-122">Velg miljøtypen for distribusjonen din.</span><span class="sxs-lookup"><span data-stu-id="84843-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="84843-123">En abonnementsbasert prøveversjon gjør det mulig å distribuere et CDS-miljø i 30 dager.</span><span class="sxs-lookup"><span data-stu-id="84843-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Distribusjonsinnstillinger](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="84843-125">Velg **Godtar** for å bekrefte vilkårene for bruk, og velg deretter **Ferdig** for å gå tilbake til distribusjonsinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="84843-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Distribusjonssamtykke](./media/2DeploymentConsent.png)

7. <span data-ttu-id="84843-127">Valgfritt – Bruk demodata i miljøet.</span><span class="sxs-lookup"><span data-stu-id="84843-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="84843-128">Gå til **Avanserte innstillinger**, velg **Tilpass konfigurasjon av SQL-database**, og sett **Angi et datasett for applikasjonsdatabase** til **Demo**.</span><span class="sxs-lookup"><span data-stu-id="84843-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="84843-129">Fyll ut de gjenstående nødvendige feltene i veiviseren, og bekreft distribusjonen.</span><span class="sxs-lookup"><span data-stu-id="84843-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="84843-130">Tidspunktet for klargjøring av miljøet varierer basert på miljøtypen.</span><span class="sxs-lookup"><span data-stu-id="84843-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="84843-131">Klargjøring kan ta opptil seks timer.</span><span class="sxs-lookup"><span data-stu-id="84843-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="84843-132">Når distribusjonen er fullført, viser miljøet som **Distribuert**.</span><span class="sxs-lookup"><span data-stu-id="84843-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="84843-133">Velg **Logg på** og logg på miljøet for å bekrefte at det er installert.</span><span class="sxs-lookup"><span data-stu-id="84843-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![-miljødetaljer](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="84843-135">Bruk oppdateringer i Finance-miljøet</span><span class="sxs-lookup"><span data-stu-id="84843-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="84843-136">Project Operations krever et Finance-miljø med programversjon **10.0.13 (10.0.569.20009)** eller høyere.</span><span class="sxs-lookup"><span data-stu-id="84843-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="84843-137">Det kan hende du må bruke kvalitetsoppdateringer i Finance-miljøet for å få denne versjonen.</span><span class="sxs-lookup"><span data-stu-id="84843-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="84843-138">I LCS, på siden **Miljødetaljer**, i delen **Tilgjengelige oppdateringer**, velger du **Vis oppdatering**.</span><span class="sxs-lookup"><span data-stu-id="84843-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Vis oppdateringer](./media/5ViewUpdates.png)

2. <span data-ttu-id="84843-140">På siden **Binære oppdateringer** velger du **Lagre pakke.**</span><span class="sxs-lookup"><span data-stu-id="84843-140">On the **Binary updates** page, select **Save package.**</span></span>

![Lagre pakke](./media/6SavePackage.png)

3. <span data-ttu-id="84843-142">Klikk **Velg alle**, og velg deretter **Lagre pakke**.</span><span class="sxs-lookup"><span data-stu-id="84843-142">Click **Select all** and then select **Save package**.</span></span>

![Se gjennom og lagre oppdateringer](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="84843-144">Skriv inn et navn og en beskrivelse av pakken, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="84843-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="84843-145">Denne prosessen kan ta tid, avhengig av Internett-tilkoblingen.</span><span class="sxs-lookup"><span data-stu-id="84843-145">Depending on the internet connection, this process might take some time.</span></span>

![Last opp pakke til aktivabibliotek](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="84843-147">Etter at pakken er lagret, velger du **Fullført** og lagrer denne pakken i aktivabiblioteket i LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="84843-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="84843-148">Lagring og validering av pakken kan ta omtrent 15 minutter.</span><span class="sxs-lookup"><span data-stu-id="84843-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="84843-149">For å bruke oppdateringen går du til siden **Miljødetaljer** i LCS og velger **Vedlikehold** > **Bruk oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="84843-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Vedlikeholde miljøer](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="84843-151">I listen over oppdateringer velger du pakken du opprettet, og deretter velger du **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="84843-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Bruke oppdateringer](./media/10ApplyUpdates.png)

<span data-ttu-id="84843-153">Behandling av miljøet kan ta litt tid.</span><span class="sxs-lookup"><span data-stu-id="84843-153">Environment servicing will take some time.</span></span> <span data-ttu-id="84843-154">Når det er ferdig, går miljøet tilbake til en distribuert tilstand.</span><span class="sxs-lookup"><span data-stu-id="84843-154">After it is complete, the environment will return to a deployed state.</span></span>

![Miljø distribuert](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="84843-156">Opprett en tilkobling for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="84843-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="84843-157">I LCS-prosjektet går du til siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="84843-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="84843-158">Under **Common Data Service-miljøinformasjon** velger du **Koble til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="84843-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="84843-159">Når koblingen er fullført, velger du **Koble til CDS for Apps** på nytt.</span><span class="sxs-lookup"><span data-stu-id="84843-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="84843-160">Du vil bli videresendt til dobbel skriving i Finance.</span><span class="sxs-lookup"><span data-stu-id="84843-160">You will be redirected to Dual Write in Finance.</span></span>

![Kobling til CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="84843-162">Velg **Bruk løsning** for å få tilgang til enhetene som skal tilordnes i integrasjonen.</span><span class="sxs-lookup"><span data-stu-id="84843-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Bruk løsninger](./media/13ApplySolutions.png)

5. <span data-ttu-id="84843-164">Velg begge løsningene, **Dynamics 365 Finance and Operations Enhetstilordning for dobbel skriving** og **Dynamics 365 Project Operations Enhetstilordning for dobbel skriving**, og velg deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="84843-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Bekreft løsninger](./media/14ConfirmSolutions.png)

<span data-ttu-id="84843-166">Når løsningene er tatt i bruk, brukes enhetene for dobbel skriving i miljøet.</span><span class="sxs-lookup"><span data-stu-id="84843-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Bruke løsninger](./media/15ApplyingSolutions.png)

<span data-ttu-id="84843-168">Når enhetene er brukt, vises alle tilgjengelige tilordninger i miljøet.</span><span class="sxs-lookup"><span data-stu-id="84843-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Tilordninger for dobbel skriving](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="84843-170">Oppdater dataenhetene etter oppdateringen</span><span class="sxs-lookup"><span data-stu-id="84843-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="84843-171">I Finance går du til arbeidsområdet **Dataadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="84843-171">In Finance, go to the **Data management** workspace.</span></span>

![Arbeidsområde for dataadministrasjon](./media/16DataManagement.png)

2. <span data-ttu-id="84843-173">Velg flisen **Parametere for rammeverk**.</span><span class="sxs-lookup"><span data-stu-id="84843-173">Select the **Framework parameters** tile.</span></span>

![Parametere for rammeverk](./media/17FrameworkParameters.png)

3. <span data-ttu-id="84843-175">På siden **Enhetsinnstillinger** velger du **Oppdater enhetsliste**.</span><span class="sxs-lookup"><span data-stu-id="84843-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Oppdater enhetsliste](./media/18RefreshEntityList.png)

<span data-ttu-id="84843-177">Oppdateringen tar ca. 20 minutter.</span><span class="sxs-lookup"><span data-stu-id="84843-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="84843-178">Du mottar et varsel når den er fullført.</span><span class="sxs-lookup"><span data-stu-id="84843-178">You will receive an alert when it is complete.</span></span>

![Bekreftelse på oppdatering](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="84843-180">Oppdatere sikkerhetsinnstillinger for Project Operations i Dataverse</span><span class="sxs-lookup"><span data-stu-id="84843-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="84843-181">Gå til Project Operations i Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="84843-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="84843-182">Gå til **Innstillinger** > **Sikkerhet** > **Sikkerhetsroller**.</span><span class="sxs-lookup"><span data-stu-id="84843-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="84843-183">På siden **Sikkerhetsroller** velger du **appbruker med dobbeltskriving** i listen over roller og velger kategorien **Egendefinerte enheter**.</span><span class="sxs-lookup"><span data-stu-id="84843-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="84843-184">Kontroller at rollen har tillatelsene **Lese** og **Tilføye i** for følgende:</span><span class="sxs-lookup"><span data-stu-id="84843-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="84843-185">**Valutakurstype**</span><span class="sxs-lookup"><span data-stu-id="84843-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="84843-186">**Plan over kontoer**</span><span class="sxs-lookup"><span data-stu-id="84843-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="84843-187">**Regnskapskalender**</span><span class="sxs-lookup"><span data-stu-id="84843-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="84843-188">**Finans**</span><span class="sxs-lookup"><span data-stu-id="84843-188">**Ledger**</span></span>

5. <span data-ttu-id="84843-189">Etter at sikkerhetsrollen er oppdatert, går du til **Innstillinger** > **Sikkerhet** > **Team** og velger standardteamet i teamvisningen **Lokale forretningseier**.</span><span class="sxs-lookup"><span data-stu-id="84843-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="84843-190">Velg **Administrer roller** og bekreft at sikkerhetsrettigheten **appbruker med dobbeltskriving** gjelder for dette teamet.</span><span class="sxs-lookup"><span data-stu-id="84843-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="84843-191">Kjøre tilordninger med dobbel skriving for Project Operations</span><span class="sxs-lookup"><span data-stu-id="84843-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="84843-192">I LCS-prosjektet går du til siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="84843-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="84843-193">Under **Common Data Service-miljøinformasjon** velger du **Koble til CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="84843-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="84843-194">Når du har valgt koblingen, blir du omdirigert til listen over enheter i tilordningene.</span><span class="sxs-lookup"><span data-stu-id="84843-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="84843-195">Start tilordningene slik det er beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="84843-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="84843-196">Pass på at du følger rekkefølgen slik den er oppført.</span><span class="sxs-lookup"><span data-stu-id="84843-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="84843-197">**Enhetstilordning**</span><span class="sxs-lookup"><span data-stu-id="84843-197">**Entity Map**</span></span> | <span data-ttu-id="84843-198">**Oppdater enhet**</span><span class="sxs-lookup"><span data-stu-id="84843-198">**Refresh entity**</span></span> | <span data-ttu-id="84843-199">**Første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="84843-199">**Initial sync**</span></span> | <span data-ttu-id="84843-200">**Hovedoppføring for første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="84843-200">**Master for initial sync**</span></span> | <span data-ttu-id="84843-201">**Forhåndskrav for kjøring**</span><span class="sxs-lookup"><span data-stu-id="84843-201">**Run prerequisites**</span></span> | <span data-ttu-id="84843-202">**Forhåndskrav for innledende synkronisering**</span><span class="sxs-lookup"><span data-stu-id="84843-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="84843-203">**Prosjektressursroller for alle selskaper (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="84843-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="84843-204">No</span><span class="sxs-lookup"><span data-stu-id="84843-204">No</span></span> | <span data-ttu-id="84843-205">Ja</span><span class="sxs-lookup"><span data-stu-id="84843-205">Yes</span></span> | <span data-ttu-id="84843-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="84843-206">Common Data Service</span></span> | <span data-ttu-id="84843-207">No</span><span class="sxs-lookup"><span data-stu-id="84843-207">No</span></span> | <span data-ttu-id="84843-208">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-208">N\A</span></span> |
| <span data-ttu-id="84843-209">**Juridiske enheter (cdm\_selskaper)**</span><span class="sxs-lookup"><span data-stu-id="84843-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="84843-210">No</span><span class="sxs-lookup"><span data-stu-id="84843-210">No</span></span> | <span data-ttu-id="84843-211">Ja</span><span class="sxs-lookup"><span data-stu-id="84843-211">Yes</span></span> | <span data-ttu-id="84843-212">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="84843-212">Finance and Operations apps</span></span> | <span data-ttu-id="84843-213">No</span><span class="sxs-lookup"><span data-stu-id="84843-213">No</span></span> | <span data-ttu-id="84843-214">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-214">N\A</span></span> |
| <span data-ttu-id="84843-215">**Finans (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="84843-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="84843-216">No</span><span class="sxs-lookup"><span data-stu-id="84843-216">No</span></span> | <span data-ttu-id="84843-217">Ja</span><span class="sxs-lookup"><span data-stu-id="84843-217">Yes</span></span> | <span data-ttu-id="84843-218">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="84843-218">Finance and Operations apps</span></span> | <span data-ttu-id="84843-219">Ja</span><span class="sxs-lookup"><span data-stu-id="84843-219">Yes</span></span> | <span data-ttu-id="84843-220">Ja, Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="84843-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="84843-221">**Faktiske verdier for Project Operations-integrering (msdyn\_faktiske verdier)**</span><span class="sxs-lookup"><span data-stu-id="84843-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="84843-222">No</span><span class="sxs-lookup"><span data-stu-id="84843-222">No</span></span> | <span data-ttu-id="84843-223">No</span><span class="sxs-lookup"><span data-stu-id="84843-223">No</span></span> | <span data-ttu-id="84843-224">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-224">N\A</span></span> | <span data-ttu-id="84843-225">Ja</span><span class="sxs-lookup"><span data-stu-id="84843-225">Yes</span></span> | <span data-ttu-id="84843-226">No</span><span class="sxs-lookup"><span data-stu-id="84843-226">No</span></span> |
| <span data-ttu-id="84843-227">**Prosjektkontraktlinjer (salgsordredetaljer)**</span><span class="sxs-lookup"><span data-stu-id="84843-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="84843-228">No</span><span class="sxs-lookup"><span data-stu-id="84843-228">No</span></span> | <span data-ttu-id="84843-229">No</span><span class="sxs-lookup"><span data-stu-id="84843-229">No</span></span> | <span data-ttu-id="84843-230">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-230">N\A</span></span> | <span data-ttu-id="84843-231">No</span><span class="sxs-lookup"><span data-stu-id="84843-231">No</span></span> | <span data-ttu-id="84843-232">No</span><span class="sxs-lookup"><span data-stu-id="84843-232">No</span></span> |
| <span data-ttu-id="84843-233">**Integreringsenhet for prosjekttransaksjonsrelasjoner (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="84843-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="84843-234">No</span><span class="sxs-lookup"><span data-stu-id="84843-234">No</span></span> | <span data-ttu-id="84843-235">No</span><span class="sxs-lookup"><span data-stu-id="84843-235">No</span></span> | <span data-ttu-id="84843-236">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-236">N\A</span></span> | <span data-ttu-id="84843-237">No</span><span class="sxs-lookup"><span data-stu-id="84843-237">No</span></span> | <span data-ttu-id="84843-238">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-238">N\A</span></span> |
| <span data-ttu-id="84843-239">**Kontraktlinjemilepæler for Project Operations-integrering (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="84843-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="84843-240">No</span><span class="sxs-lookup"><span data-stu-id="84843-240">No</span></span> | <span data-ttu-id="84843-241">No</span><span class="sxs-lookup"><span data-stu-id="84843-241">No</span></span> | <span data-ttu-id="84843-242">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-242">N\A</span></span> | <span data-ttu-id="84843-243">No</span><span class="sxs-lookup"><span data-stu-id="84843-243">No</span></span> | <span data-ttu-id="84843-244">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-244">N\A</span></span> |
| <span data-ttu-id="84843-245">**Enhet for utgiftsestimater for Project Operations-integrering (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="84843-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="84843-246">No</span><span class="sxs-lookup"><span data-stu-id="84843-246">No</span></span> | <span data-ttu-id="84843-247">No</span><span class="sxs-lookup"><span data-stu-id="84843-247">No</span></span> | <span data-ttu-id="84843-248">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-248">N\A</span></span> | <span data-ttu-id="84843-249">No</span><span class="sxs-lookup"><span data-stu-id="84843-249">No</span></span> | <span data-ttu-id="84843-250">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-250">N\A</span></span> |
| <span data-ttu-id="84843-251">**Eksportenhet for prosjektutgiftskategorier for Project Operations-integrering (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="84843-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="84843-252">No</span><span class="sxs-lookup"><span data-stu-id="84843-252">No</span></span> | <span data-ttu-id="84843-253">No</span><span class="sxs-lookup"><span data-stu-id="84843-253">No</span></span> | <span data-ttu-id="84843-254">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-254">N\A</span></span> | <span data-ttu-id="84843-255">No</span><span class="sxs-lookup"><span data-stu-id="84843-255">No</span></span> | <span data-ttu-id="84843-256">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-256">N\A</span></span> |
| <span data-ttu-id="84843-257">**Eksportenhet for prosjektutgifter for Project Operations-integrering (msdyn\_utgifter)**</span><span class="sxs-lookup"><span data-stu-id="84843-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="84843-258">Ja</span><span class="sxs-lookup"><span data-stu-id="84843-258">Yes</span></span> | <span data-ttu-id="84843-259">No</span><span class="sxs-lookup"><span data-stu-id="84843-259">No</span></span> | <span data-ttu-id="84843-260">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-260">N\A</span></span> | <span data-ttu-id="84843-261">No</span><span class="sxs-lookup"><span data-stu-id="84843-261">No</span></span> | <span data-ttu-id="84843-262">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-262">N\A</span></span> |
| <span data-ttu-id="84843-263">**Enhet for timesestimater for Project Operations-integrering (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="84843-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="84843-264">Ja</span><span class="sxs-lookup"><span data-stu-id="84843-264">Yes</span></span> | <span data-ttu-id="84843-265">No</span><span class="sxs-lookup"><span data-stu-id="84843-265">No</span></span> | <span data-ttu-id="84843-266">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-266">N\A</span></span> | <span data-ttu-id="84843-267">No</span><span class="sxs-lookup"><span data-stu-id="84843-267">No</span></span> | <span data-ttu-id="84843-268">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84843-268">N\A</span></span> |


4. <span data-ttu-id="84843-269">Hvis du vil oppdatere enheten, velger du tilordningsnavnet, og deretter velger du **Oppdater enhteter**.</span><span class="sxs-lookup"><span data-stu-id="84843-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Oppdater tilordning](./media/20RefreshMapping.png)

5. <span data-ttu-id="84843-271">Kjør tilordningen etter at oppdateringen er fullført.</span><span class="sxs-lookup"><span data-stu-id="84843-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="84843-272">Før du aktiverer den neste tilordningen, må du kontrollere at tilordningen i tabellen er tilstanden **Kjører**.</span><span class="sxs-lookup"><span data-stu-id="84843-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="84843-273">Det kan ta litt tid å kjøre tilordninger med et større antall forhånds krav.</span><span class="sxs-lookup"><span data-stu-id="84843-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="84843-274">Hvis du vil kjøre en tilordning med forhåndskrav, aktiverer du **Vis relaterte enhetstilordninger**.</span><span class="sxs-lookup"><span data-stu-id="84843-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="84843-275">Hvis tabellen angir at **Forhåndskrav for innledende synkronisering** er **Nei**, må du kontrollere at flagget **Innledende synkronisering** er **Av** i alle tilordninger med forhåndskrav før kjøring.</span><span class="sxs-lookup"><span data-stu-id="84843-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Kjør tilordning](./media/21RunMap.png)

6. <span data-ttu-id="84843-277">Valider alle prosjektrelaterte tilordninger er i tilstanden Kjører.</span><span class="sxs-lookup"><span data-stu-id="84843-277">Validate all project related maps are in the running state.</span></span>

![Alle tilordninger kjører](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="84843-279">Bruk konfigurasjonsdata i CDS for Project Operations (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="84843-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="84843-280">Hvis du har brukt demonstrasjonsdata i Finance-miljøet, kan du se [Konfigurere og bruke konfigurasjonsdata i Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) for å bruke demonstrasjonsdata i CDS-miljø.</span><span class="sxs-lookup"><span data-stu-id="84843-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="84843-281">Project Operations-miljøet ditt er nå klargjort og konfigurert.</span><span class="sxs-lookup"><span data-stu-id="84843-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]