---
title: Definere ressurskalendere
description: Dette emnet gir informasjon om hvordan du definerer arbeidstidskalendrene for ressurser i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081468"
---
# <a name="define-resource-calendars"></a>Definere ressurskalendere

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Hver bestillbare ressurs som arbeider i et prosjekt, må ha en kalender for arbeidstid for å definere tilgjengeligheten deres. Arbeidstimer for en ressurs kan defineres på to måter: 

   - Definere individuelle kalenderregler for en ressurs
   - Bruke en eksisterende kalendermal for ressursen

## <a name="define-a-resources-working-hours"></a>Definerer arbeidstimer for en ressurs

1. Velg **Ressurser** på **Ressurser** -menyen.
2. Velg den aktuelle **bestillbare ressursen** i rutenettvisningen.
3. På siden **Ressursdetaljer** velger du kategorien **Arbeidstid**. Som standard vil kalenderen for bestillbare ressurser ha arbeidstimene til standard arbeidstidsmal som er definert for organisasjonen.
4. Hvis du vil oppdatere arbeidstiden, høyre klikker du startdatoen for den foreslåtte kalenderregelen som skal defineres. Bruk kalenderregelmenyen til å definere en kalenderregel for en bestemt dag, resten av serien eller hele kalenderen.
5. Når alternativet er valgt, kan du deretter definere følgende:

    - Hvilken dag i uken arbeidstimene skal gjelde for.
    - Arbeidstiden for hver dag.
    - Den lokale tidssonen for kalenderregelen.
    - Hvis det er aktuelt, kan du også angi ikke-arbeidstid for regelen.

## <a name="applying-a-calendar-template-to-a-resource"></a>Bruke en kalendermal for en ressurs

1. Velg **Ressurser** på **Ressurser** -menyen.
2. I rutenettvisningen kan du velge opptil 25 **bestillbare ressurser** som skal oppdateres.
3. Velg **Angi kalender** , og en dialogboks vil be om en liste over tilgjengelige arbeidstidsmaler.
4. Velg malen malen du vil bruke, og velg deretter **Bruk**.
