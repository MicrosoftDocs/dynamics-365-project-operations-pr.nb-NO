---
title: Oversikt over prosjektsporing
description: Dette emnet gir informasjon om hvordan du sporer prosjektfremdrift og kostnadsforbruk.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907375"
---
# <a name="project-tracking-overview"></a>Oversikt over prosjektsporing

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Behovet for å spore fremdriften mot en tidsplan varierer etter bransje. Noen bransjer sporer på et detaljert nivå, mens andre bransjer sporer på et høyere nivå. Dette emnet viser hvordan du planlegger for å oppfylle organisasjonens krav.

## <a name="effort-tracking-view"></a>Visning av innsatssporing

Visningen **Innsatssporing** sporer fremdriften for oppgaver i tidsplanen ved å sammenligne de faktiske innsatstimene som er brukt på en oppgave, med oppgavens planlagte innsatstimer. Dynamics 365 Project Operations bruker følgende formler til å beregne sporingsmåledata:

- **Fremdriftsprosent**: Faktisk innsats brukt til dags dato ÷ sluttestimat (EAC) 
- **Estimat for fullføring (ETC)**: Planlagt innsats – faktisk innsats brukt til dags dato 
- **EAC**: Resterende innsats + faktisk innsats brukt til dags dato 
- **Forventet innsatsavvik**: Planlagt innsats – EAC

Project Operations viser en projeksjon av innsatsvariasjonen for oppgaven. Hvis EAC er større enn den planlagte innsatsen, blir oppgaven beregnet til å ta mer tid enn det som opprinnelig ble planlagt, og er etter tidsplanen. Hvis EAC er mindre enn den planlagte innsatsen, blir oppgaven beregnet til å ta mindre tid enn det som opprinnelig ble planlagt, og er foran tidsplanen.

## <a name="reprojecting-effort"></a>Projisere innsats på nytt

Prosjektleder reviderer ofte de opprinnelige beregningene på en aktivitet. Reprojisering av prosjekter er en prosjektleders oppfatning av estimater, gitt gjeldende status for et prosjekt. Vi anbefaler imidlertid ikke at prosjektledere endrer de opprinnelige tallene. Dette er fordi den opprinnelige planen for prosjektet er den etablerte sannhetskilden for prosjektets tidsplan og kostnadsestimat, som alle interessenter i prosjektet har godtatt.

Det er to måter en prosjektleder kan reprojisere innsats på aktiviteter:

- Overstyr standard anslagstid med ny beregning av gjenstående gjenstående innsats for aktiviteten. 
- Overstyr standard fremdriftsprosent med ny beregning av den virkelige fremdriften for aktiviteten.

Hver metode forårsaker en ny beregning av aktivitetens ETC, EAC, fremdriftsprosent og beregnet innsatsavvik for en aktivitet. EAC, ETC- og fremdriftsprosenten på aktivitetssammendragene beregnes også på nytt, og det lages en ny projisering av innsatsavvik.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reprojisering av innsats i aktivitetssammendrag

Innsats i aktivitetssammendrag eller beholderaktivitet kan projiseres på nytt. Uansett om brukeren reaktiverer prosjekter ved hjelp av gjenstående innsats eller fremdriftsprosenten for aktivitetssammendraget, starter følgende sett med beregninger:

- EAC, ETC og fremdriftsprosent for aktiviteten beregnes.
- Den nye EAC fordeles i de underordnede aktivitetene i samme proporsjon som den opprinnelige EAC var på aktiviteten.
- Den nye EAC for hver av de individuelle aktivitetene ned til bladnodeoppgavene blir beregnet. 
- De berørte underordnede oppgavene til bladnodene får ETC og fremdriftsprosenten beregnet på nytt basert på EAC-verdien. Dette fører til en ny projeksjon for innsatsavviket i aktiviteten. 
- EAC-er for aktivitetssammendragene helt til rotnoden beregnes på nytt.

### <a name="cost-tracking-view"></a>Kostnadssporingsvisning 

**Kostnadssporings**-visningen sammenligner de faktiske kostnadene som ble brukt på en aktivitet, med de planlagte kostnadene på en aktivitet. 

> [!NOTE]
> Denne visningen viser bare arbeidskostnader og inkluderer ikke kostnader fra utgiftsestimater. Project Operations bruker følgende formler til å beregne sporingsmåledata:

- **Prosentandel av kostnadene som brukes**: Faktisk kostnad brukt til dato ÷ beregnet kostnad ved fullføring
- **Kostnad for fullføring (CTC)**: Planlagt kostnad – faktisk kostnad brukt til dags dato
- **EAC**: Gjenværende kostnad + faktisk kostnad brukt til dato
- **Beregnet kostnadsavvik**: Planlagt kostnad – EAC

En projeksjon av kostnadsavviket vises for oppgaven. Hvis EAC er større enn den planlagte kostnaden, blir oppgaven beregnet til for å koste mer enn det som opprinnelig ble planlagt. Derfor tenderer den til å være over budsjettet. Hvis EAC er mindre enn den planlagte kostnaden, blir oppgaven beregnet til å koste mindre enn det som opprinnelig ble planlagt. Derfor tenderer den til å være under budsjettet.

## <a name="project-managers-reprojection-of-cost"></a>Prosjektlederens nye projisering av kostnad

Når innsatsen reprojiseres, blir alt forbrukt CTC, EAC, prosent av kostnad brukt og beregnet kostnadsavvik beregnet på nytt i visningen **Kostnadssporing**.

## <a name="project-status-summary"></a>Oppsummering av prosjektstatus

Sporingsdata i visningene **Innsatssporing** og **Kostnadssporing** viser fremdrift og kostnadsforbruk på oppgavenivåene prosjektrotnode, aktivitetssammendrags og bladnode. **Status**-delen på siden **Prosjektenhet** viser et sammendrag av status på prosjektnivå.

## <a name="status-summary-fields"></a>Statussammendragsfelt

Feltet **Generell prosjektstatus** er et redigerbart felt som viser den generelle statusen til prosjektet. Det bruker fargekoding, for eksempel grønn, gul og rød, for å vise økende risikoer. Med **Kommentarer**-feltet kan prosjektlederen angi spesifikke kommentarer om statusen. Feltet **Status oppdatert** er ikke redigerbart, og verdien er et tidsstempel som angir når statusen sist ble oppdatert.

Feltene **Tidsplanytelse** og **Kostnadsytelse** angis fra sporingsdatoen. Når tidsplan- og kostnadsavviket for rotnoden i visningen **Innsatssporing** er positive, kan du angi disse feltene til **Foran**. Når tidsplan- og kostnadsavviket for rotnoden er negativ, kan du angi dem til **Bak**.
