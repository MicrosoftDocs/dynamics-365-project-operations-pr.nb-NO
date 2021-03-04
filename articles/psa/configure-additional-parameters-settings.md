---
title: Konfigurere innstillinger for flere parametere
description: Slik konfigurerer du flere parameterinnstillinger i Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73264845808e12950a48eea2b79e54c393d9c024
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151580"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="afbbb-103">Konfigurere flere parameterinnstillinger (Project Service)</span><span class="sxs-lookup"><span data-stu-id="afbbb-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="afbbb-104">Når du har konfigurert elementene i tidligere emner, må du angi flere prosjektparametere som skal brukes for prosjekter.</span><span class="sxs-lookup"><span data-stu-id="afbbb-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="afbbb-105">Da du installerte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] for første gang, opprettet du en parameterinnstilling for først å opprette alle oppføringer som kreves for at [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] skal fungere.</span><span class="sxs-lookup"><span data-stu-id="afbbb-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="afbbb-106">Nå er det på tide å gå tilbake og konfigurere flere felt for disse innstillingene.</span><span class="sxs-lookup"><span data-stu-id="afbbb-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="afbbb-107">Må du ha konfigurert følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="afbbb-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="afbbb-108">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="afbbb-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="afbbb-109">Fakturafrekvens</span><span class="sxs-lookup"><span data-stu-id="afbbb-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="afbbb-110">Mal for arbeidstimer</span><span class="sxs-lookup"><span data-stu-id="afbbb-110">Work hours template</span></span>  
  
-   <span data-ttu-id="afbbb-111">Prisliste</span><span class="sxs-lookup"><span data-stu-id="afbbb-111">Price list</span></span>  
 
<span data-ttu-id="afbbb-112">I dette trinnet skal du også angi hvilken type ressurstildeling du ønsker:</span><span class="sxs-lookup"><span data-stu-id="afbbb-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="afbbb-113">**Sentralt**.</span><span class="sxs-lookup"><span data-stu-id="afbbb-113">**Central**.</span></span> <span data-ttu-id="afbbb-114">Bare ressursansvarlige kan tildele ressurser til prosjekter.</span><span class="sxs-lookup"><span data-stu-id="afbbb-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="afbbb-115">**Hybrid**.</span><span class="sxs-lookup"><span data-stu-id="afbbb-115">**Hybrid**.</span></span> <span data-ttu-id="afbbb-116">Ressursansvarlige, prosjektledere og regnskapsansvarlige kan tildele ressurser til prosjekter.</span><span class="sxs-lookup"><span data-stu-id="afbbb-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="afbbb-117">Slik angir du prosjektparametere:</span><span class="sxs-lookup"><span data-stu-id="afbbb-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="afbbb-118">Gå til **Project Service > Parametere**.</span><span class="sxs-lookup"><span data-stu-id="afbbb-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="afbbb-119">Klikk parameterinnstillingen du vil konfigurere (den ene du opprettet da du installerte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]for første gang), eller klikk **Ny** for å opprette en ny.</span><span class="sxs-lookup"><span data-stu-id="afbbb-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="afbbb-120">I **Generelt**-området angir du alle alternativene for prosjektparameterne.</span><span class="sxs-lookup"><span data-stu-id="afbbb-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="afbbb-121">I **Prisliste**-området klikker du **+** for å legge til en prisliste, velger en prisliste i rullegardinlisten **Prisliste for prosjektparameter** og klikker deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="afbbb-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="afbbb-122">Klikk **Lagre** nederst til høyre på skjermen.</span><span class="sxs-lookup"><span data-stu-id="afbbb-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="afbbb-123">Prosjektparameteroppføringen må opprettholdes for at Project Service skal fungere riktig.</span><span class="sxs-lookup"><span data-stu-id="afbbb-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="afbbb-124">Denne oppføringen bør ikke slettes.</span><span class="sxs-lookup"><span data-stu-id="afbbb-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="afbbb-125">Se også</span><span class="sxs-lookup"><span data-stu-id="afbbb-125">See Also</span></span>  
 [<span data-ttu-id="afbbb-126">Definere ressurser</span><span class="sxs-lookup"><span data-stu-id="afbbb-126">Set up resources</span></span>](../psa/set-up-resources.md)
