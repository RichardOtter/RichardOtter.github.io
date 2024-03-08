# ExclusionTable

## DDL

CREATE TABLE ExclusionTable (RecID INTEGER PRIMARY KEY, ExclusionType INTEGER, ID1 INTEGER, ID2 INTEGER, UTCModDate FLOAT );

CREATE UNIQUE INDEX idxExclusionIndex ON ExclusionTable (ExclusionType, ID1, ID2);


## LIST

|#  | Name          | Type      |
|---|---------------|-----------|
1	| RecID			| INTEGER
2	| ExclusionType	| INTEGER
3	| ID1			| INTEGER
4	| ID2			| INTEGER
5	| UTCModDate	| FLOAT


## NOTES

|#  | Name          | Note      |
|---|---------------|-----------|
1	| RecID			| 
2	| ExclusionType	| 
3	| ID1			| 
4	| ID2			| 
5	| UTCModDate	| 



Type
1		PersonID	PersonIPD		not a match
2		PersonID	problem flag to ignore

	problem flag to ignore


