---
title: Foreslå prosjektressurser
description: Dette emnet gir informasjon om hvordan du foreslår prosjektressurser.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 2003f6f06912b0c47eb942aae17e509b00e19487
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283020"
---
# <a name="propose-project-resources"></a>Foreslå prosjektressurser

[!include [banner](../includes/psa-now-project-operations.md)]

Ressursledere kan foreslå en ressurs til prosjektlederen ved å bruke en ressursforespørsel.

1. Fra rutenettet med forspørsler eller fra selve forespørselen velger du **Søk etter ressurser**.
2. På siden **Planleggingsassistent** velger du ressursen, og deretter i ruten **Opprett ressursbestilling**, i feltet **Bestillingsstatus**, velger du **Bestill**.

    ![Foreslått ressurs valgt](media/Resource-Management-image62.png)

Følgende statusoppdateringer inntreffer:

- På siden **Planleggingsassistent** oppdateres statusindikatorene for å indikere at bestillingen er foreslått, ikke forpliktende bestilt.

    ![Statusindikatorer for foreslått bestilling på siden Planleggingsassistent](media/Resource-Management-image63.png)

- I ressursforespørselen endres statusen til **Må gjennomgås**.

    ![Status for ressursforespørsel endret til Må gjennomgås](media/Resource-Management-image64.png)

- I kategorien **Team** i prosjektet endres verdien for det generelle teammedlemmets **Forespørselsstatus** til **Må gjennomgås**.

    ![Generelt teammedlems forespørselsstatus endret til Må gjennomgås i kategorien Team.](media/Resource-Management-image48.png)

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

![Visningen Ressursutnyttelse](media/Resource-Management-image65.png)

Hver celle i rutenettet representerer den fakturerbare utnyttelsesprosenten for ressursen i en periode, for eksempel en dag, uke eller måned. Følgende formler brukes til å fargelegge cellene:

- **Grønn:** fakturerbar utnyttelse \>= ressursmålutnyttelse
- **Gul:** målutnyttelse – 20 \<= fakturerbar utnyttelse \< målutnyttelse
- **Rød:** fakturerbar utnyttelse \< målutnyttelse – 20.

Siden visningen **Ressursutnyttelse** er basert på planleggingstavlen, kan du bruke filtreringsfunksjonene på planleggingstavlen til å filtrere resultatene.

Rutenettet krever at du angir en målutnyttelse for rollen eller den individuelle ressursen. Du kan sette opp dette ved å gå til **Ressurser** \> **Ressursroller**.

I tillegg må en standardrolle tilordnes til hver bestillbare ressurs. Gå til **Ressurser** \> **Ressurser**. I kategorien **Project Service** kontrollerer du at det er definert en ressursrolle, og at **Er standard**-feltet er satt til **Ja**. Du kan legge til flere roller der **Er standard = Nei**. Rollen der **Er standard = Ja** brukes til å evaluere ressursens utnyttelse mot målet for den aktuelle rollen.

![Standardrolle angitt](media/Resource-Management-image67.png)

I kategorien **Project Service** kan du også angi en individuell målutnyttelse for ressursen. Beregningen av utnyttelsen bruker deretter denne målutnyttelsen til å evaluere ressursens mål i stedet for målet for standardrollen for ressursen.

Utnyttelse vises bare for en ressurs hvis ressursen har godkjent, belastbar tid i perioden som vises i rutenettet.

## <a name="resource-availability"></a>Ressurstilgjengelighet

Det er svært viktig at ressurslederne kan vise tilgjengeligheten til ressurser og oppdatere bestillinger. I noen tilfeller er det ingen formell etterspørsel (ressursforespørsel), men en ressursleder må reagere på et ikke-planlagt behov som kommer gjennom kanaler, for eksempel en e-postmelding, telefonsamtale eller direkte melding. Ressursledere bruker planleggingstavlen til å oppdatere ressurser og bestillinger.

Arbeidstimer for ressursen brukes som grunnlag for beregning av tilgjengeligheten for en ressurs. Ressursbestillinger opptar kapasiteten til ressursene.

![Planleggingstavle](media/Resource-Management-image68.png)

Planleggingstavlen bruker farger og skyggelegging til å vise bestillinger, tilgjengelighet og overbestillinger, samt statusen til bestillinger. Ved hjelp av en innstilling for planleggingstavlen kan du vise en forklaring.

Hvis en pil mot høyre vises ved siden av en individuell bestillbar ressurs på planleggingstavlen, kan ressursen utvides for å vise detaljer om arbeidet som er bestilt av ressursen.

![Bestillbar ressurs utvidet på planleggingstavlen](media/Resource-Management-image69.png)

Ettersom Dynamics 365 Project Service Automation bruker Universal Resource Scheduling-motoren, hvis du også har Dynamics 365 Field Service installert, kan du vise detaljene for ressursbestillinger for prosjekter, arbeidsordrer og alle andre enheter du har utvidet planlegging til.

![Detaljer for ressursbestillinger for prosjekter og arbeidsordrer](media/Resource-Management-image70.png)

Hvis du vil vise flere detaljer om en individuell ressurs, høyreklikker du den for å åpne ressurskortet.

![Ressurskort](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]