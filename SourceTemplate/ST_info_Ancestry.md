# Ancestry.com collection Source Template

[Home](https://richardotter.github.io)

Download link for the rmst file =
[Ancestry.rmst](https://RichardOtter.github.io/SourceTemplate/rmst/Ancestry.rmst)

## Overview

Records are lumped by Ancestry collection. Therefore this template will be used
multiple times to create a source record for each collection used on Ancestry.

For Ancestry, the problem to be solved is that many of the Source Citations
provided by Ancestry are not good enough to use as is.

Of course, one could simply reference the Ancestry source web page, but that
wouldn't provide any information on reliability of the source and relies on
an Ancestry subscription for access.

The goal for the Ancestry template was to capture all of the information
that Ancestry provides and later figure out what the footnote sentences
should be. I think that I've now done that. At least for most cases.

## Terminology

In order to get the terminology straight, let's use an example from
Ancestry, the collection named "Indiana, U.S., Birth Certificates,
1907-1944". I will use the word "Source" to refer to the entire
Ancestry collection of that name. RM sometimes uses the term
Master Source. It's the same thing. The source's main web page is at:\
[Indiana, U.S., Birth Certificates, 1907-1944](https://www.ancestry.com/search/collections/60871/)

The Ancestry web page where a particular person is listed in that source is
called a Citation. RM sometimes uses the term Source Detail.
It's the same thing.
A example citation to the Indiana Birth Certificates Source is:\
[Birth certificate entry for Anna May Ripberger](https://www.ancestry.com/discoveryui-content/view/5463776:60871)

Information about the Ancestry collection is taken from the collections's main page,
half way down the page, below the search fields, starting with "Source Information",
and continuing with the section "About Indiana, U.S., Birth Certificates, 1907-1944".

Note the subsection in the About section labeled "Original data:". We will use
that later. Some sources have a sentence or two, while others are very long.
This will need attention.
Never include more than a sentence or two in the Original Data field.
If it is longer give a summary and reference the online or file attachment.

## Template details

The template contain the template name, an optional description, the filed names,
hints, and the sentences to be used to form the footnotes. etc.

```text
Source Template= _Ancestry Database
Version= 2025-02-18

Field          Type       Display name
-----------------------------------------------------

Source Fields
Title           Text    Anc. collection name -short
DateSource      Date    Date source last updated
SrcInfo         Text    Anc. collection name -full
OrigData        Text    Original data 
dbID            Text    Anc. collection number

Citation Fields
Name            Name    Person #1 name
BirthDate       Date    Person #1 birth date
Name2           Name    Person #2 name
EventDate       Date    Event date
ANC_SRC_ID      Text    Ancestry source ID
CD              Text    Citation detail
SrcCitation     Text    Citation provided by Anc.
DateCitation    Date    Date citation last updated
```

### Source Data

For the source data examples below, the
[Indiana, U.S., Birth Certificates, 1907-1944](https://www.ancestry.com/search/collections/60871/)
is used.

#### Ancestry database name -short

FieldName=Name, Type=Text
>Example Title = Indiana, U.S., Birth Certificates, 1907-1944

Find this data in Source Info section of the collection main page whose URL is above.
The first sentence is the Ancestry full name-

Indiana Archives and Records Administration
Ancestry.com. Indiana, U.S., Birth Certificates, 1907-1944 [database on-line].
Lehi, UT, USA: Ancestry.com Operations, Inc., 2016.

In this case, Ancestry gives the original data provider top
billing in a separate sentence.
Just use the part starting with  "Ancestry.com".
The first part will go into the original data field.

This field uses a shortened version to improve readability:\
New York, New York, U.S., Birth Index, 1910-1965

#### Date source last updated

FieldName=DateSource, Type=Date
>Example DateSource = 2 Jan 2024

This field contains the date on which this source record was entered
into RM, or last updated in RM. Use today's date.

#### Ancestry database name -full

FieldName=SrcInfo, Type=Text
>Example SrcInfo = Ancestry.com. Indiana, U.S., Birth Certificates,
1907-1944 [database on-line]. Lehi, UT, USA: Ancestry.com Operations, Inc., 2016.

Use the Ancestry supplied name in full.
Looks at Source Info section of the collection page whose URL is above.
The first sentence is the Ancestry full name- Ancestry.com.
New York, New York, U.S., Birth Index, 1910-1965 [database on-line].
Lehi, UT, USA: Ancestry.com Operations, Inc., 2017.

#### Original data

FieldName=OrigData, Type=Text
>Example OrigData = Indiana State Board of Health. Birth Certificates, 1907-1944.
Microfilm. Indiana Archives and Records Administration, Indianapolis, Indiana.

Use the Ancestry supplied info in the Source Info section of the collection
page whose URL is above.
The second sentence is the Ancestry original data info-

Note, not all Ancestry collections have this information listed and some will
have far too much text to use in this field.

#### Ancestry Database ID

FieldName=dbID, Type=Text
>Example dbID = 60871

The is the Ancestry database number. It can be found in the URL that points
to the collection main page.

### Citation Data

For the citation data examples below, the
[Indiana, U.S., Birth Certificates, 1907-1944](https://www.ancestry.com/search/collections/60871/)
is used.

#### Citation Name

Autogenerated by RM. In this case:
>Anna May Ripberger; 2 May 1929; ; 2 May 1929; 60871::5463776; ; Indiana
Archives and Records Administration; Indianapolis, Indiana;
Birth Records; Year: 1929; Roll: 010; 4 September 2022

#### Person #1 name

FieldName=Name, Type=Name
>Example Name = Anna May Ripberger

The name for the citation.

#### Person #1 birth date

FieldName=BirthDate, Type=Date
>Example BirthDate = 2 May 1929

Birth date of the focus person. All normal date modifiers allowed.

#### Person #2 name

FieldName=Name2, Type=Name
>Example Name2 = [blank]

If the citation is for a couple, (marriage, divorce) then the
second name goes here. Otherwise leave empty.

#### Event date

FieldName=EventDate, Type=Date

Example EventDate = 2 May 1929

Date of event from the source. May be same as birth date for
birth record. Sometimes blank.

#### Ancestry source ID

FieldName=ANC_SRC_ID, Type=Text
>Example ANC_SRC_ID = 60871::5463776

This is the database number : record number\
Gotten from the URL, or ORA panel.

#### Citation detail

FieldName=CD, Type=Text
>Example CD = [blank]

Some other information about this citation goes into this Citation Detail field.
May be used if there are multiple citations to the same record in a source,
or to describe the citation in some way. Usually left blank.

#### Ancestry Source Citation

FieldName=SrcCitation, Type=Text
>Example SrcCitation = Indiana Archives and Records Administration; Indianapolis,
Indiana; Birth Records; Year: 1929; Roll: 010

This is the full contents of the Ancestry provided Source Citation. Not all
collections have this info. It is often not very helpful, other times it is crucial.

Look in the Source tab in the center of the page, (next to the Detail tab).
The first paragraph is labeled "Source Citation". If it exists for the citation
being entered, that's what goes in into the SrcCitation field.

Leave empty if source citation is not provided.

#### Date citation last updated

FieldName=DateCitation, Type=Date
>Example DateCitation = 2 Jan 2024

This field contains the date on which this citation record was entered, or
last updated in RM. Most importantly, it should reflect the last time that the
online data was accessed.

## Citations produced

### Footnote

>Ancestry.com. Indiana, U.S., Birth Certificates, 1907-1944 [database on-line].
Lehi, UT, USA: Ancestry.com Operations, Inc., 2016.
Entry for: Anna May Ripberger, event date: 2 May 1929, accessed:
4 September 2022. Citing: Indiana State Board of Health.
Birth Certificates, 1907-1944. Microfilm.
Indiana Archives and Records Administration, Indianapolis, Indiana.

### Short footnote

>Indiana, U.S., Birth Certificates, 1907-1944, entry for:
Anna May Ripberger, event: 2 May 1929

### Bibliography

>Ancestry.com. Indiana, U.S., Birth Certificates, 1907-1944
[database on-line]. Lehi, UT, USA: Ancestry.com Operations, Inc., 2016.

## rmst File Analysis

This is the relevant part of the rmst file. End tags a\have been removed.

```text
<SourceTemplates>
    <Copyright>RootsMagic source templates, template language, and
    template file format are copyright 2009-2020 RootsMagic, Inc. 
    All rights reserved.
    
    <Template Id="10068">
        <Name>_Ancestry Database
        <Description>version 2025-02-18

Used to cite a source collection on the Ancestry.com website.

        <Category>
        
        <Footnote>[SrcInfo] Entry for: [Name]< and [Name2]>, event date: [EventDate], accessed: [DateCitation]. Citing: [OrigData].< [CD]>
        
        <ShortFootnote>[Title], entry for: [Name]< and [Name2]>, event: [EventDate]<, [CD]>
    
        <Bibliography>[SrcInfo]
        

        <Field>
            <Type>Text
            <Name>Title
            <Display>Anc. collection name -short
            <Hint>
            <Detail>false
            <LongHint>

        <Field>
            <Type>Date
            <Name>DateSource
            <Display>Date source last updated
            <Hint>
            <Detail>false
            <LongHint>

        <Field>
            <Type>Text
            <Name>SrcInfo
            <Display>Anc. collection name -full
            <Hint>
            <Detail>false
            <LongHint>

        <Field>
            <Type>Text
            <Name>OrigData
            <Display>Original data
            <Hint>Not applicable to all collections
            <Detail>false
            <LongHint>

        <Field>
            <Type>Text
            <Name>dbID
            <Display>Anc. collection number
            <Hint>Found in URL
            <Detail>false
            <LongHint>

        <Field>
            <Type>Name
            <Name>Name
            <Display>Person #1 name
            <Hint>
            <Detail>true
            <LongHint>

        <Field>
            <Type>Date
            <Name>BirthDate
            <Display>Person #1 birth date
            <Hint>Not necessarily from record.
            <Detail>true
            <LongHint>

        <Field>
            <Type>Name
            <Name>Name2
            <Display>Person #2 name
            <Hint>Only entered for couple events (marriage, dev etc)
            <Detail>true
            <LongHint>

        <Field>
            <Type>Date
            <Name>EventDate
            <Display>Event date
            <Hint>
            <Detail>true
            <LongHint>

        <Field>
            <Type>Text
            <Name>ANC_SRC_ID
            <Display>Ancestry source ID
            <Hint>
            <Detail>true
            <LongHint>

        <Field>
            <Type>Text
            <Name>CD
            <Display>Citation detail
            <Hint>
            <Detail>true
            <LongHint>

        <Field>
            <Type>Text
            <Name>SrcCitation
            <Display>Citation provided by Anc.
            <Hint>Leave empty if none
            <Detail>true
            <LongHint>

        <Field>
            <Type>Date
            <Name>DateCitation
            <Display>Date citation last updated
            <Hint>
            <Detail>true
            <LongHint>
```
