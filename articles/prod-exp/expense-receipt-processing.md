---
title: Behandling av utgiftskvittering
description: Dette emnet gir informasjon om optisk tegngjenkjenning (OCR) for kvitteringer. Denne funksjonen er utformet for å forbedre brukeropplevelsen når reiseregninger opprettes i Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271815"
---
# <a name="expense-receipt-processing"></a>Behandling av utgiftskvittering

Utgiftsregistrering er forbedret gjennom innføringen av optisk tegngjenkjenning (OCR) for kvitteringer. Denne funksjonen er utformet for å forbedre brukeropplevelsen når reiseregninger opprettes.

## <a name="key-features"></a>Nøkkelfunksjoner

- Forhandlernavn, dato og totalt beløp hentes ut fra kvitteringer.
- Funksjonen prøver å samsvare ikke-tilknyttede mottak med ikke-tilknyttede utgiftstransaksjoner.
- Brukerne kan opprette manuelt angitte utgiftstransaksjoner fra kvitteringer.

## <a name="usage-examples"></a>Eksempler på bruk

Hvis du automatisk vil legge ved kvitteringer som inkluderer kredittkorttransaksjoner når en reiseregning opprettes, kan du gjøre følgende:

  1. Åpne arbeidsområdet **Utgiftshåndtering**.
  2. I kategorien **Kvitteringer** kontrollerer du at det finnes ikke-tilknyttede kvitteringer. Du kan også laste opp kvitteringer i kategorien **Kvitteringer**.
  3. I kategorien **Utgifter** kontrollerer du at det finnes ikke-tilknyttede utgifter. Vanligvis importerer utgiftsadministrator disse utgiftene fra kredittkortleverandøren.
  4. Velg **Ny reiseregning**. Legg merke til at du kan ta med utgifter og nå også kvitteringer når du oppretter en reiseregning. Hvis du legger til både utgifter og kvitteringer, utløses automatisk avstemming av kvitteringene mot utgiftene.

Gjør følgende for å opprette en utgift eller samsvare en utgift fra en kvittering:

  1. Legg ved en kvittering i en reiseregning ved å velge kategorien **Kvitteringer** og deretter **Legg til kvitteringer**.
  2. Under det opplastede bildet av kvitteringen legger du merke til alternativene **Opprett** og **Samsvar**.

      - Velg **Opprett** for å opprette en manuelt angitt utgiftstransaksjon, og fyll ut verdiene som trekkes ut fra kvitteringen.
      - Hvis du velger **Samsvar**, prøver systemet å samsvare en eksisterende utgift med kvitteringen.

## <a name="installation"></a>Installasjon

Denne funksjonen fungerer sammen med funksjonen **Nyskapte utgiftsrapporter**, noe som forenkler utgiftsopplevelsen. Denne funksjonen er bare tilgjengelig for nivå 2+-miljøer, som er sandkasse og produksjon.

Hvis du vil bruke disse avanserte utgiftsfunksjonene, installerer du tilleggsprogrammet for reiseregning og utlegg for Microsoft Dynamics 365 Finance, og deretter aktiverer du funksjonene i forekomsten. Du kan få tilgang til tillegget fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS).

1. Logg på LCS, og åpne ønsket miljø.
2. Gå til **Detaljert informasjon**.
3. Velg **Vedlikehold**, eller rull ned til hurtigfanen **Tilleggsprogrammer for miljø**.
4. Velg **Installer et nytt tillegg**.
5. Velg **Expense Management Service**.
6. Følg installasjonsveiledningen, og godta vilkårene.
7. Velg **Installer**.

Aktiver følgende funksjoner i arbeidsområdet **Funksjonsbehandling**:

- Nyskapte utgiftsrapporter
- Automatisk samsvar og opprette utgift fra kvittering

Når du aktiverer disse funksjonene, oppstår følgende handlinger:

- Det eksisterende arbeidsområdet for **utgiftshåndtering** erstattes av det nye arbeidsområdet.
- Det legges til et nytt menyelement for synlighet for utgiftsfelt.
- Du kan fremdeles åpne siden for de tidligere **reiseregningene** ved å gå til **Utgiftshåndtering > Mine utgifter > Reiseregninger**.
- Arbeidsflyter og godkjenninger fører deg fremdelses til den eksisterende reiseregningssiden.
- Kvitteringer blir behandlet gjennom Microsoft Azure Cognitive Services, og metadata blir trukket ut og lagt til.
- Det legges til et alternativ som du kan bruke til å opprette en reiseregning som inkluderer samsvarte, ikke-tilknyttede kvitteringer.
- Ved hjelp av et alternativ som legges til i reiseregninger, kan du opprette en utgiftslinje fra en kvittering, eller forsøk på å samsvare en eksisterende kvittering med en eksisterende utgiftslinje.

Hvis du vil ha mer informasjon om funksjonen Nyskapte utgiftsrapporter, kan du se [Nyskapte utgiftsrapporter](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

**Bruker Microsoft dataene mine for modellene sine?**

Nei, Microsoft har bygget en generell maskinlæringsmodell for tjenesten for mottaksbehandling. Denne modellen er ikke basert på mottakene du laster opp.

**Hvor er denne funksjonen tilgjengelig og behandlet?**

USA støttes for øyeblikket.

**Hvor havner kvitteringene mine?**

Økonomiavdelingen Cognitive Services for å trekke ut feltdataene. Cognitive Services beholder en kopi av kvitteringen i opptil 24 timer, mens behandlingen utføres. Når behandlingen er fullført, fjerner Cognitive Services kvitteringen. Kvitteringer lagres fremdeles i økonomi.

Hvis du vil ha mer informasjon, kan du se [Aktivere kvitteringsforståelse med den nye funksjonen i Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]