---
title: Prosjektmaler
description: Dette emnet gir informasjon om hvordan du bruker prosjektmaler for et raskt prosjektoppsett.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: db42c9ea7280274cdc9cc90f1487f27e08f892e5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148070"
---
# <a name="project-templates"></a>Prosjektmaler 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En prosjektmal er et forhåndsdefinert rammeverk som hjelper deg med å starte et prosjekt raskt og enkelt. Du kan bruke en forhåndsdefinert mal til å opprette et nytt prosjekt med ett klikk. Som for prosjekter må du definere forhåndskravene for prosjektmaler. Du må definere en prosjektkalender for hver prosjektmal, og roller og prislister må være forhåndsdefinert i organisasjonen, slik at komponentene i malen har nyttige data.

En prosjektmal består av tre komponenter: en tidsplan, prosjektestimater og prosjektteammedlemmer.

## <a name="schedule"></a>Tidsplan

En tidsplan i en prosjektmal har samme sett elementer som en tidsplan i et prosjekt. Du kan opprette et oppgavehierarki, tilordne roller til oppgaver, definere attributter for tidsplan og angi avhengigheter. En tidsplan i en prosjektmal støtter også oppgavemoduser for hver oppgave. Den støtter derfor planleggingsmotoren. Du må knytte en prosjektkalender til prosjektet. Når du oppretter en arbeidsplan, er det ingen forskjell mellom en prosjektmal og et prosjekt.

## <a name="project-estimates"></a>Prosjektestimater

Prosjektestimater i en prosjektmal fungerer på samme måte som prosjektestimater i et prosjekt. Kostnads- og salgsprisene trekkes imidlertid fra standard kostnads- og salgsprislistene som er definert i parameterne.

## <a name="creating-a-project-from-a-template"></a>Opprette et prosjekt fra en mal
 
Det finnes flere måter å opprette et prosjekt på fra en prosjektmal:

- Når du oppretter et prosjekt fra et tilbud, kan du velge en prosjektmal i dialogboksen **Hurtigoppretting: Prosjekt**.

> ![Dialogboksen Hurtigoppretting: Prosjekt](media/project-11.png)

- Når du oppretter et prosjekt ved å velge **Nytt prosjekt**, vises **Prosjekt**-siden før oppføringen lagres. I feltet **Velg en mal** velger du en av de forhåndsdefinerte prosjektmalene i organisasjonen.
- Bruk **Opprett prosjekt fra mal** på siden **Malenhet**.

## <a name="copying-components-of-template-to-project"></a>Kopiere komponenter i en mal til et prosjekt

Når du kopierer komponentene i en prosjektmal til et prosjekt, kan det oppstå noen overstyringer, avhengig av innstillingene i prosjektet.

### <a name="copying-the-schedule"></a>Kopiere tidsplanen

Når du kopierer tidsplanen fra en prosjektmal, hvis prosjektet har en annen prosjektkalender enn malen, brukes arbeidstimene fra prosjektkalenderen på tidsplanen for oppgavene. Dette justerer tidsplanen til reserveprosjektkalenderen. På samme måte tar den første oppgaven i tidspnalen prosjektets startdato, og tidsplanen for resten av oppgavehierarkiet oppdateres basert på varigheten og avhengighetene som er angitt i malen. 

### <a name="copying-project-estimates"></a>Kopiere prosjektestimater 

Når du kopierer på tvers av prosjektestimatlinjer, oppdateres prislistene. For kostnadsprislisten er disse oppdateringene basert på den eiende enheten til prosjektet. For salgsprislisten er de basert på kunden. For prosjekter som er knyttet til en salgsenhet, bestemmes enhetskosten og salgsprisene basert på disse prislistene.

### <a name="copying-a-project-team"></a>Kopiere et prosjektteam

Når et prosjektteam kopieres fra en prosjektmal til et prosjekt, kopieres de generelle ressursene, sammen med ferdighetene og kompetansene som er definert i malen. Tildeling av generelle ressurser blir også vedlikeholdt slik som i prosjektmalen. Navngitte ressurser støttes ikke i prosjektmaler.


[!INCLUDE[footer-include](../includes/footer-banner.md)]