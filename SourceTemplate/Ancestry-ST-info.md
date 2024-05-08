---
title: Ancestry Source Template
---
[Home](https://richardotter.github.io)

# Ancestry.com

Download link for rmst file =\
<a href="https://RichardOtter.github.io/SourceTemplate/ST-Ancestry-single%20and%20double.rmst" download="ST-Ancestry-single and double.rmst"> Ancestry (data collections, single and double subject) </a>

For Ancestry, the dilemma to be solved was that many of the Source Citations provided by Ancestry for most collections were not good enough to use as provided.

Of course, one could simply reference the Ancestry source web page, but that wouldn't provide any information on reliability of the source and relies on an Ancestry subscription for access.

The goal for the Ancestry template was to capture all of the information that Ancestry provided and later figure out what the footnote sentences should be. I think that I've now done that. At least for many cases.

In order to get our terminology straight, let use an example from Ancestry, the collection named "New York, New York, U.S., Birth Index, 1910-1965". I will use the word "Source" to refer to the entire Ancestry collection of that name. RM sometimes uses the term Master Source. It's the same thing. The source's main web page is at:\
[New York, New York, U.S., Birth Index, 1910-1965](https://www.ancestry.com/search/collections/61457/)

The Ancestry web page where a particular person, or household, is listed in that source is called a Citation. RM sometimes uses the term Source Detail. It's the same thing. A example citation to the NY Birth index Source is:\
[Birth index entry for Walter Otter](https://www.ancestry.com/discoveryui-content/view/3335191:61457)

This template creates a "lumped" source, meaning that in RM, only one source record is created, but many RM citations are created referencing it. A "split" source would put all of the information in the source record. A reference to each person in the collection would necessitate creation of a separate source record for each person. Each source would probably have only one citation.

Information about the Source is taken from the source's main page, half way down the page, below the search fields, starting with "Source Information", and continuing with the section "About New York, New York, U.S., Birth Index, 1910-1965".

Note the subsection in the About section labeled "Original data:". We will use that later.

I decided to create two template for Ancestry collections- one for collections that deal with a single person or household such as birth, death, census etc and another that deals with two equal people such as marriage, divorce, etc.

I'll describe the Single person template first. "_Ancestry Database-Single -L" (The -L indicates that this is a 'lumped' source, as opposed to a split source.) "_Ancestry Database-Double -L" is described later, below.

## _Ancestry-Single -L

###  Source Template Data
These contain the template name, an optional description , and the sentences to be used to form the footnotes. etc.

&lt;Name>_Ancestry-Single -L\
&lt;Description>\
&lt;Footnote>[SrcInfo] Entry for: [Name]&lt;, born: [BirthDate]&gt;&lt;, event date: [EventDate]&gt;&lt;, accessed: [DateCitation].&gt;&lt; Citing: [OrigData]&gt;&lt;  [CD]&gt;\
&lt;ShortFootnote>[Title], entry for: [Name], born: [BirthDate]&lt;, event: [EventDate].&gt;&lt;  [CD]&gt;\
&lt;Bibliography>[SrcInfo]

###  Source fields
For Source fields, use the example at: <a href="https://www.ancestry.com/search/collections/61457/">New York, New York, U.S., Birth Index, 1910-1965</a>

#### &lt;Field>
&lt;Type>Text\
&lt;Name>Title\
&lt;Display>Ancestry database name -short\
&lt;Detail>false &#160;&#160;&#160; [This is a Source field. It describes the entire collection.]

Example Title = New York, New York, U.S., Birth Index, 1910-1965

Find this data in Source Info section of the collection main page whose URL is above.
The first sentence is the Ancestry full name-
Ancestry.com. New York, New York, U.S., Birth Index, 1910-1965 [database on-line]. Lehi, UT, USA: Ancestry.com Operations, Inc., 2017.
This field uses a shortened version to improve readability:
New York, New York, U.S., Birth Index, 1910-1965

#### &lt;Field>
&lt;Type>Date\
&lt;Name>Date\
&lt;Display>Last DB info update\
&lt;Detail>false &#160;&#160;&#160; [This is a Source field. It describes the entire collection.]

Example Date = 2 Jan 2024

This field contains the date on which this source record was entered, or last updated in RM. Use today's date.

#### &lt;Field>
&lt;Type>Text\
&lt;Name>SrcInfo\
&lt;Display>Ancestry Source Info\
&lt;Detail>false &#160;&#160;&#160; [This is a Source field. It describes the entire collection.]

Example SrcInfo = Ancestry.com. New York, New York, U.S., Birth Index, 1910-1965 [database on-line]. Lehi, UT, USA: Ancestry.com Operations, Inc., 2017.

Use the Ancestry supplied name in full.
Looks at Source Info section of the collection page whose URL is above.
The first sentence is the Ancestry full name-
Ancestry.com. New York, New York, U.S., Birth Index, 1910-1965 [database on-line]. Lehi, UT, USA: Ancestry.com Operations, Inc., 2017.

#### &lt;Field>
&lt;Type>Text\
&lt;Name>OrigData\
&lt;Display>Original Data\
&lt;Hint>not applicable to all Ancestry collections\
&lt;Detail>false &#160;&#160;&#160; [This is a Source field. It describes the entire collection.]

Example OrigData = New York City Department of Health, courtesy of www.vitalsearch-worldwide.com. Digital Images.

Use the Ancestry supplied info in the  Source Info section of the collection page whose URL is above.
The second sentence is the Ancestry original data info-
New York City Department of Health, courtesy of www.vitalsearch-worldwide.com. Digital Images.
Note, not all Ancestry collections have this information listed and some will have far too much text to use. 

#### &lt;Field>
&lt;Type>Text\
&lt;Name>dbID\
&lt;Display>Ancestry Database ID\
&lt;Hint>Found in URL\
&lt;Detail>false &#160;&#160;&#160; [This is a Source field. It describes the entire collection.]

Example dbID = 61457

The is the Ancestry database number. It can be found in the URL that points to the collection main page.

#### Standard source data
Enter the URL of the Ancestry source as a WebTag for the source:

Example WebTag = Ancestry  /  https://www.ancestry.com/search/collections/61457/

Enter the full text from the Source main page into the Master source "Source Text" field. (I am still deciding on whether this is a good idea. The problem is that is hows in the footnote window and *may* slow down operation for very long text)

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

### Citation fields

For citation fields, use the example found at <a href="https://www.ancestry.com/discoveryui-content/view/3335191:61457"> Birth index entry for Walter Otter</a>

#### &lt;Field>

&lt;Type>Name\
&lt;Name>Name\
&lt;Display>Person name\
&lt;Detail>true &#160;&#160;&#160; [This is a Citation field.]

Example Name = Walter Otter

This template is for Ancestry collections that have a single person as their focus. This is where that name goes. Given and then Surname. Note that the field type is Name, so name sentence transforms are allowed.

#### &lt;Field>

&lt;Type>Date\
&lt;Name>BirthDate\
&lt;Display>Person's birth date\
&lt;Hint>Not necessarily from record. Only for identification.\
&lt;Detail>true &#160;&#160;&#160; [This is a Citation field.]

Example BirthDate = 29 Dec 1935

Birth date of the focus person. All normal date modifiers allowed.

#### &lt;Field>

&lt;Type>Date\
&lt;Name>EventDate\
&lt;Display>Event date\
&lt;Detail>true &#160;&#160;&#160; [This is a Citation field.]

Example EventDate = 29 Dec 1935

Date of event from the source. May be same as birth date for birth record. Sometimes blank.

#### &lt;Field>

&lt;Type>Text\
&lt;Name>CD\
&lt;Display>Citation Detail\
&lt;Detail>true &#160;&#160;&#160; [This is a Citation field.]

Example CD = &lt;blank>

Some other information about this citation goes into this Citation Detail field. May be used if there are multiple citations to the same record in a source, or to describe the citation in some way. Usually left blank.

#### &lt;Field>

&lt;Type>Date\
&lt;Name>DateCitation\
&lt;Display>Date citation updated\
&lt;Detail>true &#160;&#160;&#160; [This is a Citation field.]

Example DateCitation = 2 Jan 2024

This field contains the date on which this citation record was entered, or last updated in RM. Use today's date.

#### &lt;Field>

&lt;Type>Text\
&lt;Name>SrcCitation\
&lt;Display>Ancestry Source Citation\
&lt;Detail>true &#160;&#160;&#160; [This is a Citation field.]

Example SrcCitation = &lt;blank>

This is the full contents of the Ancestry provided Source Citation. Not all collections have this info. It is often not very helpful, other times it is crucial.

To show what data this is referring to, here is a different example that actually has the Ancestry Source Citation data- <a href="https://www.ancestry.com/discoveryui-content/view/291511995:62308"> 1850 census entry for Walter Otter</a>

Look in the Source tab in the center of the page, (next to the Detail tab). The first paragraph is labeled "Source Citation". If it exists for the citation being entered, that's what goes in into the SrcCitation field. 

Example SrcCitation = National Archives at Washington, DC; Washington, D.C.; Seventeenth Census of the United States, 1950; Year: 1950; Census Place: New York, Kings, New York; Roll: 2327; Page: 5; Enumeration District: 24-3136

#### Standard citation data

* Enter the URL of the Ancestry citation as a WebTag for the citation:
Example Citation WebTag = https://www.ancestry.com/discoveryui-content/view/3335191:61457

* Attach source image to Media for the Citation, if an image is available.

* Enter the full text of the transcribed record in the Citation "Research Note" field

Example Research Note =

Name&#160;&#160;&#160;Walter Otter\
Birth Date&#160;&#160;&#160;29 Dec 1935\
Birth Place&#160;&#160;&#160;Brooklyn, New York City, New York, USA\


## _Ancestry-Double -L

###  Source Template Data

These contain the template name, an optional description , and the sentences to be used to form the footnotes. etc.

&lt;Name>_Ancestry-Double -L\
&lt;Description>\
&lt;Footnote>[SrcInfo] Entry for: [Name], event date: [EventDate], accessed: [DateCitation].&lt; Citing: [OrigData]&gt;&lt;-  [CD]&gt;\
&lt;ShortFootnote>[Title], entry for: [Name], event date: [EventDate].&lt;-  [CD]&gt;\
&lt;Bibliography>[SrcInfo]


###  Source fields

All the same as above for the single template.

### Citation fields

All the same as above \
 EXCEPT\
the Name field is of type Text and the hint is different.\
and there is no BirthDate field. The reason is that instead of a nase for a particular person, a set of two namaes for the couple is entered. There is no birthdate for the couple.

#### &lt;Field>

&lt;Type>Text\
&lt;Name>Name\
&lt;Display>Couple surnames\
&lt;Detail>true &#160;&#160;&#160; [This is a Citation field.]

Example Name = Weinberg & Mead

This template is for Ancestry collections that have a two persons as their focus.\
I use the format [male surname] & [female surname]

Note that the field type is Text, since name sentence transforms wouldn't make sense.
