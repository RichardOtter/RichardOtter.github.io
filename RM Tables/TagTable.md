# TagTable

## DDL

CREATE TABLE TagTable (TagID INTEGER PRIMARY KEY, TagType INTEGER, TagValue INTEGER, TagName TEXT COLLATE RMNOCASE, Description TEXT, UTCModDate FLOAT );

CREATE INDEX idxTagType ON TagTable (TagType);

## LIST

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | TagID         | INTEGER
| 2  | TagType       | INTEGER
| 3  | TagValue      | INTEGER
| 4  | TagName       | TEXT
| 5  | Description   | TEXT
| 6  | UTCModDate    | FLOAT

## NOTE
 
| #  | Name          | Note      |
|----|---------------|-----------|
| 1  | TagID         | _PK
| 2  | TagType       | 
| 3  | TagValue      | 
| 4  | TagName       | 
| 5  | Description   | 
| 6  | UTCModDate    | 

## QUESTIONS

````
Look up

TagType
0    Names of Groups
1    Task Folder Names


TagValue        TODO  
                GroupID in GrouoTable points to TagValue, not TagID


TagName            simple name
Description        explanation of name
UTCModDate        mod julian date set for each write
````
