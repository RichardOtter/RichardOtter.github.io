# CitationLinkTable

## DDL

CREATE TABLE CitationLinkTable (LinkID INTEGER PRIMARY KEY, CitationID INTEGER, OwnerType INTEGER, OwnerID INTEGER, SortOrder INTEGER, Quality TEXT, IsPrivate INTEGER, Flags INTEGER, UTCModDate FLOAT );

CREATE INDEX idxCitationLinkOwnerID ON CitationLinkTable (OwnerID);

## LIST

| #   | Name          | Type      |
|-----|---------------|-----------|
|  1  | LinkID        | INTEGER
|  2  | CitationID    | INTEGER
|  3  | OwnerType     | INTEGER
|  4  | OwnerID       | INTEGER
|  5  | SortOrder     | INTEGER
|  6  | Quality       | TEXT
|  7  | IsPrivate     | INTEGER
|  8  | Flags         | INTEGER
|  9  | UTCModDate    | FLOAT

## NOTES

| #   | Name          | Note      |
|-----|---------------|-----------|
|  1  | LinkID        | _PK
|  2  | CitationID    | 
|  3  | OwnerType     | 
|  4  | OwnerID       | 
|  5  | SortOrder     | SortOrder
|  6  | Quality       | 
|  7  | IsPrivate     | 
|  8  | Flags         | 
|  9  | UTCModDate    | standard

## QUESTIONS

```
Lookups
OwnerType is one of 
0    link to a person            PersonTable.PersonID
1    link to a family            FamilyTable.FamilyID
2    link to a fact/event        EventTable.EventID
6    link to a task                TaskTable.TaskID
7    link to a name                NameTable.NameID
19    link to an association        FANTable.FanID

OwnerID        foreign key to one of several tables, depending on value of OwnerType


Quality is one of

    ~~~
    P~~
    S~~
    PDO
    SDX
    P~X
    S~O
    PDX
    PN~
    S~X
    ~N~
    P~O
    SNX
    SDO


    RM UI        Source
    Original    O
    Derivative    X
    Don't know    ~

    RM UI      Information
    Primary        P
    Secondary    S
    Don't know    ~

    RM UI      Evidence
    Direct        D
    Indirect    I
    Negative    N
    Don't know    ~

Quality has three positions

    1    Information        P,S,~
    2    Evidence        D,I,N,~
    3    Source            O,X,~


is either 0 or null
external scripts change it

IsPrivate is all 0

Flags is all 0



A citation may only be linked to 
CitationLinkTable
and
Source    citation must always link to a Source, otherwise it is an orphan.



Person
Family
Event-person
Event-family
Tasks
Name
Association



!!!!
Not allowed to link to ChildTable
This is where evidence for a connection goes.
It already has proof values for mother  father

Link to association is new and different
It gives evidence for a relationship.

```


## QUESTIONS














