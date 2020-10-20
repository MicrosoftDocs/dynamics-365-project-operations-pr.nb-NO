---
title: Klargjør et nytt miljø
description: Dette emnet gir informasjon om hvordan du klargjør et nytt Project Operations-miljø.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949374"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="3058a-103">Klargjør et nytt miljø</span><span class="sxs-lookup"><span data-stu-id="3058a-103">Provision a new environment</span></span>

<span data-ttu-id="3058a-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="3058a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3058a-105">Dette emnet gir informasjon om hvordan du klargjør et nytt Dynamics 365 Project Operations-miljø for ressursbaserte/ikke-lagerbaserte scenarioer.</span><span class="sxs-lookup"><span data-stu-id="3058a-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="3058a-106">Aktiver automatisk klargjøring av Project Operations i et LCS-prosjekt</span><span class="sxs-lookup"><span data-stu-id="3058a-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="3058a-107">Bruk fremgangsmåten nedenfor for å aktivere den automatiserte klargjøringsflyten for Project Operations for LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3058a-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="3058a-108">Gå til [LCS](https://lcs.dynamics.com/v2), og velg flisen **Behandling av evalueringsfunksjonalitet**.</span><span class="sxs-lookup"><span data-stu-id="3058a-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="3058a-109">I listen **Evalueringsfunksjonalitet** velger du **Project Operations** og deretter **Evalueringsfunksjonalitet aktivert** for å aktivere Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3058a-109">In the **Preview feature** list, select **Project Operations** and the select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="3058a-110">Dette trinnet utføres bare én gang per LCS-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="3058a-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="3058a-111">Klargjør et Project Operations-miljø</span><span class="sxs-lookup"><span data-stu-id="3058a-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="3058a-112">Åpne en ny Dynamics 365 Finance-distribusjon med et [demonstrasjonsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) eller et [sandkasse-/produksjonsmiljø](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="3058a-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="3058a-113">Gå gjennom veiviseren for **klargjøring av miljø**.</span><span class="sxs-lookup"><span data-stu-id="3058a-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="3058a-114">Kontroller at den valgte programversjon er 10.0.13 eller høyere.</span><span class="sxs-lookup"><span data-stu-id="3058a-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="3058a-115">Du klargjør Project Operations ved å gå til **Avanserte innstillinger** og velge **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="3058a-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="3058a-116">Aktiver **Common Data Service-innstillingen** ved å velge **Ja**, og skriv deretter inn informasjon i de obligatoriske feltene:</span><span class="sxs-lookup"><span data-stu-id="3058a-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="3058a-117">Navn</span><span class="sxs-lookup"><span data-stu-id="3058a-117">Name</span></span>
  - <span data-ttu-id="3058a-118">Område</span><span class="sxs-lookup"><span data-stu-id="3058a-118">Region</span></span>
  - <span data-ttu-id="3058a-119">Language</span><span class="sxs-lookup"><span data-stu-id="3058a-119">Language</span></span>
  - <span data-ttu-id="3058a-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="3058a-120">Currency</span></span>
 
5. <span data-ttu-id="3058a-121">I feltet **Common Data Service-mal** velger du **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="3058a-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="3058a-122">Velg miljøtypen for distribusjonen din.</span><span class="sxs-lookup"><span data-stu-id="3058a-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="3058a-123">En abonnementsbasert prøveversjon gjør det mulig å distribuere et CDS-miljø i 30 dager.</span><span class="sxs-lookup"><span data-stu-id="3058a-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Distribusjonsinnstillinger](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="3058a-125">Velg **Godtar** for å bekrefte vilkårene for bruk, og velg deretter **Ferdig** for å gå tilbake til distribusjonsinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="3058a-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Distribusjonssamtykke](./media/2DeploymentConsent.png)

7. <span data-ttu-id="3058a-127">Fyll ut de gjenstående nødvendige feltene i veiviseren, og bekreft distribusjonen.</span><span class="sxs-lookup"><span data-stu-id="3058a-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="3058a-128">Tiden det tar å klargjøre miljøet, varierer avhengig av miljøtypen.</span><span class="sxs-lookup"><span data-stu-id="3058a-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="3058a-129">Klargjøring kan ta opptil seks timer.</span><span class="sxs-lookup"><span data-stu-id="3058a-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="3058a-130">Når distribusjonen er fullført, viser miljøet som **Distribuert**.</span><span class="sxs-lookup"><span data-stu-id="3058a-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="3058a-131">For å bekrefte at miljøet er distribuert velger du **Logg på** og logger deg på miljøet for å bekrefte.</span><span class="sxs-lookup"><span data-stu-id="3058a-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![-miljødetaljer](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="3058a-133">Bruk Project Operations Finance-demodata (valgfritt trinn)</span><span class="sxs-lookup"><span data-stu-id="3058a-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="3058a-134">Bruk Project Operations Finance-demodata for det skydriftede miljøet i versjon 10.0.13, som beskrevet i [denne artikkelen](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="3058a-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="3058a-135">Bruk oppdateringer i Finance-miljøet</span><span class="sxs-lookup"><span data-stu-id="3058a-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="3058a-136">Project Operations krever et Finance-miljø med programversjon **10.0.13 (10.0.569.20009)** eller høyere.</span><span class="sxs-lookup"><span data-stu-id="3058a-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="3058a-137">Det kan hende du må bruke kvalitetsoppdateringer i Finance-miljøet for å få denne versjonen.</span><span class="sxs-lookup"><span data-stu-id="3058a-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="3058a-138">I LCS, på siden **Miljødetaljer**, i delen **Tilgjengelige oppdateringer**, velger du **Vis oppdatering**.</span><span class="sxs-lookup"><span data-stu-id="3058a-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Vis oppdateringer](./media/5ViewUpdates.png)

2. <span data-ttu-id="3058a-140">På siden **Binære oppdateringer** velger du **Lagre pakke.**</span><span class="sxs-lookup"><span data-stu-id="3058a-140">On the **Binary updates** page, select **Save package.**</span></span>

![Lagre pakke](./media/6SavePackage.png)

3. <span data-ttu-id="3058a-142">Klikk **Velg alle**, og velg deretter **Lagre pakke**.</span><span class="sxs-lookup"><span data-stu-id="3058a-142">Click **Select all** and then select **Save package**.</span></span>

![Se gjennom og lagre oppdateringer](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="3058a-144">Skriv inn et navn og en beskrivelse av pakken, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3058a-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="3058a-145">Denne prosessen kan ta tid, avhengig av Internett-tilkoblingen.</span><span class="sxs-lookup"><span data-stu-id="3058a-145">Depending on the internet connection, this process might take some time.</span></span>

![Last opp pakke til aktivabibliotek](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="3058a-147">Etter at pakken er lagret, velger du **Fullført** og lagrer denne pakken i aktivabiblioteket i LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3058a-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="3058a-148">Lagring og validering av pakken kan ta omtrent 15 minutter.</span><span class="sxs-lookup"><span data-stu-id="3058a-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="3058a-149">For å bruke oppdateringen går du til siden **Miljødetaljer** i LCS og velger **Vedlikehold** > **Bruk oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="3058a-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Vedlikeholde miljøer](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="3058a-151">I listen over oppdateringer velger du pakken du opprettet, og deretter velger du **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="3058a-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Bruke oppdateringer](./media/10ApplyUpdates.png)

<span data-ttu-id="3058a-153">Behandling av miljøet kan ta litt tid.</span><span class="sxs-lookup"><span data-stu-id="3058a-153">Environment servicing will take some time.</span></span> <span data-ttu-id="3058a-154">Når det er ferdig, går miljøet tilbake til en distribuert tilstand.</span><span class="sxs-lookup"><span data-stu-id="3058a-154">After it is complete, the environment will return to a deployed state.</span></span>

![Miljø distribuert](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="3058a-156">Opprett en tilkobling for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="3058a-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="3058a-157">I LCS-prosjektet går du til siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="3058a-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="3058a-158">Under **Common Data Service-miljøinformasjon** velger du **Koble til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="3058a-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="3058a-159">Når koblingen er fullført, velger du **Koble til CDS for Apps** på nytt.</span><span class="sxs-lookup"><span data-stu-id="3058a-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="3058a-160">Du vil bli videresendt til dobbel skriving i Finance.</span><span class="sxs-lookup"><span data-stu-id="3058a-160">You will be redirected to Dual Write in Finance.</span></span>

![Kobling til CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="3058a-162">Velg **Bruk løsning** for å få tilgang til enhetene som skal tilordnes i integrasjonen.</span><span class="sxs-lookup"><span data-stu-id="3058a-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Bruk løsninger](./media/13ApplySolutions.png)

5. <span data-ttu-id="3058a-164">Velg begge løsningene, **Enhetstilordning for dobbel skriving i Dynamics 365 Finance and Operations** og **Enhetstilordninger for dobbel skriving i Dynamics 365 Project Operations**, og velg deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="3058a-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Bekreft løsninger](./media/14ConfirmSolutions.png)

<span data-ttu-id="3058a-166">Når løsningene er tatt i bruk, brukes enhetene for dobbel skriving i miljøet.</span><span class="sxs-lookup"><span data-stu-id="3058a-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Bruke løsninger](./media/15ApplyingSolutions.png)

<span data-ttu-id="3058a-168">Når enhetene er brukt, vises alle tilgjengelige tilordninger i miljøet.</span><span class="sxs-lookup"><span data-stu-id="3058a-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Tilordninger for dobbel skriving](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="3058a-170">Oppdater dataenhetene etter oppdateringen</span><span class="sxs-lookup"><span data-stu-id="3058a-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="3058a-171">I Finance går du til arbeidsområdet **Dataadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="3058a-171">In Finance, go to the **Data management** workspace.</span></span>

![Arbeidsområde for dataadministrasjon](./media/16DataManagement.png)

2. <span data-ttu-id="3058a-173">Velg flisen **Parametere for rammeverk**.</span><span class="sxs-lookup"><span data-stu-id="3058a-173">Select the **Framework parameters** tile.</span></span>

![Parametere for rammeverk](./media/17FrameworkParameters.png)

3. <span data-ttu-id="3058a-175">På siden **Enhetsinnstillinger** velger du **Oppdater enhetsliste**.</span><span class="sxs-lookup"><span data-stu-id="3058a-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Oppdater enhetsliste](./media/18RefreshEntityList.png)

<span data-ttu-id="3058a-177">Oppdateringen tar ca. 20 minutter.</span><span class="sxs-lookup"><span data-stu-id="3058a-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="3058a-178">Du mottar et varsel når den er fullført.</span><span class="sxs-lookup"><span data-stu-id="3058a-178">You will receive an alert when it is complete.</span></span>

![Bekreftelse på oppdatering](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="3058a-180">Kjøre tilordninger med dobbel skriving for Project Operations</span><span class="sxs-lookup"><span data-stu-id="3058a-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="3058a-181">I LCS-prosjektet går du til siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="3058a-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="3058a-182">Under **Common Data Service-miljøinformasjon** velger du **Koble til CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="3058a-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="3058a-183">Når du har valgt koblingen, blir du omdirigert til listen over enheter i tilordningene.</span><span class="sxs-lookup"><span data-stu-id="3058a-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="3058a-184">Start tilordningene slik det er beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="3058a-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="3058a-185">Pass på at du følger rekkefølgen slik den er oppført.</span><span class="sxs-lookup"><span data-stu-id="3058a-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="3058a-186">**Enhetstilordning**</span><span class="sxs-lookup"><span data-stu-id="3058a-186">**Entity Map**</span></span> | <span data-ttu-id="3058a-187">**Oppdater enhet**</span><span class="sxs-lookup"><span data-stu-id="3058a-187">**Refresh entity**</span></span> | <span data-ttu-id="3058a-188">**Første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="3058a-188">**Initial sync**</span></span> | <span data-ttu-id="3058a-189">**Hovedoppføring for første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="3058a-189">**Master for initial sync**</span></span> | <span data-ttu-id="3058a-190">**Forhåndskrav for kjøring**</span><span class="sxs-lookup"><span data-stu-id="3058a-190">**Run prerequisites**</span></span> | <span data-ttu-id="3058a-191">**Forhåndskrav for innledende synkronisering**</span><span class="sxs-lookup"><span data-stu-id="3058a-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="3058a-192">**Prosjektressursroller for alle selskaper (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="3058a-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="3058a-193">No</span><span class="sxs-lookup"><span data-stu-id="3058a-193">No</span></span> | <span data-ttu-id="3058a-194">Ja</span><span class="sxs-lookup"><span data-stu-id="3058a-194">Yes</span></span> | <span data-ttu-id="3058a-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3058a-195">Common Data Service</span></span> | <span data-ttu-id="3058a-196">No</span><span class="sxs-lookup"><span data-stu-id="3058a-196">No</span></span> | <span data-ttu-id="3058a-197">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-197">N\A</span></span> |
| <span data-ttu-id="3058a-198">**Juridiske enheter (cdm\_selskaper)**</span><span class="sxs-lookup"><span data-stu-id="3058a-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="3058a-199">No</span><span class="sxs-lookup"><span data-stu-id="3058a-199">No</span></span> | <span data-ttu-id="3058a-200">Ja</span><span class="sxs-lookup"><span data-stu-id="3058a-200">Yes</span></span> | <span data-ttu-id="3058a-201">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="3058a-201">Finance and Operations apps</span></span> | <span data-ttu-id="3058a-202">No</span><span class="sxs-lookup"><span data-stu-id="3058a-202">No</span></span> | <span data-ttu-id="3058a-203">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-203">N\A</span></span> |
| <span data-ttu-id="3058a-204">**Faktiske verdier for Project Operations-integrering (msdyn\_faktiske verdier)**</span><span class="sxs-lookup"><span data-stu-id="3058a-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="3058a-205">No</span><span class="sxs-lookup"><span data-stu-id="3058a-205">No</span></span> | <span data-ttu-id="3058a-206">No</span><span class="sxs-lookup"><span data-stu-id="3058a-206">No</span></span> | <span data-ttu-id="3058a-207">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-207">N\A</span></span> | <span data-ttu-id="3058a-208">Ja</span><span class="sxs-lookup"><span data-stu-id="3058a-208">Yes</span></span> | <span data-ttu-id="3058a-209">No</span><span class="sxs-lookup"><span data-stu-id="3058a-209">No</span></span> |
| <span data-ttu-id="3058a-210">**Prosjektkontraktlinjer (salgsordredetaljer)**</span><span class="sxs-lookup"><span data-stu-id="3058a-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="3058a-211">No</span><span class="sxs-lookup"><span data-stu-id="3058a-211">No</span></span> | <span data-ttu-id="3058a-212">No</span><span class="sxs-lookup"><span data-stu-id="3058a-212">No</span></span> | <span data-ttu-id="3058a-213">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-213">N\A</span></span> | <span data-ttu-id="3058a-214">No</span><span class="sxs-lookup"><span data-stu-id="3058a-214">No</span></span> | <span data-ttu-id="3058a-215">No</span><span class="sxs-lookup"><span data-stu-id="3058a-215">No</span></span> |
| <span data-ttu-id="3058a-216">**Integreringsenhet for prosjekttransaksjonsrelasjoner (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="3058a-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="3058a-217">No</span><span class="sxs-lookup"><span data-stu-id="3058a-217">No</span></span> | <span data-ttu-id="3058a-218">No</span><span class="sxs-lookup"><span data-stu-id="3058a-218">No</span></span> | <span data-ttu-id="3058a-219">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-219">N\A</span></span> | <span data-ttu-id="3058a-220">No</span><span class="sxs-lookup"><span data-stu-id="3058a-220">No</span></span> | <span data-ttu-id="3058a-221">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-221">N\A</span></span> |
| <span data-ttu-id="3058a-222">**Kontraktlinjemilepæler for Project Operations-integrering (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="3058a-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="3058a-223">No</span><span class="sxs-lookup"><span data-stu-id="3058a-223">No</span></span> | <span data-ttu-id="3058a-224">No</span><span class="sxs-lookup"><span data-stu-id="3058a-224">No</span></span> | <span data-ttu-id="3058a-225">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-225">N\A</span></span> | <span data-ttu-id="3058a-226">No</span><span class="sxs-lookup"><span data-stu-id="3058a-226">No</span></span> | <span data-ttu-id="3058a-227">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-227">N\A</span></span> |
| <span data-ttu-id="3058a-228">**Enhet for utgiftsestimater for Project Operations-integrering (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="3058a-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="3058a-229">No</span><span class="sxs-lookup"><span data-stu-id="3058a-229">No</span></span> | <span data-ttu-id="3058a-230">No</span><span class="sxs-lookup"><span data-stu-id="3058a-230">No</span></span> | <span data-ttu-id="3058a-231">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-231">N\A</span></span> | <span data-ttu-id="3058a-232">No</span><span class="sxs-lookup"><span data-stu-id="3058a-232">No</span></span> | <span data-ttu-id="3058a-233">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-233">N\A</span></span> |
| <span data-ttu-id="3058a-234">**Enhet for timesestimater for Project Operations-integrering (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="3058a-234">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="3058a-235">No</span><span class="sxs-lookup"><span data-stu-id="3058a-235">No</span></span> | <span data-ttu-id="3058a-236">No</span><span class="sxs-lookup"><span data-stu-id="3058a-236">No</span></span> | <span data-ttu-id="3058a-237">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-237">N\A</span></span> | <span data-ttu-id="3058a-238">No</span><span class="sxs-lookup"><span data-stu-id="3058a-238">No</span></span> | <span data-ttu-id="3058a-239">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-239">N\A</span></span> |
| <span data-ttu-id="3058a-240">**Eksportenhet for prosjektutgifter for Project Operations-integrering (msdyn\_utgifter)**</span><span class="sxs-lookup"><span data-stu-id="3058a-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="3058a-241">Ja</span><span class="sxs-lookup"><span data-stu-id="3058a-241">Yes</span></span> | <span data-ttu-id="3058a-242">No</span><span class="sxs-lookup"><span data-stu-id="3058a-242">No</span></span> | <span data-ttu-id="3058a-243">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-243">N\A</span></span> | <span data-ttu-id="3058a-244">No</span><span class="sxs-lookup"><span data-stu-id="3058a-244">No</span></span> | <span data-ttu-id="3058a-245">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-245">N\A</span></span> |
| <span data-ttu-id="3058a-246">**Enhet for timesestimater for Project Operations-integrering (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="3058a-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="3058a-247">Ja</span><span class="sxs-lookup"><span data-stu-id="3058a-247">Yes</span></span> | <span data-ttu-id="3058a-248">No</span><span class="sxs-lookup"><span data-stu-id="3058a-248">No</span></span> | <span data-ttu-id="3058a-249">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-249">N\A</span></span> | <span data-ttu-id="3058a-250">No</span><span class="sxs-lookup"><span data-stu-id="3058a-250">No</span></span> | <span data-ttu-id="3058a-251">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="3058a-251">N\A</span></span> |

4. <span data-ttu-id="3058a-252">Hvis du vil oppdatere enheten, velger du tilordningsnavnet, og deretter velger du **Oppdater enhteter**.</span><span class="sxs-lookup"><span data-stu-id="3058a-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 
5. <span data-ttu-id="3058a-253">Fortsett med å kjøre tilordningen etter at oppdateringen er fullført.</span><span class="sxs-lookup"><span data-stu-id="3058a-253">Proceed with running the map after the refresh is complete.</span></span>

![Oppdater tilordning](./media/20RefreshMapping.png)

<span data-ttu-id="3058a-255">Før du aktiverer den neste tilordningen, må du kontrollere at tilordningen i tabellen er tilstanden **Kjører**.</span><span class="sxs-lookup"><span data-stu-id="3058a-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="3058a-256">Det kan ta litt tid å kjøre tilordninger med et større antall forhånds krav.</span><span class="sxs-lookup"><span data-stu-id="3058a-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="3058a-257">Hvis du vil kjøre en tilordning med forhåndskrav, aktiverer du **Vis relaterte enhetstilordninger**.</span><span class="sxs-lookup"><span data-stu-id="3058a-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="3058a-258">Hvis tabellen angir at **Forhåndskrav for innledende synkronisering** er **Nei**, må du kontrollere at flagget **Innledende synkronisering** er **Av** i alle tilordninger med forhåndskrav før kjøring.</span><span class="sxs-lookup"><span data-stu-id="3058a-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Kjør tilordning](./media/21RunMap.png)

6. <span data-ttu-id="3058a-260">Valider alle prosjektrelaterte tilordninger er i tilstanden Kjører.</span><span class="sxs-lookup"><span data-stu-id="3058a-260">Validate all project related maps are in the running state.</span></span>

![Alle tilordninger kjører](./media/22AllMapsRunning.png)

<span data-ttu-id="3058a-262">Project Operations-miljøet ditt er nå klargjort og konfigurert.</span><span class="sxs-lookup"><span data-stu-id="3058a-262">Your Project Operations environment is now provisioned and configured.</span></span>
