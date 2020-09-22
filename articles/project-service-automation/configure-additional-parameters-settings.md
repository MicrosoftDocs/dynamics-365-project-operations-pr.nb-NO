---
title: Konfigurere innstillinger for flere parametere
description: Slik konfigurerer du flere parameterinnstillinger i Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: de2fe830-4313-4711-b03b-76d56bf56cb6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: f3e110163088f8e3b78da9f273113d74775bf24c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754209"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Konfigurere flere parameterinnstillinger (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Når du har konfigurert elementene i tidligere emner, må du angi flere prosjektparametere som skal brukes for prosjekter. Da du installerte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] for første gang, opprettet du en parameterinnstilling for først å opprette alle oppføringer som kreves for at [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] skal fungere. Nå er det på tide å gå tilbake og konfigurere flere felt for disse innstillingene.  
  
 Må du ha konfigurert følgende innstillinger:  
  
-   Organisasjonsenhet  
  
-   Fakturafrekvens  
  
-   Mal for arbeidstimer  
  
-   Prisliste  
 
I dette trinnet skal du også angi hvilken type ressurstildeling du ønsker:  
  
- **Sentralt**. Bare ressursansvarlige kan tildele ressurser til prosjekter.  
  
- **Hybrid**. Ressursansvarlige, prosjektledere og regnskapsansvarlige kan tildele ressurser til prosjekter.  
  
 
Slik angir du prosjektparametere:  
  
1. Gå til **Project Service > Parametere**.  
  
2. Klikk parameterinnstillingen du vil konfigurere (den ene du opprettet da du installerte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]for første gang), eller klikk **Ny** for å opprette en ny.  
  
3. I **Generelt**-området angir du alle alternativene for prosjektparameterne.  
  
4. I **Prisliste**-området klikker du **+** for å legge til en prisliste, velger en prisliste i rullegardinlisten **Prisliste for prosjektparameter** og klikker deretter **Lagre**.  
  
5. Klikk **Lagre** nederst til høyre på skjermen.  

> [!NOTE]
> Prosjektparameteroppføringen må opprettholdes for at Project Service skal fungere riktig. Denne oppføringen bør ikke slettes.

### <a name="see-also"></a>Se også  
 [Definere ressurser](../project-service/set-up-resources.md)
