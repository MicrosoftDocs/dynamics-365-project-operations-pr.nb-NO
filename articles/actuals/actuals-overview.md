---
title: Faktiske verdier
description: Denne emne inneholder informasjon om hvordan du arbeider med faktiske verdier i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a086fe0be67c21ed73793b6f3b58b47ad08eaa4e8a4c98870b4b2264562e3dce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991813"
---
# <a name="actuals"></a>Faktiske verdier 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Faktiske verdier representerer den gjennomgåtte og godkjente økonomiske og planlagte fremdriften for et prosjekt. De opprettes som et resultat av godkjenning av tid, utgifter, materialbruksoppføringer og loggoppføringer og fakturaer.

## <a name="journal-lines-and-time-submission"></a>Journallinjer og tidssending

Hvis du vil ha mer informasjon om tidsregistrering, kan du se [Oversikt over tidsregistrering](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Tid og materialer

Når en tidsregistrering som er sendt, er koblet til et prosjekt som er tilordnet en kontraktlinje for tid og materialer, oppretter systemet to journallinjer, én for kostnad og én for ufakturert salg.

### <a name="fixed-price"></a>Fast pris

Når en tidsoppføring som er sendt, kobles til et prosjekt som er tilordnet en kontraktlinje for fast pris, oppretter systemet én journallinje for kostnad.

### <a name="default-pricing"></a>Standardprising

Logikken for oppretting av standardpriser finnes på journallinjen. Feltverdiene fra tidsoppføringen kopieres til journallinjen. Disse verdiene inneholder transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet i den aktuelle prislisten.

Feltene som påvirker standardpriser, for eksempel **Rolle** og **Ressursenhet**, brukes til å bestemme passende pris på journallinjen. Du kan legge til et egendefinert felt for tidsoppføringen. Hvis du vil at feltverdien skal overføres til faktiske verdier, oppretter du feltet i tabellene **Faktiske verdier** og **Journallinje**. Bruk egendefinert kode til å overføre den valgte feltverdien fra Tidsoppføring til Faktiske verdier via journallinjen ved hjelp av transaksjonsopphav. Hvis du vil ha mer informasjon om transaksjonsopphav og tilkoblinger, kan du se [Koble faktiske verdier til opprinnelige oppføringer](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Journallinjer og sending av grunnleggende utgifter

Hvis du vil ha mer informasjon om utgiftsregistrering, kan du se [Oversikt over utgifter](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Tid og materialer

Når en grunnleggende utgiftsregistrering som er sendt, er koblet til et prosjekt som er tilordnet en kontraktlinje for tid og materialer, oppretter systemet to journallinjer, én for kostnad og én for ufakturert salg.

### <a name="fixed-price"></a>Fast pris

Når en innsendt enkel utgiftsoppføring er knyttet til et prosjekt som er tilordnet en kontraktlinje for fast pris, oppretter systemet én journallinje for kostnad.

### <a name="default-pricing"></a>Standardprising

Logikken for å angi standardpriser for utgifter er basert på utgiftskategorien. Både transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet brukes til å bestemme den aktuelle prislisten. Feltene som påvirker standardpriser, for eksempel **Transaksjonskategori** og **Enhet**, brukes til å bestemme passende pris på journallinjen. Dette fungerer imidlertid bare når prismodellen i prislisten er **Pris per enhet**. Hvis prismetoden er **Kostpris** eller **Påslag over kostnad**, blir prisen som angis når utgiftsoppføringen opprettes, brukt til kostnad, og prisen på salgsjournallinjen beregnes basert på prismetoden. 

Du kan legge til et egendefinert felt i utgiftsoppføringen. Hvis du vil at feltverdien skal overføres til faktiske verdier, oppretter du feltet i tabellene **Faktiske verdier** og **Journallinje**. Bruk egendefinert kode til å overføre den valgte feltverdien fra Tidsoppføring til Faktiske verdier via journallinjen ved hjelp av transaksjonsopphav. Hvis du vil ha mer informasjon om transaksjonsopphav og tilkoblinger, kan du se [Koble faktiske verdier til opprinnelige oppføringer](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Innsending av journallinjer og materialbrukslogg

Hvis du vil ha mer informasjon om utgiftsregistrering, kan du se [Logg over materialbruk](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Tid og materialer

Når en innsendt loggoppføring for materialbruk er koblet til et prosjekt som er tilordnet en kontraktlinje for tid og materiell, opprettes det to journallinjer, én for kostnad og én for ikke-fakturert salg.

### <a name="fixed-price"></a>Fast pris

Når en innsendt loggoppføring for materialbruk er knyttet til et prosjekt som er tilordnet en kontraktlinje for fast pris, oppretter systemet én journallinje for kostnad.

### <a name="default-pricing"></a>Standardprising

Logikken for å angi standardpriser for materiale er basert på produkt- og enhetskombinasjonen. Både transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet brukes til å bestemme den aktuelle prislisten. Feltene som påvirker standardpriser, for eksempel **Produkt-ID** og **Ressursenhet**, brukes til å bestemme passende pris på journallinjen. Dette fungerer imidlertid bare for katalogprodukter. Når det gjelder produkter som ikke er i katalogen, brukes prisen som angis når oppføringen i materialbruksloggen opprettes, for kostnad og salgspris på journallinjene. 

Du kan legge til et egendefinert felt i oppføringen **Logg over materialbruk**. Hvis du vil at feltverdien skal overføres til faktiske verdier, oppretter du feltet i tabellene **Faktiske verdier** og **Journallinje**. Bruk egendefinert kode til å overføre den valgte feltverdien fra Tidsoppføring til Faktiske verdier via journallinjen ved hjelp av transaksjonsopphav. Hvis du vil ha mer informasjon om transaksjonsopphav og tilkoblinger, kan du se [Koble faktiske verdier til opprinnelige oppføringer](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Bruk oppføringsjournaler til å registrere kostnader

Du kan bruke oppføringsjournaler til å registrere kostnad eller omsetning i transaksjonsklassene for materialer, gebyr, tid, utgift eller avgift. Journaler kan brukes til følgende formål:

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
