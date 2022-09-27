---
title: Administrasjon av underkontrakt i Project Operations
description: Denne artikkelen gir en oversikt over hele prosessen med administrasjon av underkontrakter som vanligvis utføres i prosjektbaserte organisasjoner.
author: rumant
ms.date: 09/14/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b2e4518f77b2099f9818ea56623be9efb20b01f4
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522338"
---
# <a name="subcontract-management-in-project-operations"></a>Administrasjon av underkontrakt i Project Operations


_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen gir en oversikt over hele prosessen med administrasjon av underkontrakter i prosjektbaserte organisasjoner. Underkontrakter for tjenester følger vanligvis fremgangsmåten forretningsprosessflyt som vises i diagrammet nedenfor.

![Prosessflyt for underkontrakt](../media/SubcontractingProcessFlow.png)

Følgende liste viser en trinnvis beskrivelse av underkontraktprosessen.

1. Prosjektlederen oppretter en underkontrakt med en leverandør. Som standard brukes prislistene som er knyttet til leverandøroppføringen, for underkontrakten. Leverandørkontoen har relasjonstypen **Leverandør** eller **Forsyner**.
2. Prosjektlederen kan angi alle innkjøpene som linjeelementer på underkontrakten. Underkontraktlinjer kan være for klokkeslett, utgifter eller produkter. Transaksjonsklassen for underkontraktlinjen avgjør hva linjen gjelder.
3. Kontolederen for leverandøren og prosjektlederen kan gå over underkontrakten. Priser kan justeres i kjøpsprislister som er tilknyttet underkontrakten.
4. Hvis underkontraktlinjen gjelder et tidsskjema, knytter leverandørkontolederen leverandørkontakter til hver underkontraktlinje. Denne tilknytningen inneholder informasjon til prosjektlederen som arbeider med underkontrakten. Når en leverandørkontakt tilknyttes en underleverandørlinje, oppretter systemet automatisk en ressurs som kan reserveres fra kontakten, hvis en ressurs som kan reserveres, ikke allerede finnes.
5. Faktureringsmetoden for hver underkontraktlinje kan være **Fast pris** eller **Tid og materiell**. For underkontraktlinjer med fast pris angis en milepælbasert fakturaplan.
6.  Når underkontrakten er konfigurert og forhandlingen er fullført, bekreftes den. Bekreftede underkontrakter kan ikke redigeres, men hvis det skjer endringer, kan en underkontrakt bli åpnet på nytt for redigeringer, noe som angir statusen fra **Bekreftet** tilbake til **Utkast**, og forhandlinger kan åpnes på nytt. 
7.  Når du oppretter et generisk teammedlem på et prosjekt, kan teammedlemmet tilknyttes en underkontraktlinje. Dette angir behovet for å bemanne det generiske teammedlemmet med underkontraktkapasitet.
8.  Navngitte teammedlemmer kan enten opprettes direkte på et prosjekt eller opprettes ved å reservere dem ved hjelp av funksjonene for ressursplanlegging. Hvis et navngitt prosjektteammedlem er en kontraktarbeider, er det mulig å knytte dette til en underkontraktlinje. Dermed trekkes den tilgjengelige kapasiteten ned på en underkontraktlinje.
9.  Underkontraktressurser kan logge tid, utgifter og materialbruk på prosjekter og prosjektoppgaver, og deretter sende til godkjenning. Dette er likt for ansatte. Når tiden registreres, kan en kontraktarbeider velge en bestemt underkontrakt- og underkontraktlinje.
10. Når godkjenningen er godkjent av underkontraktene, registreres faktiske prosjektkostnader basert på innkjøpsprisen til kontraktarbeideren eller rollen de utførte på prosjektet.
11. Leverandørfakturaer og leverandørfakturalinjeelementer kan registreres i systemet for arbeidet som utføres av leverandørressurser eller produkter som leveres av leverandøren. Leverandørfakturalinjer må være spesifikke for et prosjekt og for en transaksjonsklasse med tid, utgifter, produkt/materiell, milepæl eller avgift. Alternativt kan leverandørfakturalinjer referere til en underkontraktlinje.
12. Systemet knytter automatisk alle faktiske kostnader som samsvarer med underkontraktlinjen og prosjektet, til leverandørfakturaen. Dette vil muliggjøre en treveis samsvars- og verifiseringsprosess.
13. Deretter kan prosjektlederen gå gjennom de faktiske prosjektene automatisk, fjerne eller legge til faktiske prosjektkostnader og fullføre verifiseringsprosessen.
14. Når verifiseringsprosessen er fullført på alle linjer, merkes leverandørfakturaen som **Klar for betaling**. På dette trinnet kan leverandørfakturaen og -linjene overføres til et regnskaps- eller leverandørsystem for å behandle betalingen til leverandøren. Tidligere registrerte prosjektkostnader blir reversert, og faktiske kostnader fra leverandørfakturalinjen registreres på prosjektet.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Antallsbaserte og arbeidsbaserte underkontraktlinjer

En underkontraktlinje kan være antallsbasert eller arbeidsbasert. 

Når en underkontraktlinje er **antallsbasert**, kan antallet som kjøpes på underkontraktlinjen for tid, utgifter eller materiell, brukes på et hvilket som helst prosjekt.

Når en underkontraktlinje er **arbeidsbasert**, tilordnes underkontraktlinjen til en enhet av arbeid representert av en node i prosjektplanen. Verdien til underkontraktlinjen er summen av alle komponentene som kreves for å levere denne arbeidsenheten. Disse er modellert som underkontraktlinjedetaljer og kan være en samling av tid, utgifter eller materiell. For en arbeidsbasert underkontraktlinje er underkontraktlinjen også dedikert til ett enkelt prosjekt. Disse typene underkontrakter støttes ikke av Project Operations.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

