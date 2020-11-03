---
title: Oversikt over godkjenninger
description: Dette emnet gir information om å arbeide med godkjenninger i Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081480"
---
# <a name="approvals-overview"></a>Oversikt over godkjenninger

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Tids- og utgiftsoppføringer går gjennom en godkjenningsarbeidsflyt. Når oppføringene er godkjent, registreres transaksjoner i faktisk verdier, eller tiden bestilles i tidsplanen.

## <a name="approvals-workflow"></a>Godkjenningsarbeidsflyt
Når du oppretter og sender en tids- eller utgiftsoppføring, opprettes det en godkjenningsoppføring. Prosjektgodkjenneren eller lederen din ser gjennom og godkjenner oppføringen. Hvis oppføringen er relatert til et prosjekt blir de faktiske verdiene opprettet når den er godkjent. På denne måten kan kostnad og fakturering spores. 

## <a name="approve-an-entry"></a>Godkjenne en oppføring
På skjemaet **Godkjenninger** kan du bytte mellom forskjellige visninger, slik at du kan vise de forskjellige godkjenningstypene.
  
1. Gå til **Godkjenninger** -skjemaet, og velg **Utgifter** , **Tid** eller **Tilbakekallinger**.
2. Gå gjennom hver godkjenning, og velg de du vil godkjenne.
3. Velg **Godkjenn** for å godkjenne de valgte oppføringene.
Systemet behandler disse oppføringene og oppretter faktiske verdier eller en bestilling.

## <a name="reject-an-entry"></a>Avvise en oppføring
Som prosjektgodkjenner kan det hende du må sende en oppføring tilbake til en bruker for korrigering.
  
1. Gå til **Godkjenninger** -skjemaet, og velg oppføringen du vil avvise. 
2. Velg **Avvis**.
3. Valgfritt – Legg til en kommentar i dialogboksen **Avvisningskommentarer** for å informere brukeren hvorfor oppføringen blir avvist.
4. Velg **OK**. Oppføringen returneres til brukeren.
  
## <a name="recall-entries"></a>Tilbakekall oppføringer
Det kan hende du må kalle tilbake en oppføring som er sendt. Hvis oppføringen ikke er godkjent, returneres den umiddelbart. En godkjent oppføring har imidlertid kanskje en materialinnvirkning. Prosjektgodkjenneren må godkjenne tilbakekallingen for å kunne reversere transaksjonen i faktiske verdier.

## <a name="specify-project-approvers"></a>Angi prosjektgodkjennere
Hvert prosjekt har flere prosjektteammedlemmer. Du kan angi hvilke teammedlemmer som også er prosjektgodkjennere.

1. Gå til **Prosjekter** -skjemaet, og åpne prosjektet fra listen.
2. På **Team** -fanen velger du teammedlemmet som skal være en prosjektgodkjenner, og deretter velger du **Rediger**.
3. Sett feltet **Prosjektgodkjenner** til **Ja**.
4. Velg **Lagre**.
5. Gjenta trinn 2 til 4 hvis du vil legge til flere prosjektgodkjennere.

## <a name="configure-the-users-manager"></a>Konfigurere brukerens overordnede

1. Gå til **Innstillinger** > **Sikkerhet** > **Brukere**.
2. Velg brukeren som du tilordner en overordnet til, og velg lederen fra listen i området **Organisasjonsinformasjon**. 
3. Velg **Lagre**.


