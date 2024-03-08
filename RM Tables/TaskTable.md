# TaskTable

## DDL

CREATE TABLE TaskTable (TaskID INTEGER PRIMARY KEY, TaskType INTEGER, RefNumber TEXT, Name TEXT COLLATE RMNOCASE, Status INTEGER, Priority INTEGER, Date1 TEXT, Date2 TEXT, Date3 TEXT, SortDate1 BIGINT, SortDate2 BIGINT, SortDate3 BITINT, Filename TEXT, Details TEXT, Results TEXT, UTCModDate FLOAT, Exclude INTEGER );

CREATE INDEX idxTaskName ON TaskTable (Name);



## LIST

| #     | Name          | Type      |
|-------|---------------|-----------|
1		| TaskID		| INTEGER
2		| TaskType		| INTEGER
3		| RefNumber		| TEXT
4		| Name			| TEXT
5		| Status		| INTEGER
6		| Priority		| INTEGER
7		| Date1			| TEXT
8		| Date2			| TEXT
9		| Date3			| TEXT
10		| SortDate1		| BIGINT
11		| SortDate2		| BIGINT
12		| SortDate3		| BITINT
13		| Filename		| TEXT
14		| Details		| TEXT
15		| Results		| TEXT
16		| UTCModDate	| FLOAT
17		| Exclude		| INTEGER

## NOTES

| #     | Name          | Note      |
|-------|---------------|-----------|
1		| TaskID		| 
2		| TaskType		| 
3		| RefNumber		| 
4		| Name			| 
5		| Status		| 
6		| Priority		| 
7		| Date1			| 
8		| Date2			| 
9		| Date3			| 
10		| SortDate1		| BIGINT	not std dates or sort dates
11		| SortDate2		| BIGINT	not std dates or sort dates
12		| SortDate3		| BIGINT	not std dates or sort dates
13		| Filename		| A path to a file, absolute path.
Not connected to media gallery
14		| Details		| 
15		| Results		| 
16		| UTCModDate	| 
17		| Exclude		| 


Lookup



Task type
0		<blank>
1		Research
2		To-Do
3		Correspondence

Status		INTEGER
0		New
1		In progress
2		Completed
3		On hold
4		Problem
5		Canceled

Priority		INTEGER
0		1 (Highest)
1		2 (Very high)
2		3 (High)
3		4 (Med high)
4		5 (Medium)
5		6 (Med low)
6		7 (Low)
7		8 (Very low)
8		9 (Lowest)


## QUESTIONS
