---
title: Registrer en kvittering ved hjelp av OCR
description: Dette emnet gir informasjon om optisk tegngjenkjenning (OCR) for kvitteringer.
author: suvaidya
ms.date: 11/10/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d4c2cce88514e7822515fc407fc7cf31cb34924
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596292"
---
# <a name="capture-a-receipt-using-ocr"></a>Registrer en kvittering ved hjelp av OCR

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Utgiftsregistrering er forbedret gjennom innføringen av optisk tegngjenkjenning (OCR) for kvitteringer. Denne funksjonaliteten er utformet for å forbedre brukeropplevelsen ved opprettelse av reiseregninger.

## <a name="key-features"></a>Nøkkelfunksjoner

- Systemet trekker ut forhandlernavn, dato og totalt beløp fra mottak.
- Systemet prøver å samsvare ikke-tilknyttede mottak med ikke-tilknyttede utgiftstransaksjoner.
- Du kan opprette manuelt angitte utgiftstransaksjoner fra mottak.

## <a name="attach-receipts-to-an-expense-report"></a>Legge ved kvitteringer i en reiseregning

Hvis du automatisk vil legge ved kvitteringer som inkluderer kredittkorttransaksjoner når en reiseregning opprettes, kan du følge fremgangsmåten nedenfor.

  1. Åpne arbeidsområdet **Reiseregning og utlegg**.
  2. I kategorien **Kvitteringer** kontrollerer du at det finnes ikke-tilknyttede kvitteringer. Du kan også laste opp kvitteringer i kategorien **Kvitteringer**.
  3. I kategorien **Utgifter** kontrollerer du at det finnes ikke-tilknyttede utgifter. Vanligvis importerer utgiftsadministrator disse utgiftene fra kredittkortleverandøren.
  4. Velg **Ny reiseregning**. Legg merke til at du kan ta med utgifter og nå også kvitteringer når du oppretter en reiseregning. Hvis du legger til både utgifter og kvitteringer, utløses automatisk avstemming av kvitteringene mot utgiftene.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Opprette eller samsvare kvitteringer mot en reiseregning
Fullfør fremgangsmåten nedenfor for å opprette en utgift eller samsvare en utgift fra en kvittering.

  1. Legg ved en kvittering i en reiseregning ved å velge kategorien **Kvitteringer** og deretter **Legg til kvitteringer**.
  2. Under det opplastede bildet av kvitteringen legger du merke til alternativene **Opprett** og **Samsvar**.

      - Velg **Opprett** for å opprette en manuelt angitt utgiftstransaksjon, og fyll ut verdiene som trekkes ut fra kvitteringen.
      - Hvis du velger **Samsvar**, prøver systemet å samsvare en eksisterende utgift med kvitteringen.

## <a name="installation"></a>Installasjon

For å kunne bruke disse avanserte utgiftsfunksjonene må du installere Expense Management Service-tillegget for Microsoft Dynamics 365 Finance og aktivere funksjonene i forekomsten. Du kan få tilgang til tillegget fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS).

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

- Det eksisterende arbeidsområdet for **Reiseregning og utlegg** erstattes av det nye arbeidsområdet.
- Det legges til et nytt menyelement for synlighet for utgiftsfelt.
- Du kan fremdeles åpne siden for de tidligere **reiseregningene** ved å gå til **Reiseregning og utlegg > Mine utgifter > Reiseregninger**.
- Arbeidsflyter og godkjenninger fører deg fremdelses til den eksisterende reiseregningssiden.
- Kvitteringer blir behandlet gjennom Microsoft Azure Cognitive Services, og metadata blir trukket ut og lagt til.
- Det legges til et alternativ som du kan bruke til å opprette en reiseregning som inkluderer samsvarte, ikke-tilknyttede kvitteringer.
- Ved hjelp av et alternativ som legges til i reiseregninger, kan du opprette en utgiftslinje fra en kvittering, eller forsøk på å samsvare en eksisterende kvittering med en eksisterende utgiftslinje.

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

**Bruker Microsoft dataene mine for modellene sine?**

Nei, Microsoft har bygget en generell maskinlæringsmodell for tjenesten for mottaksbehandling. Denne modellen er ikke basert på mottakene du laster opp.

**Hvor er denne funksjonen tilgjengelig og behandlet?**

Tabellen nedenfor viser de ulike områdene der denne funksjonen er tilgjengelig. Hvis det ikke er støtte for området ditt for øyeblikket, sender du en forespørsel om at tilgjengeligheten av OCR-tjenesten prioriteres i området ditt. 

| Område | Støttes                         |
|--------|-----------------------------------|
| USA    | Ja                               |
| CAN    | Ja                               |
| Storbritannia     | Ja                               |
| AUS    | Ja                               |
| EU     | Delvis. Bare engelske kvitteringer. |
| Asia   | No                                |
| Japan  | No                                |
| Afrika | No                                |

**Hvor havner kvitteringene mine?**

Økonomiavdelingen Cognitive Services for å trekke ut feltdataene. Cognitive Services beholder en kopi av kvitteringen i opptil 24 timer, mens behandlingen utføres. Når behandlingen er fullført, fjerner Cognitive Services kvitteringen. Kvitteringer lagres fremdeles i økonomi.

Hvis du vil ha mer informasjon, kan du se [Aktivere kvitteringsforståelse med den nye funksjonen i Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
