---
title: Bruk Project Operations-demodata for miljø driftet i skyen i Finance
description: Dette emnet forklarer hvordan du bruker demonstrasjonsdata fra Project Operations i et skydriftet Dynamics 365 Finance-miljø.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949005"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="01bd7-103">Bruk Project Operations-demodata for miljø driftet i skyen i Finance</span><span class="sxs-lookup"><span data-stu-id="01bd7-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="01bd7-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="01bd7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

><span data-ttu-id="01bd7-105">[Viktig] Dette emnet bare gjelder bare for Microsoft Dynamics 365 Finance versjon 10.0.13, og kan bare utføres i et skybasert miljø.</span><span class="sxs-lookup"><span data-stu-id="01bd7-105">[Important] This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="01bd7-106">Fullfør trinnene i dette emnet **FØR** du bruker kvalitetsoppdateringer i miljøet.</span><span class="sxs-lookup"><span data-stu-id="01bd7-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="01bd7-107">I LCS-prosjektet åpner du siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="01bd7-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="01bd7-108">Legg merke til at den inneholder detaljene som kreves for å koble til miljøet ved hjelp av RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="01bd7-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![-miljødetaljer](./media/1EnvironmentDetails.png)

<span data-ttu-id="01bd7-110">Det første settet med uthevede legitimasjoner er legitimasjonen for den lokale forretningsforbindelsen og inneholder en hyperkobling til tilkoblingen til eksternt skrivebord.</span><span class="sxs-lookup"><span data-stu-id="01bd7-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="01bd7-111">Legitimasjonen inkluderer brukernavn og passord for miljøadministratoren.</span><span class="sxs-lookup"><span data-stu-id="01bd7-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="01bd7-112">Det andre settet med legitimasjon brukes til å logge på SQL Server i dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="01bd7-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="01bd7-113">Koble til miljøet ved hjelp av hyperkoblingen i **Lokale forretningsforbindelser**, og bruk **legitimasjonen for den lokale forretningsforbindelsen** til å godkjenne.</span><span class="sxs-lookup"><span data-stu-id="01bd7-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="01bd7-114">Gå til **Internet Information Services** > **Applikasjonsutvalg** > **AOSService**, og stopp tjenesten.</span><span class="sxs-lookup"><span data-stu-id="01bd7-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="01bd7-115">Du stopper tjenesten på dette tidspunktet, slik at du kan fortsette å erstatte SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="01bd7-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Stopp AOS](./media/2StopAOS.png)

4. <span data-ttu-id="01bd7-117">Gå til **Tjenester**, og stopp følgende to elementer:</span><span class="sxs-lookup"><span data-stu-id="01bd7-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="01bd7-118">Microsoft Dynamics 365 Unified Operations: Tjenesten for partiadministrasjon</span><span class="sxs-lookup"><span data-stu-id="01bd7-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="01bd7-119">Microsoft Dynamics 365 Unified Operations: Rammeverket for import/eksport av data</span><span class="sxs-lookup"><span data-stu-id="01bd7-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Stopp tjenester](./media/3StopServices.png)

5. <span data-ttu-id="01bd7-121">Åpne Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="01bd7-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="01bd7-122">Logg på med legitimasjonen for SQL-serveren, og bruk axdbadmin-brukeren og passordet fra LCS-siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="01bd7-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="01bd7-124">I Object Explorer velger du **Databaser**, og finn **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="01bd7-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="01bd7-125">Du skal erstatte databasen med en ny database som er plassert i [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="01bd7-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="01bd7-126">Kopier zip-filen til den virtuelle maskinen du er koblet eksternt til, og pakk ut zip-innholdet.</span><span class="sxs-lookup"><span data-stu-id="01bd7-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="01bd7-127">I SQL Server Management Studio høyreklikker du på **AxDB**, og deretter velger du **Oppgaver** > **Gjenopprett** > **Database**.</span><span class="sxs-lookup"><span data-stu-id="01bd7-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Gjenopprett database](./media/5RestoreDatabase.png)

9. <span data-ttu-id="01bd7-129">Velg **Kildeenhet**, og naviger til filen som ble pakket ut fra zip-filen du kopierte.</span><span class="sxs-lookup"><span data-stu-id="01bd7-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Kildeenheter](./media/6SourceDevice.png)

10. <span data-ttu-id="01bd7-131">Velg **Alternativer**, og velg deretter **Overskriv den eksisterende databasen** og **Lukk eksisterende tilkoblinger til måldatabase**.</span><span class="sxs-lookup"><span data-stu-id="01bd7-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="01bd7-132">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="01bd7-132">Select **OK**.</span></span>

![Gjenopprett innstillinger](./media/7RestoreSetting.png)

<span data-ttu-id="01bd7-134">Du vil motta en bekreftelse på at AXDB-gjenopprettingen var vellykket.</span><span class="sxs-lookup"><span data-stu-id="01bd7-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="01bd7-135">Når du har mottatt denne bekreftelsen, kan du lukke SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="01bd7-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="01bd7-136">Gå tilbake til **Internet Information Services** > **Applikasjonsutvalg** > **AOSService**, og start AOSService.</span><span class="sxs-lookup"><span data-stu-id="01bd7-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="01bd7-137">Gå til **Tjenester**, og start de to tjenestene du stoppet tidligere.</span><span class="sxs-lookup"><span data-stu-id="01bd7-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="01bd7-138">Finn AdminUserProvisioning-verktøyet på denne virtuelle maskinen.</span><span class="sxs-lookup"><span data-stu-id="01bd7-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="01bd7-139">Se under K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="01bd7-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="01bd7-140">Kjør .ext-filen ved å bruke brukeradressen din i feltet **E-postadresse**.</span><span class="sxs-lookup"><span data-stu-id="01bd7-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="01bd7-141">Velg **Send inn**.</span><span class="sxs-lookup"><span data-stu-id="01bd7-141">Select **Submit**.</span></span>

![Klargjøring av administratorbruker](./media/8AdminUserProvisioning.png)

<span data-ttu-id="01bd7-143">Dette tar noen minutter å fullføre.</span><span class="sxs-lookup"><span data-stu-id="01bd7-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="01bd7-144">Du skal få en bekreftelsesmelding om at administratorbrukeren er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="01bd7-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="01bd7-145">Til slutt kjører du ledeteksten som administrator og utfører iisreset</span><span class="sxs-lookup"><span data-stu-id="01bd7-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS-tilbakestilling](./media/9IISReset.png)

18. <span data-ttu-id="01bd7-147">Lukk den eksterne skrivebordsøkten, og bruk LCS-siden **Miljødetaljer** til å logge deg på miljøet for å bekrefte at det fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="01bd7-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
