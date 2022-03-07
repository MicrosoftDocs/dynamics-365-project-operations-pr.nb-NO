---
title: Nyheter eller endringer i Project Operations, juli 2021 for lagerførte/produksjonsbaserte scenarioer
description: Denne emne inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i juli 2021-versjonen av Project Operations for lagerførte/produksjonsbaserte scenarioer.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: fb1814330b5e474ccbda0ab85dd67758a6f270a9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334579"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Nyheter eller endringer i Project Operations, juli 2021 for lagerførte/produksjonsbaserte scenarioer

_**Gjelder:** Project Operations for lagerførte/produksjonsbaserte scenarioer_

Dette emnet gjelder for følgende Dynamics 365 Project Operations-komponenter og versjoner:

- Prosjektstyring og regnskap i Dynamics 365 Finance-miljø versjon 10.0.20
 
### <a name="quality-updates"></a>Kvalitetsoppdateringer
                                                                                                                                                                                  
| Funksjonsområdet                      | Referansenummer| Kvalitetsoppdatering                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prosjektstyring og regnskap | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Oppføringer for kostnadsinnsats fra kjøpsrekvisisjon tømmes så snart bestillingen er frigitt fra kjøpsrekvisisjonsproblemet.                                                                           |
| Prosjektstyring og regnskap | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Budsjettvalideringen utføres to ganger i kjøpsrekvisisjon. Denne dupliseringen betyr at innløsningen ikke kan lukkes, og den tilsvarende bestillingen blir ikke opprettet.                                                                                                                        |
| Prosjektstyring og regnskap | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Faktureringsregelen **Prosent som skal faktureres** kan ikke fullføres på grunn av et avrundingsproblem.                                                                              |
| Prosjektstyring og regnskap | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Når du justerer transaksjonen og prosentandelen har desimaler, justeres ikke kostnaden og salgsprisen på riktig måte.                                      |
| Prosjektstyring og regnskap | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Regnskapskildeutforskeren viser timer for én enkelt timelistelinje for flere timelistelinjer med forskjellige aktiviteter.                                      |
| Prosjektstyring og regnskap | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Tilpasning av lagrede visninger og timelistelinjedetaljer fører til at systemet alltid åpner detaljene for den første timelisten i listen under forsøk på å åpne en timeliste.  |
| Prosjektstyring og regnskap | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Prosjektrotnoden forsvinner, og oppføringer for arbeidsnedbrytningsstruktur slettes etter import.                                                                                             |
| Prosjektstyring og regnskap | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Når varer mottas og utstedes delvis fra varekravet, oppdaterer systemet feil budsjettforbrukssaldo. |
| Prosjektstyring og regnskap | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Bestillinger for prosjekthonorar viser ikke totalsummer riktig i **Totaler**-ruten eller rutenettet for **Ventende faktura**.                                                                  |
| Prosjektstyring og regnskap | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Når lagerbeholdningen lukkes, posteres kostnadsjusteringer for prosjektvaren til saldokontoen i stedet for resultatkontoen.                                                            |
| Prosjektstyring og regnskap | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Et prosjekt som er lagt inn for transaksjoner og et estimatbilag bruker USD som regnskapsvaluta, men beløpet viser hva CAD-ekvivalenten vil være.              |
| Prosjektstyring og regnskap | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Iverksatte kostnader med et varekrav og en bestilling er feil i bestillingsfakturaprosessen med produktkvittering og delfakturering.       |
| Prosjektstyring og regnskap | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Prosjektjustering oppdaterer ikke salgsbeløpet riktig med indirekte kostnader.                                                                                    |
| Prosjektstyring og regnskap | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Tabellen **Timeliste** mangler en definert relasjon med visningen **Arbeider/ressurs**.                                                                                   |
| Prosjektstyring og regnskap | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Kan ikke fylle ut **Aktivitetsnummer**-feltet når du velger det fra rullegardinlisten for en konsernintern timeliste.                                                                 |
| Prosjektstyring og regnskap | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Du kan ikke legge til et tilpasset felt for **Formål** eller **Aktivitetsbeskrivelse** på følgende sider: **Prosjektpostert transaksjon**, **Oppretting fakturaforslag** eller **Fakturaforslag**.  |
| Prosjektstyring og regnskap | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Feil kontroll for leveringsdato angis når du oppretter varekrav ved hjelp av databehandling (**ProjSalesItemRequirementEntity**).                                              |
| Prosjektstyring og regnskap | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Når du velger en prosjektkontrakt-ID i Økonomi, åpner det Project Operations-integrerte miljøet siden for å opprette en ny oppføring i stedet for å åpne den eksisterende prosjektkontrakten.                                                                                                                 |
| Prosjektstyring og regnskap | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Etiketten @SYS4083080 (Finner ikke en unik arbeideroppføring som samsvarer med de angitte verdiene) oversettes ikke til dansk.                                |
| Prosjektstyring og regnskap | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Feltet **Mva-gruppe for vare** kan ikke redigeres i et fakturaforslag.                                                                               |
| Prosjektstyring og regnskap | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Igangsatt kostnad overdrives med ikke-fradragsberettigede avgiftsbeløp.                                                                                                    |
| Prosjektstyring og regnskap | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Når du legger inn en konsernintern timeliste med flere prosjekter og ulike finansdimensjoner, genereres uventede verdier i hovedboken.                             |
| Prosjektstyring og regnskap | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Fakturaforslagslinjer dupliseres på grunn av flere forekomster av den periodiske prosessen, **Import fra oppsamling** kjører samtidig.                                      |
| Prosjektstyring og regnskap | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Det er en feil i postering av fakturaforslaget for kreditnotaen, så transaksjonene på bilaget balanseres ikke.    |
| Prosjektstyring og regnskap | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Igangsatte prosjektkostnader blir feil etter at ventende fakturaer på vent er frigitt.                                                                             |
| Prosjektstyring og regnskap | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Du kan ikke opprette et notat for en prosjektsalgsordre når avgiften er i en annen valuta enn firmavalutaen.                                      |
| Prosjektstyring og regnskap | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Sletting av en kontrakt sletter også adressen som er tilknyttet kunden.                                                                                     |
| Prosjektstyring og regnskap | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Et fakturaforslag som er et resultat av en negativ tidstransaksjonskorrigering, kan ikke posteres.                                                                    |
| Reise og utgift                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Avgifter beregnes på forskjellig måte i utgiftsrapporter.                                                                                                                  |
| Reise og utgift                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Utgivelsesoppdatering **DB72_Expense.updateTrvExpTransProjTransId()** tillater ikke at **trvExpTrans.ReferenceDataAreaId** oppretter den nye nummersekvensen.                    |
| Reise og utgift                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Det angitte beløpet vises ikke med det obligatoriske feltet.                                                                                                             |
| Reise og utgift                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Forbedringer i ytelsen ved å legge ved en utgift i utgiftsrapporten ved hjelp av brukergrensesnittet Nyskapte utgiftsrapporter.                                                            |
| Reise og utgift                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Du kan slette posterte utgiftsrapporter.                                                                                           |
| Reise og utgift                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Utgiftspolicymeldingen vises flere ganger.                                                                                                       |
| Reise og utgift                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Feltet **Betalingsmåte** er inkludert i ruten **Ny utgift**.                                                                                                      |
| Reise og utgift                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Verktøyet **Tilbakestill utgiftsdokumentstatus** skal tilbakestille statusen for utgiftsrapporten til **Utkast** hvis arbeidsflyten ikke ble funnet. 

### <a name="regulatory-updates"></a>Forskriftsmessige oppdateringer
Hvis du vil ha informasjon om forskriftsmessige oppdateringer for Finance and Operations-apper, kan du se [Forskriftsmessige oppdateringer](/dynamics365/finance/localizations/regulatory-updates). Du kan også logge på Lifecycle Services (LCS) og vise de planlagte forskriftsoppdateringene ved hjelp av verktøyet Problemsøk. Problemsøk lar deg søke etter land, type funksjon og utgave.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
