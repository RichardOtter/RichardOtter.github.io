# SourceTable

## DDL

CREATE TABLE SourceTable (SourceID INTEGER PRIMARY KEY, Name TEXT COLLATE RMNOCASE, RefNumber TEXT, ActualText TEXT, Comments TEXT, IsPrivate INTEGER, TemplateID INTEGER, Fields BLOB, UTCModDate FLOAT );

CREATE INDEX idxSourceName ON SourceTable (Name COLLATE RMNOCASE) ;


## DESIGN

RecNo	FieldName	SQLType	Size	Scale	PKDisplay	DefaultValue	NotNull	NotNullConflictClause	Unique	UniqueConflictClause	CollateValue	GeneratedExpr	GeneratedStorage	FKDisplay
1	SourceID	INTEGER			True		False		False					
2	Name	TEXT			False		False		False		RMNOCASE			
3	RefNumber	TEXT			False		False		False					
4	ActualText	TEXT			False		False		False					
5	Comments	TEXT			False		False		False					
6	IsPrivate	INTEGER			False		False		False					
7	TemplateID	INTEGER			False		False		False					
8	Fields	BLOB			False		False		False					
9	UTCModDate	FLOAT			False		False		False					

## LIST
| #     | Name          | Type      |
|-------|---------------|-----------|
1	| SourceID	| INTEGER	
2	| Name		| TEXT		
3	| RefNumber	| TEXT	
4	| ActualText	| TEXT	
5	| Comments	| TEXT	
6	| IsPrivate	| INTEGER	
7	| TemplateID	| INTEGER	
8	| Fields		| BLOB		
9	| UTCModDate	| FLOAT	


## NOTES
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

