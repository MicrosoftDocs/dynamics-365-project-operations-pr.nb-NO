---
title: Legg til nye egendefinerte enhetsskjemaer (Project Service Automation 2.x)
description: Dette emnet gir informasjon om hvordan du legger til egendefinerte enhetsskjemaer for salgsmuligheter, tilbud, ordrer eller fakturaer i Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e59e343887ef59ee28bee13346a0c9bf3ad7df27346e2a4f3f02a1e5c08c060f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995233"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Legg til nye egendefinerte enhetsskjemaer (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Felttype 

Dynamics 365 Project Service Automation avhenger av feltet **Type** (**msdyn\_ordertype**) i enhetene for salgsmulighet, tilbud, ordre og faktura for å skille **arbeidsbaserte** versjoner av disse enhetene fra **varebasert** og **tjenestebaserte** versjoner. Arbeidsbaserte versjoner av disse entitetene håndteres av PSA. Mye forretningslogikk på klientsiden og serversiden av løsningen avhenger av **Type**-feltet. Derfor er det viktig at feltet initialiseres med en korrekt verdi når enhetene opprettes. Feil verdi kan føre til feil funksjonalitet, og det kan hende at noe av forretningslogikken ikke kjører på riktig måte.

## <a name="automatic-form-switching"></a>Automatisk skjemabytting

For å unngå potensiell dataskade og uventet atferd som forårsakes av feil initialisering og redigering av salgsenhetsoppføringene, inkluderer PSA nå logikk for automatisk bytting av skjema i medfølgende skjemaer. Denne logikken fører brukere til riktig skjema for å arbeide med den arbeidsbaserte versjonen eller en annen type salgsmulighets-, tilbuds-, ordre- eller fakturaenhet. Når en bruker åpner den arbeidsbaserte versjonen av en salgsmulighets-, tilbuds-, ordre- eller fakturaenhet, byttes skjemaet til **Prosjektinformasjon**.

Den automatiske logikken for skjemabytting er avhengig av tilordningen mellom verdien **formId** og feltet **msdyn\_ordertype**. Alle medfølgende skjemaer er lagt til i tilordningen. Egendefinerte skjemaer må imidlertid legges til manuelt for å angi hvilken versjon av enheten de er ment å håndtere. Dette er basert på feltet **msdyn\_ordertype**. Hvis skjemabyttingen mangler fra tilordningen, bytter logikken til det medfølgende skjemaet basert på verdien som er lagret i feltet **msdyn\_ordertype** for enheten.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Legge til egendefinerte skjemaer og aktivere logikken for skjemabytting

Følgende eksempel viser hvordan du legger til et egendefinert skjema, **Min prosjektinformasjon**, slik at det fungerer med arbeidsbaserte salgsmuligheter. Den samme prosessen brukes til å legge til egendefinerte skjemaer, slik at de kan fungere med tilbud, ordrer og fakturaer.

Følg fremgangsmåten nedenfor for å opprette en egendefinert versjon av skjemaet **Prosjektinformasjon**.

1. Åpne skjemaet **Prosjektinformasjon** i salgsmulighetsenheten, og lagre en kopi under navnet **Min prosjektinformasjon**.
2. Åpne det nye skjemaet, og kontroller deretter at skriptene for skjemainitialisering fra skjemaet **Prosjektinformasjon** finnes. 

    > [!IMPORTANT]
    > Ikke fjern skriptene. Ellers kan enkelte data bli initialisert feil.

3. Kontroller at feltet **Type** (**msdyn\_ordertype**) finnes i skjemaet. 

    > [!IMPORTANT]
    > Ikke fjern dette feltet. Ellers vil initialiseringsprosessen mislykkes.

4. Finn **formId**-verdien for det nye skjemaet. Du kan gjøre dette på to forskjellige måter:

    - Eksporter skjemaet **Min prosjektinformasjon** som en del av en uadministrert løsning, og slå deretter opp **formId**-verdien i filen customization.xml i den eksporterte løsningen.
    - Åpne skjemaet **Min prosjektinformasjon** i skjemaredigeringsprogrammet, og se etter den globalt unike identifikatoren (GUID) ved siden av **fromId**-parameteren i URL-adressen, som vist i følgende illustrasjon.

    ![Verdien formId for det nye skjemaet i URL-adressen.](media/how-to-add-custom-forms-in-v2.0.png)

5. Opprett en **msdyn\_ordertype**-tilordning for **formId**-verdien ved å redigere nettressursen msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Fjern koden fra ressursen, og erstatt den med følgende kode.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Lagre og publiser tilpassingene.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]