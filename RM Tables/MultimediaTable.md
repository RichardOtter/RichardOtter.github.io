# MultimediaTable

## DDL

CREATE TABLE MultimediaTable (MediaID INTEGER PRIMARY KEY, MediaType INTEGER, MediaPath TEXT, MediaFile TEXT COLLATE RMNOCASE, URL TEXT, Thumbnail BLOB, Caption TEXT COLLATE RMNOCASE, RefNumber TEXT COLLATE RMNOCASE, Date TEXT, SortDate BIGINT, Description TEXT, UTCModDate FLOAT );

CREATE INDEX idxMediaFile ON MultimediaTable (MediaFile);

CREATE INDEX idxMediaURL ON MultimediaTable (URL);


## LIST

| #     | Name          | Type      |
|-------|---------------|-----------|
1		| MediaID		| INTEGER
2		| MediaType		| INTEGER
3		| MediaPath		| TEXT
4		| MediaFile		| TEXT
5		| URL			| TEXT
6		| Thumbnail		| BLOB	
7		| Caption		| TEXT
8		| RefNumber		| TEXT
9		| Date			| TEXT
10		| SortDate		| BIGINT
11		| Description	| TEXT
12		| UTCModDate	| FLOAT


## NOTES

| #     | Name          | Note      |
|-------|---------------|-----------|
1		| MediaID		| primary key
2		| MediaType		| 
3		| MediaPath		| path with optional relative path anchor character
4		| MediaFile		| file name
5		| URL			| unimplemented
6		| Thumbnail		| format ?, size ?
7		| Caption		| 
8		| RefNumber		| 
9		| Date			| 
10		| SortDate		| standard
11		| Description	| 
12		| UTCModDate	| standard



RMNOCASE used for-
RefNumber
MediaFile
Caption

## QUESTIONS

