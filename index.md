---
Title: Home - My Bare Minimum Site
---

Last Updated: 2025-02-02

This site and its contents are a work in progress.

Some of these links (e.g. Genealogy standard forms, RootsMagic database design docs and notes) point to GitHub.com files.
[This](GitHub_fie_download.html) is a description of how to download a single file or a collection of files from Github without any knowledge of git.


## General Topics

### [Genealogy standard forms](https://github.com/ricko2001/Standard-forms-for-genealogy)

A slowly growing list of forms encountered in genealogical research.

Includes transcription and data entry versions.

## RootsMagic Topics

The following topics concern the RootsMagic Genealogy Project Management software. See the software publisher's [Homepage](https://RootsMagic.com/RootsMagic).
I have no affiliation with the RootsMagic organization. 

### [RootsMagic Tips and Tricks](tips/RootsMagic_Tips_and_Tricks.html) <a name="Tips"></a>

A collection of ideas and investigations regarding the RootsMagic (RM) software.

I use RM on Windows, but most items will also apply to the MacOS version.

### [RootsMagic bugs and design-change wish list](RootsMagic_Bugs_and_WishList.html)

Current RootsMagic bugs that annoy me, and some wishes for design changes.

### [Custom RootsMagic source templates](SourceTemplate/Source_templates.html)

A sample of some of the custom source templates I've created for RM and an explanation of the problems they solve. Also included are several [ORA-Extension](https://www.ora-extension.com) templates.

### [RootsMagic database design docs and notes](https://github.com/ricko2001/RootsMagic_Database_Design/tree/main/Tables) <a name="DBdesign"></a>

A set of documents describing what has been reverse engineered about the
design of the v10 RootsMagic database and its contents. (see the git branches for previous versions.)
The information is useful when designing SQL to directly access and modify the database.

This is an Open Source type project where anyone can contribute and anyone can use the data, and the data is
all under version control. Contributors are acknowledged.

### [Run SQL on your RootsMagic database safely](Run_SQL_on_RM_database.html) <a name="Run_SQL_on_RMdb"></a>

A short, work in progress, tutorial on how to run SQL on your database and not cause a disaster.

Be aware that RM Inc. support does not recommend running SQL on an RM database and may not offer help if they learn that you have done so.


## RootsMagic Helper Utilities <a name="RMUtilities"></a>

I have created a set of Python scripts which provide features not found in the RootsMagic software.

The software utilities listed below are ones that I've "released". That means that I've done a reasonable amount of testing and the documentation is accurate.
Each is documented by a ReadMe.txt file.

### Download the utility apps <a name="Download"></a>

<b>The utilities are all available in a single zip file name "RM.Utilities.Suite.v[n.n.n].zip".

To use any or all of these helper utilities, visit the Releases page at 
github.com: [RM_Utilities_Suite_v[n.n.n].zip](https://github.com/ricko2001/Genealogy-scripts/releases/tag/RM_Utilities_Suite_v1.0.2)</b>

The download link, above, points to a "Release" page on Github. Look for the section at the bottom labeled "Assets".\
You want to download the first item in the list: RM_Utilities_Suite_v[n.n.n].zip

That zip file will contain most everything you need to get started.
You will not find the items "Source code (zip)" and "Source code (tar.gzip)" useful.

See the [note below](https://richardotter.github.io/#ReleaseFormatChange) for why the download format has changed.

### [Media files helper utility: "TestExternalFiles"](https://richardotter.github.io/#Download) <a name="TestExternalFiles"></a>

A utility application that can help maintain integrity of the external file links in RootsMagic.

Capabilities-

* Find items in the media gallery that have broken/incorrect file path.
* Find duplicate items in the media gallery.
* Find media items that are not tagged/used.
* Find items in the media gallery that are not located in the RM Media Folder.
* Find items in your media folder that are not referenced by the database.
* Find files in your media folder that have identical file names.
* Create an listing of all media items along with their MD5 hashes.

The utility app was favorably reviewed at the [SQLite Tools for RootsMagic](https://sqlitetoolsforrootsmagic.com/new-app-aids-media-management) site. Thanks Tom !

### [Group creator/updater utility: "GroupFromSQL"](https://richardotter.github.io/#Download) <a name="GroupFromSQL"></a>

Update a group in a RootsMagic database from a previously tested SQL SELECT statement.

Benefits-

* Any query that you can write can be used to create (update) a group.
* Not limited to RM search capabilities. (especially with multi-instance facts e.g census, residence)
* Many groups can be updated in one run.

### [Sample SQL queries for use with group creator utility (see above)](https://github.com/ricko2001/Genealogy-scripts/tree/main/RM/SQL%20for%20creating%20useful%20groups)

Copy and paste into your RM-Python-config.ini file and create the group!\
These are included in the download file in the Group From SQL folder.

### [Color code utility: "ColorFromGroup"](https://richardotter.github.io/#Download) <a name="ColorFromGroup"></a>

Update the color coding for a group of people in a RootsMagic database. Can do many groups in the same run.\
Works well with the GroupFromSQL utility.

### [List all citations attached to a person utility: "ListCitationsForPersonID"](https://richardotter.github.io/#Download) <a name="ListCitationsForPersonID"></a>

A simple utility to list all of the source citations connected with a person. The user supplies a RIN/PersonID and all citations are listed alphabetically in a text file.\

### [RootsMagic: Change source for a citation utility: "ChangeSrcForCitation"](https://richardotter.github.io/#Download) <a name="ChangeSrcForCitation"></a>

A simple utility to fix a particular kind of data entry mistakes. It does lots of error checking to prevent further errors.

The fix that this utility makes is trivial in SQL, but this app takes information that is available in the RootsMagic user interface and does all of the look-ups for you. A final change summary report is shown.

### [Citation sort order utility: "CitationSortOrder"](https://richardotter.github.io/#Download) <a name="CitationSortOrder"></a>

A utility to allow the user to re-order the listing of citations attached to Persons, Names, or Facts.

### [Convert fact to another fact Type utility: "ConvertFact"](https://richardotter.github.io/#Download) <a name="ConvertFact"></a>

A utility to convert a fact or set of facts from one fact type to another. Deals correctly with existing witnesses and their roles. Allows the conversion to be limited to a subset of facts
as opposed to RM's solution which will convert all facts.

### [Change source template that is in use: "ChangeSourceTemplate"](https://richardotter.github.io/#Download) <a name="ChangeSourceTemplate"></a>

A utility to change the source template used by a set of sources.

Used to allow change/improvement of a source template even after it has been used to create sources and citations.

### [Run SQL on your database utility: "RunSQL"](https://richardotter.github.io/#Download) <a name="RunSQL"></a>

This utility is meant to help the novice SQL user get the task done.
It attempts to eliminate most of the complications found using more sophisticated off-the-shelf software.

This utility will run SQL statements and SQL script files on a database and display the results in a text file.

Step 1 for using this utility- "Create or find or solicit an SQL statement or file to run.
<https://SQLiteToolsForRootsMagic.com> is a great place to ask for help with SQL.
For questions about this utility, use the email found at the end of the ReadMe file to contact me.

## Developing SQL against the RootsMagic database

This [link](https://github.com/ricko2001/Genealogy-scripts) brings you to the root of my GitHub repo for database SQL development.

Check out these [queries](https://github.com/ricko2001/Genealogy-scripts/tree/main/RM/SQL%20for%20creating%20useful%20groups)
using recursive SQL. They are perfect for use with the GroupFromSQL utility.

Perhaps interesting to folks starting out with SQL on their RM database will be the
document describing the issues with the
proprietary SQLite collation "RMNOCASE". [Notes on collation RMNOCASE](https://github.com/ricko2001/Genealogy-scripts/blob/main/RM/doc/Notes%20on%20collation%20RMNOCASE.md)

## Misc

[RM Utilities Release History with MD5 hashes](RM_Utilities_Release_History.html)

How popular are the RootsMagic utilities? Check [this](https://tooomm.github.io/github-release-stats/?username=ricko2001&repository=Genealogy-scripts) link for download statistics.

### RM Utilities Release Format Change <a name="ReleaseFormatChange"></a>

News as of 2024-12-10  \
A new release format was necessitated by an indirect problem I was not aware of until recently.
The problem was, in a sense, only an inconvenience, as there were ways to circumvent it.

People who have previously attempted to download the utilities
have probably been warned that the zip file contained a virus or malware.
I want to state emphatically that none of the files ever posted on my GitHub site ever posed an actual hazard.
The anti virus tools simply miss-identified my zip files as containing malware.

PyInstaller is a Python tool that allows a python 
text script to be packaged with all that is needed to run and then compressed into an exe executable file.
This was done as a convenience for the user.

A web search for "PyInstaller virus warning" shows the magnitude of the issue.

It is clear that malware has also been packaged by bad actors using the same software distribution system 
I was using (PyInstaller).
The anti virus companies then created file signatures that detected these threats.
Unfortunately, it seems like every piece of software packaged using PyInstaller has the same "signature".

The Internet has gotten to be a dangerous place, and it seems there
are fewer and fewer ways for non-corporate software developers to
distribute ready-to-run files.

#### There are advantages to the new format

* All apps in the same zip file will perhaps encourage users to try an app they didn't know they needed.

* All apps are tested with each other using the same RMpy package (common code).

* Much less effort maintaining one release than in the previous system.

* All of the software is human-readable. Each user can read the code and confirm that
nothing bad is happening.





\
\
\
\
\
About me:\
Richard J Otter\
California, United States\
[My Linked-In profile](https://www.linkedin.com/in/richardotter/)

Public comments regarding the contents of this site may be left using the GitHub issue tracking system at-
[Web site Issues and Comments](https://github.com/RichardOtter/RichardOtter.github.io/issues)\
or you can contact me at:\
RichardJOtter &emsp;=-at-=&emsp;g&emsp;mail
