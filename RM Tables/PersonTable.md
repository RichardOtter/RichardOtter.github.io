# PersonTable

## DDL

CREATE TABLE PersonTable (PersonID INTEGER PRIMARY KEY, UniqueID TEXT, Sex INTEGER, ParentID INTEGER, SpouseID INTEGER, Color INTEGER, Color1 INTEGER, Color2 INTEGER, Color3 INTEGER, Color4 INTEGER, Color5 INTEGER, Color6 INTEGER, Color7 INTEGER, Color8 INTEGER, Color9 INTEGER, Relate1 INTEGER, Relate2 INTEGER, Flags INTEGER, Living INTEGER, IsPrivate INTEGER, Proof INTEGER, Bookmark INTEGER, Note TEXT, UTCModDate FLOAT );


## LIST

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | PersonID      | INTEGER
| 2  | UniqueID      | TEXT
| 3  | Sex           | INTEGER
| 4  | ParentID      | INTEGER
| 5  | SpouseID      | INTEGER
| 6  | Color         | INTEGER
| 7  | Color1        | INTEGER
| 8  | Color2        | INTEGER
| 9  | Color3        | INTEGER
| 10 | Color4        | INTEGER
| 11 | Color5        | INTEGER
| 12 | Color6        | INTEGER
| 13 | Color7        | INTEGER
| 14 | Color8        | INTEGER
| 15 | Color9        | INTEGER
| 16 | Relate1       | INTEGER
| 17 | Relate2       | INTEGER
| 18 | Flags         | INTEGER
| 19 | Living        | INTEGER
| 20 | IsPrivate     | INTEGER
| 21 | Proof         | INTEGER
| 22 | Bookmark      | INTEGER
| 23 | Note          | TEXT
| 24 | UTCModDate    | FLOAT


## NOTES

| #  | Name          | Note      |
|----|---------------|-----------|
| 1  | PersonID      | Primary key     Many ==>
| 2  | UniqueID      | 
| 3  | Sex           | 
| 4  | ParentID      | 
| 5  | SpouseID      | 
| 6  | Color         | 
| 7  | Color1        | 
| 8  | Color2        | 
| 9  | Color3        | 
| 10 | Color4        | 
| 11 | Color5        | 
| 12 | Color6        | 
| 13 | Color7        | 
| 14 | Color8        | 
| 15 | Color9        | 
| 16 | Relate1       | 
| 17 | Relate2       | 
| 18 | Flags         | 
| 19 | Living        | 
| 20 | IsPrivate     | 
| 21 | Proof         | 
| 22 | Bookmark      | 
| 23 | Note          | 
| 24 | UTCModDate    | 

## QUESTIONS

````
No indexes created

PersonID PRIMARY KEY
UniqueID TEXT, Sex INTEGER

ParentID => FamilyID        primary set of parents (one to one) (used for report)
SpouseID => FamilyId        primary spouse (one to one)

ColorN        color id for the person

Relate1 0 -> 12 & 999 (7 o these)
Relate2 1 -> 12

Flags INTEGER

Living        1=yes, 0=no
IsPrivate not seen in UI
Proof        not seen in UI
Bookmark     used to see bookmarked people. Odd that there isn't a bookmark table
Note        person note
UTCModDate



There are a number of fields in PersonTable that can change for book keeping reasons. 
Data for person not changed. Do all changes update date edited field?

````