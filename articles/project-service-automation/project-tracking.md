---
title: Fremdrift for prosjekt og kostnadsforbruk
description: Dette emnet gir informasjon om hvordan du sporer prosjektfremdrift og kostnadsforbruk.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754174"
---
# <a name="project-progress-and-cost-consumption"></a>Fremdrift for prosjekt og kostnadsforbruk

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Behovet for å spore fremdriften mot en tidsplan varierer etter bransje. Noen bransjer sporer på et detaljert nivå, mens andre bransjer sporer på et høyere nivå. Dette emnet viser hvordan du planlegger for å oppfylle organisasjonens krav.

## <a name="effort-tracking-view"></a>Visning av innsatssporing

Visningen **Innsatssporing** sporer fremdriften for oppgavene i tidsplanen. Den sammenligner de faktiske innsatstimene som er brukt på en oppgave, mot de planlagte innsatstimene for oppgaven. PSA bruker følgende formler til å beregne sporingsmåledata:

- Fremdriftsprosent = faktisk innsats brukt til dato ÷ planlagt innsats for oppgaven 
- Estimat for fullføring (ETC) = planlagt innsats – faktisk innsats brukt til dags dato 
- Estimat vedr fullføring (EAC) = resterende innsats + faktisk innsats brukt til dags dato 
- Forventet innsatsavvik = planlagt innsats – EAC

PSA viser en projeksjon av innsatsvariasjonen for oppgaven. Hvis EAC er større enn den planlagte innsatsen, blir aktiviteten beregnet for å ta mer tid enn det som opprinnelig ble planlagt. Derfor er den bak tidsplanen. Hvis EAC er mindre enn den planlagte innsatsen, blir aktiviteten beregnet for å ta mindre tid enn det som opprinnelig ble planlagt. Derfor er den foran tidsplanen.

## <a name="re-projecting-effort"></a>Projisere innsats på nytt

Det er vanlig at en prosjektleder kan revidere de opprinnelige beregningene på en aktivitet. Reprojisering av prosjekter er en prosjektleders oppfatning av estimater, gitt gjeldende status for et prosjekt. Vi anbefaler imidlertid ikke at prosjektledere endrer tallene i den opprinnelige planen, fordi den opprinnelige planen for prosjektet er den etablerte sannhetskilden for prosjektets tidsplan og kostnadsestimat, som alle interessenter i prosjektet har godtatt.

Det er to måter en prosjektleder kan reprojisere innsats på aktiviteter:

- Overstyr standard anslagstid med ny beregning av gjenstående gjenstående innsats for aktiviteten. 
- Overstyr standard fremdriftsprosent med ny beregning av den virkelige fremdriften for aktiviteten.

Hver av disse metodene forårsaker en ny beregning av aktivitetens ETC, EAC og fremdriftsprosent samt beregnet innsatsavvik for en aktivitet. EAC, ETC- og fremdriftsprosenten på aktivitetssammendragene beregnes også på nytt, og det lages en ny projisering av innsatsavvik.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Reprojisering av innsats i aktivitetssammendrag

Innsats i aktivitetssammendrag eller beholderaktivitet kan projiseres på nytt. Uansett om brukeren reaktiverer prosjekter ved hjelp av gjenstående innsats eller fremdriftsprosenten for aktivitetssammendraget, starter følgende sett med beregninger:

- EAC, ETC og fremdriftsprosent for aktiviteten beregnes.
- Den nye EAC fordeles i de underordnede aktivitetene i samme proporsjon som den opprinnelige EAC var på aktiviteten.
- Den nye EAC for hver av de individuelle aktivitetene ned til bladnodeoppgavene blir beregnet. 
- De berørte underordnede oppgavene til bladnodene får ETC og fremdriftsprosenten beregnet på nytt basert på EAC-verdien. Dette fører til en ny projeksjon for innsatsavviket i aktiviteten. 
- EAC-er for aktivitetssammendragene helt til rotnoden beregnes på nytt.

### <a name="cost-tracking-view"></a>Kostnadssporingsvisning 

**Kostnadssporings**-visningen sammenligner de faktiske kostnadene som ble brukt på en aktivitet, med de planlagte kostnadene på en aktivitet. 

> [!NOTE]
> Denne visningen viser bare arbeidskostnader og inkluderer ikke kostnader fra utgiftsestimater. 

PSA bruker følgende formler til å beregne sporingsmåledata:

- Prosentandel av kostnadene som brukes = faktisk kostnad brukt til dato ÷ planlagt kostnad for aktiviteten
- Kostnad for fullføring (CTC) = planlagt kostnad – faktisk kostnad brukt til dags dato
- EAC = CTC + faktisk kostnad brukt til dato
- Beregnet kostnadsavvik = planlagt kostnad – EAC

En projeksjon av kostnadsavviket vises for oppgaven. Hvis EAC er større enn den planlagte kostnaden, blir oppgaven beregnet til for å koste mer enn det som opprinnelig ble planlagt. Derfor tenderer den til å være over budsjettet. Hvis EAC er mindre enn den planlagte kostnaden, blir oppgaven beregnet til å koste mindre enn det som opprinnelig ble planlagt. Derfor tenderer den til å være under budsjettet.

## <a name="project-managers-re-projection-of-cost"></a>Prosjektlederens nye projisering av kostnad

Når innsatsen reprojiseres, blir alt forbrukt CTC, EAC, prosent av kostnad brukt og beregnet kostnadsavvik beregnet på nytt i visningen **Kostnadssporing**.

## <a name="project-status-summary"></a>Oppsummering av prosjektstatus

Sporingsdata i visningene **Innsatssporing** og **Kostnadssporing** viser fremdrift og kostnadsforbruk på oppgavenivåene prosjektrotnode, aktivitetssammendrags og bladnode. **Status**-delen på siden **Prosjektenhet** viser et sammendrag av status på prosjektnivå.

## <a name="status-summary-fields"></a>Statussammendragsfelt

Feltet **Generell prosjektstatus** er et redigerbart felt som viser den generelle statusen til prosjektet. Det bruker fargekoding, for eksempel grønn, gul og rød, for å vise økende risikoer. Med **Kommentarer**-feltet kan prosjektlederen angi spesifikke kommentarer om statusen. Feltet **Status oppdatert** er ikke redigerbart, og verdien er et tidsstempel som angir når statusen sist ble oppdatert.

Feltene **Tidsplanytelse** og **Kostnadsytelse** angis fra sporingsdatoen. Når tidsplan- og kostnadsavviket for rotnoden i visningen **Innsatssporing** er positive, kan du angi disse feltene til **Foran**. Når tidsplan- og kostnadsavviket for rotnoden er negativ, kan du angi dem til **Bak**.
