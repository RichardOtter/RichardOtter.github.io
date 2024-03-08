# PersonTable

## DDL

CREATE TABLE PersonTable (PersonID INTEGER PRIMARY KEY, UniqueID TEXT, Sex INTEGER, ParentID INTEGER, SpouseID INTEGER, Color INTEGER, Color1 INTEGER, Color2 INTEGER, Color3 INTEGER, Color4 INTEGER, Color5 INTEGER, Color6 INTEGER, Color7 INTEGER, Color8 INTEGER, Color9 INTEGER, Relate1 INTEGER, Relate2 INTEGER, Flags INTEGER, Living INTEGER, IsPrivate INTEGER, Proof INTEGER, Bookmark INTEGER, Note TEXT, UTCModDate FLOAT );

## DESIGN

RecNo	FieldName	SQLType	Size	Scale	PKDisplay	DefaultValue	NotNull	NotNullConflictClause	Unique	UniqueConflictClause	CollateValue	GeneratedExpr	GeneratedStorage	FKDisplay
1	PersonID	INTEGER			True		False		False					
2	UniqueID	TEXT			False		False		False					
3	Sex	INTEGER			False		False		False					
4	ParentID	INTEGER			False		False		False					
5	SpouseID	INTEGER			False		False		False					
6	Color	INTEGER			False		False		False					
7	Color1	INTEGER			False		False		False					
8	Color2	INTEGER			False		False		False					
9	Color3	INTEGER			False		False		False					
10	Color4	INTEGER			False		False		False					
11	Color5	INTEGER			False		False		False					
12	Color6	INTEGER			False		False		False					
13	Color7	INTEGER			False		False		False					
14	Color8	INTEGER			False		False		False					
15	Color9	INTEGER			False		False		False					
16	Relate1	INTEGER			False		False		False					
17	Relate2	INTEGER			False		False		False					
18	Flags	INTEGER			False		False		False					
19	Living	INTEGER			False		False		False					
20	IsPrivate	INTEGER			False		False		False					
21	Proof	INTEGER			False		False		False					
22	Bookmark	INTEGER			False		False		False					
23	Note	TEXT			False		False		False					
24	UTCModDate	FLOAT			False		False		False					


## LIST

| #     | Name          | Type      |
|-------|---------------|-----------|
1	| PersonID	| INTEGER
2	| UniqueID	| TEXT
3	| Sex			| INTEGER
4	| ParentID	| INTEGER
5	| SpouseID	| INTEGER
6	| Color		| INTEGER
7	| Color1		| INTEGER
8	| Color2		| INTEGER
9	| Color3		| INTEGER
10	| Color4		| INTEGER
11	| Color5		| INTEGER
12	| Color6		| INTEGER
13	| Color7		| INTEGER
14	| Color8		| INTEGER
15	| Color9		| INTEGER
16	| Relate1		| INTEGER
17	| Relate2		| INTEGER
18	| Flags		| INTEGER
19	| Living		| INTEGER
20	| IsPrivate	| INTEGER
21	| Proof		| INTEGER
22	| Bookmark	| INTEGER
23	| Note		| TEXT
24	| UTCModDate	| FLOAT


## NOTES

No indexes created

PersonID PRIMARY KEY
UniqueID TEXT, Sex INTEGER

ParentID => FamilyID		primary set of parents (one to one) (used for report)
SpouseID => FamilyId		primary spouse (one to one)

ColorN		color id for the person

Relate1 0 -> 12 & 999 (7 o these)
Relate2 1 -> 12

Flags INTEGER

Living		1=yes, 0=no
IsPrivate not seen in UI
Proof		not seen in UI
Bookmark 	used to see bookmarked people. Odd that there isn't a bookmark table
Note		person note
UTCModDate


## QUESTIONS

There are a number of fields in PersonTable that can change for book keeping reasons. 
Data for person not changed. Do all changes update date edited field?
