# FANTable

## DDL

CREATE TABLE FANTable (FanID INTEGER PRIMARY KEY, ID1 INTEGER, ID2 INTEGER, FanTypeID INTEGER, PlaceID INTEGER, SiteID INTEGER, Date TEXT, SortDate BIGINT, Description TEXT, Note TEXT, UTCModDate FLOAT );

CREATE INDEX idxFanId2 ON FANTable (ID2);

CREATE INDEX idxFanId1 ON FANTable (ID1);



## LIST

|#  | Name          | Type      |
|---|---------------|-----------|
1	| FanID			| INTEGER
2	| ID1			| INTEGER
3	| ID2			| INTEGER
4	| FanTypeID		| INTEGER
5	| PlaceID		| INTEGER
6	| SiteID		| INTEGER
7	| Date			| TEXT
8	| SortDate		| BIGINT
9	| Description	| TEXT
10	| Note			| TEXT
11	| UTCModDate	| FLOAT

## NOTES

|#  | Name          | Note      |
|---|---------------|-----------|
1	| FanID			| primary key
2	| ID1			| ==> PersonTable.PersonID
3	| ID2			| ==> PersonTable.PersonID
4	| FanTypeID		| 
5	| PlaceID		| 
6	| SiteID		| 
7	| Date			| 
8	| SortDate		| standard
9	| Description	| one line text
10	| Note			| multi-line text
11	| UTCModDate	| standard



## QUESTIONS



