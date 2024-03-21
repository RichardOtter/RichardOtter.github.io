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
| 2   | OwnerType  | LOOKUP   |
| 3   | Name       | _TEXT-SL |
| 4   | Abbrev     | _TEXT-SL |
| 5   | GedcomTag  | _TEXT-SL |
| 6   | UseValue   | _01-FLAG |
| 7   | UseDate    | _01-FLAG |
| 8   | UsePlace   | _01-FLAG |
| 9   | Sentence   | _TEXT-SL |
| 10  | Flags      |          |
| 11  | UTCModDate | _STD     |


UseValue, UseDate, UsePlace are yes no type flags that determine
whether the corresponding fields are displayed in th GUI when 
editing and displaying a fact of this type.

Sentence is the default narrative sentence template used by this fact type.

Flags are involved in which repprts the fact type is used in.
Most records have a -1.
Asscoiation fact has a very hight flag value  TODO
Values seen in a database-
-1
-64
-31
-4
-25
-32
2147483647

## Lookup Tables

| OwnerType | object            |
| --------- | ----------------- |
| 0         | individual fact   |
| 1         | famil/couple fact |

UseValue, UseDate, UsePlace are 0/1 flags no/yes

## Open Questions

Flags are involved in which repprts the fact type is used in.
Asscoiation fact has a very hight flag value  TODO

### DONE 1
