---
title: Sporing av prosjektsalg
description: Denne artikkelen inneholder informasjon om hvordan Project Operations sporer fremdriften mot arbeidsinntekt på et prosjekt.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ce61acf95ee5e9ac10047406c9d4a5c9b1f92aad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911286"
---
# <a name="project-sales-tracking"></a>Sporing av prosjektsalg

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations sporer arbeidsestimater og inntekt til lavest mulig detaljstyring i en prosjektplan. Estimatet for arbeidsinntekt er basert på planlagt innsats og de generiske eller navngitte ressursene som er tilordnet hver bladnodeoppgave i prosjektplanen. Når prosjektet starter og personene begynner å rapportere tid på ulike prosjektoppgaver, oppsummeres den faktiske inntekten på arbeid som starter en beregning av prognosene.

## <a name="labor-revenue-tracking-view"></a>Visningen Omsetningssporing av arbeid

På **Prosjekter**-siden, på **Sporing**-fanen, kan du velge **Sporing** > **Kostnad** for å åpne visningen **Kostnadssporing**. Du kan også velge **Bruk** > **Fakturasats** for å åpne visningen **Inntektssporing**, som viser fremdriften til arbeidsinntekt for hver oppgave i prosjektplanen. Denne visningen sammenligner også den faktiske arbeidsinntekten som er brukt på en aktivitet, med aktivitetens planlagte arbeidsinntekt. Project Operations bruker følgende formler til å beregne måledata for arbeidsinntekt:

- **Planlagt omsetning**: Estimert salgsverdi for alle ressurstilordninger for hver oppgave i bladnode
- **Faktisk omsetning**: Summen av alle ufakturerte faktiske salgsverdier for tid som er registrert for oppgaven
- **Fakturerbar omsetning i %**: Faktisk inntekt ÷ Omsetningsestimat ved fullføring
- **Gjenværende omsetning**: Omsetningsestimat ved fullføring – Faktisk omsetning
- **Estimert omsetning ved fullføring**: Gjenværende omsetning + Faktisk omsetning
- **Omsetningsavvik**: Planlagt omsetning – Estimert omsetning ved fullføring


> [!NOTE]
> Project Operations viser bare arbeidsomsetning på **Prosjekt**-siden på **Sporing**-fanen. Materialer og utgifter kan estimeres og spores for forbruk, men denne omsetningen er ikke inkludert i omsetningen som vises på **Sporing**-fanen. Denne fanen er utformet for bare å fungere for ny projisering av arbeidsomsetning ved å projisere innsats på nytt.  
> Alle omsetningsbeløp som vises, konverteres til kostnadsvalutaen for prosjektet. Kostnadsvalutaen for prosjektet er valutaen til kontraktsenheten i prosjektet. For prosjekter med fast pris er omsetningstall i visningen **Omsetningssporing av arbeid** ikke relevante, fordi ufakturerte faktiske salgsverdier ikke registreres ved godkjenningen av tid.
> De estimerte salgsverdiene for tid som vises på **Estimat**-fanen i prosjektet, utgjør kanskje ikke den planlagte omsetningsverdien på **Sporing**-fanen. Kilden til dette avviket skyldes to mulige årsaker:
><ol>
   ><li> <b>Estimater</b>-fanen viser estimert omsetning i salgsvalutaen, mens <b>Sporing</b>-fanen viser planlagt omsetningn konvertert til kostnadsvalutaen. </li>
   ><li> Når estimert salg konverteres til kontraktvalutaen som vist på <b>Estimater</b>-fanen, til prosjektvalutaen, innebærer konverteringen trinn som kan føre til tap av nøyaktighet: </li>
><ol>
><li> Det beregnede salgsbeløpet i kontraktssvalutaen konverteres først til basisvalutaen (konvertering 1).</li>
><li> Det beregnede salgsbeløpet i basisvalutaen konverteres til prosjektkostnadsvalutaen (konvertering 2). </li>
></ol>
></ol>
> Valutapresisjon brukes i begge trinnene, noe som fører til et avvik i planlagt omsetning i prosjektvalutaen fra planlagt salg i kontraktvalutaen.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Projisere omsetning på nytt for bladnodeoppgaver

Arbeidsomsetning i en bladnodeoppgave kan ikke løses på nytt direkte i kategorien **Sporing** på **Prosjekt**-siden. Du kan imidlertid bruke visningen **Innsatssporing** til å utføre gjenstående innsats på en oppgave på nytt. Dette fører til en omberegning av den gjenstående omsetningen for aktiviteten. Nedenfor finner du en beskrivelse av hvordan dette fungerer.

1. En prosjektleder kan projisere innsats på oppgaver på nytt ved å oppdatere standardverdien i **Gjenstående innsats**-feltet med et nytt overslag over gjenstående innsats for aktiviteten. Ny projisering fører til en omberegning av oppgavens innsatsestimat ved fullføring, fremdriftsprosenten og det beregnede innsatsavviket for en oppgave. EAC, estimatet for fullføring (ETC) og fremdriftsprosenten på aktivitetssammendragene beregnes også på nytt, og det lages en ny projisering av innsatsavvik.
2. Basert på den nye verdien for gjenstående innsats på oppgaven beregner systemet den gjenstående omsetningen i visningen **Omsetningssporing**. For å beregne gjenstående omsetning basert på resterende innsats beregner systemet først den gjennomsnittlige omsetning for en times innsats på oppgaven som planlagt omsetning eller planlagt innsats. Den planlagte omsetningen er summen av omsetningen for alle ressurstilordninger for aktiviteten. Gjennomsnittlig omsetning per time brukes til å beregne gjenstående omsetning for den nylig beregnede gjenstående innsatsen for aktiviteten.
3. Den estimerte omsetningen ved fullføring og omsetningsinntaksprosenten for bladnodeoppgaven beregnes på nytt.
4. Omsetning ved fullføring for sammendragsoppgavene helt til rotnoden beregnes på nytt.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Projisere omsetning på nytt for sammendragsoppgaver

Du kan projisere arbeidsomsetning på nytt for sammendragsoppgaver eller beholderoppgaver. Du kan imidlertid ikke løse arbeidsomsetning direkte på nytt for en prosjektsammendragsoppgave i kategorien **Sporing** på **Prosjekt**-siden. På samme måte som med oppgaver med bladnoder kan du utføre sammendrags- og beholderoppgaver på nytt ved hjelp av visningen **Innsatssporing**. I denne visningen kan du projisere gjenstående innsats på nytt for en sammendragsoppgave, noe som fører til en omberegning av den gjenstående omsetningen for sammendragsoppgaven. Nedenfor finner du en beskrivelse av hvordan dette fungerer.

1. En prosjektleder kan projisere innsats på oppgaver på nytt ved å oppdatere standardverdien i **Gjenstående innsats**-feltet med et nytt overslag over **gjenstående innsats** for aktiviteten. Ny projisering fører til en omberegning av oppgavens estimat ved fullføring, fremdriftsprosenten og det beregnede innsatsavviket for en oppgave. EAC, ETC- og fremdriftsprosenten på aktivitetssammendragene beregnes også på nytt, og det lages en ny projisering av innsatsavvik.
2. Basert på den nye verdien i feltet **Gjenstående innsats** på oppgaven beregner systemet den gjenstående omsetningen i visningen **Omsetningssporing**. For å beregne gjenstående omsetning basert på resterende innsats beregner systemet først den gjennomsnittlige omsetning for en times innsats på oppgaven som planlagt omsetning eller planlagt innsats. Den planlagte omsetningen er summen av omsetningen for alle ressurstilordninger for aktiviteten. Denne gjennomsnittlige omsetningen per time brukes deretter til å beregne omsetningen for den nylig beregnede gjenstående innsatsen for aktiviteten.
3. Den estimerte omsetningen ved fullføring og omsetningsinntaksprosenten for sammendragsoppgaven beregnes på nytt.
4. Den nye verdien for estimert omsetning ved fullføring fordeles i de underordnede aktivitetene i samme proporsjon som den opprinnelige planlagte omsetningen var på aktiviteten.
5. Den nye estimerte omsetningen ved fullføring for hver av de individuelle aktivitetene ned til bladnodeoppgavene blir beregnet. Basert på denne verdien beregnes de berørte underordnede oppgavene ned til bladnodene, gjenstående omsetning og omsetningsinntaksprosent basert på omsetningen til en fullstendig verdi. Dette fører til en ny projeksjon for omsetningsavviket i aktiviteten. 
6. Omsetning ved fullføring for sammendragsoppgavene helt til rotnoden beregnes på nytt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

