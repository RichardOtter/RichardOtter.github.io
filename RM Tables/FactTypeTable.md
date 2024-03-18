# FactTypeTable

## DDL

CREATE TABLE FactTypeTable (FactTypeID INTEGER PRIMARY KEY, OwnerType INTEGER, Name TEXT COLLATE RMNOCASE, Abbrev TEXT, GedcomTag TEXT, UseValue INTEGER, UseDate INTEGER, UsePlace INTEGER, Sentence TEXT, Flags INTEGER, UTCModDate FLOAT );

CREATE INDEX idxFactTypeAbbrev ON FactTypeTable (Abbrev);

CREATE INDEX idxFactTypeGedcomTag ON FactTypeTable (GedcomTag);

CREATE INDEX idxFactTypeName ON FactTypeTable (Name);

## LIST

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | FactTypeID    | INTEGER
| 2  | OwnerType     | INTEGER
| 3  | Name          | TEXT
| 4  | Abbrev        | TEXT
| 5  | GedcomTag     | TEXT
| 6  | UseValue      | INTEGER
| 7  | UseDate       | INTEGER
| 8  | UsePlace      | INTEGER
| 9  | Sentence      | TEXT
| 10 | Flags         | INTEGER
| 11 | UTCModDate    | FLOAT

## NOTES

| #  | Name          | Note      |
|----|---------------|-----------|
| 1  | FactTypeID    | 
| 2  | OwnerType     | 
| 3  | Name          | 
| 4  | Abbrev        | 
| 5  | GedcomTag     | 
| 6  | UseValue      | 
| 7  | UseDate       | 
| 8  | UsePlace      | 
| 9  | Sentence      | 
| 10 | Flags         | 
| 11 | UTCModDate    | 

## QUESTIONS

