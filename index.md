---
Title: Home - My Bare Minimum Site
---

Last Updated: 2024-04-25

This site and its contents are a work in progress.

## Topics

Some of these links (e.g. Genealogy standard forms, RootsMagic database design docs and notes) point to GitHub.com source files.

[Here](https://zapier.com/blog/how-to-download-from-github/) is a nice explanation on how to download a single file or a collection of files from Github.

### [RootsMagic Tips and Tricks](tips/RootsMagic_Tips_and_Tricks.html)

A collection of ideas and investigations regarding RootsMagic (RM) genealogy project management software.

I use RM on Windows, but most items will also apply to the MacOS version.

### [RootsMagic bugs and design-change wish list](RootsMagic_Bugs_and_WishList.html)

Current RootsMagic bugs that annoy me, and some design change wishes.

### [Run SQL on your RootsMagic database safely](Run_SQL_on_RM_database.html)

A short, work in progress, tutorial on how to run SQL on your database and not cause a disaster.

### [Some custom RM source templates](SourceTemplate/Source_templates.html)

A sample of some of the custom source templates I've created for RM and an explanation of the problems they solve.

### [RootsMagic database design docs and notes](https://github.com/ricko2001/RootsMagic_Database_Design/tree/main/Tables)

A set of documents describing what has been reverse-engineered about the
design of the v9 RootsMagic database and its contents.
The information is useful when designing SQL to directly access and modify
the database.

The goal is to make this an Open Source type project where anyone can contribute and anyone can use the data, and all under version control.
Contributors are acknowledged.

### [Genealogy standard forms](https://github.com/ricko2001/Standard-forms-for-genealogy)

A slowly growing list of forms encountered in genealogical research.

Includes transcription and data entry versions.

<!-- ### [Genealogy Scripts repo Read Me file](https://github.com/ricko2001/Genealogy-scripts/blob/main/README.md)

This is a summary of what's in the Genealogy Scripts repo, similar to this page. -->

## Software utilities

The utilities listed below are ones that I've "released". That means that I've done a reasonable amount of testing, documentation is accurate, and I've included a single file exe version of the Python script so Python installation is not required. Each has a ReadMe.txt file that attempts to be a user manual.

The links provided point to a "Release" page on Github. Look for the section labels "Assets". You want to download the first item in the list:\
 [appname] v[n.n.n].zip\
That zip file will contain everything you need to get started. The items "Source code (zip)" and "Source code (tar.gzip)" are not useful.

### [RootsMagic Media Files Helper Utility: "TestExternalFiles"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/TestExternalFiles_v1.6.0.0)

A utility application that can help maintain integrity of the external files links in RootsMagic.

Capabilities-

* Find items in the media gallery that have broken/incorrect file path.
* Find duplicate items in the media gallery.
* Find media items that are not tagged/used.
* Find items in your media folder that are not referenced by the database.
* Find files in your media folder that have identical file names.
* Create an listing of all media items along with their MD5 hashes.

The utility app was favorably reviewed at the [SQLite Tools for RootsMagic](https://sqlitetoolsforrootsmagic.com/new-app-aids-media-management) site. Thanks Tom !

New!&emsp;v1.6 released on 2024-02-13

### [RootsMagic Group creator utility: "GroupFromSQL"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/GroupFromSQL_v1.1.0.0)

Create or update a group in a RootsMagic database from a previously tested SQL SELECT statement.

Benefits-

* Any query that you can write can be used to create a group.
* Not limited to RM search capabilities.
* Very fast. Double click an icon and it's done in 1 to 5 seconds.

New!&emsp;v1.1 released on 2023-12-31

### [Sample SQL queries for use with Group creator utility (see above)](https://github.com/ricko2001/Genealogy-scripts/tree/main/RM%20-SQL%20for%20creating%20useful%20groups)

Copy and paste into your RM-Python-config.ini file and create the group!

### [RootsMagic Change Source for a Citation Utility: "ChangeSrcForCitation"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/ChangeSrcForCitation_v1.0.0.0)

A simple utility to fix a particular kind of data entry mistakes. It does lots of error checking to prevent further errors.

The fix that this utility makes is trivial in SQL, but this app takes information that is available in the RootsMagic user interface and does all of the look ups for you. A final change summary is also shown.

### [RootsMagic Citation Sort Order: "CitationSortOrder"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/CitationSortOrder_v1.0.0.0)

A utility to allow the user to re-order the listing of citations attached to Persons, Names, or Facts.

### [RootsMagic Convert Fact to another Fact Type: "ConvertFact"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/ConvertFact_v1.0.0)

A utility to convert a fact or set of facts from one fact type to another. Deals correctly with existing witnesses and their roles.

### [RootsMagic Change source template that is in use: "ChangeSourceTemplate"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/ChangeSourceTemplate_v1.0.0)

A utility to change the source template used by a set of sources.

Used to allow change/improvement of a source template even after it has been used to create sources and citations.

### [RootsMagic Run a SQL command on your database: "RunSQL"](https://github.com/ricko2001/Genealogy-scripts/releases/tag/RunSQL_v1.0.0)

This utility is meant to help the novice SQL user get the task done.
It attempts to eliminate most of the complications found using more sophisticated
off-the-shelf software.

This utility will run one or two SQL statements on a database and display the
results in a report file.

Step 1 for using this utility- "Create or find or solicit an SQL statement to run.
<https://SQLiteToolsForRootsMagic.com> is a great place to ask for help with SQL.
For questions about this utility, use the email found at the end of the ReadMe file.

## [Developing SQL against the RootsMagic databae](https://github.com/ricko2001/Genealogy-scripts)

This link brings you to the root of my GitHub repo for database SQL development.

Check out these [queries](https://github.com/ricko2001/Genealogy-scripts/tree/main/RM%20-SQL%20for%20creating%20useful%20groups)

Probably the most interesting will be the document describing the issues with the
proprieoty collation RMNOCASE [Notes on collation RMNOCASE](https://github.com/ricko2001/Genealogy-scripts/blob/main/Notes%20on%20collation%20RMNOCASE.md)

\-\
\-\
\-\
\-\
\-\
\-\
\-

About me:\
Richard J Otter\
California, United States\
[My Linked-In profile](https://www.linkedin.com/in/richardotter/)

Comments regarding the contents of this site may be left using the GitHub issue tracking system at-
[Web site Issues and Comments](https://github.com/RichardOtter/RichardOtter.github.io/issues)\
or if you'd prefer, you can contact me at:\
RichardJOtter &emsp;=-at-=&emsp;g&emsp;mail
