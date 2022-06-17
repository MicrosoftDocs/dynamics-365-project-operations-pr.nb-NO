---
title: Nyheter juli 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra juli 2021.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c004a6adc265f8f02fc557700d9b88a174c221c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931710"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter juli 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

*Gjelder: Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer*

Denne artikkelen gjelder følgende komponenter og versjoner av Dynamics 365 Project Operations:

   - Project Operations i Microsoft Dataverse-miljø, versjon 4.12.0.148 eller 4.12.0.152.
   - Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.20.

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

Følgende funksjoner er inkludert i denne versjonen:

- Mulighet for administratorer til å vise PSS-logger og operasjonssettlogger fra Innstillinger-menyen. Loggene lagres i 90 dager.

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Det finnes ingen oppdateringer for tilordninger av dobbel skriving i Project Operations i denne versjonen.

Hvis du vil ha en gjeldende liste og versjoner av tilordninger for dobbel skriving i Project Operations, kan du se [Tilordningsversjoner av dobbel skriving for Project Operations](../environment/resource-dual-write-maps.md).

Kjør alltid den nyeste versjonen av kartet i miljøet, og aktiver alle relaterte tabellkart når du oppdaterer Project Operations Dataverse-løsningen og Finance-løsningsversjonen. Enkelte funksjoner fungerer kanskje ikke på riktig måte hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen på siden **Dobbel skriving** i kolonnen **Versjon**. Aktiver en ny versjon av tilordningen ved å velge **Versjoner av tabelltilordningen**, velge den nyeste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en medfølgende tabelltilordning, må du bruke endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem med å starte kartet, følger du instruksjonene i delen [Problem med manglende tabellkolonner på kart](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funksjonsområdet**              | **Referansenummer** | **Kvalitetsoppdatering**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fakturering og prising           | 2224046              | Feltet **Transaksjonsklasse** kan redigeres i fanen **Tilbudslinjedetaljer**, men er låst hvis du arbeider på siden **Tilbudslinjedetaljer**.                                                                     |
| Fakturering og prising           | 2224400              | Handlingen **Lukk tilbud som vunnet** mislykkes når et tilbud ikke har datomilepæler.                                                                                                                                    |
| Fakturering og prising           | 2234089              | Når du angir en produktbeskrivelse manuelt, tømmes den etter at du har angitt et antall for et materialestimat.                                                                                                                         |
| Fakturering og prising           | 2234100              | Rutenettet **Faktureringsoppsett for oppgave** inneholder ikke **Material**-kolonnen, og verdien er i fanen **Oppgavefakturering** for prosjektet.                                                                                                       |
| Fakturering og prising           | 2277409              | Produkt-ID-en er ikke tilgjengelig på kontraktlinjedetaljene for en materialtypelinje.                                                                                                                                        |
| Fakturering og prising           | 2281728              | Oppretting av en kontraktlinje omevaluerer unødvendig faktiske data som fører til betydelig økning i datavolumet, noe som har innvirkning på ytelsen.                                                                                |
| Fakturering og prising           | 2298668              | Journallinjer som er knyttet til en tilbakekalt og slettet utgift, fjernes ikke.                                                                                                                                     |
| Fakturering og prising           | 2300192              | Når flere brukere redigerer en faktura, er det mulig å opprette en ny fakturalinjedetalj på en bekreftet faktura.                                                                                   |
| Fakturering og prising           | 2301569              | Fakturaer kan ikke korrigeres hvis et beløpshonorar på \$ 0 er brukt.                                                                                                                                        |
| Fakturering og prising           | 2307965              | Det vises en feil hvis en kategoripris opprettes med manglende verdier.                                                                                                                           |
| Fakturering og prising           | 2326870              | Det oppstår en feil i **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** hvis **producttypecode** er null.                                                                            |
| Fakturering og prising           | 2332732              | Det vises en feil hvis en kontraktlinjemilepæl opprettes uten en ordrelinje.                                                                                                                |
| Prosjektplanlegging og sporing | 2181094              | API-en for prosjektplanlegging støtter nå PSS-logger og operasjonssettlogger som er lagret i 90 dager.                                                                                                                  |
| Prosjektplanlegging og sporing | 2254201              | Etiketten **Tidsplanmodus** oppdateres med detaljer som beskriver standardlogikken.                                                                                                                                      |
| Prosjektplanlegging og sporing | 2300252              | Svarhurtigbufferen **openProject** oppdateres og inkluderer tokeneieren i hurtigbuffernøkkelen, **primær URL-adresse** og **URL-adresse for segmentet** slik at **URL-adressen for forespørselen** alltid kan opprettes på nytt hvis **primær URL-adresse** endres. |
| Prosjektplanlegging og sporing | 2301312              | **msdyn_membershipstatus** er fjernet fra visningen **Prosjektteammedlem**.                                                                                                                                        |
| Prosjektplanlegging og sporing | 2302759              | Produkter hentes unødvendig i fanen **Ressurstilordninger**, **Estimater** og **Utgiftsestimater**.                                                                                                        |
| Prosjektplanlegging og sporing | 2308050              | **CopyProject** mislykkes med feilen Kan ikke hente token for å snakke med ekstern tjeneste.                                                                                                                           |
| Prosjektplanlegging og sporing | 2322650              | Visningen **Prosjektoppgaveliste** er oppdatert til å vise datoen for oppgaven som standard.                                                                                                            |
| Prosjektplanlegging og sporing | 2327266              | **CopyProject** genererer feilmeldingen Finner ikke nøkkelen i ordlisten under kopiering av estimater.                                                                                                      |
| Prosjektplanlegging og sporing | 2328123              | **CopyProject** genererer feilen Kan ikke hente token for å snakke med ekstern tjeneste.                                                                                                                          |
| Prosjektplanlegging og sporing | 2336258              | **CopyProject** kopierer feil posisjonsnavnene for ressurser.                                                                                                                                                 |
| Fakturering og prising           | 2224476              | Feltet **Ressurs som kan reserveres** er ikke riktig standard for den påloggede brukeren på **Materialbruk**-siden.                                                                                                            |
| Ressursbehandling           | 2277249              | Det oppstår en feil når et ikke-prosjektbasert ressurskrav oppdateres.                                                                                                            |
| Ressursbehandling           | 2323869              | Ressursutnyttelse gjenkjenner ikke filtrerte ressurser riktig.                                                                                                                                             |
| Tid og utgift              | 2176538              | Feil filteroperatorer brukes på **Tidsoppføring**-kontrollen.                                                                                                                                                   |
| Tid og utgift              | 2177462              | Hvis du sletter en tidsoppføring i rutenettet, oppdateres ikke statusen for **Send**, **Tilbakekall**, **Slett** og **Rediger oppføring** som forventet.                                                                                        |
| Tid og utgift              | 2299985              | **TimeEntriesImportFromResourceAssignment** vedlikeholder ikke start-/sluttiden fra tildelingsprofilene.                                                                                                  |
| Tid og utgift              | 2318426              | Når en tidsoppføring er sendt, kan du likevel redigere låste felter.                                                                                                                                   |
| Tid og utgift              | 2323749              | Det oppstår en feil når en utgift opprettes fra fanen **Relatert** for en ressurs som kan reserveres.                                                                                                      |
| Tid og utgift              | 2327678              | Når du oppretter en tidsoppføring fra fanen **Relatert** for en ressurs som kan reserveres, sendes ikke den overordnede ressursen til tidsoppføringskontrollen.                                                                            |
| Generelt                       | 2296857              | Fremdriftssporing for langvarige jobber.                                                                                                                                                                        |
| Generelt                       | 2253682              | Løsningen for dobbel skriving i Project Operations bør ikke installeres når kjernen for dobbel skriving er installert i et miljø uten orkestreringsløsningen med dobbel skriving.                                                |
| Generelt                       | 2316420              | Kjerneklargjøring av prosjekttjeneste mislykkes hvis programbrukerens forretningsenhet endres.                                                                                                                     |
| Generelt                       | 2376405              | Problem med fast utgiverdrevet oppdatering (kvalitetsoppdateringen er tilgjengelig i versjon 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

| Funksjonsområdet                      | Referansenummer | Kvalitetsoppdatering                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prosjektstyring og regnskap | 4620267          | Kan ikke tilpasse skjemaer for å legge til et felt for **Formål** på sidene **Prosjektpostert transaksjon**, **Oppretting fakturaforslag** og **Fakturaforslag**.                                                                                                                                                                                         |
| Prosjektstyring og regnskap | 4613449          | Når du velger en prosjektkontrakt-ID i Økonomi, åpner det Project Operations-integrerte miljøet siden for å opprette en ny oppføring i stedet for siden for allerede opprettede prosjektkontrakter.                                                                                                                                           |
| Prosjektstyring og regnskap | 4614445          | I distribusjonen av Project Operations-integrert scenario kan du ikke redigere feltet **Mva-gruppe for vare** i fakturaforslaget som er importert fra oppsamlingen. Mva-gruppen for vare må kunne redigeres for et åpent fakturaforslag for alle transaksjonstyper, inkludert på konto, timer, utgifter, gebyrer og varer. |
| Prosjektstyring og regnskap |                  | Kan ikke postere et fakturaforslag som er et resultat av en negativ tidstransaksjonskorrigering.                                                                                                                                                                                                                                              |
| Prosjektstyring og regnskap |                  | Fakturaforslagslinjer dupliseres på grunn av flere periodiske prosesser for **Import fra oppsamling** som kjører samtidig.                                                                                                                                                                                                                |

