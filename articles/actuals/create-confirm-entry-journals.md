---
title: Opprette og bekrefte oppføringsjournaler
description: Dette emnet inneholder informasjon om hvordan du oppretter og bekrefter oppføringsjournaler i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584240"
---
# <a name="create-and-confirm-entry-journals"></a>Opprette og bekrefte oppføringsjournaler

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Du bruker oppføringsjournalene til å registrere faktiske data direkte i Microsoft Dynamics 365 Project Operations. Når du bruker oppføringsjournaler, trenger du ikke å angi tids-, utgifts- og materialbrukslogger i Project Operations.

Med én enkelt oppføringsjournal kan du opprette flere journallinjer. Når journalen er bekreftet, registrerer en oppføringsjournallinje den faktiske verdien for følgende detaljer:

- Kostnaden eller inntekten, avhengig av transaksjonstypen som ble valgt.
- Den valgte transaksjonsklassen. De tilgjengelige klassene er **Tid**, **Utgift**, **Materiale**, **Honorar**, **Milepæl** og **Avgift**.
- Prosjektet og/eller en oppgave som er valgt på journallinjen.

Følg denne fremgangsmåten for å opprette en oppføringsjournal i Project Operations.

1. Gå til **Salg** \> **Transaksjoner** \> **Journaler**.
2. På listesiden **Oppføringsjournaler**, i handlingsruten, velger du **Ny** for å opprette en journal.
3. På siden **Ny journal**, i **Beskrivelse**-feltet, skriver du inn en beskrivelse av journalen.
4. Kontroller at feltet **Journaltype** er satt til **Oppføring**, og velg deretter **Lagre**. Når den nye oppføringsjournalen er lagret, skal fanen **Journallinjer** vises på journalsiden.
5. På fanen **Journallinjer**, på verktøylinjen over rutenettet, velger du **Ny** for å opprette en oppføringsjournallinje.
6. I dialogboksen **Hurtigoppretting** for oppretting av en oppføringsjournallinje angir du feltene slik de er beskrevet i tabellen nedenfor.

    | Felt | Bekrivelse | Funksjonsinnvirkning |
    | --- | --- | --- |
    | Transaksjonsklasse | Journallinjen kan klassifiseres i én av de seks transaksjonsklassene: **Tid**, **Utgift**, **Materiale**, **Honorar**, **Milepøl** eller **Avgift**. | **Avgift**-transaksjonsklassen er avskrevet i Project Operations. <br> Hvis du oppretter en **Avgift**-transaksjonsklasse, behandles den ikke ved fakturering eller i beregning av kostnader eller inntekt. **Milepæl** er en transaksjonsklasse som bare gjelder inntekt. <br>Transaksjonsklassen **Honorar** representerer et forskudd som ble mottatt fra en kunde. Den må alltid opprettes som et par med fakturerte og ufakturerte salgsjournallinjer. |
    | Transaksjonstype | Transaksjonstypene **Kostnad**, **Salg mellom organisasjoner** og **Kostnad for ressursenhet** skal brukes til å registrere kostnader.<br> Transaksjonstypene **Ufakturert salg** og **Fakturert salg** skal brukes til å registrere inntekt. | Transaksjonsklassen **Honorer** fungerer bare med transaksjonstypene **Ufakturert salg** og **Fakturert salg**.<br> Transaksjonsklassen **Milepæl** fungerer bare med transaksjonstypen **Fakturert salg**. <br>Transaksjonstypene **Salg mellom organisasjoner** og **Kostnad for ressursenhet** gjelder bare for transaksjonsklassen **Tid**, og disse kan bare brukes i oppføringsjournaler i Lite-distribusjonen, og ikke ved distribusjon av Project Operations i ressursbaserte/ikke-lagerførte scenarioer. |
    | Velg produkt | Når transaksjonsklassen **Materiale** er valgt, kan du i dette feltet angi om materialtransaksjonen du oppretter journallinjen for, er et eksisterende produkt eller et produkt som ikke finnes i produktkatalogen. | Hvis du velger **Ikke i produktkatalog**, kan du skrive inn et navn på produktet. |
    | Produkt | En referanse til produktet fra katalogen. | |
    | Bekrivelse | En beskrivelse av journallinjen for å gjøre den enkel å identifisere. | For ufakturerte salgsjournallinjer brukes verdien som beskrivelse når fakturalinjedetaljene opprettes. |
    | Ekstern beskrivelse | En beskrivelse av journallinjen som kan brukes til deling med eksterne interessenter. | For ufakturerte salgsjournallinjer brukes verdien som ekstern beskrivelse når fakturalinjedetaljene opprettes. Den kan også vises på fakturaen som sendes til kunden. |
    | Faktureringstype | En verdi som angir om journallinjen skal telles som en belastbar, gratis eller ikke-belastbar komponent i prosjektet. | I en vanlig flyt avledes faktureringstypen fra de avtalte betingelsene som er angitt på kontrakten. Når du registrerer en journallinje, kan du imidlertid angi en verdi i dette feltet. |
    | Dokumentdato | Bruk datoen da transaksjonen inntraff. | |
    | Startdato | Bruk datoen da transaksjonen inntraff. | Dette feltet brukes til å sammenligne med datoen for oppretting av en faktura for transaksjoner av typen **Ufakturert salg**. Denne sammenligningen hjelper deg med å avgjøre om transaksjonen er datert i fremtiden eller i fortiden. Bare transaksjoner der datoen er passert, blir lagt til i fakturaen. |
    | Sluttdato | Bruk datoen da transaksjonen inntraff. | |
    | Regnskapsdato | Bruk datoen da regnskapsinnvirkningen blir registrert. | |
    | Kontraktlinjekunde | Hvis kontraktlinjen bare har én kunde, angis dette feltet som standard til kunden på kontraktlinjen når journallinjen lagres. Hvis kontraktlinjen har flere kunder, må du velge riktig kunde på kontraktlinjen. | Hvis systemet ikke kan fastsette kontraktlinjekunden på journallinjen, og hvis den er tom for den faktiske verdien av typen **Ufakturert salg** som opprettes fra journallinjen, blir ikke den faktiske verdien fakturert. |
    | Project | Velg prosjektet du vil registrere den faktiske verdien i. | Basert på valgt prosjekt, transaksjonsklasse og oppgave vil systemet prøve å fastsette kontrakten, kontraktlinjen og kontraktlinjekunden. |
    | Oppgave | Velg oppgaven du vil registrere den faktiske verdien i. | Hvis du tilknytter oppgaver med kontraktlinjer under kontraktoppsettet, bruker systemet den valgte oppgaven, sammen med et prosjekt og en transaksjonsklasse, til å bestemme kontrakten, kontraktlinjen og kontraktlinjekunden. |
    | Transaksjonskategori | Velg transaksjonskategorien du vil registrere den faktiske verdien i. | For utgifter bestemmer den valgte transaksjonskategorien standardprisen som skal angis på journallinjen når den lagres. |
    | Rolle | Dette feltet er relevant for tidsjournallinjer. Velg rollen til ressursen som brukte tid på prosjektet og/eller oppgaven. | Hvis du bruker standardkonfigurasjonen for Tid-journallinjer til å angi standard ressurskostnader og fakturasatser, brukes den valgte rollen sammen med ressursenheten til å fastsette standardprisen som skal angis på journallinjen når den lagres. Hvis du bruker en egendefinert konfigurasjon for oppføring av standardpriser, bør du se gjennom denne konfigurasjonen for å finne ut om **Rolle**-feltet brukes til å angi standard prisverdier. |
    | Underkontrakt | Hvis journallinjen representerer en kapasitet i en underkontrakt eller utgifter eller materiell i en underkontrakt, må du velge den relevante underkontrakten. | Når kostnadsjournallinjer registreres, bestemmer den valgte underkontrakten prislisten som brukes til å angi standard enhetskostnad. |
    | Underkontraktlinje | Hvis journallinjen representerer en kapasitet i en underkontrakt eller utgifter eller materiell i en underkontrakt, må du velge den relevante underkontraktlinjen. | Når du registrerer kostnadsjournallinjer, sikrer den valgte underkontraktlinjen at de tilgjengelige kapasitetsberegningene for underkontraktlinjen beregnes riktig. |
    | Beløpsmetode | Dette feltet er angitt til **Multipliser antall med pris** som standard. Når denne metoden brukes, beregnes beløpet som *Antall* × *Pris*. Den andre metoden som støttes, er **Fast pris**. Når denne metoden brukes, blir prisen satt til beløpet, og antallet vil ikke bli brukt i beregningen. | |
    | Enhetsplan og enhet | Sammen identifiserer enhetsplanen og enheten antallsenheten. | Kombinasjonen av enheten og transaksjonskategorien brukes til å angi standardpriser for utgifter. I standardkonfigurasjonen av Project Operations brukes kombinasjonen av enheten, rollen og ressursenheten til å angi standardpriser for tid. Hvis du har en tilpasset konfigurasjon for oppføring av standardpriser, brukes den sammen med enheten. Kombinasjonen av produktet og enheten brukes til å angi standardpriser for materialer. |
    | Antall | Anti antallet. | |
    | Pris | Hvis prisen står tom når journallinjen opprettes, brukes de relevante verdiene til å angi standardprisene, avhengig av transaksjonsklassen. Hvis en pris angis når journallinjen opprettes, brukes den prisen. | |
    | Avgift | Angi et hvilket som helst avgiftsbeløp. | Avhengig av avgiftsbeløpet som er angitt, beregnes det utvidede beløpet som *Beløp* + *Avgift*. |

## <a name="confirm-an-entry-journal"></a>Bekreft en oppføringsjournal

Når du har angitt alle journallinjene i en oppføringsjournal, kan du bekrefte journalen. Denne prosessen registrerer hver journallinje som faktiske verdier i de aktuelle prosjektene.

Når en journal er bekreftet, kan du ikke lenger redigere den eller noen av linjene.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Faktiske verdier opprettet ved hjelp av bekreftelse av oppføringsjournal

Det finnes noen få viktige forskjeller mellom faktiske verdier som opprettes ved hjelp av bekreftelse av oppføringsjournal og faktiske data som opprettes under godkjenning av tids-, utgifts- og materialbrukslogger og fakturabekreftelse i Project Operations:

- Oppføringsjournaler bruker ikke transaksjonstilkoblinger til å koble faktiske verdier til ufakturert faktisk salg. De faktiske verdiene som opprettes når tids-, utgifts- og materialbrukslogger godkjennes, bruker alltid transaksjonstilkoblinger til å koble kostnader og ufakturert faktisk salg.
- Oppføringsjournaler bruker ikke transaksjonsopprinnelser til å koble faktiske verdier og ufakturert faktisk salg til en opprinnelig oppføring. De faktiske verdiene som opprettes når tids-, utgifts- og materialbrukslogger godkjennes, bruker alltid transaksjonsopprinnelser til å koble kostnader og ufakturert faktisk salg til den opprinnelige tidsoppføringen.
- Når ufakturert faktisk salg som opprettes av bekreftelse på oppføringsjournalen faktureres, kobles de fakturerte faktiske salgene som opprettes under fakturabekreftelsen, til det ufakturerte faktiske salget, på samme måte som ufakturert faktisk salg som opprettes når loggene for tids-, utgifts- og materialbruk godkjennes.
- Oppføringsjournallinjer som opprettes for tid som angis av interorganisasjonelle ressurser, fører ikke til at faktiske verdier for typene **Kostnad for ressursenhet** og **Salg mellom organisasjoner** blir opprettet automatisk. Disse faktiske verdiene må opprettes manuelt. Denne virkemåten er forskjellig fra funksjonaliteten for tidsoppføringer som registreres av interorganisasjonelle ressurser. Når tiden er godkjent, oppretter appen i så fall automatisk faktiske data av typen **Kostnad** i prosjektet og faktiske verdier for typene **Kostnad for ressursenhet** og **Salg mellom organisasjoner** i den ansattes eiende divisjon. Deretter brukes transaksjonstilkoblinger til å koble sammen de faktiske verdiene og transaksjonsopprinnelsene for å koble dem til den opprinnelige tidsoppføringen.
- Når oppføringsjournaler bekreftes, opprettes faktiske verdier. Korreksjonsjournaler kan imidlertid ikke brukes til å korrigere disse faktiske verdiene. Denne virkemåten er forskjellig fra funksjonaliteten for faktiske verdier som opprettes når tids-, utgifts- og materialbrukslogger godkjennes. I slike tilfeller kan du bruke korreksjonsjournaler i appen til å korrigere de faktiske verdiene for å rette opp eventuelle feil, forutsatt at de faktiske verdiene ikke er fakturert ennå. Hvis de allerede er fakturert, kan du fremdeles korrigere en faktisk verdi hvis du behandler en full kreditt på den faktiske verdien til kunden.

> [!NOTE]
> Oppføringsjournaler håndhever ikke strenge standardregler. Bruk derfor disse oppføringsjournalene så lite som mulig, og vær forsiktig og pass på at du ikke oppretter skadde finansielle data i systemet. Når du kan, bruker du tids-, utgifts- og materialbrukslogger, milepæl- og honoraroppsettet for prosjektkontrakter og prosjektfakturabekreftelsesprosessen i stedet for oppføringsjournaler til å opprette faktiske verdier.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
