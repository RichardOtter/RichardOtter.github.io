# AddressTable

## DDL

CREATE TABLE AddressTable (AddressID INTEGER PRIMARY KEY, AddressType INTEGER, Name TEXT COLLATE RMNOCASE, Street1 TEXT, Street2 TEXT, City TEXT, State TEXT, Zip TEXT, Country TEXT, Phone1 TEXT, Phone2 TEXT, Fax TEXT, Email TEXT, URL TEXT, Latitude INTEGER, Longitude INTEGER, Note TEXT, UTCModDate FLOAT );

CREATE INDEX idxAddressName ON AddressTable (Name);

## Columns List

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | AddressID     | INTEGER
| 2  | AddressType   | INTEGER
| 3  | Name          | TEXT
| 4  | Street1       | TEXT
| 5  | Street2       | TEXT
| 6  | City          | TEXT
| 7  | State         | TEXT
| 8  | Zip           | TEXT
| 9  | Country       | TEXT
| 10 | Phone1        | TEXT
| 11 | Phone2        | TEXT
| 12 | Fax           | TEXT
| 13 | Email         | TEXT
| 14 | URL           | TEXT
| 15 | Latitude      | INTEGER
| 16 | Longitude     | INTEGER
| 17 | Note          | TEXT
| 18 | UTCModDate    | FLOAT

## Notes

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | AddressID     | _PK
| 2  | AddressType   | 
| 3  | Name          | 
| 4  | Street1       | 
| 5  | Street2       | 
| 6  | City          | 
| 7  | State         | 
| 8  | Zip           | 
| 9  | Country       | 
| 10 | Phone1        | 
| 11 | Phone2        | 
| 12 | Fax           | 
| 13 | Email         | 
| 14 | URL           | 
| 15 | Latitude      | 
| 16 | Longitude     | 
| 17 | Note          | 
| 18 | UTCModDate    | _STD

## Open Questions
