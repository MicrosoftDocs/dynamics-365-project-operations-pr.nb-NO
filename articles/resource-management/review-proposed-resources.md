---
title: Se gjennom foreslåtte ressurser
description: Dette emnet gir informasjon om hvordan du foreslår prosjektressurser.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3d2ab3ba9e5b18a2b42acaa2dc51ad94b8189274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584976"
---
# <a name="review-proposed-resources"></a>Se gjennom foreslåtte ressurser

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Ressursledere kan foreslå en ressurs til prosjektlederen ved å bruke en ressursforespørsel.

Følg denne fremgangsmåten for å se gjennom foreslåtte ressurser:

1. Fra rutenettet **Forespørsler** eller fra selve forespørselen velger du **Søk etter ressurser**.
2. Velg ressursen på siden **Planleggingsassistent**, og bekreft deretter at alle foreslåtte timer er inkludert i den foreslåtte bestillingen.
3. I ruten **Opprett ressursbestilling** angir du feltet **Bestillingsstatus** til **Foreslått** og velger deretter **Bestill**.

    > [!NOTE]
    > Hvis du angir **bestillingsstatusen** er **Foreslått**, blir ikke ressursen forpliktende bestilt og erstatter ikke den generelle ressursen med det navngitte teammedlemmet.

    Følgende statusoppdateringer inntreffer:

    - På siden **Planleggingsassistent** oppdateres statusindikatorene for å indikere at bestillingen er foreslått, ikke forpliktende bestilt.
    - I ressursforespørselen endres statusen til **Må gjennomgås**.
    - I kategorien **Team** i prosjektet endres verdien for det generelle teammedlemmets **Forespørselsstatus** til **Må gjennomgås**.

Prosjektlederen kan godta eller avvise forslaget.

Når ressursledere behandler ressursforespørsler, kan de bruke én av følgende metoder:

- Foreslå flere ressurser for å tilfredsstille behovet hvis det ikke er noen enkelt ressurs tilgjengelig for å oppfylle de nødvendige timene. Foreslåtte timer deles deretter mellom flere ressurser som kan oppfylle de nødvendige timene. I dette scenariet kan ikke timene overlappe.
- Foreslå færre ressurser enn nødvendig. I dette scenariet er den foreslåtte ressurskapasiteten mindre enn de påkrevde timene som er angitt. Når anmoderen godtar de foreslåtte ressursene, opprettes det et ressurskrav som ikke er fullført, for å fange opp det gjenstående behovet.
- Bestille flere ressurser for å tilfredsstille behovet hvis det ikke er noen enkelt ressurs tilgjengelig for å utføre arbeidet.
- Bestill færre ressurser enn nødvendig. I dette scenariet er de bestilte timene færre enn de obligatoriske timene. Systemet veileder deg om hvordan du foreslår ressurser i stedet for bestillinger, slik at anmoderen kan kontrollere og holde oversikt over gjenstående behov.

## <a name="resource-availability"></a>Ressurstilgjengelighet

Ressurslederne må kunne vise tilgjengeligheten til ressurser og oppdatere bestillinger. I noen tilfeller er det ingen formelle behov (ressursforespørsel). En ressursleder må imidlertid svare på et ikke planlagt behov som kommer via andre kanaler, for eksempel e-postmeldinger, telefonsamtaler eller direktemeldinger. Ressursledere bruker **planleggingstavlen** til å oppdatere ressurser og bestillinger.

Arbeidstimer for ressursen brukes som grunnlag for å beregne tilgjengeligheten for en ressurs. Ressursbestillinger opptar kapasiteten til ressursene.

**Planleggingstavlen** bruker farger og skyggelegging til å vise bestillinger, tilgjengelighet og overbestillinger, samt statusen til bestillinger. Med en innstilling på **planleggingstavlen** kan du vise en forklaring.

Hvis en pil mot høyre vises ved siden av en individuell bestillbar ressurs på **planleggingstavlen**, kan ressursen utvides for å vise detaljer om arbeidet som er bestilt av ressursen.

Ettersom Dynamics 365 Project Operations bruker Universal Resource Scheduling-motoren, hvis du også har Dynamics 365 Field Service installert, kan du vise detaljene for ressursbestillinger for prosjekter, arbeidsordrer og alle andre enheter du har utvidet planlegging til.

Hvis du vil vise flere detaljer om en individuell ressurs, høyreklikker du den for å åpne ressurskortet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
