---
title: Family Tress Source Template
---
[Home](https://richardotter.github.io)

# RR Family Tree Data Source Template

Download link for rmst file =
[RR Family Tree Data.rmst](https://RichardOtter.github.io/SourceTemplate/rmst/RR%20Family%20Tree%20Data.rmst)

## Overview

Records created by users at the various online genealogy sites can be cited using this template.
Records are lumped by the tree, either a member created tree, or a universal tree.
The template name bins with "RR"indicating that is falls into the Research Report category.

## Template details

These contain the template name, an optional description , the filed names, hints,  and the sentences to be used to form the footnotes. etc.

```text
Source Template= _RR Family Tree Data

Field                   Type       Display name
-----------------------------------------------------

Source Fields
NameService             Text        Website Name
NameTree                Text        Tree Name
NameOwner               Text        Tree Owner
TreeID                  Text        Tree ID
DateSource              Date        Date Source last updated

Citation Fields
Person                  Name        Person
DateBirth               Date        Birth Date
PersonID                Text        Person ID
CD                      Text        Citation Detail
DateCitation            Date        Date Citation last updated
```

## Worked example - Source Fields

For Source fields example, , I'll use: <a href="https://www.ancestry.com/search/collections/6224/records/45336434">1930 United States Federal Census</a>

### Website Name

FieldName=NameService, Type=Text\
Example NameService = 1930 US Federal Census, population schedules

### Tree Name

FieldName = NameTree, Type=Text\
Example NameTree = T-0626

See my notes on data entry for the census for the complete list.

### Tree Owner

FieldName=NameOwner, Type=Text\
Example NameOwner = Minnesota

### Tree ID

FieldName=TreeID, Type=Text\
Example TreeID = Minnesota

### Date Source last updated

FieldName=DateSource, Type=Date\
Example DateSource = 30 March 2023

## Worked example - Citation fields

### Person

FieldName=Person, Type=Name\
Example Person = Francis W Myers

I use the spelling of the name as I have for the primary or married name in the person database.
Use the same nick name as in the census. This is not done consistently right now.

### Birth date

FieldName=DateBirth, Type=Date\
Example DateBirth = 28 April 1885

### Person ID

FieldName=PersonID, Type=Text\
Example PersonID = 

### Citation Detail

FieldName=CD, Type=Text\
Example CD = [blank]

Whatever info needed to explain what info this citation provides. Usually blank.

### Date Citation last updated

FieldName=DateCitation, Type=Date\
Example DateCitation = 12 February 2024

Last date citation wsa updated, accessed online.


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
