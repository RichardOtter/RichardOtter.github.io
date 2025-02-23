# Fact types

Facts may be either of type  Personal or Family\
OwnerType =0, Personal Fact\
OwnerType =1, Family Fact

## Standard RM Fact Types

Alphabetically by Name

As of RM v10.0.5

Using the SQL:

```text
SELECT format(" %4u   %4u    %30s %17s", FactTypeID, OwnerType, Name, Abbrev) 
    AS 'FactTypeID  OwnerType                     Name      Abbreviation'
FROM FactTypeTable
WHERE FactTypeID <=1000
ORDER BY Name COLLATE NOCASE ASC
```

```text
FactTypeID  OwnerType                     Name      Abbreviation
    6      0                          Adoption          Adoption
  900      0                    Alternate name         Alt. Name
   34      0             Ancestral File Number               AFN
  301      1                         Annulment         Annulment
  902      0                       Association       Association
    7      0                           Baptism           Baptism
    8      0                       Bar Mitzvah       Bar Mitzvah
    9      0                       Bas Mitzvah       Bas Mitzvah
    1      0                             Birth             Birth
   10      0                          Blessing          Blessing
    4      0                            Burial            Burial
   36      0                             Caste             Caste
   18      0                            Census            Census
  311      1                   Census (family)      Census (fam)
    3      0                          Christen               Chr
   11      0                  Christen (adult)       Chr (adult)
   12      0                      Confirmation      Confirmation
    5      0                         Cremation         Cremation
    2      0                             Death             Death
  500      0                            Degree            Degree
   23      0                       Description       Description
  302      1                           Divorce           Divorce
  303      1                     Divorce filed        Div. filed
  901      0                          DNA test               DNA
   24      0                         Education         Education
  507      0                          Election           Elected
   16      0                        Emigration        Emigration
  304      1                        Engagement        Engagement
  508      0                   Excommunication            Excomm
   13      0                   First communion        First comm
   21      0                        Graduation        Graduation
  504      0                           Illness           Illness
   17      0                       Immigration       Immigration
   31      0                       LDS Baptism          LDS Bapt
   38      0                  LDS Confirmation          LDS Conf
   32      0                     LDS Endowment         LDS Endow
   39      0                    LDS Initiatory          LDS Init
   33      0               LDS Seal to parents       LDS SealPar
  309      1                LDS Seal to spouse        LDS SealSp
  505      0                            Living            Living
  300      1                          Marriage          Marriage
  305      1                     Marriage Bann         Marr Bann
  306      1                 Marriage Contract     Marr Contract
  307      1                  Marriage License          Marr Lic
  308      1               Marriage Settlement   Marr Settlement
  501      0                          Military          Military
  999      0                     Miscellaneous              Misc
  502      0                           Mission           Mission
  509      0                          Namesake          Namesake
   25      0                       Nationality       Nationality
   15      0                    Naturalization    Naturalization
   26      0                        Occupation        Occupation
   14      0                        Ordination        Ordination
   19      0                           Probate           Probate
   27      0                          Property          Property
   35      0                      Reference No             Ref #
   28      0                          Religion          Religion
   29      0                         Residence         Residence
  310      1                Residence (family)   Residence (fam)
   22      0                        Retirement        Retirement
  510      1                        Separation        Separation
   30      0                        Soc Sec No               SSN
  503      0                         Stillborn         Stillborn
   37      0                  Title (Nobility)             Title
   20      0                              Will              Will
```

### Notes on Standard Facts

The Association fact is not the same as the FAN type associate.
FAN entries are stored in the FANTable, not the EventTable.

RM will use the date in a Christen fact as the birth date if there is no Birth fact
(or if the birth fact has no date ??)  Baptism date is not used as such. 
(Let the religious discussion begin...)

All of the family type facts have to do with marriage
EXCEPT Residence (family) and Census (family).

## All Fact Types in my database

Alphabetically by Name

As of 2025-03-20

Using the SQL:

```text
SELECT format(" %4u   %4u    %30s %17s", FactTypeID, OwnerType, Name, Abbrev) 
    AS 'FactTypeID  OwnerType                     Name      Abbreviation'
FROM FactTypeTable
--WHERE FactTypeID <=1000
ORDER BY Name COLLATE NOCASE ASC
```

```text
FactTypeID  OwnerType                     Name      Abbreviation
    6      0                          Adoption          Adoption
  900      0                    Alternate name         Alt. Name
   34      0             Ancestral File Number               AFN
 1021      0                          Anecdote          Anecdote
  301      1                         Annulment         Annulment
 1061      0                           Arrival           Arrival
  902      0                       Association       Association
 1023      0                        Attributes        Attributes
    7      0                           Baptism           Baptism
    8      0                       Bar Mitzvah       Bar Mitzvah
    9      0                       Bas Mitzvah       Bas Mitzvah
    1      0                             Birth             Birth
   10      0                          Blessing          Blessing
    4      0                            Burial            Burial
   36      0                             Caste             Caste
   18      0                            Census            Census
  311      1                   Census (family)      Census (fam)
 1102      0                   Census_research   Census_research
 1065      0                       ChildParent       ChildParent
    3      0                          Christen               Chr
   11      0                  Christen (adult)       Chr (adult)
   12      0                      Confirmation      Confirmation
    5      0                         Cremation         Cremation
    2      0                             Death             Death
 1080      0                       Death_Cause       Death_Cause
  500      0                            Degree            Degree
   23      0                       Description       Description
  302      1                           Divorce           Divorce
  303      1                     Divorce filed        Div. filed
 1062      0                               DNA               DNA
  901      0                          DNA test               DNA
   24      0                         Education         Education
  507      0                          Election           Elected
   16      0                        Emigration        Emigration
  304      1                        Engagement        Engagement
 1100      0                  Evidence-Summary      Evidence-Sum
  508      0                   Excommunication            Excomm
   13      0                   First communion        First comm
 1089      0                  Friend-Associate      Friend-Assoc
   21      0                        Graduation        Graduation
 1101      0                           History           History
 1098      0                            ID_ANC            ID_ANC
 1094      0                             ID_FG             ID_FG
 1063      0                           ID_FSFT           ID_FSFT
 1064      0                            ID_TMG            ID_TMG
 1050      0                          ID_WIKTR          ID_WIKTR
  504      0                           Illness           Illness
   17      0                       Immigration       Immigration
 1086      0                      Imprisonment      Imprisonment
   31      0                       LDS Baptism          LDS Bapt
   38      0                  LDS Confirmation          LDS Conf
   32      0                     LDS Endowment         LDS Endow
   39      0                    LDS Initiatory          LDS Init
   33      0               LDS Seal to parents       LDS SealPar
  309      1                LDS Seal to spouse        LDS SealSp
  505      0                            Living            Living
  300      1                          Marriage          Marriage
  305      1                     Marriage Bann         Marr Bann
  306      1                 Marriage Contract     Marr Contract
  307      1                  Marriage License          Marr Lic
  308      1               Marriage Settlement   Marr Settlement
 1054      0                           Medical           Medical
 1099      0                        MetWithRJO    MetWithRJOtter
  501      0                          Military          Military
 1079      0       Military Draft Registration     Mil Draft Reg
 1081      0                  Military Service  Military Service
  999      0                     Miscellaneous              Misc
  502      0                           Mission           Mission
  509      0                          Namesake          Namesake
   25      0                       Nationality       Nationality
   15      0                    Naturalization    Naturalization
 1087      0           Naturalization Petition       Natural Pet
 1090      0                      NeverMarried      NeverMarried
 1026      0                              Note              Note
 1048      0                         Num Child         Num Child
 1067      1                   Num Child (fam)   Num Child (fam)
 1085      0                          Obituary          Obituary
   26      0                        Occupation        Occupation
   14      0                        Ordination        Ordination
 1093      1                       Partnership     Partner (fam)
 1083      0              Passport Application       Passpt Appl
 1055      0                             Photo             Photo
 1073      1                       Photo (fam)       Photo (fam)
   19      0                           Probate           Probate
   27      0                          Property          Property
   35      0                      Reference No             Ref #
   28      0                          Religion          Religion
 1096      0                      ResearchNote           ResNote
   29      0                         Residence         Residence
  310      1                Residence (family)   Residence (fam)
   22      0                        Retirement        Retirement
  510      1                        Separation        Separation
   30      0                        Soc Sec No               SSN
  503      0                         Stillborn         Stillborn
   37      0                  Title (Nobility)             Title
 1001      0                            Travel            Travel
   20      0                              Will              Will
```

## Fact Types created by RJO for personal use

Alphabetically by Name

As of 2025-02-20

Using the SQL:

```text
SELECT format(" %4u   %4u    %30s %17s", FactTypeID, OwnerType, Name, Abbrev) 
    AS 'FactTypeID  OwnerType                     Name      Abbreviation'
FROM FactTypeTable
WHERE FactTypeID >=1000
ORDER BY Name COLLATE NOCASE ASC
```

```text
FactTypeID  OwnerType                     Name      Abbreviation
 1021      0                          Anecdote          Anecdote
 1061      0                           Arrival           Arrival
 1023      0                        Attributes        Attributes
 1102      0                   Census_research   Census_research
 1065      0                       ChildParent       ChildParent
 1080      0                       Death_Cause       Death_Cause
 1062      0                               DNA               DNA
 1100      0                  Evidence-Summary      Evidence-Sum
 1089      0                  Friend-Associate      Friend-Assoc
 1101      0                           History           History
 1098      0                            ID_ANC            ID_ANC
 1094      0                             ID_FG             ID_FG
 1063      0                           ID_FSFT           ID_FSFT
 1064      0                            ID_TMG            ID_TMG
 1050      0                          ID_WIKTR          ID_WIKTR
 1086      0                      Imprisonment      Imprisonment
 1054      0                           Medical           Medical
 1099      0                        MetWithRJO    MetWithRJOtter
 1079      0       Military Draft Registration     Mil Draft Reg
 1081      0                  Military Service  Military Service
 1087      0           Naturalization Petition       Natural Pet
 1090      0                      NeverMarried      NeverMarried
 1026      0                              Note              Note
 1048      0                         Num Child         Num Child
 1067      1                   Num Child (fam)   Num Child (fam)
 1085      0                          Obituary          Obituary
 1093      1                       Partnership     Partner (fam)
 1083      0              Passport Application       Passpt Appl
 1055      0                             Photo             Photo
 1073      1                       Photo (fam)       Photo (fam)
 1096      0                      ResearchNote           ResNote
 1001      0                            Travel            Travel
```
