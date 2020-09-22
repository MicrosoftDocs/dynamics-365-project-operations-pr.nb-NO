---
title: Legg til nye egendefinerte enhetsskjemaer (Project Service Automation 2.x)
description: Dette emnet gir informasjon om hvordan du legger til egendefinerte enhetsskjemaer for salgsmuligheter, tilbud, ordrer eller fakturaer i Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9eb9fc5e-4c7d-466c-9362-fdb0faa30506
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 2bd955ad3eb26d31676ac4ad387baccaee913cd2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754027"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="36f42-103">Legg til nye egendefinerte enhetsskjemaer (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="36f42-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="36f42-104">Felttype</span><span class="sxs-lookup"><span data-stu-id="36f42-104">Type field</span></span> 

<span data-ttu-id="36f42-105">Dynamics 365 Project Service Automation avhenger av feltet **Type** (**msdyn\_ordertype**) i enhetene for salgsmulighet, tilbud, ordre og faktura for å skille **arbeidsbaserte** versjoner av disse enhetene fra **varebasert** og **tjenestebaserte** versjoner.</span><span class="sxs-lookup"><span data-stu-id="36f42-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="36f42-106">Arbeidsbaserte versjoner av disse entitetene håndteres av PSA.</span><span class="sxs-lookup"><span data-stu-id="36f42-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="36f42-107">Mye forretningslogikk på klientsiden og serversiden av løsningen avhenger av **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="36f42-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="36f42-108">Derfor er det viktig at feltet initialiseres med en korrekt verdi når enhetene opprettes.</span><span class="sxs-lookup"><span data-stu-id="36f42-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="36f42-109">Feil verdi kan føre til feil funksjonalitet, og det kan hende at noe av forretningslogikken ikke kjører på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="36f42-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="36f42-110">Automatisk skjemabytting</span><span class="sxs-lookup"><span data-stu-id="36f42-110">Automatic form switching</span></span>

<span data-ttu-id="36f42-111">For å unngå potensiell dataskade og uventet atferd som forårsakes av feil initialisering og redigering av salgsenhetsoppføringene, inkluderer PSA nå logikk for automatisk bytting av skjema i medfølgende skjemaer.</span><span class="sxs-lookup"><span data-stu-id="36f42-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="36f42-112">Denne logikken fører brukere til riktig skjema for å arbeide med den arbeidsbaserte versjonen eller en annen type salgsmulighets-, tilbuds-, ordre- eller fakturaenhet.</span><span class="sxs-lookup"><span data-stu-id="36f42-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="36f42-113">Når en bruker åpner den arbeidsbaserte versjonen av en salgsmulighets-, tilbuds-, ordre- eller fakturaenhet, byttes skjemaet til **Prosjektinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="36f42-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="36f42-114">Den automatiske logikken for skjemabytting er avhengig av tilordningen mellom verdien **formId** og feltet **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="36f42-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="36f42-115">Alle medfølgende skjemaer er lagt til i tilordningen.</span><span class="sxs-lookup"><span data-stu-id="36f42-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="36f42-116">Egendefinerte skjemaer må imidlertid legges til manuelt for å angi hvilken versjon av enheten de er ment å håndtere.</span><span class="sxs-lookup"><span data-stu-id="36f42-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="36f42-117">Dette er basert på feltet **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="36f42-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="36f42-118">Hvis skjemabyttingen mangler fra tilordningen, bytter logikken til det medfølgende skjemaet basert på verdien som er lagret i feltet **msdyn\_ordertype** for enheten.</span><span class="sxs-lookup"><span data-stu-id="36f42-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="36f42-119">Legge til egendefinerte skjemaer og aktivere logikken for skjemabytting</span><span class="sxs-lookup"><span data-stu-id="36f42-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="36f42-120">Følgende eksempel viser hvordan du legger til et egendefinert skjema, **Min prosjektinformasjon**, slik at det fungerer med arbeidsbaserte salgsmuligheter.</span><span class="sxs-lookup"><span data-stu-id="36f42-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="36f42-121">Den samme prosessen brukes til å legge til egendefinerte skjemaer, slik at de kan fungere med tilbud, ordrer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="36f42-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="36f42-122">Følg fremgangsmåten nedenfor for å opprette en egendefinert versjon av skjemaet **Prosjektinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="36f42-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="36f42-123">Åpne skjemaet **Prosjektinformasjon** i salgsmulighetsenheten, og lagre en kopi under navnet **Min prosjektinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="36f42-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="36f42-124">Åpne det nye skjemaet, og kontroller deretter at skriptene for skjemainitialisering fra skjemaet **Prosjektinformasjon** finnes.</span><span class="sxs-lookup"><span data-stu-id="36f42-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="36f42-125">Ikke fjern skriptene.</span><span class="sxs-lookup"><span data-stu-id="36f42-125">Don't remove the scripts.</span></span> <span data-ttu-id="36f42-126">Ellers kan enkelte data bli initialisert feil.</span><span class="sxs-lookup"><span data-stu-id="36f42-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="36f42-127">Kontroller at feltet **Type** (**msdyn\_ordertype**) finnes i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="36f42-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="36f42-128">Ikke fjern dette feltet.</span><span class="sxs-lookup"><span data-stu-id="36f42-128">Don't remove this field.</span></span> <span data-ttu-id="36f42-129">Ellers vil initialiseringsprosessen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="36f42-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="36f42-130">Finn **formId**-verdien for det nye skjemaet.</span><span class="sxs-lookup"><span data-stu-id="36f42-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="36f42-131">Du kan gjøre dette på to forskjellige måter:</span><span class="sxs-lookup"><span data-stu-id="36f42-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="36f42-132">Eksporter skjemaet **Min prosjektinformasjon** som en del av en uadministrert løsning, og slå deretter opp **formId**-verdien i filen customization.xml i den eksporterte løsningen.</span><span class="sxs-lookup"><span data-stu-id="36f42-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="36f42-133">Åpne skjemaet **Min prosjektinformasjon** i skjemaredigeringsprogrammet, og se etter den globalt unike identifikatoren (GUID) ved siden av **fromId**-parameteren i URL-adressen, som vist i følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="36f42-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Verdien formId for det nye skjemaet i URL-adressen.](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="36f42-135">Opprett en **msdyn\_ordertype**-tilordning for **formId**-verdien ved å redigere nettressursen msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="36f42-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="36f42-136">Fjern koden fra ressursen, og erstatt den med følgende kode.</span><span class="sxs-lookup"><span data-stu-id="36f42-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="36f42-137">Lagre og publiser tilpassingene.</span><span class="sxs-lookup"><span data-stu-id="36f42-137">Save and then publish the customizations.</span></span>
