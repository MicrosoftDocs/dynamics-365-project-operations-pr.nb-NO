---
title: Prosjektjusteringer
description: Denne artikkelen inneholder informasjon om prosjektjusteringer.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788305"
---
# <a name="project-adjustments"></a>Prosjektjusteringer

_**Gjelder for:** Project Operations for lagerførte/produksjonsbaserte scenarioer_

## <a name="adjustments-overview"></a>Justeringsoversikt

Du kan konfigurere Microsoft Dynamics 365 Project Operations slik at brukere kan gjøre endringer i posterte transaksjoner. Du kan justere prosjekttransaksjoner enkeltvis eller velge flere transaksjoner om gangen i en liste over alle prosjekttransaksjoner. Prosjektjusteringer brukes for eksempel til å masseoppdatere den fakturerbare statusen, beregne kostnadene på nytt etter en konfigurasjonsendring eller oppdatere finansieringskilder.

Brukere kan få tilgang til funksjonaliteten for prosjektjustering på flere måter:

- De kan bruke siden **Juster transaksjoner**, som de får tilgang til fra **Prosjektstyring og regnskap** \> **Oppsett**.
- De kan bruke **Justering**-knappen på siden **Posterte prosjekttransaksjoner**, som de får tilgang til fra **Prosjektstyring og regnskap** \> **Transaksjoner**.
- De kan bruke **Justering**-knappen på siden **Posterte prosjekttransaksjoner** i konteksten for et prosjekt. Denne siden er tilgjengelig fra **Prosjektstyring og regnskap** \> **Alle prosjekter**.

Hvis du vil tillate justeringer, må du aktivere én eller flere transaksjonsstatuser **Prosjektstyring og regnskap** \> **Parametere for prosjektstyring og regnskap** i **Generelt**-fanen under **Tillat justering av transaksjonsstatus**. Eksempler på transaksjonsstatuser omfatter posterte transaksjoner, fakturerte transaksjoner eller eliminerte transaksjoner. Alle transaksjonsstatuser som **Nei** er angitt for, har transaksjoner i denne statusen som ikke vises i justeringsprosessen og ikke kan velges for justering.

Et konfigurasjonsalternativ kalt **Opprett alltid justeringstransaksjon** er for øyeblikket tilgjengelig i Parametere for prosjektstyring og regnskap. Du kan deaktivere dette alternativet for å oppdatere den opprinnelige transaksjonen i stedet for å opprette nye transaksjoner under justering i et delsett med scenarioer. Det er kunngjort at denne parameteren blir avskrevet 1. mars 2023. Etter 1. mars 2023 fungerer systemet alltid som om alternativet er aktivert.

## <a name="adjustments-process-flow"></a>Flyt for justeringsprosess

Fremgangsmåten nedenfor viser den vanlige flyten for behandling av justeringer.

1. Åpne siden **Prosjektjusteringer**.
2. Velg **Velg** for å søke etter transaksjoner som oppfyller de forventede justeringsvilkårene.
3. Velg alle transaksjoner eller et delsett av transaksjonene for justering i listen over transaksjoner.
4. Velg **Juster**, og endre attributtene på linjen. Hvis verdiene ble angitt manuelt under transaksjonsregistreringen, kan du alternativt velge å angi standard systemverdier.
5. Listen over transaksjoner returneres, og det vises et merke i kolonnen **Ventende justering** for å angi hvor endringer ble gjort. Eventuelle justeringer som har ventende endringer, vises på nedre halvdel av siden. Der kan du gjøre flere detaljerte endringer utover de som ble vist på forrige side.
6. Velg **Poster** for å postere justeringstransaksjonene.

Avhengig av konfigurasjonen opprettes det vanligvis nye transaksjoner for justeringen.

- Feltet **Fakturastatus** for den opprinnelige transaksjonen er satt til **Justert**.
- En tilbakeføringstransaksjon opprettes for å tilbakeføre den opprinnelige transaksjonen, og **Status**-feltet settes til **Justert**.
- Det opprettes en ny transaksjon som har endringene som ble gjort i justeringsprosessen.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Valg av flere posterte prosjekttransaksjoner om gangen for justeringer og kreditnotaer

En ny funksjon som ble innført i 10.0.30-versjonen gjør at det går an å velge flere transaksjoner for justering om gangen fra siden **Posterte prosjekttransaksjoner**.

Før du kan bruke denne funksjonen, må du aktivere den i systemet. Administratorer kan bruke arbeidsområdet **Funksjonsbehandling** til å kontrollere funksjonsstatusen og aktivere den om nødvendig. Søk etter og velg **Velg flere posterte prosjekttransaksjoner for justeringer og kreditnotaer** i arbeidsområdet **Funksjonsbehandling**, og velg deretter **Aktiver nå**.

Denne funksjonen aktiverer følgende funksjonalitet:

- Du får tilgang til den fra siden for postert transaksjon i et prosjekt ved å bruke den eksisterende **Justering**-knappen.
- Den aktiverer en kontroll for valg av flere rader på siden **Posterte prosjekttransaksjoner**. Du kan bruke filtre på listesiden og velge oppføringene før du begynner justeringene.
- Den deaktiverer **Justering**-knappen hvis én enkelt transaksjon ikke kan justeres, eller hvis du velger en kombinasjon av kreditnotaer og journaler sammen i stedet for enkeltvis.
- På grunn av tilføyingen av kontrollen for valg av flere deaktiveres ikke lenger koblingen **Igangsatt kost** på båndet, hvis flere rader er valgt.
- Følgende advarsel tilføyes: «Du har valgt flere enn (valgt antall) oppføringer for justering. Det kan ta litt tid å fortsette med denne handlingen. Er du sikker på at du vil fortsette med denne handlingen?»

Denne funksjonen fjerner også trinn 2 fra prosessflyten som ble beskrevet tidligere i denne artikkelen. Alle transaksjoner som ble valgt før siden **Juster transaksjoner** ble åpnet, tas derfor med i listen over transaksjoner for justering. Du trenger ikke å bruke **Velg**-knappen til å søke etter dem.

> [!NOTE] 
> Selv om denne funksjonen er deaktivert, kan du likevel velge flere oppføringer for justering. Det er imidlertid bare én oppføring som *forblir valgt*, og dialogboksen **Velg transaksjoner** vises like etter at du har valgt å åpne justeringer.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Statuser for justeringstransaksjoner som kan aktiveres eller deaktiveres for justeringer

Følgende statuser kan aktiveres eller deaktiveres i **Generelt**-fanen på siden **Parametere for prosjektstyring og regnskap**:

- Lagt inn
- Fakturaforslag
- Fakturert
- Estimert
- Eliminert
- Startsaldo (time)

## <a name="adjustment-parameters"></a>Justeringsparametere

Disse parameterne vises på siden **Parametere for prosjektstyring og regnskap** i **Generelt**-fanen i **Justering**-gruppen og endrer hvordan justeringer behandles. 

| Parameternavn | Bekrivelse |
|----------------|-------------
| Opprett alltid justeringstransaksjon | Hvis denne parameteren aktiveres, oppretter alltid justeringsprosessen en ny tilbakeføringstransaksjon og en ny justert transaksjon når finans eller rapportering påvirkes. Hvis parameteren deaktiveres, oppdaterer justeringsprosessen den opprinnelige transaksjonen i stedet for å opprette en tilbakeføring og en ny transaksjon for et scenario, for eksempel en oppdatering av transaksjonsteksten. |
| Oppdater felt automatisk | Hvis denne parameteren aktiveres, beregner systemet kostpris og salgspris på nytt. |
| Bruk justeringsdato som nytt prosjekt | Denne parameteren brukes til å flytte transaksjoner til en fremtidig regnskapsperiode før systemet støttet denne funksjonen. Vi anbefaler at du ikke bruker den, fordi den endrer forretningsdatoen for transaksjonen og blir avskrevet i en fremtidig versjon. |
| Tillat lukkede aktiviteter | Transaksjoner kan vanligvis ikke opprettes for lukkede aktiviteter. Hvis denne parameteren aktiveres, overstyres denne funksjonaliteten. Justeringer kan derfor opprettes for lukkede aktiviteter. |
