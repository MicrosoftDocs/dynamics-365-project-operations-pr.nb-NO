---
title: Nyheter eller endringer i Project Operations i september 2021 for lagerførte/produksjonsbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for lagerførte/produksjonsbaserte scenarioer fra september 2021.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 1e99471b4338209c1f7fe411084d1745d74b2d2c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916530"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Nyheter eller endringer i Project Operations i september 2021 for lagerførte/produksjonsbaserte scenarioer

_**Gjelder:** Project Operations for lagerførte/produksjonsbaserte scenarioer_

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.21
 
## <a name="quality-updates"></a>Kvalitetsoppdateringer

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
|---|---|---|
| Prosjektstyring og regnskap | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Hvis du gir innkjøpslederrollen tilgang til én juridisk enhet, får den også tilgang til alle prosjekter i alle juridiske enheter. |
| Prosjektstyring og regnskap | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Det oppstår et avrundingsproblem med merverdiavgiften (mva) når en kreditnota utlignes mot en opprinnelig prosjektfaktura. |
| Prosjektstyring og regnskap | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Bruk et alternativt prosjektbudsjett til budsjettbekreftelse. |
| Prosjektstyring og regnskap | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Prisgruppen **Salgspris – time** beregnes ikke på arbeidsnedbrytningsstrukturen for prosjekttilbud. |
| Prosjektstyring og regnskap | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Estimering av eliminering mislykkes når funksjonen **Aktiver estimatberegning for prosjektkontraktvaluta** er aktivert. |
| Prosjektstyring og regnskap | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorisering av merverdiavgift etter antall legges til salgsprisbeløpet når use tax brukes på mva-gruppen i prosjektutgiftsjournalen. |
| Prosjektstyring og regnskap | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Betinget avgift beregnes ikke riktig for den siste betalingen når leverandøroppbevaring og forskuddsbetaling brukes på bestillingsfakturaer. |
| Prosjektstyring og regnskap | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Justeringssporing fungerer ikke for journaler for startsaldo. |
| Prosjektstyring og regnskap | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Tildeling av prosjektbudsjettendring etter periode** deles på tvers av alle budsjettperioder. Oppføringen fjernes ikke etter at tildelingen er sendt inn. |
| Prosjektstyring og regnskap | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | VIA-posteringer (varer i arbeid) i økonomimodulen har et feil beløp. |
| Prosjektstyring og regnskap | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Godkjenning av prosjekttimejournalen fungerer ikke. |
| Prosjektstyring og regnskap | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Salgsprisen for prosjektjustering oppdateres ikke med indirekte kostnader når finansieringsgrensen er umerket. |
| Prosjektstyring og regnskap | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Et varebehov kan ikke opprettes når salgstabellhodet er fakturert og støttebestillingen for eksisterende linjer er fullført. |
| Prosjektstyring og regnskap | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Tilbakeholdelsesbeløpet for en faktureringsregel som har en milepæl for et annet prosjekt, posteres ikke i den tilsvarende prosjekt-ID-en som ble valgt for milepælen. Det posteres i stedet i det første prosjektet. |
| Prosjektstyring og regnskap | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Når du velger **Finansdimensjonssett** i et fakturaforslag, oppstår følgende feil: «Kan ikke bruke objekttypen Dynamics.AX.Application.FormIntControl som Dynamics.AX.Application.FormStringControl.» |
| Prosjektstyring og regnskap | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | **Prosjektfaktura**-rapporten hopper over linjer. |
| Prosjektstyring og regnskap | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Det oppstår en feil når du beregner kostnadskontrollen for et investeringsprosjekt. |
| Prosjektstyring og regnskap | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metoden **ProjTable::InitFromCustTable - canDeletePostalAddress** forårsaker et ytelsesproblem. |
| Prosjektstyring og regnskap | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Feilmeldingen skal være klarere enn «Uventet feil». |
| Prosjektstyring og regnskap | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Den satsvise jobben for postering av prosjektfaktura behandler og posterer fakturaforslaget selv om fakturalinjene ikke er generert. |
| Prosjektstyring og regnskap | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Det oppstår et avrundingsproblem når lisenskonfigurasjonsnøkkelen for offentlig sektor er deaktivert. Feil kostnad eller salgspris genereres i timeregistreringstimene for kontrakter som har flere finansieringskilder. |
| Prosjektstyring og regnskap | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Prosjektsalgsprisen i en fakturert prosjektbestilling beregnes feil når salgsprismodellen er **Dekningsgrad**. |
| Prosjektstyring og regnskap | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Systemet tar ikke hensyn til de aktive dagene i mellom ved beregning av effektiv arbeidssats for en ansatt. |
| Prosjektstyring og regnskap | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Det oppstår en posteringsfeil i konsernintern timeregistrering på grunn av følgende valideringsfeil: «Ingen handelspartner er konfigurert for juridisk enhet.» |
| Prosjektstyring og regnskap | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Beskrivelsen fra en bestilling som har en utgiftskategori, hentes ikke i den posterte prosjekttransaksjonslisten. |
| Prosjektstyring og regnskap | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Det oppstår en feil konvertering i varejournaler som posteres i et prosjekt. |
| Prosjektstyring og regnskap | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Du kan bekrefte en bestilling selv om finansieringsgrensen er overskredet. |
| Prosjektstyring og regnskap | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Delen **Rettelse / Annuller faktura** i en fritekstfaktura forsvinner når du velger en prosjekt-ID. |
| Prosjektstyring og regnskap | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Det oppstår ytelsesproblemer når et prosjektfakturaforslag posteres fra en prosjektsalgsordre som omfatter en lagerført vare. |
| Prosjektstyring og regnskap | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Du kan ikke postere prosjektinnkjøpsfakturaer fordi følgende feil oppstår: «Funksjonen AccDistProcessorProjectExtension.createForProjectRevenueLine er kalt på feil måte.» |
| Prosjektstyring og regnskap | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Opprettelse av satsvise jobber for prosjektestimat er oppdatert for å støtte kjøring av flere deloppgaver. |
| Prosjektstyring og regnskap | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Statusen for en timeregistrering kan ikke oppdateres til **Utkast** når arbeidsflyten sitter fast i tilstanden **Annullert**. |
| Prosjektstyring og regnskap | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Oppbevaringsbeløp beregnes ikke i fakturaforslaget for kreditnota hvis det finnes flere linjer. |
| Prosjektstyring og regnskap | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Når du prøver å endre beløpet i en generert faktura fra en bestilling, får du følgende feil: «Transaksjoner på bilag stemmer ikke per XX/XX/XXXX.» (regnskapsvaluta: 0,00 – rapporteringsvaluta: 0,01)». |
| Prosjektstyring og regnskap | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Det oppstår et ytelsesproblem når et prosjektfakturaforslag posteres i satsvis modus, på grunn av sammenføyning med **GeneralJournalAccountEntry**. |
| Prosjektstyring og regnskap | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Det oppstår ytelsesproblemer når en timeregistrering posteres. |
| Prosjektstyring og regnskap | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Kostnadsestimathierarkiet i arbeidsnedbrytningsstrukturen er ikke riktig justert etter at alle oppgavene er utvidet, eller etter at en enkeltoppgave er utvidet manuelt. |
| Prosjektstyring og regnskap | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Excel-malen for prosjekttilbud kan ikke legges til på menyen **Åpne i Excel**. |
| Prosjektstyring og regnskap | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Nummeret for avgiftsfritak for en juridisk enhet vises ikke på utskriften av prosjektfakturaen. |
| Prosjektstyring og regnskap | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Ingen økonomiske data blir oppdatert i lagerenhetsfeilen når et prosjekt justeres i forhold til kredittlinjer. |
| Prosjektstyring og regnskap | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Etter at du har brukt KB 461935, kan du ikke postere estimater hvis du bytter til sammenhengende nummerserier. |
| Prosjektstyring og regnskap | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** gjør at mobilappen Project-timeregistrering for Android slutter å svare. |
| Prosjektstyring og regnskap | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Verdien for tilbakeført VIA fra en fakturapostering er forskjellig fra den opprinnelige posterte VIA-verdien fra tidsoppføringen. |
| Prosjektstyring og regnskap | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | I tilfeller med brukte honorarer er ikke transaksjonene i et bilag i balanse når fakturert omsetning for et prosjekt posteres. |
| Prosjektstyring og regnskap | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Når funksjonen **Aktiver ytelsesforbedring for prosjektressursplanlegging** er aktivert, blir ikke desimalverdier riktig avrundet for ressurstilgjengelighet og -kapasitet. |
| Prosjektstyring og regnskap | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Når funksjonen **Opprett prosjektestimater ved hjelp av flere satsvise oppgaver** er aktivert, fungerer oppretting av estimater i en satsvis jobb med flere deloppgaver bare for gjeldende periode. |
| Reise og utgift | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | En policy for reiserekvisisjon ignoreres, og arbeidsflyten godkjennes uten feil. |
| Reise og utgift | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Mobilutgiftsappen lagrer ikke følgende informasjon på utgiftslinjen:</p><ul><li>Prosjekt-ID-en</li><li>Hvorvidt utgiften er fakturerbar</li><li>Aktivitetsnummeret</li></ul> |
| Reise og utgift | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Feltet **Vedlagte kvitteringer** er satt til **Ja** selv om ingen kvitteringer er lagt ved utgiftslinjen. |
| Reise og utgift | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Det oppstår en feil når du endrer utgiftskategorien til **Personlig**. |
| Reise og utgift | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Du kan ikke legge ved en kvittering og redigere den overordnede utgiften etter at en kredittkorttransaksjon er delt opp til en personlig utgift. |
| Reise og utgift | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Utgiftspolicyen for konserninterne transaksjoner som har en prosjekt-ID, fungerer ikke som den skal. |
| Reise og utgift | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Posteringsdatoinformasjonen mangler for posterte utgiftsrapporter. |
| Reise og utgift | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Det er problemer med betalingsmetode i mobilappen for utgifter. |
| Reise og utgift | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | En reiserekvisisjon som er opprettet for én arbeider, kan brukes for en annen arbeiders utgiftsrapport før delegeringsdatoen. |
| Reise og utgift | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Når du oppretter en utgift, blir ikke endring av finansdimensjonsverdier riktig oppdatert på regnskapsdistribusjonsnivået i arbeidsområdet **Reiseregning og utlegg**. |
| Reise og utgift | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Godkjenningsstatusen for hovedutgiftslinjen synkroniseres ikke med godkjenningsstatusen for den spesifiserte linjearbeidsflyten. |
| Reise og utgift | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Det oppstår en feil hvis du posterer en utgiftsrapport og skatterefusjon er aktivert. |
| Reise og utgift | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | En representant kan ikke slette utgiftsdokumenter for en avsluttet ansatt. |
| Reise og utgift | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Det tar lengre tid enn forventet å slette en utgiftslinje, og ytelsen påvirkes. |
| Reise og utgift | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** forårsaker en frittstående **TaxUncommitted**-oppføring siden bare **SourceDocumentLine** slettes. |
| Reise og utgift | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** overholder ikke **trvExpTrans.ReferenceDataAreaId** for å opprette den nye nummerserien. |

## <a name="regulatory-updates"></a>Forskriftsmessige oppdateringer

Hvis du vil ha informasjon om forskriftsmessige oppdateringer for økonomi- og driftsapper, kan du se [Forskriftsmessige oppdateringer](/dynamics365/finance/localizations/regulatory-updates). Du kan også logge på Microsoft Dynamics Lifecycle Services (LCS) og bruke verktøyet Problemsøk til å vise de planlagte forskriftsmessige oppdateringene. Med Problemsøk kan du søke etter land eller område, funksjonstype og utgivelse.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
