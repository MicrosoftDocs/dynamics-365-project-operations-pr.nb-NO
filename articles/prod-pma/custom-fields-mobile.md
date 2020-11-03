---
title: Implementere egendefinerte felt for Microsoft Dynamics 365 Project Timesheet-mobilappen på iOS og Android
description: Dette emnet inneholder vanlige mønstre for bruk av utvidelser for å implementere egendefinerte felt.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081674"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementere egendefinerte felt for Microsoft Dynamics 365 Project Timesheet-mobilappen på iOS og Android

[!include [banner](../includes/banner.md)]

Dette emnet inneholder vanlige mønstre for bruk av utvidelser for å implementere egendefinerte felt. Følgende emner omhandles:

- De forskjellige datatypene som det egendefinerte feltrammeverket støtter
- Slik viser du skrivebeskyttede eller redigerbare felt i timeregistreringsoppføringer og lagrer brukerangitte verdier tilbake til databasen
- Slik viser du skrivebeskyttede felt i timeregistreringshodet
- Slik integrerer du andre egendefinerte forretningslogikker for å angi standardverdier i felt og utføre ytterligere validering

## <a name="audience"></a>Målgruppe

Dette emnet er ment for utviklere som integrerer sine egendefinerte felt i Microsoft Dynamics 365 Project Timesheet-mobilappen som er tilgjengelig for Apple iOS og Google Android. Det forutsettes er at lesere er kjent med funksjonene for X++-utvikling og funksjonene for prosjekttimeregistrering.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Datakontrakt – klassen TSTimesheetCustomField X++

**TSTimesheetCustomField** -klassen er X++-datakontraktklassen som representerer informasjon om et egendefinert felt for timeregistreringsfunksjonalitet. Det blir sendt lister over de egendefinerte feltobjektene både for TSTimesheetDetails-datakontrakten og TSTimesheetEntry-datakontrakten for å vise egendefinerte felt i mobilappen.

- **TSTimesheetDetails** – Kontrakten for timeregistreringshodet.
- **TSTimesheetEntry** – Kontrakten for timeregistreringstransaksjonen. Grupper av disse objektene som har samme prosjektinformasjon og **timesheetLineRecId** -verdi, utgjør en linje.

### <a name="fieldbasetype-types"></a>fieldBaseType (typer)

Egenskapen **FieldBaseType** i **TsTimesheetCustom** -objektet bestemmer typen av feltet som vises i appen. Følgende **Typer** -verdier som støttes.

| Typer-verdi | Type              | Notater |
|-------------|-------------------|-------|
| 0           | Streng (og Enum) | Feltet vises som et tekstfelt. |
| 1           | Integer           | Verdien vises som et tall uten desimalplasser. |
| 2           | Reell              | Verdien vises som et tall med desimalplasser.<p>Hvis du vil vise den reelle verdien som en valuta i appen, bruker du egenskapen **fieldExtenededType**. Du kan bruke egenskapen **numberOfDecimals** til å angi antall desimalplasser som vises.</p> |
| 3           | Date              | Datoformater bestemmes av innstillingene for brukerens **dato, klokkeslett og tallformat** som er angitt under **innstillingen for språk og land/område** i **Brukeralternativer**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Hvis egenskapen **stringOptions** ikke er angitt på **TSTimesheetCustomField** -objektet, gis det et fritekstfelt til brukeren.

    Egenskapen **stringLength** kan brukes til å angi maksimal strenglengde som brukere kan angi.

- Hvis **stringOptions** er angitt på **TSTimesheetCustomField** -objektet, er disse listeelementene de eneste verdiene brukerne kan velge ved å bruke alternativknapper (alternativknapper).

    I dette tilfellet kan strengfeltet fungere som en opplistingsverdi for formålet med brukeroppføringen. Hvis du vil lagre verdien i databasen som en opplisting, må du manuelt tilordne strengverdien tilbake til opplistingsverdien før du lagrer databasen ved hjelp av kommandokjede (se "Bruke kommandokjede i TSTimesheetEntryService-klassen for å lagre en timeregistreringsoppføring fra appen tilbake til databasen" senere i dette emnet for å se et eksempel).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Du kan bruke denne egenskapen til å formatere reelle verdier som valuta. Denne metoden gjelder bare når **fieldBaseType** -verdien er **Reell**.

- **TSCustomFieldExtendedType:None** – Ingen formatering brukes.
- **TSCustomFieldExtendedType::Currency** – Formaterer verdien som valuta.

    Når valutaformatering er aktiv, kan **stringValue** -feltet brukes til å sende valutakoden som skal vises i appen. Verdien er en skrivebeskyttet verdi.

    Feltet **realValue** inneholder pengebeløpet som skal lagres i databasen.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Du kan bruke denne egenskapen til å angi hvor det egendefinerte feltet skal vises i appen.

- **TSCustomFieldSection::Header** – Feltet vises i delen **Vis flere detaljer** i appen. Disse feltene er alltid skrivebeskyttet.
- **TSCustomFieldSection::Line** – Feltet vises etter alle standardlinjefelt i timeregistreringsoppføringer. Disse feltene kan enten være redigerbare eller skrivebeskyttet.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Denne egenskapen identifiserer feltet når verdier som appen gir, lagres tilbake til databasen.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Denne egenskapen identifiserer feltet når verdier som appen gir, lagres tilbake til databasen.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Sett denne egenskapen til **Ja** for å angi at feltet i delen for timeregistreringoppføring bør redigeres av brukere. Sett egenskapen til **Nei** for å gjøre feltet skrivebeskyttet.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Sett denne egenskapen til **Ja** for å angi at feltet i delen for timeregistreringoppføring bør være obligatorisk.

### <a name="label-str"></a>label (str)

Denne egenskapen angir etiketten som vises ved siden av feltet i appen.

### <a name="stringoptions-list-of-strings"></a>stringOptions (liste over strenger)

Denne egenskapen gjelder bare når **fieldBaseType** er satt til **String**. Hvis **stringOptions** er angitt, angis strengverdiene som er tilgjengelige for valget via alternativknapper (alternativknapper), av strengene i listen. Hvis det ikke er angitt noen strenger, tillates fritekstregistrering i strengfeltet (se "Bruke kommandokjede i TSTimesheetEntryService-klassen for å lagre en timeregistreringsoppføring fra appen tilbake til databasen" senere i dette emnet for å se et eksempel).

### <a name="stringlength-int"></a>stringLength (int)

Denne egenskapen angir maksimumslengden for et strengfelt. Den gjelder bare når **fieldBaseType** er satt til **Streng**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Denne egenskapen angir antallet desimaler som vises for et reelt felt. Den gjelder bare når **fieldBaseType** er satt til **Reell**.

### <a name="ordersequence-int"></a>orderSequence (int)

Denne egenskapen kontrollerer i hvilken rekkefølge de egendefinerte feltene vises i appen når mer enn ett egendefinert felt er angitt. Felt som har lavere tall, vises først.

### <a name="booleanvalue-boolean"></a>booleanValue (boolsk)

For felt av typen **Boolsk** sender denne egenskapen den boolske verdien for feltet mellom serveren og appen.

### <a name="guidvalue-guid"></a>guidValue (guid)

For felt av typen **GUID** sender denne egenskapen verdien for den globalt unike identifikatoren (GUID) for feltet mellom serveren og appen.

### <a name="int64value-int64"></a>int64Value (Int64)

For felt av typen **Int64** sender denne egenskapen int64-verdien for feltet mellom serveren og appen.

### <a name="intvalue-int"></a>intValue (int)

For felt av typen **Int** sender denne egenskapen int-verdien for feltet mellom serveren og appen.

### <a name="realvalue-real"></a>realValue (reell)

For felt av typen **Reell** sender denne egenskapen reell-verdien for feltet mellom serveren og appen.

### <a name="stringvalue-str"></a>stringValue (str)

For felt av typen **Streng** sender denne egenskapen streng-verdien for feltet mellom serveren og appen. Det brukes også for felt av typen **Reell** som er formatert som valuta. For disse feltene brukes egenskapen til å sende valutakoden til appen.

### <a name="datevalue-date"></a>dateValue (dato)

For felt av typen **Dato** sender denne egenskapen dato-verdien for feltet mellom serveren og appen.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Vise og lagre et egendefinert felt i delen for timeregistreringsoppføring

Nedenfor vises et skjermbilde fra mobilappen av oppretting av en timeregistreringsoppføring. Den viser felt med flere bokser og et egendefinert felt i delen "Tidsregistrering" som kalles "Test streng" der opplistingsverdien "Andre alternativ" allerede er angitt.

![Egendefinerte felt for teststreng i appen](media/timesheet-entry.jpg)



Nedenfor finner du et skjermbilde fra mobilappen av brukeren som velger et av opplistingsalternativene som er tilgjengelige for det egendefinerte feltet "Teststreng".  De to alternativene er "Første alternativ" og "Andre alternativ" som vises som alternativknapper. Det andre alternativet er allerede valgt.

![Alternativknapper (radioknapper) for det egendefinerte feltet Teststreng](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Utvid TSTimesheetLine-tabellen slik at den inneholder et egendefinert felt

I typiske scenarier er det sannsynlig at dataene for et egendefinert felt i delen for timeregistreringsoppføring blir lagret i TSTimesheetLine-tabellen. Andre tabeller kan imidlertid brukes hvis dataene kan hentes basert på en TSTimesheetTrans-oppføring som er levert, eller hvis den ikke har en bestemt oppføringskontekst (for eksempel hvis feltet er angitt som skrivebeskyttet i prosjektparameterne).

Vær oppmerksom på at egendefinerte felt ikke trenger å ha noen sikkerhetskopi av databaseoppføringer. De kan genereres dynamisk basert på X++-logikk. Denne metoden kan være nyttig i skrivebeskyttede scenarier (se delen "Bruke kommandokjede i TSTimesheetDetails-klassen buildCustomFieldListForHeader-metoden for å fylle ut timeregistreringsdetaljer" for å se et eksempel på dynamisk genererte egendefinerte feltverdier.)

Nedenfor vises et skjermbilde fra Visual Studio av programobjekttreet. Den viser en utvidelse av tabellen TSTimesheetLine med TestLineString-feltet lagt til som et egendefinert felt.

![Linjestreng](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Bruke kommandokjede på buildCustomFieldList-metoden i TSTimesheetSettings-klassen for å vise et felt i delen for timeregistreringsoppføring

Denne koden kontrollerer visningsinnstillingene for feltet i appen. Feltet angir for eksempel felttypen, etiketten, om feltet er obligatorisk, og hvilken del feltet vises i.

Følgende eksempel viser et strengefelt for tidsoppføringer. Dette feltet har to alternativer, **Første alternativ** og **Andre alternativ** , som er tilgjengelige via alternativknapper. Feltet i appen er knyttet til **TestLineString** -feltet som legges til i TSTimesheetLine-tabellen.

Legg merke til bruken av metoden **TSTimesheetCustomField::newFromMetatdata()** for å forenkle initialiseringen av egenskapene for det egendefinerte feltet: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** og **numberOfDecimals**. Du kan også angi disse parameterne manuelt, i henhold til hva du foretrekker.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Bruke kommandokjede på buildCustomFieldListForEntry-metoden i TSTimesheetEntry-klassen for å angi verdier i en timeregistreringsoppføring

Metoden **buildCustomFieldListForEntry** brukes til å angi verdier for de lagrede timeregistreringslinjene i mobilappen. Det kreves en TSTimesheetTrans-oppføring som parameter. Felt fra denne oppføringen kan brukes til å fylle ut verdien for det egendefinerte feltet i appen.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Bruke kommandokjede i TSTimesheetEntryService-klassen til å lagre en timeregistreringsoppføring fra appen tilbake til databasen

Hvis du vil lagre et egendefinert felt tilbake til databasen i vanlig bruk, må du utvide flere metoder:

- Metoden **timesheetLineNeedsUpdating** brukes til å finne ut om linjeoppføringen har blitt endret av brukeren i appen og må lagres i databasen. Hvis ytelse ikke er problematisk, kan denne metoden forenkles, slik at den alltid returnerer **sann**.
- Metodene **PopulateTimesheetLineFromEntryDuringCreate** og **populateTimesheetLineFromEntryDuringUpdate** kan utvides slik at de registrerer verdier i TSTimesheetLine-databaseoppføringen fra TSTimesheetEntry-datakontraktoppføringen som tilbys. I eksemplet nedenfor ser du hvordan tilordningen mellom databasefeltet og oppføringsfeltet utføres manuelt via X++-kode.
- Metoden **PopulateTimesheetWeekFromEntry** kan også utvides hvis det egendefinerte feltet som er tilordnet til **TSTimesheetEntry** -objektet, må skrive tilbake til TSTimesheetLineweek-databasetabellen.

> [!NOTE]
> Følgende eksempel lagrer **firstOption** - eller **secondOption** -verdien som brukeren velger for databasen som en rå strengverdi. Hvis databasefeltet er et felt av typen **Enum** , kan disse verdiene tilordnes manuelt til en opplistingsverdi og deretter lagres i et opplistingsfelt i databasetabellen.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Vise et egendefinert felt i delen for timeregistreringshode

Nedenfor vises et skjermbilde fra mobilappen av en bruker som viser en timeregistrering. Knappen "Mer informasjon" er valgt i det øvre høyre hjørnet for å vise alternativet "Vis flere detaljer".  

![Kommandoen Vis flere detaljer](media/show-more.png)

Nedenfor vises et skjermbilde fra mobilappen som viser delen "Mer" av en timeregistrering. Et egendefinert felt kalt "Utnyttelsesgrad for denne timeregistreringen (beregnet egendefinert felt)" er lagt til i delen for timeregistrering. En skrivebeskyttet verdi på "0,667" er angitt i det egendefinerte feltet.

![Delen Mer](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Utvid TSTimesheetTable-tabellen slik at den inneholder et egendefinert felt

I typiske scenarier er det sannsynlig at dataene for et egendefinert felt i hodedelen blir hentet fra TSTimesheetLine-tabellen. Andre tabeller kan imidlertid brukes hvis dataene kan hentes basert på en TSTimesheetTable-oppføring som er levert, eller hvis den ikke har en bestemt oppføringskontekst (for eksempel hvis feltet er angitt som skrivebeskyttet i prosjektparameterne).

Vær oppmerksom på at egendefinerte felt ikke trenger å ha noen sikkerhetskopi av databaseoppføringer. De kan genereres dynamisk basert på X++-logikk. Eksemplet nedenfor viser denne metoden.

Felt i hodedelen er alltid skrivebeskyttet i appen.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Bruke kommandokjede på buildCustomFieldList-metoden i TSTimesheetSettings-klassen for å vise et felt i hodedelen

Denne koden kontrollerer visningsinnstillingene for feltet i appen. Feltet angir for eksempel felttypen, etiketten, om feltet er obligatorisk, og hvilken del feltet vises i.

Følgende eksempel viser en beregnet verdi i hodedelen i appen.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Bruke kommandokjede på buildCustomFieldListForHeader-metoden i TSTimesheetDetails-klassen for å fylle ut timeregistreringsdetaljer

Metoden **buildCustomFieldListForHeader** brukes til å fylle ut timeregistreringshodedetaljer i mobilappen. Det kreves en TSTimesheetTable-oppføring som parameter. Felt fra denne oppføringen kan brukes til å fylle ut verdien for det egendefinerte feltet i appen. Eksemplet nedenfor leser ingen verdier fra databasen. I stedet brukes X++-logikk til å generere en beregnet verdi som vises i appen.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Andre muligheter for konfigurerbarhet/utvidelse

### <a name="adding-additional-validation-for-the-app"></a>Legge til ytterligere validering for appen

Eksisterende logikk for timeregistreringsfunksjonalitet på databasenivået vil fremdeles fungere som forventet. Hvis du vil avbryte fullføringen av lagre- eller sendoperasjoner og vise en bestemt feilmelding, kan du legge til en **vis feil ("melding til bruker")** i koden via en kommandokjedeutvidelse. Her er tre eksempler på nyttige utvidbare metoder:

- Hvis **validateWrite** i TSTimesheetLine-tabellen returnerer **usann** under en lagringsoperasjon for en timeregistreringslinje, vises det en feilmelding i mobilappen.
- Hvis **validateSubmit** i TSTimesheetTable-tabellen returnerer **usann** under en sending av timeregistrering i appen, vises det en feilmelding for brukeren.
- Logikk som fyller ut feltene (for eksempel **Linjeegenskap** ) under **innsetting** -metoden i TSTimesheetLine-tabellen, kjører fremdeles.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Skjule og merke standardfelt som skrivebeskyttet via konfigurasjon

Du kan bruke prosjektparameterne til å skrivebeskytte eller skjule standardfelt i mobilappen. Angi alternativene i delen **Mobile timeregistreringer** i kategorien **Timeregistrering** på siden **Parametere for prosjektstyring og regnskap**.

![Prosjektparametere](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Endre aktivitetene som er tilgjengelige for valg via utvidelser

Aktivitetene som er tilgjengelige for valg for et prosjekt, fylles ut via metodene **getActivitiesForProject()** og **getActivityQuery()** i klassen **TsTimesheetProjectService**. Du kan bruke kommandokjeden til å endre denne virkemåten, slik at den samsvarer med forretningsscenarioet for aktivitetene som er tilgjengelige for valg for et bestemt prosjekt.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Angi en standard prosjektkategori på timeregistreringsoppføringer

Angivelse av en standard prosjektkategori på timeregistreringsoppføringer på tre nivåer. Du kan bruke kommandokjeden til å utvide virkemåten på noen av eller alle disse nivåene for å oppnå den ønskede virkemåten. Følgende hierarki brukes:

1. Appen prøver å angi standardkategorien fra prosjektressursen. Denne standardkategorien angis i metodene **getCurrentUserResource** og **getDelegatedResourcesForCurrentUser** i klassen **TSTimesheetSettingsService**.
2. Hvis standardkategorien ikke er angitt på ressursnivået for prosjektet, prøver appen å hente den fra prosjektaktiviteten. Denne standardkategorien angis i metoden **getActivitiesForProject** i klassen **TSTimesheetProjectService**.
3. Hvis standardkategorien ikke er angitt på aktivitetsnivået for prosjektet, hentes standardkategorien fra prosjektparameterne. Denne standardkategorien angis i metoden **getProjectDetailsbyRule** i klassen **TSTimesheetProjectService**.
