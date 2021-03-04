---
title: Administrere faktureringsrestansen
description: Dette emnet gir informasjon om hvordan du viser og arbeider med faktureringsrestansen i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bec6afe04a705d4f55ac3a7de93a64b47021fbb4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122355"
---
# <a name="manage-the-billing-backlog"></a>Administrere faktureringsrestansen

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations har to dedikerte visninger som hjelper deg med å arbeide med og administrere faktureringsrestansen. Disse er **Milepæler for fast pris** og **Faktureringsrestanse for Tid og materiale**. Du kan velge en visning ved å gå til **Salg**-området i Project Operations og velge **Fakturering** på den venstre navigasjonssiden. Koblingene til faktureringsrestansen er lagret der.

## <a name="fixed-price-milestones"></a>Milepæler for fast pris

Denne visningen viser alle milepæler for fast pris på tvers av alle prosjektkontraktlinjene i systemet. Én eller flere milepæler kan merkes som **Klar for fakturering** eller **Ikke klar for fakturering** fra denne visningen. Når du merker en milepæl som **Klar for fakturering**, blir milepælen tilgjengelig for et fakturautkast.

Når kontraktlinjer med flere kunder har en faktureringsmetode for fastpris, opprettes det én milepæl for hver kunde på kontraktlinjen. Brukeren oppretter en milepæl, og denne milepælen deles inn i kunde = spesifikke milepæloppføringer internt, i henhold til den delte prosentandelen for fakturering som er definert for hver kunde på kontraktlinjen. I visningen **Milepæler for fast pris** vises individuelle, kundespesifikke milepæloppføringer. Hver av disse milepæloppføringene kan merkes som **Klar for fakturering** atskilt fra denne visningen. Når én eller flere av de relaterte milepældelene er merket som **Klar for fakturering**, flyttes hodet til statusen **Pågår** fra **Ikke startet**. Når alle milepældelene er fakturert, blir statusen for hodet i milepælen **Fullført**.

En milepæl på et fakturautkast vises i denne visningen med faktureringsstatusen **Kundefaktura opprettet**. Når fakturautkastet er bekreftet, oppdateres fakturastatusen for denne oppføringen til **Faktura postert**. Det anbefales ikke å oppdatere denne statusverdien ved hjelp av egendefinert kode. Project Operations fungerer ikke riktig hvis disse statusverdiene oppdateres med egendefinert kode.

## <a name="time-and-material-billing-backlog"></a>Faktureringsrestanse for Tid og materiale

Denne visningen viser alle faktiske salgsverdier som ikke er fakturert, på tvers av alle prosjektkontrakter i systemet. Én eller flere faktiske, ikke-fakturerte salgsverdier kan merkes som **Klar for fakturering** eller **Ikke klar for fakturering** fra denne visningen. Hvis du merker en ikke-fakturert faktisk salgsverdi som **Klar for fakturering**, blir den tilgjengelig for å bli lagt inn i et fakturautkast.

Ikke-fakturerte faktiske salgsverdier med **Må ikke overskride**-statusen **Mislyktes** kan ikke merkes som **Klar for fakturering**. Hvis disse faktiske verdiene må merkes på denne måten, tilbakestiller du statusen for andre faktiske verdier på kontraktlinjen som er forpliktet, og deretter evaluerer du **Må ikke overskride**-statusen.

Når det gjelder kontraktlinjer for flere kunder som har en faktureringsmetode for tid og materialer, når tid og utgifter er godkjent, opprettes det en ikke-fakturert faktisk salgsverdi for hver kunde på kontraktlinjen i henhold til del faktureringsprosentdelingen som er definert for hver kunde på kontraktlinjen. I visningen **Faktureringsrestanse for Tid og materiale** kan du se disse individuelle, kundespesifikke, ikke-fakturerte faktiske salgsverdiene. Hver av disse oppføringene av ikke-fakturerte faktiske salgsverdier kan merkes som **Klar for fakturering** atskilt fra denne visningen.

En ikke-fakturert faktisk salgsverdi på et fakturautkast vises i denne visningen med en **Faktureringsstatus** som er **Kundefaktura opprettet**. Når fakturautkastet er bekreftet, oppdateres fakturastatusen for denne oppføringen til **Kundefaktura postert**. Det anbefales ikke å oppdatere denne statusverdien ved hjelp av egendefinert kode, når den er i denne tilstanden. Project Operations fungerer ikke riktig når disse statusverdiene oppdateres med egendefinert kode.


[!INCLUDE[footer-include](../includes/footer-banner.md)]