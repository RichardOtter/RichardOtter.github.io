# FactTypeTable

## Table DDL

```
CREATE TABLE FactTypeTable (FactTypeID INTEGER PRIMARY KEY, OwnerType INTEGER, Name TEXT COLLATE RMNOCASE, Abbrev TEXT, GedcomTag TEXT, UseValue INTEGER, UseDate INTEGER, UsePlace INTEGER, Sentence TEXT, Flags INTEGER, UTCModDate FLOAT );

CREATE INDEX idxFactTypeAbbrev ON FactTypeTable (Abbrev);

CREATE INDEX idxFactTypeGedcomTag ON FactTypeTable (GedcomTag);

CREATE INDEX idxFactTypeName ON FactTypeTable (Name);
```

## Columns List

| #   | Name       | Type    |
| --- | ---------- | ------- |
| 1   | FactTypeID | INTEGER |
| 2   | OwnerType  | INTEGER |
| 3   | Name       | TEXT    |
| 4   | Abbrev     | TEXT    |
| 5   | GedcomTag  | TEXT    |
| 6   | UseValue   | INTEGER |
| 7   | UseDate    | INTEGER |
| 8   | UsePlace   | INTEGER |
| 9   | Sentence   | TEXT    |
| 10  | Flags      | INTEGER |
| 11  | UTCModDate | FLOAT   |

## Notes

| #   | Name       | Note     |
| --- | ---------- | -------- |
| 1   | FactTypeID | _PK      |
| 2   | OwnerType  |          |
| 3   | Name       | _TEXT-SL |
| 4   | Abbrev     | _TEXT-SL |
| 5   | GedcomTag  | _TEXT-SL |
| 6   | UseValue   |          |
| 7   | UseDate    |          |
| 8   | UsePlace   | _TEXT-SL |
| 9   | Sentence   | _TEXT-SL |
| 10  | Flags      |          |
| 11  | UTCModDate | _STD     |

## Open Questions

