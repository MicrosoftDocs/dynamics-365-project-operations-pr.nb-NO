---
title: Administrer prosjektprislister i prosjekttilbud
description: Dette emnet gir information om å arbeide med prosjektprislister i tilbud.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 926581f877f91e3a351d51cac9c2b1daba035126
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994913"
---
# <a name="manage-project-price-lists-on-project-quotes"></a>Administrer prosjektprislister i prosjekttilbud 

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Prosjekttilbud er utformet for å støtte salgsprislister med flere gyldige datoer. Med Dynamics 365 Project Operations legges det til en ny tilknyttet enhet kalt **Prosjektprislister**. Denne enheten har en én-til-mange-relasjon til et prosjekttilbud.

Prosjektprislister brukes til å prise tids-, material- og utgiftstransaksjoner for et prosjekt. Når et tilbud har en eller flere prosjektprislister, brukes disse prislistene til å prise for tid, materiell, kostnadsestimater og faktiske verdier for prosjekter som er knyttet til tilbudet via tilbudslinjen.

Når det ikke er noen prosjektprislister i et prosjekttilbud, får du en advarsel. Meldingen angir at siden det ikke finnes noen prosjektprislister, vil ikke det estimerte og faktiske prosjektarbeidet og utgiftene være priset. I stedet vil de ha null (0) pris for salgsverdier.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Tilknytte eller oppheve tilknytningen av en prosjektprisliste i et prosjekttilbud

Fullfør fremgangsmåten nedenfor for å opprette eller velge en bestemt prisliste for beregning av prosjektbasert arbeid og utgifter.

1. I tilbudet velger du kategorien **Prosjektpris**, og i delrutenettet velger du **+ Legg til ny prosjektprisliste**.
2. På hurtigopprettingssiden velger du en prisliste. Rullegardinlisten viser alle prislister som har kontekst angitt til **Salg**, og valutaen samsvarer med valutaen i tilbudet.
4. Skriv inn en beskrivelse av tilknytningen for prosjektprislisten, og velg **Lagre og Lukk**.

En tilknytning for prosjektprislisten opprettes.

Du kan gjenta denne prosessen hvis du har behov for å knytte til flere enn én prosjektprisliste til prosjekttilbudet. Bare opprett flere prosjektprislister hvis du har forskjellige gyldige datoer for hver av de tilknyttede prosjektprislistene.

> [!NOTE]
> Project Operations støtter ikke overlapping av datogyldighet for prosjektprislistene. Hvis det finnes flere prosjektprislister for en transaksjon med en gitt dato, blir prisen på den transaksjonen satt til null (0) som standard.
Hvis du vil fjerne en tilknytning for prosjektprisliste, velger du prosjektprislisten, og deretter velger du **Slett prosjektprisliste for tilbud**. Prislisten fjernes fra prosjektprislistene i tilbudet, men selve prislisten slettes ikke. Bare tilknytningen til tilbudet slettes.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Definere standard prosjektprislister i et tilbud

Prosjektprislister kan defineres som standard i et prosjekttilbud. Dette oppsettet sikrer at alle tilbud i organisasjonen alltid starter med en standard prisliste for denne prisperioden.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Definere standard for organisasjonen for prosjektprislister

1. Gå til **Innstillinger** > **Generelt** > **Parametere**.
2. På listesiden **Aktive parametere** finner du oppføringer og dobbeltklikker på den for å åpne den. 
3. På **Parametere**-siden velger du kategorien **Prisliste**. Du kan se at listen over standard prislister vises. Dette er en liste over standard kostnads- og salgsprislister. Ved å ha en salgsprisliste tilknyttet her for hver valuta du selger i, sørger du for at denne salgsprislisten som standard brukes i alle tilbud som du oppretter for kunder som har transaksjoner i denne valutaen.

### <a name="set-up-customer-specific-project-price-lists"></a>Definere kundespesifikke prosjektprislister

Kundespesifikkeprosjekt prislister kan også opprettes når du har forhandlet en hovedprisingsavtale med kundene.

Følg fremgangsmåten nedenfor for å definere en kundespesifikk prosjektprisliste.

1. I **Salg**-området velger du **Kunder**.
2. Velg i listen over aktive forretningsforbindelser, og åpne kundeoppføringen du har spesialprisliste for.
3. I kategorien **Prosjektprislister** kan du opprette en ny prislistetilknytning for å få prosjektprislisten som er spesifikk for denne kunden.

## <a name="create-custom-pricing-on-a-project-quote"></a>Opprette egendefinerte priser for et prosjekttilbud

Når du har angitt organisasjonens og de kundespesifikke standard prosjektprislistene, opprettes prosjekttilbudene automatisk med disse prosjektprislistetilordningene. I enkelte tilfeller kan det imidlertid hende at du må opprette egendefinerte priser for et bestemt prosjekttilbud. 

1. Under **Prosjekttilbud** i kategorien **Prosjektprisliste** verifiserer du i delrutenettet at ingen spesifikk prislisteoppføring er valgt.
2. Velg **Opprett egendefinert prising**. Dette vil lage kopier av alle standardprislistene som er knyttet til tilbudet, og knytte disse kopiene til tilbudet. De eksisterende tilknytningene til standardprislistene blir fjernet. Selgeren kan deretter begynne å gjøre endringer i prisene på disse kopiene. Disse endrede prisene gjelder bare for dette prosjekttilbudet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
