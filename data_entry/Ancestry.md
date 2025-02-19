# Data entry in RootsMagic - Ancestry.com

[Home](https://richardotter.github.io)

Last Updated:  2025-02-19

## Contents

### [Ancestry collection as a source](#Sec_1)

### [Ancestry member tree as a source](#Sec_2)

#### [Source Fields](#source-fields)

#### [Citation Fields](#Sec_2_2)

### [URL formats at Ancestry](#Sec_R1)

\
\
\

## Ancestry collection as a source <a id="Sec_1"></a>

TODO

## Ancestry member tree as a source <a id="Sec_2"></a>

Consider member trees to be a Research Report created by the tree owner.
This is not primary data, but instead, a person's conclusions drawn from sources,
sometimes shown sometimes not.

### Source Fields <a id="Sec_2_1"></a>

#### Source Type

The source template
_RR Family Tree Data

version: 2024-12-18

See: ST_info_RR Family Tree Data.md for details about the template
and an example of how to use the fields.

#### Source Name

RRdb ANC Mem-Tr [tree name] BY [tree owner user ID]

Example names
RRdb ANC Mem-Tr Urcia Family Tree BY brianrikio
RRdb ANC Mem-Tr Viltz Family Tree BY g_cloud1

#### NameService

The name of the website.

#### NameTree

The name of the member tree
Include all characters

#### NameOwner

The name of the member tree's owner. Usually a user ID at the website.

#### Date Source last updated

Date source created or last updated
Not some date from the online repo, just the last time the RM record was changed.
This is also in the UTCModTime column in the database,
but that is not visible to the use.

#### Source Text

Free form text formatted as:

```text
    Tree Owner User Name:  
    Tree Owner Real Name:
    Owner Email:     
    Owner Location: 
    
    Tree Name:    
    
    URL:         https://www.ancestry.com/family-tree/tree/
    Status:      public/private   
    
    Families of interest:
```

example: Source Text=

```text
    Tree Owner User Name: John Schwab
    Tree Owner Real Name: John Schwab
    Owner Email: 
    Owner Location: 
    Joined: 16 Aug 2016

    Tree Name: Schwab Family Tree
    URL: https://www.ancestry.com/family-tree/tree/103144899
    Status: public

    Families of interest:
    Schwab
```

#### Source Comment

EMPTY

#### Source Ref\#

EMPTY

#### Media-Source

EMPTY

#### Repositories

EMPTY

#### Source WebTags

URL to the general tree page
  user profile
  tree

### Citation Fields <a id="Sec_2_2"></a>

#### Citation Name

Use auto generated name.
When updating fields, be sure to trigger regeneration.

#### Person

Name of person this citation refers to
As it is in the source

#### Birth Date

Birthdate of above person.
As it is in the source

#### Person ID

The person number, usually found in the URL
could be treeID:personID

#### Citation Detail

Usually blank. Can explain why citation is used.

#### Date Citation last updated

Last date citation was updated.
Specifically, when was the online data last accessed/updated.

#### Research Note

Copy the profile page information.

#### Detail Comment

Free form text helping explain the citation.
Here usually blank.
Could be used to discuss unusual aspects of the data.

#### Detail Ref\#

EMPTY

#### Media-Citation

TODO    Media File name format

#### Citation WebTags

URL of the person's profile page.
ends with "facts"

## TODO section

RRdb ANC source for a downloaded image

Research Note-

```text
Photo -shared YYYY   (date item was shared on ANC)

PHOTO
caption
date
shared
URL
```

Detail Comment-

Date and other interpretation/description

## General Reference Information

### URL formats at Ancestry <a id="Sec_R1"></a>

```text
Ancestry Source URLs
new
https://www.ancestry.com/search/collections/61009/records/1373624

new (but does not work for all databases ?)
https://www.ancestry.com/discoveryui-content/view/646978:2025


old but still working
https://search.ancestry.com/cgi-bin/sse.dll?indiv=1&db=61009&h=1373624


google AI says this is source URL format. but this one does not work
https://www.ancestry.com/interactive/646978/2025


The links shown next are point to RJO account, but the format should be general.

User profile
https://www.ancestry.com/profile/00b068f5-0003-0000-0000-000000000000

User profile Public
https://www.ancestry.com/profile/00b068f5-0003-0000-0000-000000000000?preview=true

Tree overview
https://www.ancestry.com/family-tree/tree/14741034/recent?usePUBJs=true

Main tree
owner ? centered in tree
https://www.ancestry.com/family-tree/tree/14741034/family?cfpid=155162778

Profile page
https://www.ancestry.com/family-tree/person/tree/14741034/person/155162778/facts

Source Image URLs
TODO
```
