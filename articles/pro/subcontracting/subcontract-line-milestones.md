---
title: Milepæler for underkontraktlinje
description: Dette emnet forklarer hvordan du oppretter og vedlikeholder en milepælbasert fakturaplan for en underleverandør.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d1c30f48e0d43aa55e2c1650637f7f102fb200de
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579134"
---
# <a name="subcontract-line-milestones"></a>Milepæler for underkontraktlinje

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

I Dynamics 365 Project Operations kan en underkontraktlinje med en faktureringsmetode med fast pris angi en milepælbasert fakturaplan med leverandøren.

Milepæler for fakturering av leverandører kan genereres automatisk ved hjelp av en fast frekvens, eller du kan opprette dem manuelt.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Opprett en milepælbasert fakturaplan for en underkontraktlinje automatisk

Fullfør fremgangsmåten nedenfor for automatisk å generere en milepælbasert fakturaplan for et fast sett med likt fordelte milepæler.

1. Gå til **Innstillinger** > **Fakturahyppighet**, og angi fakturahyppigheten for underkontraktlinjene.
2. Åpne siden **Underkontrakter**, åpne underkontrakten du vil arbeide med, og åpne deretter underkontraktlinjen med fast pris som du skal opprette en milepælplan for.
3. Velg **Generer periodiske milepæler** i fanen **Milepæler for underkontrakt**.
4. Angi eller velg et datointervall, antall milepæler og fakturahyppigheten i dialogboksen. Du kan velge en startdato, eller du kan velge antall milepæler og fakturafrekvensen eller startdatoen, eller du kan velge sluttdato og fakturahyppighet. Du kan ikke velge sluttdato og antall milepæler.
Ved hjelp av denne informasjonen genererer systemet milepæler og oppføringer som vises i **Milepæler**-rutenettet.

   - **Navn på milepæl** – Navnet på milepælen settes til datoen for milepælen basert på fakturahyppigheten.
   - **Milepældato** – Datoen basert på fakturafrekvensen.
   - **Milepælbeløp** – Beregnet ved å dele delsumbeløpet på underkontraktlinjen med antall milepæler.

Hvis underkontraktlinjen har en verdi i feltet **Beregnet avgiftsbeløp**, legges denne verdien til for hver milepæl likt ved generering av periodiske milepæler.

Summen for beløpene på milepæler for underkontraktlinjen må være lik verdien av underkontraktlinjen. Hvis de ikke er like, oppstår det en feil. Du kan rette feilen og kontrollere at milepælsummen er lik verdien for underkontraktlinjen ved å opprette, redigere eller slette milepæl- og avgiftsbeløp. Når endringene er utført, lagrer og oppdaterer du siden for å sikre at det ikke oppstår flere feil.

## <a name="manually-create-subcontract-line-milestones"></a>Opprett milepæler for underkontraktlinje manuelt

Milepæler med fast pris på en underkontraktlinje kan genereres manuelt når de ikke deles opp regelmessig. Fullfør fremgangsmåten nedenfor for å opprette en milepæl for underkontraktlinje manuelt.

1. Velg **Underkontrakter** i navigasjonsruten, og åpne underkontrakten du vil arbeide med.
2. Åpne underkontraktlinjen med fast pris som du vil opprette en milepæl for.
3. Velg **+ Ny milepæl for underkontraktlinje** i delskjemaet i fanen **Milepæl for underkontrakt**.
4. Angi den nødvendige informasjonen på siden **Ny milepæl for underkontraktlinje** basert på følgende tabell.

    | Felt | Beskrivelse |Funksjonsinnvirkning|
    | --- | --- |----------------------|
    | Navn på milepæl | Navnet på milepælen. |Dette vises som den første kolonnen i alle oppslag basert på milepæler for underkontraktlinjer. Leverandørfakturalinjen som opprettes basert på denne milepælen, bruker også navnet på milepælen for underkontraktlinjen som standardnavnet på leverandørfakturalinjen.|
    | Beskrivelse | En beskrivelsen av milepælen. |Leverandørfakturalinjen som opprettes basert på denne milepælen, bruker også beskrivelsen av milepælen for underkontraktlinjen som standardbeskrivelse av leverandørfakturalinjen.|
    | Milepældato | Datoen da prosessen for automatisk fakturaoppretting skal se etter statusen for denne milepælen for å vurdere den for fakturering.| Denne verdien brukes som standarddato for leverandørfakturalinjen ved fakturering for denne underkontraktlinjen. |
    | Mengde | Beløpet eller verdien av milepælen som skal faktureres til kunden. |Denne verdien brukes som standardbeløp på leverandørfakturalinjen ved fakturering for denne underkontraktlinjen. |
    | Avgift | Avgiftsbeløpet som brukes på milepælen.| Denne verdien brukes som standard avgiftsbeløp på leverandørfakturalinjen ved fakturering for denne underkontraktlinjen. |
    | Beløp etter avgift | Dette skrivebeskyttede feltet beregnes som Beløp + Avgift.|Denne verdien brukes som standard på leverandørfakturalinjen ved fakturering for denne underkontraktlinjen. |
    | Fakturastatus | Når milepælen opprettes, settes denne statusen alltid til **Ikke klar for fakturering**.|  Når statusen er **Klar til faktura**, inkluderer opprettingen av leverandørfakturaen denne milepælen i leverandørfakturaen. |

5. Velg **Lagre og lukk**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
