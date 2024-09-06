---
title: Find a Grave Source Template
---
[Home](https://richardotter.github.io)



# Find a Grave Source Template

Download link for rmst file =
[Find a Grave.mst](https://RichardOtter.github.io/SourceTemplate/ST-Find%20a%20Grave.rmst) 

## Template details

Source Template= _Finad-a-Grave
Field              Type       Display
TitleDatabase      Text       Database name
DateDatabase       Date       Last DB info update

Name               Name       Person name
DateBirth          Date       Person's birth date
CD                 Text       Citation Detail
PlaceBurial        Place      Place of Burial
PlaceCemetery      Text       Cemetery name
EntryNumber        Text       Memorial number
Transcription      Text       Transcription
DateCitation       Date       Date citation updated
SrcCitation        Text       FG Citation

Citation field description
Name
Not necessarily exactly as in FG database
Use the ORA -Name field. This takes the birth name in italics and encloses it in parentheses.
Remove name prefixes. 

DateBirth 
Not necessarily from record. Only for identification.

CD
Currently, use only for
	Gravestone transcription  if Transction = D
	OBITUARY

PlaceBurial
PlaceCemetery
	direct copy from FG

EntryNumber
	Memorial number

Transcription
	N= No image available
	A= Grave marker image available, but transcription not yet done,
	D= Transcription done and is in RM_Research_Note.

DateCitation
	Date that this citation last updated. (Judgment call when to change this)

SrcCitation
	direct copy of the citation provided by FG

Only one source created from this template= Find_a_Grave_db


### rmst analysis


This is the relevant part of the rmst file. I removed most end tags and empty tags.

		<Name>_Find-a-Grave
		<Description/>
		<Footnote>[SrcCitation]&lt;;  [CD]&gt;
		<ShortFootnote>[TitleDatabase]; Entry for: [Name]; Memorial ID: [EntryNumber]&lt;;  [CD]&gt;
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
```
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
