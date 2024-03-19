# MediaLinkTable

CREATE TABLE MediaLinkTable (LinkID INTEGER PRIMARY KEY, MediaID INTEGER, OwnerType INTEGER, OwnerID INTEGER, IsPrimary INTEGER, Include1 INTEGER, Include2 INTEGER, Include3 INTEGER, Include4 INTEGER, SortOrder INTEGER, RectLeft INTEGER, RectTop INTEGER, RectRight INTEGER, RectBottom INTEGER, Comments TEXT, UTCModDate FLOAT );

CREATE INDEX idxMediaOwnerID ON MediaLinkTable (OwnerID);

## Columns List

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | LinkID        | INTEGER   |
| 2  | MediaID       | INTEGER   |
| 3  | OwnerType     | INTEGER   |
| 4  | OwnerID       | INTEGER   |
| 5  | IsPrimary     | INTEGER   |
| 6  | Include1      | INTEGER   |
| 7  | Include2      | INTEGER   |
| 8  | Include3      | INTEGER   |
| 9  | Include4      | INTEGER   |
| 10 | SortOrder     | INTEGER   |
| 11 | RectLeft      | INTEGER   |
| 12 | RectTop       | INTEGER   |
| 13 | RectRight     | INTEGER   |
| 14 | RectBottom    | INTEGER   |
| 15 | Comments      | TEXT      |
| 16 | UTCModDate    | FLOAT     |

## Notes

| #  | Name          | Note      |
|----|---------------|-----------|
| 1  | LinkID        | _PK
| 2  | MediaID       | _FK ==> MultimediaTable.MediaID
| 3  | OwnerType     | _PFK-TYPE
| 4  | OwnerID       | _PFK
| 5  | IsPrimary     | _STD
| 6  | Include1      | 
| 7  | Include2      | 
| 8  | Include3      | 
| 9  | Include4      | 
| 10 | SortOrder     | _NOT_IMP except for person media gallery
| 11 | RectLeft      | _NOT-IMP
| 12 | RectTop       | _NOT-IMP
| 13 | RectRight     | _NOT-IMP
| 14 | RectBottom    | _NOT-IMP
| 15 | Comments      | _TEXT-ML
| 16 | UTCModDate    | _STD



## Open Questions

What are Include1  columns ?  TODO


