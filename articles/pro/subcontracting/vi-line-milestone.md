---
title: Leverandørfakturalinjer for milepæler
description: Dette emnet forklarer hvordan du oppretter leverandørfakturalinjer for milepæler på en underkontrakt.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590634"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Leverandørfakturalinjer for milepæler

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En leverandørfaktura i Microsoft Dynamics 365 Project Operations kan ha leverandørfakturalinjer for milepæler som er definert på en underkontraktslinje. Prosjektledere kan bruke leverandørfakturalinjer for milepæler til å registrere kostnadene for tjenester som er innkjøpt som milepælbaserte kostnader som påløper for tjenester eller produkter som er anskaffet for prosjektet.

Leverandørfakturalinjer for milepæler må alltid referere til en underkontraktslinje som har en faktureringsmetode med fast pris. Når en leverandørfakturalinje for milepæler refererer til en underleverandørlinje, kan prosjektledere samsvare og kontrollere de underliggende kostnadene for tid, utgifter eller materiell som refererer til denne underkontraktlinjen mot milepælen som faktureres av leverandøren.

Tabellen nedenfor inneholder informasjon om feltene på leverandørfakturalinjer for milepæler.

| Felt | Bekrivelse | Funksjonsinnvirkning |
| --- | --- | --- |
| Name | Navnet på leverandørfakturalinjen, for å hjelpe med identifisering. | Dette navnet vises som den første kolonnen i alle oppslag som er basert på leverandørfakturalinjer. |
| Bekrivelse | En kort beskrivelse av tjenester som faktureres av leverandøren på leverandørfakturalinjen. | None |
| Underkontrakt | Underkontrakten som tjenestene opprinnelig ble bestilt på. | Når en underkontrakt er valgt for leverandørfakturaen, arver alle linjene på leverandørfakturaen dette valget. En leverandørfaktura kan ikke ha leverandørfakturalinjer som refererer til ulike underkontrakter. |
| Underkontraktlinje | Underkontraktlinjen som tjenestene ble bestilt på. Listen over underkontraktslinjer som kan velges, er begrenset til linjene på den valgte underkontrakten. | Når en underkontraktslinje velges på en leverandørfakturalinje for milepæler, er feltene **Rolle** og **Transaksjonskategori**, samt produktrelaterte felter, irrelevante og utilgjengelige. Feltene **Antall**, **Enhet** og **Enhetsgruppe** er heller ikke relevante for milepælbaserte leverandørfakturalinjer. |
| Transaksjonsdato | Datoen da faktiske kostnader for leverandørfakturalinjen registreres på prosjektet. | None |
| Transaksjonsklasse | Velg **Milepæl** for å registrere en leverandørfaktura for en fullført milepæl som ble definert på en underkontraktlinje. | None |
| Milepæl | Velg milepælen som er definert på den relaterte underkontraktslinjen som er merket som **Klar til fakturering**. | Milepæler i underkontraktslinjer som har statusen **Klar til fakturering**, kan velges på en leverandørfakturalinje. |
| Project | Navnet på prosjektet som tjenestene som blir fakturert, ble brukt på. | Dette feltet er obligatorisk og kan ikke være tomt. |
| Oppgave | Navnet på prosjektoppgaven som tjenestene som blir fakturert, ble brukt på. Dette feltet er bare tilgjengelig hvis et prosjekt er valgt. Valg av en prosjektoppgave er valgfritt. | Hvis dette feltet er tomt, kan prosjektlederen samsvare med leverandørfakturalinjen til klassen av transaksjoner på den relaterte underkontraktslinjen som registreres for en hvilken som helst oppgave i prosjektet. Hvis fakturalinjen for leverandørfaktura ikke refererer til en underordnet linje, og dette feltet står tomt, blir ikke den faktiske kostnaden som opprettes av leverandørfakturalinjen, koblet til noen faktiske verdier for ikke-fakturert salg. Hvis oppgavebasert fakturering er konfigurert i dette tilfellet, kan det hende at kostnadene ikke kan faktureres til sluttkunden. |
| Milepælbeløp | Angi verdien for milepælen som er definert på underkontraktslinjen som er klar til fakturering. | None |
| Salgsavgift | Angi mva-beløpet. | None |
| Totalbeløp | Det totale beløpet for leverandørfakturalinjen, inkludert avgifter. Dette feltet beregnes som *Milepælbeløp* + *Merverdiavgift*. | None |

> [!NOTE]
> Når en leverandørfakturalinje som refererer til en underkontraktslinjemilepæl blir opprettet, oppdateres statusen for underkontraktsmilepælen til **Leverandørfaktura opprettet**. Når denne leverandørfakturaen bekreftes, oppdateres deretter statusen for milepælen for underkontraktslinjen til **Leverandørfaktura bekreftet**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
