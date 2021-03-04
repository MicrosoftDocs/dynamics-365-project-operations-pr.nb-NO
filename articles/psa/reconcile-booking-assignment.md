---
title: Avstemme bestillinger og tilordninger
description: Dette emnet gir informasjon om faktiske verdier.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9528bd983e6e18197138f0720abccdc6d6fa1ed5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147935"
---
# <a name="reconcile-bookings-and-assignments"></a>Avstemme bestillinger og tilordninger

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Et prosjektteammedlems prosjektbestillinger og prosjektaktivitetstilordninger er løst sammenkoblet. En ressurs kan derfor ha oppgavetildelinger som ikke svarer til bestillinger og bestillinger som ikke svarer til oppgavetildelinger. Ideelt sett er prosjektbestillinger og tilordninger rettet inn mot hverandre, slik at ressurser har forpliktet kapasitet til å utføre oppgavetilordningene. Virkeligheten er imidlertid at bestillinger kan forekomme basert på tilgjengelighet, og tidsberegning av oppgaver kan endres etter hvert som prosjektet fortsetter i livssyklusen. Derfor gir den løse innkoblingen fleksibilitet.

På grunn av den løse innkoblingen av prosjektbestillinger og oppgavetilordninger er en **Avstemming**-kategori inkludert i prosjektenheten. Denne kategorien hjelper prosjektledere med å avstemme teammedlemmets bestillinger og deres tilordninger for prosjektteamet.

For hvert navngitt teammedlem viser kategorien **Avstemming** bestillinger og tilordninger nedover til nivået for den individuelle oppgavetilordningen. Den viser timer i celler som kan representere tidsperioder, fra måneder til dager.

I **Tidsskala**-feltet kan du velge **Måned**, **Uke** eller **Dag**. **Uke** er valgt som standard. Du kan imidlertid endre standardverdien ved å velge **Innstillinger**-knappen. Når kategorien **Avstemming** åpnes, vises gjeldende dato, men du kan bruke kalenderkontrollen til å flytte frem eller tilbake i tid. Når et prosjekt har en startdato i fremtiden, viser kategorien denne datoen når den åpnes. Kalenderkontrollen inneholder også alternativer som gjør det mulig å gå til start- og sluttdatoer for prosjekter.

Du kan bruke utvidelseskontrollene for hver ressurs til å vise detaljene for den aktuelle ressursens bestillinger. Du kan også utvide tilordningene for hver ressurs til nivået for den individuelle oppgaven.

Nederst i **Avstemming**-kategorien vises en total nettosum for prosjektet, og kategorien inkluderer også en totalsumkolonne. For hver ressurs beregner kategorien forskjellen mellom et teammedlems bestillinger i prosjektet og en beregnet verdi av teammedlemmets oppgavetilordninger. Ideelt sett bør denne forskjellen være 0 (null). Det bør med andre ord ikke være forskjell mellom ressursens bestillinger og oppgavetildelinger. Eventuelle forskjeller angis av farger og skyggelegging for å fremheve to betingelser:

- **Få bestillinger** – Få bestillinger inntreffer når en ressurs har flere tildelinger enn bestillinger. Ettersom denne kapasiteten ikke er reservert, kan det hende at en prosjektleder kan korrigere dette ved å utvide ressursens bestillinger for å dekke underskuddet.
- **Overflødige bestillinger** – Overflødige bestillinger skjer når en ressurs er bestilt til prosjektet, men ikke er tilordnet til aktiviteter. Denne tilstanden kan være akseptabel, for eksempel hvis ressursen er bestilt før oppgavetilordning. I andre tilfeller kan det imidlertid hende at det ikke er planlagt at ressursen skal tilordnes. I slike tilfeller bør prosjektlederen vurdere å annullere ressursens bestillinger, slik at kapasiteten kan brukes for et annet prosjekt.

> [!NOTE]
> Forklaringen for disse betingelsene kan være skjult for å gi mer plass til rutenettet. I dette tilfellet kan du gjøre forklaringen synlig ved å velge **Innstillinger**-knappen.

Når **Tidsskala**-feltet er satt til et nivå som er høyere enn **Dag**, kan det i noen tilfeller føre til at differansene blir regnet som 0 (null). På **Måned**-nivået kan for eksempel nettodifferansen for en ressurs være 0 (null) for å angi at bestillinger er like tilordninger. Hvis du imidlertid ser på **Uke**-nivået, ser du at det er tildelinger på 0 (null) timer og bestillinger på 40 timer i den første uken i måneden, men tildelinger på 40 timer og bestillinger på 0 (null) timer i den andre uken i måneden. Selv om totalt antall bestillinger og tilordninger for måneden er like, er de forskjellige etter uke.

Når du viser tid på høyere nivåer, har celler i **Avstemming**-kategorien en indikator som informerer deg om at det er forskjeller på lavere nivåer. I illustrasjonen nedenfor vises for eksempel en celleindikator i cellen for måneden februar 2018 for ressursen med navnet Martine Carlson. Derfor kan du se at selv om ressursens bestillinger og tildelinger er like når de akkumuleres på **Måned**-nivå, samsvarer de ikke på de lavere nivåene.

![Ikke-samsvarende bestillinger og tilordninger på månedsnivå](media/reconcile-assignments-01.JPG)

Dobbeltklikk en celle for å zoome inn på det neste lavere nivået og vise forskjellen. Hvis du for eksempel dobbeltklikker på forskjellen til Martine Carlson for oktober 2018, kan du drille ned til **Uke**-nivået. Deretter kan du se at ressursen har bestillinger på 16 timer, men ingen tilordninger i de første to ukene i oktober, og 16 timer med tilordninger, men ingen bestillinger i den tredje uken i oktober.

![Ikke-samsvarende bestillinger og tilordninger på ukesnivå](media/reconcile-assignments-02.JPG)

Du kan høyreklikke en celle for å zoome ut på det neste høyere nivået. Du kan også deaktivere celleindikatoren ved å velge **Innstillinger**-knappen. 

Du kan også bruke knappene **Forrige** og **Neste** knappene over rutenettet til å bla gjennom eventuelle forskjeller i prosjektet. Hvis du vil bruke disse knappene, må du først velge en ressurs. Velg **Neste** for å gå til den neste forskjellen mellom bestillinger og tildelinger for den ressursen. Velg **Forrige** hvis du vil gå til den forrige forskjellen.

I situasjoner der du har oppgavetildelinger for en ressurs uten bestillinger (en bestillingsmangel), kan du velge den samlede bestillingsmangelen og deretter velge **Utvid bestilling**. Deretter kan du se bestillingen som er nødvendig for å løse ressursens underskudd. Du kan også vise ressursens bestillinger på gjeldende prosjekt og andre prosjekter. Velg **OK** for å opprette en bestilling av ressursen uten hensyn til gjeldende tilgjengelighet. Prosjektlederen eller ressurslederen kan deretter bruke planleggingstavlen til å behandle eventuelle situasjoner der en ressurs er overbestilt utover dens kapasitet fordi bestillingene ble utvidet.

## <a name="managing-with-time-zones"></a>Administrere med tidssoner
For å sikre nøyaktige og forutsigbare resultater når du bruker Utvid bestilling, er det to viktige krav som må oppfylles:  

- Brukeren må konfigurere tidssonen for enheten slik at den samsvarer med tidssonen som er angitt i systemets innstillinger for personalisering.
 
  ![Tidssoneinnstillinger i Windows 10](media/reconcile-assignments-03.png)

  ![Tidssoneinnstillinger i innstillinger for personalisering](media/reconcile-assignments-04.png)
 
- Ressursen som kan bestilles, må ha minst ett minutt med arbeidstid som overlapper med konturene som brukes til å definere den ønskede utvidelsen. Eksemplet nedenfor viser for eksempel gjennomgangsressurser med arbeidstid som faller mellom 9:00 og 19:00. 

  ![Sammenligning av ressursomfang](media/reconcile-assignments-05.png)

Følgende tabell viser:

- En prosjektkalendermal.
- Ressurs A: Denne ressursen har samme kalender og er i samme tidssone som prosjektet. Starttidspunktet for bestillinger blir kl. 9:00.
- Ressurs B: Denne ressursen befinner seg i en annen tidssone enn prosjektet og starter derfor klokken 7:00 i sin tidssone. Imidlertid vil bestillinger starte på 9:00 som det første starttidspunktet for tilordningsomfanget.
- Ressurser C og D: Ressursene ligger også i ulike tidssoner, som begge er forskjellige fra hverandre og prosjektet,

|Enhet  |Kalender  |
|-|-|
|Prosjektkalendermal   | ![prosjektkalender](media/reconcile-assignments-06.png) |
|Ressurs A  | ![Ressurs A-kalender](media/reconcile-assignments-06.png) |
|Ressurs B  |  ![Ressurs B-kalender](media/reconcile-assignments-07.png) |
|Ressurs C  |  ![Ressurs C-kalender](media/reconcile-assignments-08.png) |
|Ressurs D  | ![Ressurs D-kalender](media/reconcile-assignments-09.png)  |
 
Når du navigerer til avstemmingsvisningen, vises ressurstilordningene og de tilknyttede bestillingsmanglene.
 ![Avstemmingsvisning før utvidelse](media/reconcile-assignments-10.png)

Når funksjonen for Utvid bestilling er utført på hver ressurs, blir bestillinger utvidet for hver ressurs. Dette skyldes at hver enkelt ressurs' arbeidstid overlapper med omfanget av mangelen.
 ![Avstemmingsvisning etter bestillingsutvidelse](media/reconcile-assignments-11.png) 

En nærmere titt på detaljene i bestillinger viser imidlertid forskjellene i starttidspunktet for bestillinger. Bestillinger starter ikke tidligere enn starttidspunktet for tildelingsomfanget og ikke tidligere enn det tilgjengelige starttidspunktet for ressursen.
 ![Nye bestillinger for ressursene på planleggingstavlen](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]