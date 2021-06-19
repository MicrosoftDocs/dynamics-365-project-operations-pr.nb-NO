---
title: Arbeide med datamodell for Project Service Automation
description: Dette emnet gir informasjon om hvordan du arbeider med datamodellen.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 37c7b15daa75cc3ba53ff6a3bcc0ab54717aa62d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008818"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Arbeide med datamodell for Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation utvider andre appenheter og introduserer sine egne enheter i Common Data Service-datamodellen. Dette emnet beskriver noen av enhetene som du støter på i vanlige scenarioer for PSA-rapportering.

## <a name="reporting-on-opportunities"></a>Rapportere om salgsmuligheter

Project Service Automation utvider **Salgsmulighet**-enheten i Dynamics 365 Sales ved å legge til felt som gjør det mulig å legge til prosjektrelaterte scenarier. Disse feltene er identifisert av et skjemanavn som har prefikset **msdyn\_**. Ett nytt felt som er viktig for rapportering om PSA-salgsmuligheter, er **Ordretype**. Verdien **Arbeidsbasert** for dette feltet angir at salgsmuligheten er en PSA-mulighet. Andre felt som er lagt til i enheten, omfatter **Kontraktsorganisasjon**, som fanger opp organisasjonen som holder salgsmuligheten, og **Forretningsforbindelsesbehandling**, som registrerer navnet på den som er ansvarlig for forretningsforbindelsen som er ansvarlig for salgsmuligheten.

Enheten **Salgsmulighetslinje** inneholder også felt som er relatert til Project Service. **Faktureringsmetode** angir om salgsmulighetslinjen skal faktureres for tid og materialer eller en fast prisbasis, og **Prosjekt** henter navnet på prosjektet som støtter salgsmuligheten. Andre felt som du kan rapportere om, henter kostnader og kundebudsjettbeløp for linjeelementet.

## <a name="reporting-on-quotes"></a>Rapportere om tilbud

PSA utvider enheten **Tilbud** i Sales enheten ved å legge til prosjektrelaterte felt. **Ordretype** skiller PSA-tilbud fra ikke-PSA-tilbud. Verdien **Arbeidsbasert** for dette feltet angir at tilbudet er et PSA-tilbud. Andre felt som kan være relevante for rapportering av PSA-tilbud, inkluderer beløpsfelt som **Belastbare kostnader**, **Ikke-belastbare kostnader**, **Bruttofortjeneste**, **Estimater** og **Budsjett**. Andre nyttige felt angir om tilbudet er lønnsomt, om det skal fullføres etter planen, og om det overholder kundens forventninger til budsjettet.

PSA utvider også **Tilbudslinje**-enheten i Sales. Ett felt som legges til av PSA, er **Faktureringsmetode**, som angir hvordan tilbudslinjen skal faktureres (tid og materialer eller fast pris). Andre felt som er lagt til i enheten, registrerer det relaterte prosjektet som støtter tilbudslinjen, fakturering, kostnad og budsjett.

PSA legger også til nye tilbudsrelaterte enheter i Dynamics 365-datamodellen. Her er noen eksempler:

- **Tilbudslinjedetalj** – denne enheten inneholder prosjektestimatdetaljene for tilbudslinjen. Den har to oppføringer for hver tilbudslinje. Den ene oppføringen lagrer kostnaden og kostnadsdetaljene for tilbudslinjen, og den andre oppføringen lagrer salgsbeløpet og salgsdetaljene for tilbudslinjen.
- **Fakturaplan for tilbudslinje** – denne enheten inneholder faktureringsplanen for tilbudslinjen. Denne tidsplanen genereres basert på faktureringshyppigheten som er tilordnet til tilbudslinjen.
- **Milepæler for tilbudslinjer** – denne enheten inneholder faktureringsmilepælene for tilbudslinjer basert på fast pris.
- **Analysenedbrytinger for tilbudslinje** – denne enheten inneholder økonomiske detaljer for tilbudslinjen. Disse detaljene kan være nyttige til å rapportere oppgitte beløp for salg og beregnede kostnader etter forskjellige dimensjoner.

Andre enheter som PSA legger til i tilbudene, er **Prosjektprislinje for tilbudslinje**, **Ressurskategori for tilbudslinje** og **Transaksjonskategori for tilbudslinje**.

![Diagram som viser tilbud, tilbudslinje og prosjektrelasjoner](media/PS-Reporting-image2.png "Diagram som viser tilbud, tilbudslinje og prosjektrelasjoner")

## <a name="reporting-on-project-contracts"></a>Rapportere om prosjektkontrakter

PSA utvider **Ordre**-enheten i Sales som brukes når prosjektkontrakter registreres. Det legger til et viktig nytt felt, **Ordretype**, som identifiserer kontrakten som en PSA-prosjektkontrakt i stedet for en salgsordre. Verdien **Arbeidsbasert** for dette feltet angir at salgsordren er en PSA-prosjektkontrakt. Andre nye felt som legges til i **Ordre**-enheten, fanger opp detaljer om kostnader, status for PSA-kontrakt og organisasjonen som eier kontrakten.

PSA utvider også **Salgsordrelinje**-enheten. Blant feltene som legges til, er felt som registrerer faktureringsmetoden (etter materialer eller fast pris), kundebudsjettbeløp og det underliggende prosjektet.

PSA legger også til nye enheter som er utformet for prosjektkontrakter. Her er noen eksempler:

- **Prosjektkontraktlinjedetalj** – denne enheten inneholder detaljer på linjenivå som er oppsummert til kontraktlinjebeløpet. Dette kan være så detaljerte som linjeelementer som genereres fra en prosjektplan på oppgavenivå.
- **Fakturaplan for kontraktlinje** – denne enheten inneholder faktureringsplanen som genereres basert på fakturahyppigheten som er tilordnet til kontraktlinjen.
- **Milepæl for kontrakt** – denne enheten inneholder faktureringsmilepælene for kontraktlinjer som har en faktureringsterm med fast pris.

Andre enheter som PSA legger til i kontrakter, er **Prosjektprisliste for prosjektkontraktslinje**, **Ressurskategori for prosjektkontraktslinje** og **Transaksjonskategori for prosjektkontraktslnje**.

![Diagram som viser ordre, ordrelinje og prosjektrelasjoner](media/PS-Reporting-image3.png "Diagram som viser ordre, ordrelinje og prosjektrelasjoner")

## <a name="reporting-on-projects"></a>Rapportere om prosjekter

**Prosjekter**-enheten og de relaterte enhetene er eksklusive for PSA. **Prosjekt** er enheten på øverste nivå som brukes til å fange opp arbeids- og kostnadssiden i driften. Her er en liste over de relaterte enhetene:

- **Prosjektteammedlem** – denne enheten inneholder detaljer om de bestillbare ressursene som er tilordnet til prosjektet. Disse ressursene kan være generelt bestillbare ressurser, eller de kan være navngitte bestillbare ressurser som enten angis av prosjektlederen, eller som genereres fra prosjektplanen.
- **Prosjektoppgave** – denne enheten inneholder oppgavene som utgjør prosjektplanen eller tidsplanen.
- **Ressurstildeling** – denne enheten inneholder oppgavetildelingen for den bestillbare ressursen.
- **Ressurskrav** – denne enheten inneholder kravene for alle generelle ressursteammedlemmer.
- **Estimat** og **Estimatlinje** – disse enhetene har en relasjon mellom overskrift/linje og inneholder utgiftsestimater for prosjektet. Oppgaveestimater lagres i enheten **Ressursestimat**.

![Diagram som viser ressurskrav og prosjektrelasjoner](media/PS-Reporting-image4.png "Diagram som viser ressurskrav og prosjektrelasjoner")

## <a name="reporting-on-resources"></a>Rapportere om ressurser

Prosjektressurser bruker de **bestillbare ressursenhetene** fra Universal Resource Scheduling (URS) som deles med andre apper, for eksempel Microsoft Dynamics 365 Field Service. Her er en liste over enhetene du kanskje må bruke når du rapporterer om prosjektressurser:

- **Bestillbar ressurs** – denne enheten representerer brukeren, kontakten, den generelle ressursen, forretningsforbindelsen, gruppen eller utstyret som brukes i prosjektteamet.
- **Kjennetegn for ressurs som kan reserveres** – denne enheten inkluderer ferdigheter, sertifiseringer eller utdannelse for ressursen. Egenskapene kan ha vurderingsverdier som defineres av vurderingsmodellen.
- **Kategori for ressurs som kan reserveres** – denne enheten representerer rollen til den bestillbare ressursen.
- **Bestillinger av ressurs som kan reserveres** – denne enheten representerer tiden som er bestilt til prosjekter for ressursen. Hver bestilling har både en hodeenhet og linjeenheter, og hver linje har en status som representerer statusen for bestillingen.

![Diagram som viser relasjoner for reserverbare ressursegenskaper](media/PS-Reporting-image5.png "Diagram som viser relasjoner for reserverbare ressursegenskaper")

## <a name="reporting-on-actual-transactions"></a>Rapportere om faktiske transaksjoner

Når du godkjenner en timeregistrering eller utgift, eller fakturerer en kontrakt i PSA, registreres forretningstransaksjonen i enheten **Faktisk verdi**. Denne enheten kan fungere som grunnlag for nesten alle finansieringsrelaterte rapporter i PSA. Enheten **Faktisk verdi** registrerer kostnads- og salgstransaksjonene for forretningsarrangementet. Det fanger også opp mange relevante attributter.

Når du arbeider med den enheten **Faktisk verdi**, er det viktig at du forstår hvilke transaksjoner som registreres i enheten, og når transaksjonene registreres. Her er den typiske flyten når du arbeider med tidsoppføringer (flyten for utgiftsoppføringer er lik):

1. Når tidsoppføringen lagres, opprettes det ingen oppføringer i enheten **Faktisk verdi**.
2. Når tidsoppføringen sendes, opprettes det ingen oppføringer i enheten **Faktisk verdi**.
3. Når tidsoppføringen er godkjent, opprettes det én oppføring i enheten **Faktisk verdi**, og det kan også opprettes en ny oppføring. Den første oppføringen lagrer kostnadene for tidsoppføringen. Den andre oppføringen lagrer det ikke-fakturerte salgsbeløpet for tidsoppføringen. Den andre oppføringen er avhengig av at prosjektet enten har en kunde, et tilbud eller en kontraktlinje tilordnet seg.

    | Dokumentdato | Transaksjonstype | Transaksjonsklasse | Kunde         | Kontrakt   | Ressurs     | Ressursrolle | Faktureringstype | Antall | Enhetspris | Beløp |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Kostnad             | Time              | Alpine Ski House | Alpine CRM | Aurora Tharaldsen | Prosjektleder   | Belastbar   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Ufakturert salg   | Time              | Alpine Ski House | Alpine CRM | Aurora Tharaldsen | Prosjektleder   | Belastbar   | 8.0      | 100.00     | 800.00 |

    Disse to oppføringene er separate, men relaterte oppføringer. De er verken debit eller kredit.

4. Hvis en kontrakt er knyttet til prosjektet, opprettes det to flere oppføringer i enheten **Faktisk verdi** når tidsoppføringen blir fakturert. Først opprettes det et negativt beløp for den ikke-fakturerte salgsoppføringen. Denne oppføringen reverserer det ikke-fakturerte salget. Deretter opprettes det en transaksjon for det fakturerte salget. Disse oppføringene er separate, men relaterte oppføringer, ikke debet og ikke kredit.

    | Dokumentdato | Transaksjonstype | Transaksjonsklasse | Kunde         | Kontrakt   | Ressurs     | Ressursrolle | Faktureringstype | Antall | Enhetspris | Beløp   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Ufakturert salg   | Time              | Alpine Ski House | Alpine CRM | Aurora Tharaldsen | Prosjektleder   | Belastbar   | - 8,0    | 100.00     | - 800,00 |
    | 2/4/18        | Fakturert salg     | Time              | Alpine Ski House | Alpine CRM | Aurora Tharaldsen | Prosjektleder   | Belastbar   | 8.0      | 100.00     | 800.00   |

Enheten **Transaksjonsopprinnelse** registrerer opprinnelsen til oppføringen **Faktisk verdi**, og enheten **Transaksjonstilkobling** registrerer de relaterte oppføringene for oppføringen **Faktisk verdi**. I tillegg inneholder oppføringen **Faktisk verdi** referanser til prosjektet, prosjektkontrakten (ordre), den bestillbare ressursen og kunden.

![Diagram som viser transaksjonstilkobling, opprinnelse og faktiske relasjoner](media/PS-Reporting-image6.png "Diagram som viser transaksjonstilkobling, opprinnelse og faktiske relasjoner")


[!INCLUDE[footer-include](../includes/footer-banner.md)]