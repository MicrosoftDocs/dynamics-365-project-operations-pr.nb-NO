---
title: Tilpasse ukentlige tidsoppføringer
description: Dette emnet gir informasjon om hvordan du implementerer egendefinerte forretningsregler som støtter en organisasjons praksis.
author: stsporen
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cc395e77e987dac062251ef87fcf8295305178e2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081707"
---
# <a name="customize-weekly-time-entry"></a>Tilpasse ukentlige tidsoppføringer 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I Microsoft Dynamics 365 Project Service Automation versjon 3.3 har Microsoft satt opp et moderne rutenett som gjør det enkelt å angi tid for opptil én uke om gangen. Det nye rutenettet for ukentlige tidsoppføringer viser totaler for oppføringer etter dato, rad eller uke. Ressurser kan lage kopier av tidsoppføringer i uken og også massekopiere fra tidligere uker. Systemtilpassere kan tilpasse visningen ved å legge til felt, legge til oppslag til andre entiteter og implementere egendefinerte forretningsregler for å støtte organisasjonens fremgangsmåter.

Du får tilgang til tidsoppføringen og det nye rutenettet for ukentlige tidsoppføringer. Den ikke-utvidbare opplevelsen av egendefinert tidsoppføring som var en del av tidligere PSA-versjoner, er erstattet av det utvidbare rutenettet for ukentlige tidsoppføringer, og også av en alternativ opplevelse i det skrivebeskyttede rutenettet og kalenderen. På grunn av denne endringen kan brukerne angi tid i ukentlige tidsoppføringer.

## <a name="page-layout"></a>Sideoppsett
Det nye rutenettet for ukentlig tidsoppføring er en egendefinert kontroll som har en verktøylinje og to hoveddeler, **Dimensjoner** og **Varighet**. Verktøylinjen inneholder en knapp som bare gjelder for denne egendefinerte kontrollen for rutenettet for tidsoppføringer. Knappene i Handlingsruten øverst på siden gjelder imidlertid for tre kontrolltyper som støttes for tidsregistrering: kontrollen for ukentlig oppføring, den skrivebeskyttede kontrollen og kalenderkontrollen.

### <a name="dimensions"></a>Dimensjoner
**Dimensjoner** -delen viser for eksempel kolonneoverskrifter, alle dimensjonene som tiden kan angis i. Følgende dimensjoner støttes som standard:

- Prosjekt
- Prosjektoppgave
- Rolle
- Type
- Oppføringsstatus

**Dimensjoner** -delen tillater ikke innebygd redigering. Denne delen blir støttet av en visning som gjør det mulig å legge til egendefinerte felt i rutenettet for ukentlige tidsoppføringer. Hvis du vil ha mer informasjon om hvordan du legger til egendefinerte felt, kan du se delen "Utvidbarhet" senere i dette emnet.

### <a name="duration"></a>Varighet
Varighetsdelen viser ukedagene som kolonneoverskrifter. I denne delen kan du aktivere innebygd redigering. Når en tidsoppføringsrad med riktige dimensjoner opprettes, kan brukerne raskt angi, innebygd, hvor mye tid de har brukt på disse dimensjonene.

## <a name="create-a-new-time-entry"></a>Opprette en ny tidsoppføring
Hvis du vil opprette en ny tidsoppføring i tidsoppføringsrutenettet, velger du **Ny**. Dialogboksen **Hurtigoppretting for tidsoppføring** vises. I denne dialogboksen kan brukerne velge tidsoppføringsdato og deretter angi data for dimensjonene **Prosjekt** , **Prosjektoppgave** , **Rolle** og **Varighet** i minutter, timer eller dager ved å skrive inn **h** , **m** eller **d** sammen med tallet. Brukere kan også angi en beskrivelse og kommentarer som kan deles eksternt for tidsoppføringen. Når brukere lagrer endringene sine, vises verdiene de angav for dimensjonene, i delen **Dimensjoner**. Varighetsinformasjon de angav i feltet **Varighet** , vises på datoen tidsoppføringen ble opprettet for.

Oppslagsfelt blir støttet av systemvisninger. Når en bruker angir et prosjekt, settes feltet **Prosjektoppgave** til visningen **Kopi** som standard. Hvis du vil opprette tidsoppføringer for oppgaver som ikke er tilordnet til en bruker, velger du **Endre visning** i oppslagsdialogboksen, og deretter velger du visningen **Alle aktive prosjektoppgaver**.

## <a name="edit-a-time-entry"></a>Redigere en tidsoppføring
Detaljer fra enkelte felt på tidsoppføringssiden, for eksempel **Beskrivelse** og **Eksterne kommentarer** , vises ikke i rutenettet for ukentlig tidsoppføring. I stedet vises en liten trekantindikator i varighetsceller som har disse tilleggsdetaljene. Merk cellen, og velg deretter **Rediger detaljer** for å vise dataene i ruten **Hurtigredigering**. Hvis du vil redigere eller oppdatere detaljene for en bestemt tidsoppføring som ikke er en del av rutenettet for ukentlige tidsoppføringer, må brukere åpne ruten **Hurtigredigering**.

## <a name="copy-a-time-entry-row"></a>Kopiere en tidsoppføringsrad
Når den første tidsoppføringsraden er opprettet, kan brukere velge **Kopier rad** for å kopiere hele raden til en ny rad. Når en rad kopieres på denne måten, kopieres også dimensjoner og varigheter. Brukere kan også velge **Rediger rad** for å oppdatere dimensjonsverdier og varigheter innebygd i delen **Varighet**.

## <a name="open-a-time-entry"></a>Åpne en tidsoppføring
For å støtte optimal og rask registrering i de mest fremtredende feltene viser rutenettet for ukentlige tidsoppføringer et delsett av valgte dimensjoner og varigheter. Hvis du vil vise alle detaljene for en enkelt tidsoppføring, velg **Åpne** under **Rediger oppføring**.

## <a name="submit-a-time-entry"></a>Sende en tidsoppføring
Brukere kan sende én tidsoppføring eller gruppe med tidsoppføringer ved å velge en blokk av celler eller en hel tidsoppføringsrad og deretter velge **Send**. Sendte tidsoppføringer vises som oppføringer som venter på godkjenning, på godkjennernes **Godkjenning** -side. Når du har sendt inn tidsoppføringer, kan de ikke redigeres.

## <a name="recall-a-time-entry"></a>Tilbakekalle en tidsoppføring
Du kan tilbakekalle tidsoppføringer du har sendt. Du kan tilbakekalle én enkelt tidsoppføring, en blokk med tidsoppføringer eller en hel rad med tidsoppføringer. Tidsregistreringer som tilbakekalles, er tilgjengelige for ressurser for redigering.

## <a name="time-entry-status"></a>Status for tidsoppføringer
Nye tidsoppføringer tilordnes automatisk statusen **Utkast**. Når en tidsoppføring sendes, oppdateres statusen til **Sendt**. Når en sendt tidsoppføring er godkjent, oppdateres statusen til **Godkjent**. Hvis en tidsoppføring blir avvist, blir statusen oppdatert til **Returnert** , og oppføringen blir tilgjengelig for korrigering og ny innsending. Bare tidsoppføringer som har statusen **Utkast** , kan slettes.

## <a name="view-rejection-comments"></a>Vise avvisningskommentarer
Når en tidsoppføring blir avvist av en godkjenner, kan godkjenneren legge til avvisningskommentarer for å bidra til at ressursen forstår årsaken til avvisningen. Velg **Åpne oppføring** for å vise avvisningskommentarene for en tidsoppføring. Avvisningskommentarene vises på tidslinjen. På tidslinjen kan ressursen svare på avvisningskommentarene før han eller hun sender oppføringen på nytt.

## <a name="copy-week"></a>Kopier uke
Etter oppretting av noen få oppføringer kan brukere velge **Kopier uke** for å masseopprette flere tidsoppføringer. Dialogboksen **Kopier** vises. I **Fra periode** -delen bruker du feltene **Startdato** og **Sluttdato** til å definere datointervallet tidsoppføringer skal kopieres fra. I delen **Til-periode** i feltet **Startdato** angir du datoen tidsoppføringer skal opprettes for. Deretter velger du **Kopier**. For den angitte datoen i "til"-perioden opprettes en kopi av tidsoppføringene for den tilsvarende ukedagen i "fra"-perioden. Mandagens tidsoppføring fra forrige uke blir for eksempel kopiert til mandag for uken som er angitt som "Til"-periode.

## <a name="import"></a>Importer
Den samme grunnleggende prosessen brukes til å importere fra bestillinger, tilordninger og utvekslinger. Brukere kan angi datointervallet som bestillinger importeres fra. De må deretter eksplisitt velge bestillingene som må kopieres til Utkast-tidsoppføringer. I den tidligere versjonen ble foreslåtte tidsoppføringer vist i rutenettet og kalenderen, og de gikk tapt da økten ble oppdatert.

## <a name="extensibility"></a>Utvidbarhet
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Legge til egendefinerte felt som har oppslag til andre enheter
Det er tre hovedtrinn for å legge til et egendefinert felt i rutenettet for ukentlige tidsoppføringer.

1.  Legg til det egendefinerte feltet i dialogboksen for hurtigoppretting.
2.  Konfigurer rutenettet slik at det egendefinerte feltet vises.
3.  Legg til det egendefinerte feltet i radredigeringsoppgaveflyten eller i celleredigeringsoppgaveflyten, alt etter behov.

Du må også kontrollere at det nye feltet har de nødvendige valideringene i raden eller celleredigeringsoppgaveflyten. Som en del av dette trinnet må du låse feltet basert på tidsoppføringsstatusen.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Legge til det egendefinerte feltet i dialogboksen for hurtigoppretting
Du må legge til det egendefinerte feltet i dialogboksen for hurtigoppretting for tidsoppføring. Slik at brukere kan angi en verdi for den når de legger til tidsoppføringer ved hjelp **Ny** -knappen.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurere rutenettet slik at det egendefinerte feltet vises
Det er to måter å legge til et egendefinert felt i rutenettet for ukentlige tidsoppføringer. Det første alternativet er å tilpasse visningen **Mine ukentlige tidsoppføringer** og legge til det egendefinerte feltet i den. Du kan velge plassering og størrelse for det egendefinerte feltet i rutenettet ved å redigere egenskapene i visningen.

Det andre alternativet er å opprette en ny egendefinert tidsoppføringsvisning og angi den som standardvisning. Denne visningen skal inneholde feltene **Beskrivelse** og **Eksterne kommentarer** i tillegg til kolonnene du vil ha i rutenettet. Du kan velge plassering, størrelse og standard sorteringsrekkefølge i rutenettet ved å redigere egenskapene i visningen. Konfigurer deretter den egendefinerte kontrollen for denne visningen, slik at den er en **Rutenett for tidsoppføring** -kontroll. Legg til denne kontrollen i visningen, og velg den for nett, telefon eller nettbrett. Konfigurer deretter parameterne for rutenettet for ukentlige tidsoppføringer. Angi feltet **Startdato** til **msdyn_date** , sett **Varighet** -feltet til **msdyn_duration** , og sett feltet **Status** til **msdyn_entrystatus**. For standardvisningen er feltet **Liste over statusen Skrivebeskyttet** satt til **192350002,192350003,192350004** , feltet **Oppgaveflyt for rediger rad** er satt til **msdyn_timeentryrowedit** , og feltet **Oppgaveflyt for rediger celle** er satt til **msdyn_timeentryedit**. Du kan tilpasse disse feltene for å legge til eller fjerne skrivebeskyttelsesstatusen eller for å bruke en annen oppgavebasert opplevelse (TBX) for redigering av rader eller celler. Disse feltene skal være bundet til en statisk verdi.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Legge til det egendefinerte feltet i den riktige oppgavereredigeringsflyten
Du finner TBX-sidene som brukes til redigering, under **Prosesser**. Standardsidene er **Project Service – Radredigering for tidsoppføring** og **Project Service – Rediger tidsoppføring**. Du kan enten redigere disse standardsidene eller opprette nye egendefinerte TBX-sider.

> [!NOTE] 
> Begge alternativene fjerner noe standardfiltrering på enhetene **Prosjekt** og **Prosjektoppgave** , slik at alle oppslagsvisninger for enhetene blir synlige. Bare de relevante oppslagsvisningene er synlige som standard.

Du må angi den aktuelle oppgaveflyten for det egendefinerte feltet. Hvis du la til feltet i rutenettet, skal det mest sannsynlig være i radredigeringsoppgaveflyten som blir brukt til felt som gjelder for hele raden med tidsoppføringer. Hvis det egendefinerte feltet har en unik verdi hver dag, for eksempel et egendefinert felt for **Sluttidspunkt** , skal det være i celleredigeringsoppgaveflyten.

Hvis du vil legge til det egendefinerte feltet i en oppgaveflyt, drar du et **Felt** -element til riktig plassering på siden, og deretter angir du egenskapene. Angi egenskapen **Kilde** til **Tidsoppføring** , og sett **Datafelt** -egenskapen til det egendefinerte feltet. **Field** -egenskapen angir visningsnavnet på TBX-siden. Velg **Bruk** for å lagre endringene for feltet. Velg deretter **Oppdater** for å lagre endringene på siden.

Hvis du vil bruke en ny egendefinert TBX-side i stedet, oppretter du en ny prosess. Angi kategorien **Forretningsprosessflyt** , angi oppføringen til **Tidsoppføring** , og angi forretningsprosesstypen til **Kjør prosess som en oppgaveflyt**. Under **Egenskaper** skal egenskapen **Sidenavn** angis til visningsnavnet for siden. Legg til alle relevante felt på TBX-siden. Lagre og aktiver prosessen, og oppdater deretter den egendefinerte kontrollegenskapen for den relevante oppgaveflyten til verdien for **Navn** i prosessen.

### <a name="add-new-option-set-values"></a>Legge til nye alternativsettverdier
Hvis du vil legge til alternativsettverdier i et standardfelt, åpner du redigeringssiden for feltet, og deretter, under **Type** , velger du **Rediger** ved siden av alternativsettet. Deretter legger du til et nytt alternativ som har en egendefinert etikett og farge. Hvis du vil legge til en ny tidsoppføringsstatus, er standardfeltet kalt **Oppføringsstatus** , ikke **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Angi en ny tidsregistreringsstatus som skrivebeskyttet
Hvis du vil angi en ny tidsregistreringsstatus som skrivebeskyttet, legger du til den nye tidsoppføringsverdien (nummeret, ikke etiketten) til egenskapen **Liste over statusen Skrivebeskyttet**. Den redigerbare delen av tidsregistreringsrutenettet blir låst for rader som har den nye statusen.
Deretter legger du til forretningsregler for å låse alle feltene på TBX-sidene for **Radredigering for tidsoppføring** og **Redigering for tidsoppføring**. Du kan få tilgang til forretningsreglene for disse sidene ved å åpne redigeringsprogrammet for forretningsprosessflyt for siden og deretter velge **Forretningsregler**. Du kan legge til den nye statusen i betingelsen i de eksisterende forretningsreglene, eller du kan legge til en ny forretningsregel for den nye statusen.

### <a name="add-custom-validation-rules"></a>Legge til egendefinerte valideringsregler
Det finnes to typer valideringsregler som du kan legge til for opplevelsen for rutenettet for ukentlige tidsoppføringer: • Forretningsregler på klientsiden som fungerer i hurtigopprettingsdialogbokser og på TBX-sider •   Valideringer for plugin-moduler på serversiden som gjelder for alle tidsregistreringsoppdateringer

#### <a name="business-rules"></a>Forretningsregler
Bruk forretningsregler til å låse og låse opp felt, angi standardverdier i felt og definere valideringer som bare krever informasjon fra gjeldende tidsregistreringsoppføring. Du kan få tilgang til forretningsreglene for en TBX-side ved å åpne redigeringsprogrammet for forretningsprosessflyt for siden og deretter velge **Forretningsregler**. Deretter kan du redigere de eksisterende forretningsreglene eller legge til en ny forretningsregel. Hvis du vil bruke enda mer tilpassede valideringer, kan du bruke en forretningsregel til å kjøre JavaScript.

#### <a name="plug-in-validations"></a>Plugin-modulvalideringer
Du bør bruke plugin-modulvalideringer for valideringer som krever mer kontekst enn det som er tilgjengelig i én enkelt tidsregistreringsoppføring, eller for valideringer du vil kjøre på innebygde oppdateringer i rutenettet. For å fullføre valideringen oppretter du en egendefinert plugin-modul i enheten **Tidsoppføring**.

> [!IMPORTANT] 
> For øyeblikket hindrer et kjent problem på TBX-sidene at brukere retter informasjon og velger Fullført på nytt når en oppdatering mislykkes med en plugin-modulvalidering. Du kan omgå dette problemet ved å konfigurere forretningsregelvalideringer for å unngå denne situasjonen så mye som mulig.
