---
title: Run SQL on your RM database
---
[Home](https://richardotter.github.io)


# Tutorial: Run SQL on your RM database

Last Updated:  2024-05-14

Step by Step

## Always have a current backup of your database

You should actually be making frequent backups. There are changes that can be made in RM which would be VERY difficult to undo. Such as merging two places that shouldn't be merged.

Making a backup after two weeks of work basically means that you are willing to lose two weeks of work. I'm willing to lose an hour's of work, at most, so I do backups every hour or so. Also a good time to get up and strech.

Keep all of your backup files. Add the date and a timestamp "-HHMM" to the filenames so they don't overwrite. Disk space is so cheap compared to your time and effort.

## Options

There are a number of ways to run SQL commands against the RootsMagic (RM) database.


This procedure will use the methods I am most familiar with on Windows. The goal is to make the process as straight forward as possible, options will confuse the reader. As I update this tutorial, I'll add notes that describe alternatives.

The first part of the procedure creates your work environment. The point of creating a work environment is to avoid any possibility of confusing which database you are running SQL on and which is your precious research database. You can skip this and go to step 3 if you like to take needless risks. 

I think it's best not to work directly on your main database file. I suggest working on a copy in a separate folder. Only after I am satisfied that the modifications made to the file copy are correct, do I rename the copy and use it for actual research.

This process is called the separation of the Development environment from the Production environment.

Your main database file that you update as you do research is called the Production database, the database file on which the SQL commands will be run, is called the Development database and it is named TEST.rmtree or some varient.

After sucessfully runnig a script many times in a work environment, it can be consudered "tested". That's when I switch to running the script directly on my research database. (I still have backups.)

All of the cautions that I mention are most relevant when your SQL modifies the database, not so much if you are just running SELECT  statements. 

# Set up the development (dev) environment:

## 1 Create the folders

Use the command line to run the command-
```
mkdir "%USERPROFILE%\dev\SQL\DB"
```
or, using File Manager\
Assuming your home folder is C:\Users\Me\
create a folder named- C:\Users\Me\dev\
create another folder named-C:\Users\Me\dev\SQL\
create another folder named-C:\Users\Me\dev\SQL\DB

The SQL folder will contain copies of your code, perhaps just sql text files.

The DB folder will contain the database refresh cmd scripts and dev copies if the database.

## 2 Create the database refresh scripts

Getting a copy of the database from its normal location is something that will be done often while developing data-modifying SQL scripts. It is best to automate that procedure to avoid mistakes.

There are two command scripts (extension us .cmd) that are found in
[Genealogy-scripts\dev util scripts](https://github.com/ricko2001/Genealogy-scripts/tree/main/dev%20util%20scripts)

They can be downloaded to the above mentioned DB foler or created using the following instructions.

### Comand file #1
Create a new text file in the DB folder.\
Name it-\
DB get fresh copy.cmd

Copy the following text into the file-

```
REM Copy the production database to the local dev database folder

SET DB_EXTEN=rmtree

SET PRODUCTION_DB_PATH=C:\Users\me\Genealogy
SET PRODUCTION_DB_NAME=MyDatabaseFileName

SET DEV_DB_PATH=.

SET DEV_DB_NAME=TEST
SET DEV_DB_BACKUP=TEST_dev_backup

REM delete existing dev test database and local backup
del "%DEV_DB_PATH%\%DEV_DB_NAME%.%DB_EXTEN%" 
del "%DEV_DB_PATH%\%DEV_DB_BACKUP%.%DB_EXTEN%"

REM This is the only reference to the production database environment
copy "%PRODUCTION_DB_PATH%\%PRODUCTION_DB_NAME%.%DB_EXTEN%" "%DEV_DB_PATH%\%DEV_DB_NAME%.%DB_EXTEN%"

REM create a local backup copy of the test DB
copy "%DEV_DB_PATH%\%DEV_DB_NAME%.%DB_EXTEN%" "%DEV_DB_PATH%\%DEV_DB_BACKUP%.%DB_EXTEN%"

REM pause and request input to close window - optional
pause
```

Edit this file so that \
SET PRODUCTION_DB_PATH= is followed by the path to your production database and \
PRODUCTION_DB_NAME= is followed by your production database file name (without the extension)

In File Manager-\
open the DB folder and double click the 
"DB get fresh copy.cmd" file. You should see two new files created:\
TEST.rmtree\
and\
TEST_dev_backup.rmtree

TEST is the database that you run your SQL on. The TEST_dev_backup is just a local backup.

### Comand file #2
Create a new text file in the DB folder. \
Name it-\
DB reset test db.cmd

Copy this text into the cmd file-

```
REM reset the TEST database from the local backup copy

SET DB_EXTEN=rmtree
SET DEV_DB_PATH=.

SET DEV_DB_NAME=TEST
SET DEV_DB_BACKUP=TEST_dev_backup

REM delete existing dev test database and local backup
del "%DEV_DB_PATH%\%DEV_DB_NAME%.%DB_EXTEN%" 

REM create a local backup copy of the test DB
copy "%DEV_DB_PATH%\%DEV_DB_BACKUP%.%DB_EXTEN%" "%DEV_DB_PATH%\%DEV_DB_NAME%.%DB_EXTEN%"

REM pause and request input to close window - optional
pause
```

Assuming you didn't change other items in the first file, this file should work as-is.

In File Manager-\
open the DB folder\
delete the TEST.rmtree\
double click the "DB reset test db.cmd"\
You'll see a new copy of TEST.rmtree created.\

This last command is the command you will use routinely to refresh the database you are working on.

# Install the SQL manager software and load extension

If you don't know how to write SQL and have obtained a SQL statement from another source, perhaos the easiest way to start is to use the RunSQL utility app I've written.

When writing your own SQL, install the SQLite Expert Personal software.

## 3a  RunSQL utility app

 See the topic-
*RootsMagic Run a SQL command on your database: “RunSQL”* on this [page](https://richardotter.github.io/).

Read the ReadMe file packaged with the utility and then skip to step 9 here.

## 3b Install the free application "SQLite Expert Personal"

Direct download link-
[SQLite Expert Personal](https://www.sqliteexpert.com/v5/SQLiteExpertPersSetup64.exe)

Install using the default options.

## 4 Download the SQLite extension file named- unifuzz64.dll

Not all RM SQL work will require this database extension, but I'd recommend doing this now anyway. It provides the custom collation RMNOCASE.

Direct download link- 
[unifuzz64.dll](https://sqlitetoolsforrootsmagic.com/wp-content/uploads/2018/05/unifuzz64.dll)

Place the file in the\
C:\Users\Me\dev \
folder.

## 5  Launch SQLite Expert & Open the Database

Launch SQLite Expert\
Select the menu command File>Open Database\
In the file open window, you will need to set the files to display to all types of files (*.*) in order to see the TEST.rmtree file.

Open the TEST.rmtree file in the DB folder.

The database loads and the tables displayed at the left side. The root entry is TEST, the name of the database file.

## 6  Load the unifuzz64.dll extension

Right click the TEST top level entry, and select the "Load Extension" command.

A small dialog, "Select extension options" appears.\
Click the small box at the right end of the "File Name" field and browse to the SQL folder and select the unifuzz64.dll file.\
The "Entry Point" field is auto filled.\
Don't check the "Auto" check box for now.\
Hit OK

## 7   REINDEX

Click on the SQL tab at the top of the right side panel.\
Enter the command:

```
REINDEX RMNOCASE;
```
and click the Execute SQL button at the bottom.

## 8      Now you're ready to work. 

Run your SQL in the SQL panel,

## 9     Test your work

When you're done and ready to test your work in RootsMagic

Important:\
  For a file that has been modified by SQL or whose indexes were rebuilt outside of RM, the indexes need to be rebuilt again as the first operation done after opening in RM.
  
Do the following steps-\
Close the database in SQLiteExpert.\
Open the TEST.rmtree in RootsMagic\
In RM, open the Tools tab\
Select the "Rebuild indexes" Database tool and click the "Run selected tool" button.

Run the Test database integrity tool as well for confirmation and to make yourself feel good. The check integrity tool only diagnoses problems. it does not make any changes.


## 10  Use the modified database for research

Remember, think hard before starting to use a modified database as your production database. If you find a problem later on and need to revert to your backup, you will have lost work. I often don't use a modified database right away. I'll continue to use the production database for several days so I can continue to think about changes I made.

Rename your production database by adding a time stamp (YYY-MM-DD) to the end.

Copy the tested TEST.rmtree database to the folder where the production database is normally located.

Rename the TEST.rmtree database file to the usual name used for production.

Use the forum at [sqlitetoolsforrootsmagic](https://sqlitetoolsforrootsmagic.com/forum/forum/first-forum) to discuss your work and ask questions. 

# NOTES

## SQLite Expert Personal

Use the 64 bit version. The download page is at:\
<https://www.sqliteexpert.com/download.html>

The Personal version is free. The is also a paid Professional version, but it's not needed.

There are a number of other GUI and command line SQLite manager applications. SQLite Expert is the one I use to do development.

To run SQL scripts, I use the SQLite command line tool along with a script runner command script found in the Maintenance folder.


## Assessing safety of the unifuzz64.dll file
The download link for the unifuzz64.dll file is found in this context-\
https://sqlitetoolsforrootsmagic.com/rmnocase-faking-it-in-sqlite-expert-command-line-shell-et-al/

The SQLiteToolsforRootsMagic website has been around for years and
is run by a trusted RM user. Many posts to public RootsMagic user forums
mention use of unifuzz64.dll from the SQLiteToolsforRootsMagic website.

This is the file I have been using for years-\
----MD5 hash--------------------------------------File size------------File name\
----06a1f485b0fae62caa80850a8c7fd7c2-----256,406 bytes----unifuzz64.dll\


You can use the MD5 hash value to confirm you have the same file downloaded.

Instructions to compute the MD5 of a file can be found at-\
<https://portal.nutanix.com/page/documents/kbs/details?targetId=kA07V000000LWYqSAO\>


## The REINDEX RMNOCASE command and the "Rebuild indexes" tool

These commands are not usually needed if the database is only queried or if all the columns involved in update or insert sql statements aren't collated using RMNOCASE. 

Many queries can be written to override the use of RMNOCASE.

The fundamental issue is that the RMNOCASE collation provided by the SQLite extension unifuzz64.dll is not identical to the RMNOCASE collation provided by the RootsMagic app. 

see the document- [Notes on collation RMNOCASE](https://github.com/ricko2001/Genealogy-scripts/blob/main/Notes%20on%20collation%20RMNOCASE.md)

