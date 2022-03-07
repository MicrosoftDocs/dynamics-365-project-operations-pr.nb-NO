---
title: Integrasjonsparametere for Project Service Automation
description: Dette emnet forklarer hvordan du konfigurerer hvordan standarddata skrives inn når du integrerer Microsoft Dynamics 365 for Project Service Automation med Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b58f34cb74be531a98518100158f39d74f136afc34444468d666cd4e9394af6f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005853"
---
# <a name="project-service-automation-integration-parameters"></a>Integrasjonsparametere for Project Service Automation

[!include[banner](../includes/banner.md)]

På siden **Integrasjonsparametere for Project Service Automation** kan du konfigurere hvordan standarddata skrives inn når du integrerer Dynamics 365 Project Service Automation med Dynamics 365 Finance. For at prosjekter skal kunne synkroniseres fra Project Service Automation til Finance, må du angi følgende felt:

Hvis du vil åpne siden **Integrasjonsparametere for Project Service Automation**, går du til **Prosjektstyring og regnskap** \> **Oppsett** \> **Integrasjonsparametere for Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeoverslag, utgiftsoverslag og låsing av funksjoner er tilgjengelig i versjon 8.0.
> - Integrering av faktiske data er tilgjengelig i versjon 8.0.1 eller senere.


| Tabulator                    | Felt                | Beskrivelse |
|------------------------|----------------------|-------------|
| Generelt                | Standardprosjekttype | Velg standardprosjekttypen. Når prosjekter synkroniseres fra Project Service Automation, brukes denne verdien hvis du ikke oppgav en standardverdi i integreringsmalen. Under synkroniseringen angis feltet **Prosjekttype** i nye prosjekter til denne verdien. Verdien kan imidlertid oppdateres når prosjektkontraktlinjene synkroniseres fra Project Service Automation. |
|                        | Tidskategori        | Velg standard tidskategori. Denne verdien brukes når timeoverslag synkroniseres fra Project Service Automation. Når timeberegningene og faktiske timeverdier synkroniseres fra Project Service Automation, settes **Kategori**-feltet for nye prosjekttimeprognoser i Finance til denne verdien. |
|                        | Gebyrkategori         | Velg standard gebyrkategori. Denne verdien brukes når faktiske gebyrer synkroniseres fra Project Service Automation. Når faktiske gebyrer synkroniseres fra Project Service Automation, settes **Kategori**-feltet for nye gebyrtransaksjoner i Finance til denne verdien. |
| Projektgruppestandarder | Prosjekttype         | Klikk **Ny** for å legge til en rad der du kan velge prosjekttypen du vil angi standard prosjektgruppe for. En bestemt prosjekttype kan bare velges én gang i konfigurasjonen. |
|                        | Prosjektgruppe        | Velg standard prosjektgruppe for den valgte prosjekttypen. Når nye prosjekter synkroniseres fra Project Service Automation, settes feltet **Prosjektruppe** til standardverdien for prosjekttypen hvis du ikke oppgav en standardverdi i integreringsmalen. |
| Faktureringstypestandarder  | Faktureringstype         | Klikk **Ny** for å legge til en rad der du kan velge faktureringstypen du vil angi standard linjeegenskap for. En bestemt faktureringstype kan bare velges én gang i konfigurasjonen. |
|                        | Linjeegenskap        | Velg standard linjeegenskap for den valgte faktureringstypen. Når nye timeoverslag, nye utgiftsoverslag eller nye faktiske verdier synkroniseres fra Project Service Automation, settes **Linjeegenskap**-feltet til standardverdien for faktureringstypen. |
| Låsing av funksjoner  | Ikke aktuelt       | Velg funksjonaliteten for å deaktivere i Finance for prosjekter og kontrakter som opprinnelig kommer fra Project Service Automation. Du kan for eksempel deaktivere muligheten til å redigere kontrakter og prosjekter, opprette arbeidsnedbrytningsstrukturer og legge inn timeregistreringer i Finance. Regnskapsrelaterte felt vil fortsatt være aktivert, selv om de gjøres utilgjengelige av parameterinnstillingen. Alle funksjonene er aktivert som standard. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]