---
title: US Federal Census Source Template
---
[Home](https://richardotter.github.io)

# US Federal Census Source Template

Download link for rmst file =
[US Federal Census.rmst](https://RichardOtter.github.io/SourceTemplate/rmst/US%20Fed%20Census.rmst)

## Template details
```
Source Template= _Census: 1850-1950 US Federal -L (by site-year-state)

Field                   Type       Display name
------------------------------------------------

Source Fields
RecordType              Text        Record Type
NARA_PROD               Text        NARA Product ID
PlaceState              Text        US State
DateSource              Date        Date Source updated

Citation Fields
Household               Name        Household
DateHeadBirth           Date        >Head's birth date
Date on Sheet           Date        DateSheet
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


Citation field description
Name
Not necessarily exactly as in FG database
Use the ORA -Name field. This takes the birth name in italics and encloses it in parentheses.
Remove name prefixes. 

DateBirth 
Not necessarily from record. Only for identification.



```

### rmst File Analysis
This is the relevant part of the rmst file. I removed most end tags and empty tags.


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
