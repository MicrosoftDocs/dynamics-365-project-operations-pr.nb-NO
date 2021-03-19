---
title: Forespørsel om tidsplan for utgifter til føderale tilskudd
description: Dette emnet gir informasjon om tidsplanen for forespørselen om tidsplan for utgifter til føderale tilskudd.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288976"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Forespørsel om tidsplan for utgifter til føderale tilskudd

[!include [banner](../includes/banner.md)]

I henhold til Office of Management and Budget Circular A-133, er byråer som mottar føderale tilskudd, underlagt revisjonskrav, som også er kjent som enkeltrevisjoner. Revisjonsprosessen brukes til å rapportere om inntektene og utgiftene av føderale tilskudd på en regelmessig basis. En del av rapporten om enkel revisjon omfatter tidsplanen for utgifter til føderale tilskudd (SEFA).

Forespørselen om tidsplanen for utgifter til føderale tilskudd inkluderer tittel og nummer for Catalog of Federal Domestic Assistance (CFDA), tilskuddsnummeret, året for tilskuddet, navnet på det føderale byrået som skaffer midlene, og navnet på mellomleddet. Forespørselen gjelder for en bestemt periode. Denne perioden er vanligvis den samme som regnskapsoppgjørsperioden, som er et regnskapsår.

Forespørselen inkluderer tilskudd som har projeksjonsdatoer i det valgte datointervallet. **Tilskuddsbyrå**-kolonnen i forespørselen viser tilskuddskunden eller, for et tilskudd med mellomledd, tilskuddsbyrået. For et tilskudd med mellomledd, viser **Mellomledd**-kolonnen tilskuddskunden. Hvis tilskuddet ikke er et tilskudd med mellomledd, er **Mellomledd**-kolonnen tom.

## <a name="set-up-the-cfda-clusters"></a>Konfigurere CFDA-klyngene

Du må konfigurere CFDA-klyngene som kan knyttes til CFDA-numre i forespørselen om tidsplan for utgifter til føderale tilskudd.

1. Gå til **Prosjektstyring og regnskap \> Oppsett \> Tilskudd \> Katalog over Federal Domestic Assistance-klynger**.
2. Velg **Ny** for å opprette en CFDA-klynge.
3. Skriv inn navnet på klyngen.
4. Velg **Lagre** for å ta i bruk endringene.

## <a name="set-up-cfda-numbers"></a>Konfigurere CFDA-numre

Du må konfigurere CFDA-numrene som kan legges til for tilskudd og inkluderes i forespørselen om tidsplan for utgifter til føderale tilskudd.

1. Gå til **Prosjektstyring og regnskap \> Oppsett \> Tilskudd \> Katalog over Federal Domestic Assistance-numre**.
2. Velg **Ny** for å opprette et CFDA-nummer.
3. Angi CFDA-nummeret i **Nummer**-kolonnen.
4. Trykk på **Tab**-tasten.
5. Angi CFDA-tittelen i **Beskrivelse**-kolonnen.
6. Trykk på **Tab**-tasten.
7. Valgfritt: I feltet **Programklynge** legger du til riktig CFDA-klynge.
8. Velg **Lagre** for å ta i bruk endringene.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Sett opp tilskudd som skal rapporteres for forespørselen om tidsplan for utgifter til føderale tilskudd

1. Gå til **Prosjektstyring og regnskap \> Tilskudd \> Tilskudd**, og velg et eksisterende tilskudd.
2. På hurtigfanen **Oppsett** i feltet **Katalog over Federal Domestic Assistance**, tilordner du CFFDA-nummeret. CFDA-nummeret på tilskuddet avgjør CFDA-klyngen for rapportering.
3. På hurtigfanen **Kontaktinformasjon** angir du informasjon om giveren ved å følge disse trinnene:

    1. Angi kunden som er ansvarlig for tilskuddet, i feltet **Tilskuddskunde**. Denne informasjonen er kanskje allerede angitt for et eksisterende tilskudd.
    2. Angi om tilskuddskunden er giveren. Hvis tilskuddskunden er giveren, kan du la avmerkingsboksen **Mellomledd** stå tom. Hvis en annen kunde er giveren, og tilskuddskunden er ansvarlig for å bruke og spore pengene, merker du av for **Mellomledd**-boksen.

4. Hvis har merket av for **Mellomledd** i forrige trinn, må du angi kunden som tilbydde tilskuddet, i feltet **Giverbyrå**. Giverbyrået og tilskuddskunden kan ikke være samme kunde.

Her er et eksempel på et tilskudd med mellomledd:

Den føderale føderale regjeringen finansierte et infrastrukturprosjekt for en delstat. Den føderale regjeringen ga pengene til delstaten for forbruk. I dette tilfellet er det den føderale regjeringen som er giverbyrået, og delstaten som er tilskuddskunden.

> [!NOTE] 
> Første gang du aktiverer funksjonen, blir opprinnelige CFDA-numre angitt ved hjelp av eksisterende numre på tilskudd.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Utelate tilskudd fra SEFA-rapportering basert på tilskuddstypen

1. Gå til **Prosjektstyring og regnskap \> Oppsett \> Tilskudd \> Tilskuddstyper**.
2. På hurtigfanen **Standardinformasjon** merker du av for **Utelat fra utgiftsplan for føderale tilskudd**.
3. Velg **Lagre** for å ta i bruk endringene.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Kjøre forespørselen om tidsplan for utgifter til føderale tilskudd

1. Gå til **Prosjektstyring og regnskap \> Forespørsler og rapporter \> Tilskuddsforespørsel \> Tidsplan for utgifter til føderale tilskudd**.
2. Følg fremgangsmåten nedenfor i **Parametere**-delen:

    1. I **Datointervall**-feltet velger du koden for datointervallet. Du kan også definere datointervallet i feltene **Fra dato** og **Til dato**.
    2. Valgfritt: Hvis du bare vil ta med fakturerte transaksjoner som inntekt i forespørselen, setter du alternativet **Inkludert bare fakturert inntekt** til **Ja**.

## <a name="columns"></a>Kolonner

Forespørselen om tidsplan for utgifter til føderale tilskudd inkluderer følgende kolonner:

- Navn på katalog over Federal Domestic Assistance-klynger
- Giverbyrå
- Mellomledd
- Navn på tilskudd
- Tilskudds-ID
- Tilskuddssøknads-ID
- Katalog over Federal Domestic Assistance
- Kvitteringer
- Utgifter


[!INCLUDE[footer-include](../includes/footer-banner.md)]