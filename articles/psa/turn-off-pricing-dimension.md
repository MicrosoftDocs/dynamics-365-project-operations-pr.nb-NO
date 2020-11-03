---
title: Deaktivere en prisdimensjon
description: Dette emnet viser hvordan du konfigurerer prisdimensjoner i Project Service- løsningen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081705"
---
# <a name="turn-off-a-pricing-dimension"></a>Deaktivere en prisdimensjon

Det kan hende du må se gjennom og oppdatere prisstrategien med noen års mellomrom. Eventuelle oppdateringer du gjør, krever kanskje at du slår av en eksisterende prisdimensjon og oppretter en ny. Du kan for eksempel tidligere ha priset etter **Rolle** , men du har nå bestemt deg for å prise etter **Arbeidserfaring**. Dette kan kreve at du deaktiverer **Rolle** som en prissettingsdimensjon og oppretter **Arbeidserfaring** som en ny prissetingsdimensjon. 

Hvis du slår av en prisingsmodell, uavhengig av om den er standard eller egendefinert, kan det utføres ved å sette feltene **Gjelder kostnad** og **Gjelder salg** for prisingsdimensjonen til **Nei**.

Når du gjør dette, kan du imidlertid få følgende feilmelding:

![Feil ved forretningsprosess er sannsynlig når du slår av en prissettingssdimensjon](media/Business-Process-Error.png)


Denne feilmeldingen angir at det finnes prisoppføringer som tidligere ble angitt for dimensjonen, som blir deaktivert. Alle **Rollepris** - og **Rolleprispåslag** -oppføringer som refererer til en dimensjon, må slettes før dimensjonens bruk kan settes til **Nei**. Denne regelen gjelder både for standard prisdimensjoner og egendefinerte prisdimensjoner som du kan ha opprettet. Årsaken til denne valideringen er at Project Service har en begrensning om at hver **Rollepris** -oppføring må ha en unik kombinasjon av dimensjoner. For eksempel, på en prisliste som kalles **Amerikanske kostsatser 2018** , har du følgende **Rollepris** -rader. 

| Standardtittel         | Organisasjonsenhet    |Enhet   |Pris  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Systemingeniør|Contoso US|Hour| 100|USD|
| Senior systemingeniør|Contoso US|Hour| 150| USD|


Når du deaktiverer **Standardtittel** som prisdimensjon, og Project Service-prismotoren søker etter en pris, vil den bare bruke verdien **Organisasjonsenhet** fra inndatakonteksten. Hvis **Organisasjonsenhet** i inndatakonteksten er "Ekeli USA", vil resultatet være ikke-deterministisk, fordi begge radene samsvarer. For å unngi dette scenarioet, validerer Project Service at kombinasjonen av dimensjoner er unik når du oppretter **Rollepris**. Hvis dimensjonen er deaktivert etter at **Rollepris** -oppføringene er opprettet, kan denne begrensningen brytes. Derfor kreves det at du sletter alle **Rollepris** - og **Rolleprispåslag** -rader som har denne dimensjonsverdien fylt ut, før du slår av dimensjonen.
