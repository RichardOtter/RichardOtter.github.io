# RoleTable

## DDL

CREATE TABLE RoleTable (RoleID INTEGER PRIMARY KEY, RoleName TEXT COLLATE RMNOCASE, EventType INTEGER, RoleType INTEGER, Sentence TEXT, UTCModDate FLOAT );

CREATE INDEX idxRoleEventType ON RoleTable (EventType);

## Columns List

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | RoleID        | INTEGER   |
| 2  | RoleName      | TEXT      |
| 3  | EventType     | INTEGER   |
| 4  | RoleType      | INTEGER   |
| 5  | Sentence      | TEXT      |
| 6  | UTCModDate    | FLOAT     |

## Notes

| #  | Name          | Note      |
|----|---------------|-----------|
| 1  | RoleID        | _PK
| 2  | RoleName      | 
| 3  | EventType     | 
| 4  | RoleType      | 
| 5  | Sentence      | 
| 6  | UTCModDate    | _STD



## Open Questions
