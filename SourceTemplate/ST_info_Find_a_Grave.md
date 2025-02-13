---
title: Find a Grave Source Template
---
[Home](https://richardotter.github.io)

# Find a Grave Source Template

Download link for rmst file =
[Find a Grave.rmst](https://RichardOtter.github.io/SourceTemplate/rmst/Find%20a%20Grave.rmst)

## Overview

Records are lumped into one big group that corresponds to all the memorials on the Find a Grave website. This template will probably be used to create just one source record.

Find a Grave has one main type of record- the memorial. Perhaps one could include the cemetery database as well.
My strategy was to collect as much information as possible from the FG record. When used with the ORA-extension template described later in this file, just about all of the data is collected with just a couple of clicks.
Most will reside in the Citation's Reference Note.
I am also collecting some of that info by saving the citation created by FG in the SrcCitation field. This is optional, but my database uses just that field as the footnote. You may want to construct your own sentences.

## Template details

These contain the template name, an optional description , and the sentences to be used to form the footnotes. etc.

```text
Source Template= _Find-a-Grave

Field              Type       Display name
-----------------------------------------------------

Source Fields
TitleDatabase      Text       Database name
DateDatabase       Date       Last DB info update

Citation Fields
Name               Name       Person name
DateBirth          Date       Person's birth date
CD                 Text       Citation Detail
PlaceBurial        Place      Place of Burial
PlaceCemetery      Text       Cemetery name
EntryNumber        Text       Memorial number
Transcription      Text       Transcription
DateCitation       Date       Date citation updated
SrcCitation        Text       FG Citation
```

## Worked example - Source Fields

For an example, use Find a Grave memorial: https://www.findagrave.com/memorial/159991905

### Database name

FieldName=TitleDatabase, Type=Text\
Example TitleDatabase = Find a Grave, database and images (www.findagrave.com)

### Last DB info update

FieldName=DateDatabase, Type=Date\
Example DateDatabase = 10 February 2023

## Worked example - Citation fields

### Person name

FieldName=Name, Type=Name\
Example Name = Ann May (Ripberger) Clark

Not necessarily exactly as in FG database
Use the ORA -Name field. This takes the birth name in italics and encloses it in parentheses.
Remove name prefixes.

### Person's birth date

FieldName=DateBirth, Type=Date\
Example DateBirth = 2 May 1929

Not necessarily from record. Only for identification.

### Citation Detail

FieldName=CD, Type=Text\
Example CD = Gravestone transcription

Currently, use only for\
	"Gravestone transcription"  if Transcription = D\
	OBITUARY\

### Place of Burial

FieldName=PlaceBurial, Type=Place\
Example PlaceBurial = Bonita Springs, Lee County, Florida, USA

Direct copy from FG

### Cemetery name

FieldName=PlaceCemetery, Type=Text\
Example PlaceCemetery = Bonita Springs Cemetery

Direct copy from FG

### Memorial number

FieldName=EntryNumber, Type=Text\
Example EntryNumber = 159991905

Direct copy from FG

### Transcription

FieldName=Transcription, Type=Text\
Example Transcription = D

This is actually a flag to indicate how to interpret the data.\
	N= No image available\
	A= Grave marker image available, but transcription not yet done,\
	D= Transcription done and is in RM_Research_Note.\
Only type D is primary data that you can see for yourself: the grave stone text.

### Date citation updated

FieldName=DateCitation, Type=Date\
Example DateCitation = 9 July 2023

Date that this citation last updated. (Judgment call when to change this)

### FG Citation

FieldName=SrcCitation, Type=Text\
Example SrcCitation = Find a Grave, database and images (https://www.findagrave.com/memorial/159991905/ann-may-clark: accessed 9 July 2023), memorial page for Ann May Ripberger Clark (2 May 1929–10 Feb 2016), Find a Grave Memorial ID 159991905, citing Bonita Springs Cemetery, Bonita Springs, Lee County, Florida, USA; Maintained by Bonita (contributor 47272930).

Direct copy from FG

### Other Standard citation data

* Enter the URL of the Find a Grave memorial as a WebTag for the citation.

* Attach whatever images to Media for the Citation.

* Enter whatever text of the memorial into the Citation "Research Note" field.\
The ORA-extension template takes care of this as well.

## Citations produced

### Footnote

Find a Grave, database and images (https://www.findagrave.com/memorial/159991905/ann-may-clark: accessed 9 July 2023), memorial page for Ann May Ripberger Clark (2 May 1929–10 Feb 2016), Find a Grave Memorial ID 159991905, citing Bonita Springs Cemetery, Bonita Springs, Lee County, Florida, USA; Maintained by Bonita (contributor 47272930).; Gravestone transcription

### Short footnote

Find a Grave, database and images (www.findagrave.com); Entry for: Ann May "Ripberger" Clark; Memorial ID: 159991905; Gravestone transcription

### Bibliography

Find a Grave, database and images (www.findagrave.com)

## rmst File Analysis

This is the relevant part of the rmst file. I removed end tags and empty tags.

```text
<Name>_Find-a-Grave

<Description/>

<Footnote>[SrcCitation]<;  [CD]>

<ShortFootnote>[TitleDatabase]; Entry for: [Name]; Memorial ID: [EntryNumber]<;  [CD]>

<Bibliography>[TitleDatabase]


<Field>
	<Type>Text
	<Name>TitleDatabase
	<Display>Database name
	<Detail>false
<Field>
	<Type>Date
	<Name>DateDatabase
	<Display>Last DB info update
	<Detail>false
<Field>
	<Type>Name
	<Name>Name
	<Display>Person name
	<Hint>Not necessarily exactly as in FG database
	<Detail>true
<Field>
	<Type>Date
	<Name>DateBirth
	<Display>Person&apos;s birth date
	<Hint>Not necessarily from record. Only for identification.
	<Detail>true
<Field>
	<Type>Text
	<Name>CD
	<Display>Citation Detail
	<Detail>true
<Field>
	<Type>Place
	<Name>PlaceBurial
	<Display>Place of Burial
	<Detail>true
<Field>
	<Type>Text
	<Name>PlaceCemetery
	<Display>Cemetery name
	<Detail>true
<Field>
	<Type>Text
	<Name>EntryNumber
	<Display>Memorial number
	<Detail>true
<Field>
	<Type>Text
	<Name>Transcription
	<Display>Transcription
	<Hint>A=Avail, D=Done, N=NotAvailable
	<Detail>true
<Field>
	<Type>Date
	<Name>DateCitation
	<Display>Date citation updated
	<Detail>true
<Field>
	<Type>Text
	<Name>SrcCitation
	<Display>FG Citation
	<Detail>true
```

## ORA-extension

### AutoType Templates

POSITION 1
```
NAME:
RJO Custom FG
....................BEGIN
[=:template_ver:2024-09-04-1]
{PERCHAR=10}
{FAST}
{10}{TAB}[Name]
{10}{TAB}[Birth Date]
{10}{TAB*2}[Burial Place]
{10}{TAB}[Cemetery Name]
{10}{TAB}[Record ID]
{10}{TAB*2}
{SLOW}
[Page.Access Date]
{10}{TAB}
[Source.Citation]
{10}{TAB}
{RIGHT}
{10}
{FAST}
[var.FG_details_section]
{ENTER}
ORA template v[template_ver], var v[var_ver]
{ENTER}
....................END
```

POSITION 2
```
NAME:
RJO Custom FG  RJO created FG memorials
Transcription=D, CD=Gravestone transcription
....................BEGIN
[=:template_ver:2024-09-04-1]
{PERCHAR=10}
{FAST}
{10}{TAB}[Name]
{10}{TAB}[Birth Date]
{10}{TAB}Gravestone transcription
{10}{TAB}[Burial Place]
{10}{TAB}[Cemetery Name]
{10}{TAB}[Record ID]
{10}{TAB}D
{10}{TAB}
{SLOW}
[Page.Access Date]
{10}{TAB}
[Source.Citation]
{10}{TAB}
{RIGHT}
{10}
{FAST}
[var.FG_details_section]
{ENTER}
ORA template v[template_ver], var v[var_ver]
{ENTER}
....................END
```

### Text Template

This is used by the autotype templates

```text
NAME:
var.FG_details_section
....................BEGIN
[==:var_ver:2024-09-04-1]
===========================================DIV50=={ENTER}
Find a Grave record{ENTER}
{ENTER}
===========================================DIV50=={ENTER}
Page information{ENTER}
URL=--=[URL]{ENTER}
Memorial/Record ID=--=[Record ID]{ENTER}
{ENTER}
Person information{ENTER}
Name=--=[Name]{ENTER}
GivenName=--=[GivenName]{ENTER}
Surname=--=[Surname]{ENTER}
MaidenName=--=[MaidenName]{ENTER}
{ENTER}
Birth Date=--=[Birth Date]{ENTER}
Birth Place=--=[Birth Place]{ENTER}
Death Date=--=[Death Date]{ENTER}
Death Place=--=[Death Place]{ENTER}
{ENTER}
Burial information{ENTER}
Cemetery Name=--=[Cemetery Name]{ENTER}
Burial Place=--=[Burial Place]{ENTER}
Plot=--=[Plot]{ENTER}
LatLong=--=[LatLong]{ENTER}
{ENTER}
Biography=----={ENTER}[DOM:queryInner:.biotext-wrapper:1:replace:\n\n:{ENTER}]{ENTER}
=----={ENTER}
{ENTER}
Grave marker information{ENTER}
Inscription=----={ENTER}[Inscription:replace:<br>:{ENTER}]{ENTER}
=----={ENTER}
Gravesite details=----={ENTER}[Gravesite details:replace:<br>:{ENTER}]{ENTER}
=----={ENTER}
{ENTER}
Contributor information{ENTER}
Originally created by=--=[DOM:queryValue:#originallyCreatedBy:1:replace:originally created by\: ([^(]+).*:$1]{ENTER}
Maintainer Name=--=[Source.Maintainer Name]{ENTER}
Maintainer ID=--=[Source.Maintainer ID]{ENTER}
Date Added=--=[Source.Date Added]{ENTER}
{ENTER}
Family information{ENTER}
Parents=--=[Parents]{ENTER}
Siblings=--=[Siblings]{ENTER}
Spouses=--=[Spouses]{ENTER}
{ENTER}
Main Photo information{ENTER}
Image URL=--=[Image URL]{ENTER}
Photographer Name=--=[Source.Photographer Name]{ENTER}
Photographer ID=--=[Source.Photographer ID]{ENTER}
{ENTER}
{ENTER}
Source.Citation=----={ENTER}[Source.Citation]{ENTER}
=----={ENTER}
{ENTER}
===========================================DIV50=={ENTER}
....................END
```
