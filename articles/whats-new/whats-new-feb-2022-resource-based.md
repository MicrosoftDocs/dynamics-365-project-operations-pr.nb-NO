---
title: Nyheter februar 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra februar 2022.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932998"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter februar 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

*Gjelder: Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer*

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.28.0.120
- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.24

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

- I denne versjonen kan du legge til opptil 300 teammedlemmer i ett enkelt prosjekt. Tidligere var grensen for antall teammedlemmer 150. For mer informasjon, se [Prosjektgrenser](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Tilordningsoppdateringer av dobbel skriving for Project Operations

Listen nedenfor viser tilordningene for dobbel skriving som er endret eller lagt til i februar 2022-versjonen av Project Operations.

| Enhetstilordning | Oppdatert versjon | Kommentarer |
| --- | --- | --- |
| Eksportenhet for prosjektutgifter for Project Operations-integrering (msdyn\_expenses) | 1.0.0.3 | Utvidet for synkronisering av prosjektaktivitet til Dataverse. |

Hvis du vil se gjeldende liste og versjoner av tilordninger med dobbel skriving i Project Operations, kan du se [Tilordningsversjoner av dobbel skriving for Project Operations](../environment/resource-dual-write-maps.md).

Kjør alltid den nyeste versjonen av tilordningen i miljøet, og aktiver alle relaterte tabelltilordninger når du oppdaterer versjonen av Project Operations Dataverse-løsningen og Finance-løsningen. Enkelte funksjoner fungerer kanskje ikke riktig hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en bruksklar tabelltilordning, bruker du endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem når du starter tilordningen, følger du instruksjonene i delen [Problemer med manglende tabellkolonner i tilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Fakturering og prising | 2415109 | Standardverdien i feltet **Betalingsbetingelser for operasjoner** må være kundeoppføringen for prosjektkontrakten og oppføringen for proformafaktura. |
| Fakturering og prising | 2497369 | Materialkorrigering må følge datoverdien i **Korreksjon**-parameterne. |
| Fakturering og prising | 2498697 | Forbedret sikkerhetskonfigurasjonen for **Tilbakekalling av tidsoppføring**. |
| Fakturering og prising | 2513824 | For ressursbaserte scenarioer må ikke transaksjonskategori-ID-en overskride 28 tegn i Project Operations. |
| Fakturering og prising | 2517455 | Handlingen **Oppdater fakturalinjetransaksjoner** må ikke tillates å bli utløst flere samtidige ganger for samme faktura. |
| Fakturering og prising | 2517465 | Handlingen **Deaktiver fakturalinjedetaljer** er blokkert fordi den ikke støttes. |
| Fakturering og prising | 2556660 | Løste datoeffektivitetskontrollen som utføres i prislisten som er knyttet til en oppføring for prosjektparametere. |
|   Administrasjon av salgsmuligheter | 2369202 | Korrigerte forretningslogikken som kontrollerer at prislister som har overlappende virkningsdatoer, kan knyttes til samme prosjektkontrakt. |
|   Administrasjon av salgsmuligheter | 2385965 | Korrigerte funksjonaliteten på **Kunder**-fanen på **Prosjektkontrakt**-siden når du velger **Lagre og lukk**. |
| Tid og utgifter | 2538503 | En prosjektoppgave må være tilgjengelig i enheten **Faktiske verdier for prosjekt** etter at en utgiftsrapport er postert. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Prosjektstyring og regnskap | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Under import av leverandørkreditnotaer oppstår det en feil. Feilmeldingen er: "Tilbakeholdt beløp kan ikke være større enn resterende nettobeløp." |
| Prosjektstyring og regnskap | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Hvis et fakturaforslag inkluderer transaksjoner med avgifter med null i beløp som er ufakturerte faktiske salg, kan det ikke utføres fakturering. |
| Prosjektstyring og regnskap | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Den posterte kostnaden stemmer ikke etter at innkjøpsprisen er oppdatert og **Aktiver endringsadministrasjon** er aktivert.|
| Prosjektstyring og regnskap | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Posteringsestimatet for et prosjekt med fast pris bruker feil valuta og beløp i estimatbilaget, selv når funksjonen **Aktiver estimatberegning for prosjektkontraktvaluta** er aktivert. |
| Prosjektstyring og regnskap | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** skal ikke utføre et kall for å aktivere endringssporing uten å fange opp unntak for enheter som har konfigurasjonsnøkler som ikke er aktivert. |
| Prosjektstyring og regnskap | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Den satsvise jobben er løst når flere avanserte kladder posteres og det oppstår en feil. |
| Reise og utgift | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | På grunn av et problem med oppgjør som er relatert til forskudd i reiseregninger, dekkes ikke avgiftsbeløpet som en del av forskuddet. |
| Reise og utgift | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Informasjon om merverdiavgift er ikke inkludert i rapporten **Ugift – Postert transaksjoner**. |
| Reise og utgift | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Brudd utgiftspolicyen **Kvitteringer påkrevd** viser en feilaktig advarsel på utgiftsrapporter. |
| Reise og utgift | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | En prosjekttransaksjon inkluderer ikke merverdiavgift som ikke er fradragsberettiget, i det totale salgsbeløpet når transaksjonen er et resultat av en kjørelengdeutgift. |
| Reise og utgift | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Når en spesifisert linje har avgifter, kan du ikke endre datoen for den spesifiserte linjen, og det oppstår en tilstandsfeil i kildedokumentet. |

## <a name="removed-and-deprecated-features"></a>Funksjoner som er fjernet og avskrevet

Artikkelen [Fjernede eller avskrevne funksjoner i Project Operations](removed-depreciated-features-project.md) beskriver funksjoner som er fjernet eller avskrevet for Dynamics 365 Project Operations.

- En fjernet funksjon er ikke lenger tilgjengelig i produktet.
- En avskrevet funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

En kunngjøring om avskrivning vil vises i artikkelen [Fjernede eller avskrevne funksjoner i Project Operations](removed-depreciated-features-project.md) 12 måneder før en funksjon blir fjernet fra produktet.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Disse endringene er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.
