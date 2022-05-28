---
title: Metoder for ferdigstillelseskostnad
description: Dette emnet gir informasjon om metodene som brukes til å beregne kostnaden for å fullføre et prosjekt.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 244afa919e5fbc16be8f905acce2e2354c7da974
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601674"
---
# <a name="cost-to-complete-methods"></a>Metoder for ferdigstillelseskostnad

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet gir informasjon om metodene som brukes til å beregne kostnaden for å fullføre et prosjekt. Det finnes flere metoder du kan bruke til å beregne kostnaden for å fullføre et prosjekt. 

Når du oppretter et estimat for et prosjekt, kan du velge én av følgende metoder for ferdigstillelseskostnad på **Opprett estimat**-siden i **Metode for ferdigstillelseskostnad**-feltet.

| Metode for ferdigstillelseskostnad    | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Total kostnad – faktisk            | Angi estimerte kostnader manuelt i **Total kostnad**- eller **Totalt antall**-feltene ved å bruke **Kostnadsestimat**-knappen på **Estimatsiden**. Systemet trekker fra de faktiske kostnadene fra totalverdiene du har angitt. Totalen er kostnaden for å fullføre prosjektet. Denne metoden bruker ikke utgiftsestimater og ressurstildelinger som er angitt i Project Operations som er innebygd i Microsoft Dataverse. Total kostnad eller totalt antall kan oppdateres manuelt etter behov.  |
| Samlet prognose – faktisk        | Ressurstilordninger og utgiftsestimater brukes til å fastsette det samlede prognosebeløpet for prosjektet. Faktiske kostnader sammenlignes med denne prognosen for å beregne kostnaden for å fullføre.                                                                                                                                                                                                                                                                          |
| Som forrige estimat         | De samme estimatmetodene som ble brukt i den forrige perioden, brukes her. Denne metoden krever en prognosemodell hvis den forrige perioden krever en prognosemodell.                                                                                                                                                                                                                                                                                                                           |
| Sett ferdigstillelseskostnad til null | Denne metoden brukes vanligvis før estimatprosjektet er eliminert, og samsvarer totale estimater med faktisk posterte transaksjoner og tømmer **Ferdigstillelseskostnader**-kolonnen. Når fullført, er resultatet alltid 100 prosent. For hver kostnadslinje du oppretter, tømmes **Prognose**-avmerkingsboksen og det totale estimatet kopieres fra det forrige kostnadsestimatet. Det faktiske forbruket for estimatperioden er trukket fra ferdigstillelseskostnadene for prosjektet.              |
| Fra kostnadsmal           | Metoden for ferdigstillelseskostnader som er konfigurert i kostnadsmalen som er tilknyttet det valgte estimatprosjektet.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]