# RR Family Tree Data Source Template

[Home](https://richardotter.github.io)

Download link for rmst file =
[RR Family Tree Data.rmst](https://RichardOtter.github.io/SourceTemplate/rmst/RR%20Family%20Tree%20Data.rmst)

## Overview

Records created by users at the various online genealogy sites can be cited
using this template.
Records are lumped by the tree, either a member created tree, or a universal tree.
The template name bins with "RR"indicating that is falls into the
Research Report category.

## Template details

These contain the template name, an optional description,
the filed names, hints, and the sentences to be used to
form the footnotes. etc.

```text
Source Template= _RR Family Tree Data
Version= 2025-02-18

Field                   Type       Display name
-----------------------------------------------------

Source Fields
NameService             Text        Website Name
NameTree                Text        Tree Name
NameOwner               Text        Tree Owner
TreeID                  Text        Tree ID
DateSource              Date        Date Source last updated

Citation Fields
Person                  Name        Person
DateBirth               Date        Birth Date
PersonID                Text        Person ID
CD                      Text        Citation Detail
DateCitation            Date        Date Citation last updated
```

## Source Data

For the source data examples below, the
[Ancestry profile page](https://www.ancestry.com/family-tree/person/tree/14741034/person/155162784/facts)
is used.

### Website Name

FieldName=NameService, Type=Text
>Example NameService = Ancestry.com, member tree

### Tree Name

FieldName = NameTree, Type=Text
>Example NameTree = Otter-Saito

### Tree Owner

FieldName=NameOwner, Type=Text
>Example NameOwner = Richard_J_Otter

### Tree ID

FieldName=TreeID, Type=Text
>Example TreeID = 14741034

### Date Source last updated

FieldName=DateSource, Type=Date
>Example DateSource = 19 Feb 2025

## Citation Data

For the citation data examples below, the
[Ancestry profile page](https://www.ancestry.com/family-tree/person/tree/14741034/person/155162784/facts)
is used.

### Citation Name

Autogenerated by RM. In this case:
>Ferdinand Otter; 29 September 1894; 155162784; ; 19 February 2025

### Person

FieldName=Person, Type=Name
>Example Person = Ferdinand Otter

I use the spelling of the name as it is in the profile page.

### Birth date

FieldName=DateBirth, Type=Date
>Example DateBirth = 29 SEP 1894

### Person ID

FieldName=PersonID, Type=Text
>Example PersonID = 155162784

### Citation Detail

FieldName=CD, Type=Text
>Example CD = EMPTY

Whatever info needed to explain what info this citation provides. Usually blank.

### Date Citation last updated

FieldName=DateCitation, Type=Date
>Example DateCitation = 19 Feb 2025

Last date citation wsa updated, accessed online.

## Citations produced

### Footnote

>Ancestry.com, member trees. Member tree: Otter-Saito by Richard_J_Otter, entry for Ferdinand Otter, born: 29 September 1894, ID:155162784 -- updated: 19 February 2025. Not a primary source.

### Short footnote

>Member tree: Otter-Saito by Richard_J_Otter, entry for Ferdinand Otter.

### Bibliography

>Ancestry.com, member trees, member tree: Otter-Saito by Richard_J_Otter

## rmst File Analysis

This is the relevant part of the rmst file. 
End tags have been removed.

```text
<SourceTemplates>
    <Copyright>RootsMagic source templates, template language, and template file format are copyright 2009-2020 RootsMagic, Inc.  All rights reserved.

    <Template Id="10069">
        <Name>_RR Family Tree Data

        <Description>For use when citing Ancestry or MyHeritage member trees or the FamilySearch universal tree as source data.

        <Category>ver 2025-02-18

        <Footnote> [NameService]. Member tree: [NameTree] by [NameOwner], entry for [Person]<, born: [DateBirth]><, ID:[PersonID]> -- updated: [DateCitation]< -- [CD]>. Not a primary source.

        <ShortFootnote>Member tree: [NameTree] by [NameOwner], entry for [Person].

        <Bibliography>[NameService], member tree: [NameTree] by [NameOwner]

        <Field>
            <Type>Text
            <Name>NameService
            <Display>Website Name
            <Hint>
            <Detail>false
            <LongHint>

        <Field>
            <Type>Text
            <Name>NameTree
            <Display>Tree Name
            <Hint>
            <Detail>false
            <LongHint>

        <Field>
            <Type>Text
            <Name>NameOwner
            <Display>Tree Owner
            <Hint>
            <Detail>false
            <LongHint>

        <Field>
            <Type>Text
            <Name>TreeID
            <Display>Tree ID
            <Hint>
            <Detail>false
            <LongHint>

        <Field>
            <Type>Date
            <Name>DateSource
            <Display>Date Source last updated
            <Hint>
            <Detail>false
            <LongHint>

        <Field>
            <Type>Name
            <Name>Person
            <Display>Person
            <Hint>As in source.
            <Detail>true
            <LongHint>

        <Field>
            <Type>Date
            <Name>DateBirth
            <Display>Birth Date
            <Hint>As in source.
            <Detail>true
            <LongHint>

        <Field>
            <Type>Text
            <Name>PersonID
            <Display>PersonID
            <Hint>
            <Detail>true
            <LongHint>

        <Field>
            <Type>Text
            <Name>CD
            <Display>Citation Detail
            <Hint>
            <Detail>true
            <LongHint>

        <Field>
            <Type>Date
            <Name>DateCitation
            <Display>Date Citation last updated
            <Hint>
            <Detail>true
            <LongHint>
```
