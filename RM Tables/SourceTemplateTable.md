# SourceTemplateTable

## Table DDL

```
CREATE TABLE SourceTemplateTable (TemplateID INTEGER PRIMARY KEY, Name TEXT COLLATE RMNOCASE, Description TEXT, Favorite INTEGER, Category TEXT, Footnote TEXT, ShortFootnote TEXT, Bibliography TEXT, FieldDefs BLOB, UTCModDate FLOAT );

CREATE INDEX idxSourceTemplateName ON SourceTemplateTable (Name);
```

## Columns List

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | TemplateID    | INTEGER   |
| 2  | Name          | TEXT      |
| 3  | Description   | TEXT      |
| 4  | Favorite      | INTEGER   |
| 5  | Category      | TEXT      |
| 6  | Footnote      | TEXT      |
| 7  | ShortFootnote | TEXT      |
| 8  | Bibliography  | TEXT      |
| 9  | FieldDefs     | BLOB      |
| 10 | UTCModDate    | FLOAT     |

## Notes

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | TemplateID    | _PK
| 2  | Name          | _TEXT-SL
| 3  | Description   | _TEXT-SL
| 4  | Favorite      | 
| 5  | Category      | _TEXT-SL
| 6  | Footnote      | _TEXT-SL
| 7  | ShortFootnote | _TEXT-SL
| 8  | Bibliography  | _TEXT-SL
| 9  | FieldDefs     |  XML
| 10 | UTCModDate    | _STD



## Open Questions

How does Favorites int work
What format for category ?