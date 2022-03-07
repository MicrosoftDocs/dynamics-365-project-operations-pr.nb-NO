---
title: Administrer faktureringsrestanse for prosjekt
description: Dette emnet inneholder informasjon om de ulike visningene som er tilgjengelige for bruk ved behandling av faktureringsreserve på prosjekter.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddd0b62133139a8d9d8d09920986890bd8616808
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003958"
---
# <a name="manage-project-billing-backlog"></a>Administrer faktureringsrestanse for prosjekt 

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations har dedikerte visninger som bidrar til å administrere faktureringsrestansen. Hvis du vil administrere faktureringsrestansen, velger du koblingene i **Salg**-området under **Fakturering**. 

Følgende visninger er tilgjengelige:

- Honorarer og forskudd
- Tilgjengelige honorarer og forskudd
- Milepæler for fast pris
- Faktureringsrestanse for produkt
- Faktureringsrestanse for Tid og materiale

## <a name="retainers-and-advances"></a>Honorarer og forskudd

**Honorarer og forskudd**-visningslistene viser alle honorarer og forskudd på tvers av alle prosjektkontrakter i systemet. Etter at et honorar eller forskudd er fakturert, blir forskuddsbeløpet tilgjengelig for bruk.

## <a name="available-retainers-and-advances"></a>Tilgjengelige honorarer og forskudd

**Tilgjengelige honorarer og forskudd**-visningslistene viser alle tilgjengelige honorarer og forskudd på tvers av alle prosjektkontrakter i systemet. Etter at et honorar eller forskudd er fakturert, blir forskuddsbeløpet tilgjengelig for bruk og legges til i listen. Etter at honorar- og forskuddbeløpet er brukt i sin helhet, fjernes det fra listen.

## <a name="fixed-price-milestones"></a>Milepæler for fast pris

**Milepæler for fast pris**-visningen viser alle faste prismilepæler på tvers av alle prosjektkontraktlinjer i systemet. Én eller flere milepæler kan merkes som **Klar for fakturering** eller **Ikke klar for fakturering** fra denne visningen. Når du merker en milepæl som **Klar for fakturering**, blir den tilgjengelig for å bli lagt til i en kladdefaktura.

Når flerkundekontraktlinjer har en fastprisfaktureringsmetode, opprettes det en milepæl for hver kunde på kontraktlinjen. En milepæl kan opprettes og deretter deles inn i individuelle kundespesifikke milepæloppføringer. Denne delingen er intern og i henhold til faktureringsprosentdelingen som er definert for hver kunde på kontraktlinjen. I visningen **Milepæler for fast pris** vises de enkelte kundespesifikke milepæloppføringene. Hver av disse milepæloppføringene kan merkes som **Klar for fakturering** atskilt fra denne visningen. Når én eller flere av de relaterte milepæloppdelingene er merket som **Klar til fakturering**, oppdateres hodestatusen til **Pågår** fra **Ikke startet**. Når alle milepældelingene er fakturert, oppdateres statusen for overskriftsmilepælen til **Fullført**.

En milepæl på et fakturautkast vises i denne visningen med faktureringsstatusen **Kundefaktura opprettet**. Når utkastfakturaen er bekreftet, oppdateres fakturastatusen for oppføringen til **Kundefaktura postert**. Ikke oppdater denne statusverdien ved hjelp av egendefinert kode. Project Operations fungerer ikke på riktig måte når disse statusverdiene oppdateres med egendefinert kode.

## <a name="product-billing-backlog"></a>Faktureringsrestanse for produkt

Visningen **Faktureringsrestanse for produkt** viser alle produktbaserte kontraktlinjer på tvers av alle prosjektkontrakter i systemet. Én eller flere produktbaserte kontraktlinjer kan merkes som **Klar for fakturering** eller **Ikke klar for fakturering** fra denne visningen. Når du merker en produktbasert kontraktlinje som **Klar for fakturering**, blir den tilgjengelig for å bli lagt til i en kladdefaktura.

En produktbasert kontraktlinje som er på en kladdefaktura, vises i denne visningen med faktureringsstatusen **Opprettet kundefaktura**. Når fakturautkastet er bekreftet, oppdateres fakturastatusen for denne oppføringen til **Kundefaktura postert**. Ikke oppdater denne statusverdien ved hjelp av egendefinert kode. Project Operations fungerer ikke på riktig måte når disse statusverdiene oppdateres med egendefinert kode.

## <a name="time-and-material-billing-backlog"></a>Faktureringsrestanse for Tid og materiale

Visningen **Faktureringsrestanse for Tid og materiale** viser alt ufakturert faktisk salg på tvers av alle prosjektkontrakter i systemet som ikke er fakturert. Én eller flere faktiske, ikke-fakturerte salgsverdier kan merkes som **Klar for fakturering** eller **Ikke klar for fakturering** fra denne visningen. Hvis du merker en ikke-fakturert faktisk salgsverdi som **Klar for fakturering**, blir den tilgjengelig for å bli lagt inn i et fakturautkast.

Ufakturerte faktiske verdier for salg med statusen **Må ikke overskrides** satt til **Mislykket** kan ikke merkes som **Klar for fakturering**. Hvis de faktiske verdiene må merkes som **Klar for fakturering**, tilbakestilles statusen for andre faktiske verdier på kontraktlinjen som er registrert. og evaluer deretter statusen **Må ikke overskrides** på nytt.

Hvis kontraktlinjer for flere kunder har tid og materiale-faktureringsmetode, og når tid og utgifter er godkjent, opprettes det ett ufakturert faktisk salg for hver kunde på kontraktlinjen i henhold til faktureringsprosentdelingen som er definert for hver av kundene. I visningen **Faktureringsrestanse for Tid og materiale** vises disse individuelle kundespesifikke ufakturerte faktiske salgsverdiene. Hver av disse oppføringene av ikke-fakturerte faktiske salgsverdier kan merkes som **Klar for fakturering** atskilt fra denne visningen.

Et ufakturert faktisk salg på en kladdefaktura vises i denne visningen med faktureringsstatusen **Opprettet kundefaktura**. Når fakturautkastet er bekreftet, oppdateres fakturastatusen for denne oppføringen til **Kundefaktura postert**. Ikke oppdater denne statusverdien ved hjelp av egendefinert kode. Project Operations fungerer ikke på riktig måte når disse statusverdiene oppdateres med egendefinert kode.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
