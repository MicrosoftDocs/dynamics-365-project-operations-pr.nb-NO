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
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Aktivere funksjonene i Project Finder Mobile-appen (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ressursene dine kan bruke Project Finder Mobile-appen på telefoner med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] for å finne nye prosjekter å arbeide med og oppdatere ferdighetssett.  
  
 Appen er tilgjengelig for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefoner og [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Du må angi et par alternativer i parameterinnstillingen organisasjonsenheten, slik at brukerne kan vise prosjektenes ressurskrav og oppdatere sine kunnskaper.  
  
> [!NOTE]
>  Project Finder Mobile-appen fungerer bare med [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], ikke med lokale installasjoner.  
  
1. Gå til **Project Service > Parametere**.  
  
2. Velg parameterne du vil bruke for å tillate funksjonene i Project Finder Mobile-appen.  
  
3. I **Generelt**-området setter du **Ressurskrav synlige for ressurser** til **Ja**.  
  
4. Sett **Tillat at ressurser oppdaterer ferdigheter** til **Ja**.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Dette er en global innstilling. Prosjektledere kan angi om et enkelt prosjekt skal vises på dette prosjektets **Prosjektteam**-side.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-postvarslinger  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sender e-post om ressursforespørsler til følgende mottakere på følgende tidspunkt:  
  
|Mottaker|Seminar/konferanse|  
|---------------|-----------|  
|Prosjektleder|-   Når en ressurs registrerer seg for et prosjekt med Project Finder Mobile-appen.|  
|Ressurs|-   Når prosjektarbeidet ressursen har registrert seg for, allerede er utført av en annen ressurs.<br />-   Når forespørselen om kompetansegodkjenning er godkjent eller avvist.<br />-   Når forespørselen om prosjektregistrering er godkjent eller avvist.|  
  
## <a name="privacy-notice"></a>Personvernerklæring  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Se også  
 [Definere ressurser](../project-service/set-up-resources.md)
