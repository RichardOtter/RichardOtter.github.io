---
title: US Federal Census Source Template
---
[Home](https://richardotter.github.io)

# US Federal Census Ancestry or FamilySearch Source Template

Download link for rmst file =
[US Federal Census.rmst](https://RichardOtter.github.io/SourceTemplate/rmst/US%20Fed%20Census.rmst)

## Overview

Records are lumped by Census year and State. So this template will be
used multiple times to create a source record for each State-Year combination required.
I'm still not sure if lumping by state is beneficial.

US Census records are available from many sources. I have made these template to work specifically with Ancestry and/or FamilySearch, but those specifics are minor.

## Template details

These contain the template name, an optional description , the filed names, hints,  and the sentences to be used to form the footnotes. etc.

```text
Source Template= _Census: 1850-1950 US Federal -L (by site-year-state)

Field                   Type       Display name
-----------------------------------------------------

Source Fields
RecordType              Text        Record Type
NARA_PROD               Text        NARA Product ID
PlaceState              Text        US State
DateSource              Date        Date Source updated

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

## Worked example - Source Fields

For Source fields example, , I'll use: <a href="https://www.ancestry.com/search/collections/6224/records/45336434">1930 United States Federal Census</a>

### Record Type

FieldName=RecordType, Type=Text\
Example RecordType = 1930 US Federal Census, population schedules

### NARA Product ID

FieldName = NARA_PROD, Type=Text\
Example NARA_PROD = T-0626

See my notes on data entry for the census for the complete list.

### US State

FieldName=PlaceState, Type=Text\
Example PlaceState = Minnesota

### Date Source updated

FieldName=DateSource, Type=Date\
Example DateSource = 30 March 2023

## Worked example - Citation fields

### Household

FieldName=Household, Type=Name\
Example Household = Francis W Myers

I use the spelling of the name as I have for the primary or married name in the person database.
Use the same nick name as in the census. This is not done consistently right now.

### Head's birth date

FieldName=DateHeadBirth, Type=Date\
Example DateHeadBirth = 28 April 1885

Not necessarily from record. Only for identification.

### DateSheet

FieldName=DateSheet, Type=Date\
Example DateSheet = 3 April 1930

### Place -full

FieldName=PlaceFull, Type=Place\
Example PlaceFull = Saint Paul, Ramsey, Minnesota, United States

As the place appears in the Place tab in the database.

### Locality

FieldName=PlaceLocality, Type=Text\
Example PlaceLocality = Saint Paul

Found at the top right corner of census sheet.

### County

FieldName=PlaceCounty, Type=Text\
Example PlaceCounty = Ramsey

Found at the top right corner of census sheet.

### Street name

FieldName=PlaceStreet, Type=Text\
Example PlaceStreet = Asbury

### House Number

FieldName=PlaceHouseNumber, Type=Text\
Example PlaceHouseNumber = 676

### Enumeration Dist

FieldName=EnumerationDistrict, Type=Text\
Example EnumerationDistrict = 62-133

### Sheet Line

FieldName=SheetLineNumber, Type=Text\
Example SheetLineNumber = 4B, line 80-94

See data entry document for format.

### Household SN

FieldName=DwellingSN, Type=Text\
Example DwellingSN = 66

See data entry document for contents. Varies over the years..

### NARA Roll #

FieldName=FilmRollNumber, Type=Text\
Example FilmRollNumber = 01121; FHL 2340856

For 1930 census, I include the FamilyHistory Library film number. See data entry document.

### Ancestry source ID

FieldName=ANC_SRC_ID, Type=Text\
Example ANC_SRC_ID = 6224::78708024

### FamilySearch Src ID

FieldName=FS_SRC_ID, Type=Text\
Example FS_SRC_ID = ark:/61903/1:1:X3DQ-FMW

### Date Citation

FieldName=DateCitation, Type=Date\
Example DateCitation = 12 February 2024

Last date citation wsa updated, accessed online. 

### Citation Detail

FieldName=CD, Type=Text\
Example CD = [blank]

Whatever info needed to explain what info this citation provides. Usually blank.

## Citations produced

### Footnote

1930 US Federal Census, population schedules, Ramsey County, Minnesota, ED 62-133, sheet 4B, line 80-94, (Francis W Myers household), US National Archives, T-0626_01121; FHL 2340856, accessed on 12 February 2024 at Ancestry.com, ID=6224::78708024

### Short footnote

1930 US Federal Census, population schedules, Ramsey County, Minnesota, ED 62-133, sheet 4B, line 80-94, Francis W Myers

### Bibliography

1930 US Federal Census, population schedules, Ramsey County, Minnesota

## rmst File Analysis

This is the relevant part of the rmst file. I removed end tags and empty tags.

```text
<Name>_Census: 1850-1950 US Federal -L (by site-year-state)

<Description/>

<Category/>

<Footnote>[RecordType], [PlaceCounty] County, [PlaceState], &lt;ED [EnumerationDistrict], &gt;sheet [SheetLineNumber], ([Household] household), US National Archives, [NARA_PROD]_[FilmRollNumber], accessed on [DateCitation] at Ancestry.com, ID=[ANC_SRC_ID]</Footnote>

<ShortFootnote>[RecordType], [PlaceCounty] County, [PlaceState], &lt;ED [EnumerationDistrict], &gt;sheet [SheetLineNumber], [Household]</ShortFootnote>

<Bibliography>[RecordType], [PlaceCounty] County, [PlaceState]</Bibliography>

<Field>
    <Type>Text
    <Name>RecordType
    <Display>Record Type
    <Detail>false
<Field>
    <Type>Text
    <Name>NARA_PROD
    <Display>NARA Product ID
    <Detail>false
<Field>
    <Type>Text
    <Name>PlaceState
    <Display>US State
    <Detail>false
<Field>
    <Type>Date
    <Name>DateSource
    <Display>Date Source updated
    <Detail>false
<Field>
    <Type>Name
    <Name>Household
    <Display>Household Head
    <Detail>true
<Field>
    <Type>Date
    <Name>DateHeadBirth
    <Display>Head&apos;s birth date
    <Detail>true
<Field>
    <Type>Date
    <Name>DateSheet
    <Display>Date on Sheet
    <Detail>true<
<Field>
    <Type>Place
    <Name>PlaceFull
    <Display>Place -full
    <Detail>true
<Field>
    <Type>Text
    <Name>PlaceLocality
    <Display>Locality
    <Detail>true
<Field>
    <Type>Text
    <Name>PlaceCounty
    <Display>County
    <Detail>true
<Field>
    <Type>Text
    <Name>PlaceStreet
    <Display>Street name
    <Detail>true
<Field>
    <Type>Text
    <Name>PlaceHouseNumber
    <Display>House Number
    <Detail>true
<Field>
    <Type>Text
    <Name>EnumerationDistrict
    <Display>Enumeration Dist
    <Detail>true
<Field>
    <Type>Text
    <Name>SheetLineNumber
    <Display>Sheet Line
    <Detail>true
<Field>
    <Type>Text
    <Name>DwellingSN
    <Display>Household SN
    <Detail>true
<Field>
    <Type>Text
    <Name>FilmRollNumber
    <Display>NARA Roll #
    <Detail>true
<Field>
    <Type>Text
    <Name>ANC_SRC_ID
    <Display>Ancestry source ID
    <Detail>true
<Field>
    <Type>Text
    <Name>FS_SRC_ID
    <Display>FamilySearch Src ID
    <Detail>true
<Field>
    <Type>Date
    <Name>DateCitation
    <Display>Date Citation
    <Detail>true
<Field>
    <Type>Text
    <Name>CD
    <Display>Citation Detail
    <Detail>true
```
