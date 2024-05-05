---
title: Currents Bugs That Annoy Me and a Design Change Wish List
---

[Home](https://richardotter.github.io)

Last Updated:  2024-05-05

Applies to RootsMagic on Windows, x64 edition, v 9.1.4

# Bugs

## Media Tab

Left and right side panel selections in Media Tab not always synchronized.

## Add new media => Paste into field "Filename"

If the path is enclosed with quotes, as from File Manager Copy as path command, the path is pasted numerous times and the add fails.


## Text editing

Editing in both database fields and Note editor.\$##
Double click a word to select it, hit delete key to delete it => the cursor moves to incorrect location.

## Note editor

Assumes that typed text, e.g. &lt;b>, is formatting code.
Formatting codes should not be user enter-able in text mode. If formatting codes need to be visible, there should be a show formatting codes mode.

Without the separation of modes, there is a class of text that the user is not allowed to use.

## Fact description

All characters after a "&lt;" are not displayed in person edit main panel.

## Merge Citations

Open the Sources tab from the main window.\
Select any source.\
Open the selected source's list of citations.\
Select any citation.\
Select the Merge citations command from the three dot menu.\
A list of all of the citations belonging to the selected source is displayed. As expected.\
In the search box within the merge citations window, enter a broad search term, such as the letter 'a'.\
A much larger list of citations with with to merge is displayed, mostly from other sources.

Can one merge citations when they are from different sources? If only citations from sources based on the same Source Template were shown, that would make sense.

## Date entry

In RM preferences, one can choose “Use the system settings” for “Date entry”. However, if Windows short-date format is set to ISO,  RM still does not recognize ISO dates on input.

# Design Change Wish List

## RMNOCASE transparency

Either give a spec for a standalone collation sequence, 
or use an off the shelf standard collation.

## Groups and colors

Assign colors to group definitions so that members of a group are all highlighted with the assigned color.
Also define a conflict color when a person is in more than one group that has a color assigned. (Study how TMG does this. Much bettter.)

This should be the primary way of assigning a color to a person.
(The transition could be implemented in parallel with current color model to avoid shock to old time users)

## De-normalized data

Get rid of de-normalized birth and death columns in NameTable.

## Database indexes

Add unique indexes that will enforce only one Primary for each fact/name.
If possible, add some referential integrity constraints in SQLite.

## Fact Type selection dialog

Don't populate Fact type list with a query every time. Its too slow as is to keep up with keyboard entry.

## Sort children

Use Birth Sort date for arranging children on screen and in reports.

## Sort marriages

Use Marriage Sort date for arranging marriages on screen and in reports.

## Find person hot key

add a hot key (keyboard shortcut), that will shift focus to the person index without filtering. Or some other way that will guarentee the full index is searched- name name or RIN.

Currently-\
Control-F almost works, but the People List could be filtered.\
Control-S is not bad, but it is not an index, which has advantages over search.
