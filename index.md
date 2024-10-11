---
Title: Home - My Bare Minimum Site
---

Last Updated: 2024-10-11

This site and its contents are a work in progress.

## Topics

Many of these topics concern the RootsMagic Genealogy Project Management software. See the company's [Homepage](https://RootsMagic.com/RootsMagic).

Some of these links (e.g. Genealogy standard forms, RootsMagic database design docs and notes) point to GitHub.com source files. 
[Here](https://zapier.com/blog/how-to-download-from-github/) is a nice description for how to download a single file or a collection of files from Github without any knowledge of Git.

### [RootsMagic Tips and Tricks](tips/RootsMagic_Tips_and_Tricks.html)

A collection of ideas and investigations regarding RootsMagic (RM) genealogy project management software.

I use RM on Windows, but most items will also apply to the MacOS version.

### [RootsMagic bugs and design-change wish list](RootsMagic_Bugs_and_WishList.html)

Current RootsMagic bugs that annoy me, and some wishes for design changes.

### [Run SQL on your RootsMagic database safely](Run_SQL_on_RM_database.html)

A short, work in progress, tutorial on how to run SQL on your database and not cause a disaster.

### [Some custom RM source templates](SourceTemplate/Source_templates.html)

A sample of some of the custom source templates I've created for RM and an explanation of the problems they solve.

### [RootsMagic database design docs and notes](https://github.com/ricko2001/RootsMagic_Database_Design/tree/main/Tables)

A set of documents describing what has been reverse engineered about the
design of the v10 RootsMagic database and its contents. (see branches for previous versions.)
The information is useful when designing SQL to directly access and modify the database.

This is an Open Source type project where anyone can contribute and anyone can use the data, and the data is
all under version control. Contributors are acknowledged.

### [Genealogy standard forms](https://github.com/ricko2001/Standard-forms-for-genealogy)

A slowly growing list of forms encountered in genealogical research.

Includes transcription and data entry versions.

<!-- ### [Genealogy Scripts repo Read Me file](https://github.com/ricko2001/Genealogy-scripts/blob/main/README.md)

This is a summary of what's in the Genealogy Scripts repo, similar to this page. -->

## Software utilities

The utilities listed below are ones that I've "released". That means that I've done a reasonable amount of testing, documentation is accurate, and I've included a single file exe version of the Python script so Python installation is not required. Each has a ReadMe.txt file in lieu of a user manual.

The links provided point to a "Release" page on Github. Look for the section labeled "Assets".\
You want to download the first item in the list:\
 [appname] v[n.n.n].zip\
That zip file will contain everything you need to get started.\
You will not find the items "Source code (zip)" and "Source code (tar.gzip)" useful.

### [RootsMagic Media Files Helper Utility: "TestExternalFiles"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/TestExternalFiles_v1.7.0)

A utility application that can help maintain integrity of the external file links in RootsMagic.

Capabilities-

* Find items in the media gallery that have broken/incorrect file path.
* Find duplicate items in the media gallery.
* Find media items that are not tagged/used.
* Find items in the media gallery that are not located in the Media Folder.
* Find items in your media folder that are not referenced by the database.
* Find files in your media folder that have identical file names.
* Create an listing of all media items along with their MD5 hashes.

The utility app was favorably reviewed at the [SQLite Tools for RootsMagic](https://sqlitetoolsforrootsmagic.com/new-app-aids-media-management) site. Thanks Tom !

New! &emsp; v1.7 released on 2024-10-04   A couple of new features.

### [RootsMagic Group creator utility: "GroupFromSQL"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/GroupFromSQL_v1.3.0)

Update a group in a RootsMagic database from a previously tested SQL SELECT statement.

Benefits-

* Any query that you can write can be used to create (update) a group.
* Not limited to RM search capabilities.
* Very fast. Double click an icon and it's done in 1 to 5 seconds.

New! &emsp; v1.3 released on 2024-10-05
Now allows multiple line values for key GROUP_NAME
Each assigned group name, one per line, is updated in the same run.
Improved output format.

### [Sample SQL queries for use with Group creator utility (see above)](https://github.com/ricko2001/Genealogy-scripts/tree/main/RM%20-SQL%20for%20creating%20useful%20groups)

Copy and paste into your RM-Python-config.ini file and create the group!

### [RootsMagic List all citations attached to a person: "ListCitationsForPersonID"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/ListCitationsForPersonID_v1.1.0)

A simple utility to list all of the source citations connected with a person. The user supplies a RIN/PersonID and all citations are listed alphabetically in a text file.\
New! &emsp; v1.1 release includes citations attached to shared facts.

### [RootsMagic Change Source for a Citation Utility: "ChangeSrcForCitation"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/ChangeSrcForCitation_v1.0.1)

A simple utility to fix a particular kind of data entry mistakes. It does lots of error checking to prevent further errors.

The fix that this utility makes is trivial in SQL, but this app takes information that is available in the RootsMagic user interface and does all of the look ups for you. A final change summary is also shown.

New! &emsp; v1.0.1 released on 2024-10-07  Maintenance release.

### [RootsMagic Citation Sort Order: "CitationSortOrder"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/CitationSortOrder_v1.0.0.0)

A utility to allow the user to re-order the listing of citations attached to Persons, Names, or Facts.

### [RootsMagic Convert Fact to another Fact Type: "ConvertFact"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/ConvertFact_v1.1.0)

A utility to convert a fact or set of facts from one fact type to another. Deals correctly with existing witnesses and their roles.

### [RootsMagic Change source template that is in use: "ChangeSourceTemplate"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/ChangeSourceTemplate_v1.1.0)

A utility to change the source template used by a set of sources.

Used to allow change/improvement of a source template even after it has been used to create sources and citations.

New! &emsp; v1.1 released on 2024-10-07
Better error handling

### [RootsMagic Run SQL on your database: "RunSQL"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/RunSQL_v1.2.0)

This utility is meant to help the novice SQL user get the task done.
It attempts to eliminate most of the complications found using more sophisticated off-the-shelf software.

This utility will run SQL statements and SQL script files on a database and display the results in a text file.

Step 1 for using this utility- "Create or find or solicit an SQL statement or file to run.
<https://SQLiteToolsForRootsMagic.com> is a great place to ask for help with SQL.
For questions about this utility, use the email found at the end of the ReadMe file.

## [Developing SQL against the RootsMagic database](https://github.com/ricko2001/Genealogy-scripts)

This link brings you to the root of my GitHub repo for database SQL development.

Check out these [queries](https://github.com/ricko2001/Genealogy-scripts/tree/main/RM%20-SQL%20for%20creating%20useful%20groups)

Probably the most interesting will be the document describing the issues with the
proprietary collation RMNOCASE [Notes on collation RMNOCASE](https://github.com/ricko2001/Genealogy-scripts/blob/main/Notes%20on%20collation%20RMNOCASE.md)


How popular are my RootsMagic utilities? Check [this](https://tooomm.github.io/github-release-stats/?username=ricko2001&repository=Genealogy-scripts) link for download statistics.

\
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
