# PlaceTable

## DDL

CREATE TABLE PlaceTable (PlaceID INTEGER PRIMARY KEY, PlaceType INTEGER, Name TEXT COLLATE RMNOCASE, Abbrev TEXT, Normalized TEXT, Latitude INTEGER, Longitude INTEGER, LatLongExact INTEGER, MasterID INTEGER, Note TEXT, Reverse TEXT COLLATE RMNOCASE, fsID INTEGER, anID INTEGER, UTCModDate FLOAT );

CREATE INDEX idxPlaceName ON PlaceTable (Name);

CREATE INDEX idxPlaceAbbrev ON PlaceTable (Abbrev);

CREATE INDEX idxReversePlaceName ON PlaceTable (Reverse);

## LIST

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | PlaceID       | INTEGER
| 2  | PlaceType     | INTEGER
| 3  | Name          | TEXT
| 4  | Abbrev        | TEXT
| 5  | Normalized    | TEXT
| 6  | Latitude      | INTEGER
| 7  | Longitude     | INTEGER
| 8  | LatLongExact  | INTEGER
| 9  | MasterID      | INTEGER
| 10 | Note          | TEXT
| 11 | Reverse       | TEXT
| 12 | fsID          | INTEGER
| 13 | anID          | INTEGER
| 14 | UTCModDate    | FLOAT


## NOTES

| #  | Name          | Note      |
|----|---------------|-----------|
| 1  | PlaceID       | _PK
| 2  | PlaceType     | 
| 3  | Name          | 
| 4  | Abbrev        | 
| 5  | Normalized    | 
| 6  | Latitude      | interger ??
| 7  | Longitude     | interger ??
| 8  | LatLongExact  | all 0            unimplemented
| 9  | MasterID      | for Place Details, gives Master place  ==>PlaceTable.PlaceID
| 10 | Note          | multi line text
| 11 | Reverse       | denormalized ? reverse Name for master place, not place detail
| 12 | fsID          | all NULL        unimplemented    FamilySearch place ID ?
| 13 | anID          | all NULL        unimplemented    Ancestry place ID ?
| 14 | UTCModDate    | standard

## QUESTIONS

What is LatLongExact
What id scale factor for Latitude/Longitude


