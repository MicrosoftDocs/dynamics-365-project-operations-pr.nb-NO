---
title: Overfør fullt fakturerte faktureringsmilepæler ved overgang
description: Denne artikkelen forklarer hvordan du overfører faktureringsmilepæler med fast pris som er fakturert til kunden for åpne prosjektkontrakter, før ikrafttredelsesdatoen.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028714"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Overfør fullt fakturerte faktureringsmilepæler ved overgang

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

## <a name="scenario"></a>Scenario

Contoso trer i kraft med Microsoft Dynamics 365 Project Operations for ressursbaserte/ikke-lagerførte scenarioer. Som en del av overgangsaktivitetene må implementeringsteamet overføre åpne prosjektkontrakter fra det gamle systemet. Noen av prosjektkontraktene inneholder kontraktlinjer som bruker faktureringsmetoden med fast pris og allerede er delvis fakturert til sluttbrukeren. Implementeringsteamet må overføre disse faktureringsmilepælene som **Kundefaktura postert**, fordi de må inkluderes i den totale kontraktverdien for inntektsføringsformål. Kundesaldoer i utestående fordringer og økonomimodulen må imidlertid ikke påvirkes.

## <a name="solution"></a>Løsning

### <a name="prerequisites"></a>Krav

- Dynamics 365 Finance 10.0.24 eller senere må være installert.
- Miljøet der overføringstrinnene blir fullført, må være i vedlikeholdsmodus. Ingen andre aktiviteter må utføres mens milepælene overføres.
- Overføringstrinnene må følges nøyaktig slik det er beskrevet her, og kan bare brukes for overgangsaktiviteten. Microsoft støtter ingen annen bruk av denne funksjonen.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Opprett en overgangsversjon av kontraktlinjemilepælene med dobbel skrivetilordning for Project Operations 

1. Kontroller at måltilordningen for **kontraktlinjemilepælene for Project Operations-integrering** er oppdatert. 

    1. I Finance går du til **Databehandling** \> **Dataenheter**, og velg enheten **Milepæler for prosjektkontraktlinje for Project Operations**. 
    2. Velg **Endre måltilordninger**. 
    3. På siden **Tilordne oppsamling til mål** velger du **Generer tilordning** og bekrefter deretter at du vil generere tilordningen.

2. Stopp og oppdater tilordningen **Milepæler for prosjektkontraktlinje for Project Operations** (**msdyn\_contractlinescheduleofvalues**) med dobbel skriving. 

    1. Gå til **Databehandling** \> **Dobbel skriving**, velg tilordningen, og åpne detaljene. 
    2. Velg **Stopp**, og vent til systemet stopper tilordningen. 
    3. Velg **Oppdater tabeller**.

3. Legg til en tilordning for transaksjonsstatusen.

    1. Velg **Legg til tilordning**.
    2. På den nye linjen, i kolonnen **Økonomi- og driftsapper**, velger du **TRANSSTATUS \[TRANSSTATUS\]**-feltet.
    3. I **Microsoft Dataverse**-kolonnen velger du **msdyn\_invoicestatus \[Invoice status\]**.
    4. I kolonnen **Tilordningstype** velger du høyrepilen (**\>**).
    5. I dialogboksen som vises, i feltet **Synkroniseringsretning**, velger du **Dataverse til økonomi- og driftsapper**.
    6. Velg **Legg til transformering**.
    7. I feltet **Transformeringstype** velger du **ValueMap**.
    8. Velg **Legg til verditilordning**.
    9. Angi **4** i det venstre feltet. Angi **192350001** i det høyre feltet. 
    10. Velg **Lagre**, og lukk deretter dialogboksen.

4. Velg **Lagre som** for å lagre versjonen av tilordningen med dobbel skriving. 
5. I ruten **Legg til tabell**, i **Utgiver**-feltet, velger du **Standardutgiver**.
6. I **Versjon**-feltet angir du versjonen.
7. I **Beskrivelse**-feltet skriver du inn en merknad om denne overgangsversjonen av tilordningen. 
8. Velg **Lagre**.
9. Start tilordningen.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Overfør fakturerte milepæler til Dataverse-miljøet

1. I Project Operations Dataverse-miljøet oppretter du milepæler som har faktureringsstatusen **Klar for fakturering**. Ikke overfør noen milepæler som ikke er fakturert, på dette tidspunktet.

    > [!NOTE]
    > Før du overfører faktureringsmilepælene, må du kontrollere at finansdimensjonene som er relatert til prosjektkontraktlinjen, er angitt som forventet. Finansdimensjoner kan ikke redigeres etter at overføringen er fullført.

2. Når alle milepælene er overført, stopper du følgende tilordninger med dobbel skriving:

    - Milepæler for prosjektkontraktlinje for Project Operations (msdyn\_contractlinescheduleofvalues)
    - Faktiske verdier for Project Operations-integrering (msdyn\_actuals)
    - Prosjektfakturaforslag V2 (fakturaer)

    Følg disse trinnene for å stoppe tilordningene:

    1. I Finance går du til **Databehandling** \> **Dobbel skriving**, velger en tilordningen og åpner detaljene.
    2. Velg **Stopp**, og vent til systemet stopper tilordningen.

3. I Project Operations Dataverse-miljøet oppretter og bekrefter du promafakturaer for faktureringsmilepælene. 

    1. Gå til prosjektkontraktene i områdekartet, velg kontraktene, og velg deretter **Opprett fakturaer**.
    2. Når fakturaene er opprettet, åpner du dem fra **Fakturaer**-menyen i områdekartet, og deretter velger du **Bekreft**.

    Dette trinnet oppretter de nødvendige oppføringene i Dataverse-miljøet. Det påvirker imidlertid ikke økonomi og utestående fordringer fordi de tidligere oppførte tilordningene med dobbel skriving ble stoppet.

4. Når alle promafakturaene er bekreftet, returnerer du alle tilordningene med dobbel skriving til starttilstanden.

    1. Oppdater versjonen av tilordningen **Milepæler for prosjektkontraktlinje for Project Operations** (**msdyn\_contractlinescheduleofvalues**) med dobbel skriving tilbake til den opprinnelige. 
    2. Velg tilordningen med dobbel skriving i tilordningslisten, velg **Tabelltilordningsversjon**, og velg deretter den opprinnelige versjonen av tabelltilordningen.
    3. Velg **Lagre**.
    4. Start følgende tilordninger med dobbel skriving på nytt:

        - Milepæler for prosjektkontraktlinje for Project Operations (msdyn\_contractlinescheduleofvalues)
        - Faktiske verdier for Project Operations-integrering (msdyn\_actuals)
        - Prosjektfakturaforslag V2 (fakturaer)

Milepælene er nå overført, og systemet er klart for de neste trinnene i overgangsaktiviteten.
