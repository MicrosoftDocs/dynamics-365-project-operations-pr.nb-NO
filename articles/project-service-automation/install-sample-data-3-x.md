---
title: Installasjon av eksempeldata
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
ms.technology: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.assetid: 8580fc8b-868a-42a3-aa04-2afab28d6de4
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 1c1300116fe42091620267fb128ca6c63184970e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754041"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Installasjon av eksempeldata for Project Service-programmet

For å gjøre det enklere for deg å bygge dine egne demonstrasjonsmiljøer tilgjengeliggjør Microsoft nedlastbare eksempeldatapakker som viser funksjonene i appene. Det finnes to typer eksempeldatapakker:
- referanse-/konfigurasjonsdata
- demonstrasjonsdata (referanse-/konfigurasjonsdata og transaksjonsdata som arbeidsordrer og prosjekter)

Eksempelpakkene med **referansedata** kan lastes ned i tre ulike pakker, slik at du kan installere data bare for Project Service, eller bare for Field Service, eller du kan installere eksempeldata for begge programmer samtidig.

Eksempeldatapakkene for konfigurasjon/referanse er:

- [**V902PSMasterData** - Bare Project Service versjon 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Bare Field Service versjon 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x og Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Den siste **demo**-datapakken er:

 - [**FPSDemoData** - Field Service 8.x og Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Installasjonsinstruksjonene er litt forskjellige i delen om brukerne som oppretter og konfigurerer, men resten er det samme som i forrige [**blogginnlegg**](https://aka.ms/fpsdemodatablog). Denne pakken har et redusert demodatasett og tar omtrent tre timer å installere.

Disse eksempeldatapakkene er bare tilgjengelige på engelsk.

> [!IMPORTANT]
> **Det finnes ingen måte å avinstallere eksempeldataene på.** Du må bare installere disse pakkene for demonstrasjon, evaluering, opplæring og testing av systemer. Merk også det ikke er støtte for å installere en individuell pakke, og deretter installere den andre individuelle pakken. (Du kan med andre ord ikke installere **FSMasterData** etterfulgt av **PSMasterData**, eller omvendt.) Hvis du tror du kommer til å trenge eksempeldata for begge programmene en gang i fremtiden, må du installere **v902FPSMasterData**-pakken.

Når du installerer en av eksempeldatapakkene, utfører installasjonsprosessen følgende handlinger:

- Oppretter eller angir standardparametere for å bruke Project Service, Field Service eller begge programmer (hvis aktuelt).

- Importerer eksempeldata for programmene, for eksempel ressurser som kan reserveres, programspesifikke roller, salgs- og kostprislister, organisasjonsenheter, salgsbehandlingsoppføringer og andre enheter for å demonstrere viktige funksjoner.  

Med **demodata**-pakken får du dataene ovenfor og flere transaksjonsdata som arbeidsordrer og prosjekter.

Lurer du på hvilke funksjoner du kan demonstrere med eksempeldataene? Se det fiktive scenariet Fabrikam Robotics i [Tekniske merknader](#technical-notes).

Hvis du har spørsmål om hvordan du installerer disse eksempeldatapakkene, kan du [sende en e-post på fpsdemodata@microsoft.com.](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Krav

Installasjonsprotokollen forutsetter følgende om målforekomsten (organisasjon):

- Originalspråket er engelsk og standardvalutaen er amerikanske dollar (USD, $).

- Organisasjonen har ingen Project Service- eller Field Service-data, eller har bare standarddata som følger med en ny organisasjon.

- Den riktige versjonen av forretningsprogrammet er allerede installert:
       
    - **For FPSDemoData eller v902FPSMasterData:** Organisasjonen har Field Service versjon 8.x og Project Service versjon 3.x installert.

    - **For v902PSMasterData:** Organisasjonen har Project Service versjon 3.x installert.

    - **For v902FSMasterData:** Organisasjonen har Field Service versjon 8.x installert.

> [!NOTE]
> Hvis du må installere eksempeldataene på en eksisterende prøveversjon eller et demonstrasjonsmiljø for Project Service og Field Service som allerede har data (anbefales ikke), må du først oppheve sikkerhetskontrollene som er utført av installasjonsprogrammet. Hvis du vil ha mer informasjon, kan du se Tekniske merknader nedenfor.

## <a name="prepare-for-installation"></a>Forberede installasjon

Du må kjøre installasjonsprogrammet på en datamaskin med en ny versjon av Windows (Windows 10 foretrukket).

Du bør planlegge at datamaskinen skal være tilkoblet et nettverk og installasjonen skal kjøre i opptil **1 time** for **konfigurasjons-/referansedata**. (Installasjonen tar vanligvis rundt 30 minutter for **FPSMasterData**, som inneholder eksempeldata for begge programmer.) For **FPSDemoData** tar installasjonen rundt **3 timer**.

Skjermbeskytteren på datamaskinen må være deaktivert. Øktlegitimasjonen for installasjonen kan ellers gå tapt når skjermbeskyttelsen aktiveres (med mindre du holder økten aktiv under hele installasjonen).

> [!div class="mx-imgBorder"]
> ![Skjermbilde av skjermbeskytterinnstillinger med skjermbeskytter deaktivert](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Laste ned og pakke ut

Installasjonsprogrammet for Project Service- og Field Service-eksempeldata distribueres som en selvutpakkende kjørbar fil. Filnavnene kan variere avhengig av eksempeldatapakken, men ellers er trinnene de samme uansett hvilken pakke du installerer.

Når du har lastet ned en pakke, kjører du EXE-filen og godtar vilkårene for å pakke ut den komprimerte zip-filen. Deretter må du pakke ut innholdet i denne filen til en mappe på datamaskinen.

Avhengig av operativsystemet og sikkerhetsinnstillingene, må du kanskje utføre følgende trinn når pakker ut zip-filen:

1. Finn og høyreklikk **FPSDemoData.dll**-filen i **v902FPSMasterData** / **PackageDeployer_FPSDemoData**-mappen.

2. Velg **Fjern blokkering**.

3. Velg **Bruk**.

4. Velg **OK**.


## <a name="create-or-configure-users"></a>Opprette eller konfigurere brukere

**FPSDemoData**-pakken krever seks brukere mens **FPSMasterData**-pakker krever én bruker. Referer til den riktige for eksempeldatapakken.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Opprette eller konfigurere brukere - konfigurasjons-/referansedatapakker

**FPSMasterData**-pakken er utformet for å installeres med én bruker kalt Spencer Low med innstillingene som beskrives her. For å installere pakken på riktig måte må du opprette (eller gi nytt navn midlertidig) brukere i miljøet for å samsvare med den innkommende konfigurasjonen av eksempeldataene.

Hvis du vil opprette eller konfigurere brukere, kan du gå til **Innstillinger** > **Sikkerhet** > **Brukere**, og gjøre følgende:

1. Angi UserFullname = "Spencer Low" med brukernavn "spencerl" (**små bokstaver**) til rollene prosjektleder og praksisleder.

2. Velg brukeren **Spencer Low**, og velger deretter **Behandle roller**. Finn og velg **Systemadministrator**-rollen, og velg deretter **OK** for å gi fulle administratorrettigheter til Spencer Low. Dette trinnet er nødvendig for å sikre at eksempelpostene opprettes med riktig brukereierskap, og derfor fyller ut visninger på riktig måte.

3. Fra den nedlastede pakken må du oppdatere en fil for datatilordning med e-postadressene til standard brukerkonteksten. Dette gjør du ved åpne **PkgFolder** og deretter finne og åpne **ImportUserMapFile.xml**-filen i Notisblokk (eller Visual Studio eller et annet redigeringsprogram for XML). Angi **DefaultUserToMapTo=**-feltet til e-postadressen til Spencer Low-brukeren.

4. Hvis du ikke bruker Spencer Low med brukernavn **spencerl**, må du oppdatere en ekstra fil. Åpne **DemoDataPreImportConfig.xml**-filen, og finn deretter **userstocreateandconfigure**-merket. Oppdater **\<login\>**-merket med brukernavnet til Spencer Low-brukeren. Hvis du vil ha mer informasjon, kan du se [Tekniske merknader](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Opprette eller konfigurere brukere - demodatapakke

Demodatapakken krever seks brukere. For at pakken skal installeres på riktig måte, gjør du følgende:

 1. Opprett eller midlertidig gi nytt navn til eksisterende brukere for å samsvare med innkommende eksempeldatakonfigurasjon ved å gå til **Innstillinger** > **Sikkerhet** > **Brukere**.
 
    Disse rollene er bare nødvendige for personbasert demonstrasjoner.  
    - Brukers fulle navn = "David So" som feltservicetekniker   
    - Brukers fulle navn = "Jamie Reding" som fordelingsansvarlig for kundeservice og feltservice   
    - Brukers fulle navn = "Molly Clark" som kontoadministrator   
    - Brukers fulle navn = "Spencer Low" som praksis- og prosjektleder  
    - Brukers fulle navn = "Veronica Quek" som teammedlem   
    - Brukers fulle navn = "William Contoso"
  
2. For demodataimportformål tilordner du de seks brukerne ovenfor administratorrollen slik at eksempeloppføringene importeres på riktig måte. 

3. Åpne **PkgFolder** og finn og åpne **ImportUserMapFile.xml**. Oppdater **Ny=**-feltene til e-postadressene for tilsvarende brukere i systemet.

   > [!div class="mx-imgBorder"]
   > ![Skjermbilde av UserMapFile](media/sample-data-7.png)

4. Hvis brukeren med fullt navn "Spencer Low" har en annen bruker-ID enn **"spencerl"**, må du oppdatere en ekstra fil. Åpne **DemoDataPreImportConfig.xml**, og finn **userstocreateandconfigure**-merket. Oppdater **\<pålogging\>**-merket med loginId (skilles mellom små og store bokstaver). 

5. Den første brukerens kalender (i **userstocreateandconfigure**-merket) brukes til å fylle ut arbeidstimene for alle reserverbare ressurser ved import av demonstrasjonsdata. Gå til **Innstillinger** > **Sikkerhet** > **Brukere**, finn brukeren "Spencer Low", og åpne Arbeidstimer-alternativet. Rediger eksisterende arbeidstimer, og velg **Hele den regelmessige ukeplanen fra begynnelse til slutt**-alternativet. Sikre at **arbeidstimer er satt til 8 AM - 5 PM (9 timer), mandag til fredag og tidssonen angitt til Stillehavskysten (USA og Canada)**. Dette er nødvendig for å sikre at prosjekt- og planleggingstavlen vises som forventet.

**Anbefaling:** Vurder å opprette en sikkerhetskopi av organisasjonen din nå, i tilfelle du må gå tilbake til startpunktet hvis noe går galt under installeringen av eksempeldata. Hvis du vil ha mer informasjon, kan du se [Sikkerhetskopiere og gjenopprette forekomster](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Kjør Package Deployer

1. Finn og kjør **PackageDeployer.exe** i **v902FPSMasterData**- ELLER **PackageDeployer_FPSDemoData**-mappen.

2. Godta vilkårene.

3. I neste vindu:

   a. Velg distribusjonstype **Office 365**.

   b. Bruk brukeren og passordet til systemadministrator-brukeren som er konfigurert i "Opprette eller konfigurere brukere" ("Spencer Low" med brukernavn "spencerl").

   c. Kontroller at **Vis liste over tilgjengelige organisasjoner** er merket av.

      > [!div class="mx-imgBorder"]
      > ![Skjermbilde av Package Deployer-vinduet med "Vis liste over tilgjengelige organisasjoner" valgt](media/sample-data-2.png)

4. Velg organisasjonen der du vil installere eksempeldataene.

5. Velg **Neste** til du ser dialogboksen **Oppsett av demonstrasjonsdata**.

   > [!div class="mx-imgBorder"]
   > ![Skjermbilde av statusvinduet for installasjon av demonstrasjonsdata](media/sample-data-3.png)

6. Før du fortsetter, bør du merke deg at installasjon av eksempeldata kan ta opptil en time (vanligvis ca. 10 minutter). Du må forsikre deg om datamaskinen forblir på og er koblet til et nettverk gjennom hele installasjonsprosessen, og at økten er aktiv.   

7. Når du er klar, kan du klikke **Neste** for å starte installeringen av eksempeldata. Etter at eksempeldataene er lastet inn, klikker du **Fullfør**.

## <a name="verify-the-sample-data-installation"></a>Kontroller installasjonen av eksempeldata

Utfør en sunnhetskontroll ved å kontrollere at antallet oppføringer og typer enheter som er oppført i det fiktive scenarioet Fabrikam Robotics, vises som forventet.

Etter at eksempeldataene er ferdig lastet, logger du på som Spencer Low-brukeren og kontrollerer følgende:

- Hvis Project Service -programmet er installert, kan du gå til **Project Service** > **Innstillinger** > **Prislister**. Kontroller at faktura- og kostnadssatsene finnes med riktig valuta for hvert land/område i datasettet.

- Hvis Project Service-appen er installert, går du til **Universal Resource Scheduling** > **Innstillinger** > **Organisasjonsenheter**. Kontroller at en kostprisliste med riktig valuta er knyttet til hver organisasjonsenhet (unntatt oppføringer for poststed). Hvis noen mangler, finn og tilknytt den riktige kostprislisten.

- Hvis Field Service -programmet er installert, kan du gå til **Project Service** > **Innstillinger** > **Prislister**. Kontroller at faktura- og kostnadssatser finnes. Gå til **Field Service** > **Innstillinger** > **Prislister**, og kontroller at faktura- og kostnadssatsene finnes med riktig valuta for hvert land/område i datasettet.

  > [!div class="mx-imgBorder"]
  > ![Skjermbilde av aktive prislister](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Skjermbilde av aktive organisasjonsenheter](media/sample-data-5.png)

## <a name="technical-notes"></a>Tekniske merknader

Nedenfor finner du mer teknisk informasjon om installasjon av dataene.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Installere eksempeldata på eksisterende data (anbefales ikke)

Hvis du må installere eksempeldataene på en eksisterende prøveversjon eller et demonstrasjonsmiljø for Field Service eller Project Service som allerede har data (anbefales ikke), må du først oppheve sikkerhetskontrollene som er utført av installasjonsprogrammet.

Hvis du vil gjøre dette, kan du gå til **PkgFolder**-mappen for å søke etter og åpne filen **DemoDataPreImportConfig.xml** med Notisblokk (eller et annet redigeringsprogram for XML).

Finn den følgende verdien, og endre deretter innstillingen fra sann til usann:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Denne endringen fører til at installasjonsprogrammet hopper over noen viktige sikkerhetskontroller, inkludert:

- Bekrefter at det ikke er mer enn én aktiv **Organisasjonsenhet**-oppføring, og endrer deretter navn til **Fabrikam US**.

- Bekrefter at det ikke er mer enn én aktiv **Arbeidsmal**-oppføring.

- Bekrefter at det ikke er mer enn én aktiv **Prosjektparameter**-oppføring, og endrer deretter oppføringen til **Parametere**.

### <a name="configuration-components"></a>Konfigurasjonskomponenter

Det finnes en rekke andre konfigurasjonskomponenter i denne konfigurasjonsfilen før import. For teknisk brukere inkluderer noen av disse:

- **\<RequiredSolutions\>** angir nødvendige løsningsinstallasjoner og deres versjonsnumre.

- **\<InstallSampleData\>** kontrollerer om medfølgende eksempeldata for appene er installert.

    - false - hopper over installasjon av disse innebygde dataene (som er flyttbare)

    - true - installerer de innebygde dataene samtidig med installering av FS- og PSA-eksempeldataene

- **\<PreImportDataCollection\>** angir flat fil-datatilordninger og tilknyttede oppføringer som skal importeres før installeringen av hovedeksempeldata.

- **\<EntitiesToEnableScheduling\>** angir hvilke enheter som skal aktiveres for booking i Microsoft Dynamics-planlegging (aka Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** angir ressurser som kan reserveres, som opprettes (hvis de ikke allerede finnes) før eksempeldataimporten utføres. Merk at ressursen som kan reserveres i kildesystemets eksempeldata samsvarer med målsystemets oppføringer for ressurs som kan reserveres, på FullName og påloggingen for hver ressurs. Det er derfor IKKE mulig å endre navnene i denne forhåndskonfigurasjonsfilen med mindre du først importerer eksempeldata til et målsystem ved hjelp av disse navnene, og deretter endrer navn på ressursene som reserveres, til ønsket navnsett sammen med de aktiverte brukeroppføringene, og deretter eksporterer dataene på nytt for import til de endelige målsystemet (ved å oppdatere gamle og nye **ImportUserMapFile.xml**-oppføringer tilsvarende).

- **\<PluginsToDisable\>** angir svært diskrete linjeelement-plugin-moduler som må være deaktivert under eksempeldataimporten, og deretter aktiveres på nytt etterpå.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Det fiktive scenarioet Fabrikam Robotics

Eksempelreferansedatapakkene for Field Service og Project Service installerer **Fabrikam Manufacturing Master Data (v3.0.0.0)-løsningen**, sammen med omtrent 4 000 oppføringer og omtrent 40 forskjellige enheter. De separate eksempeldatapakkene for Field Service eller Project Service inneholder et delsett av **v902FPSMasterData**-eksempeldataene for programmet. **Demodata**-pakken installerer **Fabrikam Manufacturing Demo Data (v3.0.0.7)-løsningen** med omtrent 22 000 oppføringer i 148 enheter.

Det fiktive selskapet Fabrikam Robotics er produsent av elektroniske samlebåndsroboter og er kjent for sin produktkvalitet, innovasjon og gode kundeservice, inkludert installasjonsplanlegging, implementering og pågående vedlikeholdstjenester. Fabrikam har hovedkvarter i USA (Fabrikam US), og har prosjektbaserte serviceoperasjoner i Frankrike, India, Storbritannia og Sveits.

Field Service-operasjoner er sentrert i USA, hovedsaklig i det større Seattle-området. Selskapet er fokusert på å unytte Tingenes Internett (IoT)-tilkobling for å overvåke kundeaktivaytelser og levere stadig mer proaktive tjenester på stedet.

En avansert oversikt over eksempeldataene er som følger:

- Felles eksempeldataelementer (inkludert for begge programmer)

    - 1 bruker

    - 71 forretningsforbindelser

    - 137 kontakter

    - Forskjellige transaksjonstyper og kategorier

    - 50 produkter med 1 produktprisliste

    - 14 pris-/kostlister

    - 31 egenskaper (ressursferdigheter) i 2 vurderingsmodeller med 3 nivåer (vurderingsverdier)

- Project Service

    - 8 organisasjonsenheter

    - 6 rollespesifikke utnyttelsesnivåer

    - 2,8 k + rolleprisspesifikasjoner

- Field Service

    - 4 distrikter

    - 5 arbeidsordretyper

    - 22 kundeaktiva

    - 9 hendelsestyper med en rekke tilknyttede ressursegenskaper (9), tjenester (13) og serviceoppgaver (13)
   
**Demodata**-pakken installerer omtrent 179 arbeidsordrer 12 prosjekter og tilknyttede transaksjonsdata. 

### <a name="change-the-work-hours-for-sample-resources"></a>Endre arbeidstimene for eksempelressurser

Som standard har alle ressurser som kan reserveres, en arbeidstidskalender på 24 timer.

Hvis du må endre arbeidstimer for eksempelressurser som kan reserveres, går du til **Universal Resource Scheduling** > **Planlegging** > **Ressurser**.

Velg en bruker (for eksempel Spencer Low), og endre Spencers arbeidstimer til timene du vil bruke for flere brukere. Gå til **Universal Resource Scheduling** > **Innstillinger** > **Arbeidstidsmaler** og rediger **Standard arbeidsmal**-oppføringen. I **Malressurs**-feltet velger du en bruker med arbeidstimer du vil bruke for andre ressurser. Gå til **Universal Resource Scheduling** > **Planlegging** > **Ressurser** > **Aktive ressurser som kan bestilles**. Velg ressursene du vil endre, og velg deretter **Angi kalender**. På **Arbeidsmal**-rullegardinlisten velger du **Standard arbeidstimer** eller en annen mal med riktig malressurs. Når du går til planleggingstavlen, skal du kunne se at ressursene nå har oppdaterte arbeidstimer.

> [!div class="mx-imgBorder"]
> ![Skjermbilde av aktive ressurser som kan reserveres](media/sample-data-6.png)
