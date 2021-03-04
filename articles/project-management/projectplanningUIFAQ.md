---
title: Feilsøke arbeid i oppgaverutenettet
description: Dette emnet gir feilsøkingsinformasjon som er nødvendig når du arbeider i oppgaverutenettet.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031549"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Feilsøke arbeid i oppgaverutenettet 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dette emnet beskriver hvordan du løser problemer som kan oppstå når du arbeider med kostnadsbehandling.

## <a name="enable-cookies"></a>Aktivere informasjonskapsler

Project Operations krever at informasjonskapsler fra tredjeparter aktiveres for å gjengi strukturen i arbeidet. Når informasjonskapsler fra tredjeparter ikke er aktivert, vises en tom side i stedet for oppgaver når du velger kategorien **Oppgaver** på siden **Prosjekt**.

![Tom kategori når informasjonskapsler fra tredjeparter ikke er aktivert](media/blankschedule.png)


### <a name="workaround"></a>Løsning
For nettleserne Microsoft Edge eller Google Chrome beskriver fremgangsmåtene nedenfor hvordan du oppdaterer nettleserinnstillingen slik at informasjonskapsler fra tredjeparter aktiveres.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Åpne Edge-nettleseren.
2. I hjørnet øverst til høyre velger du **ellipsen** (...), og deretter velger du **Innstillinger**.
3. Under **Informasjonskapsler og tillatelser på nettsteder** velger du **Informasjonskapsler og områdedata**.
4. Deaktiver **Blokker informasjonskapsler fra tredjeparter**.

#### <a name="google-chrome"></a>Google Chrome

1. Åpne Chrome-nettleseren.
2. Velg de tre vertikale prikkene øverst i høyre hjørne, og velg deretter **Innstillinger**.
3. Under **Personvern og sikkerhet** velger du **Informasjonskapsler og andre områdedata**.
4. Velg **Tillat alle informasjonskapsler**.

> [!IMPORTANT]
> Hvis du blokkerer informasjonskapsler fra tredjeparter, blokkeres alle informasjonskapsler og områdedata fra andre områder, selv om området er tillatt i unntakslisten.

## <a name="pex-endpoint"></a>PEX-endepunkt

Project Operations krever at en prosjektparameter refererer til PEX-endepunktet. Dette endepunktet kreves for å kommunisere med tjenesten som brukes til å gjengi strukturen for arbeidsfordelingsarbeid. Hvis parameteren ikke er aktivert, vises feilmeldingen Prosjektparameteren er ikke gyldig. 

### <a name="workaround"></a>Løsning
 ![Feltet PEX-endepunkt på prosjektparameteren](media/projectparameter.png)

1. Legg til feltet **PEX-endepunkt** på siden **Prosjektparametere**.
2. Oppdater feltet med følgende verdi: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Fjern feltet fra siden **Prosjektparametere**.

## <a name="privileges-for-project-for-the-web"></a>Rettigheter for prosjekt for Internett

Project Operations er avhengig av en ekstern planleggingsservice. Servicen krever at en bruker har flere roller tilordnet til lese- og skrivetilgang til enheter som er relatert til strukturen for arbeidsinndeling. Disse enhetene omfatter prosjektoppgaver, ressurstilordninger og aktivitetsavhengigheter. Hvis en bruker ikke kan gjengi strukturen for arbeidsinndeling når de går til kategorien **Oppgaver**, skyldes det sannsynligvis at Prosjekt for Project Operations ikke er aktivert. En bruker kan motta en sikkerhetsrolle eller en feil relatert til tilgangsfornektelse.


## <a name="workaround"></a>Løsning

1. Gå til **Innstilling > Sikkerhet > Brukere > Applikasjonsbrukere**.  

   ![Applikasjonsleser](media/applicationuser.jpg)
   
2. Dobbeltklikk appbrukeroppføringen for å kontrollere følgende:

 - Brukeren har tilgang til prosjektet. Denne verifiseringen utføres vanligvis ved å sørge for at brukeren har sikkerhetsrollen **Prosjektleder**.
 - Microsoft Project-appbrukeren finnes og er riktig konfigurert.
 
3. Hvis brukeren ikke finnes, kan du opprette en ny brukeroppføring. Velg **Nye brukere**. Endre oppføringsskjemaet til **Appbruker**, og legg deretter til **App-ID-en**.

   ![Detaljer for appbruker](media/applicationuserdetails.jpg)

4. Kontroller at brukeren er tilordnet riktig lisens, og at tjenesten er aktivert i tjenesteplandetaljene for lisensen.
5. Kontroller at brukeren kan åpne project.microsoft.com.
6. Kontroller gjennom prosjektparameterne at systemet henviser til riktig endepunkt.
7. Kontroller at prosjektappbrukeren er opprettet.
8. Bruk følgende sikkerhetsroller for brukeren:

  - Dataverse-bruker
  - Project Operations-system
  - Prosjektsystem

## <a name="error-when-updating-the-work-breakdown-structure"></a>Feil under oppdatering av arbeidsnedbrytningsstrukturen

Når det gjøres én eller flere oppdateringer i arbeidsnedbrytningsstrukturen, mislykkes endringene etter hvert og blir ikke lagret. Det vises en feil i tidsplanrutenettet om at nylige endringer du har gjort, kunne ikke lagres.

### <a name="workaround"></a>Løsning

1. Kontroller at brukeren er tilordnet riktig lisens, og at tjenesten er aktivert i tjenesteplandetaljene for lisensen.
2. Kontroller at brukeren kan åpne project.microsoft.com.
3. Kontroller at systemet henviser til det riktige endepunktet.
4. Kontroller at prosjektappbrukeren er opprettet.
5. Bruk følgende sikkerhetsroller for brukeren:
  
  - Dataverse-bruker eller basebruker
  - Project Operations-system
  - Prosjektsystem
  - Dobbel skriving for Project Operations (Denne rollen kreves hvis du distribuerer det ressursbaserte/ikke-lagerbeholdte scenarioet for Project Operations.)
