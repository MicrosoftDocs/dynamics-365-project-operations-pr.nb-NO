---
title: Virkemåte i brukergrensesnitt for tidsoppføring
description: Dette emnet gir informasjon om virkemåten i brukergrensesnittet for tidsoppføring.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: fd62fb1d8e0b2d859cb7da8b99cb725af587ff2f
ms.sourcegitcommit: 639ec8a41fda15dedfd6918702d33ea406999ba6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304313"
---
# <a name="time-entry-ui-behavior"></a>Virkemåte i brukergrensesnitt for tidsoppføring

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_


Rutenettet **Ukentlig tidsoppføring** er en egendefinert kontroll som har to hoveddeler, **Dimensjoner** og **Varighet**.

## <a name="keyboard-shortcuts"></a>Hurtigtaster
| Handling        | Snarvei                  |
|------------   |------------------------   |
| Ny           | Alt + Skift + n           |
| Kopier rad      | Alt + Skift + c           |
| Rediger enhet    | Alt + Skift + e           |
| Rediger rad      | Alt + Skift + Ctrl + e    |
| Åpne oppføring    | Alt + Skift + o           |
| Start        | Alt + Skift + s           |
| Tilbakekall        | Alt + Skift + r           |
| Delete        | Alt + Skift + d           |
| Kopier uke     | Alt + Skift + w           |

## <a name="dimensions"></a>Dimensjoner
**Dimensjoner**-delen viser dimensjonene som tiden kan angis i. Følgende dimensjoner støttes som standard:

  - Project
  - Prosjektoppgave
  - Rolle
  - Type
  - Oppføringsstatus

**Dimensjoner**-delen tillater ikke innebygd redigering. Denne delen blir støttet av en visning som gjør det mulig å legge til egendefinerte felt i rutenettet for ukentlige tidsoppføringer.

## <a name="duration"></a>Varighet
Varighetsdelen viser ukedagene som kolonneoverskrifter. Denne delen tillater innebygd redigering. Når en tidsoppføringsrad med riktige dimensjoner opprettes, kan brukerne raskt angi hvor mye tid de har brukt på disse dimensjonene.

## <a name="create-a-new-time-entry"></a>Opprette en ny tidsoppføring

1. Velg **Ny** i rutenettet for tidsoppføring. 
2. I dialogboksen **Hurtigoppretting for tidsoppføring** velger du datoen for tidsoppføringen.
3. Angi data for dimensjonene **Prosjekt**, **Prosjektoppgave**, **Rolle** og **Varighet**. Denne informasjonen skal legges til i minutter, timer eller dager ved å skrive **t**, **m** eller **d**, sammen med tallet. 
4. Angi en beskrivelse for oppføringen og kommentarer som kan deles eksternt angående tidsoppføringen. 

Når du lagrer oppføringen, vises de angitte verdiene i **Dimensjoner**-delen. Informasjonen som er angitt i feltet **Varighet**, vises på datoen tidsoppføringen ble opprettet for.

Oppslagsfelt blir støttet av systemvisninger. Når en bruker angir et prosjekt, settes feltet **Prosjektoppgave** til visningen **Kopi** som standard. Hvis du vil opprette tidsoppføringer for oppgaver som ikke er tilordnet til en bruker, velger du **Endre visning** i oppslagsdialogboksen, og deretter velger du visningen **Alle aktive prosjektoppgaver**.

## <a name="edit-a-time-entry"></a>Redigere en tidsoppføring 
Detaljer fra enkelte felt på tidsoppføringssiden, for eksempel **Beskrivelse** og **Eksterne kommentarer**, vises ikke i rutenettet for ukentlig tidsoppføring. I stedet vises en liten trekantindikator i **Varighet**-cellene som har disse tilleggsdetaljene. 

1. Hvis du vil redigere en tidsoppføring, merker du cellen du vil oppdatere, i tidsoppføringen.
2. Velg **Rediger detaljer** for å oppdatere dataene i ruten **Hovedskjema for tidsoppføring**. 

## <a name="copy-a-time-entry-row"></a>Kopiere en tidsoppføringsrad
Når raden er opprettet, kan du velge **Kopier rad** for å kopiere hele raden til en ny rad. Når en rad kopieres på denne måten, kopieres også dimensjoner og varigheter. Du kan også velge **Rediger rad** for å oppdatere dimensjonsverdier og varigheter i delen **Varighet**.

## <a name="open-a-time-entry-behavior"></a>Åpne en virkemåte for tidsoppføring
For å støtte optimal og rask registrering i de mest fremtredende feltene viser rutenettet for ukentlige tidsoppføringer et delsett av valgte dimensjoner og varigheter. Hvis du vil vise alle detaljene for en enkelt tidsoppføring, velg **Åpne** under **Rediger oppføring**.

## <a name="submit-a-time-entry"></a>Sende en tidsoppføring
Du kan sende én tidsoppføring eller gruppe med tidsoppføringer ved å velge en blokk av celler eller en hel tidsoppføringsrad og deretter velge **Send**. Sendte tidsoppføringer vises som oppføringer som venter på godkjenning, på godkjennernes **Godkjenning**-side. Når du har sendt inn tidsoppføringer, kan de ikke redigeres.

## <a name="recall-a-time-entry"></a>Tilbakekalle en tidsoppføring
Du kan tilbakekalle tidsoppføringer du har sendt. Du kan tilbakekalle én enkelt tidsoppføring, en blokk med tidsoppføringer eller en hel rad med tidsoppføringer. Tilbakekalte tidsoppføringer kan redigeres.

## <a name="time-entry-status"></a>Status for tidsoppføringer

- **Utkast**: Nye tidsoppføringer tilordnes automatisk statusen **Utkast**. Bare tidsoppføringer som har statusen **Utkast**, kan slettes.
- **Sendt**: Når en tidsoppføring sendes, oppdateres statusen til **Sendt**. 
- **Godkjent**: Når en sendt tidsoppføring er godkjent, oppdateres statusen til **Godkjent**. 
- **Returnert**: Hvis en tidsoppføring blir avvist, blir statusen oppdatert til **Returnert**, og oppføringen blir tilgjengelig for korrigering og ny innsending. 

## <a name="view-rejection-comments"></a>Vise avvisningskommentarer
Når en tidsoppføring blir avvist av en godkjenner, kan godkjenneren legge til kommentarer for å bidra til at ressursen forstår årsaken til avvisningen. Velg **Åpne oppføring** for å vise avvisningskommentarene for en tidsoppføring. Avvisningskommentarene vises på tidslinjen. Brukeren kan svare på avvisningskommentarene før de sender oppføringen på nytt.

## <a name="copy-week"></a>Kopier uke
Når det er opprettet noen få oppføringer, kan brukerne opprette flere tidsoppføringer samtidig.

1. I skjemaet **Tidsoppføringer** velger du **Kopier uke** for å masseopprette flere tidsoppføringer. 
2. I dialogboksen **Kopier**, i **Fra periode**-delen bruker du feltene **Startdato** og **Sluttdato** til å definere datointervallet tidsoppføringer skal kopieres fra. 
3. I delen **Til-periode** i feltet **Startdato** angir du datoen tidsoppføringer skal opprettes for. 
4. Velg **Kopier**. For den angitte datoen i **Til periode** opprettes en kopi av tidsoppføringene for den tilsvarende ukedagen i **Fra periode**. Mandagens tidsoppføring fra forrige uke blir for eksempel kopiert til mandag for uken som er angitt som **Til periode**.

## <a name="import"></a>Import
Den samme grunnleggende prosessen brukes til å importere fra bestillinger, tilordninger og utvekslinger. Du kan angi datointervallet som bestillinger importeres fra, og deretter eksplisitt velge bestillinger som skal kopieres til Utkast-tidsoppføringer. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
