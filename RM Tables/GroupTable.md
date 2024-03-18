# GroupTable

## DDL

CREATE TABLE GroupTable (RecID INTEGER PRIMARY KEY, GroupID INTEGER, StartID INTEGER, EndID INTEGER, UTCModDate FLOAT );

## LIST

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | RecID         | INTEGER
| 2  | GroupID       | INTEGER
| 3  | StartID       | INTEGER
| 4  | EndID         | INTEGER
| 5  | UTCModDate    | FLOAT

## NOTES

| #  | Name          | Note      |
|----|---------------|-----------|
| 1  | RecID         | _PK
| 2  | GroupID       | ==> TagTable.TagValue
| 3  | StartID       | ==> PersonTable.PersonID
| 4  | EndID         | ==> PersonTable.PersonID
| 5  | UTCModDate    | 

## QUESTIONS

If the groups are only witterten by some code, then one can always use StartID == EndID
The table will be bigger, but who cares.

