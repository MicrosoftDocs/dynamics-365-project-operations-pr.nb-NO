---
title: Feilsøke arbeid i oppgaverutenettet
description: Dette emnet gir feilsøkingsinformasjon som er nødvendig når du arbeider i oppgaverutenettet.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031549"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="52a63-103">Feilsøke arbeid i oppgaverutenettet</span><span class="sxs-lookup"><span data-stu-id="52a63-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="52a63-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="52a63-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="52a63-105">Dette emnet beskriver hvordan du løser problemer som kan oppstå når du arbeider med kostnadsbehandling.</span><span class="sxs-lookup"><span data-stu-id="52a63-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="52a63-106">Aktivere informasjonskapsler</span><span class="sxs-lookup"><span data-stu-id="52a63-106">Enable cookies</span></span>

<span data-ttu-id="52a63-107">Project Operations krever at informasjonskapsler fra tredjeparter aktiveres for å gjengi strukturen i arbeidet.</span><span class="sxs-lookup"><span data-stu-id="52a63-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="52a63-108">Når informasjonskapsler fra tredjeparter ikke er aktivert, vises en tom side i stedet for oppgaver når du velger kategorien **Oppgaver** på siden **Prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="52a63-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Tom kategori når informasjonskapsler fra tredjeparter ikke er aktivert](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="52a63-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="52a63-110">Workaround</span></span>
<span data-ttu-id="52a63-111">For nettleserne Microsoft Edge eller Google Chrome beskriver fremgangsmåtene nedenfor hvordan du oppdaterer nettleserinnstillingen slik at informasjonskapsler fra tredjeparter aktiveres.</span><span class="sxs-lookup"><span data-stu-id="52a63-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="52a63-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="52a63-112">Microsoft Edge</span></span>

1. <span data-ttu-id="52a63-113">Åpne Edge-nettleseren.</span><span class="sxs-lookup"><span data-stu-id="52a63-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="52a63-114">I hjørnet øverst til høyre velger du **ellipsen** (...), og deretter velger du **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="52a63-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="52a63-115">Under **Informasjonskapsler og tillatelser på nettsteder** velger du **Informasjonskapsler og områdedata**.</span><span class="sxs-lookup"><span data-stu-id="52a63-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="52a63-116">Deaktiver **Blokker informasjonskapsler fra tredjeparter**.</span><span class="sxs-lookup"><span data-stu-id="52a63-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="52a63-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="52a63-117">Google Chrome</span></span>

1. <span data-ttu-id="52a63-118">Åpne Chrome-nettleseren.</span><span class="sxs-lookup"><span data-stu-id="52a63-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="52a63-119">Velg de tre vertikale prikkene øverst i høyre hjørne, og velg deretter **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="52a63-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="52a63-120">Under **Personvern og sikkerhet** velger du **Informasjonskapsler og andre områdedata**.</span><span class="sxs-lookup"><span data-stu-id="52a63-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="52a63-121">Velg **Tillat alle informasjonskapsler**.</span><span class="sxs-lookup"><span data-stu-id="52a63-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52a63-122">Hvis du blokkerer informasjonskapsler fra tredjeparter, blokkeres alle informasjonskapsler og områdedata fra andre områder, selv om området er tillatt i unntakslisten.</span><span class="sxs-lookup"><span data-stu-id="52a63-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="52a63-123">PEX-endepunkt</span><span class="sxs-lookup"><span data-stu-id="52a63-123">PEX Endpoint</span></span>

<span data-ttu-id="52a63-124">Project Operations krever at en prosjektparameter refererer til PEX-endepunktet.</span><span class="sxs-lookup"><span data-stu-id="52a63-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="52a63-125">Dette endepunktet kreves for å kommunisere med tjenesten som brukes til å gjengi strukturen for arbeidsfordelingsarbeid.</span><span class="sxs-lookup"><span data-stu-id="52a63-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="52a63-126">Hvis parameteren ikke er aktivert, vises feilmeldingen Prosjektparameteren er ikke gyldig.</span><span class="sxs-lookup"><span data-stu-id="52a63-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="52a63-127">Løsning</span><span class="sxs-lookup"><span data-stu-id="52a63-127">Workaround</span></span>
 ![Feltet PEX-endepunkt på prosjektparameteren](media/projectparameter.png)

1. <span data-ttu-id="52a63-129">Legg til feltet **PEX-endepunkt** på siden **Prosjektparametere**.</span><span class="sxs-lookup"><span data-stu-id="52a63-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="52a63-130">Oppdater feltet med følgende verdi: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="52a63-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="52a63-131">Fjern feltet fra siden **Prosjektparametere**.</span><span class="sxs-lookup"><span data-stu-id="52a63-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="52a63-132">Rettigheter for prosjekt for Internett</span><span class="sxs-lookup"><span data-stu-id="52a63-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="52a63-133">Project Operations er avhengig av en ekstern planleggingsservice.</span><span class="sxs-lookup"><span data-stu-id="52a63-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="52a63-134">Servicen krever at en bruker har flere roller tilordnet til lese- og skrivetilgang til enheter som er relatert til strukturen for arbeidsinndeling.</span><span class="sxs-lookup"><span data-stu-id="52a63-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="52a63-135">Disse enhetene omfatter prosjektoppgaver, ressurstilordninger og aktivitetsavhengigheter.</span><span class="sxs-lookup"><span data-stu-id="52a63-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="52a63-136">Hvis en bruker ikke kan gjengi strukturen for arbeidsinndeling når de går til kategorien **Oppgaver**, skyldes det sannsynligvis at Prosjekt for Project Operations ikke er aktivert.</span><span class="sxs-lookup"><span data-stu-id="52a63-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="52a63-137">En bruker kan motta en sikkerhetsrolle eller en feil relatert til tilgangsfornektelse.</span><span class="sxs-lookup"><span data-stu-id="52a63-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="52a63-138">Løsning</span><span class="sxs-lookup"><span data-stu-id="52a63-138">Workaround</span></span>

1. <span data-ttu-id="52a63-139">Gå til **Innstilling > Sikkerhet > Brukere > Applikasjonsbrukere**.</span><span class="sxs-lookup"><span data-stu-id="52a63-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Applikasjonsleser](media/applicationuser.jpg)
   
2. <span data-ttu-id="52a63-141">Dobbeltklikk appbrukeroppføringen for å kontrollere følgende:</span><span class="sxs-lookup"><span data-stu-id="52a63-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="52a63-142">Brukeren har tilgang til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="52a63-142">The user has access to the project.</span></span> <span data-ttu-id="52a63-143">Denne verifiseringen utføres vanligvis ved å sørge for at brukeren har sikkerhetsrollen **Prosjektleder**.</span><span class="sxs-lookup"><span data-stu-id="52a63-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="52a63-144">Microsoft Project-appbrukeren finnes og er riktig konfigurert.</span><span class="sxs-lookup"><span data-stu-id="52a63-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="52a63-145">Hvis brukeren ikke finnes, kan du opprette en ny brukeroppføring.</span><span class="sxs-lookup"><span data-stu-id="52a63-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="52a63-146">Velg **Nye brukere**.</span><span class="sxs-lookup"><span data-stu-id="52a63-146">Select **New Users**.</span></span> <span data-ttu-id="52a63-147">Endre oppføringsskjemaet til **Appbruker**, og legg deretter til **App-ID-en**.</span><span class="sxs-lookup"><span data-stu-id="52a63-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Detaljer for appbruker](media/applicationuserdetails.jpg)

4. <span data-ttu-id="52a63-149">Kontroller at brukeren er tilordnet riktig lisens, og at tjenesten er aktivert i tjenesteplandetaljene for lisensen.</span><span class="sxs-lookup"><span data-stu-id="52a63-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="52a63-150">Kontroller at brukeren kan åpne project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="52a63-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="52a63-151">Kontroller gjennom prosjektparameterne at systemet henviser til riktig endepunkt.</span><span class="sxs-lookup"><span data-stu-id="52a63-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="52a63-152">Kontroller at prosjektappbrukeren er opprettet.</span><span class="sxs-lookup"><span data-stu-id="52a63-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="52a63-153">Bruk følgende sikkerhetsroller for brukeren:</span><span class="sxs-lookup"><span data-stu-id="52a63-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="52a63-154">Dataverse-bruker</span><span class="sxs-lookup"><span data-stu-id="52a63-154">Dataverse User</span></span>
  - <span data-ttu-id="52a63-155">Project Operations-system</span><span class="sxs-lookup"><span data-stu-id="52a63-155">Project Operations System</span></span>
  - <span data-ttu-id="52a63-156">Prosjektsystem</span><span class="sxs-lookup"><span data-stu-id="52a63-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="52a63-157">Feil under oppdatering av arbeidsnedbrytningsstrukturen</span><span class="sxs-lookup"><span data-stu-id="52a63-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="52a63-158">Når det gjøres én eller flere oppdateringer i arbeidsnedbrytningsstrukturen, mislykkes endringene etter hvert og blir ikke lagret.</span><span class="sxs-lookup"><span data-stu-id="52a63-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="52a63-159">Det vises en feil i tidsplanrutenettet om at nylige endringer du har gjort, kunne ikke lagres.</span><span class="sxs-lookup"><span data-stu-id="52a63-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="52a63-160">Løsning</span><span class="sxs-lookup"><span data-stu-id="52a63-160">Workaround</span></span>

1. <span data-ttu-id="52a63-161">Kontroller at brukeren er tilordnet riktig lisens, og at tjenesten er aktivert i tjenesteplandetaljene for lisensen.</span><span class="sxs-lookup"><span data-stu-id="52a63-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="52a63-162">Kontroller at brukeren kan åpne project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="52a63-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="52a63-163">Kontroller at systemet henviser til det riktige endepunktet.</span><span class="sxs-lookup"><span data-stu-id="52a63-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="52a63-164">Kontroller at prosjektappbrukeren er opprettet.</span><span class="sxs-lookup"><span data-stu-id="52a63-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="52a63-165">Bruk følgende sikkerhetsroller for brukeren:</span><span class="sxs-lookup"><span data-stu-id="52a63-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="52a63-166">Dataverse-bruker eller basebruker</span><span class="sxs-lookup"><span data-stu-id="52a63-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="52a63-167">Project Operations-system</span><span class="sxs-lookup"><span data-stu-id="52a63-167">Project Operations System</span></span>
  - <span data-ttu-id="52a63-168">Prosjektsystem</span><span class="sxs-lookup"><span data-stu-id="52a63-168">Project System</span></span>
  - <span data-ttu-id="52a63-169">Dobbel skriving for Project Operations (Denne rollen kreves hvis du distribuerer det ressursbaserte/ikke-lagerbeholdte scenarioet for Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="52a63-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
