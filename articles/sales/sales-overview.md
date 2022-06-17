---
title: Oversikt over salgsprosess
description: Denne artikkelen inneholder informasjon om grunnleggende salgsprosesser.
author: rumant
ms.date: 10/29/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 27b6b1e6f4d33ae1f8cfafba306b533e12c0cd2b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933159"
---
# <a name="sales-process-overview"></a>Oversikt over salgsprosess

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Salgsprosessene som brukes i en prosjektbasertert organisasjon, er forskjellig fra salgsprosessene som brukes i en produktbasert organisasjon. Dette oppstår fordi salgssyklusene for prosjektrelaterte organisasjoner er lengre og krever egendefinerte forkalkuleringsteknikker for å analysere og opprette tilbud for hver avtale. Dynamics 365 Project Operations bruker noe av følgende funksjonalitet som brukes i en salgsprosess:

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
Du kan administrere gjennomgang og godkjenning av tilbud og prosjektkontrakter ved hjelp av oppføringsveggen og innlegg. Organisasjonen kan opprette egendefinerte arbeidsflyter og programtillegg for å tilordne, omdirigere, videresende og administrere varslinger om arbeidselementer for gjennomgang og godkjenning.


[!INCLUDE[footer-include](../includes/footer-banner.md)]