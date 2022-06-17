---
title: Feilsøke arbeid i oppgaverutenettet
description: Denne artikkelen inneholder informasjon om feilsøking du trenger når du arbeider i oppgaverutenettet.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e6ab4f34fe3f6732f7bef252f298671e07a3c3ca
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911056"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Feilsøke arbeid i oppgaverutenettet 


_**Gjelder:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering, Project for the web_

Oppgaverutenettet som distribueres av Dynamics 365 Project Operations, er en driftet iframe i Microsoft Dataverse. Som et resultat av denne bruken må spesifikke krav oppfylles for å sikre at autorisasjon og godkjenning fungerer som de skal. Denne artikkelen beskriver de vanlige problemene som kan ha innvirkning på muligheten til å gjengi rutenettet eller administrere oppgaver i arbeidsnedbrytningsstrukturen (WBS).

Vanlige problemer omfatter:

- Fanen **Oppgave** i oppgaverutenettet er tom.
- Når prosjektet åpnes, lastes ikke prosjektet inn, og brukergrensesnittet (UI) sitter fast på spinneren.
- Administrasjon av rettigheter for **Project for the Web**.
- Endringer lagres ikke når du oppretter, oppdaterer eller sletter en oppgave.

## <a name="issue-the-task-tab-is-empty"></a>Problem: Fanen Oppgave er tom

### <a name="mitigation-1-enable-cookies"></a>Løsning 1: Aktiver informasjonskapsler

Project Operations krever at informasjonskapsler fra tredjeparter er aktivert for å gjengi arbeidsnedbrytningsstrukturen. Når informasjonskapsler fra tredjeparter ikke er aktivert, vises en tom side i stedet for oppgaver når du velger kategorien **Oppgaver** på siden **Prosjekt**.

For nettleserne Microsoft Edge eller Google Chrome beskriver fremgangsmåtene nedenfor hvordan du oppdaterer nettleserinnstillingen slik at informasjonskapsler fra tredjeparter aktiveres.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Åpne Edge-nettleseren.
2. I hjørnet øverst til høyre velger du **ellipsen** (...), og deretter velger du **Innstillinger**.
3. Under **Informasjonskapsler og tillatelser på nettsteder** velger du **Informasjonskapsler og områdedata**.
4. Deaktiver **Blokker informasjonskapsler fra tredjeparter**.
5. Oppdater nettleseren din. 

#### <a name="google-chrome"></a>Google Chrome

1. Åpne Chrome-nettleseren.
2. Velg de tre vertikale prikkene øverst i høyre hjørne, og velg deretter **Innstillinger**.
3. Under **Personvern og sikkerhet** velger du **Informasjonskapsler og andre områdedata**.
4. Velg **Tillat alle informasjonskapsler**.
5. Oppdater nettleseren din. 

> [!NOTE]
> Hvis du blokkerer informasjonskapsler fra tredjeparter, blokkeres alle informasjonskapsler og områdedata fra andre områder, selv om området er tillatt i unntakslisten.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Løsning 2: Valider PEX-endepunkt er riktig konfigurert

Project Operations krever at en prosjektparameter refererer til PEX-endepunktet. Dette endepunkt kreves for å kommunisere med tjenesten som brukes til å gjengi arbeidsnedbrytningsstrukturen. Hvis parameteren ikke er aktivert, vises feilmeldingen Prosjektparameteren er ikke gyldig. Hvis du vil oppdatere PEX-endepunkt, følger du fremgangsmåten nedenfor.

1. Legg til feltet **PEX-endepunkt** på siden **Prosjektparametere**.
2. Finn produkttypen du bruker. Denne verdien brukes når PEX-endepunktet er angitt. Ved er produkttypen allerede definert i PEX-endepunktet. Behold den verdien.
3. Oppdater feltet med følgende verdi: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Tabellen nedenfor inneholder typeparameteren som skal brukes basert på produkttypen.

      | **Produkttype**                     | **Typeparameter** |
      |--------------------------------------|--------------------|
      | Project for the Web i standardorganisasjon   | type=0             |
      | Project for the Web i CDS-navngitt organisasjon | type=1             |
      | Project Operations                   | type=2             |

4. Fjern feltet fra siden **Prosjektparametere**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Løsning 3: Logg på project.microsoft.com
Åpne en ny fane i Microsoft Edge-nettleseren, gå til project.microsoft.com og logg på ved å bruke brukerrollen du bruker for å få tilgang til Project Operations.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problem: Prosjektet lastes ikke inn, og brukergrensesnittet står fast på spinneren

For godkjenning må popup-vinduer være aktivert for at oppgaverutenettet skal lastes inn. Hvis popup-vinduer ikke er aktivert, blir skjermen stående fast på innlastingsspinneren. Følgende grafikk viser nettadressen med en blokkert popup-etikett på adresselinjen, som fører til at spinneren blir sittende fast og prøver å laste siden. 

   ![Fast spinner og popup-blokk.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Løsning 1: Aktiver popup-vinduer

Når prosjektet står fast i spinneren, kan det hende at popup-vinduer ikke er aktivert.

#### <a name="microsoft-edge"></a>Microsoft Edge

Popup-vinduer kan aktiveres på to måter i Edge-nettleseren.

1. Velg varselet øverst til høyre i Edge-nettleseren.
2. Velg **Tillat alltid popup-vinduer og omdirigering fra** det bestemte Dataverse-miljøet.
 
     ![Vinduet Popup-vinduer er blokkert.](media/enablepopups.png)

Alternativt kan du også fullføre følgende trinn.

1. Åpne Edge-nettleseren.
2. Velg **ellipsen** (...) øverst i høyre hjørne, og velg deretter **Innstillinger** > **Områdetillatelser** > **Popup-vinduer og omdirigeringer**.
3. Slå på/av **Popup-vinduer og omdirigering** for å blokkere popup-vinduer, eller slå på popup-vinduer på enheten.
4. Når du har aktivert popup-vinduer, oppdaterer du nettleseren. 

#### <a name="google-chrome"></a>Google Chrome
1. Åpne Chrome-nettleseren.
2. Naviger til en side der popup-vinduer er blokkert.
3. Velg **Popup-vindu blokkert** på adresselinjen.
4. Velg koblingen for popup-vinduene du vil se.
5. Når du har aktivert popup-vinduer, oppdaterer du nettleseren. 

> [!NOTE]
> Hvis du alltid vil vise popup-vinduer for området, velger du **Tillat alltid popup-vinduer og omdirigeringer fra [nettsted]**, og deretter velger du **Ferdig**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problem 3: Administrasjon av rettigheter for Project for the Web

Project Operations er avhengig av en ekstern planleggingsservice. Tjenesten krever at en bruker har flere tilordnede roller som gjør det mulig for vedkommende å lese og skrive til enheter relatert til WBS. Disse enhetene omfatter prosjektoppgaver, ressurstilordninger og aktivitetsavhengigheter. Hvis en bruker ikke kan gjengi WBS-en når vedkommende navigerer til fanen **Oppgaver**, skyldes det sannsynligvis at **Prosjekt** for **Project Operations** ikke er aktivert. En bruker kan motta en sikkerhetsrolle eller en feil relatert til tilgangsfornektelse.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Løsning 1: Valider sikkerhetsrollene for programbrukere og sluttbrukere

1. Gå til **Innstilling** > **Sikkerhet** > **Brukere** > **Appbrukere**.  

   ![Applikasjonsleser.](media/applicationuser.jpg)
   
2. Dobbeltklikk appbrukeroppføringen for å kontrollere følgende:

     - Brukeren har tilgang til prosjektet. Dette kan du gjøre ved å kontrollere at brukeren har sikkerhetsrollen **Prosjektleder**.
     - Microsoft Project-appbrukeren finnes og er riktig konfigurert.
 
3. Hvis denne brukeren ikke finnes, oppretter du en ny brukeroppføring. 
4. Velg **Nye brukere**, endre oppføringsskjemaet til **Appbruker**, og legg deretter til **App-ID-en**.

   ![Detaljer for appbruker.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problem 4: Endringer lagres ikke når du oppretter, oppdaterer eller sletter en oppgave

Når du gjør én eller flere oppdateringer for WBS, mislykkes endringene og blir ikke lagret. Det vises en feil i tidsplanrutenettet med meldingen om at endringen du nylig har gjort, ikke kan lagres.

### <a name="mitigation-1-validate-the-license-assignment"></a>Løsning 1: Valider lisenstilordningen

1. Kontroller at brukeren er tilordnet riktig lisens, og at tjenesten er aktivert i tjenesteplandetaljene for lisensen.  
2. Kontroller at brukeren kan åpne **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Løsning 2: Valideringskonfigurasjon av prosjektappbrukeren
1. Kontroller at prosjektappbrukeren er opprettet.
2. Bruk følgende sikkerhetsroller for brukeren:
  
  - Dataverse-bruker eller basebruker
  - Project Operations-system
  - Prosjektsystem
  - System for dobbel skriving i Project Operations. Denne rollen er obligatorisk for ressursbaserte/ikke-lagerbaserte scenarioer i Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
