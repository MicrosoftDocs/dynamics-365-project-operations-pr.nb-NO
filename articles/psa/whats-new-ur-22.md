---
title: Hva er nytt eller endret i Project Service Automation Update Release 22, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 22, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081568"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation, Update Release 22, V3

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 22. Denne versjonen har et build-nummer på V 3.10.33.48 og er generelt tilgjengelig via en egen oppdatering i juni 2020.

## <a name="update-release-22"></a>Update Release 22

### <a name="bug-fixes"></a>Feilrettinger



**Tid og utgift**

Følgende problemer har blitt løst:

- **Tidsoppføringer** legges ikke til automatisk i tidsplanen for tidsoppføringer etter importen.
- Datovelgerrutenettet for **Tidsoppføring** gjenkjenner ikke brukerens regionale innstillinger.

**Ressursbehandling**

Følgende problemer har blitt løst:

- I manuell modus gjenkjennes ikke endringer i **Ressurstilordning** -konturer ved generering av **Ressurskrav**.
- **Ressursforespørsler** støtter ikke egendefinerte forespørselsstatuser.

**Prosjektledelse**

Følgende problemer har blitt løst:

- Bruk av dobbeltklikking på EstimateGridControl analyserer ikke nederlandske formatnumre riktig.
- Tildelte timer oppdateres ikke riktig når tilordninger endres ved hjelp av Microsoft Project-klienttilleggsprogrammet for stasjonære datamaskiner.
- Rutenettet for Prosjektsporing og Estimater viser feil salgsvalutakode når kontraktvaluta er forskjellig fra kundevalutaen, og organisasjonen er konfigurert til å vise valutakoder i stedet for valutasymboler.
- Sluttdatoen for et teammedlem vil legge til én dag hvis tidsplanen for arbeidstimer er 24 timer per dag.
- Når du legger til en transaksjonskategori i en oppgave i prosjektplanen, utløses ikke automatisk lagring.
- Følgende feil vises når du legger til et teammedlem i prosjektmalen: "Ressurskrav kan ikke knyttes til prosjektmaler". 
- Skript på båndregel "msdyn.Approval.CanApproveOrReject" viser en tidsavbruddsfeil.

**Sales**

Følgende problemer har blitt løst:

- Valideringsfeilmelding vises ikke når en kostprisliste er valgt i prislisteoppslag i skjema/enhet for ny prosjektprisliste for tilbud.
- Hvis du lukker tilbudet som vunnet, går det ikke videre til den opprettede kontrakten hvis en BPF som er knyttet til tilbudet, er i det siste trinnet.
- Tilbakeføring av **Ufakturert salg** er koblet til opprinnelig kostnad når en tidsoppføring blir tilbakekalt.
- Når du har valgt **Bekreft** -knappen, endres ikke fakturastatusen til **Bekreftet** med mindre fakturaen oppdateres.
