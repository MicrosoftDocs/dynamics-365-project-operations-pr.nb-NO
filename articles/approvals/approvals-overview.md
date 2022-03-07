---
title: Oversikt over godkjenninger
description: Dette emnet gir information om å arbeide med godkjenninger i Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 9148c9f55e8664850c38aebbc9c4bbaa243475ad
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368668"
---
# <a name="approvals-overview"></a>Oversikt over godkjenninger

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Innsendinger av tids-, utgifts- og materialbruk flyttes gjennom en arbeidsflyt for godkjenning. Når oppføringene er godkjent, registreres transaksjoner i faktisk verdier, eller tiden bestilles i tidsplanen.

## <a name="approvals-workflow"></a>Godkjenningsarbeidsflyt
Når du oppretter og sender en oppføring for tids-, utgifts- eller materialbruk, opprettes det en godkjenningsoppføring. Prosjektgodkjenneren eller -lederen ser gjennom og godkjenner oppføringen. Hvis oppføringen er relatert til et prosjekt, opprettes de faktiske dataene når den er godkjent. På denne måten kan kostnad og fakturering spores.

## <a name="approve-an-entry"></a>Godkjenne en oppføring
**Godkjenninger**-siden gjør det mulig å veksle mellom ulike visninger, slik at du kan vise de ulike godkjenningstypene.
  
1. Gå til **Godkjenninger**-siden, og velg **Utgifter**, **Tid**, **Materialbruk** eller **Tilbakekallinger**.
2. Gå gjennom hver godkjenning, og velg de du vil godkjenne.
3. Velg **Godkjenn** for å godkjenne de valgte oppføringene.
Systemet behandler disse oppføringene og oppretter faktiske data.

## <a name="reject-an-entry"></a>Avvise en oppføring
Som prosjektgodkjenner kan det hende du må sende en oppføring tilbake til en bruker for korrigering.
  
1. Gå til **Godkjenninger**-siden, og velg oppføringen som skal avvises. 
2. Velg **Avvis**.
3. Du kan eventuelt legge til en kommentar i dialogboksen **Avvisningskommentarer** for å informere brukeren om hvorfor oppføringen blir avvist.
4. Velg **OK**. Oppføringen returneres til brukeren.
  
## <a name="cancel-approval"></a>Avbryt godkjenning
I noen tilfeller kan det hende du må annullere en tidligere godkjent oppføring. Annullering av en tidligere godkjent oppføring vil ha økonomisk innvirkning. 

## <a name="approving-recall-requests"></a>Godkjenning av tilbakekallingsforespørsler
I noen tilfeller kan det hende at en konsulent må tilbakekalle en tidligere godkjent oppføring. Annullering av en tidligere godkjent oppføring vil ha økonomisk innvirkning. Prosjektgodkjenneren må godkjenne tilbakekallingen for å kunne reversere transaksjonen i Faktiske verdier.

## <a name="specify-project-approvers"></a>Angi prosjektgodkjennere
Hvert prosjekt har flere prosjektteammedlemmer. Du kan angi hvilke teammedlemmer som også er prosjektgodkjennere.

1. Gå til **Prosjekter**-siden, og åpne prosjektet fra listen.
2. På **Team**-fanen velger du teammedlemmet som skal være en prosjektgodkjenner, og deretter velger du **Rediger**.
3. Sett feltet **Prosjektgodkjenner** til **Ja**.
4. Velg **Lagre**.
5. Gjenta trinn 2 til 4 hvis du vil legge til flere prosjektgodkjennere.

## <a name="configure-the-users-manager"></a>Konfigurere brukerens overordnede

1. Gå til **Innstillinger** > **Sikkerhet** > **Brukere**.
2. Velg brukeren som du tilordner en overordnet til, og velg lederen fra listen i området **Organisasjonsinformasjon**. 
3. Velg **Lagre**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
