---
title: Opprett leverandørfakturaer
description: Denne artikkelen beskriver konseptet med leverandørfakturaer og forklarer hvordan du oppretter dem i Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475433"
---
# <a name="create-vendor-invoices"></a>Opprett leverandørfakturaer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Hvis du vil bruke funksjonaliteten som er beskrevet i denne artikkelen, må du aktivere funksjonen **Aktiver behandling av faktiske verdier i underkontrakter med Project Operations for ressursbaserte scenarioer** i arbeidsområdet **Funksjonsbehandling**.

Leverandørfakturering i Microsoft Dynamics 365 Project Operations kan brukes til å registrere kostnader fra leveringer av tjenester og/eller materiell i et prosjekt som fullføres av leverandører.

Når tjenester og/eller materiell er underkontraktert til en leverandør, representerer en underkontrakt den kontraktsmessige avtalen med den leverandøren. Etter hvert som leverandøren leverer tjenestene, eller materiellet mottas og brukes på prosjektoppgaver, registreres kostnader på prosjektet. Leverandøren sender deretter regelmessig fakturaer. Disse fakturaene bekreftes og samsvares med kostnader som er registrert på prosjektet. Når verifiseringsprosessen er fullført, bekreftes og frigis leverandørfakturaen for betaling.

## <a name="scenarios-for-use"></a>Scenarioer for bruk

Leverandørfakturaer i Project Operations kan brukes til å støtte to distinkte scenarioer:

- Kunder bruker hele underkontraktopplevelsen.
- Kunder bruker ikke alle underkontraktopplevelsene, men vil ha en enhetlig visning av kostnader på prosjekter i Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kunder bruker hele underkontraktsopplevelsen

Med leverandørfakturaer kan du kontrollere tidsoppføringer, materialbruk og utgiftsoppføringer som refererer til komponenter som er underordnet, og samsvare dem med leverandørfakturalinjer. Denne prosessen kan brukes til å kontrollere nøyaktigheten for leverandørfakturalinjene. Når verifiseringsprosessen er fullført og leverandørfakturaen er bekreftet, reverserer systemet de faktiske dataene som ble registrert av godkjente logger for tids-, utgifts- og materialbruk, og oppretter deretter nye faktiske kostnader ved hjelp av leverandørfakturalinjene.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kunder bruker ikke alle underkontraktsopplevelsene, men vil ha en enhetlig visning av kostnader på prosjekter i Project Operations

Hvis du sporer underkontraktsprosessen i et tredjepartssystem, kan du registrere kostnader fra det tredjepartssystemet til Project Operations ved å opprette leverandørfakturaer som ikke refererer til underkontrakter. På denne måten kan prosjektlederne ha én enhetlig visning av alle kostnader i et gitt prosjekt.

## <a name="create-vendor-invoices-in-project-operations"></a>Opprett leverandørfakturaer i Project Operations

Leverandørfakturaer opprettes i Dynamics 365 Finance ved hjelp modulen **Leverandørgjeld**. Du kan ikke opprette leverandørfakturaer direkte i Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Konfigurer verifisering av leverandørfakturaer

Hvis leverandørfakturaen er beregnet for en underkontrakt i Dataverse, må du aktivere parameteren **Prosjektleder må verifisere manuelt**. Innstillingen for alternativet fastsetter hvorvidt leverandørfakturaen skal bekreftes automatisk i Dataverse eller krever manuell bekreftelse. Hodet i hver prosjektleverandørfaktura omfatter et alternativ med samme navn. Alternativet i hodet settes som standard til verdien du angir her, i alle prosjektleverandørfakturaer. Du kan imidlertid oppdatere verdien etter behov i hodet i individuelle leverandørfakturaer.

Hvis alternativet settes til **Ja**, har leverandørfakturaen som opprettes i Finance og synkroniseres med Dataverse, statusen **Utkast**. Fakturaen må deretter valideres og verifiseres av prosjektlederen, og bekreftes, før den behandles og posteres i de bestemte prosjekt- og finanskontoene i Finance.

Hvis alternativet er satt til **Nei**, bekreftes leverandørfakturaen automatisk. Ingen flere handlinger kreves.

Følg denne fremgangsmåten for å konfigurere verifisering av leverandørfaktura.

1. Gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Parametere for prosjektstyring og regnskap** i Finance.
1. Sett alternativet **Prosjektleder må verifisere manuelt** til **Ja** i fanen **Finansielle tjenester** hvis en firmapolicy krever at underleverandørfakturaer verifiseres. Hvis prosjektlederen ikke trenger å verifisere i Dataverse, lar du alternativet være satt til **Nei**. Innstillingen brukes som standard på siden **Ventende leverandørfaktura**.

> [!NOTE]
> Leverandørfakturaer som opprettes for underkontrakter i Dataverse, kan bare behandles riktig hvis alternativet **Prosjektleder må verifisere manuelt** er satt til **Ja**. Tid, materiale og faktiske utgiftskostnader som underleverandører oppretter, kan bare samsvares manuelt med leverandørfakturalinjer av prosjektlederen hvis dette alternativet er satt til **Ja**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Konfigurer en integrasjonskonto for innkjøp for leverandørfakturaer

Når en leverandørfaktura posteres i Finance for Project Operations – integrert miljø (ikke lagerført), posteres økonomi på integrasjonskontoen for innkjøp. Systemet genererer de faktiske verdiene i Dataverse for den posterte fakturaen. Disse faktiske verdiene posteres i Finance ved hjelp av integreringsjournalen for prosjekt. Når du posterer integreringsjournalen for prosjekt, posteres de faktiske kostnadene, og integrasjonskontoen for innkjøp tilbakeføres.

Følg disse trinnene for å konfigurere en integrasjonskonto for innkjøp for leverandørfakturaer.

1. Gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Parametere for prosjektstyring og regnskap** i Finance.
1. Velg **Materialer** \> **Integrasjonskonto for innkjøp** i fanen **Project Operations i Dynamics 365 Customer Engagement**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Opprett og poster underleverandørfakturaer

Når en regnskapsassistent mottar en faktura fra underleverandøren, opprettes det en ny faktura i Finance.

1. Gå til **Leverandørgjeld** \> **Fakturaer** \> **Ventende leverandørfakturaer** i Finance.
1. I **handlingsruten** velger du **Ny** for å opprette en leverandørfaktura.
1. Velg **Underleverandør** i **Fakturakonto**-feltet i fakturahodet.
1. Velg fakturadatoen.
1. Angi **Ja** for alternativet **Prosjektleder må verifisere manuelt** i **Hode**-fanen. Standardinnstillingen for dette alternativet kommer fra siden **Parametere for prosjektstyring og regnskap**. Den kan imidlertid endres på leverandørfakturanivået.
1. Velg **Legg til linje** i hurtigfanen **Fakturalinje** for å opprette en leverandørfakturalinje.
1. Velg innkjøpskategorien som ble opprettet for underkontraktlinjer, og angi enhetspris, måleenhet og antall.
1. Velg prosjektet som underleverandøren deler underkontrakten mot, i **Prosjekt**-fanen i delen for leverandørfakturalinjene.
1. Velg prosjektkategorien. Den kan være av typen **Vare**, **Utgift**, **Materialer** eller **Timer**.
1. Velg rollen bare hvis den valgte prosjektkategorien er av typen **Time**.
1. Velg **Poster** for å postere leverandørfakturaen.

Du kan alternativt opprette en leverandørfaktura ved å gå til **Leverandørgjeld** \> **Fakturaer** \> **Åpne leverandørfakturaer** og velge **Ny**.

Når leverandørfakturaen er postert, blir den tilgjengelig i Dataverse for verifisering og behandling av prosjektledere.

## <a name="vendor-invoice-processing-in-dataverse"></a>Leverandørfakturabehandling i Dataverse

I leverandørfakturaen som er opprettet i Dataverse, kommer noen feltverdier fra leverandørfakturaen som er registrert i Finance. Andre verdier er standardverdier som kommer fra underkontrakten.

Følgende felter og relaterte oppføringer kopieres fra underkontrakten til hodet i leverandørfakturaen:

- Valuta
- Kontraktsenhet
- Betalingsbetingelser

På leverandørfakturalinjene bruker Project Operations følgende feltverdier til å angi standard underkontrakt og referanse for underkontraktlinje:

- Transaksjonsklasse
- Rolle
- Transaksjonskategori
- Produktfelter
- Project
- Oppgave

> [!NOTE]
> Underkontraktlinjer av typen Fast pris støttes ikke i Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
