---
title: Oversikt over faktiske verdier
description: Denne emnet gir informasjon om faktiske verdier for prosjekter.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73f1b14bbb4cc53111a1b3a93756a86db04475ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014668"
---
# <a name="actuals-overview"></a>Oversikt over faktiske verdier

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Faktiske verdier er mengden arbeid som er fullført på et prosjekt. Faktiske verdier for prosjekter kan spores tilbake til kildedokumentene. Disse kildedokumentene inneholder time-, utgifts- og journaloppføringer, og også fakturaer.

![Hvordan faktiske verdier for prosjekter spores i kildedokumenter](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Sende inn en tidsoppføring

Når en tidsoppføring sendes til et prosjekt som er tilordnet en kontraktlinje for tid og materialer i PSA, opprettes det to journallinjer. Den ene linje gjelder kostnad, og den andre linjen er for ikke-fakturert salg. Når en tidsoppføring sendes til et prosjekt som er tilordnet en kontraktlinje for fast pris, opprettes det en journallinje bare for kostnad. 

Logikk for angivelse av standardpriser finnes på journallinjen. Alle feltverdiene fra en tidsoppføring kopieres til journallinjen. Disse feltene inneholder transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet i den aktuelle prislisten. 

Feltene som påvirker standardpriser, for eksempel **Rolle** og **Organisasjonsenhet**, fører til at en passende pris registreres som standard på journallinjen. Hvis du legger til et egendefinert felt for tidsoppføringen, og du vil at feltverdien skal overføres til faktiske verdier, oppretter du feltet på den faktiske enheten og bruker felttilordninger til å kopiere feltet fra tidsoppføringen til den faktiske verdien.

## <a name="submitting-an-expense-entry"></a>Sende en utgiftsoppføring

Når en utgiftsoppføring sendes til et prosjekt som er tilordnet en kontraktlinje for tid og materialer i PSA, opprettes det to journallinjer. Den ene linje gjelder kostnad, og den andre linjen er for ikke-fakturert salg. Når en utgiftsoppføring sendes til et prosjekt som er tilordnet en kontraktlinje for fast pris, opprettes det en journallinje bare for kostnad.

Logikk for angivelse av standardpriser for utgifter er basert på utgiftskategorien som er valgt på siden **Utgiftsoppføring**. Både transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet brukes til å bestemme den aktuelle prislisten. For selve prisen blir imidlertid beløpet som brukeren angav, angitt direkte på de relaterte utgiftsjournallinjene for kostnad og salg som standard.

I den gjeldende versjonen av PSA er kategoribasert oppføring av standard priser per enhet på utgiftsoppføringer ikke tilgjengelig.

## <a name="using-entry-journals-to-record-costs"></a>Bruke oppføringsjournaler til å registrere kostnader

I PSA gir oppføringsjournaler deg tilgang til å registrere kostnad eller omsetninger i transaksjonsklassene for materialer, gebyr, tid, utgift eller avgift. En journal har et hode, linjer og en **bekreftelseshandling**. Her er noen scenarioer der du kan bruke en journal:

- Du må registrere faktiske kostnader og salg for materialer på et prosjekt.
- Du må flytte de faktiske transaksjonstransaksjonene fra et annet system til PSA.
- Du må registrere kostnader som har oppstått i et annet system, for eksempel innkjøps- eller underleveransekostnader.

> [!IMPORTANT]
> Bruk av oppføringsjournaler til å opprette faktiske verdier bør bare utføres av en bruker som er helt oppmerksom på den regnskapsmessige innvirkningen de faktiske verdiene har på prosjektet. Dette skyldes at programmet ikke validerer journallinjetypen eller den relaterte prissettingen som er angitt på journallinjen. På grunn av virkningen av denne journaltypen må du være forsiktig med hvem som gis tilgang til å opprette oppføringsjournaler.     


## <a name="recording-actuals-based-on-project-events"></a>Registrere faktiske verdier basert på prosjekthendelser

PSA registrerer de finansielle transaksjonene som inntreffer under et prosjekt. Disse transaksjonene registreres som **faktiske verdier**. Følgende tabeller viser de forskjellige typene faktiske verdier som opprettes, avhengig av om prosjektet er et tids-og-materiale-prosjekt eller et fastprisprosjekt, er i forsalgsfasen eller er et internt prosjekt.

**Ressursen tilhører samme organisasjonsenhet som prosjektets kontraktenhet**

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

**Ressursen tilhører en annen organisasjonsenhet enn prosjektets kontraktenhet**

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