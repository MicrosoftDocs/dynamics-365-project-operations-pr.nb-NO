---
title: Installasjon av eksempeldata
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
ms.technology: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.assetid: 8580fc8b-868a-42a3-aa04-2afab28d6de4
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 1c1300116fe42091620267fb128ca6c63184970e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754041"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="c635a-102">Installasjon av eksempeldata for Project Service-programmet</span><span class="sxs-lookup"><span data-stu-id="c635a-102">Sample data installation for the Project Service application</span></span>

<span data-ttu-id="c635a-103">For å gjøre det enklere for deg å bygge dine egne demonstrasjonsmiljøer tilgjengeliggjør Microsoft nedlastbare eksempeldatapakker som viser funksjonene i appene.</span><span class="sxs-lookup"><span data-stu-id="c635a-103">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="c635a-104">Det finnes to typer eksempeldatapakker:</span><span class="sxs-lookup"><span data-stu-id="c635a-104">There are two types of sample data packages:</span></span>
- <span data-ttu-id="c635a-105">referanse-/konfigurasjonsdata</span><span class="sxs-lookup"><span data-stu-id="c635a-105">reference/setup data</span></span>
- <span data-ttu-id="c635a-106">demonstrasjonsdata (referanse-/konfigurasjonsdata og transaksjonsdata som arbeidsordrer og prosjekter)</span><span class="sxs-lookup"><span data-stu-id="c635a-106">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="c635a-107">Eksempelpakkene med **referansedata** kan lastes ned i tre ulike pakker, slik at du kan installere data bare for Project Service, eller bare for Field Service, eller du kan installere eksempeldata for begge programmer samtidig.</span><span class="sxs-lookup"><span data-stu-id="c635a-107">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="c635a-108">Eksempeldatapakkene for konfigurasjon/referanse er:</span><span class="sxs-lookup"><span data-stu-id="c635a-108">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="c635a-109">**V902PSMasterData** - Bare Project Service versjon 3.x</span><span class="sxs-lookup"><span data-stu-id="c635a-109">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="c635a-110">**V902FSMasterData** - Bare Field Service versjon 8.x</span><span class="sxs-lookup"><span data-stu-id="c635a-110">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="c635a-111">**V902FPSMasterData** - Field Service 8.x og Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="c635a-111">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="c635a-112">Den siste **demo**-datapakken er:</span><span class="sxs-lookup"><span data-stu-id="c635a-112">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="c635a-113">**FPSDemoData** - Field Service 8.x og Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="c635a-113">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="c635a-114">Installasjonsinstruksjonene er litt forskjellige i delen om brukerne som oppretter og konfigurerer, men resten er det samme som i forrige [**blogginnlegg**](https://aka.ms/fpsdemodatablog).</span><span class="sxs-lookup"><span data-stu-id="c635a-114">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="c635a-115">Denne pakken har et redusert demodatasett og tar omtrent tre timer å installere.</span><span class="sxs-lookup"><span data-stu-id="c635a-115">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="c635a-116">Disse eksempeldatapakkene er bare tilgjengelige på engelsk.</span><span class="sxs-lookup"><span data-stu-id="c635a-116">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c635a-117">**Det finnes ingen måte å avinstallere eksempeldataene på.**</span><span class="sxs-lookup"><span data-stu-id="c635a-117">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="c635a-118">Du må bare installere disse pakkene for demonstrasjon, evaluering, opplæring og testing av systemer.</span><span class="sxs-lookup"><span data-stu-id="c635a-118">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="c635a-119">Merk også det ikke er støtte for å installere en individuell pakke, og deretter installere den andre individuelle pakken.</span><span class="sxs-lookup"><span data-stu-id="c635a-119">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="c635a-120">(Du kan med andre ord ikke installere **FSMasterData** etterfulgt av **PSMasterData**, eller omvendt.) Hvis du tror du kommer til å trenge eksempeldata for begge programmene en gang i fremtiden, må du installere **v902FPSMasterData**-pakken.</span><span class="sxs-lookup"><span data-stu-id="c635a-120">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="c635a-121">Når du installerer en av eksempeldatapakkene, utfører installasjonsprosessen følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="c635a-121">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="c635a-122">Oppretter eller angir standardparametere for å bruke Project Service, Field Service eller begge programmer (hvis aktuelt).</span><span class="sxs-lookup"><span data-stu-id="c635a-122">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="c635a-123">Importerer eksempeldata for programmene, for eksempel ressurser som kan reserveres, programspesifikke roller, salgs- og kostprislister, organisasjonsenheter, salgsbehandlingsoppføringer og andre enheter for å demonstrere viktige funksjoner.</span><span class="sxs-lookup"><span data-stu-id="c635a-123">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="c635a-124">Med **demodata**-pakken får du dataene ovenfor og flere transaksjonsdata som arbeidsordrer og prosjekter.</span><span class="sxs-lookup"><span data-stu-id="c635a-124">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="c635a-125">Lurer du på hvilke funksjoner du kan demonstrere med eksempeldataene?</span><span class="sxs-lookup"><span data-stu-id="c635a-125">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="c635a-126">Se det fiktive scenariet Fabrikam Robotics i [Tekniske merknader](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="c635a-126">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="c635a-127">Hvis du har spørsmål om hvordan du installerer disse eksempeldatapakkene, kan du [sende en e-post på fpsdemodata@microsoft.com.](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c635a-127">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="c635a-128">Krav</span><span class="sxs-lookup"><span data-stu-id="c635a-128">Requirements</span></span>

<span data-ttu-id="c635a-129">Installasjonsprotokollen forutsetter følgende om målforekomsten (organisasjon):</span><span class="sxs-lookup"><span data-stu-id="c635a-129">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="c635a-130">Originalspråket er engelsk og standardvalutaen er amerikanske dollar (USD, $).</span><span class="sxs-lookup"><span data-stu-id="c635a-130">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="c635a-131">Organisasjonen har ingen Project Service- eller Field Service-data, eller har bare standarddata som følger med en ny organisasjon.</span><span class="sxs-lookup"><span data-stu-id="c635a-131">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="c635a-132">Den riktige versjonen av forretningsprogrammet er allerede installert:</span><span class="sxs-lookup"><span data-stu-id="c635a-132">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="c635a-133">**For FPSDemoData eller v902FPSMasterData:** Organisasjonen har Field Service versjon 8.x og Project Service versjon 3.x installert.</span><span class="sxs-lookup"><span data-stu-id="c635a-133">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="c635a-134">**For v902PSMasterData:** Organisasjonen har Project Service versjon 3.x installert.</span><span class="sxs-lookup"><span data-stu-id="c635a-134">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="c635a-135">**For v902FSMasterData:** Organisasjonen har Field Service versjon 8.x installert.</span><span class="sxs-lookup"><span data-stu-id="c635a-135">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="c635a-136">Hvis du må installere eksempeldataene på en eksisterende prøveversjon eller et demonstrasjonsmiljø for Project Service og Field Service som allerede har data (anbefales ikke), må du først oppheve sikkerhetskontrollene som er utført av installasjonsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="c635a-136">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="c635a-137">Hvis du vil ha mer informasjon, kan du se Tekniske merknader nedenfor.</span><span class="sxs-lookup"><span data-stu-id="c635a-137">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="c635a-138">Forberede installasjon</span><span class="sxs-lookup"><span data-stu-id="c635a-138">Prepare for installation</span></span>

<span data-ttu-id="c635a-139">Du må kjøre installasjonsprogrammet på en datamaskin med en ny versjon av Windows (Windows 10 foretrukket).</span><span class="sxs-lookup"><span data-stu-id="c635a-139">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="c635a-140">Du bør planlegge at datamaskinen skal være tilkoblet et nettverk og installasjonen skal kjøre i opptil **1 time** for **konfigurasjons-/referansedata**.</span><span class="sxs-lookup"><span data-stu-id="c635a-140">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="c635a-141">(Installasjonen tar vanligvis rundt 30 minutter for **FPSMasterData**, som inneholder eksempeldata for begge programmer.) For **FPSDemoData** tar installasjonen rundt **3 timer**.</span><span class="sxs-lookup"><span data-stu-id="c635a-141">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="c635a-142">Skjermbeskytteren på datamaskinen må være deaktivert.</span><span class="sxs-lookup"><span data-stu-id="c635a-142">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="c635a-143">Øktlegitimasjonen for installasjonen kan ellers gå tapt når skjermbeskyttelsen aktiveres (med mindre du holder økten aktiv under hele installasjonen).</span><span class="sxs-lookup"><span data-stu-id="c635a-143">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="c635a-144">![Skjermbilde av skjermbeskytterinnstillinger med skjermbeskytter deaktivert](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="c635a-144">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="c635a-145">Laste ned og pakke ut</span><span class="sxs-lookup"><span data-stu-id="c635a-145">Download and unpack</span></span>

<span data-ttu-id="c635a-146">Installasjonsprogrammet for Project Service- og Field Service-eksempeldata distribueres som en selvutpakkende kjørbar fil.</span><span class="sxs-lookup"><span data-stu-id="c635a-146">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="c635a-147">Filnavnene kan variere avhengig av eksempeldatapakken, men ellers er trinnene de samme uansett hvilken pakke du installerer.</span><span class="sxs-lookup"><span data-stu-id="c635a-147">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="c635a-148">Når du har lastet ned en pakke, kjører du EXE-filen og godtar vilkårene for å pakke ut den komprimerte zip-filen.</span><span class="sxs-lookup"><span data-stu-id="c635a-148">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="c635a-149">Deretter må du pakke ut innholdet i denne filen til en mappe på datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="c635a-149">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="c635a-150">Avhengig av operativsystemet og sikkerhetsinnstillingene, må du kanskje utføre følgende trinn når pakker ut zip-filen:</span><span class="sxs-lookup"><span data-stu-id="c635a-150">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="c635a-151">Finn og høyreklikk **FPSDemoData.dll**-filen i **v902FPSMasterData** / **PackageDeployer_FPSDemoData**-mappen.</span><span class="sxs-lookup"><span data-stu-id="c635a-151">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="c635a-152">Velg **Fjern blokkering**.</span><span class="sxs-lookup"><span data-stu-id="c635a-152">Choose **Unblock**.</span></span>

3. <span data-ttu-id="c635a-153">Velg **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="c635a-153">Select **Apply**.</span></span>

4. <span data-ttu-id="c635a-154">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c635a-154">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="c635a-155">Opprette eller konfigurere brukere</span><span class="sxs-lookup"><span data-stu-id="c635a-155">Create or configure users</span></span>

<span data-ttu-id="c635a-156">**FPSDemoData**-pakken krever seks brukere mens **FPSMasterData**-pakker krever én bruker.</span><span class="sxs-lookup"><span data-stu-id="c635a-156">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="c635a-157">Referer til den riktige for eksempeldatapakken.</span><span class="sxs-lookup"><span data-stu-id="c635a-157">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="c635a-158">Opprette eller konfigurere brukere - konfigurasjons-/referansedatapakker</span><span class="sxs-lookup"><span data-stu-id="c635a-158">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="c635a-159">**FPSMasterData**-pakken er utformet for å installeres med én bruker kalt Spencer Low med innstillingene som beskrives her.</span><span class="sxs-lookup"><span data-stu-id="c635a-159">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="c635a-160">For å installere pakken på riktig måte må du opprette (eller gi nytt navn midlertidig) brukere i miljøet for å samsvare med den innkommende konfigurasjonen av eksempeldataene.</span><span class="sxs-lookup"><span data-stu-id="c635a-160">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="c635a-161">Hvis du vil opprette eller konfigurere brukere, kan du gå til **Innstillinger** > **Sikkerhet** > **Brukere**, og gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="c635a-161">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="c635a-162">Angi UserFullname = "Spencer Low" med brukernavn "spencerl" (**små bokstaver**) til rollene prosjektleder og praksisleder.</span><span class="sxs-lookup"><span data-stu-id="c635a-162">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="c635a-163">Velg brukeren **Spencer Low**, og velger deretter **Behandle roller**.</span><span class="sxs-lookup"><span data-stu-id="c635a-163">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="c635a-164">Finn og velg **Systemadministrator**-rollen, og velg deretter **OK** for å gi fulle administratorrettigheter til Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="c635a-164">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="c635a-165">Dette trinnet er nødvendig for å sikre at eksempelpostene opprettes med riktig brukereierskap, og derfor fyller ut visninger på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="c635a-165">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="c635a-166">Fra den nedlastede pakken må du oppdatere en fil for datatilordning med e-postadressene til standard brukerkonteksten.</span><span class="sxs-lookup"><span data-stu-id="c635a-166">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="c635a-167">Dette gjør du ved åpne **PkgFolder** og deretter finne og åpne **ImportUserMapFile.xml**-filen i Notisblokk (eller Visual Studio eller et annet redigeringsprogram for XML).</span><span class="sxs-lookup"><span data-stu-id="c635a-167">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="c635a-168">Angi **DefaultUserToMapTo=**-feltet til e-postadressen til Spencer Low-brukeren.</span><span class="sxs-lookup"><span data-stu-id="c635a-168">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="c635a-169">Hvis du ikke bruker Spencer Low med brukernavn **spencerl**, må du oppdatere en ekstra fil.</span><span class="sxs-lookup"><span data-stu-id="c635a-169">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="c635a-170">Åpne **DemoDataPreImportConfig.xml**-filen, og finn deretter **userstocreateandconfigure**-merket.</span><span class="sxs-lookup"><span data-stu-id="c635a-170">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="c635a-171">Oppdater **\<login\>**-merket med brukernavnet til Spencer Low-brukeren.</span><span class="sxs-lookup"><span data-stu-id="c635a-171">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="c635a-172">Hvis du vil ha mer informasjon, kan du se [Tekniske merknader](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="c635a-172">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="c635a-173">Opprette eller konfigurere brukere - demodatapakke</span><span class="sxs-lookup"><span data-stu-id="c635a-173">Create or configure users - demo data package</span></span>

<span data-ttu-id="c635a-174">Demodatapakken krever seks brukere.</span><span class="sxs-lookup"><span data-stu-id="c635a-174">The demo data package requires six users.</span></span> <span data-ttu-id="c635a-175">For at pakken skal installeres på riktig måte, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="c635a-175">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="c635a-176">Opprett eller midlertidig gi nytt navn til eksisterende brukere for å samsvare med innkommende eksempeldatakonfigurasjon ved å gå til **Innstillinger** > **Sikkerhet** > **Brukere**.</span><span class="sxs-lookup"><span data-stu-id="c635a-176">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="c635a-177">Disse rollene er bare nødvendige for personbasert demonstrasjoner.</span><span class="sxs-lookup"><span data-stu-id="c635a-177">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="c635a-178">Brukers fulle navn = "David So" som feltservicetekniker</span><span class="sxs-lookup"><span data-stu-id="c635a-178">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="c635a-179">Brukers fulle navn = "Jamie Reding" som fordelingsansvarlig for kundeservice og feltservice</span><span class="sxs-lookup"><span data-stu-id="c635a-179">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="c635a-180">Brukers fulle navn = "Molly Clark" som kontoadministrator</span><span class="sxs-lookup"><span data-stu-id="c635a-180">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="c635a-181">Brukers fulle navn = "Spencer Low" som praksis- og prosjektleder</span><span class="sxs-lookup"><span data-stu-id="c635a-181">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="c635a-182">Brukers fulle navn = "Veronica Quek" som teammedlem</span><span class="sxs-lookup"><span data-stu-id="c635a-182">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="c635a-183">Brukers fulle navn = "William Contoso"</span><span class="sxs-lookup"><span data-stu-id="c635a-183">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="c635a-184">For demodataimportformål tilordner du de seks brukerne ovenfor administratorrollen slik at eksempeloppføringene importeres på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="c635a-184">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="c635a-185">Åpne **PkgFolder** og finn og åpne **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="c635a-185">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="c635a-186">Oppdater **Ny=**-feltene til e-postadressene for tilsvarende brukere i systemet.</span><span class="sxs-lookup"><span data-stu-id="c635a-186">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="c635a-187">![Skjermbilde av UserMapFile](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="c635a-187">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="c635a-188">Hvis brukeren med fullt navn "Spencer Low" har en annen bruker-ID enn **"spencerl"**, må du oppdatere en ekstra fil.</span><span class="sxs-lookup"><span data-stu-id="c635a-188">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="c635a-189">Åpne **DemoDataPreImportConfig.xml**, og finn **userstocreateandconfigure**-merket.</span><span class="sxs-lookup"><span data-stu-id="c635a-189">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="c635a-190">Oppdater **\<pålogging\>**-merket med loginId (skilles mellom små og store bokstaver).</span><span class="sxs-lookup"><span data-stu-id="c635a-190">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="c635a-191">Den første brukerens kalender (i **userstocreateandconfigure**-merket) brukes til å fylle ut arbeidstimene for alle reserverbare ressurser ved import av demonstrasjonsdata.</span><span class="sxs-lookup"><span data-stu-id="c635a-191">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="c635a-192">Gå til **Innstillinger** > **Sikkerhet** > **Brukere**, finn brukeren "Spencer Low", og åpne Arbeidstimer-alternativet.</span><span class="sxs-lookup"><span data-stu-id="c635a-192">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="c635a-193">Rediger eksisterende arbeidstimer, og velg **Hele den regelmessige ukeplanen fra begynnelse til slutt**-alternativet.</span><span class="sxs-lookup"><span data-stu-id="c635a-193">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="c635a-194">Sikre at **arbeidstimer er satt til 8 AM - 5 PM (9 timer), mandag til fredag og tidssonen angitt til Stillehavskysten (USA og Canada)**.</span><span class="sxs-lookup"><span data-stu-id="c635a-194">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="c635a-195">Dette er nødvendig for å sikre at prosjekt- og planleggingstavlen vises som forventet.</span><span class="sxs-lookup"><span data-stu-id="c635a-195">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="c635a-196">**Anbefaling:** Vurder å opprette en sikkerhetskopi av organisasjonen din nå, i tilfelle du må gå tilbake til startpunktet hvis noe går galt under installeringen av eksempeldata.</span><span class="sxs-lookup"><span data-stu-id="c635a-196">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="c635a-197">Hvis du vil ha mer informasjon, kan du se [Sikkerhetskopiere og gjenopprette forekomster](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="c635a-197">For more information, see [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="c635a-198">Kjør Package Deployer</span><span class="sxs-lookup"><span data-stu-id="c635a-198">Run the Package Deployer</span></span>

1. <span data-ttu-id="c635a-199">Finn og kjør **PackageDeployer.exe** i **v902FPSMasterData**- ELLER **PackageDeployer_FPSDemoData**-mappen.</span><span class="sxs-lookup"><span data-stu-id="c635a-199">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="c635a-200">Godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="c635a-200">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="c635a-201">I neste vindu:</span><span class="sxs-lookup"><span data-stu-id="c635a-201">On the next window:</span></span>

   <span data-ttu-id="c635a-202">a.</span><span class="sxs-lookup"><span data-stu-id="c635a-202">a.</span></span> <span data-ttu-id="c635a-203">Velg distribusjonstype **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="c635a-203">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="c635a-204">b.</span><span class="sxs-lookup"><span data-stu-id="c635a-204">b.</span></span> <span data-ttu-id="c635a-205">Bruk brukeren og passordet til systemadministrator-brukeren som er konfigurert i "Opprette eller konfigurere brukere" ("Spencer Low" med brukernavn "spencerl").</span><span class="sxs-lookup"><span data-stu-id="c635a-205">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="c635a-206">c.</span><span class="sxs-lookup"><span data-stu-id="c635a-206">c.</span></span> <span data-ttu-id="c635a-207">Kontroller at **Vis liste over tilgjengelige organisasjoner** er merket av.</span><span class="sxs-lookup"><span data-stu-id="c635a-207">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="c635a-208">![Skjermbilde av Package Deployer-vinduet med "Vis liste over tilgjengelige organisasjoner" valgt](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="c635a-208">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="c635a-209">Velg organisasjonen der du vil installere eksempeldataene.</span><span class="sxs-lookup"><span data-stu-id="c635a-209">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="c635a-210">Velg **Neste** til du ser dialogboksen **Oppsett av demonstrasjonsdata**.</span><span class="sxs-lookup"><span data-stu-id="c635a-210">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="c635a-211">![Skjermbilde av statusvinduet for installasjon av demonstrasjonsdata](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="c635a-211">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="c635a-212">Før du fortsetter, bør du merke deg at installasjon av eksempeldata kan ta opptil en time (vanligvis ca. 10 minutter).</span><span class="sxs-lookup"><span data-stu-id="c635a-212">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="c635a-213">Du må forsikre deg om datamaskinen forblir på og er koblet til et nettverk gjennom hele installasjonsprosessen, og at økten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="c635a-213">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="c635a-214">Når du er klar, kan du klikke **Neste** for å starte installeringen av eksempeldata.</span><span class="sxs-lookup"><span data-stu-id="c635a-214">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="c635a-215">Etter at eksempeldataene er lastet inn, klikker du **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="c635a-215">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="c635a-216">Kontroller installasjonen av eksempeldata</span><span class="sxs-lookup"><span data-stu-id="c635a-216">Verify the sample data installation</span></span>

<span data-ttu-id="c635a-217">Utfør en sunnhetskontroll ved å kontrollere at antallet oppføringer og typer enheter som er oppført i det fiktive scenarioet Fabrikam Robotics, vises som forventet.</span><span class="sxs-lookup"><span data-stu-id="c635a-217">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="c635a-218">Etter at eksempeldataene er ferdig lastet, logger du på som Spencer Low-brukeren og kontrollerer følgende:</span><span class="sxs-lookup"><span data-stu-id="c635a-218">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="c635a-219">Hvis Project Service -programmet er installert, kan du gå til **Project Service** > **Innstillinger** > **Prislister**.</span><span class="sxs-lookup"><span data-stu-id="c635a-219">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="c635a-220">Kontroller at faktura- og kostnadssatsene finnes med riktig valuta for hvert land/område i datasettet.</span><span class="sxs-lookup"><span data-stu-id="c635a-220">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="c635a-221">Hvis Project Service-appen er installert, går du til **Universal Resource Scheduling** > **Innstillinger** > **Organisasjonsenheter**.</span><span class="sxs-lookup"><span data-stu-id="c635a-221">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="c635a-222">Kontroller at en kostprisliste med riktig valuta er knyttet til hver organisasjonsenhet (unntatt oppføringer for poststed).</span><span class="sxs-lookup"><span data-stu-id="c635a-222">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="c635a-223">Hvis noen mangler, finn og tilknytt den riktige kostprislisten.</span><span class="sxs-lookup"><span data-stu-id="c635a-223">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="c635a-224">Hvis Field Service -programmet er installert, kan du gå til **Project Service** > **Innstillinger** > **Prislister**.</span><span class="sxs-lookup"><span data-stu-id="c635a-224">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="c635a-225">Kontroller at faktura- og kostnadssatser finnes.</span><span class="sxs-lookup"><span data-stu-id="c635a-225">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="c635a-226">Gå til **Field Service** > **Innstillinger** > **Prislister**, og kontroller at faktura- og kostnadssatsene finnes med riktig valuta for hvert land/område i datasettet.</span><span class="sxs-lookup"><span data-stu-id="c635a-226">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="c635a-227">![Skjermbilde av aktive prislister](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="c635a-227">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="c635a-228">![Skjermbilde av aktive organisasjonsenheter](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="c635a-228">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="c635a-229">Tekniske merknader</span><span class="sxs-lookup"><span data-stu-id="c635a-229">Technical notes</span></span>

<span data-ttu-id="c635a-230">Nedenfor finner du mer teknisk informasjon om installasjon av dataene.</span><span class="sxs-lookup"><span data-stu-id="c635a-230">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="c635a-231">Installere eksempeldata på eksisterende data (anbefales ikke)</span><span class="sxs-lookup"><span data-stu-id="c635a-231">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="c635a-232">Hvis du må installere eksempeldataene på en eksisterende prøveversjon eller et demonstrasjonsmiljø for Field Service eller Project Service som allerede har data (anbefales ikke), må du først oppheve sikkerhetskontrollene som er utført av installasjonsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="c635a-232">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="c635a-233">Hvis du vil gjøre dette, kan du gå til **PkgFolder**-mappen for å søke etter og åpne filen **DemoDataPreImportConfig.xml** med Notisblokk (eller et annet redigeringsprogram for XML).</span><span class="sxs-lookup"><span data-stu-id="c635a-233">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="c635a-234">Finn den følgende verdien, og endre deretter innstillingen fra sann til usann:</span><span class="sxs-lookup"><span data-stu-id="c635a-234">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="c635a-235">Denne endringen fører til at installasjonsprogrammet hopper over noen viktige sikkerhetskontroller, inkludert:</span><span class="sxs-lookup"><span data-stu-id="c635a-235">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="c635a-236">Bekrefter at det ikke er mer enn én aktiv **Organisasjonsenhet**-oppføring, og endrer deretter navn til **Fabrikam US**.</span><span class="sxs-lookup"><span data-stu-id="c635a-236">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="c635a-237">Bekrefter at det ikke er mer enn én aktiv **Arbeidsmal**-oppføring.</span><span class="sxs-lookup"><span data-stu-id="c635a-237">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="c635a-238">Bekrefter at det ikke er mer enn én aktiv **Prosjektparameter**-oppføring, og endrer deretter oppføringen til **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="c635a-238">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="c635a-239">Konfigurasjonskomponenter</span><span class="sxs-lookup"><span data-stu-id="c635a-239">Configuration components</span></span>

<span data-ttu-id="c635a-240">Det finnes en rekke andre konfigurasjonskomponenter i denne konfigurasjonsfilen før import.</span><span class="sxs-lookup"><span data-stu-id="c635a-240">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="c635a-241">For teknisk brukere inkluderer noen av disse:</span><span class="sxs-lookup"><span data-stu-id="c635a-241">For technical users, some of these include:</span></span>

- <span data-ttu-id="c635a-242">**\<RequiredSolutions\>** angir nødvendige løsningsinstallasjoner og deres versjonsnumre.</span><span class="sxs-lookup"><span data-stu-id="c635a-242">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="c635a-243">**\<InstallSampleData\>** kontrollerer om medfølgende eksempeldata for appene er installert.</span><span class="sxs-lookup"><span data-stu-id="c635a-243">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="c635a-244">false - hopper over installasjon av disse innebygde dataene (som er flyttbare)</span><span class="sxs-lookup"><span data-stu-id="c635a-244">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="c635a-245">true - installerer de innebygde dataene samtidig med installering av FS- og PSA-eksempeldataene</span><span class="sxs-lookup"><span data-stu-id="c635a-245">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="c635a-246">**\<PreImportDataCollection\>** angir flat fil-datatilordninger og tilknyttede oppføringer som skal importeres før installeringen av hovedeksempeldata.</span><span class="sxs-lookup"><span data-stu-id="c635a-246">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="c635a-247">**\<EntitiesToEnableScheduling\>** angir hvilke enheter som skal aktiveres for booking i Microsoft Dynamics-planlegging (aka Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="c635a-247">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="c635a-248">**\<UsersToCreateAndConfigure\>** angir ressurser som kan reserveres, som opprettes (hvis de ikke allerede finnes) før eksempeldataimporten utføres.</span><span class="sxs-lookup"><span data-stu-id="c635a-248">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="c635a-249">Merk at ressursen som kan reserveres i kildesystemets eksempeldata samsvarer med målsystemets oppføringer for ressurs som kan reserveres, på FullName og påloggingen for hver ressurs.</span><span class="sxs-lookup"><span data-stu-id="c635a-249">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="c635a-250">Det er derfor IKKE mulig å endre navnene i denne forhåndskonfigurasjonsfilen med mindre du først importerer eksempeldata til et målsystem ved hjelp av disse navnene, og deretter endrer navn på ressursene som reserveres, til ønsket navnsett sammen med de aktiverte brukeroppføringene, og deretter eksporterer dataene på nytt for import til de endelige målsystemet (ved å oppdatere gamle og nye **ImportUserMapFile.xml**-oppføringer tilsvarende).</span><span class="sxs-lookup"><span data-stu-id="c635a-250">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="c635a-251">**\<PluginsToDisable\>** angir svært diskrete linjeelement-plugin-moduler som må være deaktivert under eksempeldataimporten, og deretter aktiveres på nytt etterpå.</span><span class="sxs-lookup"><span data-stu-id="c635a-251">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="c635a-252">Det fiktive scenarioet Fabrikam Robotics</span><span class="sxs-lookup"><span data-stu-id="c635a-252">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="c635a-253">Eksempelreferansedatapakkene for Field Service og Project Service installerer **Fabrikam Manufacturing Master Data (v3.0.0.0)-løsningen**, sammen med omtrent 4 000 oppføringer og omtrent 40 forskjellige enheter.</span><span class="sxs-lookup"><span data-stu-id="c635a-253">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="c635a-254">De separate eksempeldatapakkene for Field Service eller Project Service inneholder et delsett av **v902FPSMasterData**-eksempeldataene for programmet.</span><span class="sxs-lookup"><span data-stu-id="c635a-254">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="c635a-255">**Demodata**-pakken installerer **Fabrikam Manufacturing Demo Data (v3.0.0.7)-løsningen** med omtrent 22 000 oppføringer i 148 enheter.</span><span class="sxs-lookup"><span data-stu-id="c635a-255">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="c635a-256">Det fiktive selskapet Fabrikam Robotics er produsent av elektroniske samlebåndsroboter og er kjent for sin produktkvalitet, innovasjon og gode kundeservice, inkludert installasjonsplanlegging, implementering og pågående vedlikeholdstjenester.</span><span class="sxs-lookup"><span data-stu-id="c635a-256">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="c635a-257">Fabrikam har hovedkvarter i USA (Fabrikam US), og har prosjektbaserte serviceoperasjoner i Frankrike, India, Storbritannia og Sveits.</span><span class="sxs-lookup"><span data-stu-id="c635a-257">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="c635a-258">Field Service-operasjoner er sentrert i USA, hovedsaklig i det større Seattle-området.</span><span class="sxs-lookup"><span data-stu-id="c635a-258">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="c635a-259">Selskapet er fokusert på å unytte Tingenes Internett (IoT)-tilkobling for å overvåke kundeaktivaytelser og levere stadig mer proaktive tjenester på stedet.</span><span class="sxs-lookup"><span data-stu-id="c635a-259">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="c635a-260">En avansert oversikt over eksempeldataene er som følger:</span><span class="sxs-lookup"><span data-stu-id="c635a-260">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="c635a-261">Felles eksempeldataelementer (inkludert for begge programmer)</span><span class="sxs-lookup"><span data-stu-id="c635a-261">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="c635a-262">1 bruker</span><span class="sxs-lookup"><span data-stu-id="c635a-262">1 user</span></span>

    - <span data-ttu-id="c635a-263">71 forretningsforbindelser</span><span class="sxs-lookup"><span data-stu-id="c635a-263">71 accounts</span></span>

    - <span data-ttu-id="c635a-264">137 kontakter</span><span class="sxs-lookup"><span data-stu-id="c635a-264">137 contacts</span></span>

    - <span data-ttu-id="c635a-265">Forskjellige transaksjonstyper og kategorier</span><span class="sxs-lookup"><span data-stu-id="c635a-265">Various transaction types and categories</span></span>

    - <span data-ttu-id="c635a-266">50 produkter med 1 produktprisliste</span><span class="sxs-lookup"><span data-stu-id="c635a-266">50 products with 1 product price list</span></span>

    - <span data-ttu-id="c635a-267">14 pris-/kostlister</span><span class="sxs-lookup"><span data-stu-id="c635a-267">14 price/cost lists</span></span>

    - <span data-ttu-id="c635a-268">31 egenskaper (ressursferdigheter) i 2 vurderingsmodeller med 3 nivåer (vurderingsverdier)</span><span class="sxs-lookup"><span data-stu-id="c635a-268">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="c635a-269">Project Service</span><span class="sxs-lookup"><span data-stu-id="c635a-269">Project Service</span></span>

    - <span data-ttu-id="c635a-270">8 organisasjonsenheter</span><span class="sxs-lookup"><span data-stu-id="c635a-270">8 organizational units</span></span>

    - <span data-ttu-id="c635a-271">6 rollespesifikke utnyttelsesnivåer</span><span class="sxs-lookup"><span data-stu-id="c635a-271">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="c635a-272">2,8 k + rolleprisspesifikasjoner</span><span class="sxs-lookup"><span data-stu-id="c635a-272">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="c635a-273">Field Service</span><span class="sxs-lookup"><span data-stu-id="c635a-273">Field Service</span></span>

    - <span data-ttu-id="c635a-274">4 distrikter</span><span class="sxs-lookup"><span data-stu-id="c635a-274">4 territories</span></span>

    - <span data-ttu-id="c635a-275">5 arbeidsordretyper</span><span class="sxs-lookup"><span data-stu-id="c635a-275">5 work order types</span></span>

    - <span data-ttu-id="c635a-276">22 kundeaktiva</span><span class="sxs-lookup"><span data-stu-id="c635a-276">22 customer assets</span></span>

    - <span data-ttu-id="c635a-277">9 hendelsestyper med en rekke tilknyttede ressursegenskaper (9), tjenester (13) og serviceoppgaver (13)</span><span class="sxs-lookup"><span data-stu-id="c635a-277">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="c635a-278">**Demodata**-pakken installerer omtrent 179 arbeidsordrer 12 prosjekter og tilknyttede transaksjonsdata.</span><span class="sxs-lookup"><span data-stu-id="c635a-278">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="c635a-279">Endre arbeidstimene for eksempelressurser</span><span class="sxs-lookup"><span data-stu-id="c635a-279">Change the work hours for sample resources</span></span>

<span data-ttu-id="c635a-280">Som standard har alle ressurser som kan reserveres, en arbeidstidskalender på 24 timer.</span><span class="sxs-lookup"><span data-stu-id="c635a-280">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="c635a-281">Hvis du må endre arbeidstimer for eksempelressurser som kan reserveres, går du til **Universal Resource Scheduling** > **Planlegging** > **Ressurser**.</span><span class="sxs-lookup"><span data-stu-id="c635a-281">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="c635a-282">Velg en bruker (for eksempel Spencer Low), og endre Spencers arbeidstimer til timene du vil bruke for flere brukere.</span><span class="sxs-lookup"><span data-stu-id="c635a-282">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="c635a-283">Gå til **Universal Resource Scheduling** > **Innstillinger** > **Arbeidstidsmaler** og rediger **Standard arbeidsmal**-oppføringen.</span><span class="sxs-lookup"><span data-stu-id="c635a-283">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="c635a-284">I **Malressurs**-feltet velger du en bruker med arbeidstimer du vil bruke for andre ressurser.</span><span class="sxs-lookup"><span data-stu-id="c635a-284">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="c635a-285">Gå til **Universal Resource Scheduling** > **Planlegging** > **Ressurser** > **Aktive ressurser som kan bestilles**.</span><span class="sxs-lookup"><span data-stu-id="c635a-285">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="c635a-286">Velg ressursene du vil endre, og velg deretter **Angi kalender**.</span><span class="sxs-lookup"><span data-stu-id="c635a-286">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="c635a-287">På **Arbeidsmal**-rullegardinlisten velger du **Standard arbeidstimer** eller en annen mal med riktig malressurs.</span><span class="sxs-lookup"><span data-stu-id="c635a-287">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="c635a-288">Når du går til planleggingstavlen, skal du kunne se at ressursene nå har oppdaterte arbeidstimer.</span><span class="sxs-lookup"><span data-stu-id="c635a-288">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="c635a-289">![Skjermbilde av aktive ressurser som kan reserveres](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="c635a-289">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>
