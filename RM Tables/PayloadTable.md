# PayloadTable

## DDL

CREATE TABLE PayloadTable (RecID INTEGER PRIMARY KEY, RecType INTEGER, OwnerType INTEGER, OwnerID INTEGER, Title TEXT, DataRec BLOB, UTCModDate FLOAT );

CREATE INDEX idxPayloadType ON PayloadTable (RecType);



## LIST

|#  | Name          | Type      |
|---|---------------|-----------|
1	| RecID			| INTEGER
2	| RecType		| INTEGER
3	| OwnerType		| INTEGER
4	| OwnerID		| INTEGER
5	| Title			| TEXT
6	| DataRec		| BLOB
7	| UTCModDate	| FLOAT


## NOTES

|#  | Name          | Note      |
|---|---------------|-----------|
1	| RecID			| 
2	| RecType		| 
3	| OwnerType		| 
4	| OwnerID		| 
5	| Title			| 
6	| DataRec		| 
7	| UTCModDate	| 


https://sqlitetoolsforrootsmagic.com/rm9-data-definitions/

PayloadTable
New table added in support of Saved Criteria Search and Saved Criteria Group. So far:

OwnerType
New OwnerType values have been added in support of the new tables. These will be identified as encountered through usage and testing.

Table	RecType	OwnerType	OwnerID	
Payload	1 (SavedCriteriaSearch)	8	0	
Payload	2 (SavedCriteriaGroup)	20	TagTable.TagValue, GroupTable.GroupID	
FANTable		19	CitationLinkTable, MediaLinkTable,…	

