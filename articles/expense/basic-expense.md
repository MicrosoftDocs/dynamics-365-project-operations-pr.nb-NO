---
title: Utgiftsoppføring (Lite)
description: Dette emnet gir informasjon om hvordan du arbeider medutgifts registrering i en Lite-distribusjon.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 539d0ba6be6f49a6f0509595a0776ef67135496d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276765"
---
# <a name="expense-entry-lite"></a>Utgiftsoppføring (Lite)

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Basic-, eller Lite-utgiftsbehandling er muligheten til å registrere enkle utgifter. Du kan registrere utgifter mot et prosjekt, og deretter vil prosjektgodkjenneren se gjennom og godkjenne dem.

Hvis du vil ha mer informasjon om utgiftsmuligheter i Dynamics 365 Project Operations, kan du se [Utgiftsoversikt](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Registrere en grunnleggende utgift

Du kan registrer utgiftene dine, slik at du kan sende dem til godkjenneren.

1. Gå til **Utgifter**, og velg **Ny**.
2. På siden **Ny utgift** angir du utgiftsinformasjonen, og deretter velger du **Lagre**.

## <a name="submit-a-basic-expense"></a>Sende inn en grunnleggende utgift

Når du er ferdig med å registrere alle utgiftene, og du er klar til å få dem godkjent, må du sende dem.

1. Gå til **Utgifter**, og velg en utgift. Du kan også velge alle utgiftene ved hjelp av avmerkingsboksen i hodet.
2. Velg **Send inn**. Systemet behandler de valgte oppføringene og oppretter deretter forespørsler om utgiftsgodkjenning.

## <a name="add-an-attachment"></a>Legg til et vedlegg

Det kan hende du må gi godkjenneren tilleggsdokumentasjon om utgiftene dine. Du kan legge ved en kvittering på tidslinjen for utgiftsoppføringen. Velg **Rediger** i **Tidslinje**-seksjonen, og velg deretter bindersikonet for å legge ved kvitteringen.

## <a name="recall-a-basic-expense"></a>Tilbakekalle en grunnleggende utgift

Når du sender inn en utgift ved en feil, kan du tilbakekalle den. Tiden som kreves for å tilbakekalle en utgiftsoppføring, avhenger av godkjenningsfasen.  Hvis godkjenneren ikke har godkjent oppføringen ennå, kan tilbakekallingen skje umiddelbart. Hvis imidlertid oppføringen allerede er godkjent, blir godkjenneren bedt om å godkjenne tilbakekallingen og tilbakeføre transaksjonene.

1. Gå til **Utgifter**, og velg deretter utgiften du vil tilbakekalle, i listen over utgifter.
2. Velg **Tilbakekall**. Hvis utgiftsoppføringen ennå ikke er godkjent, tilbakekaller systemet den umiddelbart. Hvis utgifts oppføringen allerede er godkjent, blir det opprettet en tilbakekallingsforespørsel for å varsle godkjenneren om at du vil reversere utgiften. Godkjenneren vil deretter bekrefte at reverseringen kan utføres, og oppføringen vil bli returnert.

## <a name="delete-a-basic-expense"></a>Slette en grunnleggende utgift

Utgifter som ennå ikke er sendt, kan slettes. Hvis du vil slette en utgift som allerede er sendt, må du først tilbakekalle den.

## <a name="see-also"></a>Se også

- [Oversikt over godkjenninger](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]