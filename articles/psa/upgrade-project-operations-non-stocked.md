---
title: Oppgradere fra Project Service Automation til Project Operations
description: Denne artikkelen gir en oversikt over prosessen med å oppgradere fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 43ea29aeafb62f3ecd69b316f2c0a5b791707da5
ms.sourcegitcommit: bc21fbe8547534d2644269f873eb05d509840f23
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446048"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Oppgradere fra Project Service Automation til Project Operations

Det er en glede å kunngjøre den første av tre faser for oppgradering fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Project Operations. Denne artikkelen gir en oversikt over kunder som begir seg ut på denne spennende reisen. Fremtidige artikler inkluderer vurderinger fra utviklere og detaljer om funksjonsforbedringer. De gir ikke bare veiledning for å hjelpe deg med å klargjøre for oppgradering til Project Operations, men forklarer også hva du kan forvente etter at du har oppgradert.

Leveringsprogrammet for oppgraderingen deles opp i de tre fasene.

| Oppgraderingslevering | Fase 1 (januar 2022) | Fase 2 (november 2022) | Fase 3 (april bølge 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Ingen avhengighet av arbeidsnedbrytningsstrukturen (WBS) for prosjekter | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS innenfor gjeldende støttede grenser for Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| WBS utenfor gjeldende støttede grenser for Project Operations, inkludert støtte for Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funksjoner for oppgraderingsprosess 

Som en del av oppgraderingsprosessen har vi lagt til oppgraderingslogger i områdekartet, slik at administratorer lettere kan diagnostisere feil. I tillegg til det nye grensesnittet blir nye valideringsregler lagt til for å sikre dataintegritet etter en oppgradering. Valideringene nedenfor blir lagt til i oppgraderingsprosessen.

| Valideringer | Fase 1 (januar 2022) | Fase 2 (november 2022) | Fase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS valideres mot vanlige dataintegritetsbrudd (for eksempel ressurstilordninger som er tilknyttet den samme overordnede oppgaven, men som har forskjellige overordnede prosjekter). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS valideres mot de [kjente grensene for Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS valideres mot de kjente grensene for Project Desktop Client. | |  | :heavy_check_mark: |
| Ressurser og prosjektkalendere som kan reserveres, evalueres mot vanlige inkompatible unntak fra kalenderregler. | | :heavy_check_mark: | :heavy_check_mark: |

I fase 2 vil kunder som oppgraderer til Project Operations, oppgradere sine eksisterende prosjekter til en skrivebeskyttet opplevelse av prosjektplanlegging. I denne skrivebeskyttede opplevelsen vil hele WBS-en være synlig i sporingsrutenettet. Hvis du vil redigere WBS, kan prosjektledere velge **Konverter** på hovedsiden for **Prosjekter**. En bakgrunnsprosess oppdaterer deretter prosjektet, slik at det støtter den nye prosjektplanleggingsopplevelsen fra Project for the Web. Denne fasen passer for kunder som har prosjekter som passer innenfor de [kjente grensene for Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

I fase 3 legges det til støtte for Project Desktop Client, til fordel for kunder som vil fortsette å redigere prosjektene sine fra det programmet. Hvis eksisterende prosjekter imidlertid konverteres til Project for the Web-opplevelsen, blir tilgang til tillegget deaktivert for hvert konverterte prosjekt.

## <a name="prerequisites"></a>Krav

En kunde må oppfylle følgende vilkår for å kvalifisere for oppgraderingen av fase 1:

- Målmiljøet kan ikke inneholde oppføringer i **msdyn_projecttask**-enheten.
- Gyldige Project Operations-lisenser må være tilordnet alle kundens aktive brukere. 
- Kunden må validere oppgraderingsprosessen i minst ett ikke-produksjonsmiljø som har en representativt datasett som er på linje med produksjonsdata.
- Målmiljøet må oppdateres til Project Service Automation oppdateringsutgivelse 41 (3.10.62.162) eller senere.

Forhåndskrav for fase 2 og fase 3 oppdateres etter hvert som datoene for generell tilgjengelighet nærmer seg.

## <a name="licensing"></a>Lisensiering

Hvis du har aktive lisenser for Project Service Automation, kan du installere og bruke Project Operations, som omfatter alle funksjonene i Project Service Automation og så videre. På denne måten kan du teste funksjonene i Project Operations mens du fortsetter å bruke Project Service Automation i produksjon. Når lisensene for Project Service Automation utløper, må du gå over til Project Operations. Når du planlegger denne overføringen, må du ta hensyn til det faktum at Project Operations-lisensen ikke inneholder en Project Service Automation-lisens.

## <a name="testing-and-refactoring-customizations"></a>Teste og refaktorere tilpassinger

Som et startpunkt importerer du alle tilpassinger til et ryddig Project Operations-miljø (Lite) for å bekrefte at importen er vellykket, og at forretningsoperasjoner fungerer som forventet.

Her er noen ting du kan se etter:

- Importen kan mislykkes på grunn av manglende avhengigheter. Med andre ord referansefeltene for tilpassinger eller andre komponenter som er fjernet i Project Operations. I dette tilfellet fjerner du avhengighetene fra utviklingsmiljøet.
- Hvis den uadministrerte og administrerte løsningen inneholder komponenter som ikke er tilpasset, fjerner du komponentene fra løsningen. Når du for eksempel tilpasser **Prosjekt**-enheten, legger du bare til enhetsoverskriften i løsningen. Ikke legg til alle feltene. Hvis du tidligere har lagt til alle underkomponenter, må du kanskje opprette en ny løsning manuelt og legge til relevante komponenter i den.
- Skjemaer og visninger vises kanskje ikke som forventet. Hvis du i noen tilfeller har tilpasset noen av standardskjemaene eller -visningene, kan det hende at tilpassingene hindrer at nye oppdateringer i Project Operations trer i kraft. For å identifisere disse problemene anbefaler vi at du gjennomgår en side-ved-side-gjennomgang av en ren installasjon av Project Operations og en installasjon av Project Operations som omfatter tilpassingene dine. Sammenlign de skjemaene som brukes mest i firmaet, for å bekrefte at versjonen av skjemaet fortsatt er fornuftig, og at det ikke mangler noe i den rene versjonen av skjemaet. Gjør det samme for side-ved-side-gjennomganene for alle visninger du har tilpasset.
- Forretningslogikk kan mislykkes ved kjøretid. Siden referanser til felt i programtilleggene ikke valideres under importen, kan det hende forretningslogikken mislykkes på grunn av referanser til felt som ikke lenger finnes, og du kan få en feilmelding som ligner på følgende eksempel: "Prosjekt"-enhet inneholder ikke attributt med Navn = 'msdyn_plannedhours' og NameMapping = 'Logical'. I dette tilfellet endrer du tilpassingene slik at de bruker de nye feltene. Hvis du bruker automatisk genererte proxy-klasser og sterke typereferanser i programtilleggslogikken, bør du vurdere å generere proxyene på nytt fra en ren installasjon. På denne måten kan du enkelt identifisere alle stedene der programtilleggene er avhengige av avskrevne felt.

Når du har oppdatert tilpassingene slik at de importerer Project Operations på en ren måte, går du videre til de neste trinnene.

## <a name="end-to-end-testing-in-development-environments"></a>Ende-til-ende-testing i utviklingsmiljøer

### <a name="initiate-upgrade"></a>Start oppgradering 

1. I Power Platform-administrasjonssenteret finner og velger du miljøet. Deretter, i applikasjonene, finner og velger du **Dynamics 365 Project Operations**.
2. Velg **Installer** for å starte oppgraderingen. Power Platform-administrasjonssenteret presenterer denne installasjonen som en ny installasjon. Tilstedeværelsen av en tidligere versjon av Project Service Automation registreres imidlertid, og den eksisterende installasjonen blir oppgradert.

    Når oppgraderingen er fullført, skal miljøet vise at Project Operations er installert, og at Project Service Automation ikke er installert.

    > [!NOTE]
    > Oppgraderingen kan ta flere timer, avhengig av datamengden i miljøet. Kjerneteamet som administrerer oppgraderingen, bør planlegge og kjøre oppgraderingen i fritiden. I noen tilfeller bør oppgraderingen kjøres i løpet av helgen hvis datavolumet er stort. Beslutningen om planlegging bør baseres på testresultatene i lavere miljøer.

3. Oppgrader tilpassede løsninger etter behov. Nå distribuerer du eventuelle endringer du har gjort i tilpassingene, i delen [Teste og refaktorere tilpassinger](#testing-and-refactoring-customizations) i denne artikkelen.
4. Gå til **Innstillinger** \> **Løsninger**, og velg å avinstallere løsningen for **Avskrevne Project Operations-komponenter**.

    Denne løsningen er en midlertidig løsning som inneholder den eksisterende datamodellen og komponentene som finnes under oppgraderingen. Ved å fjerne denne løsningen fjerner du alle feltene og komponentene som ikke lenger brukes. På denne måten bidrar du til å forenkle grensesnittet og gjøre integrasjon og utvidelse enklere.
    
### <a name="validate-common-scenarios"></a>Valider vanlige scenarioer

Når du validerer de spesifikke tilpassingene, anbefaler vi at du også ser gjennom forretningsprosessene som støttes på tvers av programmene. Disse forretningsprosessene omfatter, men er ikke begrenset til, oppretting av salgsenheter, for eksempel tilbud og kontrakter, og oppretting av prosjekter som inkluderer WBS-er og godkjenning av faktiske data.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Store endringer mellom Project Service Automation og Project Operations

Denne delen gir et sammendrag av de store endringene du kan forvente mellom Project Service Automation og Project Operations.

### <a name="project-planning"></a>Prosjektplanlegging

Prosjektplanleggingsfunksjonene i Project Operations er ikke lenger avhengig av en kombinasjon av logikk på klientsiden og logikken på serversiden. I stedet bruker Project Operations Project for the Web som planleggingsmotor. Denne endringen i planleggingsfunksjonene gir mulighet til flere nye funksjoner, for eksempel tavle- og Gantt-visninger, ressursdrevet planlegging [elementer i oppgavesjekklisten](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) og prosjektplanleggingsmoduser. De nye planleggingsfunksjonene støttes også av et rikt sett med nye [programmeringsgrensesnitt (API-er)](../project-management/schedule-api-preview.md). Disse API-ene er ment å bidra til å sikre at ingen programmatisk operasjon for oppretting, oppdatering eller sletting av en enhet i WBS-en ødelegger de beregnede feltene i tidsplanen.

## <a name="billing-and-pricing"></a>Fakturering og prising

Som en del av fortsatte investeringer i Project Operations er flere nye funksjoner tilgjengelige i fakturering og prissetting. Her er noen eksempler:

- [Registrering av materialbruk på prosjekter og prosjektoppgaver](../material/material-usage-log.md)
- [Administrasjon av underkontrakt](../pro/subcontracting/managing-subcontracts-overview.md)
- [Forskudd og honorarbaserte kontrakter](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Må ikke overskrides-status og valideringer for kontrakt](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Oppgavebasert fakturering

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Hvilke distribusjonstyper støttes for øyeblikket for oppgradering?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite-distribusjon                        | Støttes               |
| Prosjektstyring og regnskap i Dynamics 365 Finance | Project Operations Lite-distribusjon                        | Støttes ikke for øyeblikket |
| Prosjektstyring og regnskap for Finance              | Project Operations for ressursbaserte/ikke-lagerførte scenarioer     | Støttes ikke for øyeblikket |
| Project Service Automation 3.x                         | Project Operations for ressursbaserte/ikke-lagerførte scenarioer     | Støttes ikke for øyeblikket |
| Project for the Web (dedikert miljø)            | Project Operations Lite-distribusjon                        | Støttes ikke for øyeblikket |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Hvordan installerer jeg Project Operations før oppgraderingsverktøyene er tilgjengelige?

Det er to alternativer for installasjon av Project Operations før oppgraderingsverktøyene er tilgjengelige:

- Klargjøre et nytt miljø.
- Distribuere Project Operations separat i alle salgsorganisasjoner der Project Service Automation ikke finnes.

> [!NOTE]
> Hvis Project Service Automation er installert i en organisasjon, men den ikke ble brukt, kan den avinstalleres. Når du har fjernet Project Service Automation fullstendig, kan Project Operations installeres i samme organisasjon.
