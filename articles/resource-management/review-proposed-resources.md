---
title: Se gjennom foreslåtte ressurser
description: Dette emnet gir informasjon om hvordan du foreslår prosjektressurser.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897373"
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

## <a name="billable-utilization"></a>Fakturerbar utnyttelse

Ressurser kan ha fakturerbar utnyttelse som mål. Denne målutnyttelsen er definert som et attributt i standardrollen til en ressurs eller angitt i oppføringen for en enkelt bestillbar ressurs. Utnyttelsesberegninger er basert på de faktiske timene ressursene har rapportert ved hjelp av godkjente tidsoppføringer.

Følgende formler brukes til å beregne utnyttelse:

- Fakturerbar utnyttelse = belastbare faktiske timer ÷ ressurskapasitet
- Ikke-fakturerbar utnyttelse = faktisk tid med faktureringstype-ID = ikke-belastbar, komplementær eller ikke tilgjengelig ÷ ressurskapasitet
- Intern = faktisk tid uten salgskontrakt ÷ ressurskapasitet
- Ressurskapasitet = arbeidstimer for ressursen – fravær – ikke-arbeidsdager

Du kan finne visningen **Ressursutnyttelse** i **Ressurser**-ruten.

Hver celle i rutenettet representerer den fakturerbare utnyttelsesprosenten for ressursen i en periode, for eksempel en dag, uke eller måned. Følgende formler brukes til å fargelegge cellene:

- **Grønn:** fakturerbar utnyttelse \>= ressursmålutnyttelse
- **Gul:** målutnyttelse – 20 \<= fakturerbar utnyttelse \< målutnyttelse
- **Rød:** fakturerbar utnyttelse \< målutnyttelse – 20.

Siden visningen **Ressursutnyttelse** er basert på planleggingstavlen, kan du bruke filtreringsfunksjonene på planleggingstavlen til å filtrere resultatene.

Rutenettet krever at du angir en målutnyttelse for rollen eller den individuelle ressursen. Du kan sette opp dette ved å gå til **Ressurser** \> **Ressursroller**.

I tillegg må en standardrolle tilordnes til hver bestillbare ressurs. Gå til **Ressurser** \> **Ressurser**. I kategorien **Project Service** kontrollerer du at det er definert en ressursrolle, og at **Er standard**-feltet er satt til **Ja**. Du kan legge til flere roller der **Er standard = Nei**. Rollen der **Er standard = Ja** brukes til å evaluere ressursens utnyttelse mot målet for den aktuelle rollen.

I kategorien **Project Service** kan du også angi en individuell målutnyttelse for ressursen. Beregningen av utnyttelsen bruker deretter denne målutnyttelsen til å evaluere ressursens mål i stedet for målet for standardrollen for ressursen.

Utnyttelse vises bare for en ressurs hvis ressursen har godkjent, belastbar tid i perioden som vises i rutenettet.

## <a name="resource-availability"></a>Ressurstilgjengelighet

Det er svært viktig at ressurslederne kan vise tilgjengeligheten til ressurser og oppdatere bestillinger. I noen tilfeller er det ingen formell etterspørsel (ressursforespørsel), men en ressursleder må reagere på et ikke-planlagt behov som kommer gjennom kanaler, for eksempel en e-postmelding, telefonsamtale eller direkte melding. Ressursledere bruker planleggingstavlen til å oppdatere ressurser og bestillinger.

Arbeidstimer for ressursen brukes som grunnlag for beregning av tilgjengeligheten for en ressurs. Ressursbestillinger opptar kapasiteten til ressursene.

Planleggingstavlen bruker farger og skyggelegging til å vise bestillinger, tilgjengelighet og overbestillinger, samt statusen til bestillinger. Ved hjelp av en innstilling for planleggingstavlen kan du vise en forklaring.

Hvis en pil mot høyre vises ved siden av en individuell bestillbar ressurs på planleggingstavlen, kan ressursen utvides for å vise detaljer om arbeidet som er bestilt av ressursen.

Ettersom Dynamics 365 Project Operations bruker Universal Resource Scheduling-motoren, hvis du også har Dynamics 365 Field Service installert, kan du vise detaljene for ressursbestillinger for prosjekter, arbeidsordrer og alle andre enheter du har utvidet planlegging til.

Hvis du vil vise flere detaljer om en individuell ressurs, høyreklikker du den for å åpne ressurskortet.

