---
title: Forlenge tidsoppføringer
description: Dette emnet gir informasjon om hvordan utviklere kan forlenge tidsoppføringskontrollen.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582998"
---
# <a name="extending-time-entries"></a>Forlenge tidsoppføringer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations inneholder en tilpasset kontroll for utvidbar tidsoppføring. Denne kontrollen inkluderer følgende funksjoner:

- Angi tid vannrett over en uke
- Totaler etter dag, rad eller uke
- Kopier rader eller uker
- Tidsoppføring via TT: mm eller TT.tt (konverterer automatisk til TT.tt)
- Importer fra tildelinger, bestillinger eller avtaler

UTvidelse av tidsoppføringer er mulig i to områder:
- [Legg til egendefinerte tidsoppføringer for eget bruk](#add)
- [Tilpass den ukentlige tidsoppføringskontroll](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Legg til egendefinerte tidsoppføringer for eget bruk

Tidsoppføringer er en kjerneenhet som brukes i flere scenarioer. I bølge 1 fra april 2020 ble TESA-kjerneløsningen innført. TESA inneholder en **Innstillinger**-enhet og en ny **Tidsoppføringsbruker**-sikkerhetsrolle. De nye feltene **msdyn_start** og **msdyn_end**, som har en direkte relasjon til **msdyn_duration**, er også inkludert. Den nye enheten, sikkerhetsrollen og feltene gjør det mulig å gi en mer enhetlig tilnærming til tid på tvers av flere produkter.


### <a name="time-source-entity"></a>Tidskildeenhet
| Felt | Beskrivelse | 
|-------|------------|
| Navn  | Navnet på tidskildeoppføringen som brukes som den utvalgte verdien når tidsoppføringer opprettes. |
| Standard tidskilde [tidskilde: isdefault] | Som standard kan bare én tidskilde være merket som standard. Dette gjør det mulig at oppføringer kan angis som standard til en tidskilde hvis det ikke er angitt en. |
|Tidskildetype [tidskilde: sourcetype] | Kildetypen er et alternativ (Kildetype for tidsoppføring) som tillater tilknytning av tidskilden til en app. Verdier som er større enn 190 000 000, er reservert av Microsoft.|


### <a name="time-entries-and-the-time-source-entity"></a>Tidsoppføringer og tidskildeenheten
Hver tidsoppføring er tilknyttet en tidskildeoppføring. Denne oppføringen avgjør hvilke apper som skal behandle tidsoppføringen og hvordan.

Tidsoppføringer er alltid én sammenhengende tidsblokk, der start, slutt og varighet er knyttet til hverandre.

Logikken oppdaterer automatisk tidsoppføringsposten i følgende situasjoner:

- Hvis to av de tre følgende feltene er angitt, beregnes det tredje automatisk: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Feltene **msdyn_start** og **msdyn_end** er tidssonesensitive.
- Tidsoppføringer som er opprettet med bare **msdyn_date** og **msdyn_duration** angitt, starter med midnatt. Feltene **msdyn_start** og **msdyn_end** oppdateres i henhold til dette.

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

1. Legge til det egendefinerte feltet i dialogboksen **Hurtigoppretting**.
2. Konfigurer rutenettet slik at det egendefinerte feltet vises.
3. Legg til det egendefinerte feltet på siden **Radredigering** eller **Rediger tidsoppføring**, alt etter hva som er aktuelt.

Kontroller at det nye feltet har de nødvendige valideringene på siden **Radredigering** eller **Rediger tidsoppføring**. Som en del av denne oppgaven må du låse feltet basert på statusen til tidsoppføringen.

Når du legger til et egendefinert felt i rutenettet **Tidsoppføring** og deretter oppretter tidsoppføringer direkte i rutenettet, angis det egendefinerte feltet for disse oppføringene automatisk, slik at det samsvarer med raden. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Legge til det egendefinerte feltet i dialogboksen Hurtigoppretting
Legg til det egendefinerte feltet i dialogboksen **Hurtigoppretting: Opprett tidsoppføring**. Brukere kan deretter angi en verdi når de legger til tidsoppføringer ved å velge **Ny**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurere rutenettet slik at det egendefinerte feltet vises
Det er to måter å legge til et egendefinert felt på i rutenettet **Ukentlig tidsoppføring**.

- Tilpass visningen **Mine ukentlige tidsoppføringer**, og legg til det egendefinerte feltet i den. Du kan angi plassering og størrelse for det egendefinerte feltet i rutenettet ved å redigere egenskapene i visningen.
- Opprett en ny egendefinert tidsoppføringsvisning, og angi den som standardvisning. Denne visningen skal inneholde feltene **Beskrivelse** og **Eksterne kommentarer** i tillegg til kolonnene du vil inkludere i rutenettet. Du kan angi plassering, størrelse og standard sorteringsrekkefølge i rutenettet ved å redigere egenskapene i visningen. Konfigurer deretter den egendefinerte kontrollen for denne visningen, slik at den er en **Rutenett for tidsoppføring**-kontroll. Legg til kontrollen i visningen, og velg den for **Nett**, **Telefon** og **Nettbrett**. Konfigurer deretter parameterne for rutenettet for **Ukentlig tidsoppføring**. Angi feltet **Startdato** til **msdyn\_date**, angi feltet **Varighet** til **msdyn\_duration**, og angi feltet **Status** til **msdyn\_entrystatus**. Feltet **Liste over statusen Skrivebeskyttet** er angitt til **192350002 (Godkjent)**, **192350003 (Sendt inn)** eller **192350004 (Tilbakekalling forespurt)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Legg til det egendefinerte feltet på den riktige siden
Sidene som brukes til å redigere en tidsoppføring eller en rad med tidsoppføringer, finner du under **Skjemaer**. Knappen **Rediger oppføring** i rutenettet åpner siden **Rediger oppføring**, og knappen **Rediger rad** åpner siden **Radredigering**. Du kan redigere disse sidene slik at de inneholder egendefinerte felter.

Begge alternativene fjerner noe standardfiltrering på enhetene **Prosjekt** og **Prosjektoppgave**, slik at alle oppslagsvisninger for enhetene er synlige. Bare de relevante oppslagsvisningene er synlige som standard.

Du må angi den aktuelle siden for det egendefinerte feltet. Hvis du la til feltet i rutenettet, skal det mest sannsynlig være på siden **Radredigering** som blir brukt til felter som gjelder for hele raden med tidsoppføringer. Hvis det egendefinerte feltet har en unik verdi i raden hver dag (for eksempel hvis det er et egendefinert felt for sluttiden), skal det gå til siden **Rediger tidsoppføring**.

Hvis du vil legge til det egendefinerte feltet på en side, drar du et **Felt**-element til riktig plassering på siden, og deretter angir du egenskapene.

### <a name="add-new-option-set-values"></a>Legge til nye alternativsettverdier
Følg denne fremgangsmåten for å legge til verdier for alternativsett i et standardfelt.

1. Åpne redigeringssiden for feltet, og deretter, under **Type**, velger du **Rediger** ved siden av alternativsettet.
2. Legg til et nytt alternativ som har en egendefinert etikett og farge. Hvis du vil legge til en ny tidsoppføringsstatus, er standardfeltet kalt **Oppføringsstatus**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Angi en ny tidsregistreringsstatus som skrivebeskyttet
Hvis du vil angi en ny tidsregistreringsstatus som skrivebeskyttet, legger du til den nye tidsoppføringsverdien for egenskapen **Liste over statusen Skrivebeskyttet**. Pass på at du legger til nummeret, ikke etiketten. Den redigerbare delen av tidsregistreringsrutenettet blir nå låst for rader som har den nye statusen. Hvis du vil angi egenskapen **Liste over statusen Skrivebeskyttet** på en annen måte for forskjellige **Tidsoppføring**-visninger, legger du til rutenettet **Tidsoppføring** i en visnings **Egendefinerte kontroller**-del og konfigurere parameterne etter behov.

Deretter legger du til forretningsregler for å låse alle feltene på sidene **Radredigering** og **Rediger tidsoppføring**. For å få tilgang til forretningsreglene for disse sidene kan du åpne skjemaredigeringsprogrammet for hver side og deretter velge **Forretningsregler**. Du kan legge til den nye statusen i betingelsen i de eksisterende forretningsreglene, eller du kan legge til en ny forretningsregel for den nye statusen.

### <a name="add-custom-validation-rules"></a>Legge til egendefinerte valideringsregler
Du kan legge til to typer valideringsregler for opplevelsen i rutenettet **Ukentlig tidsoppføring**:

- Forretningsregler på klientsiden som fungerer på sider
- Valideringer av plugin-moduler på serversiden som gjelder for alle tidsoppføringsoppdateringer

#### <a name="client-side-business-rules"></a>Forretningsregler på klientsiden
Bruk forretningsregler til å låse og låse opp felt, angi standardverdier i felt og definere valideringer som bare krever informasjon fra gjeldende tidsregistreringsoppføring. For å få tilgang til forretningsreglene for en side kan du åpne skjemaredigeringsprogrammet og deretter velge **Forretningsregler**. Deretter kan du redigere de eksisterende forretningsreglene eller legge til en ny forretningsregel.

#### <a name="server-side-plug-in-validations"></a>Valideringer av plugin-moduler på serversiden
Du bør bruke plugin-modulvalideringer for valideringer som krever mer kontekst enn det som er tilgjengelig i én enkelt tidsregistreringsoppføring. Du bør også bruke dem for eventuelle valideringer du vil kjøre på innebygde oppdateringer i rutenettet. For å fullføre valideringene oppretter du en egendefinert plugin-modul i enheten **Tidsoppføring**.

### <a name="limits"></a>Grenser
Rutenettet **Tidsoppføring** har for tiden en størrelsesbegrensning på 500 rader. Hvis det er flere enn 500 rader, vises ikke de overflødige radene. Denne størrelsesgrensen kan ikke økes.

### <a name="copying-time-entries"></a>Kopiere tidsoppføringer
Bruk visningen **Kopier tidsoppføringskolonner** for å definere listen over felter som skal kopieres under tidsoppføring. **Dato** og **Varighet** er obligatoriske felter som ikke bør fjernes fra visningen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
