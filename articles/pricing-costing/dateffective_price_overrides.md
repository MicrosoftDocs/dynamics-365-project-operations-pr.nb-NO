---
title: Datoeffektive prisoverstyringer
description: Denne artikkelen forklarer hvordan du konfigurerer prisoverstyringer for bestemte priser i prislisten.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445975"
---
# <a name="date-effective-price-overrides"></a>Datoeffektive prisoverstyringer 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

*Datoeffektive prisoverstyringer* gjør at du kan overstyre eller endre bestemte priser i prislisten. La oss for eksempel si at du har en standard prisliste som gjelder fra 1. januar 2022 til og med 31. desember 2022. Denne prislisten har priser for mange roller. Prisen som er definert for rollen **Nettverkstekniker**, er USD 100 per time. Når en nettverkstekniker logger tid mellom 1. januar 2022 og 31. desember 2022, blir tiden priset til USD 100. 1. oktober 2022 må du justere prisen *bare* for rollen **Nettverkstekniker**, fra USD 100 per time til USD 110 per time. Funksjonen **Datoeffektive prisoverstyringer** lar deg konfigurere denne endringen som en overstyring av raden for denne bestemte rolleprisen. Derfor trenger du ikke å kopiere hele prislisten og endre prisen i bare den ene raden.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Datoeffektive prisoverstyringer for arbeidspriser

Fremgangsmåten for å konfigurere datoeffektive prisoverstyringer for arbeidstid på et prosjekt, består av to grunnleggende trinn.

1. Aktiver funksjonen **Datoeffektive prisoverstyringer**.
1. Konfigurer en datoeffektiv prisoverstyring.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Aktiver funksjonen Datoeffektive prisoverstyringer

> [!NOTE]
> Etter at funksjonen **Datoeffektive prisoverstyringer** er aktivert, kan den ikke deaktiveres.

Følg denne fremgangsmåten for å aktivere funksjonen **Datoeffektive prisoverstyringer**.

1. Gå til **Innstillinger** \> **Parametere**.
1. Åpne oppføringen **Parametere**.
1. Velg **Aktiver datoeffektive prisoverstyringer** i fanen **Funksjonskontroll** i handlingsruten.
1. Velg **OK** i bekreftelsesdialogboksen.
1. Oppdater nettleseren etter en liten stund. Funksjoner for datoeffektiv prisoverstyring skal nå være tilgjengelige. Du kan se at disse funksjonene er aktivert hvis knappen **Aktiver datoeffektive prisoverstyringer** ikke lenger vises i handlingsruten.

### <a name="set-up-a-date-effective-price-override"></a>Konfigurer en datoeffektiv prisoverstyring

Datoeffektive prisoverstyringer kan konfigureres for prislister for **Kostnad**, **Salg** eller **Kjøp**.

> [!NOTE]
>Funksjonaliteten til **Datoeffektive prisoverstyringer** har for øyeblikket følgende begrensninger:
>
> - Bare rollepriser og rolleprispåslag støtter funksjonen **Datoeffektive prisoverstyringer** i Project Operations.
> - Når du kopierer en prisliste ved hjelp av handlingen **Kopier** på siden **Prislistedetaljer**, og når du oppretter en prosjektprisliste fra en standard eller egendefinert prisliste under kontraktopprettelse, kopieres **ikke** datoeffektive prisoverstyringer fra kildeprislisten.

Følg denne fremgangsmåten for å konfigurere en datoeffektiv prisoverstyring for en rollepris eller et rolleprispåslag.

1. Åpne siden for prislisten du vil konfigurere den datoeffektive prisoverstyringen for.
1. Velg fanen **Rollepriser**. Denne fanen viser alle **Rollepris**-oppføringene i prislisten.
1. Velg **Rollepris**-oppføringen du vil konfigurere en ny datoeffektiv overstyringspris for, og dobbelttrykk (eller dobbeltklikk)deretter på **Rollepris** for å åpne siden **Rolleprisdetaljer**.
1. Velg fanen **Datoeffektive overstyringer**. Rutenettet i denne fanen viser alle datoeffektive prisoverstyringer for den valgte **Rollepris**-oppføringen.
1. Velg **Ny rolleprisoverstyring** på verktøylinjen over rutenettet. Glidebryteren **Ny rolleprisoverstyring** åpnes.
1. Angi gyldig fra-datoen, enheten og den nye prisen for prisoverstyringen. Velg deretter **Lagre**, og lukk skjemaet.

> [!NOTE]
> - En datoeffektiv prisoverstyring for en rollepris eller et rolleprispåslag gjelder for den samme kombinasjonen av prisdimensjonsverdier som finnes i den overordnede raden **Rollepris** eller **Rolleprispåslag**.
> - Datoen som velges i **Gyldig fra**-feltet, må være innenfor gyldighetsdatoene for den overordnede prislisten. Prisoverstyringen trer i kraft på datoen som velges i **Gyldig fra**-feltet, og gjelder frem til sluttdatoen for den overordnede prislisten. Hvis du konfigurerer en ny datoeffektiv prisoverstyring for samme rollepris, trer den første prisoverstyringen i kraft på datoen som er valgt i **Gyldig fra**-feltet, og gjelder frem til begynnelsen på den andre overstyringen.

## <a name="examples"></a>Eksempler

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Eksempel 1: Fastsettelse av gyldighetsdato for en rollepris som har rolleprisoverstyringer

Eksemplet nedenfor viser hvordan gyldighetsdato fastsettes for en bestemt rollepris som rolleprisoverstyringer er konfigurert for.

**Prisliste A: 1. januar til 30. juni**

*Rollepris*

| Rollepris | Enhet | Pris | Virkning på priser for innkommende transaksjoner |
|---|---|---|---|
| Nettverkstekniker | Time | 100 | Denne prisen brukes i alle transaksjoner der transaksjonsdatoen er mellom 1. januar og 14. mars. |

*Rolleprisoverstyring*

| Gyldig fra | Enhet | Pris | Virkning på priser for innkommende transaksjoner |
|---|---|---|---|
| Mars 15 | Time | 110 | Denne prisen brukes i alle transaksjoner der transaksjonsdatoen er mellom 15. og 30. mars. |
| April 1 | Time | 120 | Denne prisen brukes i alle transaksjoner der transaksjonsdatoen er mellom 1. april og 30. juni. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Eksempel 2: Fastsettelse av gyldighetsdato for et rolleprispåslag som har rolleprispåslagsoverstyringer

Eksemplet nedenfor viser hvordan gyldighetsdato fastsettes for et bestemt rolleprispåslag som rolleprispåslagsoverstyringer er konfigurert for.

**Prisliste A: 1. januar til 30. juni**

*Rollepris*

| Rollepris | Arbeidstimer | Enhet | Pris | Virkning på priser for innkommende transaksjoner |
|---|---|---|---|---|
| Nettverkstekniker | Vanlig | Time | 100 | Denne prisen brukes i alle transaksjoner der transaksjonsdatoen er mellom 1. januar og 14. mars. |

*Rolleprispåslag*

| Organisasjonsenhet | Arbeidstimer | Påslagsprosent |
|---|---|---|
| Contoso US | Overtid | 10 % |

*Rolleprispåslagsoverstyring*

| Gyldig fra | Pris | Virkning på priser for innkommende transaksjoner |
|---|---|---|
| Mars 15 | 20 % | Denne påslagsprosenten brukes i alle transaksjoner der transaksjonsdatoen er mellom 15. og 30. mars. |
| April 1 | 25 % | Dette påslaget brukes i alle transaksjoner der transaksjonsdatoen er mellom 1. april og 30. juni. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
