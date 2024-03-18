# MediaLinkTable

CREATE TABLE MediaLinkTable (LinkID INTEGER PRIMARY KEY, MediaID INTEGER, OwnerType INTEGER, OwnerID INTEGER, IsPrimary INTEGER, Include1 INTEGER, Include2 INTEGER, Include3 INTEGER, Include4 INTEGER, SortOrder INTEGER, RectLeft INTEGER, RectTop INTEGER, RectRight INTEGER, RectBottom INTEGER, Comments TEXT, UTCModDate FLOAT );

CREATE INDEX idxMediaOwnerID ON MediaLinkTable (OwnerID);

## LIST

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | LinkID        | INTEGER
| 2  | MediaID       | INTEGER
| 3  | OwnerType     | INTEGER
| 4  | OwnerID       | INTEGER
| 5  | IsPrimary     | INTEGER
| 6  | Include1      | INTEGER
| 7  | Include2      | INTEGER
| 8  | Include3      | INTEGER
| 9  | Include4      | INTEGER
| 10 | SortOrder     | INTEGER
| 11 | RectLeft      | INTEGER
| 12 | RectTop       | INTEGER
| 13 | RectRight     | INTEGER
| 14 | RectBottom    | INTEGER
| 15 | Comments      | TEXT
| 16 | UTCModDate    | FLOAT

## NOTES

| #  | Name          | Note      |
|----|---------------|-----------|
| 1  | LinkID        | _PK
| 2  | MediaID       | 
| 3  | OwnerType     | 
| 4  | OwnerID       | 
| 5  | IsPrimary     | 
| 6  | Include1      | 
| 7  | Include2      | 
| 8  | Include3      | 
| 9  | Include4      | 
| 10 | SortOrder     | mostly unimplemented except for person's media gallery
| 11 | RectLeft      | unimplemented        Cropping point
| 12 | RectTop       | unimplemented        Cropping point
| 13 | RectRight     | unimplemented        Cropping point
| 14 | RectBottom    | unimplemented        Cropping point
| 15 | Comments      | 
| 16 | UTCModDate    | standard

## QUESTIONS



Lookups

OwnerType


