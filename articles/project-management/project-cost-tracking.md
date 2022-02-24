---
title: Sporing av prosjektkostnader
description: Dette emnet inneholder informasjon om hvordan Project Operations sporer fremdriften mot arbeidskostnader og forbruk i et prosjekt.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28cb692c61ae4137a28973dc1bd70ffd989dd535
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711072"
---
# <a name="labor-cost-tracking-on-projects"></a>Kostnadssporing av arbeid på prosjekter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations sporer arbeidsestimater og forbruk til lavest mulig detaljstyring i prosjektplanen. Det økonomiske estimatet for arbeidskostnader er basert på planlagt innsats og de generiske eller navngitte ressursene som er tilordnet hver bladnodeoppgave i prosjektplanen. Når prosjektet starter og personene begynner å rapportere tid på ulike prosjektoppgaver, oppsummeres det faktiske forbruket av arbeid som starter en beregning av prognosene.

## <a name="labor-cost-tracking-view"></a>Visningen Kostnadssporing av arbeid

På **Prosjekter**-siden, på **Sporing**-fanen, kan du velge **Sporing** > **Kostnad** for å åpne **Kostnadssporing**-visningen og se fremdriften av arbeid brukt på hver oppgave i prosjektplanen. Denne visningen sammenligner også de faktiske arbeidskostnadene som er brukt på en aktivitet, med aktivitetens planlagte arbeidskostnader. Project Operations bruker følgende formler til å beregne måledata for arbeidskostnader:

- **Planlagt kostnad**: Beregnet kostnad for alle ressurstilordninger for hver oppgave i bladnode
- **Faktisk kostnad**: Summen av alle faktiske kostnader for tid som er registrert for oppgaven
- **Kostnadsforbruk i prosent**: Faktisk kostnad ÷ Kostnadsestimat ved fullføring
- **Gjenstående kostnad**: Kostnadsestimat ved fullføring – Faktisk kostnad
- **Kostnad ved fullføring**: Gjenstående kostnad + Faktisk kostnad
- **Kostnadsavvik**: Planlagt kostnad – Kostnadsestimat ved fullføring

Hver oppgave viser en projisering av kostnadsavviket for oppgaven. Hvis kostnadsestimatet ved fullføring er mer enn planlagt kostnad, beregnes det at aktiviteten skal gå over budsjettet. Hvis kostnadsestimatet ved fullføring er mindre enn planlagt kostnad, beregnes det at aktiviteten skal fullføres under budsjettet.

>[!NOTE]
> Project Operations viser bare arbeidskostnader på **Prosjekt**-siden på **Sporing**-fanen. Materialer og utgifter kan estimeres og spores for forbruk, men disse kostnadene er ikke inkludert i kostandene som vises på **Sporing**-fanen. Denne fanen er utformet for bare å fungere for ny projisering av arbeidskostnader ved å projisere innsats på nytt.
Alle kostnadsbeløp som vises, konverteres til prosjektets kostnadsvaluta fra prosjektets kostprisvaluta som brukes til å fastsette kostnadssatsen. Kostnadsvalutaen for prosjektet er valutaen til kontraktsenheten i prosjektet. Det kan hende at de estimerte kostnadsverdiene for tiden som vises på **Estimater**-fanen på **Prosjekt**-siden, ikke utgjør hele den planlagte kostnadsen på **Sporing**-fanen. Årsaken til dette avviket er forskjellene i hvordan estimert kostnad opppsummeres i rutenettet **Estimater**, og hvordan planlagt kostnad beregnes i rutenettet **Sporing**. 
>
> - **Estimater**-fanen beregner den estimerte kostnaden ved å bruke samme valuta for kostnadssatsen i prislisten. Deretter konverteres den beregnede kostnaden i prislistevalutaen til den beregnede kostnaden i prosjektets kostnadsvaluta. Beregnet kostnad i prosjektvalutaen vises avrundet til to desimaler. Valutapresisjon brukes ikke under konverteringen. 
> - På **Sporing**-fanen følger beregningen av planlagte kostnader en litt annen beregningsrekkefølge som innebærer at valutapresisjon brukes i to faser: 
   ><ol>
   ><li>Det beregnede kostnadsbeløpet i prislistevalutaen konverteres til standardvalutaen (konvertering 1).</li>
   ><li>Det beregnede kostnadsbeløpet i basisvalutaen konverteres til prosjektkostnadsvalutaen (konvertering 2). </li>
   ></ol>
   >Valutapresisjon brukes i begge trinnene for å få en planlagt kostnad (på **Sporing**-fanen) som avviker noe fra den estimerte kostnaden (i visningen **Tidsinndelt** på **Estimater**-fanen). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Projisere kostnader på nytt for bladnodeoppgaver

Arbeidskostnader i en bladnodeoppgave kan ikke løses på nytt direkte i kategorien **Sporing** på **Prosjekt**-siden. Du kan imidlertid bruke visningen **Innsatssporing** til å utføre gjenstående innsats på en oppgave på nytt. Dette fører til en omberegning av de gjenstående kostnadene for aktiviteten. Nedenfor finner du en beskrivelse av hvordan dette fungerer.

1. En prosjektleder kan projisere innsats på oppgaver på nytt ved å oppdatere standardverdien i **Gjenstående innsats**-feltet med et nytt overslag over gjenstående innsats for aktiviteten. Ny projisering fører til en omberegning av oppgavens innsatsestimat ved fullføring, fremdriftsprosenten og det beregnede innsatsavviket for en oppgave. EAC, estimatet for fullføring (ETC) og fremdriftsprosenten på aktivitetssammendragene beregnes også på nytt, og det lages en ny projisering av innsatsavvik.
2. Basert på den nye verdien for gjenstående innsats på oppgaven beregner systemet de gjenstående kostnadene i visningen **Kostnadssporing**. For å beregne gjenstående kostnad basert på resterende innsats beregner systemet først den gjennomsnittlige kostnaden for en times innsats på aktiviteten som planlagt kostnad eller planlagt innsats. De planlagte kostnadene er summen av kostnadene for alle ressurstilordninger for aktiviteten. Gjennomsnittlig kostnad per time brukes til å beregne gjenstående kostnad for den nylig beregnede gjenstående innsatsen for aktiviteten.
3. Kostnaden for fullført og kostnadsinntaksprosenten for aktiviteten med bladnode beregnes på nytt.
4. Kostnaden ved fullføring for aktivitetssammendragene helt til rotnoden beregnes på nytt.

## <a name="reprojecting-costs-on-summary-tasks"></a>Projisere kostnader på nytt for sammendragsoppgaver

Du kan projisere arbeidskostnader på nytt for sammendragsoppgaver eller beholderoppgaver. Du kan imidlertid ikke løse arbeidskostnader direkte på nytt for en prosjektsammendragsoppgave i kategorien **Sporing** på **Prosjekt**-siden. På samme måte som med oppgaver med bladnoder kan du utføre sammendrags- og beholderoppgaver på nytt ved hjelp av visningen **Innsatssporing**. I denne visningen kan du projisere gjenstående innsats på nytt for en sammendragsoppgave, noe som fører til en omberegning av de gjenstående kostnadene for sammendragsoppgaven. Nedenfor finner du en beskrivelse av hvordan dette fungerer.

1. En prosjektleder kan projisere innsats på sammendragsoppgaver på nytt ved å oppdatere standardverdien for den resterende innsatsen med et nytt overslag for aktiviteten. Denne oppdateringen fører til en omberegning av sammendragsoppgavens estimat ved fullføring, fremdriftsprosenten og det beregnede innsatsavviket for en oppgave. EAC, ETC- og fremdriftsprosenten på aktivitetssammendragene beregnes også på nytt, og det lages en ny projisering av innsatsavvik.
2. Basert på den nye verdien for gjenstående innsats på sammendragsoppgaven beregner systemet de gjenstående kostnadene i visningen **Kostnadssporing**. For å beregne gjenstående kostnad basert på resterende innsats beregner systemet først den gjennomsnittlige kostnaden for en times innsats på sammendragsoppgaven som planlagt kostnad eller planlagt innsats. Gjennomsnittlig kostnad per time brukes til å beregne kostnad for den nylig beregnede gjenstående innsatsen for sammendragsoppgaven.
3. Kostnaden for fullført og kostnadsinntaksprosenten for sammendragsoppgaven beregnes på nytt.
4. Den nye kostnaden ved fullføring fordeles i de underordnede aktivitetene i samme proporsjon som den opprinnelige planlagte kostnaden var på aktiviteten.
5. Den nye kostnaden ved fullføring for hver av de individuelle aktivitetene ned til bladnodeoppgavene blir beregnet. Basert på denne verdien beregnes de berørte underordnede oppgavene ned til bladnodene, gjenstående kostnad og kostnadsinntaksprosent basert på kostnaden til en fullstendig verdi. Denne verdien fører til en ny projeksjon for kostnadsavviket i aktiviteten. 


Feltet **Kostnadsytelse** kan angis fra sporingsdataene. Når kostnadsavviket for rotnoden i visningen **Kostnadssporing** er negativ, kan du sette dette feltet til **Under budsjett**. Når kostnadsavviket for rotnoden er positiv, kan du sette verdien til **Over budsjett**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
