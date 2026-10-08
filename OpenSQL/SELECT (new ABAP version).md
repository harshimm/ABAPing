# SELECT statement (new) ✨
```
DATA it_leavereq TYPE TABLE OF zleavereq.
DATA row_leavereq LIKE LINE OF it_leavereq.
```

### Select all fields (using workarea)
```
SELECT * FROM zleavereq INTO row_leavereq.
  WRITE: / row_leavereq-client,
           row_leavereq-requestid,
           row_leavereq-talentid,
           row_leavereq-fromdate,
           row_leavereq-todate,
           row_leavereq-reqtype,
           row_leavereq-createdon,
           row_leavereq-zzfirstname,
           row_leavereq-zzsurname,
           row_leavereq-createdat,
           row_leavereq-zzmfirstname,
           row_leavereq-zzmsurname.

ENDSELECT.
ULINE.
SKIP 2.
```

### Select only particular fields (using workarea)
```
SELECT FROM ZLEAVEREQ FIELDS
  talentid,
fromdate,
todate,
reqtype,
createdon,
zzfirstname,
zzsurname,
createdat

INTO CORRESPONDING FIELDS OF @row_leavereq.

  WRITE: / row_leavereq-talentid,
             row_leavereq-fromdate,
             row_leavereq-todate,
             row_leavereq-reqtype,
             row_leavereq-createdon,
             row_leavereq-zzfirstname,
             row_leavereq-zzsurname,
             row_leavereq-createdat.

ENDSELECT.
ULINE.
SKIP 2.
```

### Using loop (using internal table)
```
SELECT * FROM zleavereq INTO TABLE @it_leavereq.

LOOP AT it_leavereq INTO row_leavereq.
  WRITE : / row_leavereq-talentid,
           row_leavereq-fromdate,
           row_leavereq-todate,
           row_leavereq-reqtype,
           row_leavereq-createdon,
           row_leavereq-zzfirstname,
           row_leavereq-zzsurname,
           row_leavereq-createdat.
ENDLOOP.
```

### Using Loop (only particular fields using internal table)
```
SELECT FROM zleavereq FIELDS
    talentid,
fromdate,
todate,
reqtype,
createdon,
zzfirstname,
zzsurname,
createdat
  INTO CORRESPONDING FIELDS OF TABLE @it_leavereq.

LOOP AT it_leavereq INTO row_leavereq.
  WRITE : / row_leavereq-talentid,
           row_leavereq-fromdate,
           row_leavereq-todate,
           row_leavereq-reqtype,
           row_leavereq-createdon,
           row_leavereq-zzfirstname,
           row_leavereq-zzsurname,
           row_leavereq-createdat.
ENDLOOP.
```
