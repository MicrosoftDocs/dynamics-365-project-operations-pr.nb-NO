---
title: Prosjektkontrakter
description: Dette emnet inneholder eksempler på prosjektkontraktene som du kan opprette for ulike typer prosjekter og finansieringskilder, og hvordan du kan administrere kontrakter og fakturere prosjektkunder.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754146"
---
# <a name="project-contracts"></a>Prosjektkontrakter

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder eksempler på prosjektkontraktene som du kan opprette for ulike typer prosjekter og finansieringskilder, og hvordan du kan administrere kontrakter og fakturere prosjektkunder.

Prosjekttypen som du oppretter for en prosjektkontrakt, bestemmer metoden som brukes til å fakturere prosjektkunder. Du kan endre en prosjektkontrakt og det relaterte prosjektet, men du kan ikke endre prosjekttypen. 

Ved hjelp av en prosjektkontrakt kan du fakturere ett eller flere prosjekter samtidig. Prosjektkontrakten bidrar også til å garantere en konsekvent faktureringsprosedyre for hvert delprosjekt i en prosjektstruktur. 

Hvert prosjekt som blir fakturert, må tilknyttes en prosjektkontrakt. Innstillingene for en prosjektkontrakt gjelder for alle prosjekter og delprosjekter som er tilknyttet prosjektkontrakten. 

En prosjektkontrakt kan angi én eller flere finansieringskilder. Derfor kan du dele opp faktureringen mellom flere fond, konfigurere finansieringsgrenser, slik at finansieringskilder ikke blir fakturert mer enn et bestemt beløp og konfigurere finansieringsregler for belastning av utgifter.

## <a name="funding-for-project-contracts"></a>Finansiering for prosjektkontrakter
Noen prosjektkontrakter spesifiserer at flere parter deler ansvaret for finansiering av prosjektkostnadene. Her er noen eksempler:

-   En stor kunde som har flere divisjoner ber om at finansiering av et prosjekt deles etter divisjon.
-   Firmaet deler kostnadene for et stort prosjekt med en ekstern organisasjon.
-   Et veiprosjekt er medfinansiert av to kommuner.
-   Et broprosjekt er finansiert av en offentlig bevilgning og en privat bedrift.

I Dynamics 365 Finance kan du dele opp faktureringen for en enkelt transaksjon eller et helt prosjekt mellom flere kunder, tilskudd eller organisasjoner. 

I prosjekter som har flere innsamlingsverktøy, kalles alle parter som bidrar til finansieringen for et avansert finansieringsprosjekt, finansieringskilder. Når en kunde, organisasjon eller et tilskudd er definert som en finansieringskilde, kan den/det tilordnes til én eller flere finansieringsregler. Finansieringsregler inneholder kriteriene som avgjør hvordan gebyrer tildeles de ulike finansieringskildene for et prosjekt. 

Fordi lagerførte varer, for eksempel de som vises på innkjøpsrekvisisjoner og bestillinger, ikke kan deles, kan ikke kostnads beløpet deles mellom flere finansieringskilder på distribusjonstidspunktet. Derfor forblir finansieringskildeverdien 0 (null) helt til lageravgangen blir postert. Når lageravgangen blir postert, blir kostnadsbeløpet fordelt i henhold til reglene for forretningsforbindelsesdistribusjonen for prosjektet.

Her er noen trinn du kan utføre for å gjøre det enklere å dele opp faktureringen blant flere finansieringskilder:

-   Angi at alle transaksjoner som er angitt for et prosjekt, bruker samme salgsvaluta som prosjektkontrakten.
-   Angi finansieringsgrenser, slik at en finansieringskilde ikke blir fakturert mer enn et bestemt beløp mot et prosjekt.
-   Konfigurere finansieringsregler og finansieringsgrenser for hver arbeider, vare, kategori, kategorigruppe og transaksjonstype (eller for alle transaksjonstyper).
-   Velg valgfrie start- og sluttdatoer for å definere perioden hver finansieringsregel er gyldig.
-   Angi prosentandelen som hver finansieringskilde er ansvarlig for.
-   Angi hvilken finansieringskilde som er ansvarlig for avrundingsdifferanser som er forårsaket av beregning av finansieringstilordninger.
-   Definer regler som avgjør hvordan prosjektkostnader faktureres til eksterne kunder og belastes interne organisasjoner.
-   Registrer transaksjoner i en på vent-finansieringskonto til flere finansieringer kan innhentes, eller til du bestemmer deg for å bære kostnadene internt.

Hvis du vil avgjøre hvilken avgiftsgruppe som skal knyttes til en transaksjon, søker du etter en avgiftsgruppetilordning. Hvis det ikke er utført en avgiftsgruppetilordning på prosjektnivået, søkes det i prosjektkontrakten.

### <a name="example-multiple-funding-sources-simple"></a>Eksempel: Flere finansieringskilder (enkel)

Tabellen nedenfor inneholder scenarier for administrasjon av finansieringsfordeling mellom flere finansieringskilder. Disse scenariene er basert på følgende antakelser:

-   Prioritetsinnstillinger er beregnet på kapitalfordelingen før det tas hensyn til andre finansieringsregelvilkår.
-   Det er ikke angitt et datointervall for å definere perioden d når finansieringsregelen er gyldig.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenario</strong></td>
<td><strong>Finansieringskilde</strong></td>
<td><strong>Fordelingsprosent</strong></td>
<td><strong>Tildelingsprioritet</strong></td>
</tr>
<tr class="even">
<td>Du vil fordele kostnader til én finansieringskilde til midlene er oppbrukt, tildele kostnader til en annen finansieringskilde til midlene er oppbrukt, og til slutt tilordne de gjenstående kostnadene til en tredje finansieringskilde.</td>
<td><ul>
<li>Finansieringskilde　1</li>
<li>Finansieringskilde　2</li>
<li>Finansieringskilde　3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Du vil fordele 75 prosent av kostnader til én finansieringskilde og 25 prosent til en annen finansieringskilde. Når en av disse finansieringskildene er oppbrukt, vil du betale de gjenstående kostnadene fra en tredje finansieringskilde.</td>
<td><ul>
<li>Finansieringskilde　1</li>
<li>Finansieringskilde　2</li>
<li>Finansieringskilde　3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Du vil fordele 75 prosent av kostnader til én finansieringskilde og 25 prosent til en annen finansieringskilde. Når en av disse finansieringskildene er oppbrukt, vil du dele de gjenstående kostnadene mellom en tredje finansieringskilde og en fjerde finansieringskilde.</td>
<td><ul>
<li>Finansieringskilde　1</li>
<li>Finansieringskilde　2</li>
<li>Finansieringskilde　3</li>
<li>Finansieringskilde　4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Du vil fordele de første 25 prosentene av kostnader til én finansieringskilde og resten til en annen finansieringskilde.</td>
<td><ul>
<li>Finansieringskilde　1</li>
<li>Finansieringskilde　2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Eksempel: Flere finansieringskilder (komplisert)

Du har tre finansieringskilder som du vil bruke i følgende rekkefølge:

1.  Bruk finansieringskilde 2 og finansieringskilde 3 likt til finansieringskilde 2 er oppbrukt.
2.  Fortsett å bruke finansieringskilde 3 til den er oppbrukt.
3.  Bruk finansieringskilde 1 etter at finansieringskilde 3 er oppbrukt.

Hvis du vil nå dette målet, må du først gjøre følgende:

-   Definer finansieringsgrenser for finansieringskilde 2 og finansieringskilde 3 for de respektive beløpene.
-   Opprett følgende finansieringsregler:
    -   Regel 1 (prioritet 1): Tildel 50 prosent av transaksjoner til finansieringskilde 2 og 50 prosent til finansieringskilde 3.
    -   Regel 2 (prioritet 2): Tildel 100 prosent av transaksjoner til finansieringskilde 3.
    -   Regel 3 (prioritet 3): Tildel 100 prosent av transaksjoner til finansieringskilde 1.

Denne installasjonen fungerer fordi transaksjoner kontrolleres mot regler og grenser for å avgjøre om noen av dem gjelder for transaksjonen. Hvis ingen spesifikke regler eller begrensninger gjelder for transaksjonen, gjelder Alle transaksjoner-regelen. Regelen Alle transaksjoner samsvarer med alle transaksjoner. 

Hvis det blir funnet en regel som samsvarer med en transaksjon, brukes prosentandelen som er tilordnet i den regelen, først, men bare etter at samsvarene er kontrollert mot eventuelle begrensninger som er satt opp. Hvis en grense er nådd og midlene til en finansieringskilde er oppbrukt, blir finansieringsregelen som er knyttet til finansieringsgrensen, ignorert, og programmet kontrollerer den neste regelen som gjelder. 

I noen tilfeller kan bare deler av en transaksjon tildeles under en regel. Dette kan skje fordi en grense er nådd når transaksjonen fordeles. I dette tilfellet fordeles bare et bestemt beløp i henhold til den regelen, for eksempel 50 prosent for hver finansieringskilde. Dette er tilfellet i regel 1, som er beskrevet tidligere i denne delen. Resten fordeles i henhold til neste regel i sekvensen. 

Følgende tabell undersøker dette scenarioet mer detaljert.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokus</strong></td>
<td><strong>Detaljer</strong></td>
</tr>
<tr class="even">
<td>Finansieringsregler</td>
<td><ul>
<li>Regel 1 (prioritet 1): Alle transaksjoner. Tildel finansieringskilde 2 på 50 % og finansieringskilde 3 på 50 %.</li>
<li>Regel 2 (prioritet 2): Alle transaksjoner. Tilordne finansieringskilde 3 på 100 %.</li>
<li>Regel 3 (prioritet 2): Alle transaksjoner. Tilordne finansieringskilde 1 på 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finansieringsgrenser</td>
<td><ul>
<li>Grense for finansieringskilde 1 = 10 000.00</li>
<li>Grense for finansieringskilde 2 = 500.00</li>
<li>Grense for finansieringskilde 3 = 750.00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transaksjon 1</td>
<td><strong>Transaksjonsbeløp:</strong> 100,00<strong>Finansiering:</strong> Transaksjonen betales bare i henhold til regel 1, fordi transaksjonen er fullt betalt etter at regel 1 er brukt. Transaksjonen er finansiert likt mellom finansieringskilde 2 og finansieringskilde 3.
<ul>
<li>Finansieringskilde 2: 50.00</li>
<li>Finansieringskilde 3: 50.00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transaksjon 2</td>
<td><strong>Transaksjonsbeløp:</strong> 5 000,00<strong>Finansiering:</strong> Transaksjonen betales i henhold til alle tre regler. <strong>Regel 1</strong>
<ul>
<li>Finansieringskilde 2: 450.00</li>
<li>Finansieringskilde 3: 450.00</li>
</ul>
<strong>Regel 2</strong>
<ul>
<li>Finansieringskilde 3: 250.00 (= 750.00 – 50.00 – 450.00)</li>
</ul>
<strong>Regel 3</strong>
<ul>
<li>Finansieringskilde 1: 3850.00 (= 5000.00 – 450.00 – 450.00 – 250.00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Totalt antall midler som er fordelt for hver finansieringskilde</td>
<td><ul>
<li>Finansieringskilde 1: 3850.00</li>
<li>Finansieringskilde 2: 500.00</li>
<li>Finansieringskilde 3: 750.00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Faktureringsregler
Når du forhandler en prosjektkontrakt med en kunde, definerer du hvordan og når du kan fakturere kunden for arbeid på et prosjekt. Etter at du har satt opp prosjektkontrakten og prosjektet, kan du definere faktureringsregler for prosjektet. Faktureringsregler er basert på prosjektvilkår som er angitt i prosjektkontrakten. Faktureringsreglene du kan opprette, avhenger av betingelsene i prosjektkontrakten og prosjekttypen, for eksempel Tid og materiale eller Fast pris, som du knytter til faktureringsregelen. Du kan opprette mer enn én faktureringsregel for en prosjektkontrakt. Du kan også tilordne en faktureringsregel til flere prosjekter som er knyttet til den samme prosjektkontrakten, og som har lignende faktureringsvilkår. 

Du kan definere følgende typer faktureringsregler:

-   **Leveringsenhet** – Fakturere en kunde når du fullfører en leveringsenhet. Du definerer leveringsenhetene i kontrakten.
-   **Fremdrift** – Fakturere en kunde når du fullfører en bestemt prosentdel av prosjektet. Du kan angi en faktureringsregel for automatisk å beregne prosentandelen av fullført arbeid, eller du kan manuelt beregne prosentandelen av fullført arbeid og beløpet for å fakturere kunden.
-   **Milepæl** – Fakturerer en kunde for hele beløpet for en prosjektmilepæl når milepælen er nådd.
-   **Gebyr** – Fakturer en kunde for tjenestene pluss et administrasjonsgebyr, som vanligvis er en prosentdel av prisen på tjenestene.
-   **Tid og materialer** – Fakturerer en kunde for verdien av tid og materialer som brukes på et prosjekt.

For alle typer faktureringsregler kan du angi en tilbakeholdelsesprosent som trekkes fra kundefakturaer til et prosjekt når en avtalt fase. Tilbakeholdelsesprosenten for betalingen er angitt i prosjektkontrakten. Beløpet beregnes basert på, og trekkes fra, totalverdien for linjene i en kundefaktura. 

For faktureringsreglene **Tid og materiale** og **Fremdrift** kan du tilordne belastbare kategorier. Belastbare kategorier angir transaksjonene som skal tas med i kundefakturaer. 

Når du er klar til å fakturere kunden, beregnes beløpet som skal faktureres for prosjektet, basert på faktureringsreglene, og et prosjektfakturaforslag genereres. 

Avsnittene nedenfor inneholder eksempler som viser hvordan du konfigurerer og behandler faktureringsregler for et prosjekt.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Eksempel: Opprett en faktureringsregel som er basert på antallet enheter som er levert

Organisasjonen går inn i en avtale for å gi totalt fem opplæringsøkter til en kundes ansatte til en kostnad på 10 000 per opplæringsøkt. Du fakturerer kunden etter hver opplæringsøkt. 

Når du definerer faktureringsreglene for kontrakten, bruker du følgende verdier:

-   Leveringsenheten er én opplæringsøkt.
-   Enhetsprisen er 10 000 per opplæringsøkt.
-   Det totale antallet enheter er fem opplæringsøkter.

Når du har fullført én opplæringsøkt, kan du opprette en faktura på 10 000 for den første enheten som er levert, og sende fakturaen til kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Eksempel: Opprett en faktureringsregel som er basert på en bestemt prosentandel av prosjektfullførelsen (manuell beregning)

Organisasjonen din, et programvarekonsulentfirma, inngår en avtale med en kunde for å utvikle en del av et produkt som kunden utvikler. Organisasjonen din godtar å levere programvarekoden over en periode på seks måneder. Kunden avtaler å betale organisasjonen en sum på 100 000 for arbeidet. Du oppretter en faktureringsregel for å fakturere kunden basert på prosentandelen av arbeid som er fullført på prosjektet, som angitt i kontrakten.

-   På slutten av den første måneden møter du kunden for å bestemme fullføringsprosenten for arbeidet som er fullført. Når du og kunden ser gjennom prosjektet, avgjør du at prosjektet er 15 % fullført.
-   Du oppretter en faktura på 15 000 (15 prosent av 100 000) og sender den til kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Eksempel: Opprett en faktureringsregel som er basert på en bestemt prosentandel av prosjektfullførelsen (automatisk beregning)

Organisasjonen din, et selskap for programvareutvikling, avtaler å utvikle en lønnsregnskapspakke for en kunde for 30 000. Kunden avtaler å betale organisasjonen basert på en prosentandel fullført arbeid. Du beregner at prosjektkostnadene er 20 000. Prosjektkontrakten spesifiserer arbeidskategoriene du bruker i faktureringsprosessen. Du definerer faktureringsregler som automatisk beregner fakturabeløpene for prosentandelen arbeid som er fullført for hver kategori. Du definerer et budsjett for hver kategori:

-   **Utvikling** – Kostnad på 15 000 og omsetning på 20 000
-   **Installasjon** – Kostnad på 5 000 og omsetning på 10 000

Når du oppretter en kundefaktura for første gang, beregnes fakturabeløpet automatisk basert på følgende informasjon:

-   Etter en måned sender arbeideren i prosjektet en timeregistrering for prosjektet. Kostnaden for arbeiderens timer er 5 000 for utvikling og 1 000 for installasjon. Utviklingsarbeidet er 33 prosent fullført (5 000 faktisk kostnad / 15 000 budsjettkostnader), og installasjonsarbeidet er 20 prosent fullført (1 000 faktisk kostnad / 5 000 budsjettkostnad).
-   Fakturabeløpet på 8 667 beregnes automatisk (33 prosent av 20 000 + 20 prosent av 10 000).
-   Du oppretter en faktura på 8,667 og sender den til kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Eksempel: Opprett en faktureringsregel som er basert på avtalte milepæler

Organisasjonen din, et konsulentfirma for ledelse, avtaler å gjennomføre markedsundersøkelse for et forbrukerprodukt som kunden planlegger å selge. Kunden avtaler å bruke tjenestene dine i tre måneder, fra og med mars, og godtar å betale organisasjonen 50 000. Prosjektet har tre milepæler:

-   Milepæl 1: Samle inn forbrukerdata – 31. mars
-   Milepæl 2: Analysere forbrukerdata – 30. april
-   Milepæl 3: Presentere et forslag til produktets levedyktighet – 31. mai

Kunden avtaler å betale organisasjonen 10 000 for den første milepælen, 20 000 for den andre milepælen og 20 000 for den tredje milepælen. 

Når du setter opp prosjektkontrakten, godtar du at kunden faktureres basert på milepælen som er fullført. Faktureringsregeloppsettet inkluderer følgende trinn:

-   Definer milepælene for prosjektet.
-   Definer beløpet som skal faktureres for kunden når hver milepæl er fullført.

Når den første milepælen er fullført 31. mars, merker du milepælen som fullført, og deretter oppretter du en faktura på 10 000 og sender den til kunden. Du kan ikke opprette en faktura for en milepæl før du har merket milepælen som fullført.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Eksempel: Opprett en faktureringsregel som er basert på tjenester pluss et administrasjonsgebyr

Organisasjonen din, et konsulentfirma for ledelse, avtaler å gjennomføre markedsundersøkelser for å evaluere levedyktigheten til et produkt som kunden, et detaljhandelsselskap, utvikler. Vilkårene i avtalen angir at du tilbyr tjenestene til de tre beste ledelseskonsulentene, som skal utføre undersøkelsen på tid og materialer-basis. Kunden godtar å betale 100 per time, pluss et 10 prosent administrasjonsgebyr for konsulenttimene som blir belastet prosjektet. 

Når du setter opp prosjektkontrakten, oppretter du en faktureringsregel som legger til 10 prosent administrasjonsgebyr på konsulenttimene som belastes prosjektet. 

Når du oppretter en faktura for kunden, faktureres kunden et administrasjonsgebyr på 10 %, pluss kostnadene for konsulenttimene. Hvis de tre konsulenter for eksempel arbeidet totalt 200 timer på prosjektet, opprettes det en faktura på 22 000 basert på følgende beregning:

-   200 timer à 100 per time = 20 000
-   10 prosent administrasjonsgebyr = 2 000
-   Totalt fakturabeløp = 22 000

Hvis gebyrer er avgiftspliktige til en kunde, og du velger en mva-gruppe i prosjektkontrakten, angis mva-gruppen automatisk i en faktureringsregel for gebyrer.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Eksempel: Opprett en faktureringsregel for verdien av tid og materialer

Organisasjonen din, et programvarekonsulentfirma, er enige om å gi fem tekniske konsulenter mulighet til å arbeide med et programvareutviklingsprosjekt for en kunde i de neste seks månedene. Kunden godtar å betale 150 for hver konsulenttime, pluss kostnadene for kontorutstyr. Organisasjonen din sender en faktura til kunden i slutten av hver måned. 

Når du setter opp prosjektkontrakten, godtar du at kunden faktureres hver måned for tid og materialer på prosjektet. Du oppretter en faktureringsregel som inneholder følgende informasjon:

-   Kontraktperioden er seks måneder.
-   Konsulenttiden blir beregnet med en sats på 150 per time.
-   Kontorrekvisita er fakturert med kostnad, og totale kostnader for prosjektet må ikke overskride 10 000.
-   Du oppretter en kundefaktura på slutten av hver kalendermåned i løpet av prosjektet.

I løpet av den første måneden registreres totalt 800 timer av konsulentene i prosjektet. Kostnadene for kontorutstyr som er belastet for prosjektet, er 2 000. På slutten av måneden oppretter du derfor en faktura på 122 000, som beregnes som 800 timer til 150 per time, og i tillegg 2 000 for kontorutstyr.



