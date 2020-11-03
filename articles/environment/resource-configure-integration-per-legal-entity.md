---
title: Konfigurere Project Operations-integrering per juridisk enhet
description: Dette emnet gir informasjon om hvordan du konfigurerer integrering per juridisk enhet i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096764"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="57078-103">Konfigurere Project Operations-integrering per juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="57078-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="57078-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="57078-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="57078-105">Dette emnet veileder deg gjennom trinnene som kreves for å konfigurere Dynamics 365 Project Operations per juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="57078-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="57078-106">Aktivere funksjonsnøkler i Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="57078-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="57078-107">Fullfør fremgangsmåten nedenfor for å aktivere nødvendige funksjoner.</span><span class="sxs-lookup"><span data-stu-id="57078-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="57078-108">I Dynamics 365 Finance går du til arbeidsområdet **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="57078-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="57078-109">Søk etter og aktiver følgende funksjoner i **funksjonslisten** :</span><span class="sxs-lookup"><span data-stu-id="57078-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="57078-110">**Aktiver flere kontraktlinjer for et prosjekt**</span><span class="sxs-lookup"><span data-stu-id="57078-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="57078-111">**Aktiver Project Operations i Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="57078-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="57078-112">Hvis du ikke ser **Funksjonsnøkler** , må du kontrollere at Finance-versjonen oppfyller minimumskravene for versjon (programversjon 10.0.13 med alle kvalitets oppdateringer brukt, eller nyere).</span><span class="sxs-lookup"><span data-stu-id="57078-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="57078-113">Velg **Se etter oppdateringer** for å oppdatere funksjonslisten.</span><span class="sxs-lookup"><span data-stu-id="57078-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="57078-114">Definere Project Operations-distribusjonsscenarioet for en juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="57078-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="57078-115">Du kan aktivere Project Operations i Dynamics 365 Customer Engagement på et nivå for en juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="57078-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="57078-116">Du kan ha én juridisk enhet som bruker Project Operations i Dynamics 365 Customer Engagement for ressursbaserte / ikke-lagerførte scenarioer.</span><span class="sxs-lookup"><span data-stu-id="57078-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="57078-117">I det samme miljøet kan du ha en ny juridisk enhet som bruker Project Operations til lagerførte scenarioer / produksjonsordrescenarier.</span><span class="sxs-lookup"><span data-stu-id="57078-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="57078-118">I Dynamics 365 Finance går du til **Prosjektstyring og regnskap** > **Oppsett** > **Globale parametere for prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="57078-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="57078-119">I listen over tilgjengelige juridiske enheter velger du enheter der flere kontraktlinjer og Project Operations i Dynamics 365 Customer Engagement skal være aktivert.</span><span class="sxs-lookup"><span data-stu-id="57078-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="57078-120">La juridiske enheter som skal bruke Project Operations for lagerførte scenarioer / produksjonsordrescenarioer, være umerket.</span><span class="sxs-lookup"><span data-stu-id="57078-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="57078-121">En juridisk enhet kan bare velges hvis den ikke har noen eksisterende prosjekter.</span><span class="sxs-lookup"><span data-stu-id="57078-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="57078-122">Konfigurere parametere for prosjektstyring og regnskap</span><span class="sxs-lookup"><span data-stu-id="57078-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="57078-123">Hver juridiske enhet som bruker Project Operations i Dynamics 365 Customer Engagement, trenger et sett med standardparametere.</span><span class="sxs-lookup"><span data-stu-id="57078-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="57078-124">Disse parameterne konfigureres på **Project Operations** -fanen på siden **Parametere for prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="57078-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="57078-125">Parameterne er:</span><span class="sxs-lookup"><span data-stu-id="57078-125">The parameters are:</span></span>

  - <span data-ttu-id="57078-126">**Faktureringstypestandarder** : Project Operations bruker et fast sett med faktureringstypestandarder som må tilordnes til linjeegenskaper i Finance.</span><span class="sxs-lookup"><span data-stu-id="57078-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="57078-127">Opprett en oppføring for hver faktureringstype: **Ikke angitt** , **Belastbar** , **Ikke-belastbar** , **Gratis** og **Ikke tilgjengelig**.</span><span class="sxs-lookup"><span data-stu-id="57078-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="57078-128">**Prosjektkategoristandarder** : Velg standard prosjektkategorier som skal brukes for hver transaksjonstype.</span><span class="sxs-lookup"><span data-stu-id="57078-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="57078-129">Disse standardene brukes i **Journal for Project Operations-integrering** og i beregninger der det ikke er angitt en transaksjonskategori for det faktiske prosjektet.</span><span class="sxs-lookup"><span data-stu-id="57078-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="57078-130">**Prognoser** : Velg prognosemodellen som skal brukes for tids- og utgiftsestimater.</span><span class="sxs-lookup"><span data-stu-id="57078-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
