---
title: Hvordan tilpasser jeg forretningsprosessflyten for prosjektfaser?
description: En oversikt over hvordan du tilpasser forretningsprosessflyten for prosjektfaser.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: a999bbffff848db7a6349df380d9ed5e73c143ab
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125055"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Hvordan tilpasser jeg forretningsprosessflyten for prosjektfaser?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Det er en kjent begrensning i tidligere versjoner av programmet Project Service at navnene på fasene i forretningsprosessflyten for prosjektfaser må samsvare nøyaktig med de forventede engelske navnene (**Quote**, **Plan**, **Close**). Ellers vil ikke forretningslogikken som er avhengig av de engelske fasenavnene, fungere som forventet. Det er derfor du ikke ser kjente handlinger som for eksempel **Bytt prosess** eller **Rediger prosess** tilgjengelig på prosjektskjemaet, og det oppfordres ikke til tilpassing av forretningsprosessflyten. 

Denne begrensningen er håndtert i versjon 2.4.5.48 og senere. Denne artikkelen inneholder foreslåtte løsninger hvis du ønsker å tilpasse standard forretningsprosessflyt for tidligere versjoner.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Forretningslogikk krever nøyaktig samsvar med engelske fasenavn

Forretningsprosessflyten for prosjektfaser inneholder forretningslogikk som bidrar til følgende virkemåter i appen:
- Når prosjektet er knyttet til et tilbud, setter koden forretningsprosessflyten til **Quote**-fasen.
- Når prosjektet er knyttet til en kontrakt, setter koden forretningsprosessflyten til **Plan**-fasen.
- Når forretningsprosessflyten er gått videre til **Close**-fasen, deaktiveres prosjektoppføringen. Når prosjektet er deaktivert, settes prosjektskjemaet og arbeidsnedbrytningsstrukturen (WBS) til skrivebeskyttet, de navngitte ressursbestillingene lanseres, og eventuelle tilknyttede prislister deaktiveres.

Denne forretningslogikken er avhengig av de engelske navnene på prosjektfasene. Denne avhengigheten av de engelske fasenavnene er hovedårsaken til at det ikke oppfordres til å tilpasse forretningsprosessflyten for prosjektfaser, og hvorfor du ikke ser vanlige forretningsprosessflythandlinger som **Bytt prosess** eller **Rediger prosess** i prosjektenheten.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Hva skjer hvis fasenavnene ikke samsvarer med de engelske navnene?

Når fasenavnene i forretningsprosessflyten ikke samsvarer nøyaktig med de engelske fasenavnene, i Project Service-appen versjon 1.x på 8.2-plattformen, blir forretningslogikken som angir riktig fase for tilbud eller kontrakter eller som lukker prosjektet, hoppet over. Ingen feilmelding vises. Det virker derfor som at du kan tilpasse forretningsprosessflyten for prosjektfaser. Du kan imidlertid ikke se noen av de automatiske prosessene som jobber for tilbud, kontrakter, og prosjektlukking.

I Project Service-appen versjon 2.4.4.30 eller tidligere på 9.0-plattformen var det en betydelig arkitektonisk endring i forretningsprosessflyter som krevde en omskriving av forretningslogikken til forretningsprosessflyten. Hvis prosessfasenavnene ikke samsvarer med de forventede engelske navnene, får du derfor en feilmelding. 

Hvis du vil tilpasse forretningsprosessflyten for prosjektfaser for prosjektenheten, kan du altså bare legge til helt nye faser i standard forretningsprosessflyt for prosjektenheten mens du beholder fasene **Quote**, **Plan** og **Close** som de er. Denne begrensningen sikrer at du ikke får feil fra forretningslogikken som forventer engelske fasenavn i forretningsprosessflyten.

I versjon 2.4.5.48 eller nyere er forretningslogikken som er beskrevet i denne artikkelen, fjernet fra standard forretningsprosessflyt for prosjektenheten. Hvis du oppgraderer til denne versjonen eller senere, kan du tilpasse eller erstatte standard forretningsprosessflyt med din egen. 

## <a name="workarounds-for-earlier-versions"></a>Løsninger for tidligere versjoner

Hvis oppgradering ikke er noe alternativ, kan du tilpasse forretningsprosessflyten for prosjektfaser for prosjektenheten på en av disse to måtene:

1. Legg til flere faser i standardkonfigurasjonen samtidig som du beholder de engelske fasenavnene for **Quote**, **Plan** og **Close**.


![Skjermbilde av å legge til faser i standardkonfigurasjon](media/FAQ-Customize-BPF-1.png)
 
2. Opprett din egen forretningsprosessflyt og gjør den til den primære forretningsprosessflyten for prosjektenheten, som lar deg ha de fasenavnene du ønsker. Hvis du imidlertid vil bruke de samme standardprosjektfasene **Quote**, **Plan** og **Close**, må du utføre noen tilpassinger som er basert på de egendefinert fasenavnene. Den mer komplekse logikken er i lukkingen av prosjektet, som du fremdeles kan utløse ved å bare deaktivere prosjektoppføringen.

![BPF-tilpassing](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Andre hensyn for Project Service-appen versjon 2.4.4.30 eller tidligere på plattform 9.0

I Project Service 2.4.4.30 eller tidligere på plattform 9.0 med en egendefinert forretningsprosessflyt brukes **Fasenavn**-feltet på prosjektenheten i **Prosjekt etter fase**-diagrammet, og prosjektlistevisninger oppdateres ikke fordi det er koblet til standard forretningsprosessflyten for prosjektfaser. Du kan løse dette problemet med følgende trinn:

- Legg til et egendefinert felt for å fange opp gjeldende forretningsprosessflyttrinn som oppdateres når brukeren går gjennom den egendefinerte forretningsprosessflyten.

- Endre **Prosjekt etter fase**-diagrammet slik at det fungerer med det egendefinerte feltet i stedet for standardkonfigurasjonen.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Trinn for å opprette din egen forretningsprosessflyt for prosjektenheten

Slik oppretter du din egen forretningsprosessflyt for prosjektenheten:

1. Gå til **Innstillinger** > **Prosessenter**. Ikke kopier forretningsprosessflyten for prosjektfaser fordi dette kopierer også forretningslogikken for Project Service.

  ![Opprett prosess](media/FAQ-Customize-BPF-3.png)

2. Bruk prosessdesigneren til å opprette de fasenavnene du vil ha. Hvis du vil ha samme funksjonalitet som standardfasene for **Tilbud**, **Planlegg** og **Lukk**, må du opprette dette basert på fasenavnene i den egendefinerte forretningsprosessflyten.

   ![Skjermbilde av prosessdesigner som brukes til å tilpasse BPF](media/FAQ-Customize-BPF-4.png) 

3. I prosessdesigneren klikker du på **Ordreprosessflyt** for å gjøre den egendefinerte forretningsprosessflyten til den primære forretningsprosessflyten for prosjektenheten, ved å flytte den over forretningsprosessflyten for prosjektfaser til øverst i listen.


   [Skjermbilde av bruk av ordreprosessflyt](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Fremgangsmåten nedenfor bruker Project Service-appen 2.4.4.30 eller tidligere på 9.0-plattform

4. Legg til et nytt egendefinert felt i prosjektenheten for å registrere de egendefinerte fasene i den egendefinerte forretningsprosessflyten. Du må legge til forretningslogikk (plugin/arbeidsflyt) for å oppdatere dette feltet når fasen i den egendefinerte forretningsprosessflyten oppdateres.

   ![Skjermbilde av tilpassing av prosjektenhet](media/FAQ-Customize-BPF-6-720.png)

5. Endre **Prosjekt etter fase**-diagrammet slik at det bruker det nye egendefinerte feltet for faser.

   ![Skjermbilde av bruk av diagrammet Prosjekt etter fase](media/FAQ-Customize-BPF-7-720.png)

6. Endre eventuelle visninger for prosjektenheten for å ta med det nye egendefinerte feltet for faser.

   ![Skjermbilde av endring av visninger i prosjektenheten](media/FAQ-Customize-BPF-8-720.png)

