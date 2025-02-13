---
title: Ancestry Source Template
---
[Home](https://richardotter.github.io)

# Ancestry.com collection Source Template

Download link for the rmst file =
[Ancestry.rmst](https://RichardOtter.github.io/SourceTemplate/rmst/Ancestry.rmst)

## Overview

Records are lumped by Ancestry collection. Therefore this template will be used multiple times to create a source record for each collection used on Ancestry.

For Ancestry, the problem to be solved is that many of the Source Citations provided by Ancestry are not good enough to use as is.

Of course, one could simply reference the Ancestry source web page, but that wouldn't provide any information on reliability of the source and relies on an Ancestry subscription for access.

The goal for the Ancestry template was to capture all of the information that Ancestry provides and later figure out what the footnote sentences should be. I think that I've now done that. At least for most cases.

## Terminology

In order to get the terminology straight, let's use an example from Ancestry, the collection named "Indiana, U.S., Birth Certificates, 1907-1944". I will use the word "Source" to refer to the entire Ancestry collection of that name. RM sometimes uses the term Master Source. It's the same thing. The source's main web page is at:\
[Indiana, U.S., Birth Certificates, 1907-1944](https://www.ancestry.com/search/collections/60871/)

The Ancestry web page where a particular person is listed in that source is called a Citation. RM sometimes uses the term Source Detail. It's the same thing. A example citation to the Indiana Birth Certificates Source is:\
[Birth certificate entry for Anna May Ripberger](https://www.ancestry.com/discoveryui-content/view/5463776:60871)

Information about the Ancestry collection is taken from the collections's main page, half way down the page, below the search fields, starting with "Source Information", and continuing with the section "About Indiana, U.S., Birth Certificates, 1907-1944".

Note the subsection in the About section labeled "Original data:". We will use that later. Some sources have a sentence or two, while others are very long. This will need attention.
Never include more than a sentence or two in the Original Data field. If it is longer give a summary and reference the online or file attachment.

## Template details

These contain the template name, an optional description , and the sentences to be used to form the footnotes. etc.

```text
Source Template= _Ancestry -L

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
DateCitation    Date    Date citation last updated
SrcCitation     Text    Citation provided by Anc.

````

### Worked example - Source Fields

For Source fields example, , I'll use: <a href="https://www.ancestry.com/search/collections/60871/">Indiana, U.S., Birth Certificates, 1907-1944</a>

#### Ancestry database name -short

FieldName=Name, Type=Text

Example Title = Indiana, U.S., Birth Certificates, 1907-1944

Find this data in Source Info section of the collection main page whose URL is above.
The first sentence is the Ancestry full name-

Indiana Archives and Records Administration
Ancestry.com. Indiana, U.S., Birth Certificates, 1907-1944 [database on-line]. Lehi, UT, USA: Ancestry.com Operations, Inc., 2016.

In this case, Ancestry gives the original data provider top billing in a separate sentence. Just use the part starting with  "Ancestry.com". The first part will go into the original data field.

This field uses a shortened version to improve readability:\
New York, New York, U.S., Birth Index, 1910-1965

#### Date source last updated

FieldName=DateSource, Type=Date

Example DateSource = 2 Jan 2024

This field contains the date on which this source record was entered into RM, or last updated in RM. Use today's date.

#### Ancestry database name -full

FieldName=SrcInfo, Type=Text

Example SrcInfo = Ancestry.com. Indiana, U.S., Birth Certificates, 1907-1944 [database on-line]. Lehi, UT, USA: Ancestry.com Operations, Inc., 2016.

Use the Ancestry supplied name in full.
Looks at Source Info section of the collection page whose URL is above.
The first sentence is the Ancestry full name-
Ancestry.com. New York, New York, U.S., Birth Index, 1910-1965 [database on-line]. Lehi, UT, USA: Ancestry.com Operations, Inc., 2017.

#### Original data

FieldName=OrigData, Type=Text

Example OrigData = Indiana State Board of Health. Birth Certificates, 1907-1944. Microfilm. Indiana Archives and Records Administration, Indianapolis, Indiana.

Use the Ancestry supplied info in the Source Info section of the collection page whose URL is above.
The second sentence is the Ancestry original data info-


Note, not all Ancestry collections have this information listed and some will have far too much text to use in this field.

#### Ancestry Database ID

FieldName=dbID, Type=Text

Example dbID = 60871

The is the Ancestry database number. It can be found in the URL that points to the collection main page.

#### Other Standard source data

Enter the URL of the Ancestry source as a WebTag for the source:

Example WebTag = Ancestry  /  https://www.ancestry.com/search/collections/60871/

Enter the full text from the Source main page into the Master source "Source Text" field. (I am still deciding on whether this is a good idea. The problem is that is hows in the footnote window and *may* slow down operation for very long text) Do a save as single file and save as external file.

Example Source Information = "
Ancestry.com. New York, New York, U.S., Birth Index, 1910-1965 [database on-line]. Lehi, UT, USA: Ancestry.com Operations, Inc., 2017.
.....
.....
[lots more text]
.....
.....
Borough in which they were born
The images for this collection are provided courtesy of www.vitalsearch-worldwide.com.
"

### Worked example - Citation fields

For citation fields, use the example found at <a href="https://www.ancestry.com/discoveryui-content/view/5463776:60871"> Birth certificate entry for Anna May Ripberger</a>

#### Person #1 name

FieldName=Name, Type=Name

Example Name = Anna May Ripberger

The name for the citation.

#### Person #1 birth date

FieldName=BirthDate, Type=Date

Example BirthDate = 2 May 1929

Birth date of the focus person. All normal date modifiers allowed.

#### Person #2 name

FieldName=Name2, Type=Name

Example Name2 = [blank]

If the citation is for a couple, (marriage, divorce) then the second name goes here. Otherwise leave empty.

#### Event date

FieldName=EventDate, Type=Date

Example EventDate = 2 May 1929

Date of event from the source. May be same as birth date for birth record. Sometimes blank.

#### Ancestry source ID

FieldName=ANC_SRC_ID, Type=Text

Example ANC_SRC_ID = 60871::5463776

This is the database number : record number\
Gotten from the URL.

#### Citation detail

FieldName=CD, Type=Text

Example CD = [blank]

Some other information about this citation goes into this Citation Detail field. May be used if there are multiple citations to the same record in a source, or to describe the citation in some way. Usually left blank.

#### Date citation last updated

FieldName=DateCitation, Type=Date

Example DateCitation = 2 Jan 2024

This field contains the date on which this citation record was entered, or last updated in RM.Most importantly, it should reflect the last time that the online data was accessed.

#### Ancestry Source Citation

FieldName=SrcCitation, Type=Text

Example SrcCitation = Indiana Archives and Records Administration; Indianapolis, Indiana; Birth Records; Year: 1929; Roll: 010

This is the full contents of the Ancestry provided Source Citation. Not all collections have this info. It is often not very helpful, other times it is crucial.

Look in the Source tab in the center of the page, (next to the Detail tab). The first paragraph is labeled "Source Citation". If it exists for the citation being entered, that's what goes in into the SrcCitation field.

#### Other Standard citation data

* Enter the URL of the Ancestry citation as a WebTag for the citation:
Example Citation WebTag = https://www.ancestry.com/discoveryui-content/view/5463776:60871

* Attach source image to Media for the Citation, if an image is available.

* Enter the full text of the Ancestry transcribed record in the Citation "Research Note" field

Example Research Note =

```
Name	Anna May Ripberger
Gender	Female
Birth Date	2 May 1929
Birth Place	Cicero, Tipton, Indiana, USA
Father	John Wm Ripberger
Mother	Gertrude Mary Cauldwell
Certificate Number	24302
Roll number	40474_356481
Volume Range	46 - 50
```

Add your own transcription here as well. Separate them clearly.

## Citations produced

### Footnote

Ancestry.com. Indiana, U.S., Birth Certificates, 1907-1944 [database on-line]. Lehi, UT, USA: Ancestry.com Operations, Inc., 2016. Entry for: Anna May Ripberger, event date: 2 May 1929, accessed: 4 September 2022. Citing: Indiana State Board of Health. Birth Certificates, 1907-1944. Microfilm. Indiana Archives and Records Administration, Indianapolis, Indiana.

### Short footnote

Indiana, U.S., Birth Certificates, 1907-1944, entry for: Anna May Ripberger, event: 2 May 1929

### Bibliography

Ancestry.com. Indiana, U.S., Birth Certificates, 1907-1944 [database on-line]. Lehi, UT, USA: Ancestry.com Operations, Inc., 2016.

## rmst File Analysis

This is the relevant part of the rmst file. I removed end tags and empty tags.

```text
<Name>_Ancestry Database -L

<Description>

<Category>

<Footnote>[SrcInfo] Entry for: [Name]< and [Name2]>, event date: [EventDate], accessed: [DateCitation]. Citing: [OrigData].< [CD]>

<ShortFootnote>[Title], entry for: [Name]< and [Name2]>, event: [EventDate]<, [CD]>

<Bibliography>[SrcInfo]

<Field>
    <Type>Text
    <Name>Title
    <Display>Anc. collection name -short
    <Detail>false
<Field>
    <Type>Date
    <Name>DateSource
    <Display>Date source last updated
    <Detail>false
<Field>
    <Type>Text
    <Name>SrcInfo
    <Display>Anc. collection name -full
    <Detail>false
<Field>
    <Type>Text
    <Name>OrigData
    <Display>Original data
    <Detail>false
<Field>
    <Type>Text
    <Name>dbID
    <Display>Anc. collection number
    <Detail>false
<Field>
    <Type>Name
    <Name>Name
    <Display>Person #1 name
    <Detail>true
<Field>
    <Type>Date
    <Name>BirthDate
    <Display>Person #1 birth date
    <Detail>true
<Field>
    <Type>Name
    <Name>Name2
    <Display>Person #2 name
    <Detail>true
<Field>
    <Type>Date
    <Name>EventDate
    <Display>Event date
    <Detail>true
<Field>
    <Type>Text
    <Name>ANC_SRC_ID
    <Display>Ancestry source ID
    <Detail>true
<Field>
    <Type>Text
    <Name>CD
    <Display>Citation detail
    <Detail>true
<Field>
    <Type>Date
    <Name>DateCitation
    <Display>Date citation last updated
    <Detail>true
<Field>
    <Type>Text
    <Name>SrcCitation
    <Display>Citation provided by Anc.
    <Detail>true
```
