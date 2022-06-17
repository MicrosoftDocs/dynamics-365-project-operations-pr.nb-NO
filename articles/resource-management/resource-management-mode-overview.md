---
title: Oversikt over modi for ressursstyring
description: Denne artikkelen inneholder informasjon om funksjonen for ressursstyring i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928444"
---
# <a name="resource-management-modes-overview"></a>Oversikt over modi for ressursstyring

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_


Dynamics 365 Project Operations støtter to moduser for at du skal kunne kjøre den totale bestillingsflyten. Administrasjonsmodusen defineres som en prosjektparameter og kan endres hvis forretningsbehovene endres.    

## <a name="central-mode"></a>Sentral modus
Organisasjoner som sentraliserer fordelingen av ressurser til prosjekter, kan bruke sentral modus til å sørge for at prosjektledere kan definere ressurskrav på prosjektnivå. Innfrielse av ressurskravene er delegert til en ressursleder. Prosjektledere kan godta eller avvise ressurser som er foreslått av ressurslederen.

![Sentral modus.](./media/resource-management-central.png)

Hvis du vil administrere ressurser med sentral modus, kan du se følgende:

- [Tilordne generelt bestillbare ressurser til en oppgave og generere ressurskrav](/dynamics365/project-service/assign-generic-bookable-resource)
- [Bestille navngitte ressurser fra ressurskrav](/dynamics365/project-service/book-named-resource)
- [Sende en ressursforespørsel](/dynamics365/project-service/submit-resource-request)
- [Oppfyll en ressursforespørsel](/dynamics365/project-service/resource-management-fulfill-requests)
- [Godta eller avvise en foreslått prosjektressurs fra en ressursforespørsel](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybrid modus
Organisasjoner som trenger fleksibilitet ved tildeling av ressurser, kan bruke hybrid modus til å sørge for at både prosjektledere og ressursledere kan bestille ressurser.

![Hybrid modus.](./media/resource-management-hybrid.png)

I tillegg til den støttede prosessen for sentral modus kan du se følgende artikler for å administrere alle andre støttede bestillingsflyter i hybrid modus:

Bestill en ressurs direkte til et prosjekt:
- [Bestille navngitte bestillbare ressurser til et prosjektteam og tilordne oppgaver](/dynamics365/project-service/assign-named-bookable-resource)

Bestill en ressurs fra et ressurskrav:
- [Tilordne generelt bestillbare ressurser til en oppgave og generere ressurskrav](/dynamics365/project-service/assign-generic-bookable-resource)
- [Bestille navngitte ressurser fra ressurskrav](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]