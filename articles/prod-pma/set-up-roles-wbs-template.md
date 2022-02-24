---
title: Konfigurere roller i maler for arbeidsnedbrytningsstruktur
description: Dette emnet gir informasjon om hvordan du konfigurerer rolleinformasjon i maler for arbeidsnedbrytingsstruktur.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143f1094c653fb7ac0e026b7875aa162a3eb83f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081600"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Konfigurere roller i maler for arbeidsnedbrytningsstruktur

[!include [banner](../includes/banner.md)]

Prosjektledere kan konfigurere WBS-maler (arbeidsnedbrytingsstruktur) som de kan bruke når de oppretter en WBS for nye prosjekter. Prosjektledere kan legge til roller når de oppretter en mal. Bruk fremgangsmåten nedenfor for å tilordne en rolle til en WBS-mal.

1. Velg **Prosjektstyring og regnskap** > **Oppsett** > **Prosjekter** > **Maler for arbeidsnedbrytningsstruktur**.
2. Velg **Detaljer** for en valgt WBS-mal.
3. Velg en oppgave i listen, og deretter, i feltet **Rolle**, velger du en rolle for å tilordne oppgaven.

## <a name="work-with-a-wbs"></a>Arbeide med en WBS

Du kan opprette en ny WBS, eller du kan kopiere en WBS fra en eksisterende WBS-mal. En prosjektleder kan enkelt administrere ressursene ved å tilordne roller til nye aktiviteter i WBS. Roller kan erstattes enten etter at en ressurs er anskaffet, eller etter at en bekreftet ressurs som skal arbeide på oppgaven, er identifisert. Denne fleksibiliteten gjør det mulig for prosjektledere å utføre følgende oppgaver:

- Identifiser antallet ressurser som kreves for WBS-arbeidspakker.
- Estimere prosjektkostnader.
- Fastslå et foreløpig budsjett.
- Estimer aktivitetsvarighet basert på roller og ressurser.
- Utvikle noen prosjektstyringsplaner basert på tilgjengelig prosjektinformasjon.

Det er lagt til flere alternativer i WBS for å bruke ressursfunksjonaliteten bedre.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Alternativ</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressurstilordninger</td>
<td>Vis tildelte ressurser, datoer, antall timer og bestillingstype for aktiviteter i WBS.</td>
</tr>
<tr class="even">
<td>Generere team automatisk</td>
<td>Legg til planlagte ressurser automatisk ved hjelp av roller som er tilknyttet en oppgave. Finance foreslår automatisk planlagte ressurser ved hjelp av beslutningsanalyse med flere vilkår som er basert på roller. Når rollene og innsatsen (timer) er angitt for oppgavene i en WBS, og etter at strukturen er frigitt, velger du <strong>Generer team automatisk</strong>. Det nødvendige antallet planlagte ressurser blir lagt til i WBS og i kategorien <strong>Prosjektteam og planlegging</strong>.</td>
</tr>
<tr class="odd">
<td>Ressurs (rullegardinliste)</td>
<td>På siden <strong>Start ressurstilordning</strong> kan du velge ressurser du vil opprette forpliktende eller ikke-forpliktende bestilling for, basert på den angitte varigheten. Du kan justere visningsinnstillingene for å vise og angi varighet for ressursaktiviteter. Du kan velge og tilordne ressurser på arbeidspakkenivået ved å bruke følgende alternativer:
<ul>
<li><strong>Godta</strong> – Bekreft endringer av ressursen som er tilordnet til en aktivitet.</li>
<li><strong>Avbryt</strong> – Avbryt endringer av ressursen som er tilordnet til en aktivitet.</li>
<li><strong>Tilordne automatisk</strong> – En tilgjengelig bemannet ressurs som har en samsvarende rolle, blir automatisk valgt og tilordnet til den valgte aktiviteten.</li>
</ul></td>
</tr>
</tbody>
</table>

1. På siden **Alle prosjekter** velger du **XYZ-oppgraderingsfase 2**-prosjektet.
2. Velg **Plan** > **Aktiviteter** > **Arbeidsnedbrytningsstruktur**.
3. Velg **Ny** for å legge til følgende nivå én-aktiviteter i WBS:

    - Starter
    - Planlegging
    - Kjører
    - Overvåking og kontroll
    - Lukk

4. Angi datoer og innsats (timer), som vist i illustrasjonen nedenfor.

    [![Angi datoer og innsats](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Velg oppgavelinjen **Innledende**, og deretter, i feltet **Rolle**, velger du **Overordnet prosjektleder**.
6. Velg **Publiser**.
7. På samme linje, i feltet **Ressurs**, velger du **Daniel Goldschmidt**, og deretter velger du **Godta**.
8. Velg oppgavelinjen **Planlegging**, og deretter, i feltet **Rolle**, velger du **Forretningsanalytiker**.
9. Velg **Publiser**, og velg deretter **Generere team automatisk**.
10. Velg **Ja** i meldingsboksen som vises.
11. I feltet **Ressurser** kontrollerer du at verdien er **Forretningsanalytiker 1**.
12. For ressursen **Forretningsanalytiker 1** åpner du oppslaget og velger **Start ressurstilordninger**. Velg deretter en arbeider for oppgaven.
13. Velg **Tilordne uforpliktende** &gt; **Full kapasitet**.

    > [!NOTE] 
    > Du får ingen advarsel om at den angitte ressursen nå er 2, fordi antallet ressurser forblir 1.

14. På siden **Arbeidsnedbrytningsstruktur** validerer du ressurstilordningen på WBS, og deretter velger du **Lagre**.
