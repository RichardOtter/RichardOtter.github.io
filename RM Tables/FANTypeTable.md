# FANTypeTable

## DDL

CREATE TABLE FANTypeTable (FANTypeID INTEGER PRIMARY KEY, Name TEXT COLLATE RMNOCASE, Role1 TEXT, Role2 TEXT, Sentence1 TEXT, Sentence2 TEXT, UTCModDate FLOAT );

CREATE INDEX idxFANTypeName ON FANTypeTable (Name);

## LIST

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | FANTypeID     | INTEGER
| 2  | Name          | TEXT
| 3  | Role1         | TEXT
| 4  | Role2         | TEXT
| 5  | Sentence1     | TEXT
| 6  | Sentence2     | TEXT
| 7  | UTCModDate    | FLOAT
 
## NOTES

| #  | Name          | Note      |
|----|---------------|-----------|
| 1  | FANTypeID     | _PK
| 2  | Name          | 
| 3  | Role1         | 
| 4  | Role2         | 
| 5  | Sentence1     | 
| 6  | Sentence2     | 
| 7  | UTCModDate    | 

## QUESTIONS
