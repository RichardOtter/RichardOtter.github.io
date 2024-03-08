# URLTable

# DDL

CREATE TABLE URLTable (LinkID INTEGER PRIMARY KEY, OwnerType INTEGER, OwnerID INTEGER, LinkType INTEGER, Name TEXT, URL TEXT, Note TEXT, UTCModDate FLOAT );


## LIST

| #     | Name          | Type      |
|-------|---------------|-----------|
1		| LinkID		| INTEGER
2		| OwnerType		| INTEGER
3		| OwnerID		| INTEGER
4		| LinkType		| INTEGER
5		| Name			| TEXT
6		| URL			| TEXT
7		| Note			| TEXT
8		| UTCModDate	| FLOAT

## NOTES

| #     | Name          | Note      |
|-------|---------------|-----------|
1		| LinkID		| 
2		| OwnerType		| 
3		| OwnerID		| 
4		| LinkType		| always 0 ?
5		| Name			| 
6		| URL			| 
7		| Note			| 
8		| UTCModDate	| 



Lookup

OwnerType

0	Person
1	not used
2	not used
3	Source
4	Citation
5	place ?
>5	not used

## QUESTIONS
