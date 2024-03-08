# FamilyTable


## DDL

CREATE TABLE FamilyTable (FamilyID INTEGER PRIMARY KEY, FatherID INTEGER, MotherID INTEGER, ChildID INTEGER, HusbOrder INTEGER, WifeOrder INTEGER, IsPrivate INTEGER, Proof INTEGER, SpouseLabel INTEGER, FatherLabel INTEGER, MotherLabel INTEGER, SpouseLabelStr TEXT, FatherLabelStr TEXT, MotherLabelStr TEXT, Note TEXT, UTCModDate FLOAT );

CREATE INDEX idxFamilyMotherID ON FamilyTable (MotherID);

CREATE INDEX idxFamilyFatherID ON FamilyTable (FatherID);



## LIST

|#  | Name          | Type      |
|---|---------------|-----------|
1	| FamilyID			| INTEGER
2	| FatherID			| INTEGER
3	| MotherID			| INTEGER
4	| ChildID			| INTEGER
5	| HusbOrder			| INTEGER
6	| WifeOrder			| INTEGER
7	| IsPrivate			| INTEGER
8	| Proof				| INTEGER
9	| SpouseLabel		| INTEGER
10	| FatherLabel		| INTEGER
11	| MotherLabel		| INTEGER
12	| SpouseLabelStr	| TEXT
13	| FatherLabelStr	| TEXT
14	| MotherLabelStr	| TEXT
15	| Note				| TEXT
16	| UTCModDate		| FLOAT


## NOTES

|#  | Name          | Note      |
|---|---------------|-----------|
1	| FamilyID			| primary key
2	| FatherID			| ==> PersonTable.PersonID
3	| MotherID			| ==> PersonTable.PersonID
4	| ChildID			| ==> ChildTable.ChildID
5	| HusbOrder			| 
6	| WifeOrder			| 
7	| IsPrivate			| 
8	| Proof				| 
9	| SpouseLabel		| 
10	| FatherLabel		| 
11	| MotherLabel		| 
12	| SpouseLabelStr	| 
13	| FatherLabelStr	| 
14	| MotherLabelStr	| 
15	| Note				| 
16	| UTCModDate		| 



FatherID and MotherID may be 0, which means the person does not exist
(why not use null?)

There is not supposed to be a personID = 0 in PersonTable.

The FamilyTable.ChildID points to ?? first born  ??

More details- see ChildTable


