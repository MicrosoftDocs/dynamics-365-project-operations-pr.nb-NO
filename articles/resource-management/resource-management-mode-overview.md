---
title: Oversikt over modi for ressursstyring
description: Dette emnet gir informasjon om ressursstyringsfunksjonaliteten i Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279465"
---
# <a name="resource-management-modes-overview"></a>Oversikt over modi for ressursstyring

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_


Dynamics 365 Project Operations støtter to moduser for at du skal kunne kjøre den totale bestillingsflyten. Administrasjonsmodusen defineres som en prosjektparameter og kan endres hvis forretningsbehovene endres.    

## <a name="central-mode"></a>Sentral modus
Organisasjoner som sentraliserer fordelingen av ressurser til prosjekter, kan bruke sentral modus til å sørge for at prosjektledere kan definere ressurskrav på prosjektnivå. Innfrielse av ressurskravene er delegert til en ressursleder. Prosjektledere kan godta eller avvise ressurser som er foreslått av ressurslederen.

![Sentral modus](./media/resource-management-central.png)

Hvis du vil administrere ressurser med sentral modus, kan du se følgende:

- [Tilordne generelt bestillbare ressurser til en oppgave og generere ressurskrav](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Bestille navngitte ressurser fra ressurskrav](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Sende en ressursforespørsel](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Oppfyll en ressursforespørsel](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Godta eller avvise en foreslått prosjektressurs fra en ressursforespørsel](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybrid modus
Organisasjoner som trenger fleksibilitet ved tildeling av ressurser, kan bruke hybrid modus til å sørge for at både prosjektledere og ressursledere kan bestille ressurser.

![Hybrid modus](./media/resource-management-hybrid.png)

I tillegg til de støttede prosessene i sentral modus, kan du se følgende emner for å administrere alle andre støttede bestillingsflyter i hybrid modus:

Bestill en ressurs direkte til et prosjekt:
- [Bestille navngitte bestillbare ressurser til et prosjektteam og tilordne oppgaver](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Bestill en ressurs fra et ressurskrav:
- [Tilordne generelt bestillbare ressurser til en oppgave og generere ressurskrav](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Bestille navngitte ressurser fra ressurskrav](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]