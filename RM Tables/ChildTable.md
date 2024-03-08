# ChildTable

## DDL

CREATE TABLE ChildTable (RecID INTEGER PRIMARY KEY, ChildID INTEGER, FamilyID INTEGER, RelFather INTEGER, RelMother INTEGER, ChildOrder INTEGER, IsPrivate INTEGER, ProofFather INTEGER, ProofMother INTEGER, Note TEXT, UTCModDate FLOAT );

CREATE INDEX idxChildOrder ON ChildTable (ChildOrder);

CREATE INDEX idxChildID ON ChildTable (ChildID);

CREATE INDEX idxChildFamilyID ON ChildTable (FamilyID);


## LIST

|#  | Name          | Type      |
|---|---------------|-----------|
1	| RecID			| INTEGER
2	| ChildID		| INTEGER
3	| FamilyID		| INTEGER
4	| RelFather		| INTEGER
5	| RelMother		| INTEGER
6	| ChildOrder	| INTEGER
7	| IsPrivate		| INTEGER
8	| ProofFather	| INTEGER
9	| ProofMother	| INTEGER
10	| Note			| TEXT
11	| UTCModDate	| FLOAT


## NOTES

|#  | Name          | Type      |
|---|---------------|-----------|
1	| RecID			| INTEGER
2	| ChildID		| INTEGER
3	| FamilyID		| INTEGER
4	| RelFather		| INTEGER
5	| RelMother		| INTEGER
6	| ChildOrder	| INTEGER
7	| IsPrivate		| INTEGER
8	| ProofFather	| INTEGER
9	| ProofMother	| INTEGER
10	| Note			| TEXT
11	| UTCModDate	| FLOAT


ChildTable
Column names are a bit off-standard
ChildID is not the primary key of this table, RecID is.


RecID		is the primary key
ChildID		ChildTable.ChildID ==> PersonTable.PersonID
			don't have to Join It is a PersonID

FamilyID	ChildTable.FamilyID ==> FamilyTable.FamilyID
			don't have to Join It is a FamilyID

The ChildTable and FamilyTable are the basis for all family relationships



Note that there is a separate proof value for father & mother
ProofFather INTEGER
ProofMother INTEGER

RelFather		relationship type
RelMother

Lookups

    	Rel values
    0	Birth
    1	Adopted
    2	Step
    3	Foster
    4	Related
    5	Guardian
    6	Sealed
    7	Unknown




ChildOrder	for records pointing to the same FamilyID, gives order within set

ChildTable is a link table between Family and person
not really because ChildTable has PersonID. so no need to use the Person Table directly
ChildTable is a link table between FamilyTable and itself (ft)

----------------------------------------------------
How to link parents and offspring- general question

Don't just use person table and family table.
That would limit each person to just one family. (set of parents)
Actual method allows multiple families for a person. 
e.g. birth & adopted families
&    OK multiple families of the same type, say 2 candidate for birth father.

A single Person can point to multiple ChildTable entries.
PersonTable.PersonID => ChildTable.ChildID *1) and  ChildTable.ChildID *2)
    Each ChildTable entry points to a family.

----------------------------------------------------


===========================================DIV50==
QUESTIONS

