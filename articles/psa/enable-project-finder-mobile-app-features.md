---
title: Aktivere funksjonene i Project Finder Mobile-appen
description: Slik aktiverer du funksjonene i Project Finder Mobile-appen for Project Service
author: JohnPBurrows
ms.prod: ''
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
ms.openlocfilehash: 8651ba591853faf648587dcbd4c50625ba94360958d7b418e89aa0bf09464a89
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004908"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Aktivere funksjonene i Project Finder Mobile-appen (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ressursene dine kan bruke Project Finder Mobile-appen på telefoner med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] for å finne nye prosjekter å arbeide med og oppdatere sine ferdigheter.  
  
 Appen er tilgjengelig for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefoner og [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
    
 Hvis du vil tillate at brukere viser prosjektressurskrav og oppdaterer ferdigheter, må alternativer velges i parameterinnstillingene for organisasjonsenheten.
  
> [!NOTE]
>  Project Finder Mobile-appen fungerer bare med [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], ikke med lokale installasjoner.  
  
1. Gå til **Project Service > Parametere**.  
  
2. Velg parameterne du vil bruke for å tillate funksjonene i Project Finder Mobile-appen.  
  
3. I **Generelt**-området setter du **Ressurskrav synlige for ressurser** til **Ja**.  
  
4. Sett **Tillat at ressurser oppdaterer ferdigheter** til **Ja**.  
  
   ![ProjectService_ProjectFinderEnable.](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Dette er en global innstilling. Prosjektledere kan angi om et enkelt prosjekt skal vises på dette prosjektets **Prosjektteam**-side.  
  
   ![ProjectService_ProjectTeamVisible.](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-postvarslinger  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sender e-post om ressursforespørsler til følgende mottakere på følgende tidspunkt:  
  
|Mottaker|Seminar/konferanse|  
|---------------|-----------|  
|Prosjektleder|- En ressurs registrerer seg for et prosjekt med Project Finder Mobile-appen.|  
|Ressurs|- Prosjektarbeidet som ressursen har registrert seg for, er allerede utført av en annen ressurs.<br />- Forespørselen om ferdighetsgodkjenning er godkjent eller avvist.<br />- Forespørselen om prosjektregistrering er godkjent eller avvist.|  
  
## <a name="privacy-notice"></a>Personvernerklæring  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Se også  
 [Definere ressurser](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]