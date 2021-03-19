---
title: Konfigurere utgiftshåndtering
description: Denne artikkelen beskriver vurderinger og avgjørelser du må gjøre under planleggingsprosessen, før du konfigurerer utgiftshåndtering i Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271365"
---
# <a name="configure-expense-management"></a>Konfigurere utgiftshåndtering

Dette emnet beskriver vurderinger og avgjørelser du må gjøre under planleggingsprosessen, før du konfigurerer Utgiftshåndtering. I Utgiftshåndtering kan du lagre informasjon om betalingsmetoder, reiserekvisisjoner, reiseregninger, policyer og så videre.

Ettersom mange av beslutningene du tar når du planlegger konfigurasjonen for Utgiftshåndtering, er basert på organisasjonens hierarki og finansielle struktur, må du referere til planleggingsdokumentene for disse områdene.

## <a name="intercompany-expenses"></a>Konserninterne utgifter

Når du aktiverer konserninterne utgifter, tillater du at juridiske enheter og ansatte påløper utgifter på vegne av en annen juridisk enhet, og krever inn betaling fra den juridiske enheten for ansettelse innenfor organisasjonen. En ansatt i juridisk enhet A fullfører for eksempel et prosjekt for juridisk enhet B, og prosjektet påløper reiserelaterte utgifter. Hvis konserninterne utgifter er aktivert, kan den ansatte deretter sende en reiseregning som vil postere utgiften til juridisk enhet B, og utgiften må deretter betales av juridisk enhet A. Hvis organisasjonen ikke har flere juridiske enheter, trenger du ikke å aktivere konserninterne utgifter.

**Beslutning:** Vil du aktivere konserninterne utgifter?

## <a name="financial-management"></a>Finansadministrasjon

Utgiftshåndtering er tett integrert med den økonomiske administreringen av organisasjonen. Mye av konfigurasjonene for Utgiftshåndtering er basert på beslutningene du har tatt om organisasjonens økonomi. Avsnittene nedenfor beskriver de forskjellige områdene som krever planlegging og beslutninger, basert på organisasjonens finansielle avgjørelser og veiledninger fra lederteamet.

### <a name="per-diems"></a>Kostgodtgjørelser

Du må definere den ansattes kostgodtgjørelse som organisasjonen tilbyr. Fordi kostgodtgjørelse vanligvis brukes til å dekke utgifter som måltider, overnatting og andre tilfeldige utgifter, kan du lage regler for kostgodtgjørelsene som organisasjonen tilbyr. Kostgodtgjørelsessatser kan baseres på tiden på året, reisestedet eller begge deler. Når du definerer en kostgodtgjørelsesregel, kan du angi at en prosentsats av kostgodtgjørelsessatsen skal tilbakeholdes hvis en arbeider mottar gratis måltider eller tjenester. Du kan også definere kostgodtgjørelsessatser for å angi et minimum og maksimum antall timer som kostgodtgjørelsessatsen kan gjelde for en arbeiders reise.

**Beslutninger:**

- Standard kostgodtgjørelsesregler for første og siste dag:

    - Hva er minste antall timer en ansatt kan kreve for en dag og likevel motta kostgodtgjørelse?
    - Blir det en reduksjon av beløpet som tilbys for måltider første dag og siste dag? Hva det er en reduksjon, hva er prosentandelen av reduksjonen?
    - Blir det en reduksjon av beløpet som tilbys for et hotell første dag og siste dag? Hva det er en reduksjon, hva er prosentandelen av reduksjonen?
    - Blir det en reduksjon av beløpet som tilbys for andre utgifter som påløpte første dag og siste dag? Hva det er en reduksjon, hva er prosentandelen av reduksjonen?

- Standardregler for kostgodtgjørelse:

    - Er det en prosentvis reduksjon i kostgodtgjørelsen for hvert måltid, hvis måltidet for eksempel er gratis? Hva det er en reduksjon, hva er reduksjonsprosenten for hvert måltid?
    - Beregnes måltidsreduksjonen per dag, per tur eller per antall måltider per dag?
    - Skal kostgodtgjørelsesbeløpene avrundes på vanlig måte eller rundes opp?
    - Er kostgodtgjørelsen beregnet i en 24-timers periode eller på en kalenderdag?

- Kostgodtgjørelsesregler som er basert på sted:

    - Varierer kostgodtgjørelsessatser etter sted? Hvilke steder er inkludert?
    - Hvis kostgodtgjørelsessatsene varierer i henhold til sted, hvilket prosentbeløp tilbys for følgende typer utgifter for hvert sted:

        - Måltider
        - Hotell
        - Andre utgifter

### <a name="expense-management-journals-and-accounts"></a>Journaler og kontoer i Utgiftshåndtering

Utgiftshåndtering krever at du bruker flere journaler og kontoer. Du må for eksempel avgjøre om den samme kontoen skal brukes til tvister om kontantforskudd og kredittkort.

**Beslutninger:**

- Hvilken hovedbokjournal bokføres godkjente reiseregninger i?
- Hvilken konto brukes til forskudd?
- Skal forskudd bli postert umiddelbart?

### <a name="payment-methods"></a>Betalingsmetoder

Når du tillater at de ansatte kan påløpe utgifte på vegne av virksomheten, må du definere betalingsmetodene som de ansatte kan bruke. Du kan for eksempel la de ansatte bruke kontanter eller et firmakredittkort. Du kan også la de ansatte bruke personlige kredittkort og deretter refundere dem. Du må ta følgende avgjørelser for hver betalingsmetode du tillater.

**Beslutninger:**

- Hvilke betalingsmetoder er tillatt?
- Hvem eier utgiftene for betalingsmetoden?
- Er det en motkontotype? Hvis det er en motkontotype, hva er den?
- Hvis det er en motkonto, hva er kontoen?
- Hvis betalingsmetoden er et kredittkort, skal betalingsmetoden bare brukes med importerte transaksjoner?

### <a name="expense-categories-and-shared-categories"></a>Utgiftskategorier og delte kategorier

Når ansatte oppretter reiseregninger, må hver utgift som de registrerer, tilknyttes en utgiftskategori. Utgiftskategorier er avledet fra delte kategorier som kan deles på tvers av de juridiske enhetene i organisasjonen. Disse kategoriene kan også deles i prosjektstyring og -regnskap, avhengig av hvilken måte organisasjonen er definert på. Basert på definisjonen av organisasjonen og veiledning fra implementeringsteamet må du bestemme om kategoriene som brukes i utgiftshåndtering, bare skal brukes i utgiftshåndtering, eller om de skal deles mellom prosjektstyring og -regnskap og utgiftshåndtering. Legg merke til at disse kategoriene kan deles mellom prosjekt og utgift eller prosjekt og produksjon, men ikke mellom utgift og produksjon. Du må ta følgende avgjørelser for hver utgiftskategori.

**Beslutninger:**

- Hva er utgiftskategorien? Eksempler inkluderer kategorier for flyreiser, hotell eller kjørelengde.
- Kan utgiftskategorien også brukes til prosjektstyring og regnskap?
- Hva er utgiftstypen?
- Hva er standard betalingsmetode for utgiftskategorien?
- Må utgifter i utgiftskategorien være spesifiserte?
- Hva er standard hovedkonto for utgiftskategorien?
- Hva er standard mva-gruppe for varesalg for utgiftskategorien?
- Er det tillatt med flere betalingsmetoder for utgiftskategorien? Hvis flere betalingsmetoder er tillatt, hvilke i så fall?
- Finnes det underkategorier i utgiftskategorien? Hvis det finnes underkategorier, må du også ta følgende beslutninger:

    - Er noen av underkategoriene utelukket fra avgiftsfradrag?
    - Hva er mva-gruppen for varesalg for underkategoriene?

Hvis utgiftskategorien også brukes i Prosjektstyring og regnskap, må du svare på de gjenstående spørsmålene. Hvis ikke, gå videre til neste del.

- Hvilke kostnadskontoer skal brukes til følgende utgifter?

    - Kostnad
    - Lønnstildeling
    - VIA – kostverdi
    - Kostnadselement
    - VIA-kostnadsverdielement
    - Påløpt tap
    - VIA – påløpt tap

- Hvilke inntektskontoer skal brukes til følgende?

    - Fakturert omsetning
    - Påløpt omsetning – Salgsverdi
    - VIA – Salgsverdi
    - Påløpt omsetning – produksjon
    - VIA – produksjon
    - Påløpt omsetning – fortjeneste
    - VIA – fortjeneste
    - Påløpt omsetning – abonnement
    - VIA – abonnement

### <a name="taxes"></a>Avgifter

Når det gjelder utgiftsrelaterte avgifter, må du bestemme hva som er inkludert i eller aktivert i reiseregninger.

**Beslutninger:**

- Er merverdiavgift inkludert i utgiftsbeløpene?
- Skal avgiftsfradrag aktiveres for utgifter?

    > [!NOTE]
    > Hvis du bestemte deg for å bruke amerikanske regler for mva og skatt da du planla hovedboken, kan du ikke aktivere avgiftsfradrag for utgifter. (Hvis du vil bruke amerikanske regler for merverdiavgift og skatt, setter du alternativet **Bruk skatteregler for mva** til **Ja**.)

## <a name="policies"></a>Policyer

Ved å opprette reise regningspolicyer kan du bidra til at organisasjonen sparer tid og penger når de ansatte påløper utgifter på vegne av organisasjonen. Policyer hjelper deg med å sørge for at de ansatte holde seg til budsjettet, oppgir all nødvendig informasjon og bruker penger bare når det er nødvendig. Du må ta følgende avgjørelser for hver reiseregningspolicy og hver godkjenningspolicy for reiseregninger som du oppretter.

**Beslutninger:**

- Hva er navnet på policyen?
- Hva er utgiftspolicyen for?
- Hvis du tidligere har bestemt deg for å aktivere konserninterne utgifter, hvilke selskaper i organisasjonen vil denne policyen gjelde for?
- Når blir policyen effektiv?
- Når utløper policyen?
- Hva er policyregelen?
- Hva er resultatet av policyregelen?


[!INCLUDE[footer-include](../includes/footer-banner.md)]