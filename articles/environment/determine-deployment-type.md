---
title: Fastslå distribusjonstypen
description: Dette emnet gir informasjon som hjelper deg med å bestemme riktig distribusjonstype for prosjektoperasjoner for firmaet ditt.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401230"
---
# <a name="determine-your-deployment-type"></a>Fastslå distribusjonstypen

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

> [!IMPORTANT]
> Når du har kjøpt lisensen, starter du her for å finne den beste distribusjonsmodellen for Dynamics 365 Project Operations ved å bruke den [veiledede installasjonsflyten](https://aka.ms/provisionprojectoperations).
> Når du har fullført den veiledede installasjonsflyten, blir du dirigert til riktig administrasjonsportal for å fullføre installasjonen. Se distribusjonsdetaljene for å fullføre installasjonen.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Eksisterende kunder av Dynamics som bruker Dynamics 365 Project Service Automation
Prosjekt Operations inkluderer funksjonene som leveres med Project Service Automation. En oppgraderingsbane blir utgitt for disse kundene i 2021-lanseringsbølge 1.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Eksisterende kunder av Dynamics 365 Finance som bruker prosjektstyring og regnskap 

Eksisterende kunder av Finance som bruker Prosjektstyring og regnskap-funksjonaliteten, kan fortsette å bruke den som den er. Se [Project Operations for lagerførte scenarioer / produksjonsordrescenarioer](#pma).


## <a name="deployment-types"></a>Distribusjonstyper
Project Operations støtter flere distribusjonsalternativer for å dekke dine behov. Enten du er en ny eller eksisterende Dynamics 365-kunde, kan Project Operations støtte dine behov.

[Spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations) hjelper deg med å finne riktig distribusjon. Resultatene leder deg mot én av følgende distribusjonstyper:

- [Lite-distribusjon – avtale til proformafakturering](#lite)
- [Project Operations for ressursbaserte/ikke-lagerførte scenarioer](#integrated)
- [Project Operations for lagerførte scenarioer / produksjonsordrescenarioer](#pma)

Project Operations støtter lagerførte scenarioer / produksjonsordrescenarioer og ordre scenarioer og ikke-lagerbaserte/ressursbaserte scenarioer i samme miljø ved hjelp av konfigurasjoner på juridisk enhetsnivå. Contoso kan for eksempel bruke funksjonene for lagerført/produksjonsordre på produksjonsanlegget i USA (juridisk enhet = Contoso Manufacturing United States). Contoso bruke funksjonene for ikke-lagerflrt/ressursbasert i Contoso Robotics Arms serviceanlegget i UK (juridisk enhet = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Lite-distribusjon – avtale til proformafakturering

Lite-distribusjonen omfatter følgende funksjoner:

- Salgsprosess for prosjekter som utvider Dynamics 365 Sales-programerfaringer
- Prosjektplanlegging ved hjelp av Microsoft Project for Internett
- Flerdimensjonal prising
- Enhetlig ressursstyring
- Tidssporing
- Grunnleggende utgift
- Proforma og kunderettet fakturering 

#### <a name="deployment-steps"></a>Trinn for distribusjon
Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).

For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](lite-preview-subscription-sign-up.md) og [Klargjøre nytt miljø](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations for ressursbaserte/ikke-lagerførte scenarioer
Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer inkluderer følgende funksjoner:
 
- Salgsprosess for prosjekter som utvider Dynamics 365 Sales-programmet
- Prosjektplanlegging ved hjelp av Microsoft Project for Internett
- Flerdimensjonal prising
- Enhetlig ressursstyring
- Tidssporing
- Grunnleggende utgift
- Fullstendig utgift
- Mottak av OCR
- Proforma og kunderettet fakturering 
- Inntektsføring for prosjekter

#### <a name="deployment-steps"></a>Trinn for distribusjon
Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).

For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](resource-sign-up-preview-subscription.md) og [Klargjøre nytt miljø](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations for lagerførte scenarioer / produksjonsordrescenarioer

- Prosjektplanlegging ved hjelp av WBS
- Ressursbehandling
- Tidssporing
- Fullstendig utgift
- Mottak av OCR
- Full fakturering
- Inntektsføring
- Produksjonsordrer
- Støtte for materiell

#### <a name="deployment-steps"></a>Trinn for distribusjon
Finn den beste distribusjonsmodellen for Project Operations ved hjelp av [spørreskjemaet for distribusjon](https://aka.ms/provisionprojectoperations).

For denne distribusjonen kan du se [Registrering for forhåndsversjonsbonnement](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) og [Klargjøre nytt miljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]