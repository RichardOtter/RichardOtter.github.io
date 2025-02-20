DNA Match input

===========================================DIV50==
DNA section of Person profile - or DnaTable entry

===========================================DIV50==
not a shared fact,
not an association
but a new relationship saved in the DNATable

See detailed info on DnaTable entry below.

Be sure to check DNA provider is correct when starting to do data entry.
During Data entry, could create the DB person then, or wait.

===========================================DIV50==
Person entry

===========================================DIV50==
Each matched person shall be in the database
Name
If married / birth names inferred, add them

Birth
Add birth date when the match info says age or place

MyHeritage birth year est for 2025

20's		ca 2010
30's		ca 1990
40's		ca 1980
50's		ca 1970
60's		ca 1960
70's		ca 1950
80's		ca 1940
90's & above	bef 1935

For MyHeritage, there is often a location given. Use as [probably] birth place
Deutschland [probably]
==United States [probably]
etc

===========================================DIV50==
DNA Fact

===========================================DIV50==
When entering people in DB that have a DNA connection
add a DNA fact with place set to match provider
=DNA Ancestry.com
=DNA-23andMe.com
etc

In some cases, enter their relatives as well if there is promise of a connection.
The match's relatives do not get a DNA fact.

Description is used as sort of a status of where analysis stands.
match	confirmed against an entry in DNATable
tree	looked at match's tree online and extracted all data. Notes in DNA note.
no tree		their online match entry says they have not created a tree. Nothing to analyze except match group.

===========================================DIV50==
DnaTable entry

===========================================DIV50==
Each entry has

DNA Provider
Person Shared cM
Shared %
Larger Seg
Shared Segs
Date
Rel (Tree)
Rel (DNA)
NOTE

Date of test is actually used as Date entry last updated, specifically last online access of data.

In all cases, don't use info from the list of matches, instead click on the item in the list to open the details page for that match.


Ancestry:
Notice that the number of shared segments is indicated in the main list, but not 
when the listing is opened. Be sure to follows rules bleow for Nte format.
No % shared. Leve it blank.

23andme:
gives only % shared. To determine cM, use the tool at-
https://dnapainter.com/tools/sharedcmv4
it might just just a multiplier of  about 74
TODO investigate why.

===========================================DIV50==
DNA Note Format

===========================================DIV50==
The Note is free form

Define it for each match provider as shown below-

===========================================DIV50==
MyHeritage:
DNA Note Sample Entry

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
===DIV50==
_CORRESPONDENCE
---DIV30--
===DIV50==


How to:

copy/paster the URL
Edit the URL to remove extraneous stuff. Make it end with a "/"

then copy all info from match page
Insert blank lines as shown in sample.
edit out "contact", add a line between the main name sections.

===========================================DIV50==
23andMe

DNA Note Sample Entry

https://you.23andme.com/profile/fcdbdb38ec83ccb4/

Richard J Otter
Leonard Schwab

Active
Over a month ago
Location
New Hampshire, United States

About
My goal is to build out my family tree. Currently I know all my 1st cousins, most 2nd cousins, some 3rd cousins, and a few 4th cousins. Let's work together to build our trees.

Your genetic relationship
Relationship
2nd Cousin, Once Removed 

Shared DNA
1.26%

Family info
Names= Schwab, Sieghartner, Scheuerer, Lips, Siegmann
Baumann, Graf, Grinsfelder, Loeffelmann., Kraus, Hahn, Schwarzenberg, Schmitt (2x), Reuss, Rückel (2x), Friedrich, Sennfelder, Dittmayer

===DIV50==
Shared DNA
DNA-Painter-tool( 1.26% ) => 94 cM

===DIV50==
_DETAILS
===DIV50==
_NOTES

No new info. Firmly established.
His tree is checked routinely.

===DIV50==
_CORRESPONDENCE
===DIV50==


How to:
URL, use as is.
Add name of matcher right above the person matched.

Copy of text from page in plain text
name, active lines, invite sent, about (if present), and the match info.

Family info is from the bottom of match window

The section Shred DNA explanation is firmly defined.
After can come either _NOTES, _DETAILS or _CORRESPONDENCE. Not set yet.

IN _CORRESPONDENCE section
use ---DIV30-- to separate messages



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


23andMe gives only % shared
to get cm, use the tool at-
https://dnapainter.com/tools/sharedcmv4
it might just just a multiplier of about 74

so 1% match
1.0 * ~74 = 74 cM
2.0 & ~74 = 149 cM
0.5 * ~74 => 37 cM

In the note, explain where cM number came from
either 
1.0% * 74 = 74 cM
or
DNA-Painter-tool( 1.26% ) => 94 cM

TODO  Since detailed DNA information was made unavailable
Try to get the detailed info from the csv previously downloaded.


===========================================DIV50==
Ancestry

DNA Note Sample Entry

https://www.ancestry.com/discoveryui-matches/compare/3472852c-4089-4840-84a0-682ac8631a96/with/d6576e06-de8f-45c2-b887-9ebd30825ebc

You and Jessica Kelly
2nd cousin 1x removed | Maternal side
1% shared DNA: 104 cM across 5 segments

Predicted: 2nd cousin 2x removed or half 2nd cousin 1x removed

Shared DNA: 104 cM across 5 segments
Unweighted shared DNA: 104 cM
Longest segment 34 cM

Jessica Kelly hasn't built a searchable tree.

===DIV50==
_NOTES

No tree
Established only by the last name and prediced relationship
DNA gives what she actually is 2nd cousin 1x removed.

===DIV50==
_CORRESPONDENCE
---DIV30--
===DIV50==


How to:

Sharing details are from inner panel. Copy the lines starting with- Predicted to Longest.

Then include online tree info
If linked tree, add a new line before the # of people
If unkinked tree, add "# people" from the largest one listed.
If no tree, copy that notice line as is.

TODO  May want to do a search and replace for "You and " => "Richard J Otter \n"

===========================================DIV50==
DNA Match entry

===========================================DIV50==
Labe1 1 is kind of useless right now. Just the database name of the person matching
Label 2 is important- it it the name used at the matching service of the second peson
Person 2 is the local database person assigned to the match.
if no other info, then it is Label 2. Usually, try to get a name, and also birth and married name from looking at their online tress.

===========================================DIV50==
TEMPLATE to copy and paster-


===========================================DIV50==
_DETAILS
===========================================DIV50==
_NOTES
===========================================DIV50==
_CORRESPONDENCE
-----------------------DIV30--
===========================================DIV50==
