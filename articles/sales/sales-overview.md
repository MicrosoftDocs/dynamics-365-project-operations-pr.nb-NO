---
title: Oversikt over salgsprosesser
description: Dette emnet gir informasjon om de grunnleggende salgsprosessene.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app: ''
ms.openlocfilehash: e66d96a940f3b22d5d1f3372d2b6767a4482d925
ms.sourcegitcommit: 7750485f8685a2ca5e1b3c165ead24a3b583c447
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3891902"
---
# <a name="sales-processes-overview"></a>Oversikt over salgsprosesser

Salgsprosessene som brukes i en prosjektbasertert organisasjon, er forskjellig fra salgsprosessene som brukes i en produktbasert organisasjon. Dette oppstår fordi salgssyklusene for prosjektrelaterte organisasjoner er lengre og krever egendefinerte forkalkuleringsteknikker for å analysere og opprette tilbud for hver avtale. Dynamics 365 Project Operations bruker noe av den følgende funksjonaliteten som brukes i en salgsprosess:

- En kundeemneoppføring brukes til å spore salgsprosessen.
- Kvalifiserte kundeemner spores som salgsmuligheter.
- Du får tilgang til alle relaterte artefakter for en salgsmulighet. Disse artefaktene inkluderer salgsteam, interessenter, sannsynlighet, vurdering, salgsfaser og forretningsprosesser.
- Det opprettes flere tilbud for en salgsmulighet.
- Et tilbud gis statusen **Lukket som vunnet** for å opprette en salgsordre. Salgsordren tilpasses i Project Operations og kalles en prosjektkontrakt.

## <a name="estimate-a-sale"></a>Estimere et salg
Verdien av et salg kan estimeres basert på prosjekter som tidligere er levert, samt kompleksiteten i prosjektene. For prosjekter som omfatter utvidelser av tidligere prosjekter, eller prosjekter der leverandørens ekspertise er høy og velkjente arbeidsmaler brukes , kan du bruke en enklere estimeringsprosess. Mer komplekse prosjekter har vanligvis en lengre innkjøpsprosess. Derfor er det flere faser i salgsberegningsprosessen. Tidlig i prosessen bruker salgsteamet inndata fra regnskapsansvarlige eksperter på emnet til å opprette et estimat på høyt nivå for hver enkelt arbeidskomponent som tilbys. Disse arbeidskomponentene representeres av tilbudslinjer. 

Du kan opprette et estimat på høyt nivå for tilbudet. Til slutt blir dette estimatet på høyt nivå erstattet med et mer detaljert estimat som er basert på en prosjektplan som du oppretter ved hjelp av de standardiserte prosjektmalene. Disse malene hjelper deg med å bygge en tidsplan og bestemme pengeverdier i tilbudet og komponentene i det (tilbudslinjer). 

Du kan opprette flere tilbud for et prosjekt og gruppere dem under én salgsmulighetsoppføring. Til slutt blir ett av tilbudene merket som **Lukket som vunnet**, og det opprettes en prosjektkontrakt eller en arbeidserklæring. En prosjektkontrakt inneholder den avtalte verdien for hver komponent (kontraktlinje) som godkjennes av kunden for levering. En arbeidserklæring opprettes vanligvis som et Microsoft Word-dokument. Alle fakturaer som sendes til kunden mens prosjektet pågår, refererer til prosjektkontrakten eller arbeidserklæringen.

Du kan også opprette alternative tilbud under én salgsmulighetsoppføring eller sette opp systemet slik at en prosjektkontrakt opprettes når et tilbud blir vunnet. I dette tilfellet kan du legge ved et Word-dokument som representerer arbeidserklæringen, i prosjektkontraktoppføringen.

## <a name="configure-the-sales-process"></a>Konfigurere salgsprosessen
Du kan bruke forretningsprosessflyter for å konfigurere salgsprosessen. Disse flytene gir et veiledet visuelt grensesnitt for å flytte avtaler fremover gjennom trinnene i salgsprosessen.

Firmaet kan for eksempel ha følgende seks faser i salgsprosessen:

1. Kvalifiser
2. Estimat
3. Intern gjennomgang
4. Kontrakt
5. Lever
6. Lukk
 
Det kan hende at organisasjonen bruker forskjellige enheter til å representere samme avtale etter hvert som den utvikles. Tidlig i salgsprosessen er en avtale representert av salgsmulighetsenheten. Etter hvert som flere detaljer oppstår, kan du bruke forhåndsberegninger på høyt nivå til å opprette ett eller flere tilbud. Hvis ett av disse tilbudene blir kontrollert av interne interessenter og kundeinteressenter, representerer tilbudsenheten avtalen. Når kunden har godtatt tilbudet, representerer en prosjektkontrakt eller arbeidserklæring avtalen. For å støtte denne virkemåten er forretningsprosessflyter strukturert slik at hver fase i prosessen er koblet til en annen databasetabell.

**Kvalifiseringsfasen** i salgsprosessen kan støttes av en salgsmulighetsenhet. **Estimatfasen** og fasen med **intern gjennomgang** kan støttes av en tilbudsenhet. Fasene for **kontrakt**, **levering** og **lukking** kan støttes av en prosjektkontraktsenhet.

Etter hvert som du flytter avtaler gjennom fasene, blir du bedt om å opprette den riktige enhetsoppføringen for å hjelpe deg med å veilede deg gjennom prosessen. Fasene kan være betingede. Hvis du for eksempel bare trenger en intern gjennomgang av et tilbud hvis tilbudet bruker en egendefinert prisliste, kan du konfigurere den betingelsen i det riktige trinnet i forretningsprosessen. Fasen for **intern gjennomgang** vises deretter bare for tilbud som bruker en egendefinert prisliste. For alle andre avtaler og tilbud følges **estimatfasen** av **kontraktfasen**.

> [!NOTE]
> Project Operations har spesifikke sider for enhetsoppføringer for salgsmulighet, tilbud, ordre og faktura. Du må opprette disse oppføringene ved hjelp av prosjektinformasjonssidene for disse enhetene. Hvis ikke kan du ikke åpne oppføringene fra siden **Prosjektinformasjon**. Hvis du vil åpne en oppføring fra siden **Prosjektinformasjon**, må du slette oppføringen og opprette den på nytt ved å bruke siden **Prosjektinformasjon**, der forretningslogikken for hver av disse enhetstypene sikrer at **Type**-feltet for oppføringen er riktig angitt, og at alle de obligatoriske konseptene er riktig initialisert.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Spore endringer i tilbud og prosjektplaner i salgssyklusen
I Project Operations kan du ikke spore endringer som er gjort i et tilbud. I stedet må du merke det eksisterende tilbudet som **Lukket som tapt** og deretter opprette et nytt tilbud. Du kan kopiere et tilbud eller klone et prosjektbasert tilbud.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Spore kommentarer og godkjenninger av tilbud og prosjektkontrakter
Du kan administrere gjennomgang og godkjenning av tilbud og prosjektkontrakter ved hjelp av oppføringsveggen og innlegg. Organisasjonen kan opprette egendefinerte arbeidsflyter og plugin-moduler for å tilordne, omdirigere, videresende og administrere varslinger om arbeidselementer for gjennomgang og godkjenning.
