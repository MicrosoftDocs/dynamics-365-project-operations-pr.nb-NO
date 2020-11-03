---
title: Klargjør et nytt miljø
description: Dette emnet gir informasjon om hvordan du klargjør et nytt Project Operations-miljø.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a43b947207b6d4276ef27ec996713bf3883e7906
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081507"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="d5775-103">Klargjør et nytt miljø</span><span class="sxs-lookup"><span data-stu-id="d5775-103">Provision a new environment</span></span>

<span data-ttu-id="d5775-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="d5775-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d5775-105">Dette emnet gir informasjon om hvordan du klargjør et nytt Dynamics 365 Project Operations-miljø for ressursbaserte/ikke-lagerbaserte scenarioer.</span><span class="sxs-lookup"><span data-stu-id="d5775-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="d5775-106">Aktiver automatisk klargjøring av Project Operations i et LCS-prosjekt</span><span class="sxs-lookup"><span data-stu-id="d5775-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="d5775-107">Bruk fremgangsmåten nedenfor for å aktivere den automatiserte klargjøringsflyten for Project Operations for LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d5775-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="d5775-108">Gå til [LCS](https://lcs.dynamics.com/v2), og velg flisen **Behandling av evalueringsfunksjonalitet**.</span><span class="sxs-lookup"><span data-stu-id="d5775-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="d5775-109">I listen **Evalueringsfunksjonalitet** velger du **Project Operations-funksjonen** og deretter **Evalueringsfunksjonalitet aktivert** for å aktivere Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d5775-109">In the **Preview feature** list, select **Project Operations Feature** , and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="d5775-110">Dette trinnet utføres bare én gang per LCS-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="d5775-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="d5775-111">Klargjør et Project Operations-miljø</span><span class="sxs-lookup"><span data-stu-id="d5775-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="d5775-112">Åpne en ny Dynamics 365 Finance-distribusjon med et [demonstrasjonsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) eller et [sandkasse-/produksjonsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="d5775-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="d5775-113">Gå gjennom veiviseren for **klargjøring av miljø**.</span><span class="sxs-lookup"><span data-stu-id="d5775-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="d5775-114">Kontroller at den valgte programversjon er 10.0.13 eller høyere.</span><span class="sxs-lookup"><span data-stu-id="d5775-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="d5775-115">Du klargjør Project Operations ved å gå til **Avanserte innstillinger** og velge **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="d5775-115">To provision Project Operations, under **Advance settings** , select **Common Data Service**.</span></span> 
4. <span data-ttu-id="d5775-116">Aktiver **Common Data Service-innstillingen** ved å velge **Ja** , og skriv deretter inn informasjon i de obligatoriske feltene:</span><span class="sxs-lookup"><span data-stu-id="d5775-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="d5775-117">Navn</span><span class="sxs-lookup"><span data-stu-id="d5775-117">Name</span></span>
  - <span data-ttu-id="d5775-118">Område</span><span class="sxs-lookup"><span data-stu-id="d5775-118">Region</span></span>
  - <span data-ttu-id="d5775-119">Language</span><span class="sxs-lookup"><span data-stu-id="d5775-119">Language</span></span>
  - <span data-ttu-id="d5775-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="d5775-120">Currency</span></span>
 
5. <span data-ttu-id="d5775-121">I feltet **Common Data Service-mal** velger du **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="d5775-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="d5775-122">Velg miljøtypen for distribusjonen din.</span><span class="sxs-lookup"><span data-stu-id="d5775-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="d5775-123">En abonnementsbasert prøveversjon gjør det mulig å distribuere et CDS-miljø i 30 dager.</span><span class="sxs-lookup"><span data-stu-id="d5775-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Distribusjonsinnstillinger](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="d5775-125">Velg **Godtar** for å bekrefte vilkårene for bruk, og velg deretter **Ferdig** for å gå tilbake til distribusjonsinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="d5775-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Distribusjonssamtykke](./media/2DeploymentConsent.png)

7. <span data-ttu-id="d5775-127">Fyll ut de gjenstående nødvendige feltene i veiviseren, og bekreft distribusjonen.</span><span class="sxs-lookup"><span data-stu-id="d5775-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="d5775-128">Tiden det tar å klargjøre miljøet, varierer avhengig av miljøtypen.</span><span class="sxs-lookup"><span data-stu-id="d5775-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="d5775-129">Klargjøring kan ta opptil seks timer.</span><span class="sxs-lookup"><span data-stu-id="d5775-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="d5775-130">Når distribusjonen er fullført, viser miljøet som **Distribuert**.</span><span class="sxs-lookup"><span data-stu-id="d5775-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="d5775-131">For å bekrefte at miljøet er distribuert velger du **Logg på** og logger deg på miljøet for å bekrefte.</span><span class="sxs-lookup"><span data-stu-id="d5775-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![-miljødetaljer](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="d5775-133">Bruk Project Operations Finance-demodata (valgfritt trinn)</span><span class="sxs-lookup"><span data-stu-id="d5775-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="d5775-134">Bruk Project Operations Finance-demodata for det skydriftede miljøet i versjon 10.0.13, som beskrevet i [denne artikkelen](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="d5775-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="d5775-135">Bruk oppdateringer i Finance-miljøet</span><span class="sxs-lookup"><span data-stu-id="d5775-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="d5775-136">Project Operations krever et Finance-miljø med programversjon **10.0.13 (10.0.569.20009)** eller høyere.</span><span class="sxs-lookup"><span data-stu-id="d5775-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="d5775-137">Det kan hende du må bruke kvalitetsoppdateringer i Finance-miljøet for å få denne versjonen.</span><span class="sxs-lookup"><span data-stu-id="d5775-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="d5775-138">I LCS, på siden **Miljødetaljer** , i delen **Tilgjengelige oppdateringer** , velger du **Vis oppdatering**.</span><span class="sxs-lookup"><span data-stu-id="d5775-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Vis oppdateringer](./media/5ViewUpdates.png)

2. <span data-ttu-id="d5775-140">På siden **Binære oppdateringer** velger du **Lagre pakke.**</span><span class="sxs-lookup"><span data-stu-id="d5775-140">On the **Binary updates** page, select **Save package.**</span></span>

![Lagre pakke](./media/6SavePackage.png)

3. <span data-ttu-id="d5775-142">Klikk **Velg alle** , og velg deretter **Lagre pakke**.</span><span class="sxs-lookup"><span data-stu-id="d5775-142">Click **Select all** and then select **Save package**.</span></span>

![Se gjennom og lagre oppdateringer](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="d5775-144">Skriv inn et navn og en beskrivelse av pakken, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d5775-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="d5775-145">Denne prosessen kan ta tid, avhengig av Internett-tilkoblingen.</span><span class="sxs-lookup"><span data-stu-id="d5775-145">Depending on the internet connection, this process might take some time.</span></span>

![Last opp pakke til aktivabibliotek](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="d5775-147">Etter at pakken er lagret, velger du **Fullført** og lagrer denne pakken i aktivabiblioteket i LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d5775-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="d5775-148">Lagring og validering av pakken kan ta omtrent 15 minutter.</span><span class="sxs-lookup"><span data-stu-id="d5775-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="d5775-149">For å bruke oppdateringen går du til siden **Miljødetaljer** i LCS og velger **Vedlikehold** > **Bruk oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="d5775-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Vedlikeholde miljøer](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="d5775-151">I listen over oppdateringer velger du pakken du opprettet, og deretter velger du **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="d5775-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Bruke oppdateringer](./media/10ApplyUpdates.png)

<span data-ttu-id="d5775-153">Behandling av miljøet kan ta litt tid.</span><span class="sxs-lookup"><span data-stu-id="d5775-153">Environment servicing will take some time.</span></span> <span data-ttu-id="d5775-154">Når det er ferdig, går miljøet tilbake til en distribuert tilstand.</span><span class="sxs-lookup"><span data-stu-id="d5775-154">After it is complete, the environment will return to a deployed state.</span></span>

![Miljø distribuert](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="d5775-156">Opprett en tilkobling for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="d5775-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="d5775-157">I LCS-prosjektet går du til siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="d5775-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="d5775-158">Under **Common Data Service-miljøinformasjon** velger du **Koble til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="d5775-158">Under **Common Data Service Environment Information** , select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="d5775-159">Når koblingen er fullført, velger du **Koble til CDS for Apps** på nytt.</span><span class="sxs-lookup"><span data-stu-id="d5775-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="d5775-160">Du vil bli videresendt til dobbel skriving i Finance.</span><span class="sxs-lookup"><span data-stu-id="d5775-160">You will be redirected to Dual Write in Finance.</span></span>

![Kobling til CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="d5775-162">Velg **Bruk løsning** for å få tilgang til enhetene som skal tilordnes i integrasjonen.</span><span class="sxs-lookup"><span data-stu-id="d5775-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Bruk løsninger](./media/13ApplySolutions.png)

5. <span data-ttu-id="d5775-164">Velg begge løsningene, **Enhetstilordning for dobbel skriving i Dynamics 365 Finance and Operations** og **Enhetstilordninger for dobbel skriving i Dynamics 365 Project Operations** , og velg deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="d5775-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps** , and then select **Apply**.</span></span>

![Bekreft løsninger](./media/14ConfirmSolutions.png)

<span data-ttu-id="d5775-166">Når løsningene er tatt i bruk, brukes enhetene for dobbel skriving i miljøet.</span><span class="sxs-lookup"><span data-stu-id="d5775-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Bruke løsninger](./media/15ApplyingSolutions.png)

<span data-ttu-id="d5775-168">Når enhetene er brukt, vises alle tilgjengelige tilordninger i miljøet.</span><span class="sxs-lookup"><span data-stu-id="d5775-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Tilordninger for dobbel skriving](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="d5775-170">Oppdater dataenhetene etter oppdateringen</span><span class="sxs-lookup"><span data-stu-id="d5775-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="d5775-171">I Finance går du til arbeidsområdet **Dataadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="d5775-171">In Finance, go to the **Data management** workspace.</span></span>

![Arbeidsområde for dataadministrasjon](./media/16DataManagement.png)

2. <span data-ttu-id="d5775-173">Velg flisen **Parametere for rammeverk**.</span><span class="sxs-lookup"><span data-stu-id="d5775-173">Select the **Framework parameters** tile.</span></span>

![Parametere for rammeverk](./media/17FrameworkParameters.png)

3. <span data-ttu-id="d5775-175">På siden **Enhetsinnstillinger** velger du **Oppdater enhetsliste**.</span><span class="sxs-lookup"><span data-stu-id="d5775-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Oppdater enhetsliste](./media/18RefreshEntityList.png)

<span data-ttu-id="d5775-177">Oppdateringen tar ca. 20 minutter.</span><span class="sxs-lookup"><span data-stu-id="d5775-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="d5775-178">Du mottar et varsel når den er fullført.</span><span class="sxs-lookup"><span data-stu-id="d5775-178">You will receive an alert when it is complete.</span></span>

![Bekreftelse på oppdatering](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="d5775-180">Kjøre tilordninger med dobbel skriving for Project Operations</span><span class="sxs-lookup"><span data-stu-id="d5775-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="d5775-181">I LCS-prosjektet går du til siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="d5775-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="d5775-182">Under **Common Data Service-miljøinformasjon** velger du **Koble til CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="d5775-182">Under **Common Data Service Environment Information** , select **Link to CDS for Apps.**</span></span> <span data-ttu-id="d5775-183">Når du har valgt koblingen, blir du omdirigert til listen over enheter i tilordningene.</span><span class="sxs-lookup"><span data-stu-id="d5775-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="d5775-184">Start tilordningene slik det er beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d5775-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="d5775-185">Pass på at du følger rekkefølgen slik den er oppført.</span><span class="sxs-lookup"><span data-stu-id="d5775-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="d5775-186">**Enhetstilordning**</span><span class="sxs-lookup"><span data-stu-id="d5775-186">**Entity Map**</span></span> | <span data-ttu-id="d5775-187">**Oppdater enhet**</span><span class="sxs-lookup"><span data-stu-id="d5775-187">**Refresh entity**</span></span> | <span data-ttu-id="d5775-188">**Første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="d5775-188">**Initial sync**</span></span> | <span data-ttu-id="d5775-189">**Hovedoppføring for første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="d5775-189">**Master for initial sync**</span></span> | <span data-ttu-id="d5775-190">**Forhåndskrav for kjøring**</span><span class="sxs-lookup"><span data-stu-id="d5775-190">**Run prerequisites**</span></span> | <span data-ttu-id="d5775-191">**Forhåndskrav for innledende synkronisering**</span><span class="sxs-lookup"><span data-stu-id="d5775-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="d5775-192">**Prosjektressursroller for alle selskaper (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="d5775-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="d5775-193">No</span><span class="sxs-lookup"><span data-stu-id="d5775-193">No</span></span> | <span data-ttu-id="d5775-194">Ja</span><span class="sxs-lookup"><span data-stu-id="d5775-194">Yes</span></span> | <span data-ttu-id="d5775-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d5775-195">Common Data Service</span></span> | <span data-ttu-id="d5775-196">No</span><span class="sxs-lookup"><span data-stu-id="d5775-196">No</span></span> | <span data-ttu-id="d5775-197">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-197">N\A</span></span> |
| <span data-ttu-id="d5775-198">**Juridiske enheter (cdm\_selskaper)**</span><span class="sxs-lookup"><span data-stu-id="d5775-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="d5775-199">No</span><span class="sxs-lookup"><span data-stu-id="d5775-199">No</span></span> | <span data-ttu-id="d5775-200">Ja</span><span class="sxs-lookup"><span data-stu-id="d5775-200">Yes</span></span> | <span data-ttu-id="d5775-201">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="d5775-201">Finance and Operations apps</span></span> | <span data-ttu-id="d5775-202">No</span><span class="sxs-lookup"><span data-stu-id="d5775-202">No</span></span> | <span data-ttu-id="d5775-203">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-203">N\A</span></span> |
| <span data-ttu-id="d5775-204">**Faktiske verdier for Project Operations-integrering (msdyn\_faktiske verdier)**</span><span class="sxs-lookup"><span data-stu-id="d5775-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="d5775-205">No</span><span class="sxs-lookup"><span data-stu-id="d5775-205">No</span></span> | <span data-ttu-id="d5775-206">No</span><span class="sxs-lookup"><span data-stu-id="d5775-206">No</span></span> | <span data-ttu-id="d5775-207">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-207">N\A</span></span> | <span data-ttu-id="d5775-208">Ja</span><span class="sxs-lookup"><span data-stu-id="d5775-208">Yes</span></span> | <span data-ttu-id="d5775-209">No</span><span class="sxs-lookup"><span data-stu-id="d5775-209">No</span></span> |
| <span data-ttu-id="d5775-210">**Prosjektkontraktlinjer (salgsordredetaljer)**</span><span class="sxs-lookup"><span data-stu-id="d5775-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="d5775-211">No</span><span class="sxs-lookup"><span data-stu-id="d5775-211">No</span></span> | <span data-ttu-id="d5775-212">No</span><span class="sxs-lookup"><span data-stu-id="d5775-212">No</span></span> | <span data-ttu-id="d5775-213">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-213">N\A</span></span> | <span data-ttu-id="d5775-214">No</span><span class="sxs-lookup"><span data-stu-id="d5775-214">No</span></span> | <span data-ttu-id="d5775-215">No</span><span class="sxs-lookup"><span data-stu-id="d5775-215">No</span></span> |
| <span data-ttu-id="d5775-216">**Integreringsenhet for prosjekttransaksjonsrelasjoner (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="d5775-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="d5775-217">No</span><span class="sxs-lookup"><span data-stu-id="d5775-217">No</span></span> | <span data-ttu-id="d5775-218">No</span><span class="sxs-lookup"><span data-stu-id="d5775-218">No</span></span> | <span data-ttu-id="d5775-219">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-219">N\A</span></span> | <span data-ttu-id="d5775-220">No</span><span class="sxs-lookup"><span data-stu-id="d5775-220">No</span></span> | <span data-ttu-id="d5775-221">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-221">N\A</span></span> |
| <span data-ttu-id="d5775-222">**Kontraktlinjemilepæler for Project Operations-integrering (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="d5775-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="d5775-223">No</span><span class="sxs-lookup"><span data-stu-id="d5775-223">No</span></span> | <span data-ttu-id="d5775-224">No</span><span class="sxs-lookup"><span data-stu-id="d5775-224">No</span></span> | <span data-ttu-id="d5775-225">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-225">N\A</span></span> | <span data-ttu-id="d5775-226">No</span><span class="sxs-lookup"><span data-stu-id="d5775-226">No</span></span> | <span data-ttu-id="d5775-227">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-227">N\A</span></span> |
| <span data-ttu-id="d5775-228">**Enhet for utgiftsestimater for Project Operations-integrering (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="d5775-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="d5775-229">No</span><span class="sxs-lookup"><span data-stu-id="d5775-229">No</span></span> | <span data-ttu-id="d5775-230">No</span><span class="sxs-lookup"><span data-stu-id="d5775-230">No</span></span> | <span data-ttu-id="d5775-231">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-231">N\A</span></span> | <span data-ttu-id="d5775-232">No</span><span class="sxs-lookup"><span data-stu-id="d5775-232">No</span></span> | <span data-ttu-id="d5775-233">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-233">N\A</span></span> |
| <span data-ttu-id="d5775-234">**Eksportenhet for prosjektutgiftskategorier for Project Operations-integrering (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="d5775-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="d5775-235">No</span><span class="sxs-lookup"><span data-stu-id="d5775-235">No</span></span> | <span data-ttu-id="d5775-236">No</span><span class="sxs-lookup"><span data-stu-id="d5775-236">No</span></span> | <span data-ttu-id="d5775-237">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-237">N\A</span></span> | <span data-ttu-id="d5775-238">No</span><span class="sxs-lookup"><span data-stu-id="d5775-238">No</span></span> | <span data-ttu-id="d5775-239">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-239">N\A</span></span> |
| <span data-ttu-id="d5775-240">**Eksportenhet for prosjektutgifter for Project Operations-integrering (msdyn\_utgifter)**</span><span class="sxs-lookup"><span data-stu-id="d5775-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="d5775-241">Ja</span><span class="sxs-lookup"><span data-stu-id="d5775-241">Yes</span></span> | <span data-ttu-id="d5775-242">No</span><span class="sxs-lookup"><span data-stu-id="d5775-242">No</span></span> | <span data-ttu-id="d5775-243">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-243">N\A</span></span> | <span data-ttu-id="d5775-244">No</span><span class="sxs-lookup"><span data-stu-id="d5775-244">No</span></span> | <span data-ttu-id="d5775-245">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-245">N\A</span></span> |
| <span data-ttu-id="d5775-246">**Enhet for timesestimater for Project Operations-integrering (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="d5775-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="d5775-247">Ja</span><span class="sxs-lookup"><span data-stu-id="d5775-247">Yes</span></span> | <span data-ttu-id="d5775-248">No</span><span class="sxs-lookup"><span data-stu-id="d5775-248">No</span></span> | <span data-ttu-id="d5775-249">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-249">N\A</span></span> | <span data-ttu-id="d5775-250">No</span><span class="sxs-lookup"><span data-stu-id="d5775-250">No</span></span> | <span data-ttu-id="d5775-251">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d5775-251">N\A</span></span> |


4. <span data-ttu-id="d5775-252">Hvis du vil oppdatere enheten, velger du tilordningsnavnet, og deretter velger du **Oppdater enhteter**.</span><span class="sxs-lookup"><span data-stu-id="d5775-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Oppdater tilordning](./media/20RefreshMapping.png)

5. <span data-ttu-id="d5775-254">Kjør tilordningen etter at oppdateringen er fullført.</span><span class="sxs-lookup"><span data-stu-id="d5775-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="d5775-255">Før du aktiverer den neste tilordningen, må du kontrollere at tilordningen i tabellen er tilstanden **Kjører**.</span><span class="sxs-lookup"><span data-stu-id="d5775-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="d5775-256">Det kan ta litt tid å kjøre tilordninger med et større antall forhånds krav.</span><span class="sxs-lookup"><span data-stu-id="d5775-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="d5775-257">Hvis du vil kjøre en tilordning med forhåndskrav, aktiverer du **Vis relaterte enhetstilordninger**.</span><span class="sxs-lookup"><span data-stu-id="d5775-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="d5775-258">Hvis tabellen angir at **Forhåndskrav for innledende synkronisering** er **Nei** , må du kontrollere at flagget **Innledende synkronisering** er **Av** i alle tilordninger med forhåndskrav før kjøring.</span><span class="sxs-lookup"><span data-stu-id="d5775-258">If the table indicates **Prerequisite initial sync** is **No** , verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Kjør tilordning](./media/21RunMap.png)

6. <span data-ttu-id="d5775-260">Valider alle prosjektrelaterte tilordninger er i tilstanden Kjører.</span><span class="sxs-lookup"><span data-stu-id="d5775-260">Validate all project related maps are in the running state.</span></span>

![Alle tilordninger kjører](./media/22AllMapsRunning.png)

<span data-ttu-id="d5775-262">Project Operations-miljøet ditt er nå klargjort og konfigurert.</span><span class="sxs-lookup"><span data-stu-id="d5775-262">Your Project Operations environment is now provisioned and configured.</span></span>
