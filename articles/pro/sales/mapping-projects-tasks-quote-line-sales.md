---
title: Tilordne prosjekter og oppgaver til en prosjektbasert tilbudslinje
description: Dette emnet gir informasjon om hvordan du tilordner prosjekter og oppgaver til en prosjektbasert oppgavelinje.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 871d323136cd982bd48ed9aa2b9c34017951d2d8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130725"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Tilordne prosjekter og oppgaver til en prosjektbasert tilbudslinje

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

På prosjektbaserte tilbudslinjer kan du tilordne de spesifikke oppgavene til et prosjekt som allerede er knyttet til en tilbudslinje.

Når du tilordner oppgaver til en tilbudslinje, vil følgende elementer du har definert i tilbudslinjen, bare gjelde for disse oppgavene:

- Faktureringsmetode
- Alternativer for belastbarhet
- Må ikke overskrides-grenser
- Kunder

Du kan for eksempel ha et prosjekt der én fase er en fast pris, og alle de andre fasene er tid og materialer. I dette tilfellet kan du knytte den første fasen og alle underordnede oppgaver til tilbudslinjen for fasen med fast pris som faktureringsmetode. Du kan deretter knytte alle de andre fasene til tilbudslinjen som er basert på tid og materialer.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Knytte oppgaver til prosjektbaserte tilbudslinjer

Du kan knytte oppgaver til tilbudslinjer fra følgende plasseringer:

- **Prosjekt**-siden > **Oppgavefakturering**-fanen (valgtritt)
- **Tilbudslinje**-siden > **Belastbare oppgaver**-fanen 

### <a name="from-the-project-page"></a>Fra prosjektsiden

**Prosjekt**-siden gir den optimale opplevelsen for tilordning av oppgaver til tilbudslinjer. Du kan bruke denne siden til å velge flere oppgaver og knytte til alle disse, samt underordnede oppgaver, til den valgte tilbudslinjen.

1. I kategorien **Generelt** for en prosjektbasert tilbudslinje, kontrollerer du at **Prosjekt**-feltet er fylt ut.
2. I feltet **Inkluderte oppgaver** velger du **Bare valgte oppgaver**.
3. Lagre den prosjektbaserte tilbudslinjen. Når skjemaet oppdateres, vises kategorien **Belastbare oppgaver**.
4. I kategorien **Generelt** velger du koblingen for prosjektet fra **Prosjekt**-feltet.
5. På siden **Prosjekr** velger du kategorien **Oppgavefakturering**.
6. I det andre rutenettet, som gjelder for oppgavespesifikke faktureringsoppsett, velger du én eller flere oppgaver, og deretter velger du **Tilknytt tilbudslinjer**.
7. På dialogsiden som vises, velger du en tilbudslinje som viser prosjektbaserte tilbudslinjer i tilbudet.
8. I feltet **Faktureringstype** angir du om disse oppgavene er belastbare eller ikke-belastbare.
9. Merk av i avmerkingsboksen for å angi om tilknytningen skal inkludere underordnede oppgaver for de valgte oppgavene. Hvis du merker av i boksen, knyttes underordnede oppgaver for de valgte oppgavene til tilbudslinjen.
10. Velg **OK** for å lukke dialogboksen.

### <a name="from-the-quote-line-page"></a>Fra tilbudslinjesiden

Du kan knytte prosjektoppgaver til tilbudslinjer fra kategorien **Belastbare oppgaver** på **Tilbudslinje**-siden.

>[!NOTE]
>Det optimale stedet for å knytte prosjektoppgaver til tilbudslinjer er på **Oppgavefakturering**-fanen på **Prosjekt**-siden. Hvis du knytter oppgaver fra kategorien **Belastbare oppgaver** på **Tilbudslinje**-siden, må du knytte til hvert prosjekt manuelt.

1. I kategorien **Generelt** for en prosjektbasert tilbudslinje, kontrollerer du at et prosjekt er valgt i **Prosjekt**-feltet.
2. I feltet **Inkluderte oppgaver** velger du **Bare valgte oppgaver**.
3. Lagre den prosjektbaserte tilbudslinjen. Når skjemaet oppdateres, vises kategorien **Belastbare oppgaver**.
4. I kategorien **Belastbare oppgaver** velger du **Legg til en tilbudslinjeoppgave**.
5. På siden **Tilbudslinjeoppgave**, i **Oppgaver**-feltet velger du oppgaven, og i **Faktureringstype**-feltet velger du **Lagre**. 
6. Lukk siden. Den valgte oppgaven er nå knyttet til tilbudslinjen.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Oppheve tilknytning av oppgaver fra prosjektbaserte tilbudslinjer

### <a name="from-the-project-page"></a>Fra prosjektsiden

Denne metoden gir den mest optimale opplevelsen for oppheving av tilknytning av oppgaver fra tilbudslinjer. Du kan velge flere oppgaver og oppheve tilknytningen for alle disse, samt underordnede oppgaver, fra den valgte tilbudslinjen.

1. I kategorien **Generelt** for en prosjektbasert tilbudslinje velger du prosjektkoblingen i **Prosjekt**-feltet.
2. På siden **Prosjekr** velger du kategorien **Oppgavefakturering**.
3. I det andre rutenettet, som gjelder for oppgavespesifikke faktureringsoppsett, velger du én eller flere oppgaver, og deretter velger du **Opphev tilknytning av tilbudslinjer**.
4. På dialogsiden som vises, velger du en tilbudslinje.
5. Merk av i avmerkingsboksen for å angi om tilknytningen også skal fjernes fra underordnede oppgaver for de valgte oppgavene. Hvis du merker av i boksen, oppheves også tilknytningen for underordnede oppgaver for de valgte oppgavene til tilbudslinjen.
6. Velg **OK**. Du får en advarselsmelding om at hvis du fjerner denne tilknytningen, kan eventuelle faktiske verdier som tidligere er registrert for oppgaven, tilbakeføres. 
7. Velg **OK** for å fortsette og fjerne tilknytningen mellom oppgaven og den prosjektbaserte tilbudslinjen.

### <a name="from-the-quote-line-page"></a>Fra tilbudslinjesiden

Du kan oppheve tilknytning av prosjektoppgaver til tilbudslinjer fra kategorien **Belastbare oppgaver** på **Tilbudslinje**-siden.

1. I kategorien **Belastbare oppgaver** velger du **Slett en tilbudslinjeoppgave**.
2. Velg **OK**. Du får en advarselsmelding om at hvis du fjerner denne tilknytningen, kan eventuelle faktiske verdier som tidligere er registrert for oppgaven, tilbakeføres. 
3. Velg **OK** for å fortsette og fjerne tilknytningen mellom oppgaven og den prosjektbaserte tilbudslinjen.

>[!NOTE]
> Denne prosedyren sletter ikke oppgaven fra prosjektet. Den fjerner bare oppgavetilknytningen fra den prosjektbaserte tilbudslinjen.
