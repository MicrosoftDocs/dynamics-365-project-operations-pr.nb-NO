---
title: Planleggingsytelse for prosjektressurs
description: Dette emnet gir informasjon om hvordan du forbedrer ytelsen til ressursplanlegging for et stort antall prosjekter.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289021"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="826f9-103">Planleggingsytelse for prosjektressurs</span><span class="sxs-lookup"><span data-stu-id="826f9-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="826f9-104">Det kan oppstå ytelsesproblemer knyttet til ressursplanlegging når antallet prosjekter er flere tusener.</span><span class="sxs-lookup"><span data-stu-id="826f9-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="826f9-105">En funksjon som brukes til å forbedre ressursplanleggingsytelsen, er tilgjengelig, og den gjør det mulig for brukere å redusere tiden det tar å starte ressurstilgjengelighetsskjemaet.</span><span class="sxs-lookup"><span data-stu-id="826f9-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="826f9-106">Dette fjerner spesielt synkroniseringsprosessen for ressurskapasitet, og bruker **ResProjectResource**-tabellen til å øke hastigheten på ressursoppslagene.</span><span class="sxs-lookup"><span data-stu-id="826f9-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="826f9-107">Vær oppmerksom på at **ResRollup**-tabellen ikke lenger skal brukes.</span><span class="sxs-lookup"><span data-stu-id="826f9-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="826f9-108">Hvis det er en avhengighet av synkroniseringsprosessen for akkumulert ressurskapasitet eller **ResProjectResource**-tabellen, må du ikke bruke denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="826f9-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="826f9-109">Aktivere ytelsesforbedring for ressursplanlegging</span><span class="sxs-lookup"><span data-stu-id="826f9-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="826f9-110">Følg fremgangsmåten nedenfor for å aktivere ytelsesforbedring for ressursplanlegging.</span><span class="sxs-lookup"><span data-stu-id="826f9-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="826f9-111">Gå til **Funksjonsbehandling** > **Alle**, og finn **Aktiver funksjonen for ytelsesforbedring for ressursplanlegging** i funksjonslisten .</span><span class="sxs-lookup"><span data-stu-id="826f9-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="826f9-112">Velg **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="826f9-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="826f9-113">Hvis du ikke finner funksjonen i listen, velger du **Se etter oppdateringer** for å oppdatere listen.</span><span class="sxs-lookup"><span data-stu-id="826f9-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="826f9-114">Oppdater nettleseren, og gå deretter til **Prosjektstyring og regnskap** > **Periodisk** > **Prosjektressurser** > **Synkroniser ressurskalenderkapasitet på tvers av alle firmaer**.</span><span class="sxs-lookup"><span data-stu-id="826f9-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="826f9-115">Sett **Fjern eksisterende kapasitetsoppføringer** til **Ja** for å fjerne tidligere data.</span><span class="sxs-lookup"><span data-stu-id="826f9-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="826f9-116">Hvis du vil generere trinnvise data, setter du det til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="826f9-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="826f9-117">I **Periodekode**-feltet velger du perioden som data skal genereres i.</span><span class="sxs-lookup"><span data-stu-id="826f9-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="826f9-118">Hvis du velger en periodekode, trenger du ikke definere en start- og sluttdato.</span><span class="sxs-lookup"><span data-stu-id="826f9-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="826f9-119">Hvis du lar **Periodekode**-feltet være tomt, velger du bestemte start- og sluttdatoer for å generere data.</span><span class="sxs-lookup"><span data-stu-id="826f9-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="826f9-120">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="826f9-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="826f9-121">Dette distribuerer generelle data til **ResCalendarCapacity**-tabellen i alle selskaper i miljøet, slik at den satsvise jobben bare må kjøres i én juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="826f9-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="826f9-122">Dataene i denne satsvise jobben er nødvendige for å beregne ressurskapasitet gjennom den tilknyttede kalenderen.</span><span class="sxs-lookup"><span data-stu-id="826f9-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="826f9-123">Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Prosjektressurser** > **Fyll ut prosjektressurser på tvers av alle firmaer**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="826f9-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="826f9-124">Dette er dataoppgraderingsskriptet for generelle data i tabellene **ResProjectResource**, **ResCalendarDateTimeRange** og **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="826f9-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="826f9-125">Verdier for feltet **PSAPRojSchedRole.RootActivity** oppdateres også.</span><span class="sxs-lookup"><span data-stu-id="826f9-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="826f9-126">Hvis dette ikke kjøres, får du en advarsel når du prøver å kjøre ressursplanleggingsoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="826f9-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="826f9-127">Deaktivere ytelsesforbedring for ressursplanlegging</span><span class="sxs-lookup"><span data-stu-id="826f9-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="826f9-128">Gå til **Funksjonsbehandling** > **Alle**, og søk etter **Aktiver funksjonen for ytelsesforbedring for ressursplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="826f9-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="826f9-129">Velg funksjonen, og klikk deretter **Deaktiver**-knappen.</span><span class="sxs-lookup"><span data-stu-id="826f9-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="826f9-130">Oppdater nettleseren din.</span><span class="sxs-lookup"><span data-stu-id="826f9-130">Refresh your browser.</span></span>
4. <span data-ttu-id="826f9-131">Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Kapasitetssynkronisering** > **Synkronisering opprulling av ressurskapasitet**.</span><span class="sxs-lookup"><span data-stu-id="826f9-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="826f9-132">På siden **Synkronisering opprulling av kapasitet** setter du **Fjern eksisterende kapasitetsoppføringer** til **Ja** for å fjerne tidligere data.</span><span class="sxs-lookup"><span data-stu-id="826f9-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="826f9-133">Hvis du vil generere trinnvise data, setter du det til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="826f9-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="826f9-134">I **Periodekode**-feltet velger du perioden som data skal genereres i.</span><span class="sxs-lookup"><span data-stu-id="826f9-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="826f9-135">Hvis du velger en periodekode, trenger du ikke definere en start- og sluttdato.</span><span class="sxs-lookup"><span data-stu-id="826f9-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="826f9-136">Hvis du lar **Periodekode**-feltet være tomt, velger du bestemte start- og sluttdatoer for å generere data.</span><span class="sxs-lookup"><span data-stu-id="826f9-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="826f9-137">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="826f9-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="826f9-138">Dette distribuerer generelle data til **ResRollup**-tabellen i alle selskaper i miljøet, slik at den satsvise jobben bare må kjøres i én juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="826f9-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="826f9-139">Denne satsvise jobben er nødvendig for alle **Ressurstilgjengelighet**-visninger.</span><span class="sxs-lookup"><span data-stu-id="826f9-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="826f9-140">Hvis denne satsvise jobben ikke kjøres, genereres **ResRollup**-dataene direkte, noe som kan ta tid.</span><span class="sxs-lookup"><span data-stu-id="826f9-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]