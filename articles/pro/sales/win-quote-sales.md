---
title: Lukke et tilbud – Lite
description: Dette emnet gir informasjon om hvordan du lukker et tilbud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764876"
---
# <a name="close-a-quote---lite"></a>Lukke et tilbud – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Et prosjekttilbud kan lukkes som vunnet eller tapt. Et tilbudsutkast kan lukkes fordi operasjonene Aktiver og Revider tilbud ikke støttes i Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Lukk et tilbud som vunnet

Når du lukker et prosjekttilbud som Vunnet, settes statusen til Lukket, og statusårsak er Vunnet. Ved å lukke tilbudet blir prosjekttilbudet skrivebeskyttet, og det opprettes et prosjektkontraktutkast som inneholder tilbudsinformasjonen. Et lukket tilbud kan ikke åpnes på nytt, og derfor bekreftes endringene i en bekreftelsesdialogboks.

Hvis tilbudet er knyttet til en salgsmulighet, lukkes eventuelle andre prosjekttilbud på salgsmuligheten automatisk som tapt.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Økonomisk påvirkning av å lukke et tilbud som vunnet

Hvis det finnes faktiske data for tid på et prosjekt mens det fremdeles er knyttet til et tilbudsutkast, registreres bare kostnadene for tids- eller utgiftene. Når et tilbud er lukket som vunnet, vil programmet refaktorere kostnadene ved å reversere de eldre faktiske kostnadsverdiene og opprette nye faktiske kostnadsverdier på nytt. Programmet behandler disse faktiske kostnadsverdiene basert på faktureringsmetoden for den tilknyttede prosjektkontraktlinjen. Hvis de faktiske kostnadene refererer til en tids- og materialkontraktlinje, opprettes tilsvarende faktiske salg for når tilbudet lukkes og prosjektkontrakten opprettes. Hvis de faktiske kostnadene refererer til en kontraktlinje med fast pris, slutter programmet å reprosessere de faktiske kostnadene som er basert på de delte faktureringsreglene for prosjektkontraktkundene.

## <a name="closing-a-quote-as-lost"></a>Lukk et tilbud som tapt:

Når du lukker et prosjekttilbud som Tapt, settes statusen til Lukket, og statusårsak er Tapt. Hvis du lukker tilbudet, blir prosjekttilbudet skrivebeskyttet. Siden et lukket tilbud ikke kan åpnes på nytt, vil en bekreftelsesdialogboks bekrefte endringene før du lukker et tilbud.

Hvis prosjekttilbudet som lukkes som Tapt, refererer til et prosjekt på noen av linjene, blir det prosjektet også merket som Lukket. Eventuelle ressursbestillinger fra den dagen og fremover annulleres.

> [!NOTE]
> I Project Operations vil lukking av et tilbud som vunnet eller tapt ikke virke inn på statusen for salgsmuligheten, som forblir åpen til den lukkes manuelt.
