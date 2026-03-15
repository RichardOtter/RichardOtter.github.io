---
title: Current Bugs That Annoy Me and a Design Change Wish List
---

[Home](https://richardotter.github.io)

Last Updated:  2026-03-15

Applies to RootsMagic on Windows, x64 edition, v 11.0.4

# Bugs

## Fact Type selection dialog

In Edit Person window, click on the + button to add a fact.
Enter some random text in the filter so that no facts are displayed.
Hit the OK button
A new fact is added but of type 0. A fact type of 0 is undefined.
The Fact panel will show a somewhat random fact type
but when it is saved, it will display as blank.

Suggestion: Don't populate Fact type list with a query every time. Its too slow
as is to keep up with keyboard entry.

## Data loss when entering Fact data

A common workflow will result in data loss:
Open any database, or create new one.
Open any person or create a new one.
In the Edit Person window, click the + button to add any fact. In the new fact,
add data to any or all of the fields (date, description, place, place detail,
proof, primary, private). Without clicking the "check mark" button, add a
Source, Media,  Task, or fact Share. When done, use the Close button to exist
the Edit Person window.

Reopen the Person and the new Fact. Notice that any data in date, description,
place, place detail, proven, primary, private is lost.

**Same problem** when adding an Alt Name.

The data was saved in earlier post 7 versions.

Workaround:

* after entering data in the Fact or Name fields, click the Check Mark button.
* after entering a Source, Media,  Task, or Share, use the < button to display
  the Fact/Name data before using the Close button.
* after entering a Source, Media,  Task, or Share, click on a different Fact on
  the screen.

If in doubt, look at the main fact listing in the edit window. If the new fact
is blank, nothing has been saved.

## The 'Pop Under' window bug

The RootsMagic "pop-under" problem has existed since version 8. I have seen this
problem on 3 different Windows computers, 2 of which had factory installs of the
OS. They each had very different video subsystems and drivers. Messages about
the issue appear at a steady rate in the support forums. No other applications
show this behavior.

This may be an issue with the RM application framework that RM Inc can't control,
but that's not clear.

The problem manifests when a RootsMagic window changes its z-order, displaying
below other RM windows on the desktop. It is a bug because RM can't deal with
restoring the window to the top. One needs an OS function to do that. I find
that clicking the RM icon on the Windows Explorer task bar always works. For
instance the "Add Citation" window will pop to the bottom. Clicking on any other
RM window generates a beep and nothing else. One can't move the Add Citation
window below others because it is a modal window that should always stay on top.
The problem mostly (but not exclusively) occurs for me when rapidly switching
between Chrome and RM in copy and pasting operations.

This the biggest software factor in slowing down my research.

## Media Tab

Left and right side panel selections in Media Tab not always synchronized.

Workaround:
If the left and right side are not synchronized-
Right click the mouse on the left side image.
This will display the context menu and synchronize the right side.
Left click the mouse anywhere else on the window to dismiss the context menu.

## Note editor

Assumes that typed text, e.g. &lt;b>, is formatting code.
Formatting codes should not be user enter-able in text mode. If formatting codes
need to be visible, there should be a "show formatting codes" mode.

Without the separation of modes, there is a class of text that the user is not
allowed to use.

## Fact description

All characters after a "<" character are not displayed in person edit main
panel.\
This is also true in DNA Label2 field. Probably others as well.

## Merge Citations

Open the Sources tab from the main window.\
Select any source.\
Open the selected source's list of citations.\
Select any citation.\
Select the Merge citations command from the three dot menu.\
A list of all of the citations belonging to the selected source is displayed.
As expected.\
In the search box within the merge citations window, enter a broad search term,
such as the letter 'a'.\
A much larger list of citations with with to merge is displayed, mostly from
other sources.

Can one merge citations when they are from different sources? If only citations
from sources based on the same Source Template were shown, that would make
sense.

## Date entry

In RM preferences, one can choose “Use the system settings” for “Date entry”.
However, if Windows short-date format is set to ISO  (YYY-MM-DD),  RM still does
not recognize ISO 8601 dates on input.

## UTCModDate in the PersonTable

Some RM code is still updating this as an integer giving only day level precision.
Fix it so that the usual floating point number is inserted.

# Design-Change Wish List

Features I wish were differently implemented.

## Add new media => Paste into field "Filename"

If the path is enclosed with quotes, as from File Manager Copy as path command,
the path is pasted numerous times and the add fails. Workaround is to remove the
initial and ending quotes.

## Groups and colors

Assign colors to group definitions so that members of a group are all
highlighted with the assigned color. 

Also define a conflict color when a person is in more than one group that has a
color assigned. (Study how TMG does this. Much better.)

This should be the primary way of assigning a color to a person. (The transition
could be implemented in parallel with current color model to avoid shock to old
time users)

## De-normalized data

Get rid of de-normalized birth and death columns in NameTable. Causes continual
tech support questions when they get out of synch.

## Data constraints

Add unique indexes that will enforce only one Primary for each fact/name. Add
some referential integrity constraints in SQLite, especially foreign person
fields of value 0.

## Sort children

Use Birth Sort date for arranging children on screen and in reports.

## Sort marriages

Use Marriage Sort date for arranging marriages on screen and in reports.

## RMNOCASE transparency

Either give a spec for a standalone collation sequence,
or use an off the shelf standard collation.

## Find person hot key

add a hot key (keyboard shortcut), that will shift focus to the person index
without filtering.
Or some other way that will guarantee the full index is searched- name name or RIN.

Currently-\
Control-F almost works, but the People List could be filtered.\
Control-S is not bad, but it is not an index, which has advantages over search.

## Share a Fact #1

Using the RootsMagic explorer can be time consuming. I generally display
people's RIN and use that to find the person in the RootsMagic explorer. Why do
I need to look at the screen, note and remember the RIN of the person I want to
share to and then type it in. I should just be able to point to anyone on screen
and have the fact shared to that person.

# New Feature Wishes

## Add additional sort options
Add a sort option to most views that allows sorting by UTCModDate or Primary
key (order entered.)

## Allow use of an external editor instead of the Note editor

## Expose Primary Keys

Add an option so that when a control key is held and mouse hovers over a record,
that record's primary database key is displayed. Cold be hidden for RM internal
use and disclosed on case by case.

## Allow command line options

I would like to specify the database to open on a command line.
 
## Add an AI assisted option to look for possible duplicates in Places List


