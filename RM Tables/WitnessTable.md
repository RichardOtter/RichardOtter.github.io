# WitnessTable

## DDL

CREATE TABLE WitnessTable (WitnessID INTEGER PRIMARY KEY, EventID INTEGER, PersonID INTEGER, WitnessOrder INTEGER, Role INTEGER, Sentence TEXT, Note TEXT, Given TEXT COLLATE RMNOCASE, Surname TEXT COLLATE RMNOCASE, Prefix TEXT COLLATE RMNOCASE, Suffix TEXT COLLATE RMNOCASE, UTCModDate FLOAT );

CREATE INDEX idxWitnessPersonID ON WitnessTable (PersonID);

CREATE INDEX idxWitnessEventID ON WitnessTable (EventID);

## LIST

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | WitnessID     | INTEGER
| 2  | EventID       | INTEGER
| 3  | PersonID      | INTEGER
| 4  | WitnessOrder  | INTEGER
| 5  | Role          | INTEGER
| 6  | Sentence      | TEXT
| 7  | Note          | TEXT
| 8  | Given         | TEXT
| 9  | Surname       | TEXT
| 10 | Prefix        | TEXT
| 11 | Suffix        | TEXT
| 12 | UTCModDate    | FLOAT

## NOTES

| #  | Name          | Note      |
|----|---------------|-----------|
| 1  | WitnessID     | _PK
| 2  | EventID       | ==> EventTable.EventID   fact that is witnessed
| 3  | PersonID      | ==> PersonTable.PersonID  person this is attached to,  ?? if 0, use name in this table ??
| 4  | WitnessOrder  | unimplemented        sort order
| 5  | Role          | ==>  RoleTable.RoleID
| 6  | Sentence      | ??? perhaps custom sentence instead of the RoleTable's sentence ?
| 7  | Note          | multi line text
| 8  | Given         | used for "just type in witness names"
| 9  | Surname       | used for "just type in witness names"
| 10 | Prefix        | used for "just type in witness names"
| 11 | Suffix        | used for "just type in witness names"
| 12 | UTCModDate    | standard

## QUESTIONS

````
Person edit window, list of items:
    events
    witnessed events
    names
    associations
    relative events (which events, which relatives?)

````
