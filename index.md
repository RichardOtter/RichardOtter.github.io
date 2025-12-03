# My Bare-Minimum Site

Last Update: 2025-12-03

## What's New?

* Data Entry DNA match: added ORA templates for MyHeritage
* Added Genealogical Resources page
* minor update to page showing FG ORA autotype templates

This site is a work in progress.

## General Topics

### [Genealogical Online Resources](Genealogical%20Resources.html)

A simple list of the sites I use.

### [Genealogy Standard Forms](https://github.com/RichardOtter/Standard-forms-for-genealogy)<a id="forms"></a>

A slowly growing list of forms encountered in genealogical research.

Includes transcription and data entry versions with optional XML wrappers.

## RootsMagic Topics

The following topics concern the RootsMagic Genealogy Project Management software.

See the software publisher's [Homepage](https://RootsMagic.com/RootsMagic).

I have no affiliation with the RootsMagic organization, I am only a user of
their product.

### [Tips and Tricks](tips/Tips.html) <a id="tips"></a>

A collection of ideas and investigations regarding the RootsMagic (RM) software.

I use RM on Windows, but most items will also apply to the MacOS version.

### [Data Entry Guidelines](data_entry/Data_Entry.html) <a id="data-entry"></a>

My rules for data entry into RM. I wish that I could say that I follow them exactly.

### [Bugs and Design-change Wish List](RootsMagic_Bugs_and_WishList.html)<a id="rm-changes"></a>

Current RootsMagic bugs that annoy me, and some wishes for design changes.

### [Custom Source RM and ORA Templates](SourceTemplate/Source_templates.html)<a id="src-temp"></a>

A sample of some of the custom source templates I've created for RM and an
explanation of the problems they solve. Also included are several
[ORA-Extension](https://www.ORA-extension.com) auto-type templates.

### [Database Design Docs and Notes](https://github.com/RichardOtter/RootsMagic_Database_Design/tree/main/Tables) <a id="db-design"></a>

A set of documents describing what has been reverse engineered about the
design of the v10 RootsMagic database and its contents. (see the git
branches for previous versions.)
The information is useful when designing SQL to directly access and
modify the database.

This is an Open Source type project where anyone can contribute and
anyone can use the data, and the data is all under version control.
Contributors are acknowledged.

### [Run SQL on Your RootsMagic Database Safely](Run_SQL_on_RM_database.html) <a id="run-sql-info"></a>

A short, work in progress, tutorial on how to run SQL on your database
and not cause a disaster.

Be aware that RM Inc. support does not recommend running SQL on an RM database
and may not offer help if they learn that you have done so.

## RootsMagic Helper Utilities <a id="rm-utilities"></a>

I have created a set of Python scripts which provide features not found in
the RootsMagic software.

The software utilities listed below are ones that I've "released".
That means that I've done a reasonable amount of testing and the
documentation is accurate.
Each is documented by a ReadMe.txt file.

### Download the utility apps <a id="download"></a>

**The utilities are all available in a single zip file with the general file
name of "RM_Utilities_Suite_v[n.n.n].zip".**

The zip file is found on the "Release" page on Github.
Looking at the
[Release page]((https://github.com/RichardOtter/Genealogy-scripts/releases/latest)),
find the section at the bottom of the page labeled "Assets".

You want to download the first item in the list: RM_Utilities_Suite_v[n.n.n].zip

That zip file will contain most everything you need to get started.
You will not find the items "Source code (zip)" and "Source code (tar.gzip)" useful.

**To use any or all of these utilities**, start by going to the RootsMagic Utilities
[Releases page at github.com](https://github.com/RichardOtter/Genealogy-scripts/releases/latest)

See the [note below](https://RichardOtter.github.io/#ReleaseFormatChange)
for why the download format has changed from past releases.

### [Media Files Helper Utility: "TestExternalFiles"](https://RichardOtter.github.io/#Download) <a id="tef"></a>

A utility application that can help maintain integrity of the external
file links in RootsMagic.

Capabilities-

* Find items in the media gallery that have broken/incorrect file path.
* Find duplicate items in the media gallery.
* Find media items that are not tagged/used.
* Find items in the media gallery that are not located in the RM Media Folder.
* Find items in your media folder that are not referenced by the database.
* Find files in your media folder that have identical file names.
* Create an listing of all media items along with their MD5 hashes.

The utility app was favorably reviewed at the
[SQLite Tools for RootsMagic](https://sqlitetoolsforrootsmagic.com/new-app-aids-media-management)
site. Thanks Tom !

### [Group Creator/Updater Utility: "GroupFromSQL"](https://RichardOtter.github.io/#Download) <a id="group"></a>

Update a group in a RootsMagic database from a previously tested SQL SELECT statement.

Benefits-

* Any query that you can write can be used to create (update) a group.
* Not limited to RM search capabilities. (especially with
multi-instance facts e.g census, residence)
* Many groups can be updated in one run.

### [Sample SQL Queries for Use with the Group Creator Utility (see above)](https://github.com/RichardOtter/Genealogy-scripts/tree/main/RM/SQL%20for%20creating%20useful%20groups)

Copy and paste into your RM-Python-config.ini file and create the group!\
These are included in the download file in the Group From SQL folder.

### [Color Code Utility: "ColorFromGroup"](https://RichardOtter.github.io/#Download) <a id="color"></a>

Update the color coding for a group of people in a RootsMagic database.
Can do many groups in the same run.

Works well with the GroupFromSQL utility.

### [List all citations attached to a person utility: "ListCitationsForPersonID"](https://RichardOtter.github.io/#Download) <a id="list-citations"></a>

A simple utility to list all of the source citations connected with a person.
The user supplies a RIN/PersonID and all citations are listed
alphabetically in a text file.

### [RootsMagic: Change Source for a Citation Utility: "ChangeSrcForCitation"](https://RichardOtter.github.io/#Download) <a id="change-src"></a>

A simple utility to fix a particular kind of data entry mistakes.
It does lots of error checking to prevent further errors.

The fix that this utility makes is trivial in SQL, but this app
takes information that is available in the RootsMagic user interface
and does all of the look-ups for you. A final change summary
report is shown.

### [Citation Sort Order Utility: "CitationSortOrder"](https://RichardOtter.github.io/#Download) <a id="sort"></a>

A utility to allow the user to re-order the listing of citations
attached to Persons, Names, or Facts.

### [Convert Fact to Another Fact Type Utility: "ConvertFact"](https://RichardOtter.github.io/#Download) <a id="convert-fact"></a>

A utility to convert a fact or set of facts from one fact type to another.
Deals correctly with existing witnesses and their roles.
Allows the conversion to be limited to a subset of facts
as opposed to RM's solution which will convert all facts.

### [Change Source Template Already In Use: "ChangeSourceTemplate"](https://RichardOtter.github.io/#Download) <a id="change-template"></a>

A utility to change the source template used by a set of sources.

Used to allow change/improvement of a source template even after
it has been used to create sources and citations.

### [Run SQL On Your Database Utility: "RunSQL"](https://RichardOtter.github.io/#Download) <a id="run-sql"></a>

This utility is meant to help the novice SQL user get the task done.
It attempts to eliminate most of the complications found using
more sophisticated off-the-shelf software.

This utility will run SQL statements and SQL script files on a
database and display the results in a text file.

Step 1 for using this utility- "Create or find or solicit an SQL
statement or file to run.
<https://SQLiteToolsForRootsMagic.com> is a great place to ask for help with SQL.
For questions about this utility, use the email found at the end
of the ReadMe file to contact me.

## Developing SQL Against the RootsMagic Database

This [link](https://github.com/RichardOtter/Genealogy-scripts) brings
you to the root of my GitHub repo for database SQL development.

Check out these [queries](https://github.com/RichardOtter/Genealogy-scripts/tree/main/RM/SQL%20for%20creating%20useful%20groups)
using recursive SQL. They are perfect for use with the GroupFromSQL utility.

Perhaps interesting to folks starting out with SQL on their RM database will be the
document describing the issues with the
proprietary SQLite collation "RMNOCASE". [Notes on collation RMNOCASE](https://github.com/RichardOtter/Genealogy-scripts/blob/main/RM/doc/Notes%20on%20collation%20RMNOCASE.md)

## Miscellaneous

### [RM Utilities Release History with MD5 hashes](RM_Utilities_Release_History.html)

### [Download stats for recent RootsMagic utilities](https://tooomm.github.io/github-release-stats/?username=RichardOtter&repository=Genealogy-scripts)

### RM Utilities Release Format Change

News as of 2024-12-10  \
A new release format was necessitated by an indirect problem I
was not aware of until recently.
The problem was, in a sense, only an inconvenience, as there were
ways to circumvent it.

People who have previously attempted to download the utilities
have probably been warned that the zip file contained a virus or malware.
I want to state emphatically that none of the files ever posted on
my GitHub site ever posed an actual hazard.
The anti virus tools simply miss-identified my zip files as containing malware.

PyInstaller is a Python tool that allows a python
text script to be packaged with all that is needed to run and then
compressed into an exe executable file.
This was done as a convenience for the user.

A web search for "PyInstaller virus warning" shows the magnitude of the issue.

It is clear that malware has also been packaged by bad actors
using the same software distribution system I was using (PyInstaller).
The anti virus companies then created file signatures that detected these threats.
Unfortunately, it seems like every piece of software packaged
using PyInstaller has the same "signature".

The Internet has gotten to be a dangerous place, and it seems there
are fewer and fewer ways for non-corporate software developers to
distribute ready-to-run files.

#### Advantages to the New Format

* All apps in the same zip file will perhaps encourage users to
try an app they didn't know they needed.

* All apps are tested with each other using the same RMpy package (common code).

* Much less effort maintaining one release than in the previous system.

* All of the software is human-readable. Each user can read the
code and confirm that nothing bad is happening.

## GitHub File Download Help

Some of the links above (e.g. Genealogy standard forms, RootsMagic database
design docs and notes) point to GitHub.com files.

[This](GitHub_fie_download.html) is a description of how to
download a single file or a collection of files from
Github without any knowledge of the git software.
\
\
\
\
\
\
About me:\
Richard J Otter\
California, United States\
[My Linked-In profile](https://www.linkedin.com/in/RichardOtter/)

Public comments regarding the contents of this site may be left using
the GitHub issue tracking system at-
[Web site Issues and Comments](https://github.com/RichardOtter/RichardOtter.github.io/issues)\
or you can contact me at:\
RichardJOtter &emsp;=-at-=&emsp;g&emsp;mail

I much prefer email over FaceBook messenger.
