---
title: Bruke en ressurs som kan reserveres som en prisdimensjon
description: Dette emnet gir informasjon om hvordan du bruker en ressurs som kan reserveres som en prisdimensjon.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dcd01d80236f0218bc6fa3a1fe1389f8314f3c9b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598639"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Bruke en ressurs som kan reserveres som en prisdimensjon

 _**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_ 

Dette emnet gir informasjon om hvordan du bruker en ressurs som kan reserveres som en prisdimensjon. Hvis prisstrategien er konfigurert slik at hver bestillingsbare ressurs må ha en bestemt pris eller kostnadssats, må du bruke bestillingsbar ressurs som en prisdimensjon.

## <a name="prerequisites"></a>Forutsetninger
Før du fullfører prosedyrene i dette emnet, må du ha en ny prisdimensjonsløsning for organisasjonen. Hvis du ikke allerede har opprettet en, kan du se [Opprette egendefinerte felt og enheter](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Legge til Ressurs som kan reserveres-feltet i skjemaer og visninger
Hvis du vil gjøre **Ressurs som kan reserveres**-feltet synlig i prisdimensjonsløsningen, må du legge til feltet i alle skjemaer og visninger som en enhet.

Tabellen nedenfor viser alle de medfølgende skjemaene og visningene etter enhet. Du må også legge til det nye feltet i andre ekstra skjemaer eller visninger i de egendefinerte enhetene.

|   Entity        | Skjemaer   |Visninger        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollepris| Informasjon | - Aktive ressurskategoripriser<br> - Tilknyttede ressurskategoripriser |
|  Rolleprispåslag| Informasjon| - Aktive rolleprispåslag<br>- Tilknyttede rolleprispåslag |
|  Tilbudslinjedetalj| - Prosjektinformasjon<br>- Hurtigoppretting av prosjekt| - Aktiv tilbudslinjedetalj<br>- Kombinerte tilbudslinjedetaljer<br>- Tilknyttet tilbudslinjedetalj |
|  Detalj for prosjektkontraktlinjer| - Prosjektinformasjon<br>- Hurtigoppretting av prosjekt| - Kombinerte kontraktlinjedetaljer<br>- Aktive kontraktlinjedetaljer<br>- Tilknyttede kontraktlinjedetaljer |
|  Prosjektoppgave| - Informasjon<br>- Nytt skjema| &nbsp; |
|  Prosjektteammedlem| - Informasjon<br>- Nytt skjema| - Aktive prosjektteammedlemmer<br>- Prosjektteammedlemmer<br>- Tilknyttede teammedlemmer i prosjektet |
|  Tidsoppføring| - Informasjon<br>- Opprett tidsoppføring| - Mine tidsoppføringer etter dato<br>- Mine tidsoppføringer for denne uken<br>- Tidsoppføringer til godkjenning|
|  Journallinje| - Informasjon<br>- Hurtigoppretting| - Aktive journallinjer<br>- Tilknyttet journallinje |
|  Fakturalinjedetalj| - Informasjon<br>- Hurtigoppretting| - Aktive fakturalinjedetaljer<br>- Belastbare fakturatransaksjoner<br>- Gratis fakturatransaksjoner<br>- Tilknyttet fakturalinjedetalj <br>- Ikke-belastbare fakturatransaksjoner|
|  Faktisk| - Informasjon<br>- Aktive faktiske data| Faktisk tilknyttet |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Konfigurere en ressurs som kan reserveres som en prisdimensjon
Du konfigurerer en ressurs som kan reserveres som en prisdimensjon ved å følge disse trinnene:

1. Gå til **Innstillinger** > **Parametere**. 
2. På **Parameter**-siden i **Beløpsbaserte prisdimensjoner**-kategorien, bekrefter du at rutenettet viser oppføringene i **Prisdimensjoner**-enheten. 
2. Legg den **bestillbare ressursen** i denne listen over prisdimensjoner som **msdyn_bookableresource**. 
3. Velg en verdi i **Gjelder kostnad** og **Gjelder salg**.
4. I **Dimensjonstype** velger du **Beløpsbasert**. 
5. Velg kostnads- og salgsprioriteten for den bestillbare ressursen. Vanligvis har en ressurs som kan reserveres høyest prioritet når den tas med som en prisdimensjon. Angi prioriteten til **1** (eller **0** avhengig av hvordan du teller prioriteten) for å sikre denne virkemåten.

## <a name="set-up-pricing-dimension-field-names"></a>Angi feltnavn for prisdimensjon

Når feltnavnet for en prisdimensjon i **Rollepris**-tabellen er forskjellig fra feltnavnet i noen av de andre enhetene der standardprisen brukes, må prisdimensjonsoppføringen varsles om de forskjellige navnene.  

For en ressurs som kan reserveres, har **Prosjektteammedlemmer**-enheten et litt annet feltnavn enn hva det er kalt på **Rollepris**-enheten: 

 - **Prosjektteammedlemmer**-enhet = **msdyn_bookableresourceid**
 - **Rollepris**-enhet = **msdyn_bookableresource**

Prisdimensjonsoppføringen for **msydn_bookableresource** må varsles om denne forskjellen.

1. Dobbeltklikk på raden i **Prisdimensjoner**-rutenettet for å åpne dimensjonssiden til **msdyn_bookableresource**.
2. På dimensjonssiden, på **Relatert**-fanen, velger du **Feltnavn for prisdimensjon**.

  ![Fanen Feltnavn for prisdimensjon.](media/PD-fieldname.png)

3. I den tilknyttede visningen som åpnes, velger du **Legg til nytt feltnavn for prisdimensjon**.

  ![Legge til nye feltnavn for prisdimensjon.](media/Add-NewPD-fieldname.png)

  Dette åpner siden **Nytt feltnavn for prisdimensjon** for **msdyn_bookableresource**. 

4. På **Nytt feltnavn for prisdimensjon**-siden legger du **msdyn_projectteam** til **Logisk navn på enhet**.
5. Legg  **Msdyn_bookableresourceid** til i **Feltnavn**.

 ![Skjema for nytt feltnavn for prisdimensjon.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]