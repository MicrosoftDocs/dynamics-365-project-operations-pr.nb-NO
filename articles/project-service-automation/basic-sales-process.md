---
title: Salgsprosesser
description: Dette emnet gir informasjon om de grunnleggende salgsprosessene.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: a169dee5-f4a7-42c8-9bf1-7f0018cc25cb
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: eaaa4b8fe6577ff572489ac0c6abac3c4e970c63
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754129"
---
# <a name="sales-processes"></a>Salgsprosesser

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Salgsprosessene som brukes i en prosjektbasertert organisasjon, er forskjellig fra salgsprosessene som brukes i en produktbasert organisasjon. Denne forskjellen oppstår fordi salgssyklusene for prosjektrelaterte organisasjoner er lengre og krever egendefinerte forkalkuleringsteknikker for å analysere og opprette tilbud for hver avtale. Dynamics 365 Project Service Automation bruker noe av den samme funksjonaliteten som brukes i salgsprosessen for Dynamics 365 Sales. Her er noen eksempler:

- En kundeemneenhet brukes til å spore salgsprosessen.
- Kvalifiserte kundeemner spores som salgsmuligheter. Salgsprosessen kan også starte med salgsmulighet.
- Du får tilgang til alle relaterte artefakter for en salgsmulighet. Disse artefaktene inkluderer salgsteam, interessenter, sannsynlighet, vurdering, salgsfaser og forretningsprosesser.
- Det opprettes flere tilbud for en salgsmulighet.
- Et tilbud merkes som **Lukket som vunnet** for å opprette en salgsordre. Salgsordren tilpasses i PSA og kalles en prosjektkontrakt.

Illustrasjonen nedenfor viser en typisk salgsprosess i en prosjektbasert organisasjon.

> ![Salgsprosess i en prosjektbasert organisasjon](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Estimere et salg
Verdien av et salg kan estimeres basert på prosjekter som tidligere er levert, samt kompleksiteten i prosjekter. For prosjekter som omfatter utvidelser av tidligere prosjekter, eller prosjekter der leverandørens ekspertise er høy og velkjente arbeidsmaler brukes , kan du bruke en enklere estimeringsprosess. Mer komplekse prosjekter har vanligvis en lengre innkjøpsprosess. Derfor er det flere faser i salgsberegningsprosessen. Tidlig i prosessen bruker salgsteamet inndata fra regnskapsansvarlige eksperter på emnet til å komme i gang med å opprette en et estimat på høyt nivå for hver enkelt arbeidskomponent som tilbys. Disse arbeidskomponentene representeres av tilbudslinjer. 

Du kan opprette et estimat på høyt nivå for tilbudet. Til slutt blir dette estimatet på høyt nivå erstattet med et mer detaljert estimat som er basert på en prosjektplan som du oppretter ved hjelp av de standardiserte prosjektmalene. Disse malene hjelper deg med å bygge en tidsplan og bestemme pengeverdier i tilbudet og komponentene i det (tilbudslinjer). 

Du kan opprette flere tilbud for et prosjekt og gruppere dem under én enhetstype for salgsmulighet. Til slutt blir ett av disse tilbudene merket som **Lukket som vunnet**, og det opprettes en prosjektkontrakt eller en arbeidserklæring. En prosjektkontrakt inneholder den avtalte verdien for hver komponent (kontraktlinje) som godkjennes av kunden for levering. En arbeidserklæring opprettes vanligvis som et Microsoft Word-dokument. Alle fakturaer som sendes til kunden mens prosjektet pågår, refererer til prosjektkontrakten eller arbeidserklæringen.

Du kan også opprette alternative tilbud under én enhetstype for salgsmulighet eller sette opp systemet slik at en prosjektkontrakt opprettes når et tilbud blir vunnet. I dette tilfellet kan du legge ved et Word-dokument som representerer arbeidserklæringen, i prosjektkontraktoppføringen.

![Lukke et tilbud for å opprette en prosjektkontrakt](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Konfigurere salgsprosessen
Du kan bruke forretningsprosessflyter i Microsoft Dynamics 365 for å konfigurere salgsprosessen. Forretningsprosessflyter gir salgspersonellet et veiledet visuelt grensesnitt som de kan bruke til å flytte avtaler fremover gjennom fasene som er typiske for firmaet.

Firmaet kan for eksempel ha følgende seks faser i salgsprosessen:

1. Kvalifiser
2. Estimat
3. Intern gjennomgang
4. Kontrakt
5. Lever
6. Lukk

Disse seks fasene vises med vinkeltegn (\>) som du velger for å utvide hver enhetstype for salgsmulighet som du oppretter.

![Konfigurasjon av forretningsprosess i Dynamics 365](media/basic-guide-3.png)
 
Det kan hende at organisasjonen bruker forskjellige enheter til å representere samme avtale etter hvert som den utvikles. Tidlig i salgsprosessen er en avtale representert av salgsmulighetsenheten. Etter hvert som flere detaljer oppstår, kan du bruke forhåndsberegninger på høyt nivå til å opprette ett eller flere tilbud. Hvis ett av disse tilbudene blir kontrollert av interne interessenter og kundeinteressenter, representerer tilbudsenheten avtalen. Når kunden har godtatt tilbudet, representerer en prosjektkontrakt eller arbeidserklæring avtalen. For å støtte denne virkemåten er forretningsprosessflyter strukturert slik at hver fase i prosessen er koblet til en annen databasetabell.

**Kvalifiseringsfasen** i salgsprosessen kan støttes av en salgsmulighetsenhet. **Estimatfasen** og fasen med **intern gjennomgang** kan støttes av en tilbudsenhet. Fasene for **kontrakt**, **levering** og **lukking** kan støttes av en prosjektkontraktsenhet.

Etter hvert som du flytter avtaler gjennom fasene, blir du bedt om å opprette den riktige enhetsoppføringen for å hjelpe deg med å veilede deg gjennom prosessen. Fasene kan være betingede. Hvis du for eksempel bare trenger en intern gjennomgang av et tilbud hvis tilbudet bruker en egendefinert prisliste, kan du konfigurere den betingelsen i det riktige trinnet i forretningsprosessen. Fasen for **intern gjennomgang** vises deretter bare for tilbud som bruker en egendefinert prisliste. For alle andre avtaler og tilbud følges **estimatfasen** av **kontraktfasen**.

> [!NOTE]
> PSA har bestemte sider for salgsmuligheter, tilbud, ordrer og fakturaer. Du må opprette salgsmuligheter, tilbud, ordrer og fakturaer i Project Service ved hjelp av prosjektinformasjonssidene for disse enhetene. Hvis du bruker en annen side til å opprette en oppføring, kan du ikke åpne oppføringen fra siden **Prosjektinformasjon**. Hvis du vil åpne en oppføring fra siden **Prosjektinformasjon**, må du slette oppføringen og opprette den på nytt ved å bruke siden **Prosjektinformasjon**. På siden **Prosjektinformasjon** sørger forretningslogikken for hver av disse enhets typene for at **Type**-feltet for oppføringen angis på riktig måte, og alle de obligatoriske konseptene blir riktig initialisert.

> ![Prosjektinformasjon for en ny ordre](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Forskjeller mellom Project Service Automation og Sales
Selv om salgsprosessen i PSA bruker de grunnleggende funksjonene i salgsprosessen i Sales, er det noen viktige forskjeller på grunn av variasjoner i forretningspraksisen i prosjektrelaterte organisasjoner. Her er noen eksempler:

- **Prosjekttilbud** – i Project Service Automation lukkes et tilbud etter at en prosjektkontrakt er opprettet fra et tilbud. I Sales kan du ha et tilbud åpent etter at du har vunnet det. Årsaken til denne forskjellen er at et samsvar mellom et tilbud og en prosjektkontrakt er bedre for prosjektbaserte organisasjoner. 
- **Aktivering og revisjoner** – i PSA støttes ikke aktivering og revisjoner for prosjekttilbud. I Sales kan et tilbud låses for å forhindre ytterligere redigering.
- **Lukke et tilbud som tapt eller vunnet** – i PSA, når et prosjekttilbud lukkes som vunnet eller tapt, forblir salgsmuligheten åpen. Alle andre tilbud på salgsmuligheten lukkes som tapt. Når et tilbud lukkes som vunnet eller tapt i Sales, blir brukeren bedt om å utføre en handling på salgsmuligheten. Avhengig av brukerinndataene kan det hende at den underliggende salgsmuligheten lukkes eller forblir åpen.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Spore endringer i tilbud og prosjektplaner i salgssyklusen
I PSA kan du ikke spore endringer som er gjort i et tilbud. I stedet må du merke det eksisterende tilbudet som **Lukket som tapt** og deretter opprette et nytt tilbud. Du kan kopiere et tilbud eller klone et prosjektbasert tilbud ved hjelp av PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Spore kommentarer og godkjenninger av tilbud og prosjektkontrakter
Du kan administrere gjennomgang og godkjenning av tilbud og prosjektkontrakter ved hjelp av oppføringsveggen og innlegg. Organisasjonen kan opprette egendefinerte arbeidsflyter og plugin-moduler for å tilordne, omdirigere, videresende og administrere varslinger om arbeidselementer for gjennomgang og godkjenning.
