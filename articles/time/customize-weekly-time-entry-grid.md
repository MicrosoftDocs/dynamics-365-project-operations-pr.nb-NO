---
title: Forlenge tidsoppføringer
description: Dette emnet gir informasjon om hvordan utviklere kan forlenge tidsoppføringskontrollen.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930892"
---
# <a name="extending-time-entries"></a>Forlenge tidsoppføringer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations inneholder en utvidbar, egendefinert kontroll for tidsoppføring. Denne kontrollen inkluderer følgende funksjoner:

- Angi tid vannrett over en uke
- Totaler etter dag, rad eller uke
- Kopier rader eller uker
- Tidsoppføring via TT: mm eller TT.tt (konverterer automatisk til TT.tt)
- Importer fra tildelinger, bestillinger eller avtaler

UTvidelse av tidsoppføringer er mulig i to områder:
- [Legg til egendefinerte tidsoppføringer for eget bruk](#add)
- [Tilpass den ukentlige tidsoppføringskontroll](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Legg til egendefinerte tidsoppføringer for eget bruk.

Tidsoppføringer er en kjerneenhet som er utformet for bruk i flere scenarioer. I lanseringsbølge 1, april 2020, ble TESA-kjerneløsningen introdusert, som har en **Innstillinger**-enhet og en ny **Tidsoppføringsbruker**-sikkerhetsrolle. De nye feltene **msdyn_start** og **msdyn_end**, som har en direkte relasjon til **msdyn_duration**, er også inkludert. Den nye enheten, sikkerhetsrollen og feltene gjør det mulig å gi en mer enhetlig tilnærming til tid på tvers av flere produkter.


### <a name="time-source-entity"></a>Tidskildeenhet
| Felt | Beskrivelse | 
|-------|------------|
| Navn  | Navnet på tidskildeoppføringen som brukes som den utvalgte verdien under oppretting av tidsoppføring. |
| Standard tidskilde [tidskilde: isdefault] | Som standard kan bare én tidskilde være merket som standard tidskilde. Denne funksjonaliteten gjør det mulig at oppføringer kan angis som standard til en tidskilde hvis det ikke er angitt en. |
|Tidskildetype [tidskilde: sourcetype] | Kildetypen er et alternativ (Kildetype for tidsoppføring) som tillater tilknytning av tidskilden til en app. Flere verdier blir lagt til i dette alternativsettet etter hvert som det legges til flere programmer. Vær oppmerksom på at verdier som er større enn 190 000 000, er reservert av Microsoft.|


### <a name="time-entries-and-the-time-source-entity"></a>Tidsoppføringer og tidskildeenheten
Hver tidsoppføring er tilknyttet en tidskildeoppføring. Denne oppføringen avgjør hvordan og hvilke programmer som skal behandle tidsoppføringen.

Tidsoppføringer er alltid én sammenhengende tidsblokk, der start, slutt og varighet er knyttet til hverandre.

Logikken oppdaterer automatisk tidsoppføringsposten i følgende situasjoner:

- Hvis to av de tre følgende feltene er angitt, beregnes det tredje automatisk 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Feltene **msdyn_start** og **msdyn_end** skiller mellom tidssoner.
- Tidsoppføringer som er opprettet der bare **msdyn_date** og **msdyn_duration** er angitt, starter ved midnatt, og **msdyn_start** og **msdyn_end** oppdateres i henhold til dette.

#### <a name="time-entry-types"></a>Tidsoppføringstyper

Tidsoppføringsposter har en tilknyttet type som definerer virkemåten til innsendingsflyten for det tilknyttede programmet.

|Etikett | Verdi|
|-----|-----|
|Pause   |192,355,000|
|Reise | 192,355,001|
|Overtid   | 192,354,320|
|Arbeid   | 192,350,000|
|Fravær    | 192,350,001|
|Ferie   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Tilpass den ukentlige tidsoppføringskontrollen
Utviklere kan legge til flere felt og oppslag i andre enheter og implementere egendefinerte forretningsregler for å støtte virksomhetsscenarioene sine.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Legge til egendefinerte felt med oppslag til andre enheter
Det er tre hovedtrinn for å legge til et egendefinert felt i rutenettet for ukentlige tidsoppføringer.

- Legg til det egendefinerte feltet i dialogboksen for hurtigoppretting.
- Konfigurer rutenettet slik at det egendefinerte feltet vises.
- Legg til det egendefinerte feltet i radredigeringsoppgaveflyten eller i celleredigeringsoppgaveflyten.

Du må også kontrollere at det nye feltet har de nødvendige valideringene i raden eller celleredigeringsoppgaveflyten. Som en del av dette trinnet må du låse feltet basert på tidsoppføringsstatusen.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Legge til det egendefinerte feltet i dialogboksen for hurtigoppretting
Du må legge til det egendefinerte feltet i dialogboksen for **hurtigoppretting for tidsoppføring**. Brukere kan deretter angi en verdi når de legger til tidsoppføringer ved å velge **Ny**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurere rutenettet slik at det egendefinerte feltet vises
Det er to måter å legge til et egendefinert felt i rutenettet for ukentlige tidsoppføringer:

  - Tilpasse en visning og legge til et egendefinert felt
  - Opprette en ny standard egendefinert tidsoppføring 


**Tilpasse en visning og legge til et egendefinert felt**

Du kan tilpasse visningen **Mine ukentlige tidsoppføringer** og legge til det egendefinerte feltet i den. Du kan velge plassering og størrelse for det egendefinerte feltet i rutenettet ved å redigere egenskapene i visningen.

**Opprette en ny standard egendefinert tidsoppføring** 

Denne visningen skal inneholde feltene **Beskrivelse** og **Eksterne kommentarer** i tillegg til kolonnene du vil ha i rutenettet. 

1. Velg plassering, størrelse og standard sorteringsrekkefølge i rutenettet ved å redigere egenskapene i visningen. 
2. Konfigurer den egendefinerte kontrollen for denne visningen, slik at den er en **Rutenett for tidsoppføring**-kontroll. 
3. Legg til denne kontrollen i visningen, og velg den for nett, telefon eller nettbrett. 
4. Konfigurer parameterne for rutenettet for ukentlige tidsoppføringer. Angi feltet **Startdato** til **msdyn_date**, sett **Varighet** -feltet til **msdyn_duration**, og sett feltet **Status** til **msdyn_entrystatus**. 
5. For standardvisningen er feltet **Liste over statusen Skrivebeskyttet** satt til **192350002,192350003,192350004**, feltet **Oppgaveflyt for rediger rad** er satt til **msdyn_timeentryrowedit**, og feltet **Oppgaveflyt for rediger celle** er satt til **msdyn_timeentryedit**. 
6. Du kan tilpasse disse feltene for å legge til eller fjerne skrivebeskyttelsesstatusen eller for å bruke en annen oppgavebasert opplevelse (TBX) for redigering av rader eller celler. Disse feltene skal være bundet til en statisk verdi.


> [!NOTE] 
> Begge alternativene fjerner noe standardfiltrering på enhetene **Prosjekt** og **Prosjektoppgave**, slik at alle oppslagsvisninger for enhetene blir synlige. Bare de relevante oppslagsvisningene er synlige som standard.
Du må angi den aktuelle oppgaveflyten for det egendefinerte feltet. Hvis du la til feltet i rutenettet, skal det mest sannsynlig være i radredigeringsoppgaveflyten som blir brukt til felt som gjelder for hele raden med tidsoppføringer. Hvis det egendefinerte feltet har en unik verdi hver dag, for eksempel et egendefinert felt for **Sluttidspunkt**, skal det være i celleredigeringsoppgaveflyten.

Hvis du vil legge til det egendefinerte feltet i en oppgaveflyt, drar du et **Felt**-element til riktig plassering på siden, og deretter angir du feltegenskapene. Angi egenskapen **Kilde** til **Tidsoppføring**, og sett **Datafelt**-egenskapen til det egendefinerte feltet. **Field**-egenskapen angir visningsnavnet på TBX-siden. Velg **Bruk** for å lagre endringene i feltet, og velg deretter **Oppdater** for å lagre endringene på siden.

Hvis du vil bruke en ny egendefinert TBX-side i stedet, oppretter du en ny prosess. Angi kategorien **Forretningsprosessflyt**, angi oppføringen til **Tidsoppføring**, og angi forretningsprosesstypen til **Kjør prosess som en oppgaveflyt**. Under **Egenskaper** skal egenskapen **Sidenavn** angis til visningsnavnet for siden. Legg til alle relevante felt på TBX-siden. Lagre og aktiver prosessen, og oppdater deretter den egendefinerte kontrollegenskapen for den relevante oppgaveflyten til verdien for **Navn** i prosessen.

### <a name="add-new-option-set-values"></a>Legge til nye alternativsettverdier
Hvis du vil legge til alternativsettverdier i et standardfelt, åpner du redigeringssiden for feltet, og deretter, under **Type**, velger du **Rediger** ved siden av alternativsettet. Deretter legger du til et nytt alternativ som har en egendefinert etikett og farge. Hvis du vil legge til en ny tidsoppføringsstatus, er standardfeltet kalt **Oppføringsstatus**, ikke **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Angi en ny tidsregistreringsstatus som skrivebeskyttet
Hvis du vil angi en ny tidsregistreringsstatus som skrivebeskyttet, legger du til den nye tidsoppføringsverdien for egenskapen **Liste over statusen Skrivebeskyttet**. Den redigerbare delen av tidsregistreringsrutenettet blir låst for rader som har den nye statusen.
Deretter legger du til forretningsregler for å låse alle feltene på TBX-sidene for **Radredigering for tidsoppføring** og **Redigering for tidsoppføring**. Du kan få tilgang til forretningsreglene for disse sidene ved å åpne redigeringsprogrammet for forretningsprosessflyt for siden og deretter velge **Forretningsregler**. Du kan legge til den nye statusen i betingelsen i de eksisterende forretningsreglene, eller du kan legge til en ny forretningsregel for den nye statusen.

### <a name="add-custom-validation-rules"></a>Legge til egendefinerte valideringsregler
Det finnes to typer valideringsregler som du kan legge til i det ukentlige rutenettet for tidsoppføring:

- Forretningsregler på klientsiden som fungerer i dialogbokser for hurtigoppretting og på TBX-sider.
- Valideringer av plugin-moduler på serversiden som gjelder for alle tidsoppføringsoppdateringer.

#### <a name="business-rules"></a>Forretningsregler
Bruk forretningsregler til å låse og låse opp felt, angi standardverdier i felt og definere valideringer som bare krever informasjon fra gjeldende tidsregistreringsoppføring. Du kan få tilgang til forretningsreglene for en TBX-side ved å åpne redigeringsprogrammet for forretningsprosessflyt for siden og deretter velge **Forretningsregler**. Deretter kan du redigere de eksisterende forretningsreglene eller legge til en ny forretningsregel. Hvis du vil bruke enda mer tilpassede valideringer, kan du bruke en forretningsregel til å kjøre JavaScript.

#### <a name="plug-in-validations"></a>Plugin-modulvalideringer
Du bør bruke plugin-modulvalideringer for valideringer som krever mer kontekst enn det som er tilgjengelig i én enkelt tidsregistreringsoppføring, eller for valideringer du vil kjøre på innebygde oppdateringer i rutenettet. For å fullføre valideringen oppretter du en egendefinert plugin-modul i enheten **Tidsoppføring**.
