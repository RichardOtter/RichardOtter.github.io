# SourceTemplateTable

## DDL

CREATE TABLE SourceTemplateTable (TemplateID INTEGER PRIMARY KEY, Name TEXT COLLATE RMNOCASE, Description TEXT, Favorite INTEGER, Category TEXT, Footnote TEXT, ShortFootnote TEXT, Bibliography TEXT, FieldDefs BLOB, UTCModDate FLOAT );

CREATE INDEX idxSourceTemplateName ON SourceTemplateTable (Name);

## LIST

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | TemplateID    | INTEGER
| 2  | Name          | TEXT
| 3  | Description   | TEXT
| 4  | Favorite      | INTEGER
| 5  | Category      | TEXT
| 6  | Footnote      | TEXT
| 7  | ShortFootnote | TEXT
| 8  | Bibliography  | TEXT
| 9  | FieldDefs     | BLOB
| 10 | UTCModDate    | FLOAT

## NOTES

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | TemplateID    | _PK
| 2  | Name          | 
| 3  | Description   | 
| 4  | Favorite      | 
| 5  | Category      | 
| 6  | Footnote      | 
| 7  | ShortFootnote | 
| 8  | Bibliography  | 
| 9  | FieldDefs     | 
| 10 | UTCModDate    | 

## QUESTIONS

