---
title: Aktivere funksjonene i Project Finder Mobile-appen
description: Slik aktiverer du funksjonene i Project Finder Mobile-appen for Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754050"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="27e75-103">Aktivere funksjonene i Project Finder Mobile-appen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="27e75-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="27e75-104">Ressursene dine kan bruke Project Finder Mobile-appen på telefoner med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] for å finne nye prosjekter å arbeide med og oppdatere ferdighetssett.</span><span class="sxs-lookup"><span data-stu-id="27e75-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="27e75-105">Appen er tilgjengelig for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefoner og [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="27e75-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="27e75-106">Du må angi et par alternativer i parameterinnstillingen organisasjonsenheten, slik at brukerne kan vise prosjektenes ressurskrav og oppdatere sine kunnskaper.</span><span class="sxs-lookup"><span data-stu-id="27e75-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="27e75-107">Project Finder Mobile-appen fungerer bare med [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], ikke med lokale installasjoner.</span><span class="sxs-lookup"><span data-stu-id="27e75-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="27e75-108">Gå til **Project Service > Parametere**.</span><span class="sxs-lookup"><span data-stu-id="27e75-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="27e75-109">Velg parameterne du vil bruke for å tillate funksjonene i Project Finder Mobile-appen.</span><span class="sxs-lookup"><span data-stu-id="27e75-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="27e75-110">I **Generelt**-området setter du **Ressurskrav synlige for ressurser** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="27e75-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="27e75-111">Sett **Tillat at ressurser oppdaterer ferdigheter** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="27e75-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="27e75-112">![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="27e75-112">![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="27e75-113">Dette er en global innstilling.</span><span class="sxs-lookup"><span data-stu-id="27e75-113">This is a global setting.</span></span> <span data-ttu-id="27e75-114">Prosjektledere kan angi om et enkelt prosjekt skal vises på dette prosjektets **Prosjektteam**-side.</span><span class="sxs-lookup"><span data-stu-id="27e75-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="27e75-115">![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="27e75-115">![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="27e75-116">E-postvarslinger</span><span class="sxs-lookup"><span data-stu-id="27e75-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="27e75-117">sender e-post om ressursforespørsler til følgende mottakere på følgende tidspunkt:</span><span class="sxs-lookup"><span data-stu-id="27e75-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="27e75-118">Mottaker</span><span class="sxs-lookup"><span data-stu-id="27e75-118">Recipient</span></span>|<span data-ttu-id="27e75-119">Seminar/konferanse</span><span class="sxs-lookup"><span data-stu-id="27e75-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="27e75-120">Prosjektleder</span><span class="sxs-lookup"><span data-stu-id="27e75-120">Project manager</span></span>|<span data-ttu-id="27e75-121">-   Når en ressurs registrerer seg for et prosjekt med Project Finder Mobile-appen.</span><span class="sxs-lookup"><span data-stu-id="27e75-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="27e75-122">Ressurs</span><span class="sxs-lookup"><span data-stu-id="27e75-122">Resource</span></span>|<span data-ttu-id="27e75-123">-   Når prosjektarbeidet ressursen har registrert seg for, allerede er utført av en annen ressurs.</span><span class="sxs-lookup"><span data-stu-id="27e75-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="27e75-124">-   Når forespørselen om kompetansegodkjenning er godkjent eller avvist.</span><span class="sxs-lookup"><span data-stu-id="27e75-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="27e75-125">-   Når forespørselen om prosjektregistrering er godkjent eller avvist.</span><span class="sxs-lookup"><span data-stu-id="27e75-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="27e75-126">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="27e75-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="27e75-127">Se også</span><span class="sxs-lookup"><span data-stu-id="27e75-127">See Also</span></span>  
 [<span data-ttu-id="27e75-128">Definere ressurser</span><span class="sxs-lookup"><span data-stu-id="27e75-128">Set up resources</span></span>](../project-service/set-up-resources.md)
