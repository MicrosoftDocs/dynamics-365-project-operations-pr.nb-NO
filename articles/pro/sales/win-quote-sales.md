---
title: Lukke et tilbud – Lite
description: Dette emnet gir informasjon om hvordan du lukker et tilbud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175723"
---
# <a name="close-a-quote---lite"></a>Lukke et tilbud – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Et prosjekttilbud kan lukkes som vunnet eller tapt. Operasjonene Aktiver og Revider i tilbud støttes ikke i Microsoft Dynamics 365 Project Operations, slik at et utkasttilbud kan lukkes.

## <a name="close-a-quote-as-won"></a>Lukk et tilbud som vunnet

Hvis du lukker et prosjekttilbud som vunnet, lukkes tilbudet med statusen satt til Lukket, og statusårsaken satt til Vunnet. Ved å lukke tilbudet blir prosjekttilbudet skrivebeskyttet, og det opprettes et prosjektkontraktutkast som inneholder tilbudsinformasjonen. Siden et lukket tilbud ikke kan åpnes på nytt, vises det en bekreftelsesdialogboks før endringene blir utført, siden endringene kan ikke gjøres om.

Hvis tilbudet er knyttet til en salgsmulighet, lukkes eventuelle andre prosjekttilbud på salgsmuligheten automatisk som tapt.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Økonomisk påvirkning av å lukke et tilbud som vunnet

Hvis det har vært faktiske verdier for tid registrert i et prosjekt mens det fremdeles er knyttet til et utkasttilbud, registreres bare kostnadene for tiden eller utgiften. Når et tilbud er lukket som vunnet, vil programmet refaktorere kostnadene ved å reversere de eldre faktiske kostnadsverdiene og opprette nye faktiske kostnadsverdier på nytt. Programmet behandler disse faktiske kostnadsverdiene basert på faktureringsmetoden for den tilknyttede prosjektkontraktlinjen. Hvis de faktiske kostnadsverdiene refererer til en kontraktlinje for tid og materialer, oppretter systemet automatisk tilsvarende faktiske verdier for ikke-fakturerte salg når tilbudet lukkes og prosjektkontrakten opprettes. Hvis de faktiske kostnadsverdiene refererer til en kontraktlinje med fast pris, stoppes den nye behandlingen av de faktiske kostnadsverdiene basert på reglene for delt fakturering for prosjektkontraktkundene.

## <a name="closing-a-quote-as-lost"></a>Lukk et tilbud som tapt:

Hvis du lukker et prosjekttilbud som tapt, settes statusen til Lukket og statusårsaken til Tapt. Hvis du lukker tilbudet, blir prosjekttilbudet skrivebeskyttet. Siden et lukket tilbud ikke kan åpnes på nytt, vil en bekreftelsesdialogboks bekrefte endringene før du lukker et tilbud.

Hvis prosjekttilbudet som er lukket som tapt, har et prosjekt det er referert til på noen av linjene, blir dette prosjektet også merket som lukket, og eventuelle ressursbestillinger fra den dagen og fremover blir annullert.

> [!NOTE]
> I Project Operations vil lukking av et tilbud som vunnet eller tapt ikke virke inn på statusen for salgsmuligheten, som forblir åpen til den lukkes manuelt.
