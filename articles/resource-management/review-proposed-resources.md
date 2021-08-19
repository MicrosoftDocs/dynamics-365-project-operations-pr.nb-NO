---
title: Se gjennom foreslåtte ressurser
description: Dette emnet gir informasjon om hvordan du foreslår prosjektressurser.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a9d3f7b9194b29859ee1479fea8158067e22e819e8f190ef1659e14b7c0cd6b5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998023"
---
# <a name="review-proposed-resources"></a>Se gjennom foreslåtte ressurser

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Ressursledere kan foreslå en ressurs til prosjektlederen ved å bruke en ressursforespørsel.

1. Fra rutenettet med forspørsler eller fra selve forespørselen velger du **Søk etter ressurser**.
2. På siden **Planleggingsassistent** velger du ressursen, og deretter i ruten **Opprett ressursbestilling**, i feltet **Bestillingsstatus**, velger du **Bestill**.

Følgende statusoppdateringer inntreffer:

- På siden **Planleggingsassistent** oppdateres statusindikatorene for å indikere at bestillingen er foreslått, ikke forpliktende bestilt.
- I ressursforespørselen endres statusen til **Må gjennomgås**.
- I kategorien **Team** i prosjektet endres verdien for det generelle teammedlemmets **Forespørselsstatus** til **Må gjennomgås**.

Prosjektlederen kan enten godta eller avvise forslaget.

Når ressursledere behandler ressursforespørsler, kan de bruke én av følgende metoder:

- Foreslå flere ressurser for å tilfredsstille behovet hvis det ikke er noen enkelt ressurs tilgjengelig for å oppfylle de nødvendige timene. Foreslåtte timer deles deretter mellom flere ressurser som kan oppfylle de nødvendige timene. I dette scenariet kan ikke timene overlappe.
- Foreslå færre ressurser enn nødvendig. I dette scenariet er den foreslåtte ressurskapasiteten mindre enn de påkrevde timene som er angitt. Når anmoderen godtar de foreslåtte ressursene, opprettes det derfor et ressurskrav som ikke er fullført, for å fange opp det gjenstående behovet.
- Bestille flere ressurser for å tilfredsstille behovet hvis det ikke er noen enkelt ressurs tilgjengelig for å utføre arbeidet.
- Bestille færre ressurser enn nødvendig. I dette scenariet er de bestilte timene færre enn de obligatoriske timene. Systemet veileder deg om hvordan du foreslår ressurser i stedet for bestillinger, slik at anmoderen kan kontrollere og holde oversikt over gjenstående behov.

## <a name="resource-availability"></a>Ressurstilgjengelighet

Det er svært viktig at ressurslederne kan vise tilgjengeligheten til ressurser og oppdatere bestillinger. I noen tilfeller er det ingen formell etterspørsel (ressursforespørsel), men en ressursleder må reagere på et ikke-planlagt behov som kommer gjennom kanaler, for eksempel en e-postmelding, telefonsamtale eller direkte melding. Ressursledere bruker planleggingstavlen til å oppdatere ressurser og bestillinger.

Arbeidstimer for ressursen brukes som grunnlag for beregning av tilgjengeligheten for en ressurs. Ressursbestillinger opptar kapasiteten til ressursene.

Planleggingstavlen bruker farger og skyggelegging til å vise bestillinger, tilgjengelighet og overbestillinger, samt statusen til bestillinger. Ved hjelp av en innstilling for planleggingstavlen kan du vise en forklaring.

Hvis en pil mot høyre vises ved siden av en individuell bestillbar ressurs på planleggingstavlen, kan ressursen utvides for å vise detaljer om arbeidet som er bestilt av ressursen.

Ettersom Dynamics 365 Project Operations bruker Universal Resource Scheduling-motoren, hvis du også har Dynamics 365 Field Service installert, kan du vise detaljene for ressursbestillinger for prosjekter, arbeidsordrer og alle andre enheter du har utvidet planlegging til.

Hvis du vil vise flere detaljer om en individuell ressurs, høyreklikker du den for å åpne ressurskortet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]