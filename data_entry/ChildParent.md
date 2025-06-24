# ChildParent Fact

ChildParent fact's sources document this person's parents as shown in the tree.

The data in the fact also guides research work by using certain keywords in the description field.

## FACT standard data items

### Fact Name

### Date

NOT USED

### Place

NOT USED

### Place Details

NOT USED

### Description

``` text
[blank]
_STOP
_START-OF-LINE

other temporary terms
_TENTATIVE
_CENSUS
_OBIT
TODO
TODO source
TODO adopted
TODO [other text]
```

If parents available from known sources, also use Start of line. but include a source citation for the parents.

Used for source of cousin's parents. That as far as I go under normal circumstances. ??

ChildParent Description Keywords

```text
empty                   Fact should have sources for the listed parents
_STOP                   Don't go further than this person in research
_START-OF-LINE          last known person in direct ancestor line I want to continue-
_TENTATIVE              connection is not proven. Conjecture

_CENSUS                 connection from census record but only summary is entered
_OBIT                   connection from obituary but only summary is entered

TODO source             has parents and needs source
TODO                    last known person in a line I want to continue to next generation
```

normal situation
blank, has parents, has source(s)

needs source
has parents, no source

### Proof

TODO

### Primary

NONE

### Private

NONE

### Sort date

Filled in with SQL Script.\
Set to "4000" so that it sorts near the end on the other Facts.

### Note

NONE

### Sources

Attach source that support this person is child of the parents in the tree. 
If uncertain, list all sources regarding parentage.

If this is a _STOP person, can still add sources to parents if known,
even though parents are not in database.

### Media

NONE

### Tasks

As needed.

### Shared

NONE

## Color coding of Person

Color code person based on some of the keywords in the description.

_STOP = yellow

cousins  red   (listed here for possible interactions/interference)

## Group memberships

FACT-ChildParent= blank & no parents\
FACT-ChildParent= blank & no source\
FACT-ChildParent= fact missing\
FACT-ChildParent= not blank & parents\
FACT-ChildParent= _START-OF-LINE\
FACT-ChildParent= _STOP\
FACT-ChildParent= TODO\
FACT-ChildParent= TODO Start of line.\

TODO\
explanations\
FACT-ChildParent= blank & no source\
if has parents, needs source\
if no parents, either TODO source   or _STOP\

