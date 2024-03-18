# NameTable

## DDL

CREATE TABLE NameTable (NameID INTEGER PRIMARY KEY, OwnerID INTEGER, Surname TEXT COLLATE RMNOCASE, Given TEXT COLLATE RMNOCASE, Prefix TEXT COLLATE RMNOCASE, Suffix TEXT COLLATE RMNOCASE, Nickname TEXT COLLATE RMNOCASE, NameType INTEGER, Date TEXT, SortDate BIGINT, IsPrimary INTEGER, IsPrivate INTEGER, Proof INTEGER, Sentence TEXT, Note TEXT, BirthYear INTEGER, DeathYear INTEGER, Display INTEGER, Language TEXT, UTCModDate FLOAT, SurnameMP TEXT, GivenMP TEXT, NicknameMP TEXT );

CREATE INDEX idxSurnameGiven ON NameTable (Surname, Given, BirthYear, DeathYear);

CREATE INDEX idxSurnameGivenMP ON NameTable (SurnameMP, GivenMP, BirthYear, DeathYear);

CREATE INDEX idxNamePrimary ON NameTable (IsPrimary);

CREATE INDEX idxGivenMP ON NameTable (GivenMP);

CREATE INDEX idxNameOwnerID ON NameTable (OwnerID);

CREATE INDEX idxGiven ON NameTable (Given);

CREATE INDEX idxSurname ON NameTable (Surname);

CREATE INDEX idxSurnameMP ON NameTable (SurnameMP);

# LIST

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | NameID        | INTEGER
| 2  | OwnerID       | INTEGER
| 3  | Surname       | TEXT
| 4  | Given         | TEXT
| 5  | Prefix        | TEXT
| 6  | Suffix        | TEXT
| 7  | Nickname      | TEXT
| 8  | NameType      | INTEGER
| 9  | Date          | TEXT
| 10 | SortDate      | BIGINT
| 11 | IsPrimary     | INTEGER
| 12 | IsPrivate     | INTEGER
| 13 | Proof         | INTEGER
| 14 | Sentence      | TEXT
| 15 | Note          | TEXT
| 16 | BirthYear     | INTEGER
| 17 | DeathYear     | INTEGER
| 18 | Display       | INTEGER
| 19 | Language      | TEXT
| 20 | UTCModDate    | FLOAT
| 21 | SurnameMP     | TEXT
| 22 | GivenMP       | TEXT
| 23 | NicknameMP    | TEXT

## NOTES

| #  | Name          | Note      |
|----|---------------|-----------|
| 1  | NameID        | _PK
| 2  | OwnerID       | 
| 3  | Surname       |         collated with RMNOCASE
| 4  | Given         |         collated with RMNOCASE
| 5  | Prefix        |         collated with RMNOCASE
| 6  | Suffix        |         collated with RMNOCASE
| 7  | Nickname      |         collated with RMNOCASE
| 8  | NameType      | see Lookups
| 9  | Date          | standard
| 10 | SortDate      | standard
| 11 | IsPrimary     | 
| 12 | IsPrivate     | 
| 13 | Proof         | 
| 14 | Sentence      | 
| 15 | Note          | multi line text
| 16 | BirthYear     | 
| 17 | DeathYear     | 
| 18 | Display       | unimplemented
| 19 | Language      | unimplemented
| 20 | UTCModDate    | standard
| 21 | SurnameMP     | unimplemented        not collated with RMNOCASE
| 22 | GivenMP       | unimplemented        not collated with RMNOCASE
| 23 | NicknameMP    | unimplemented        not collated with RMNOCASE


## MP Columns
````
these columns have an 'ASCIIized' version of the data in the corresponding column without the MP.

Here are several examples-

|Surname        |SurnameMP        |
|---------------|-----------------|
|Öhring         |   Ohring
|Rüb            |  Rub
|\[wife of Rüb] |  \[wife of Rub]

The Japanese names in my database aren't changed, so ASCIIized is not at 
all a correct description of the transformation. It could also involve using the normalized version of names containing Unicode combining characters.

The columns were not populated at upgrade time, but are filled when a name 
is now added or edited.

The new columns are not declared with a collation, so the indexes that exist were created using the default binary collation.


Lookups

    NameType
    1        AKA
    2        Birth
            Immigrant
            Maiden
    5        Married
            Nickname
            Other Spelling
            
````
## QUESTIONS
Denomalized Birth and death dates should go in the PersonTable.
A person can have multiple names, can each name have a dif B & D date in the index?



