---
title: Run SQL on your RootsMagic database
---
[Home](https://richardotter.github.io)


# Tutorial: Run SQL on your RootsMagic database

Last Updated:  2024-10-23


## Always have a current backup of your database

You should actually already be making frequent backups. There are changes that can be made within RM which would be VERY difficult to undo. Such as merging two places that shouldn't be merged.

Making a backup after two weeks of work basically means that you are willing to lose two weeks of work. I'm willing to lose an hour's of work, at most, so I do backups every hour or so. Also a good time to get up and stretch.

Keep all of your backup files. Add the date and a timestamp "-HHMM" to the filenames so they don't overwrite. Disk space is so cheap compared to your time and effort.

## Options

There are several ways to run SQL commands against the RootsMagic (RM) database.

This tutorial will use the methods I am most familiar with on Windows. The goal is to make the process as straight forward as possible, options will confuse the reader. As I update this tutorial, I'll add notes that describe alternatives.

The first part of this tutorial creates your work environment. The point of creating a work environment is to avoid any possibility of confusing which database you are running SQL on and which is your precious research database. You can skip this, if you like to take needless risks.

I think it's best not to work directly on your main database file. I suggest working on a copy in a separate folder. Only after I am satisfied that the modifications made to the file copy are correct, do I rename the copy and use it for actual research.

This concept is called the separation of the Development environment from the Production environment.

Your main database file that you update as you do research is called the Production database, the database file on which the SQL commands will be run, is called the Development database and it should be named TEST.rmtree or some variant.

After successfully running a script many times in a development environment, it can be considered "tested". That's when I switch to running the script directly on my research database. (I still have backups.)

All of the cautions that I mention are most relevant when your SQL modifies the database, not so much if you are just running SELECT statements, but mistakes are guaranteed to happen.

# Set up the development environment:

## Create the folders
There are three command scripts (extension ".cmd") that can be found in GitHub at:
[dev util scripts](https://github.com/ricko2001/Genealogy-scripts/tree/main/dev%20util%20scripts)

The first file and link is:

* SetUp dev folders.cmd  [FILE_LINK](https://github.com/ricko2001/Genealogy-scripts/blob/main/dev%20util%20scripts/SetUp%20dev%20folders.cmd)


[Here](GitHub_fie_download.md) is how to download a file from the above file link.

Download the 'SetUp dev folders.cmd' file, examine it to convince yourself that it is safe, and run it. It doesn't matter where you initially save it. You will only run it once.

The cmd file will create a set of nested folders in your Home folder:
Your home folder is the folder with your login name, 'Me' ( C:\Users\Me )\
C:\Users\Me\dev\
C:\Users\Me\dev\SQL\
C:\Users\Me\dev\SQL\DB

The SQL folder is intended to contain your SQL script text file.
The DB folder will contain the copy of you database on which you will experiment and a backup copy.
The DB folder will also contain the database refresh cmd scripts. (see below)

## Download the database refresh scripts

Getting a copy of the database from its normal location is something that will be done often while
developing data-modifying SQL scripts. It is best to automate that procedure to avoid mistakes.

Download these two files, using the FILE_LINKS to the above mentioned DB folder:

* _DB get fresh copy.cmd [FILE_LINK](https://github.com/ricko2001/Genealogy-scripts/blob/main/dev%20util%20scripts/_DB%20get%20fresh%20copy.cmd)
* _DB reset test db.cmd  [FILE_LINK](https://github.com/ricko2001/Genealogy-scripts/blob/main/dev%20util%20scripts/_DB%20reset%20test%20db.cmd)

Edit the "_DB get fresh copy.cmd" file so that \
SET PRODUCTION_DB_PATH= is followed by the path to your production database folder and \
PRODUCTION_DB_NAME= is followed by your production database file name (without the extension)

Again, examine the file to see that it is safe. It simply copies your production database to the SQL folder and then copies the copy.

To test and demonstrate the cmd file, in File Manager-\
open the DB folder\
double click the "_DB get fresh copy.cmd" file.\
You should see two new files created:\
TEST-SQL.rmtree\
and\
BACKUP_TEST-SQL.rmtree

TEST-SQL.rmtree is the database that you run your SQL on. 
The BACKUP_TEST-SQL.rmtree is just a local backup.

Assuming you didn't change other items in the first file, the "DB reset test db" file should work as-is.

To test and demonstrate the cmd file, in File Manager-\
open the DB folder\
delete the TEST-SQL.rmtree fike\
double click the "DB reset test db.cmd"\
You'll see a new copy of TEST-SQL.rmtree created. 
(The new copy was created from the BACKUP_TEST-SQL.rmtree file)

This last command is the command you will use routinely to refresh the database you are working on.

## Install the SQL manager software

If you don't know how to write SQL and have obtained a SQL statement from another source, perhaps the easiest way to start is to use the RunSQL utility app I've written.
See the NOTES section.

When creating your own SQL, I suggest that you install the "SQLite Expert Personal" software. Many alternatives exist; it's just the one I use.

Direct download link-
[SQLite Expert Personal](https://www.sqliteexpert.com/v5/SQLiteExpertPersSetup64.exe)

Install using the default options.

## You're ready to work

You may now run any SQL query or update that does not involve sorting or comparing data in columns collated with RMNOCASE.

If your SQL returns with an error such as "No such collation sequence: RMNOCASE",
extra work will be needed.

## No such collation sequence: RMNOCASE

"No such collation sequence: RMNOCASE" is an error message that may surprise the novice SQL user.

SQLite needs the ability to sort data. It does so by comparing two items and determining if one is equal, less than or greater than the other by using a collation function. This collation function will always say that "a" = "a", but how about "a" = "A"?  That will depend on how the collation function is designed.

The RootsMagic database was designed to use a collation function name "RMNOCASE". This function is not part of SQLite, but was created by RootsMagic developers and has not been made public. 

Some examples will help clarify.
The SourceTable contains a column "Name". This is the source name displayed in RM.

The query:\
SELECT Name FROM SourceTable;\
will now work. The Name column is collated with RMNOCASE, but this query does not do any comparisons or sorting on it.

The query:\
SELECT Name FROM SourceTable ORDER BY Name;\
however, will return the above mentioned error message, because comparisons are needed to execute the 'ORDER BY Name' clause.

One can work around this issue by recoding the SQL to:\
SELECT Name FROM SourceTable ORDER BY Name COLLATE NOCASE;\
This will execute without error, but may give the list in a different sort order than RM because it is using the SQLite builtin NOCASE collation instead of the RM proprietary RMNOCASE collation.

Using the COLLATE NOCASE trick works in most situations when doing queries. One may have to add it multiple times in the same SQL statement.

The results may differ for some lists depending on the content. Most issues will involve characters outside the usual western european range, such as Cyrillic, Greek, Chinese characters etc. etc.

Update, Insert and Delete statements are a different matter.
I will group these data change statements into the category modifying SQL. Modifying SQL that does not involve changes to columns collated with RMNOCASE should run without error. COLLATE NOCASE may need to be used in join clauses etc.
If a column that is indexed and collated with RMNOCASE is modified, however, then the corresponding index also must be updated- and that can't be done unless RMNOCASE is available. That's when the "No such collation sequence: RMNOCASE" error message will appear.

We can make a collation function named RMNOCASE available by using a database extension. This database extension is in a file named unifuzz64.dll. It is in a Windows shared library file. Note however, that this is not the same as the collation named RMNOCASE using within RM.

This leads to some extra limitations and extra steps, but nothing too severe- unless they are not followed!

The easy part is getting the database extension and loading it. See next section.

## Obtain the SQLite extension file named 'unifuzz64.dll' and load it

Direct download link- 
[unifuzz64.dll](https://sqlitetoolsforrootsmagic.com/wp-content/uploads/2018/05/unifuzz64.dll)

Place the dll file in the "C:\Users\Me\dev\SQL" folder.

Launch SQLite Expert and open the TEST-SQL.rmtree file in the DB folder as above.

The database loads and the tables displayed at the left side.\
The root entry is TEST-SQL, the name of the database file.

Right click the TEST top level entry, and select the "Load Extension" command.

A small dialog, "Select extension options" appears.\
Click the small box at the right end of the "File Name" field and browse to the SQL folder and select the unifuzz64.dll file.\
The "Entry Point" field is filled automatically. Don't change it. \
Don't check the box labeled  "Auto" for now.\
Hit OK

## Use of the RMNOCASE collation provided by 'unifuzz64.dll'

**Important:\
  When the database extension providing RMNOCASE command is loaded, the file being worked on in the SQL manager app should not be open in RM.  I'd suggest closing RM before loading the unifuzz64.dll extension.**

Now that the unifuzz64.dll database extension is loaded, the RMNOCASE collation provided by it is available to SQL commands. However, because this RMNOCASE is not identical to the one in RM, the database produced with RM has indexes that are not compatible with this version of RMNOCASE.

This is easily solved by issuing the SQL command: **REINDEX RMNOCASE;**

That will regenerate the appropriate indexes so that are are all compatible with the loaded RMNOCASE. Now you are ready to run you modifying SQL statements that affect any column.

## Test your work

When you're satisfied with the results shown the the SQL manager app, you are ready to test your work in RootsMagic.

**Important:\
  For a file that has been modified by SQL or whose indexes were rebuilt outside of RM (as in the above REINDEX RMNOCASE command), the indexes need to be rebuilt again as the first operation done after opening in RM.**

Do the following steps-\
Close the database file in SQLiteExpert.\
Open the database file in RootsMagic\
In RM, open the Tools tab\
Select the "Rebuild indexes" Database tool and click the "Run selected tool" button.

Run the Test database integrity tool as well for confirmation and to make yourself feel good. The check integrity tool only diagnoses problems. it does not make any changes.

Check that you have the expected results in RM.

## Use the modified database for research

Remember, think hard before starting to use a modified database as your production database. If you find a problem later on and need to revert to your backup, you will have lost work. I often don't use a modified database right away. I'll continue to use the production database for several days so I can continue to think about changes I made.

Rename your production database by adding a time stamp (YYY-MM-DD) to the end.

Copy the tested TEST.rmtree database to the folder where the production database is normally located.

Rename the TEST.rmtree database file to the usual name used for production.

Use the forum at [SqliteToolsForRootsMagic](https://sqlitetoolsforrootsmagic.com/forum/forum/first-forum) to discuss your work and ask questions.

# NOTES

## RunSQL utility app

 See the topic-
*RootsMagic Run a SQL command on your database: “RunSQL”* 
on this [page](https://richardotter.github.io/).

Read the ReadMe file packaged with the utility.

When the ReadeMe file refers to the "working folder", it mostly corresponds to the 
"C:\Users\Me\dev\SQL" folder created in the instructions above. Thus, the "C:\Users\Me\dev\SQL" folder will contain the two files "RunSQL.exe" and "RM-Python-config.ini".

The ReadMe file advises that a database copy be placed in the working folder, but these instructions suggest using the database refresh scripts instead of doing the manual copy. The scripts place the database copy in the "C:\Users\Me\dev\SQL\DB" folder.

The RM-Python-config.ini configuration file that comes with the utility has the DB_PATH set to TEST.rmtree. You will need to change it to "DB_PATH = DB\TEST-SQL.rmtree"

## SQLite Expert Personal

Use the 64 bit version. The download page is at:\
<https://www.sqliteexpert.com/download.html>

The Personal version is free. There is also a paid Professional version, but it's not needed.

There are a number of other GUI and command line SQLite manager applications.SQLite Expert is the one I use to do development.

To run SQL script files, I use my RunSQL utility.

## Creating additional folders under C:\Users\dev

You may decide to create a folder for each project. Just make the new folder under C:\Users\dev and the DB folder within it. Copy the two cmd files to the new DB folder. When they are run, the database copies will use the name of the new folder in their names. Thus, database files will always have unique names to avoid confusion.

## Assessing safety of the unifuzz64.dll file

The download link for the unifuzz64.dll file is found in this context-\
<https://sqlitetoolsforrootsmagic.com/rmnocase-faking-it-in-sqlite-expert-command-line-shell-et-al/>

The SQLiteToolsforRootsMagic website has been around for years and
is run by a trusted RM user. Many posts to public RootsMagic user forums
mention use of unifuzz64.dll from the SQLiteToolsforRootsMagic website.

This is the file I have been using for years-\
----MD5 hash-----------------------------------File size----------File name\
----06a1f485b0fae62caa80850a8c7fd7c2-----256,406 bytes----unifuzz64.dll\

You can use the MD5 hash value to confirm you have the exact-same file downloaded.

Instructions to compute the MD5 of a file can be found at:
<https://portal.nutanix.com/page/documents/kbs/details?targetId=kA07V000000LWYqSAO\>

## Use of the REINDEX RMNOCASE command and the "Rebuild indexes" tool

These commands are needed only in specific circumstances.\
Not required when:\
the database is only queried using SQL\
AND\
if none of the columns involved in update or insert sql statements are collated using RMNOCASE.

Situations in which oly queries are done:
If the query involves RMNOCASE collated columns, and you use unifuzz64, you may get errors on occasion. It appears to be rare, but the query is not guaranteed to work unless you do a REINDEX RMNOCASE before the query. That will obviously require use of the "Rebuild indexes" tool in RM.

Many queries can be written to override the use of RMNOCASE.

The fundamental issue is that the RMNOCASE collation provided by the SQLite extension unifuzz64.dll is not identical to the RMNOCASE collation provided by the RootsMagic app.


see the document- [Notes on collation RMNOCASE](https://github.com/ricko2001/Genealogy-scripts/blob/main/Notes%20on%20collation%20RMNOCASE.md)

## Use of regular expressions in SQLite

Some SQL manager apps directly support regular expressions. I am not clear if this is done by using a special SQLlite build or if it is done in the manager app.

I prefer to use a database extension.\
See: <https://antonz.org/sqlean-regexp/>

The extension can be downloaded from:\
<https://github.com/nalgeon/sqlean/releases>