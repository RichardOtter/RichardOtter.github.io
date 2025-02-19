# US Federal Census Ancestry or FamilySearch Source Template

[Home](https://richardotter.github.io)

Download link for rmst file =
[US Federal Census.rmst](https://RichardOtter.github.io/SourceTemplate/rmst/US%20Fed%20Census.rmst)

## Overview

Records are lumped by Census year and State. So this template will be
used multiple times to create a source record for each State-Year combination required.
I'm still not sure if lumping by state is beneficial.

US Census records are available from many sources. I have made these template
to work specifically with Ancestry and/or FamilySearch, but those specifics are minor.

## Template details

These contain the template name, an optional description , the filed names, hints,  and the sentences to be used to form the footnotes. etc.

```text
Source Template= _Census: 1850-1950 US Federal (by site-year-state)
Version= 2025-02-18

Field                   Type       Display name
-----------------------------------------------------

Source Fields
RecordType              Text        Record Type
NARA_PROD               Text        NARA Product ID
PlaceState              Text        US State
DateSource              Date        Date Source

Citation Fields
Household               Name        Household
DateHeadBirth           Date        Head's birth date
DateSheet               Date        Date on Sheet
PlaceFull               Place       Place -full
PlaceLocality           Text        Locality
PlaceCounty             Text        County
PlaceStreet             Text        Street name
PlaceHouseNumber        Text        House Number
EnumerationDistrict     Text        Enumeration Dist
SheetLineNumber         Text        Sheet Line
DwellingSN              Text        Household SN
FilmRollNumber          Text        NARA Roll #
ANC_SRC_ID              Text        Ancestry source ID
FS_SRC_ID               Text        FamilySearch Src ID
DateCitation            Date        Date Citation
CD                      Text        Citation Detail
```

## Source Data

For the source data examples below, the
[1930 United States Federal Census](https://www.ancestry.com/search/collections/6224/records/45336434)
is used.

### Record Type

FieldName=RecordType, Type=Text
>Example RecordType = 1930 US Federal Census, population schedules

### NARA Product ID

FieldName = NARA_PROD, Type=Text
>Example NARA_PROD = T-0626

See my notes on data entry for the census for the complete list.

### US State

FieldName=PlaceState, Type=Text
>Example PlaceState = Minnesota

### Date Source updated

FieldName=DateSource, Type=Date
>Example DateSource = 30 March 2023

## Citation Data

For the citation data examples below, the
[1930 United States Federal Census](https://www.ancestry.com/search/collections/6224/records/45336434)
is used.

### Household

FieldName=Household, Type=Name
>Example Household = Francis W Myers

I use the spelling of the name as I have for the primary or married
name in the person database.
Use the same nick name as in the census. This is not done consistently right now.

### Head's birth date

FieldName=DateHeadBirth, Type=Date
>Example DateHeadBirth = 28 April 1885

Not necessarily from record. Only for identification.

### DateSheet

FieldName=DateSheet, Type=Date
>Example DateSheet = 3 April 1930

### Place -full

FieldName=PlaceFull, Type=Place
>Example PlaceFull = Saint Paul, Ramsey, Minnesota, United States

As the place appears in the Place tab in the database.

### Locality

FieldName=PlaceLocality, Type=Text
>Example PlaceLocality = Saint Paul

Found at the top right corner of census sheet.

### County

FieldName=PlaceCounty, Type=Text
>Example PlaceCounty = Ramsey

Found at the top right corner of census sheet.

### Street name

FieldName=PlaceStreet, Type=Text
>Example PlaceStreet = Asbury

### House Number

FieldName=PlaceHouseNumber, Type=Text
>Example PlaceHouseNumber = 676

### Enumeration Dist

FieldName=EnumerationDistrict, Type=Text
>Example EnumerationDistrict = 62-133

### Sheet Line

FieldName=SheetLineNumber, Type=Text
>Example SheetLineNumber = 4B, line 80-94

See data entry document for format.

### Household SN

FieldName=DwellingSN, Type=Text
>Example DwellingSN = 66

See data entry document for contents. Varies over the years..

### NARA Roll \#

FieldName=FilmRollNumber, Type=Text
>Example FilmRollNumber = 01121; FHL 2340856

For 1930 census, I include the FamilyHistory Library film number.
See data entry document.

### Ancestry source ID

FieldName=ANC_SRC_ID, Type=Text
>Example ANC_SRC_ID = 6224::78708024

### FamilySearch Src ID

FieldName=FS_SRC_ID, Type=Text
>Example FS_SRC_ID = ark:/61903/1:1:X3DQ-FMW

### Date Citation

FieldName=DateCitation, Type=Date
>Example DateCitation = 12 February 2024

Last date citation wsa updated, accessed online. 

### Citation Detail

FieldName=CD, Type=Text
>Example CD = [blank]

Whatever info needed to explain what info this citation provides. Usually blank.

## Citations produced

### Footnote

>1930 US Federal Census, population schedules, Ramsey County, Minnesota, ED 62-133, sheet 4B, line 80-94, (Francis W Myers household), US National Archives, T-0626_01121; FHL 2340856, accessed on 12 February 2024 at Ancestry.com, ID=6224::78708024

### Short footnote

>1930 US Federal Census, population schedules, Ramsey County, Minnesota, ED 62-133, sheet 4B, line 80-94, Francis W Myers

### Bibliography

>1930 US Federal Census, population schedules, Ramsey County, Minnesota

## rmst File Analysis

This is the relevant part of the rmst file. The end tags have been removed.

```text
<SourceTemplates>
    <Copyright>RootsMagic source templates, template language, and template file format are copyright 2009-2020 RootsMagic, Inc.  All rights reserved.
    
    <Template Id="10054">
        <Name>_Census: 1850-1950 US Federal (by site-year-state)
        <Description>version 2025-02-18

Used to cite US census records

        <Category>
        
        <Footnote>[RecordType], [PlaceCounty] County, [PlaceState], &lt;ED [EnumerationDistrict], &gt;sheet [SheetLineNumber], ([Household] household), US National Archives, [NARA_PROD]_[FilmRollNumber], accessed on [DateCitation] at Ancestry.com, ID=[ANC_SRC_ID]
        
        <ShortFootnote>[RecordType], [PlaceCounty] County, [PlaceState], &lt;ED [EnumerationDistrict], &gt;sheet [SheetLineNumber], [Household]</
        
        <Bibliography>[RecordType], [PlaceCounty] County, [PlaceState]
        
        <Field>
            <Type>Text
            <Name>RecordType
            <Display>Record Type
            <Hint>
            <Detail>false
            <LongHint>

        <Field>
            <Type>Text
            <Name>NARA_PROD
            <Display>NARA Product ID
            <Hint>National Archives Product ID
            <Detail>false
            <LongHint>e.g. ..T-1234   use leading zeros to fill 4 digit field

        <Field>
            <Type>Text
            <Name>PlaceState
            <Display>US State
            <Hint>State or Territory
            <Detail>false
            <LongHint>

        <Field>
            <Type>Date
            <Name>DateSource
            <Display>Date Source
            <Hint>Date source created or last updated
            <Detail>false
            <LongHint>

        <Field>
            <Type>Name
            <Name>Household
            <Display>Household Head
            <Hint>
            <Detail>true
            <LongHint>GivenName FamilyName 

        <Field>
            <Type>Date
            <Name>DateHeadBirth
            <Display>Head&apos;s birth date
            <Hint>for identification
            <Detail>true
            <LongHint>This is not what is reported in census, but from best available information.

        <Field>
            <Type>Date
            <Name>DateSheet
            <Display>Date on Sheet
            <Hint>Date census was taken for this household
            <Detail>true
            <LongHint>

        <Field>
            <Type>Place
            <Name>PlaceFull
            <Display>Place -full
            <Hint>as in database places list
            <Detail>true
            <LongHint>Use same name as used in this RootsMagic database...e.g...Chicago, Cook, Illinois, United States..

        <Field>
            <Type>Text
            <Name>PlaceLocality
            <Display>Locality
            <Hint>
            <Detail>true
            <LongHint>

        <Field>
            <Type>Text
            <Name>PlaceCounty
            <Display>County
            <Hint>
            <Detail>true
            <LongHint>

        <Field>
            <Type>Text
            <Name>PlaceStreet
            <Display>Street name
            <Hint>
            <Detail>true
            <LongHint>

        <Field>
            <Type>Text
            <Name>PlaceHouseNumber
            <Display>House Number
            <Hint>
            <Detail>true
            <LongHint>

        <Field>
            <Type>Text
            <Name>EnumerationDistrict
            <Display>Enumeration Dist
            <Hint>
            <Detail>true
            <LongHint>

        <Field>
            <Type>Text
            <Name>SheetLineNumber
            <Display>Sheet Line
            <Hint>Sheet, line range
            <Detail>true
            <LongHint>e.g...79, line 5..45, line 3-4..23, line 29-30 &amp; 24, line 1-2

        <Field>
            <Type>Text
            <Name>DwellingSN
            <Display>Household SN
            <Hint>Dwelling Serial Number
            <Detail>true
            <LongHint>Do not confuse with house number...Census year..1950     Dwelling ..1940     Household

        <Field>
            <Type>Text
            <Name>FilmRollNumber
            <Display>NARA Roll #
            <Hint>National Archives Roll Number
            <Detail>true
            <LongHint>e.g...12345..Include leading zeros to fill 5 digit field

        <Field>
            <Type>Text
            <Name>ANC_SRC_ID
            <Display>Ancestry source ID
            <Hint>
            <Detail>true
            <LongHint>e.g.  62308::207402110

        <Field>
            <Type>Text
            <Name>FS_SRC_ID
            <Display>FamilySearch Src ID
            <Hint>
            <Detail>true
            <LongHint>e.g.   ark:/61903/1:1:6XTB-ZCT6

        <Field>
            <Type>Text
            <Name>CD
            <Display>Citation Detail
            <Hint>
            <Detail>true
            <LongHint>

        <Field>
            <Type>Date
            <Name>DateCitation
            <Display>Date Citation
            <Hint>Date citation created or last updated
            <Detail>true
            <LongHint>

```
