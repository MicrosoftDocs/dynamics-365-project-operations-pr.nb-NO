---
title: Administrere Må ikke overskrides-status og valideringer
description: Dette emnet gir informasjon om Må ikke overskrides-grensekontrollene som utføres i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5c491d4014ffc2568d7df72b542761ec9b1a90b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274040"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Administrere Må ikke overskrides-status og valideringer 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

## <a name="not-to-exceed-on-approvals"></a>Må ikke overskrides på godkjenninger

Når en tids- eller utgiftsoppføring sendes, opprettes en godkjenningsoppføring. Hvis godkjenningen er avgiftsbelagt og tilordnet en kontraktlinje for tid og materialer, fullfører systemet en Må ikke overskrides-validering på følgende nivåer:

  - Kontroll mot grensen som er angitt for kunden på prosjektkontraktlinjen
  - Kontroll mot grensen som er angitt på kontraktlinjen
  - Kontroll mot grensen som er angitt for kunden
  - Kontroll mot grensen som er angitt på kontrakten

Kontrollene på hvert nivå innebærer at det sikres at salgsverdien i denne godkjenningen ikke er i strid med Må ikke overskrides-grensen på dette nivået etter å ha tatt høyde for beløpet som allerede er registrert, og beløpet som er fakturert til dato på dette nivået.

Hvis kontrollen passerer, får godkjenningen valideringsstatusen **Vellykket**.

Hvis kontrollen mislykkes, får godkjenningen valideringsstatusen **Mislykket**. Må ikke overskrides-valideringsdetaljen informerer brukeren om hvilket nivå valideringen mislyktes på.

Når den sendte tids- eller utgiftsoppføringen anses som ikke-belastbar, settes Må ikke overskrides-valideringsstatusen til **Ikke aktuelt** med valideringsdetaljene lik **Ikke aktuelt**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Må ikke overskrides for ufakturerte faktiske verdier for salg

Når en tids- eller utgiftsoppføring godkjennes, opprettes det oppføringer for faktiske verdier for salg. Hvis ikke-fakturert faktisk salg som opprettes, er belastbar og tilordnet en kontraktlinje for tid og materialer, fullfører programmet en Må ikke overskrides-validering på følgende nivåer:

  - Kontroll mot grensen som er angitt for kunden for prosjektkontraktlinjen
  - Kontroll mot grensen som er angitt på kontraktlinjen
  - Kontroll mot grensen som er angitt for kunden
  - Kontroll mot grensen som er angitt på kontrakten

Kontrollene på hvert nivå sørger for at salgsverdien for den faktiske verdien ikke bryter Må ikke overskrides-grensen på dette nivået etter å ha tatt høyde for beløpet som allerede er registrert, og beløpet som er fakturert til dato på dette nivået.

Hvis kontrollen godkjennes, gis den ufakturerte salgverdien Må ikke overskrides-statusen **Beregnet**.

Hvis kontrollen ikke godkjennes, gis den ufakturerte salgverdien Må ikke overskrides-statusen **Mislykket**. Valideringsdetaljen informerer brukeren om hvilket nivå valideringen mislyktes på.

Når det ikke-fakturerte faktiske salget anses som ikke-belastbart eller gratis, og det ikke finnes noen Må ikke overskrides-grense på noen av de fire nivåene, eller den faktiske vedien som opprettes, er Kostnad, Honorar, Ressursenhet eller Salg mellom organisasjoner, må feltene **Må ikke overskrides-status** og **Må ikke overskrides-valideringsdetalj** være angitt til **Ikke aktuelt**.

## <a name="reset-the-not-to-exceed-status"></a>Tilbakestille statusen Må ikke overskrides

Du kan utføre en massetilbakestilling av Må ikke overskrides-statusen. Dette gjør det mulig for prosjektledere å justere Må ikke overskrides-valideringen for å prioritere fakturering av én bestemt jobb, tid eller utgift over andre som allerede er forpliktet fra den tilgjengelige Må ikke overskrides-mengden.

Når Må ikke overskrides-statusen tilbakestilles på ufakturert faktisk salg, reduseres det beregnede beløpet. Prosjektlederen kan velge en annen jobb, tid eller utgift som tidligere ikke bestod Må ikke overskrides-valideringen, og evaluere dem på nytt. Ved reduksjon av igangsatt beløp vil disse faktiske verdiene nå bestå valideringen. Dette hjelper prosjektlederen med å utøve større innflytelse på og kontroll av de fakturerbare transaksjonene for den perioden.

Hvis du vil tilbakestille Må ikke overskrides-statusen, velger du én eller flere faktiske verdier fra visningen **Faktureringsrestanse for Tid og materiale** eller **Faktiske verdier**, og deretter velger du **Tilbakestill statusen Må ikke overskrides**.

Statusen Må ikke overskrides-statusen blir tilbakestilt til **Ikke evaluert** på alle de relevante valgte faktiske verdiene. Faktiske verdier der Må ikke overskrides-statusen er tilbakestilt, er ikke-fakturert faktisk salg som ikke allerede er fakturert, ikke på en utkastfaktura, og er merket som belastbare. Alle andre valgte faktiske verdier ignoreres.

## <a name="reevaluate-not-to-exceed-status"></a>Evaluere statusen Må ikke overskrides på nytt

Du kan utføre en ny masseevaluering av Må ikke overskrides-statusen. Det kan være nyttig å evaluere Må ikke overskrides-status på nytt i følgende tilfeller:

  - Det er en ny forhandling om Må ikke overskrides-grensene med kunden, og de faktiske verdiene må evalueres på nytt.
  - Prosjektlederen ønsker å finjustere faktureringen av ufakturert salgsrestanse ved å prioritere én jobb over enn annen.

Hvis du vil evaluere Må ikke overskrides-statusen på nytt, velger du én eller flere faktiske verdier fra visningen **Faktureringsrestanse for Tid og materiale** eller **Faktiske verdier**, og deretter velger du **Evaluere statusen Må ikke overskrides på nytt**.

Alle de relevante valgte faktiske verdiene med en Må ikke overskrides-grense evalueres mot grensen som ikke må overskrides. Faktiske verdier som er relevante for ny evaluering av Må ikke overskrides-statusen, er ikke-fakturert faktisk salg som ikke allerede er fakturert, ikke på en utkastfaktura, og er merket som belastbare. Alle andre utvalgte faktiske verdier er valgt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]