---
title: Nyheter mars 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Dette emnet inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra mars 2022.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600754"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter mars 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

*Gjelder: Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer*

Dette emnet gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.30.0.99
- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.25

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

Kostgodtgjørelser støttes nå i det nye og nyskapte moderne arbeidsområdet for utgifter. Firmaer som bruker kostgodtgjørelse, kan aktivere denne funksjonen for å gi brukere en enkel måte å sende inn og få refusjon for utgiftene til kostgodtgjørelse. Hvis du vil ha mer informasjon, kan du se [Utgifter til kostgodtgjørelse](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Listen nedenfor viser tilordningene for dobbel skriving som er endret eller lagt til i mars 2022-versjonen av Project Operations.

| **Enhetstilordning** | **Oppdatert versjon** | **Kommentarer** |
| --- | --- | --- |
| Project Operations-integrering, prosjektleverandør fakturalinjeeksportenhet msdyn\_projectvendorinvoicelines | 1.0.0.3 | Tilordninger oppdateres for å samsvare med enheten Leverandørfakturalinje i Dataverse. <br>Ikke aktiver tilordning av versjon 1.0.0.4. Den vil være klar til bruk sammen med Finance-miljøet versjon 10.0.26 i den neste månedlige oppdateringen. |

Kjør alltid den nyeste versjonen av tilordningen i miljøet, og aktiver alle relaterte tabelltilordninger når du oppdaterer versjonen av Project Operations Dataverse-løsningen og Finance-løsningen. Enkelte funksjoner fungerer kanskje ikke riktig hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en bruksklar tabelltilordning, bruker du endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem når du starter tilordningen, følger du instruksjonene i delen [Problemer med manglende tabellkolonner i tilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Tid og utgifter | 2388011 | Vis avslagskommentarer til innsendere av tidsoppføringer under massegodkjenning. |
| Prosjektplanlegging og sporing | 2495294 | Prosjektdetaljer kan ikke redigeres på **Oppgavedetaljer**-siden. |
| Fakturering og prising | 2499605 | Kontraktmilepæler som opprettes fra tilbudsmilepæler, er feilmarkert som skrivebeskyttet. |
| Prosjektplanlegging og sporing | 2506050 | Operasjonssettet står på vent i én time hvis det ikke er endringer som skal lagres. Settet merkes deretter som **Mislykket**, mens det skulle vært fullført umiddelbart. |
| Fakturering og prising | 2507401 | Standard kontraktsenheter er feil angitt på prosjekter på grunn av feil hurtigbufring. |
| Fakturering og prising | 2541660 | **Validering av oppretting av salgsordre** i dobbel skriving skal bare være for prosjektbaserte ordrer. |
| Fakturering og prising | 2552745 | Avgifter deles ikke mellom kunder som har konfigurert delte faktureringsregler. |
| Fakturering og prising | 2558859 | Forbedrede feilmeldinger når prisdimensjoner er konfigurert. |
| Fakturering og prising | 2558933 | **Import fra prosjektestimater** mislykkes når **msdyn\_project** er lagt til som en prisdimensjon. |
| Fakturering og prising | 2559101 | Sletting av prosjektparametere er ikke blokkert og forårsaker problemer. |
|   Administrasjon av salgsmuligheter | 2570390 | Plugin-modulen for dobbel skriving tvinger kontotypen i tilbud, bestillinger og muligheter til å være **Kunde**, selv når denne kontotypen ikke er korrekt. |
| Fakturering og prising | 2586097 | Deling av fakturerte faktiske kostnader reverseres ikke når et prosjekt fjernes fra en prosjektkontraktlinje. |
| Fakturering og prising | 2589619 | Avgifter på materiell som ikke er i katalogen, overføres til ufakturert faktisk salg og til fakturaen. |
|   Administrasjon av salgsmuligheter | 2594015 | Et tilbud kan ikke lukkes som vunnet for kunder som har **Net60**-betalingsbetingelser. |
| Prosjektplanlegging og sporing | 2595841 | I Project for the Web mottar brukerne en feilmelding om en manglende **msdyn\_actualstart** når de oppretter en ny ressursforespørsel. |
| Tid og utgift | 2602511 | Feltet **Avvist av** for tidsoppføringer viser **System** i stedet for en navngitt bruker som avviser. |
| Tid og utgift | 2602528 | En prosjektgodkjenner kan godkjenne tid på prosjekter der de ikke er oppført som godkjennere. |
| Fakturering og prising | 2608550 | En korrigeringsfaktura kan bekreftes selv om det ikke er endringer i originalen. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Prosjektstyring og regnskap | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Det er manglende samsvar mellom Finance og Project Operations i den tillatte lengden for feltet **Kategori-ID**. |
| Prosjektstyring og regnskap | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Prosjekter med fast pris kan ikke fjernes når feltet **A konto-fakturering** er angitt til **Resultat** og prinsippet **Fullført prosent** brukes. |
| Prosjektstyring og regnskap | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | En feil standard mva-gruppe er angitt fra prosjektoppsettet på utgiftslinjer i journalen for Project Operations-integrering. |
| Prosjektstyring og regnskap | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Du kan ikke redigere overskriftsdimensjoner for prosjektfakturaforslag i en integrert distribusjon med Project Operations. |
| Prosjektstyring og regnskap | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Konserninterne leverandørfakturaer må ikke integreres med Dataverse. |
| Prosjektstyring og regnskap | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Det er manglende samsvar mellom valutaen for kundesaldoer og rapporteringsvalutaen. |
| Prosjektstyring og regnskap | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Du kan postere en prosjektfaktura selv om kunden er på vent for alle fakturaer. |
| Prosjektstyring og regnskap | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Knappen **Slett alle linjer** mangler i prosjektfakturaforslag som har visningene **Overskrift** og **Linjer**. |
| Prosjektstyring og regnskap | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Når du posterer en leverandørfaktura, vises følgende feilmelding: "Regnskapsdatoen for fakturaen må være i samme regnskapsår som den relaterte bestillingen. Kjør årsavslutningsprosessen for bestillingen, eller endre datoen til gjeldende regnskapsår." |
| Reise og utgift | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Den igangsatte kostnaden for et prosjekt frigis ikke etter at den igangsatte kostnaden for reiserekvisisjonen er frigitt. |
| Reise og utgift | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Følgende feil oppstår når du sender en utgiftsrapport "Stakksporing: Firmaet finnes ikke." |
| Reise og utgift | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Standard **Prosjekt-ID** angis ikke i reiseregninger når parameteren **Krev aktivitet for journal** er valgt i prosjektet. |
| Reise og utgift | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Knappen **Poster utgifter** fungerer ikke som den skal i Project Operations for ressursbaserte/ikke-lagerførte scenarioer. |
| Reise og utgift | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Det oppstår et problem med **Sats per kilometer** for en reiseregning med kjørelengde som inkluderer passasjerer. |
| Reise og utgift | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Satser for kjørelengdeutgifter for ansatte summeres ikke riktig når to forskjellige biltyper er brukt i utgiftskategorien **Satsnivåer for kjørelengde**. |
| Reise og utgift | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Oppslaget for **Prosjekt**-feltet på en reiserekvisisjonslinje returnerer ikke riktig liste over prosjekter. |
| Reise og utgift | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Kjørelengde til gjennomgang** viser en advarsel om reiseregninger. |
| Reise og utgift | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | OCR-tjenesten (optisk tegngjenkjenning) for kvitteringer fungerer ikke på grunn av et problem med URL-adressen til OCR-tjenesten for utgifter. |
| Reise og utgift | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Når funksjonen **Evne til å spesifisere regelmessige utgifter** er aktivert, endres beløpene på spesifiserte linjer i reiseregninger hver gang **Spesifiser**-siden åpnes. |
| Reise og utgift | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Du kan ikke slette en reiseregning når den midlertidige listen har flere godkjennere. |

## <a name="removed-and-deprecated-features"></a>Funksjoner som er fjernet og avskrevet

Emnet [Fjernede eller avskrevne funksjoner i Project Operations](removed-depreciated-features-project.md) beskriver funksjoner som er fjernet eller avskrevet for Dynamics 365 Project Operations.

- En fjernet funksjon er ikke lenger tilgjengelig i produktet.
- En avskrevet funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

En kunngjøring om avskrivning vil vises i emnet [Fjernede eller avskrevne funksjoner i Project Operations](removed-depreciated-features-project.md) 12 måneder før en funksjon blir fjernet fra produktet.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Disse endringene er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.
