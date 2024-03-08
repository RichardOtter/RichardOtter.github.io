# SourceTable

## DDL

CREATE TABLE SourceTable (SourceID INTEGER PRIMARY KEY, Name TEXT COLLATE RMNOCASE, RefNumber TEXT, ActualText TEXT, Comments TEXT, IsPrivate INTEGER, TemplateID INTEGER, Fields BLOB, UTCModDate FLOAT );

CREATE INDEX idxSourceName ON SourceTable (Name COLLATE RMNOCASE) ;

## LIST

| #     | Name          | Type      |
|-------|---------------|-----------|
1		| SourceID		| INTEGER	
2		| Name			| TEXT		
3		| RefNumber		| TEXT	
4		| ActualText	| TEXT	
5		| Comments		| TEXT	
6		| IsPrivate		| INTEGER	
7		| TemplateID	| INTEGER	
8		| Fields		| BLOB		
9		| UTCModDate	| FLOAT	

## NOTES

| #     | Name          | Note      |
|-------|---------------|-----------|
1		| SourceID		| 
2		| Name			| 
3		| RefNumber		| 
4		| ActualText	| 
5		| Comments		| 
6		| IsPrivate		| 
7		| TemplateID	| 
8		| Fields		| 
9		| UTCModDate	| 


Name is the source name and it is collated with RMNOCASE
TemplateID refers to the SourceTemplateTable, except when it is 0, which
is a special case. See below.


Fields = all data in XML as shown below. 
Field name from SourceTemplate, goes in the Name element.
Text goes in the Value element. 

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

XMK field starts with <Root>
no XML processing statement, no BOM
Value does not contain \r\n

Special Case:
for free form templated sources
In the SourceTable
TemplateID = 0
Fields = Name elements must be  "Footnote", "ShortFootnote" and "Bibliography"


## QUESTIONS
Why are so many of my sources marked Private ? (IsPrivate=1)


<Root><Fields>
<Field><Name>Footnote</Name>
<Value></Value></Field>

<Field><Name>ShortFootnote</Name>
<Value></Value></Field>

<Field><Name>Bibliography</Name>
<Value></Value></Field>
</Fields></Root>

