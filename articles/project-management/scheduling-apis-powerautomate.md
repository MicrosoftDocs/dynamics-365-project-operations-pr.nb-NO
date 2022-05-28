---
title: Bruk API-er for prosjektplan med Power Automate
description: Denne emne inneholder en eksempelflyt som bruker API-er (programmeringsgrensesnitt) for prosjektplan.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597718"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Bruk API-er for prosjektplan med Power Automate

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dette emnet beskriver en eksempelflyt som viser hvordan du oppretter en komplett prosjektplan ved å bruke Microsoft Power Automate, hvordan du oppretter et operasjonssett og oppdaterer en enhet. Eksemplet viser hvordan du oppretter et prosjekt, et prosjektteammedlem, operasjonssett, prosjektoppgaver og ressurstildelinger. Dette emnet forklarer også hvordan du oppdaterer en enhet og kjører et operasjonssett.

Følgende er en fullstendig liste over trinnene som er dokumentert i eksempelflyten i dette emnet:

1. [Opprett en PowerApps-utløser](#1)
2. [Opprette et prosjekt](#2)
3. [Initialiser en variabel for teammedlemmet](#3)
4. [Opprett et generelt teammedlem](#4)
5. [Opprett et operasjonssett](#5)
6. [Opprett en prosjektsamling](#6)
7. [Initialiser en variabel for koblingsstatusen](#7)
8. [Initialiser en variabel for antall oppgaver](#8)
9. [Initialiser en variabel for ID-en til prosjektoppgaven](#9)
10. [Utfør til](#10)
11. [Angi en prosjektoppgave](#11)
12. [Opprett en prosjektoppgave](#12)
13. [Opprett en ressurstildeling](#13)
14. [Reduser en variabel](#14)
15. [Gi nytt navn til en prosjektoppgave](#15)
16. [Kjør et operasjonssett](#16)

## <a name="assumptions"></a>Antagelser

Dette emnet forutsetter at du har grunnleggende kunnskaper om Dataverse-plattformen, skyflyter og API-en (programmeringsgrensesnitt) for prosjektplan. Hvis du vil ha mer informasjon, kan du se delen [Referanser](#references) senere i dette emnet.

## <a name="create-a-flow"></a>Opprett en flyt

### <a name="select-an-environment"></a>Velg et miljø

Du kan opprette Power Automate-flyten i miljøet ditt.

1. Gå til <https://flow.microsoft.com>, og bruk legitimasjonen for administrator for å logge på.
2. Velg **Miljøer** i øverste høyre hjørne.
3. Fra listen velger du miljøet der Dynamics 365 Project Operations er installert.

### <a name="create-a-solution"></a>Opprett en løsning

Følg disse trinnene for å opprette en [løsningsavhengig flyt](/power-automate/overview-solution-flows). Ved å opprette en løsningsklar flyt kan du enklere eksportere flyten for å bruke den senere.

1. I navigasjonsruten velger du **Løsninger**.
2. På **Løsninger**-siden velger du **Ny løsning**.
3. I dialogboksen **Ny løsning** angir du de obligatoriske feltene og velger deretter **Opprett**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Trinn 1: Opprett en PowerApps-utløser

1. På **Løsninger**-siden velger du løsningen du opprettet, og velger deretter **Ny**.
2. I den venstre ruten velger du **Skyflyter** \> **Automatisering** \> **Skyflyt** \> **Direkte**.
3. I **Flytnavn**-feltet skriver du inn **Schedule API Demo Flow**.
4. I listen **Velg hvordan denne flyten skal utløses** velger du **Power Apps**. Når du oppretter en Power Apps-utløser, er logikken opp til deg som forfatter. I dette emnet lar du inndataparameterne være tomme for testformål.
5. Velg **Opprett**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Trinn2: Opprett et prosjekt

Følg denne fremgangsmåten for å opprette et eksempelprosjekt.

1. Velg **Nytt trinn** i flyten du opprettet.

    ![Legg til et nytt trinn.](media/newstep.png)

2. I dialogboksen **Velg en operasjon** skriver du inn **utfør ubindet handling** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.

    ![Velg en operasjon.](media/chooseactiontab.png)

3. I det nye trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.

![Gi nytt navn til et trinn.](media/renamestep.png)

4. Endre navnet på trinnet til **Opprett prosjekt**.
5. I **Handlingsnavn**-feltet velger du **msdyn\_CreateProjectV1**.
6. Under **msdyn\_subject**-feltet velger du **Legg til dynamisk innhold**.
7. På **Uttrykk**-fanen i funksjonsfeltet skriver du inn **Prosjektnavn - utcNow()**.
8. Velg **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Trinn 3: Initialiser en variabel for teammedlemmet

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **initialiser variabel** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. I det nye trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.
4. Endre navnet på trinnet til **Initialiser teammedlem**.
5. Skriv inn **TeamMemberAction** i **Navn**-feltet.
6. Velg **Streng** i **Type**-feltet.
7. I **Verdi**-feltet angir du **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Trinn 4: Opprett et generelt teammedlem

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **utfør ubindet handling** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. I det nye trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.
4. Endre navnet på trinnet til **Opprett teammedlem**.
5. For **Handlingsnavn**-feltet velger du **TeamMemberAction** i dialogboksen **Dynamisk innhold**.
6. I **Handlingsparametere**-feltet angir du parameterinformasjonen nedenfor.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Her er en forklaring av parameterne:

    - **\@\@odata.type** – Enhetsnavnet. Skriv for eksempel inn **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – Primærnøkkelen for ID-en til prosjektteamet. Verdien er et GUID-uttrykk (globalt unik identifikator).   ID-en genereres fra uttrykksfanen.

    - **msdyn\_project\@odata.bind** – Prosjekt-ID-en til det eiende prosjektet. Verdien vil være dynamisk innhold som kommer fra svaret fra trinnet "Opprett prosjekt". Kontroller at du angir den fullstendige banen og legger til dynamisk innhold mellom parentesene. Anførselstegn er obligatoriske. Skriv for eksempel inn **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – Navnet på teammedlemmet. Skriv for eksempel inn **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Trinn 5: Opprett et operasjonssett

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **utfør ubindet handling** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. I det nye trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.
4. Endre navn på trinnet til **Opprett operasjonssett**.
5. I **Handlingsnavn**-feltet velger du den egendefinerte handlingen **msdyn\_CreateOperationSetV1** i Dataverse.
6. I **Beskrivelse**-feltet skriver du inn **ScheduleAPIDemoOperationSet**.
7. I **Prosjekt**-feltet skriver du inn **/msdyn\_projects(**.
8. I dialogboksen **Dynamisk innhold** velger du **msdyn\_CreateProjectV1Response ProjectId**.
9. I **Prosjekt**-feltet skriver du inn **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Trinn 6: Opprett en prosjektsamling

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **legg til ny rad** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. I det nye trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.
4. Endre navnet på trinnet til **Opprett samling**.
5. I **Tabellnavn**-feltet velger du **Prosjektsamlinger**.
6. I **Navn**-feltet skriver du inn **ScheduleAPIDemoBucket1**.
7. For **Prosjekt**-feltet velger du **msdyn\_CreateProjectV1Response ProjectId** i dialogboksen **Dynamisk innhold**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Trinn 7: Initialiser en variabel for koblingsstatusen

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **initialiser variabel** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. I det nye trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.
4. Endre navnet på trinnet til **Initialiser koblingsstatus**.
5. Skriv inn **linkstatus** i **Navn**-feltet.
6. Velg **Heltall** i **Type**-feltet.
7. Angi **192350000** i **Verdi**-feltet.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Trinn 8: Initialiser en variabel for antall oppgaver

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **initialiser variabel** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. I det nye trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.
4. Endre navnet på trinnet til **Initialiser antall oppgaver**.
5. Skriv inn **number of tasks** i **Navn**-feltet.
6. Velg **Heltall** i **Type**-feltet.
7. Angi **5** i **Verdi**-feltet.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Trinn 9: Initialiser en variabel for ID-en til prosjektoppgaven

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **initialiser variabel** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. I det nye trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.
4. Endre navnet på trinnet til **Init ProjectTaskID**.
5. Skriv inn **number of tasks** i **Navn**-feltet.
6. Velg **Streng** i **Type**-feltet.
7. For **Verdi**-feltet angir du **guid()** i uttrykksverktøyet.

## <a name="step-10-do-until"></a><a id="10"></a>Trinn 10: Utfør til

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **utfør til** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. Angi den første verdien i den betingede setningen til variabelen **number of tasks** fra dialogboksen **Dynamisk innhold**.
4. Angi betingelsen til **mindre enn eller lik**.
5. Angi den andre verdien i den betingede setningen til **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Trinn 11: Angi en prosjektoppgave

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **angi variabel** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. I det nye trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.
4. Endre navnet på trinnet til **Angi prosjektoppgave**.
5. I **Navn**-feltet velger du **msdyn\_projecttaskid**.
6. For **Verdi**-feltet angir du **guid()** i uttrykksverktøyet.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Trinn 12: Opprett en prosjektoppgave

Følg denne fremgangsmåten for å opprette en prosjektoppgave som har en unik ID som tilhører det gjeldende prosjektet og prosjektsamlingen du opprettet.

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **utfør ubindet handling** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. I trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.
4. Endre navnet på trinnet til **Opprett prosjektoppgave**.
5. I **Handlingsnavn**-feltet velger du **msdyn\_PssCreateV1**.
6. I **Enhet**-feltet angir du parameterinformasjonen nedenfor.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Her er en forklaring av parameterne:

    - **\@\@odata.type** – Enhetsnavnet. Skriv for eksempel inn **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – Den unike ID-en for oppgaven. Verdien må settes til en dynamisk variabel fra **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – Prosjekt-ID-en til det eiende prosjektet. Verdien vil være dynamisk innhold som kommer fra svaret fra trinnet "Opprett prosjekt". Kontroller at du angir den fullstendige banen og legger til dynamisk innhold mellom parentesene. Anførselstegn er obligatoriske. Skriv for eksempel inn **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** – Et hvilket som helst oppgavenavn.
    - **msdyn\_projectbucket\@odata.bind** – Prosjektsamlingen som inneholder oppgavene. Verdien vil være dynamisk innhold som kommer fra svaret fra trinnet "Opprett samling". Kontroller at du angir den fullstendige banen og legger til dynamisk innhold mellom parentesene. Anførselstegn er obligatoriske. Skriv for eksempel inn **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start** – Dynamisk innhold for startdatoen. I morgen blir for eksempel representert som **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – Den planlagte startdatoen. I morgen blir for eksempel representert som **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – Den planlagte sluttdatoen. Velg en dato i fremtiden. Angi for eksempel **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Koblingsstatusen. Angi for eksempel **"192350000"**.

7. For **OperationSetId**-feltet velger du **msdyn\_CreateOperationSetV1Response** i dialogboksen **Dynamisk innhold**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Trinn 13: Opprett et ressurstildeling

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **utfør ubindet handling** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. I trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.
4. Endre navnet på trinnet til **Opprett tildeling**.
5. I **Handlingsnavn**-feltet velger du **msdyn\_PssCreateV1**.
6. I **Enhet**-feltet angir du parameterinformasjonen nedenfor.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. For **OperationSetId**-feltet velger du **msdyn\_CreateOperationSetV1Response** i dialogboksen **Dynamisk innhold**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Trinn 14: Reduser en variabel

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **reduser variabel** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. Velg **number of tasks** i **Navn**-feltet.
4. Angi **1** i **Verdi**-feltet.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Trinn 15: Gi nytt navn til en prosjektoppgave

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **utfør ubindet handling** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. I trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.
4. Endre navnet på trinnet til **Gi nytt navn til prosjektoppgave**.
5. I **Handlingsnavn**-feltet velger du **msdyn\_PssUpdateV1**.
6. I **Enhet**-feltet angir du parameterinformasjonen nedenfor.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. For **OperationSetId**-feltet velger du **msdyn\_CreateOperationSetV1Response** i dialogboksen **Dynamisk innhold**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Trinn 16: Kjør et operasjonssett

1. Velg **Nytt trinn** i flyten.
2. I dialogboksen **Velg en operasjon** skriver du inn **utfør ubindet handling** i søkefeltet. Deretter velger du operasjonen i resultatlisten på **Handlinger**-fanen.
3. I trinnet velger du ellipsen (**...**) og velger deretter **Gi nytt navn**.
4. Endre navn på trinnet til **Utfør operasjonssett**.
5. I **Handlingsnavn**-feltet velger du **msdyn\_ExecuteOperationSetV1**.
6. For **OperationSetId**-feltet velger du **msdyn\_CreateOperationSetV1Response OperationSetId** i dialogboksen **Dynamisk innhold**.

## <a name="references"></a>Referanser

- [Oversikt over hvordan du integrerer flyter med Dataverse – Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Bruk API-er for prosjektplan til å utføre operasjoner med planleggingsenheter](schedule-api-preview.md)
- [Oversikt over skyflytene – Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Oversikt over løsningsavhengige flyter – Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
