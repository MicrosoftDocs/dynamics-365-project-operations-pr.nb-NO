---
title: Administrere faktureringsrestanse
description: Dette emnet gir informasjon om hvordan du viser og arbeider med faktureringsrestansen i Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2e839c1f32248fff6d97271796666b5031f66490ccd98574045b770100bf379f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991093"
---
# <a name="manage-billing-backlog"></a>Administrere faktureringsrestanse

_ **Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

Dynamics 365 Project Operations har dedikerte visninger som bidrar til å administrere faktureringsrestansen. Hvis du vil administrere faktureringsrestansen, velger du koblingene i **Salg**-området under **Fakturering**. 

Følgende visninger er tilgjengelige:

- Honorarer og forskudd
- Tilgjengelige honorarer og forskudd
- Milepæler for fast pris
- Faktureringsrestanse for Tid og materiale

## <a name="retainers-and-advances"></a>Honorarer og forskudd

Visningen **Honorarer og forskudd** viser honorarer og forskudd for alle prosjektkontrakter. Etter at et honorar eller forskudd er fakturert, blir forskuddsbeløpet tilgjengelig for bruk.

## <a name="available-retainers-and-advances"></a>Tilgjengelige honorarer og forskudd

Visningen **Tilgjengelige honorarer og forskudd** viser alle tilgjengelige honorarer og forskudd for alle prosjektkontrakter. Etter at et honorar eller forskudd er fakturert, blir forskuddsbeløpet tilgjengelig for bruk og legges til i listen. Når beløpet for honoraret eller forskuddet er fullstendig brukt, fjernes det fra listen.

## <a name="fixed-price-milestones"></a>Milepæler for fast pris

Visningen **Milepæler for fast pris** viser alle milepæler med fast pris på alle prosjektkontraktslinjer. Fra denne visningen kan én eller flere milepæler merkes som **Klar for fakturering** eller **Ikke klar for fakturering**. Når du merker en milepæl som **Klar for fakturering**, blir den tilgjengelig for å bli lagt til i en kladdefaktura.

Når flerkundekontraktlinjer har en fastprisfaktureringsmetode, opprettes det en milepæl for hver kunde på kontraktlinjen. En milepæl kan opprettes og deretter deles inn i individuelle kundespesifikke milepæloppføringer. Denne delingen er intern og i henhold til faktureringsprosentdelingen som er definert for hver kunde på kontraktlinjen. I visningen **Milepæler for fast pris** vises de enkelte kundespesifikke milepæloppføringene. Hver av disse milepæloppføringene kan merkes som **Klar for fakturering** atskilt fra denne visningen. Når én eller flere av de relaterte milepælsdelingene er merket som **Klar for fakturering**, oppdateres hodestatusen til **Pågår** fra **Ikke startet**. Når alle milepæloppdelingene er fakturert, oppdateres statusen for hodemilepælene til **Fullført**.

En milepæl på et fakturautkast vises i denne visningen med faktureringsstatusen **Kundefaktura opprettet**. Når utkastfakturaen er bekreftet, oppdateres fakturastatusen for oppføringen til **Kundefaktura postert**. 

> [!NOTE] 
> Ikke oppdater denne statusverdien ved hjelp av egendefinert kode. Project Operations fungerer ikke på riktig måte når disse statusverdiene oppdateres med egendefinert kode.

## <a name="time-and-material-billing-backlog"></a>Faktureringsrestanse for Tid og materiale

Visningen **Faktureringsrestanse for Tid og materiale** viser alt ufakturert faktisk salg på tvers av alle prosjektkontrakter i systemet som ikke er fakturert. Én eller flere faktiske, ikke-fakturerte salgsverdier kan merkes som **Klar for fakturering** eller **Ikke klar for fakturering** fra denne visningen. Hvis du merker en ikke-fakturert faktisk salgsverdi som **Klar for fakturering**, blir den tilgjengelig for å bli lagt inn i et fakturautkast.

Ufakturerte faktiske verdier for salg med statusen **Må ikke overskrides** satt til **Mislykket** kan ikke merkes som **Klar for fakturering**. Hvis de faktiske verdiene må merkes som **Klar for fakturering**, tilbakestiller du statusen for andre faktiske verdier på kontraktlinjen som er inngått, og deretter evaluerer du statusen **Må ikke overskride** på nytt.

Hvis kontraktlinjer for flere kunder har tid og materiale-faktureringsmetode, og når tid og utgifter er godkjent, opprettes det ett ufakturert faktisk salg for hver kunde på kontraktlinjen i henhold til faktureringsprosentdelingen som er definert for hver av kundene. I visningen **Faktureringsrestanse for Tid og materiale** vises disse individuelle kundespesifikke ufakturerte faktiske salgsverdiene. Hver av disse oppføringene av ikke-fakturerte faktiske salgsverdier kan merkes som **Klar for fakturering** atskilt fra denne visningen.

En ufakturert faktisk salgsverdi som er på et fakturautkast, vises i denne visningen med faktureringsstatusen **Opprettet kundefaktura**. Når fakturautkastet er bekreftet, oppdateres fakturastatusen for denne oppføringen til **Kundefaktura postert**. 

> [!NOTE] 
> Ikke oppdater denne statusverdien ved hjelp av egendefinert kode. Project Operations fungerer ikke på riktig måte når disse statusverdiene oppdateres med egendefinert kode.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
