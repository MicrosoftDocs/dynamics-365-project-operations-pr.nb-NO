---
title: Registrer materialbruk på prosjekter og prosjektoppgaver
description: Dette emnet inneholder informasjon om hvordan du logger materialbruk mot prosjekter og prosjektoppgaver.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d8757049953fab0ad8bf6ee1a1d695fcb6df75b1be52641ad4af3b3137d7a0a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999283"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Registrer materialbruk på prosjekter og prosjektoppgaver

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Når et prosjektteam arbeider gjennom oppgaver på et prosjekt, bruker de materialer. Ved hjelp av en logg for materialbruk kan du registrere denne bruken slik at den kan godkjennes av prosjektlederen og etter hvert faktureres til kunden. 

Følg denne fremgangsmåten for å registrere bruk av materialer for katalogprodukter eller ikke-katalogprodukter og sende dem til godkjenneren: 

1. Velg **Materialbruk** i navigasjonsruten, og velg deretter **Ny**.
2. På siden **Ny materialbruk** angir du den nødvendige informasjonen om materialbruk, og deretter velger du **Lagre**.

Tabellen nedenfor inneholder informasjon om feltene på siden **Logg over materialbruk**. 

| **Felt** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- |
| Beskrivelse | En beskrivelse av den bestemte materialbruken. | Dette feltet har ingen nedstrøms påvirkning. |
| Dato | Datoen for bruk av materialet. | Dette feltet har ingen nedstrøms påvirkning. |
| Project | En liste over prosjekter som er aktive. | Valg av et prosjekt for en logg for materialbruk har innvirkning på **Oppgave**-feltet, slik at bare de oppgavene som er i prosjektet, vises. |
| Oppgave | En liste over oppgaver for prosjektet, inkludert sammendrags- og bladnodeoppgaver. | Når du velger en oppgave for en logg for materialbruk, påvirker dette den faktiske materialkostnaden og det faktiske materialsalget for en oppgave. Hvis dette feltet står tomt, spores den tilsvarende materialbrukskostnaden og salget og oppsummeres bare på prosjektnivå. |
| Velg produkt | Angi om materialbruken gjelder et **eksisterende** produkt (i produktkatalogen) eller et produkt som **ikke er** i produktkatalogen. | Dette feltet avgjør produkttypen. |
| Produkt | ID-en for produktet fra produktkatalogen. Når du velger en produkt-ID, oppdateres feltet **Velg produkt** automatisk til **Eksisterende produkt**. ID-en brukes til å hente kost- og salgspriser fra prislisten. | Dette feltet har ingen nedstrøms påvirkning. |
| Beskrivelse av produkt ikke i produktkatalog | Et tekstfelt for å skrive inn navnet på produktet. Dette feltet er tilgjengelig når du velger **Ikke i produktkatalog** i **Velg produkt**-feltet.| Dette feltet har ingen nedstrøms påvirkning. |
| Ressurs som kan reserveres| Ressurs som brukte dette materialet i prosjektet. Standarden for dette feltet er ressursen som kan reserveres for den innloggede brukeren, men kan endres til oppføringsbruk på vegne av andre medlemmer i prosjektteamet. | Dette feltet har ingen nedstrøms påvirkning. |
| Enhetsgruppe | Standardverdien i dette feltet kommer fra enhetsgruppen som er angitt som standard for katalogproduktet. Du kan oppdatere dette feltet for å velge en annen enhetsgruppe. | Dette feltet har ingen nedstrøms påvirkning. |
| Enhet | Standardverdien i dette feltet kommer fra standardenheten for det valgte produktet. Du kan oppdatere dette feltet for å velge en annen enhet. | Endring av enheten fører til en annen standard enhetspris og -kostnad. |
| Antall | Antallet av produktet som er brukt i prosjektet eller prosjektoppgaven. | Dette feltet har ingen nedstrøms påvirkning. |
| Enhetskost | Enhetskostnaden for det valgte produktet og enhetskombinasjonen som angitt i den aktuelle kostnadsprislisten. | Enhetskostnaden vises alltid i kostnadsvalutaen for prosjektet. Hvis det ikke er noen enhetskostnad for kombinasjonen av produktet og enheten i prislisten, settes enhetskostnaden til 0,00 som standard. |
| Totale kostnader | Kostnadsbeløpet som beregnes som antall \* enhetskostnad.| Kostnadsbeløpet vises alltid i kostnadsvalutaen for prosjektet. |


## <a name="submit-material-usage-for-review-and-approval"></a>Send inn materialbruk til gjennomsyn og godkjenning 
Når du har registrert all materialbruken og er klar til å få den godkjent, må du sende inn bruksinformasjonen for gjennomsyn.

1. Gå til **Logg over materialbruk**, og velg én eller flere oppføringer. Du kan også velge alle materialbruksoppføringene ved å bruke avmerkingsboksen i hodet.
2. Velg **Send inn**. Systemet behandler de valgte oppføringene og oppretter deretter forespørsler om godkjenning av materiale.

## <a name="recall-a-material-usage-log"></a>Tilbakekall en logg over materialbruk

Når det er nødvendig, kan du tilbakekalle innsendt materialbruk. Tiden som kreves for å tilbakekalle en oppføring for materialbruk, avhenger av godkjenningsfasen.  Hvis godkjenneren ikke har godkjent oppføringen ennå, kan tilbakekallingen skje umiddelbart. Hvis imidlertid oppføringen allerede er godkjent, blir godkjenneren bedt om å godkjenne tilbakekallingen og tilbakeføre transaksjonene.

1. Gå til **Materialbruk**, og velg materialbruken du vil kalle tilbake, i listen over materialbrukslogger.
2. Velg **Tilbakekall**. Hvis oppføringen for materialbruk ikke er godkjent ennå, tilbakekalles den umiddelbart. Hvis materialoppføringen allerede er godkjent, opprettes det en forespørsel om tilbakekalling for å varsle godkjenneren om at du vil tilbakekalle materialbruken. Godkjenneren vil deretter bekrefte at reverseringen kan utføres, og oppføringen vil bli returnert.

## <a name="delete-a-material-usage-log"></a>Slett en logg over materialbruk

Du kan slette logger for materialbruk som ikke er sendt. Hvis du vil slette en logg for materialbruk som allerede er sendt, må du først tilbakekalle den.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
