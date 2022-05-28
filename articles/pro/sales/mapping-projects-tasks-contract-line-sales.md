---
title: Tilordne prosjekter og oppgaver til en prosjektbasert kontraktlinje – Lite
description: Dettee emnet inneholder informasjon om hvordan du legger til og fjerner prosjekter og oppgaver på en kontraktlinje.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: da6017a6bbf138a4d30f1cd29b5b00a520e6990f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600248"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Tilordne prosjekter og oppgaver til en prosjektbasert kontraktlinje 

_**Gjelder for:** Lite-distribusjon – avtale til proformafakturering, Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

På prosjektbaserte kontraktlinjer kan du tilordne bestemte oppgaver i et prosjekt til kontraktlinjen.

Når du tilordner bestemte oppgaver til en kontraktlinje, vil faktureringsmetoden, alternativer for belastbarhet, Må ikke overskrides-grenser og kundene som er definert på kontraktlinjen, bare gjelde for disse spesifikke oppgavene.

Hvis du har et scenario der én fase av et prosjekt, for eksempel prototypefasen, er fast pris og alle de andre fasene er tid og materiell, vil du kunne knytte prototypefasen og alle tilknyttede underordnede aktiviteter til kontraktlinjen for denne fasen med en faktureringsmetode med fast pris.

Alle de andre fasene i prosjektets arbeidsnedbrytningsstruktur (WBS) kan tilknyttes kontraktlinjen for tid og materialer.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Knytte oppgaver til prosjektbaserte kontraktlinjer

Oppgaver kan knyttes til kontraktlinjer fra kategorien **Belastbare oppgaver** på siden **Kontraktlinje** eller fra kategorien **Oppgavefakturering** på siden **Prosjekt**.

### <a name="from-the-contract-line-page"></a>Fra siden Kontraktlinje

Fullfør fremgangsmåten nedenfor for å knytte prosjektaktiviteter til kontraktlinjen fra kategorien **Belastbare oppgaver** på siden **Kontraktlinje**.

1. I kategorien **Generelt** på en prosjektbasert kontraktlinje kontrollerer du at **Prosjekt**-feltet er utfylt.
2. I feltet **Inkluderte oppgaver** velger du **Bare valgte oppgaver**.
3. Lagre endringene. Skjemaet blir oppdatert, og kategorien **Belastbare oppgaver** vil være synlig.
4. Velg kategorien **Belastbare oppgaver**, og i underrutenettet velger du **Legg til en kontraktlinjeoppgave**.
5. På siden **Kontraktlinjeoppgaver**, i rullegardinlisten **Oppgaver**, velger du oppgaven. 
6. Angi informasjon i **Faktureringstype**-feltet, og velg deretter **Lagre og Lukk**. Den valgte aktiviteten er knyttet til kontraktlinjen.

> [!NOTE]
> Dette er ikke den mest optimale opplevelsen for tilordning av prosjektoppgaver til kontraktlinjer. Hvert prosjekt må tilknyttes manuelt i denne opplevelsen. Den foretrukkede måten er å gå fra kategorien **Oppgavefakturering** på siden **Prosjekt**.

### <a name="from-the-project-page"></a>Fra prosjektsiden

Dette er den optimale metoden for å knytte oppgaver til kontraktlinjer. Du kan velge flere oppgaver og knytte alle de underordnede oppgavene til den valgte kontraktlinjen. Fullfør fremgangsmåten nedenfor for å knytte aktiviteter til kontraktlinjen fra **Prosjekt**-siden.

1. I kategorien **Generelt** på en prosjektbasert kontraktlinje kontrollerer du at **Prosjekt**-feltet er utfylt.
2. I feltet **Inkluderte oppgaver** velger du **Bare valgte oppgaver**.
3. Lagre den prosjektbaserte kontraktlinjen. Skjemaet blir oppdatert, og kategorien **Belastbare oppgaver** vil være synlig. Dette er bare for godkjenningsformål.
4. I kategorien **Generelt** på den prosjektbaserte kontraktlinjen i feltet **Prosjekt** velger du prosjektkoblingen.
5. På **Prosjekt**-siden velger du kategorien **Faktureringsoppsett for oppgave**.
6. Det finnes to rutenett. Ett rutenett er for kontraktlinjer som gjelder for hele prosjektet. Det andre rutenettet gjelder for faktureringsoppsett for en bestemt oppgave. Velg én eller flere oppgaver i det andrerute nettet, og velg deretter **Tilknytt kontraktlinjer**.
7. På dialogsiden som åpnes, velger du en kontraktlinje fra rullegardinlisten.
8. Bruk rullegardinlisten **Faktureringstype** for å merke oppgavene som belastbare eller ikke-belastbare.
9. Merk av i avmerkingsboksen for å angi om tilknytningen også skal inkludere underordnede oppgaver for de valgte oppgavene. Hvis du merker av i boksen, blir også de underordnede oppgavene for de valgte oppgavene tilknyttet til kontraktlinjen.
10. Velg **OK** for å lukke dialogboksen.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Fjerne tilknytning til oppgaver fra prosjektbaserte kontraktlinjer

### <a name="from-the-contract-line-page"></a>Fra kontraktlinjesiden

Fullfør fremgangsmåten nedenfor for å fjerne tilknytningen til prosjektaktiviteter fra kontraktlinjen i kategorien **Belastbare oppgaver** på siden **Kontraktlinje**.

1. I kategorien **Belastbare oppgaver** velger du **Slett en kontraktlinjeoppgave**.
2. En varselmelding angir at fjerning av denne tilordningen kan føre til at eventuelle faktiske verdier som tidligere er registrert på oppgaven, blir annullert. Velg **OK** i dialogboksen for å fjerne tilknytningen mellom oppgaven og den prosjektrelaterte kontraktlinjen. 

> [!NOTE]
> Dette sletter ikke oppgaven fra prosjektet. I stedet fjernes oppgavetilknytningen fra den prosjektbaserte kontraktlinjen.

### <a name="from-the-project-page"></a>Fra prosjektsiden

Dette er ikke den mest optimale opplevelsen for fjerning av tilordning til oppgaver fra kontraktlinjer. Du kan velge flere oppgaver og fjerne tilknytning til alle og de underordnede oppgavene fra den valgte kontraktlinjen. Fullfør fremgangsmåten nedenfor for å fjerne oppgavene fra kontraktlinjen.

1. Fra kategorien **Generelt** på den prosjektbaserte kontraktlinjen i feltet **Prosjekt** klikker du på koblingen for prosjektet.
2. På **Prosjekt**-siden velger du kategorien **Faktureringsoppsett for oppgave**.
3. Det finnes to rutenett på siden. Ett rutenett er for kontraktlinjer som gjelder for hele prosjektet, og det andre for et aktivitetsspesifikt faktureringsoppsett. Velg én eller flere oppgaver i det andre rutenettet, og velg deretter **Opphev tilknytning til kontraktlinjer**.
4. På dialogsiden som åpnes, velger du en kontraktlinje fra rullegardinlisten.
5. Merk av i avmerkingsboksen for å angi om tilknytningen også skal fjernes fra eventuelle underordnede oppgaver for de valgte oppgavene. Hvis du merker av i boksen, vil også fjerne tilknytningen av de underordnede oppgavene til de valgte oppgavene fra kontraktlinjen.
6. Velg **OK**. En varselmelding angir at fjerning av denne tilordningen kan føre til at eventuelle faktiske verdier som tidligere er registrert på oppgaven, blir annullert. Velg **OK** i advarselsdialogboksen for å fjerne tilknytningen mellom oppgaven og den prosjektrelaterte kontraktlinjen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
