---
title: Administrere prosjektprislister i prosjektkontrakter
description: Dette emnet gir informasjon om behandling av prosjektprislister på prosjektkontrakter.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ffc48782394995781535ae56142dc76afeb9a040
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858575"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Administrere prosjektprislister i prosjektkontrakter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Prosjektkontrakter i Dynamics 365 Project Operations er utformet for å støtte flere salgsprislister med gyldighetsdato på en kontrakt. In Project Operations er det en ny tilknyttet enhet kalt **Prosjektprislister**. Denne enheten har en én-til-mange-relasjon til en prosjektkontrakt.

Prosjektprislister brukes til å prise tids-, material- og utgiftstransaksjoner for et prosjekt. Når en kontrakt har en eller flere prosjektprislister, brukes disse prislistene til å prise for tid, materiell, kostnadsestimater og faktiske verdier for prosjekter som er knyttet til kontrakten via kontraktlinjen.

Når det ikke finnes prosjektprislister på en prosjektkontrakt, vises en advarsel om at det ikke finnes prosjektprislister, og at estimater, faktisk prosjektarbeid, materiale og utgifter som er logget, ikke er priset. Det vil ikke være pris for salgsverdier.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Knytte eller oppheve tilknytningen til en prosjektprisliste i en prosjektkontrakt

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Opprett eller tilknytt en bestemt prisliste for beregning av prosjektbasert arbeid, materiell og utgifter

1. Velg kategorien **Prosjektprislister** i prosjektkontrakten.
2. Velg **+ Legg til ny prosjektprisliste** i delrutenettet.
3. Velg en prisliste på glidebryteren **Hurtigoppretting**. 

  Rullegardinlisten viser alle prislister som har konteksten satt til **Salg**, der valutaen på prislisten samsvarer med valutaen på kontrakten.
  
4. Skriv inn en beskrivelse for prosjektprislistetilknytningen, velg **Lagre**, og lukk deretter **Hurtigoppretting**-glidebryteren.

   En tilknytning for prosjektprislisten opprettes.
   
5. Gjenta trinn 1–4 for å knytte mer enn én prosjektprisliste til prosjektkontrakten. Bare opprett flere prosjektprislister hvis du har ulik gyldighetsdato for hver av de tilknyttede prosjektprislistene.

> [!NOTE]
> Project Operations støtter ikke overlappende gyldighetsdato for prosjektprislistene. Hvis det finnes flere prosjektprislister for en transaksjon med en gitt dato, blir prisen på transaksjonen som standard null.

### <a name="remove-a-project-price-list-association"></a>Fjerne en tilknytning til en prosjektprisliste

- Velg prosjektprislisten, og velg deretter valget for **slett kontraktprosjektprisliste** i delrutenettet. 

  Prislisten fjernes fra prosjektprislistene i kontrakten. Selve prislisten blir ikke slettet. Bare tilknytningen til kontrakten blir slettet.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Konfigurere automatisk standardering av prosjektprislister på en kontrakt

En prosjektprisliste kan angis som standard prosjektprisliste. Dette oppsettet sikrer at alle kontraktene i organisasjonen alltid starter med en standard prosjektprisliste for den prisperioden.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Konfigurere organisasjonsstandarden for prosjektprislister

1. Gå til **Innstillinger** > **Generelt**, og velg deretter **Parametere**.
2. På listesiden **Aktive parametere** velger eller dobbeltklikker du oppføringen for å åpne den. Når du dobbeltklikker, må du passe på at du ikke klikker på en feltverdi som er en hyperkobling. 
3. På siden **Aktive parametere** velger du kategorien **Prisliste**. Et delrutenett viser en liste over standard prislister. Dette er en liste over standard kostnads- og salgsprislister. Det å ha en **Salg**-prisliste tilknyttet her ofr hver hver valuta du selger inn, sikrer at salgsprislisten er standard for alle kontrakter som du oppretter for kunder som utfører transaksjoner i denne valutaen.

### <a name="set-up-a-customer-specific-project-price-list"></a>Konfigurere en kundespesifikk prosjektprisliste

Du kan også sette opp kundespesifikke prosjektprislister når du har forhandlet en hovedprisavtale med kundene.

1. Gå til **Salg** > **Kunder**.
2. Velg kunden som har spesialprisliste, fra listen over aktive forretningsforbindelser.
3. Velg kundeoppføringen for å åpne den, og velg deretter kategorien **Prosjektprislister**. Et delrutenett viser en liste over prosjektprislister som er spesifikke for denne kunden. 
4. Opprett en ny prislistetilknytning her for å få prosjektprisliste som er spesifikk for denne kunden.

## <a name="custom-pricing-on-a-project-contract"></a>Egendefinert prissetting for en prosjektkontrakt

Når du har angitt organisasjons- og kundespesifikke standard prosjektprislister, blir prosjektkontraktene opprettet automatisk med disse prosjektprislistetilordningene. Prosjektprislister i en prosjektkontrakt blir imidlertid alltid kopiert med dato og kontraktnavn lagt til. Forretningsforbindelses- og prosjektlederne kan deretter begynne å gjøre endringer i prisene på disse kopiene. Disse endrede prisene gjelder bare for denne prosjektkontrakten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
