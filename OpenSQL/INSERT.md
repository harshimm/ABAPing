# Insert statement ➡️

### Using only work area
```
DATA rec_leavereq TYPE zleavereq.

rec_leavereq-requestid = '05'.
rec_leavereq-talentid = '004O21744'.
rec_leavereq-zzfirstname = 'HARSHINI'.
rec_leavereq-zzsurname = 'MARAPPAN'.
rec_leavereq-reqtype = 'S'.
rec_leavereq-fromdate = '10/09/2026'.
rec_leavereq-todate = '10/09/2026'.
rec_leavereq-createdon = sy-datum.
rec_leavereq-zzmfirstname = 'ALE'.
rec_leavereq-zzmsurname = 'VALLIN'.

INSERT zleavereq FROM rec_leavereq.
ULINE.
SKIP 2.
```

### Using internal table
```
DATA IT_LEAVEREQ TYPE TABLE OF ZLEAVEREQ.
DATA rec_leavereq LIKE LINE OF IT_LEAVEREQ.


rec_leavereq-requestid = '04'.
rec_leavereq-talentid = '004O21744'.
rec_leavereq-zzfirstname = 'HARSHINI'.
rec_leavereq-zzsurname = 'MARAPPAN'.
rec_leavereq-reqtype = 'S'.
rec_leavereq-fromdate = '09102026'.
rec_leavereq-todate = '09102026'.
rec_leavereq-createdon = sy-datum.
rec_leavereq-createdat = sy-uzeit.
rec_leavereq-zzmfirstname = 'ALE'.
rec_leavereq-zzmsurname = 'VALLIN'.

INSERT zleavereq FROM rec_leavereq.
ULINE.
SKIP 2.
```
