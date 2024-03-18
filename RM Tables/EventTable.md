# EventTable

## DDL

CREATE TABLE EventTable (EventID INTEGER PRIMARY KEY, EventType INTEGER, OwnerType INTEGER, OwnerID INTEGER, FamilyID INTEGER, PlaceID INTEGER, SiteID INTEGER, Date TEXT, SortDate BIGINT, IsPrimary INTEGER, IsPrivate INTEGER, Proof INTEGER, Status INTEGER, Sentence TEXT, Details TEXT, Note TEXT, UTCModDate FLOAT );

CREATE INDEX idxOwnerEvent ON EventTable (OwnerID,EventType);

CREATE INDEX idxOwnerDate ON EventTable (OwnerID,SortDate);

## LIST

| #  | Name            | Type      |
|----|-----------------|-----------|
| 1  |    EventID      |  INTEGER    |
| 2  |    EventType    |  INTEGER    |
| 3  |    OwnerType    |  INTEGER    |
| 4  |    OwnerID      |  INTEGER    |
| 5  |    FamilyID     |  INTEGER    |
| 6  |    PlaceID      |  INTEGER    |
| 7  |    SiteID       |  INTEGER    |
| 8  |    Date         |  TEXT        |
| 9  |    SortDate     |  BIGINT    |
| 10 |    IsPrimary    |  INTEGER    |
| 11 |    IsPrivate    |  INTEGER    |
| 12 |    Proof        |  INTEGER    |
| 13 |    Status       |  INTEGER    |
| 14 |    Sentence     |  TEXT        |
| 15 |    Details      |  TEXT        |
| 16 |    Note         |  TEXT        |
| 17 |    UTCModDate   |  FLOAT    |


## NOTES

| #  | Name            | Note      |
|----|-----------------|-----------|
| 1  |    EventID      | _PK
| 2  |    EventType    | ==> FactTypeTable.FactTypeID
| 3  |    OwnerType    | 0 for person fact, 1 for family fact
| 4  |    OwnerID      | PersonTable.PersonID  or  FamilyTable.FamilyID
| 5  |    FamilyID     | always 0   not used ?
| 6  |    PlaceID      | ==> PlaceTable.PlaceID
| 7  |    SiteID       | place detail? , mostly 0, many in same range as PlaceID, 13000 are -1 along with -1 for PlaceID  Probably fact that does not have a place,     import from TMG artifact
| 8  |    Date         | standard
| 9  |    SortDate     | standard
| 10 |    IsPrimary    | 
| 11 |    IsPrivate    | 
| 12 |    Proof        | 0, 1, 2, 3
| 13 |    Status       | always 0    unimplemented
| 14 |    Sentence     | if not null, use this as sentence for fact
| 15 |    Details      | single line text
| 16 |    Note         | multi line text
| 17 |    UTCModDate   | standard

## QUESTIONS

``

Lookups

IsPrimary

    0 = no
    1 = yes

IsPrivate

    0 = no
    1 = yes

Proof

    0  not set
    1  Proven
    2  Disproven
    3  Disputed

OwnerEventType

    0 person event
    1 family event

This is redundant with the EventType which also says what kind of event it is.

```