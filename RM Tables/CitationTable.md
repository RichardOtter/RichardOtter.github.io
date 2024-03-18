# CitationTable

## DDL

CREATE TABLE CitationTable (CitationID INTEGER PRIMARY KEY, SourceID INTEGER, Comments TEXT, ActualText TEXT, RefNumber TEXT, Footnote TEXT, ShortFootnote TEXT, Bibliography TEXT, Fields BLOB, UTCModDate FLOAT, CitationName TEXT COLLATE RMNOCASE );

CREATE INDEX idxCitationName ON CitationTable (CitationName);

CREATE INDEX idxCitationSourceID ON CitationTable (SourceID);

## LIST

| #  | Name          | Type      |
|----|---------------|-----------|
| 1  | CitationID    | INTEGER
| 2  | SourceID      | INTEGER
| 3  | Comments      | TEXT
| 4  | ActualText    | TEXT
| 5  | RefNumber     | TEXT
| 6  | Footnote      | TEXT
| 7  | ShortFootnote | TEXT
| 8  | Bibliography  | TEXT
| 9  | Fields        | BLOB
| 10 | UTCModDate    | FLOAT
| 11 | CitationName  | TEXT

## NOTES

| #  | Name          | Note      |
|----|---------------|-----------|
| 1  | CitationID    | 
| 2  | SourceID      | 
| 3  | Comments      | 
| 4  | ActualText    | 
| 5  | RefNumber     | 
| 6  | Footnote      | 
| 7  | ShortFootnote | 
| 8  | Bibliography  | 
| 9  | Fields        | 
| 10 | UTCModDate    | 
| 11 | CitationName  | collated with RMNOCASE| 

 ## QUESTIONS

Columns: Footnote, ShortFootnote, and Bibliography are used for custom sentences.
Haven't tested, but its plain text, so probably exactly the same as the Footnote, ShortFootnote, and Bibliography columns in SourceTemplateTable


Fields = all data in XML as shown below. 
Field name from SourceTemplate, goes in the Name element.
Text goes in the Value element. 

```
<Root><Fields>

    <Field>
    <Name></Name>
    <Value></Value>
    </Field>
    
    <Field>
    <Name></Name>
    <Value></Value>
    </Field>
    
    <Field>
    <Name></Name>
    <Value></Value>
    </Field>
    
    </Fields></Root>

XML field starts with <Root>
no XML processing statement, no BOM
Value does not contain \r\n

```