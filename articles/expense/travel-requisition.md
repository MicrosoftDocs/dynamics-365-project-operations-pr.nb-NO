---
title: Reiserekvisisjoner
description: Dette emnet inneholder informasjon om reiserekvisisjoner.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 46a678ac4486c99f11d74dbac07dedd08364cb2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123750"
---
# <a name="travel-requisitions"></a>Reiserekvisisjoner

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

En reiserekvisisjon gir en oversikt over utgiftene som vil påløpe for reiseformål. En reiserekvisisjon sendes inn til gjennomgang og kan brukes til å autorisere utgifter.

Du kan bli bedt om å sende en reiserekvisisjon før du påløper noen som helst utgift som skal belastes organisasjonen. Dette kravet gjelder uansett om du betaler utgifter med et kredittkort som tilhører bedriften, bruker kontanter som du har mottatt fra forskudd, eller betaler utgifter av egen lomme som skal refunderes av organisasjonen.

Reiserekvisisjoner og policyer kan brukes til å administrere organisasjonens utgifter. Hvis for eksempel organisasjonen din arbeider med et fastprisprosjekt som krever reise, må reiseutgiftene for prosjektets teammedlemmer være innenfor prosjektbudsjettet. Ved å kreve at reiseutgifter godkjennes før de påløper, kan organisasjonen bidra til å sikre at prosjektet holder seg innenfor budsjettet.

## <a name="configuration"></a>Konfigurasjon 

Reiserekvisisjoner kan konfigureres som "obligatorisk" ved å aktivere parameteren "Forhåndsautorisasjon av reise er obligatorisk" i parametere for utgiftshåndtering. 

## <a name="create-and-submit-a-travel-requisition"></a>Opprette og sende en reiserekvisisjon

1. Gå til **Mine utgifter: Reiserekvisisjon**, og velg **Ny reiserekvisisjon**.
2. Angi et formål og et mål for rekvisisjonen.
3. Skriv inn eventuell tilleggsinformasjon i feltet **Reisebeskrivelse**. 
4. For hver av de forventede utgiftene, for eksempel flyreiser, måltider eller bilutleie, oppretter du et utgiftslinjeelement. Inkluder estimert dato, estimert beløp og valuta for hver utgift. 
5. Når du er ferdig med å legge til de forventede utgiftene, velger du **Lagre**.
6. Når du er klar til å sende inn reise rekvisisjonen, velger du **Arbeidsflyt** > **Send**.

Du kan vise godkjente reiserekvisisjoner under **Mine utgifter: Reiserekvisisjon**. 

## <a name="view-available-travel-requisitions"></a>Vise tilgjengelige reiserekvisisjoner

Du kan vise alle reiserekvisisjonene dine under **Mine utgifter: Reiserekvisisjoner**.

## <a name="approve-travel-requisitions"></a>Godkjenn reiserekvisisjoner

Velg reiserekvisisjonen du vil godkjenne, og velg deretter **Arbeidsflyt** > **Godkjenn**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Send inn en reiseregning ved hjelp av den godkjente reiserekvisisjonen

1. Opprett en ny reiseregning, og i hodet i reiseregningen, og fra listen over godkjente reiserekvisisjoner, velger du **Tilordne til reiserekvisisjon**.
2. Feltet **Beløp for reiserekvisisjon** oppdateres automatisk i hodet i reiseregningen.
3. Legg til hver utgift som er påløpt for reisen. Hvis feltet **Forhåndsgodkjent** er aktivert, oppdateres det avstemte beløpet og det godkjente beløpet for den spesifikke utgiftskategorien.

> [!NOTE]
> Når du tilordner en reiseregning til en godkjent reiserekvisisjon, kan ikke transaksjonsbeløpet være større enn det godkjente beløpet. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]