# Fact types

Facts may be either of type  Personal or Family\
OwnerType =0, Personal Fact\
OwnerType =1, Family Fact

## Standard RM Fact Types

Alphabetically by Name

As of RM v10.0.5

Using the SQL:

```text
SELECT format(" %4u    %4u       %s ", FactTypeID, OwnerType, Name)
FROM FactTypeTable
WHERE FactTypeID <=1000
ORDER BY Name COLLATE NOCASE ASC
```

```text
FactTypeID  OwnerType   Name

    6       0       Adoption
  900       0       Alternate name
   34       0       Ancestral File Number
  301       1       Annulment
  902       0       Association
    7       0       Baptism
    8       0       Bar Mitzvah
    9       0       Bas Mitzvah
    1       0       Birth
   10       0       Blessing
    4       0       Burial
   36       0       Caste
   18       0       Census
  311       1       Census (family)
    3       0       Christen
   11       0       Christen (adult)
   12       0       Confirmation
    5       0       Cremation
    2       0       Death
  500       0       Degree
   23       0       Description
  302       1       Divorce
  303       1       Divorce filed
  901       0       DNA test
   24       0       Education
  507       0       Election
   16       0       Emigration
  304       1       Engagement
  508       0       Excommunication
   13       0       First communion
   21       0       Graduation
  504       0       Illness
   17       0       Immigration
   31       0       LDS Baptism
   38       0       LDS Confirmation
   32       0       LDS Endowment
   39       0       LDS Initiatory
   33       0       LDS Seal to parents
  309       1       LDS Seal to spouse
  505       0       Living
  300       1       Marriage
  305       1       Marriage Bann
  306       1       Marriage Contract
  307       1       Marriage License
  308       1       Marriage Settlement
  501       0       Military
  999       0       Miscellaneous
  502       0       Mission
  509       0       Namesake
   25       0       Nationality
   15       0       Naturalization
   26       0       Occupation
   14       0       Ordination
   19       0       Probate
   27       0       Property
   35       0       Reference No
   28       0       Religion
   29       0       Residence
  310       1       Residence (family)
   22       0       Retirement
  510       1       Separation
   30       0       Soc Sec No
  503       0       Stillborn
   37       0       Title (Nobility)
   20       0       Will
```

## All Fact Types in my database

Alphabetically by Name

As of 2025-03-20

Using the SQL:

```text
SELECT format(" %4u    %4u       %s ", FactTypeID, OwnerType, Name)
FROM FactTypeTable
--WHERE FactTypeID <=1000
ORDER BY Name COLLATE NOCASE ASC
```

```text
FactTypeID  OwnerType   Name

    6       0       Adoption
  900       0       Alternate name
   34       0       Ancestral File Number
 1021       0       Anecdote
  301       1       Annulment
 1061       0       Arrival
  902       0       Association
 1023       0       Attributes
    7       0       Baptism
    8       0       Bar Mitzvah
    9       0       Bas Mitzvah
    1       0       Birth
   10       0       Blessing
    4       0       Burial
   36       0       Caste
   18       0       Census
  311       1       Census (family)
 1102       0       Census_research
 1065       0       ChildParent
    3       0       Christen
   11       0       Christen (adult)
   12       0       Confirmation
    5       0       Cremation
    2       0       Death
 1080       0       Death_Cause
  500       0       Degree
   23       0       Description
  302       1       Divorce
  303       1       Divorce filed
 1062       0       DNA
  901       0       DNA test
   24       0       Education
  507       0       Election
   16       0       Emigration
  304       1       Engagement
 1100       0       Evidence-Summary
  508       0       Excommunication
   13       0       First communion
 1089       0       Friend-Associate
   21       0       Graduation
 1101       0       History
 1098       0       ID_ANC
 1094       0       ID_FG
 1063       0       ID_FSFT
 1064       0       ID_TMG
 1050       0       ID_WIKTR
  504       0       Illness
   17       0       Immigration
 1086       0       Imprisonment
   31       0       LDS Baptism
   38       0       LDS Confirmation
   32       0       LDS Endowment
   39       0       LDS Initiatory
   33       0       LDS Seal to parents
  309       1       LDS Seal to spouse
  505       0       Living
  300       1       Marriage
  305       1       Marriage Bann
  306       1       Marriage Contract
  307       1       Marriage License
  308       1       Marriage Settlement
 1054       0       Medical
 1099       0       MetWithRJO
  501       0       Military
 1079       0       Military Draft Registration
 1081       0       Military Service
  999       0       Miscellaneous
  502       0       Mission
  509       0       Namesake
   25       0       Nationality
   15       0       Naturalization
 1087       0       NaturalizationPetition
 1090       0       NeverMarried
 1026       0       Note
 1048       0       Num Child
 1067       1       Num Child (fam)
 1085       0       Obituary
   26       0       Occupation
   14       0       Ordination
 1093       1       Partnership
 1083       0       Passport Application
 1055       0       Photo
 1073       1       Photo (fam)
   19       0       Probate
   27       0       Property
   35       0       Reference No
   28       0       Religion
 1096       0       ResearchNote
   29       0       Residence
  310       1       Residence (family)
   22       0       Retirement
  510       1       Separation
   30       0       Soc Sec No
  503       0       Stillborn
   37       0       Title (Nobility)
 1001       0       Travel
   20       0       Will
```

## Fact Types created by RJO for personal use

Alphabetically by Name

As of 2025-02-20

Using the SQL:

```text
SELECT format(" %4u    %4u       %s ", FactTypeID, OwnerType, Name)
FROM FactTypeTable
WHERE FactTypeID >=1000
ORDER BY Name COLLATE NOCASE ASC
```

```text
FactTypeID  OwnerType   Name
 1021       0       Anecdote
 1061       0       Arrival
 1023       0       Attributes
 1102       0       Census_research
 1065       0       ChildParent
 1080       0       Death_Cause
 1062       0       DNA
 1100       0       Evidence-Summary
 1089       0       Friend-Associate
 1101       0       History
 1098       0       ID_ANC
 1094       0       ID_FG
 1063       0       ID_FSFT
 1064       0       ID_TMG
 1050       0       ID_WIKTR
 1086       0       Imprisonment
 1054       0       Medical
 1099       0       MetWithRJO
 1079       0       Military Draft Registration
 1081       0       Military Service
 1087       0       NaturalizationPetition
 1090       0       NeverMarried
 1026       0       Note
 1048       0       Num Child
 1067       1       Num Child (fam)
 1085       0       Obituary
 1093       1       Partnership
 1083       0       Passport Application
 1055       0       Photo
 1073       1       Photo (fam)
 1096       0       ResearchNote
 1001       0       Travel
```
