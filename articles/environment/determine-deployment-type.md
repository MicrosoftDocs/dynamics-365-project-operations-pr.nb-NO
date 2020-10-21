---
title: Distribusjonstyper
description: Dette emnet gir informasjon som hjelper deg med å bestemme riktig distribusjonstype for prosjektoperasjoner for firmaet ditt.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948998"
---
# <a name="deployment-types"></a>Distribusjonstyper

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

> [!IMPORTANT]
> Når du har kjøpt lisensen, starter du her for å finne den beste distribusjonsmodellen for Dynamics 365 Project Operations ved å bruke den [veiledede installasjonsflyten](https://aka.ms/provisionprojectoperations).
> Når du har fullført den veiledede installasjonsflyten, blir du dirigert til riktig administrasjonsportal for å fullføre installasjonen. Se distribusjonsdetaljene nedenfor for å fullføre installasjonen.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Eksisterende kunder av Dynamics som bruker Dynamics 365 Project Service Automation
Prosjekt Operations inkluderer funksjonene som leveres med Project Service Automation. En oppgraderingsbane blir utgitt for disse kundene i fremtiden.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Eksisterende kunder av Dynamics 365 Finance som bruker prosjektstyring og regnskap 

Eksisterende kunder av Finance som bruker prosjektstyrings og regnskap, kan fortsette å bruke dette som de er. Se [Project Operations for lagerførte scenarioer / produksjonsordrescenarioer](#pma).

Project Operations støtter flere distribusjonsalternativer for å dekke dine behov. Enten du er en ny eller eksisterende Dynamics 365-kunde, kan Project Operations støtte dine behov.

[Spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations) hjelper deg med å finne riktig distribusjon. Resultatene leder deg mot én av følgende distribusjonstyper:

- [Lite-distribusjon – avtale til proformafakturering](#lite)
- [Project Operations for ressursbaserte/ikke-lagerførte scenarioer](#integrated)
- [Project Operations for lagerførte scenarioer / produksjonsordrescenarioer](#pma)

Project Operations støtter lagerførte scenarioer / produksjonsordrescenarioer og ordre scenarioer og ikke-lagerbaserte/ressursbaserte scenarioer i samme miljø ved hjelp av konfigurasjoner på juridisk enhetsnivå. Contoso kan for eksempel dra nytte av funksjoner for lagerbasert/produksjonsordre i amerikanske produksjonsanlegg (juridisk enhet = Contoso Manufacturing United States), og ikke-lagerbaserte/ressursbaserte funksjoner i Contoso Robotics Arms vedlikeholdsanlegg i Storbritannia (juridisk enhet = Contoso Robotics United Kingdom).

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>Lite-distribusjon – avtale til proformafakturering
Lite-distribusjonen omfatter følgende funksjoner:

- Prosjektplanlegging ved hjelp av Microsoft Project for Internett
- Flerdimensjonal prising
- Enhetlig ressursstyring
- Tidssporing
- Grunnleggende utgift
- Fakturaforslag

### <a name="deployment-steps"></a>Distribusjonstrinn:
Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).

For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](lite-preview-subscription-sign-up.md) og [Klargjøre nytt miljø](lite-deployment.md). 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>Project Operations for ressursbaserte/ikke-lagerførte scenarioer
Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer inkluderer følgende funksjoner:
  
- Prosjektplanlegging ved hjelp av Microsoft Project for Internett
- Flerdimensjonal prising
- Enhetlig ressursstyring
- Tidssporing
- Grunnleggende utgift
- Fullstendig utgift
- Mottak av OCR
- Full fakturering
- Inntektsføring

### <a name="deployment-steps"></a>Distribusjonstrinn:
Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).

For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](resource-sign-up-preview-subscription.md) og [Klargjøre nytt miljø](resource-provision-new-environment.md). 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations for lagerførte scenarioer / produksjonsordrescenarioer

- Prosjektplanlegging ved hjelp av WBS
- Ressursbehandling
- Tidssporing
- Fullstendig utgift
- Mottak av OCR
- Full fakturering
- Inntektsføring
- Produksjonsordrer
- Støtte for materiell

### <a name="deployment-steps"></a>Distribusjonstrinn:
Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).

For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) og [Klargjøre nytt miljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



