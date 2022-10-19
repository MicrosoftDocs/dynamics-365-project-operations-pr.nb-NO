---
title: Konverteringsprosess for prosjektplanlegging av Project Service Automation til Project Operations
description: Denne artikkelen gir en oversikt over funksjonsendringene for Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642581"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Konverteringsprosess for prosjektplanlegging av Project Service Automation til Project Operations

Etter at et prosjekt er oppgradert fra Microsoft Dynamics 365 Project Service Automation 3.X til Dynamics 365 Project Operations Lite, går det ikke an å redigere prosjektoppgaver i arbeidsnedbrytningsstrukturen (WBS) for oppgaverutenett. Kundene kan gå gjennom WBS-ene i sporingsrutenettet der nye felter er lagt til, for å oppgi alle detaljene som er knyttet til oppgaven. Når det gjelder prosjekter der WBS-en må endres, kan du selektivt konvertere kvalifiserte prosjekter til den nye planleggingsopplevelsen Project for the Web.

## <a name="project-conversion-process"></a>Prosjektkonverteringen

Følg denne fremgangsmåten for å konvertere et prosjekt.

1. Åpne hovedsiden for prosjektet, og velg **Konverter** i handlingsruten.
1. Velg **OK** i bekreftelsesmeldingsboksen for å starte prosjektkonverteringen. Følgende handlinger forekommer:

    1. Følgende står på en meldingslinje som vises på hovedsiden for prosjektet: «Prosjektplanen konverteres. Du kan ikke gjøre endringer i prosjektet før konverteringen er fullført.»
    1. Du blir omdirigert til prosjektlisten.

    Etter at prosjektkonverteringen er fullført, utføres følgende handlinger:

    1. Den tilordnede prosjektlederen mottar et varsel til høyre i programmet.
    1. Meldingslinjen som angir at konverteringen pågår, er fjernet.
    1. Fanen **Tidsplan** viser den nye planleggingsopplevelsen med Project for the Web. Alle brukere som har de riktige lisensene og sikkerhetsrollene, kan redigere WBS-en.
    1. Feltet **Planleggingsmotor** oppdateres til **Project for the Web**.
    1. **Konverter**-knappen fjernes fra handlingsruten.

> [!IMPORTANT]
> Massekonvertering av prosjekter er ikke tillatt. Ethvert forsøk på å oppdatere et stort antall prosjekter samtidig blir begrenset. Denne begrensningen bidrar til å sikre høy ytelse for alle kunder.

## <a name="manual-tasks-vs-automatic-tasks"></a>Manuelle oppgaver kontra automatiske oppgaver

Når et miljø oppgraderes fra Project Service Automation til Project Operations, betraktes alle oppgaver i WBS som automatisk planlagt. Konseptet med manuelt planlagte oppgaver er ikke tilgjengelig i Project for the Web. Du kan imidlertid definere foretrukket planleggingsfunksjonalitet for prosjektene ved å bruke innstillingen for [planleggingsmodus](/project-management/scheduling-modes.md) når du oppretter nye prosjekter.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Begrensede operasjoner for prosjekter før konvertering

Denne delen skisserer funksjonsforskjellene du kan forvente når prosjekter ikke er konvertert.

### <a name="copy-project"></a>Kopier prosjekt

**Kopier**-operasjonen støttes bare for konverterte prosjekter. Oppgraderte prosjekter kan ikke kopieres før konvertering.

### <a name="move-project"></a>Flytt prosjekt

En endring i startdatoen for et prosjekt flytter ikke starten på oppgavene proporsjonalt med mindre prosjektet er konvertert.

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Hva er forskjellene på konverterte prosjekter og nye prosjekter som opprettes etter at oppgraderingen er fullført?

Når det gjelder prosjekter som konverteres etter at miljøet er oppgradert, angis det et flagg som fastsetter at tidsplanen bare skal ta hensyn til prosjektkalenderen. Denne funksjonaliteten samsvarer med funksjonaliteten i Project Service Automation. Flagget angis imidlertid ikke for nye prosjekter som er opprettet etter oppgraderingen. Derfor vil tidsplanen ta hensyn til arbeidstiden for ressurser når de er tilordnet til en oppgave.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Hva skal jeg gjøre hvis prosjektet ikke blir konvertert?

Hvis prosjektet ikke kan konverteres, må du først gå gjennom feilloggene for å identifisere vanlige problemer som er knyttet til WBS-ene. Hvis loggene ikke angir en bestemt feil du kan gjøre noe med, kontakter du kundestøtte, slik at saken kan gjennomgås videre.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Hvordan håndteres stengetider i Project for the Web?

Project for the Web tar ikke hensyn til stengetider som organisasjonen definerer på organisasjonsnivået. Den tar imidlertid hensyn til andre typer fridager som er definert i en gitt arbeidstidsmal.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Hva er begrensningene ved Project for the Web?

Se [Opprett en arbeidsnedbrytningsstruktur: prosjektbegrensninger](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Kan jeg forvente endringer i kostnads- og salgsestimatene?

I sjeldne tilfeller der profiler for ressurstilordning beregnes på nytt, eller der de faller innen en annen datogrense enn kildeprosjektet, kan det hende at du ser forskjeller i salgs- og kostnadsestimat. Som en del av oppgraderingsprosessen forventes kundene å teste et representativt eksempelsett med prosjekter, slik at de kan bli klar over eventuelle potensielle endringer i tidsplanen.
