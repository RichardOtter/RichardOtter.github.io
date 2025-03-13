# DNA Match data input

Last update: 2025-03-12

[Home](https://richardotter.github.io)

## Overview

New in RootsMagic 10- the DNA Table\
not a shared fact,\
not an association\
but a new relationship saved in the DNATable

The DNA Table is accessed in the person edit window and displayed by
clicking the "DNA" icon in the window's left side bar.

My practice for entering match data is to-

1. Create an entry in the DNA Table. For the "Person 2" field, select an
existing "pseudo person". All other fields use the match data from
the DNA service website.
2. Examine the data available- closeness of match, matchee's online tree, shared
matches list etc
3. Reassign the pseudo-person assigned in step 1\
   3.1 with either another, more specific pseudo-person\
   3.2  or to a newly created parson who represents the matchee.
4. For newly created Persons,\
  4.1 add a DNA custom fact to the match person with place representing the
  DNA match service name\
  4.2 add a weblink to the person pointing to the match page (name=AncD-[test-taker-name]).\
  4.3 add a weblink to the person pointing to the matchee in the matchee's
  online tree (name=ANC)\
  4.4 add a weblink to the person pointing to the person in my online tree\
  4.5 add as many facts to the person as the evidence allows.\
5 Go back to step 2. Reexamine the match data and repeat.

Before starting entering DNA matches into the DNA table, create at least
the pseudo person named '[lev 0=initial] [_DNA]'.
See the section on Person entry, below.

## DNA Match entry

Ignore the slider controls. They do not help or show much.

Each entry has the following fields:

### DNA Provider

Enter the name of the service that did the DNA matching with other DNA test takers.

Be sure to confirm that the DNA provider entered is correct when starting to
do data entry.

Open your service's web page listing your DNA matches.
If your account manages more than oe test, be sure the correct one is selected.

For the services Ancestry, MyHeritage and 23andMe, don't use info
from the list of matches, instead click on the
match item in the list to open the details page for that match.

### Person 1

This field will be auto filled to be the person whose edit windows you
are working in. It will be the person whose DNA match results you manage 
at the DNA matching service. It will likely be you.

### Label 1

This should be Person 1's user name at the DNA provider site used above.

Labe1 1 is kind of useless right now. Just the database name of the person matching
Label 2 is important- it it the name used at the matching service of the second person
Person 2 is the local database person assigned to the match.
if no other info, then it is Label 2. Usually, try to get a name, and
also birth and married name from looking at their online tress.

### Person 2

This is the person matched to Person 1.
Clicking this field displays the RM Explorer window which lets the user
find an existing person in the database, or allows entry of a new person.

RM forces the user to enter someone right away. This is quite inconvenient.
When I create a new person in the DB, I like to spend a bit of time to add correct
facts. In this flow, one can see the person add window, but the edit window
does not appear and is not accessible while the Add DNA match modal window is open.

1. Be sure you have a pseudo-person in the database named '[lev 0=initial] [_DNA]'.
2. Use the Explorer window to select this user.
This will be updated later. See Overview section, above.

### Label 2

Enter the exact user name of the person matched at the matching service.

### Shared (cM)

Enter the number of shared centiMorgans provided.

23andMe:
Provides only the  per cent shared DNA number.
To determine cM, use the tool at- <https://dnapainter.com/tools/sharedcmv4>
(it might just just a multiplier of about 74)
0.5 \* ~74 => 37 cM
1.0 \* ~74 = 74 cM
2.0 & ~74 = 149 cM

TODO investigate why. May have to do with absolute numbers of shared
nucleotides vs. the rate of recombination expressed by the # of Morgan.

### Shared %

Ancestry:
If <1%,  leave it blank.

### Largest Seg (cM)

Enter the number provided.

### Shared Segments

Enter the number provided.

Ancestry:
Notice that the number of shared segments is indicated in the main list, but not
when the listing is opened. In the match details window, one needs to click the link.

### Test Date

Test Date field is actually used as "Date entry last updated", specifically last
online access of data.

### DNA Note

Free  form text. We want to capture all of the data from the DNA match website.

Define the format for each match provider as shown below-

#### MyHeritage

##### DNA Note Sample Entry

```text
https://www.myheritage.com/dna/match/D-ED9X522N-E728-LTW1-D9E2-D9E258U227X9-D-7782E9C1-22AQ-2P59-2928-292827P75EAA/270653051/

Rosa Johanna Maier
Mother
Age: 90 or above
Appears in your tree

Richard J Otter
This is you
From: USA

Probable relationship
Son
DNA Match quality?
49.6% (3,518.5‎ cM)
Shared DNA
22
Shared segments
284.3‎ cM
Largest segment

_NOTES
===========================================DIV50==
_CORRESPONDENCE
-----------------------DIV30--
===========================================DIV50==
```

##### How to

copy/paster the URL
Edit the URL to remove extraneous stuff. Make it end with a "/"

then copy all info from match page
Insert blank lines as shown in sample.
edit out "contact", add a line between the main name sections.

#### Ancestry

##### DNA Note Sample Entry

```text
URL=----=
https://www.ancestry.com/discoveryui-matches/compare/855339eb-af29-43ec-bb83-bce76aff38fa/with/a583d4cb-19ab-4ec5-b438-e1a8696c1a9a
=----=
Accessed=--=9 March 2025

Page Title=--=AncestryDNA® Matches Compare

Test name=--=Roman Otter
Match name=--=James Heeley

Shared DNA (cM)=--=20 cM
Longest shared segment=--=22 cM
# shared segments=--=1
Unweighted shared DNA (cM)=--=22 cM

Estimated Relationship=--=4th cousin or half 3rd cousin 1x removed
Match on Maternal/Paternal =Maternal side

Ancestry group memberships=--=

User entered match note=----=
=----=

Has Linked Tree with 804 people.

ORA template v2025-03-09-1

===========================================DIV50==
_NOTES

Tree:
Shared matches: 
Placement:


===========================================DIV50==
_CORRESPONDENCE
-----------------------DIV30--
-----------------------DIV30--
===========================================DIV50==
```

##### How to

This is the output of my ORA autotype template.

Sharing details are from inner panel.

Include online tree info:\
If linked tree, add a newline before the # of people\
If unlinked tree, add on a new line, "# people" from the largest one listed.\
If no tree, copy that notice line as is.

#### 23andMe

##### DNA Note Sample Entry

```text
https://you.23andme.com/profile/fcdbdb38ec83ccb4/

Richard J Otter
Leonard Schwab

Active
Over a month ago
Location
New Hampshire, United States

About
My goal is to build out my family tree. Currently I know all my 1st
cousins, most 2nd cousins, some 3rd cousins, and a few 4th cousins.
Let's work together to build our trees.

Your genetic relationship
Relationship
2nd Cousin, Once Removed 

Shared DNA
1.26%

Family info
Names= Schwab, Sieghartner, Scheuerer, Lips, Siegmann
Baumann, Graf, Grinsfelder, Loeffelmann., Kraus, Hahn, Schwarzenberg, Schmitt (2x), Reuss, Rückel (2x), Friedrich, Sennfelder, Dittmayer

===========================================DIV50==
_DETAILS

DNA-Painter-tool( 1.26% ) => 94 cM

===========================================DIV50==
_NOTES

No new info. Firmly established.
His tree is checked routinely.

===========================================DIV50==
_CORRESPONDENCE
-----------------------DIV30--
===========================================DIV50==
```

##### How to

URL, use as is.
Add name of matcher right above the person matched.
That way, the note is self documenting.

Copy of text from page in plain text
name, active lines, invite sent, about (if present), and the match info.

Family info is from the bottom of match window

The section Shred DNA explanation is firmly defined.
After can come either _NOTES, _DETAILS or _CORRESPONDENCE. Not set yet.

IN _CORRESPONDENCE section
use a divider:
-----------------------DIV30--
to separate messages

In the _DETAILS note section, explain where cM number came from
either
1.0% * 74 => 74 cM
or
DNA-Painter-tool( 1.26% ) => 94 cM

TODO  Since detailed DNA information was made unavailable at website
Try to get the detailed info from the csv previously downloaded.

## Person entry

Ideally, each matched person is a relative and should ultimately be entered into
the database and connected to the main tree.
Some matches provide much information in assisting you with the identification
and placement in the tree. Others have little potential for identification.

Instead of entering all matches directly in the database, all are initially
connected to a "pseudo-person" and then, after analysis, connected to a real
Person in the database that would hopefully be connected to the tree.

There is a judgement call as to whether to leave the match connected to a pseudo-person
or whether to enter the matchee's name in the database as a real Person.

If the matchee has no online tree and has not provided a real name, there is not
much hope to identify that parson and place him in the tree.
Leave the match attached to a pseudo-person.
Could message the person if it looks promising.

I have created several "pseudo-persons" in my database.
The only facts attached to them are the Primary name and a DNA custom fact.
No other information is appropriate as each of these represents multiple
DNA matched people.

My pseudo-people are:
[lev 0=initial] [_DNA]\
[lev 1=no info] [_DNA]\
[lev 2=examined] [_DNA]\
[lev 3=priority] [_DNA]\

[lev 0=initial] is the given name, [_DNA] is the surname.
I enclose the names in square brackets because that is my convention indicating
that the enclosed is not a real person name.

When the match is first entered in the DNA table, Person 2 is assigned to
'[lev 0=initial] [_DNA]'.
After the first analysis of the data associated with a particular match,
the Person 2 for that match is re-assigned to either one of the other
pseudo-people, or to an existing person in the database, or
to a newly created person.

If a DNA match is considered promising and a real person is entered into
the database for the match, enter this data:

Name\
If married / birth names inferred from the matchee's provided data,
perhaps from their attached tree, add them as alternate names and indicate
name type.

Birth\
Add birth date when the match data gives age or place the matchee is from.

The MyHeritage service match data will often list an approximate age.
Use these birth year estimates (as of 2025):

|  age         | birth    |
| ------------ | -------- |
| 20's         | ca 2010  |
| 30's         | ca 1990  |
| 40's         | ca 1980  |
| 50's         | ca 1970  |
| 60's         | ca 1960  |
| 70's         | ca 1950  |
| 80's         | ca 1940  |
| 90's & above | bef 1935 |

Many entries include a location. Since it's not known to be birth place,
use the [probably] form of the country.
e.g.\
Deutschland [probably]\
United States [probably]\
etc\

### DNA Fact

Preparation:\

* Create a custom fact that displays place and description.
Uncheck the boxes to exclude it from most reports.

* Enter into the Places list, a "place" for each DNA match provider
you expect to use. e.g.\
=DNA Ancestry.com\
=DNA-23andMe.com\
etc

When entering people in DB that have a DNA match,
add a DNA fact with the place set to match provider.

In some cases, enter their relatives as well if there is promise of a connection.
The match's relatives do not get a DNA fact.

Description is used as sort of a flag for where analysis stands. TODO

|         |                                                                                                    |
| ------- | -------------------------------------------------------------------------------------------------- |
| match   | Confirmed against an entry in DNA table                                                            |
| tree    | Looked at match's tree online and extracted all data. Notes in DNA note.                           |
| no tree | their online match entry says they have not created a tree. Nothing to analyze except match group. |
| _CLOSE  | Close relative. No further work on this match needed                                               |

## ORA AutoType templates for entering DNA Matches

### Ancestry.com matches

1  First create a user named "[lev 0=initial] [_DNA]".\
All DNA matches will initially be automatically assigned to this person. \
Label 2 will be correct so it can be used to later create
the correct people in the database.
At that time, the person entry can be edited to conform to standards.

2  Open the DNA entry match window and click the PLUS symbol
to start crating a new entry.

3  Open the web browser to the match to be entered.
NOTE whether the person has an unlinked tree.
Note the number of people in either the linked tree or the nax
number of people in the set of unlinked trees.

4  click on the link to open the pop up, then click on the page to close the pop-up

5  click autotype 1

6  Follow the prompts.

If the match person has a linked tree, the rest is automatic.

If not, you are prompted for the number f people in the attached unlinked tree.

Enter number or people in the unlinked tree, if it exists,
enter 0 if there is no tree attached or it is private.

Analysis-
Create the Persons-
given name  surname
"[lev 1=no info] [_DNA]"
"[lev 2=examined] [_DNA]"
"[lev 3=priority] [_DNA]"

These will act as groups.
The DNA match Person 2 was initially assigned to
person "[lev 0=initial] [_DNA]".
If upon further examination of the data in the match web page, we
find that there is no path forward to identify the real name of
the match person, change the assigned person from "[lev 0=initial] [_DNA]"
to "[lev 1=no info] [_DNA]".
If when examining the match data, you find some information that is encouraging
in terms of determining the real name and relationship, the set the match's
Person 2 field to "[lev 3=priority] [_DNA]"
If yo're not sure what to think, set the field to "[lev 2=examined] [_DNA]"/
That just means that you've at least looked at the data.

If can add the match person to the tree, or he is already there, add the person to
the database and set Person 2 field to that person.

#### Template Version 2025-03-09-1

Found in export file "Settings-2025-03-09 13-44-56.ora-settings"

Minimumm ORA version: "OraExtension v1.91"

POSITION 1

```text
Reminder:
NEW entry
Prompt for number_if_people)in_tree:
Enter number or people in either the linked or unlinked tree.

....................BEGIN
[=:template_ver:2025-03-09-1]
#
# Cursor starts in the Person 2
#
[=:number_of_people_in_linked_tree:[DOM:queryInner:#linkedTreePersonCountDiv::split:People:1]]
<[?:Has Linked Tree!=Yes][=:number_of_people_in_unlinked_tree]>

{PERCHAR=10}
{FAST}
{10}{RIGHT}{30}
dna,lev 0 {2000}
{ALT+O}{1000}
{10}{TAB}[Match Name]
{10}{TAB}[centiMorgans]
{10}{TAB}
{10}{TAB}[Longest segment:split:cM:1]
{10}{TAB}[Segments]
{10}{TAB}[Page.Access Date]
{10}{TAB}
{10}{RIGHT}
{10}
URL=----={ENTER}
[URL]{ENTER}
=----={ENTER}
Accessed=--=[Page.Access Date]{ENTER}
{ENTER}
Page Title=--=[Page.Title]{ENTER}
{ENTER}
Test name=--=<[?:Test Name=You]Richard J Otter><[?:Test Name!=You][Test Name]>{ENTER}
Match name=--=[Match Name]{ENTER}
{ENTER}
Shared DNA (cM)=--=[centiMorgans] cM{ENTER}
Longest shared segment=--=[Longest segment]{ENTER}
\# shared segments=--=[Segments]{ENTER}
Unweighted shared DNA (cM)=--=[Unweighted shared DNA]{ENTER}
{ENTER}
Estimated Relationship=--=[Estimated Relationship]{ENTER}
Match on Maternal/Paternal =[Side]{ENTER}
{ENTER}
Ancestry group memberships=--=[Groups]{ENTER}
{ENTER}
User entered match note=----={ENTER}
<[Match Note]{ENTER}>
=----={ENTER}
{ENTER}
<[?:Has Linked Tree=Yes]Has Linked Tree with [number_of_people_in_linked_tree] people.>
<[?:Has Linked Tree!=Yes][?:number_of_people_in_unlinked_tree!=0]Has at least one unlinked tree with [number_of_people_in_unlinked_tree] people.>
<[?:Has Linked Tree!=Yes][?:number_of_people_in_unlinked_tree=0]Does not have a tree on Ancestry.>{ENTER}{ENTER}
ORA template v[template_ver]{ENTER}
{ENTER}
===========================================DIV50=={ENTER}
_NOTES{ENTER}
{ENTER}
Tree: {ENTER}
Shared matches: {ENTER}
Placement:{ENTER}
{ENTER}
===========================================DIV50=={ENTER}
_CORRESPONDENCE{ENTER}
-----------------------DIV30--{ENTER}
-----------------------DIV30--{ENTER}
===========================================DIV50=={ENTER}
{ENTER}
....................END
```

POSITION 2
```text
Reminder:
UPDATE entry
Prompt for number_if_people)in_tree:
Enter number or people in either the linked or unlinked tree.

....................BEGIN
[=:template_ver:2025-03-09-1]
# 
# Cursor starts in Label 2. 
# The script does not change Person 2 or Label 2
#
[=:number_of_people_in_linked_tree:[DOM:queryInner:#linkedTreePersonCountDiv::split:People:1]]
<[?:Has Linked Tree!=Yes][=:number_of_people_in_unlinked_tree]>

{PERCHAR=10}
{FAST}
{10}{TAB}[centiMorgans]
{10}{TAB}[Shared DNA]
{10}{TAB}[longest]
{10}{TAB}[Segments]
{10}{TAB}[Page.Access Date]
{10}{TAB}
{10}{RIGHT}
{500}
{ENTER}
{ENTER}
{ENTER}
{ENTER}
{ENTER}
{ENTER}
{UP}
{UP}
{UP}
{UP}
{UP}
{UP}
URL=----={ENTER}
[URL]{ENTER}
=----={ENTER}
Accessed=--=[Page.Access Date]{ENTER}
{ENTER}
Page Title=--=[Page.Title]{ENTER}
{ENTER}
Test name=--=<[?:Test Name=You]Richard J Otter><[?:Test Name!=You][Test Name]>{ENTER}
Match name=--=[Match Name]{ENTER}
{ENTER}
Shared DNA (cM)=--=[centiMorgans] cM{ENTER}
Longest shared segment=--=[Longest segment]{ENTER}
\# shared segments=--=[Segments]{ENTER}
Unweighted shared DNA (cM)=--=[Unweighted shared DNA]{ENTER}
{ENTER}
Estimated Relationship=--=[Estimated Relationship]{ENTER}
Match on Maternal/Paternal =[Side]{ENTER}
{ENTER}
Ancestry group memberships=--=[Groups]{ENTER}
{ENTER}
User entered match note=----={ENTER}
<[Match Note]{ENTER}>
=----={ENTER}
{ENTER}
<[?:Has Linked Tree=Yes]Has Linked Tree with [number_of_people_in_linked_tree] people.>
<[?:Has Linked Tree!=Yes][?:number_of_people_in_unlinked_tree!=0]Has at least one unlinked tree with [number_of_people_in_unlinked_tree] people.>
<[?:Has Linked Tree!=Yes][?:number_of_people_in_unlinked_tree=0]Does not have a tree on Ancestry.>{ENTER}{ENTER}
ORA template v[template_ver]{ENTER}
{ENTER}
===========================================DIV50=={ENTER}
_NOTES{ENTER}
{ENTER}
Tree: {ENTER}
Shared matches: {ENTER}
Placement:{ENTER}
{ENTER}
===========================================DIV50=={ENTER}
_CORRESPONDENCE{ENTER}
-----------------------DIV30--{ENTER}
-----------------------DIV30--{ENTER}
===========================================DIV50=={ENTER}
{ENTER}
....................END
```

```
TODO
add info from the downloaded DNA Match csv file.
detailed info header-
"Display Name","Surname","Chromosome Number",
"Chromosome Start Point","Chromosome End Point",
"Genetic Distance","# SNPs","Full IBD",
"Link to Profile Page","Sex","Birth Year",
"Set Relationship","Predicted Relationship","Relative Range",
"Percent DNA Shared","# Segments Shared",
"Maternal Side","Paternal Side","Maternal Haplogroup","Paternal Haplogroup",
"Family Surnames","Family Locations",
"Maternal Grandmother Birth Country","Maternal Grandfather Birth Country",
"Paternal Grandmother Birth Country","Paternal Grandfather Birth Country",
"Notes","Sharing Status","Showing Ancestry Results","Family Tree URL"
```