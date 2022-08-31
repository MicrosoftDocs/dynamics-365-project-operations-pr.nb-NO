---
title: Leverandørfakturering – Konsept og oppretting
description: Denne artikkelen beskriver konseptet med leverandørfakturaer, scenarioer for bruk og hvordan du oppretter leverandørfakturaer i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261956"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Leverandørfakturering – Konsept og oppretting

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Leverandørfakturering i Microsoft Dynamics 365 Project Operations kan brukes til å registrere kostnader fra leveringer av tjenester og/eller materiell i et prosjekt av leverandører.

Når tjenester og/eller materiell er underkontraktert til en leverandør, representerer en underkontrakt den kontraktsmessige avtalen med den leverandøren. Etter hvert som leverandøren leverer tjenestene, eller materiellet mottas og brukes på prosjektoppgaver, registreres kostnader på prosjektet. Leverandøren sender regelmessig fakturaer som bekreftes og samsvares med kostnader som er registrert på prosjektet. Når verifiseringsprosessen er fullført, bekreftes og frigis leverandørfakturaen for betaling.

## <a name="scenarios-for-use"></a>Scenarioer for bruk

Leverandørfakturaer i Project Operations kan brukes til å støtte to distinkte scenarioer.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kunder bruker hele underkontraktsopplevelsen

Ved hjelp av leverandørfakturaer kan du kontrollere og samsvare tidsoppføringer, materialbruk og utgiftsoppføringer som refererer til komponenter som er underordnet, med leverandørfakturalinjer. Denne prosessen kan brukes til å kontrollere nøyaktigheten for leverandørfakturalinjene. Når verifiseringsprosessen er fullført og leverandørfakturaen er bekreftet, reverserer programmet de faktiske dataene som ble registrert av godkjente logger for tids-, utgifts- og materialbruk, og oppretter nye faktiske kostnader ved hjelp av leverandørfakturalinjene.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kunder bruker ikke alle underkontraktsopplevelsene, men vil ha en enhetlig visning av kostnader på prosjekter i Project Operations

Hvis du sporer underkontraktsprosessen i et tredjepartssystem, kan du registrere kostnader fra det tredjepartssystemet til Project Operations ved å opprette leverandørfakturaer som ikke refererer til underkontrakter. På denne måten kan prosjektlederne ha én enhetlig visning av alle kostnader i et gitt prosjekt.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Oppretting av leverandørfakturaer i Project Operations

Leverandørfakturaer kan opprettes på to måter:

- Fra listesiden for leverandørfakturaer eller detaljsiden for én enkelt leverandørfaktura
- Fra listesiden for underkontrakter eller detaljsiden for én enkelt underkontrakt

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Oppretting fra listesiden eller detaljsiden for for leverandørfakturaer

1. Gå til **Innkjøp** \> **Leverandørfakturaer**.
2. På listesiden for leverandørfakturaer eller på detaljsiden for én enkelt leverandørfaktura velger du **Ny** for å opprette en ny leverandørfaktura.

Leverandørfakturaer som opprettes på denne måten, kan også referere til en underkontrakt.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Oppretting fra listesiden eller detaljsiden for for underkontrakter

1. Gå til **Innkjøp** \> **Underkontrakter**.
2. Velg én eller flere underkontrakter.
3. På listesiden for underkontrakter eller på detaljsiden for én enkelt underkontrakt velger du **Opprett leverandørfaktura** for å opprette en ny leverandørfaktura.

Det opprettes en ny leverandørfaktura i **Utkast**-status for hver underkontrakt du har valgt.

Leverandørfakturaer som du oppretter på denne måten, refererer alltid til underkontrakten i leverandørfakturahodet. Hver linje i underkontrakten som har faktureringsmetoden Tid og materiell, fører til at det blir opprettet en linje på leverandørfakturaen. Hver linje i underkontrakten som har faktureringsmetoden Fast pris, fører til at det opprettes en linje på leverandørfakturaen for hver milepæl i underkontraktslinjen som har statusen **Klar for fakturering**.

Følgende felter og relaterte oppføringer kopieres fra underkontrakten til hodet i leverandørfakturaen:

- Leverandør.
- Relaterte prislister kopieres til leverandørfakturaen som prislister.
- Valuta.
- Kontraktsenhet.
- Betalingsbetingelser.

For underkontraktlinjer av typen Tid og materiale kopieres følgende felter og relaterte oppføringer fra underkontraktlinjen til leverandørfakturalinjen:

- Underkontrakt og referanser til linjer i underkontrakt
- Transaksjonsklasse
- Rolle
- Transaksjonskategori
- Produktfelter
- Project
- Oppgave
- Ressurs som kan reserveres

For underkontraktlinjer av typen Fast pris og materiale kopieres følgende felter fra underkontraktlinjen og milepælen på underkontraktlinjen til leverandørfakturalinjen:

- Underkontrakt og referanser til linjer i underkontrakt.
- Transaksjonsklasse. Som standard blir verdien **Milepæl**.
- Navn på og beløp for milepæl kopieres fra den relaterte milepælen for underkontraktslinjen.
- Brukeren kan velge et prosjekt og en oppgave på leverandørfakturalinjen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
