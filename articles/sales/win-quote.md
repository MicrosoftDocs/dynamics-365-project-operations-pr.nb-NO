---
title: Lukke et tilbud
description: Denne artikkelen inneholder informasjon om lukking av tilbud i Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 45bdfe5fb9eddb8f96ed1bc017596c8fe436245e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931894"
---
# <a name="close-a-quote"></a>Lukke et tilbud

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Et prosjekttilbud kan lukkes som vunnet eller tapt. Siden funksjonene Aktiver og Revider ikke støttes på tilbud i Microsoft Dynamics 365 Project Operations, kan du lukke et utkasttilbud.

## <a name="close-a-quote-as-won"></a>Lukk et tilbud som vunnet

Hvis du lukker et prosjekttilbud som vunnet, settes statusen for tilbudet til **Lukket**, og statusårsaken settes til **Vunnet**. Ved å lukke tilbudet blir det skrivebeskyttet, og det opprettes et prosjektkontraktutkast med all tilbudsinformasjonen. Siden et lukket tilbud ikke kan åpnes på nytt, vil en bekreftelsesdialogboks bekrefte endringene før du lukker et tilbud.

Prosjektkontrakten som opprettes fra et prosjekttilbud, gjøres også tilgjengelig i modulen for prosjektstyring og regnskap i Project Operations. Hvis en prosjektkontrakt ikke er tilordnet til et prosjekt på noen av linjene, gjøres denne prosjektkontrakten tilgjengelig som en inaktiv prosjektkontrakt, og den blir aktiv så snart et prosjekt er tilordnet til minst én av kontraktlinjene.

Hvis tilbudet er knyttet til en salgsmulighet, lukkes eventuelle andre prosjekttilbud på salgsmuligheten automatisk som tapt.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Økonomisk påvirkning av å lukke et tilbud som vunnet

Hvis det har vært faktiske verdier for tid registrert i et prosjekt mens det fremdeles er knyttet til et utkasttilbud, registreres bare kostnadene for tiden eller utgiften. Når et tilbud er lukket som vunnet, vil programmet refaktorere kostnadene ved å reversere de eldre faktiske kostnadsverdiene og opprette nye faktiske kostnadsverdier på nytt. Programmet behandler disse faktiske kostnadsverdiene basert på faktureringsmetoden for den tilknyttede prosjektkontraktlinjen. Hvis de faktiske kostnadsverdiene refererer til en kontraktlinje for tid og materialer, oppretter systemet automatisk tilsvarende faktiske verdier for ikke-fakturerte salg når tilbudet lukkes og prosjektkontrakten opprettes. Hvis de faktiske kostnadsverdiene refererer til en kontraktlinje med fast pris, stoppes den nye behandlingen av de faktiske kostnadsverdiene basert på reglene for delt fakturering for prosjektkontraktkundene.

Alle etterbehandlede faktiske verdier er tilgjengelige i modulen for prosjektstyring og regnskap, slik at prosjektregnskapsføreren kan se gjennom, oppdatere og postere dem til hovedboken. 

## <a name="close-a-quote-as-lost"></a>Lukk et tilbud som tapt

Hvis du lukker et prosjekttilbud som tapt, settes statusen til **Lukket** og statusårsaken til **Tapt**. Hvis du lukker tilbudet, blir det skrivebeskyttet. Siden et lukket tilbud ikke kan åpnes på nytt, vil en bekreftelsesdialogboks bekrefte endringene før du lukker et tilbud.

Hvis prosjekttilbudet som er lukket som tapt, har et prosjekt det er referert til på noen av linjene, blir dette prosjektet også merket som lukket, og eventuelle ressursbestillinger fra den dagen og fremover blir annullert.

> [!NOTE]
> I Project Operations vil lukking av et tilbud som vunnet eller tapt ikke virke inn på statusen for salgsmuligheten, som forblir åpen til den lukkes manuelt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]