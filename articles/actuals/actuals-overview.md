---
title: Faktiske verdier
description: Dette emnet gir informasjon om å arbeide med faktiske verdier i Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081610"
---
# <a name="actuals"></a>Faktiske verdier 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Faktiske verdier er mengden arbeid som er fullført på et prosjekt. De opprettes som et resultat av tids- og utgiftsoppføringer og journaloppføringer og fakturaer.

## <a name="journal-lines-and-time-submission"></a>Journallinjer og tidssending

Hvis du vil ha mer informasjon om tidsregistrering, kan du se [Oversikt over tidsregistrering](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Tid og materialer

Når en tidsregistrering som er sendt, er koblet til et prosjekt som er tilordnet en kontraktlinje for tid og materialer, oppretter systemet to journallinjer, én for kostnad og én for ufakturert salg.

### <a name="fixed-price"></a>Fast pris

Når en tidsoppføring som er sendt, kobles til et prosjekt som er tilordnet en kontraktlinje for fast pris, oppretter systemet én journallinje for kostnad.

### <a name="default-pricing"></a>Standardprising

Logikken for oppretting av standardpriser finnes på journallinjen. Feltverdiene fra tidsoppføringen kopieres til journallinjen. Disse verdiene inneholder transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet i den aktuelle prislisten.

Feltene som påvirker standardprising, for eksempel **Rolle** og **Organisasjonsenhet** , brukes til å bestemme den passende prisen på journallinjen. Du kan legge til et egendefinert felt for tidsoppføringen. Hvis du vil at feltverdien skal overføres til faktiske verdier, oppretter du feltet på den faktiske enheten og bruker felttilordninger til å kopiere feltet fra tidsoppføringen til den faktiske verdien.

## <a name="journal-lines-and-basic-expense-submission"></a>Journallinjer og sending av grunnleggende utgifter

Hvis du vil ha mer informasjon om utgiftsregistrering, kan du se [Oversikt over utgifter](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Tid og materialer

Når en grunnleggende utgiftsregistrering som er sendt, er koblet til et prosjekt som er tilordnet en kontraktlinje for tid og materialer, oppretter systemet to journallinjer, én for kostnad og én for ufakturert salg.

### <a name="fixed-price"></a>Fast pris

Når en grunnleggende utgiftsoppføring som er sendt, kobles til et prosjekt som er tilordnet en kontraktlinje for fast pris, oppretter systemet én journallinje for kostnad.

### <a name="default-pricing"></a>Standardprising

Logikken for å angi standardpriser for utgifter er basert på utgiftskategorien. Både transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet brukes til å bestemme den aktuelle prislisten. Beløpet som er angitt for selve prisen, blir imidlertid som standard angitt direkte på de relaterte utgiftsjournallinjene for kostnad og salg som standard.

Kategoribasert oppføring av standardpriser per enhet på utgiftsoppføringer er ikke tilgjengelig.

## <a name="use-entry-journals-to-record-costs"></a>Bruk oppføringsjournaler til å registrere kostnader

Du kan bruke oppføringsjournaler til å registrere kostnad eller omsetning i transaksjonsklassene for materialer, gebyr, tid, utgift eller avgift. Journaler kan brukes til følgende formål:

- Registrer de faktiske kostnadene for materialer og salg på et prosjekt.
- Flytt faktiske verdier for transaksjoner fra et annet system til Microsoft Dynamics 365 Project Operations.
- Registrer kostnader som er påløpt i et annet system. Disse kostnadene kan omfatte innkjøps- eller underleveransekostnader.

> [!IMPORTANT]
> Programmet validerer ikke journallinjetypen eller den relaterte prisingen som er angitt på journallinjen. Derfor bør bare en bruker som er fullstendig klar over regnskapsinnvirkningen de faktiske verdiene har på prosjektet, bruke oppføringsjournaler til å opprette faktiske verdier. På grunn av innvirkningen til denne journaltypen bør du være nøye når du skal velge hvem som skal ha tilgang til å opprette oppføringsjournaler.
## <a name="record-actuals-based-on-project-events"></a>Registrer faktiske verdier basert på prosjekthendelser

Project Operations registrerer de finansielle transaksjonene som inntreffer under et prosjekt. Disse transaksjonene registreres som faktiske verdier. Følgende tabeller viser de forskjellige typene faktiske verdier som opprettes, avhengig av om prosjektet er et tids-og-materiale-prosjekt eller et fastprisprosjekt, er i forsalgsfasen eller er et internt prosjekt.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Ressursen tilhører samme organisasjonsenhet som prosjektets kontraktenhet

<table>
<thead>
<tr>
<th rowspan="3">Hendelse</th>
<th colspan="4">Fakturerbart eller solgt prosjekt</th>
<th rowspan="3">Prosjekt i forsalgsfasen</th>
<th rowspan="3">Internt prosjekt</th>
</tr>
<tr>
<th colspan="2">Tid og materialer</th>
<th colspan="2">Fast pris</th>
</tr>
<tr>
<th>Faktisk</th>
<th>Transaksjonsvaluta</th>
<th>Fast pris</th>
<th>Transaksjonsvaluta</th>
</tr>
</thead>
<tbody>
<tr>
<td>En tidsoppføring opprettes.</td>
<td colspan="6">Ingen aktivitet i den faktiske enheten</td>
</tr>
<tr>
<td>En tidsoppføring sendes.</td>
<td colspan="6">Ingen aktivitet i den faktiske enheten</td>
</tr>
<tr>
<td rowspan="2">Tiden godkjennes, og ingen endringer av eller økning av fakturerbar tid oppstår under godkjenning.</td>
<td>Faktisk kostnad</td>
<td>Valuta for kontraktsenhet</td>
<td rowspan="2">Faktisk kostnad</td>
<td rowspan="2">Valuta for kontraktsenhet
<td rowspan="2">Faktisk kostnad</td>
<td rowspan="2">Faktisk kostnad</td>
</tr>
<tr>
<td>Ufakturert faktisk salg – belastbart</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td rowspan="3">Tiden godkjennes, og en reduksjon av fakturerbar tid oppstår under godkjenning.</td>
<td>Faktisk kostnad</td>
<td>Valuta for kontraktsenhet</td>
<td rowspan="3">Faktisk kostnad</td>
<td rowspan="3">Valuta for kontraktsenhet</td>
<td rowspan="3">Faktisk kostnad</td>
<td rowspan="3">Faktisk kostnad</td>
</tr>
<tr>
<td>Ufakturert faktisk salg – belastbart for det nye antallet</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td>Ufakturert faktisk salg – ikke-belastbart for forskjellen</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td rowspan="2">En faktura bekreftes, og ingen endringer av eller økning av fakturerbar tid oppstår.</td>
<td>Ufakturert salg omgjort</td>
<td>Valuta for prosjektkontrakt</td>
<td rowspan="2">Fakturert salg for milepæl</td>
<td rowspan="2">Valuta for prosjektkontrakt</td>
<td rowspan="2">Ikke aktuelt</td>
<td rowspan="2">Ikke aktuelt</td>
</tr>
<tr>
<td>Fakturert salg</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td rowspan="3">En faktura bekreftes, og en reduksjon av fakturerbar tid oppstår.</td>
<td>Ufakturert salg omgjort</td>
<td>Valuta for prosjektkontrakt</td>
<td rowspan="3">Ikke aktuelt</td>
<td rowspan="3">Ikke aktuelt</td>
<td rowspan="3">Ikke aktuelt</td>
<td rowspan="3">Ikke aktuelt</td>
</tr>
<tr>
<td>Fakturert salg – belastbart for det nye antallet</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td>Fakturert salg – ikke-belastbart for forskjellen</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td rowspan="2">En faktura korrigeres for å øke det belastbare antallet.</td>
<td>Fakturert salg – tilbakeføring</td>
<td>Valuta for prosjektkontrakt</td>
<td rowspan="5">
<ul>
<li>Tilbakeføring av fakturert salg for milepæl</li>
<li>Endring i milepælstatus fra <strong>Fakturert</strong> til <strong>Klar for faktura</strong></li>
</ul>
</td>
<td rowspan="5">Valuta for prosjektkontrakt</td>
<td rowspan="5">Ikke aktuelt</td>
<td rowspan="5">Ikke aktuelt</td>
</tr>
<tr>
<td>Fakturert salg</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td rowspan="3">En faktura korrigeres for å redusere det belastbare antallet.</td>
<td>Fakturert salg – tilbakeføring</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td>Fakturert salg for det nye antallet</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td>Ufakturert salg – belastbart for forskjellen</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Ressursen tilhører en annen organisasjonsenhet enn prosjektets kontraktenhet

<table>
<thead>
<tr>
<th rowspan="3">Hendelse</th>
<th colspan="4">Fakturerbart eller solgt prosjekt</th>
<th rowspan="3">Prosjekt i forsalgsfasen</th>
<th rowspan="3">Internt prosjekt</th>
</tr>
<tr>
<th colspan="2">Tid og materialer</th>
<th colspan="2">Fast pris</th>
</tr>
<tr>
<th>Faktisk</th>
<th>Transaksjonsvaluta</th>
<th>Fast pris</th>
<th>Transaksjonsvaluta</th>
</tr>
</thead>
<tbody>
<tr>
<td>En tidsoppføring opprettes.</td>
<td colspan="6">Ingen aktivitet i den faktiske enheten</td>
</tr>
<tr>
<td>En tidsoppføring sendes.</td>
<td colspan="6">Ingen aktivitet i den faktiske enheten</td>
</tr>
<tr>
<td rowspan="4">Tiden godkjennes, og ingen endringer av eller økning av fakturerbar tid oppstår under godkjenning.</td>
<td>Faktisk kostnad</td>
<td>Valuta for kontraktsenhet</td>
<td rowspan="4">Faktisk kostnad</td>
<td rowspan="4">Valuta for kontraktsenhet</td>
<td rowspan="4">Faktisk kostnad</td>
<td rowspan="4">Faktisk kostnad</td>
</tr>
<tr>
<td>Ufakturert faktisk salg – belastbart</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td>Kostnad for ressursenhet</td>
<td>Valuta for ressursenhet</td>
</tr>
<tr>
<td>Salg mellom organisasjoner</td>
<td>Valuta for kontraktsenhet</td>
</tr>
<tr>
<td rowspan="5">Tiden godkjennes, og en reduksjon av fakturerbar tid oppstår under godkjenning.</td>
<td>Faktisk kostnad</td>
<td>Valuta for kontraktsenhet</td>
<td rowspan="5">Faktisk kostnad</td>
<td rowspan="5">Valuta for kontraktsenhet</td>
<td rowspan="5">Faktisk kostnad</td>
<td rowspan="5">Faktisk kostnad</td>
</tr>
<tr>
<td>Kostnad for ressursenhet</td>
<td>Valuta for ressursenhet</td>
</tr>
<tr>
<td>Salg mellom organisasjoner</td>
<td>Valuta for kontraktsenhet</td>
</tr>
<tr>
<td>Ufakturert faktisk salg – belastbart for det nye antallet</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td>Ufakturert faktisk salg – ikke-belastbart for forskjellen</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td rowspan="2">En faktura bekreftes, og ingen endringer av eller økning av fakturerbar tid oppstår.</td>
<td>Ufakturert salg omgjort</td>
<td>Valuta for prosjektkontrakt</td>
<td rowspan="2">Fakturert salg for milepæl</td>
<td rowspan="2">Valuta for prosjektkontrakt</td>
<td rowspan="2">Ikke aktuelt</td>
<td rowspan="2">Ikke aktuelt</td>
</tr>
<tr>
<td>Fakturert salg</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td rowspan="3">En faktura bekreftes, og en reduksjon av fakturerbar tid oppstår.</td>
<td>Ufakturert salg omgjort</td>
<td>Valuta for prosjektkontrakt</td>
<td rowspan="3">Ikke aktuelt</td>
<td rowspan="3">Ikke aktuelt</td>
<td rowspan="3">Ikke aktuelt</td>
<td rowspan="3">Ikke aktuelt</td>
</tr>
<tr>
<td>Fakturert salg – belastbart for det nye antallet</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td>Fakturert salg – ikke-belastbart for forskjellen</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td rowspan="2">En faktura korrigeres for å øke det belastbare antallet.</td>
<td>Fakturert salg – tilbakeføring</td>
<td>Valuta for prosjektkontrakt</td>
<td rowspan="5">
<ul>
<li>Tilbakeføring av fakturert salg for milepæl</li>
<li>Endring i milepælstatus fra <strong>Fakturert</strong> til <strong>Klar for faktura</strong></li>
</ul>
</td>
<td rowspan="5">Valuta for prosjektkontrakt</td>
<td rowspan="5">Ikke aktuelt</td>
<td rowspan="5">Ikke aktuelt</td>
</tr>
<tr>
<td>Fakturert salg</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td rowspan="3">En faktura korrigeres for å redusere det belastbare antallet.</td>
<td>Fakturert salg – tilbakeføring</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td>Fakturert salg for det nye antallet</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
<tr>
<td>Ufakturert salg – belastbart for forskjellen</td>
<td>Valuta for prosjektkontrakt</td>
</tr>
</tbody>
</table>
