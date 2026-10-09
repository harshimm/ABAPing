# CLEAR statement
- Used to initialize values back to initial value of the data type

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
- Use CLEAR to initialise the field(s) and add a new value.

```
CLEAR.

rec_leavereq-requestid = '06'.
rec_leavereq-talentid = '004O21744'.
rec_leavereq-zzfirstname = 'HARSHINI'.
rec_leavereq-zzsurname = 'MARAPPAN'.
rec_leavereq-reqtype = 'S'.
rec_leavereq-fromdate = '12/09/2026'.
rec_leavereq-todate = '12/09/2026'.
rec_leavereq-createdon = sy-datum.
rec_leavereq-zzmfirstname = 'ALE'.
rec_leavereq-zzmsurname = 'VALLIN'.

INSERT zleavereq FROM rec_leavereq.
ULINE.
SKIP 2.
```

- Use clear only for a specific fields

```
CLEAR rec_leavereq-requestid.

rec_leavereq-requestid = '07'.
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
