---
title: Synkronisere faktiske prosjektdata direkte fra Project Service Automation til prosjektintegreringsjournalen for postering i Finance and Operations
description: Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere faktiske prosjektdata direkte fra Microsoft Dynamics 365 Project Service Automation til Finance and Operations.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 11ccbd64c37341b2969e10e9a737f1aa4b4a61f9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289696"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synkronisere faktiske prosjektdata direkte fra Project Service Automation til prosjektintegreringsjournalen for postering i Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere faktiske prosjektdata direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.

Malen synkroniserer transaksjoner fra Project Service Automation til en oppsamlingstabell i Finance. Når synkroniseringen er fullført, **må** du importere dataene fra oppsamlingstabellen til integreringsjournalen.

> [!NOTE]
> - Integrering av faktiske prosjektdata er tilgjengelig fra og med versjon 8.0.1.
> - Hvis du bruker Enterprise Edition 7.3.0 etter at du har installert KB-4132657 og KB-4132660, kan du bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske verdier, og til å konfigurere låsing av funksjoner. Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.
> - Hvis du bruker versjon 7.3.0 og overfører gebyrtransaksjoner fra Project Service Automation, må du installere KB 4345320 for å kunne ta med de avgiftene i prosjektfakturaen.
> - Hvis du skal angi mva-beløp i tids- eller utgiftstransaksjoner i Project Service Automation, må du installere Project Service Automation oppdatering 7. Hvis ikke blir de faktiske mva-verdiene ikke koblet til de tilknyttede faktiske dataene for tid og utgifter, og de synkroniseres ikke til Finance. Kontakt Støtte hvis du vil ha mer informasjon.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflyt for Project Service Automation til Finance

Project Service Automation til Finance-integreringsløsningen bruker funksjonen for dataintegrering til å synkronisere data på tvers av forekomster av Project Service Automation og Finance. Integreringsmalene som er tilgjengelige med funksjonen for dataintegrering, muliggjør dataflyt om faktiske prosjektdata fra Project Service Automation til Finance.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance.

[![Dataflyt for Project Service Automation-integrasjon med Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Faktiske prosjektdata fra Project Service Automation

### <a name="template-and-tasks"></a>Mal og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, går du til Microsoft Power Apps og velger **Prosjekter**, og deretter velger du **Nytt prosjekt** i øverste høyre hjørne for å velge offentlige maler.

Følgende mal og underliggende oppgaver brukes til å synkronisere faktiske prosjektdasta fra Project Service Automation til Finance:

- **Navn på malen i dataintegrering:** Faktiske prosjektdata (PSA til Fin og Ops)
- **Navn på oppgavene i prosjektet:**

    - Faktiske verdier
    - TransactionConnections

### <a name="entity-set"></a>Enhetssett

| Project Service Automation | Finans                                   |
|----------------------------|----------------------------------------------------------|
| Faktiske verdier                    | Integreringsenhet for faktiske prosjektdata                   |
| Transaksjonstilkoblinger    | Integreringsenhet for prosjekttransaksjonsrelasjoner |

### <a name="entity-flow"></a>Enhetsflyt

Faktiske prosjektdata administreres i Project Service Automation, og de synkroniseres til prosjektintegreringsjournalen i Finance. Regnskapet tas i bruk basert på standard finansdimensjoner og bokføringsoppsettet.

### <a name="prerequisites"></a>Forutsetninger

Før synkronisering av faktiske verdier kan skje må du konfigurere Project Service Automation-integrasjonsparameterne og synkronisere prosjekter, prosjektoppgaver og prosjektets utgiftstransaksjonskategorier.

### <a name="power-query"></a>Power Query

I malen for faktiske prosjektdata må du bruke Microsoft Power Query for Excel til å utføre disse oppgavene:

- Transformer transaksjonstypen i Project Service Automation til riktig transaksjonstype i Finance. Denne transformasjonen er allerede definert i malen for faktiske prosjektdata (PSA til Fin og Ops).
- Transformer faktureringstypen i Project Service Automation til riktig faktureringstype i Finance. Denne transformasjonen er allerede definert i malen for faktiske prosjektdata (PSA til Fin og Ops). Faktureringstypen tilordnes deretter til linjeegenskapen basert på konfigurasjonen på siden for **Project Service Automation-integrasjonsparametere**.
- Filtrer på bestemte ressursorganisasjonsenheter som må synkroniseres med denne malen.
- Hvis de faktiske dataene for konsernintern tid eller utgifter skal synkroniseres til Finance, må du transformere kontraktorganisasjonsenheten til riktig juridisk enhet i Finance. I malen for faktiske prosjektdata (PSA til Fin og Ops) defineres en betingelseskolonne basert på demonstrasjonsdata. Du må oppdatere den sist innsatte betingelseskolonnen til riktige juridiske enheter. Ellers kan det oppstå en integreringsfeil, eller feil faktiske transaksjoner kan importeres til Finance.
- Hvis de faktiske verdiene for konsernintern tid eller konserninterne utgifter ikke skal synkroniseres til Finance, må du slette den sist innsatte betingelseskolonnen fra malen. Ellers kan det oppstå en integreringsfeil, eller feil faktiske transaksjoner kan importeres til Finance.

#### <a name="contract-organizational-unit"></a>Kontraktorganisasjonsenhet
Hvis du vil oppdatere den innsatte betingelseskolonnen i malen, klikker du **Tilordne**-pilen for å åpne tilordningen. Velg koblingen **Avansert spørring og filtrering** for å åpne Power Query.

- Hvis du bruker standardmalen for faktiske prosjektdata (PSA til Fin og OPS) i Power Query, velger du siste **Innsatt betingelse** fra delen **Brukte trinn**. I **Funksjon**-oppføringen erstatter du **USSI** med navnet på den juridiske enheten som skal brukes med integrasjonen. Legg til flere betingelser i **Funksjon**-oppføringen slik du ønsker, og oppdater **hvis ikke**-betingelsen fra **USMF** til riktig juridisk enhet.
- Hvis du oppretter en ny mal, må du legge til kolonnen for å støtte konserninterne tid og utgifter. Velg **Legg til betinget kolonne**, og skriv inn et navn på den nye kolonnen, for eksempel **Juridisk enhet**. Angi en betingelse for kolonnen, der hvis **msdyn\_contractorganizationalunitid.msdyn\_name** er \<organizational unit\>, så \<enter the legal entity\>. Hvis ikke null.

### <a name="template-mapping-in-data-integration"></a>Maltilordning i dataintegrering

Illustrasjonene nedenfor viser et eksempel på maloppgavetilordningen i dataintegrering. Tilordningen viser feltinformasjonen som blir synkronisert fra Project Service Automation til Finance.

[![Maltilordning – faktiske verdier](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Maltilordning – transaksjonstilkoblinger](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importere fra oppsamlingstabell etter integrering fra Project Service Automation

Den periodiske prosessen for import fra oppsamlingstabell må kjøres etter synkroniseringen av faktiske verdier fra Project Service Automation til Finance. Denne prosessen fører til at prosjekttransaksjonene importeres fra oppsamlingstabellen til integrasjonsjournalen for Project Service Automation, der regnskapsføringen brukes og de importerte transaksjonene kan posteres. Vi anbefaler at du kjører denne prosessen i satsvis modus. Den kan eventuelt konfigureres til å kjøre som en regelmessig satsvis jobb.

## <a name="update-actuals-from-finance"></a>Oppdatere faktiske verdier fra Finance

### <a name="template-and-tasks"></a>Mal og oppgaver

Følgende mal og underliggende oppgaver brukes til å synkronisere bilagsnummeret og merverdiavgiften for posterte prosjekttransaksjoner fra Finance til Project Service Automation:

- **Navn på malen i dataintegrering:** Oppdatering av faktiske prosjektdata (Fin Ops til PSA)
- **Navn på oppgavene i prosjektet:**

    - Faktiske verdier 
    - TransactionConnections

### <a name="entity-set"></a>Enhetssett

| Finans                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integreringsenhet for faktiske prosjektdata                   | Faktiske verdier                    |
| Integreringsenhet for prosjekttransaksjonsrelasjoner | Transaksjonstilkoblinger    |

### <a name="entity-flow"></a>Enhetsflyt

Faktiske prosjektdata administreres i Project Service Automation, og de synkroniseres til prosjektintegreringsjournalen i Finance. Etter at faktiske verdier er postert i Finance, oppdateres de i Project Service Automation med bilagsnummeret fra Finance. Hvis merverdiavgift ble lagt til i Finance, opprettes det nye faktiske avgiftsverdier i Project Service Automation.

### <a name="power-query"></a>Power Query

I malen for oppdatering av faktiske prosjektdata må du bruke Power Query til å utføre disse oppgavene:

- Transformer transaksjonstypen i Finance til riktig transaksjonstype i Project Service Automation. Denne transformasjonen er allerede definert i malen for oppdatering av faktiske prosjektdata (Fin Ops til PSA).
- Transformer faktureringstypen i Finance til riktig faktureringstype i Project Service Automation. Denne transformasjonen er allerede definert i malen for oppdatering av faktiske prosjektdata (Fin Ops til PSA).

### <a name="template-mapping-in-data-integration"></a>Maltilordning i dataintegrering

Illustrasjonene nedenfor viser eksempler på maloppgavetilordningene i dataintegrering. Tilordningen viser feltinformasjonen som blir synkronisert fra Finance til Project Service Automation.

[![Maltilordning – oppdatering av faktiske verdier](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Maltilordning – oppdatering av transaksjon](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]