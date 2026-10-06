# Time field ⏰
- It is a string field
- Stores values in HHMMSS format
- The initial values are '000000'
- Values can be specified explicitly using the VALUE statement
- Variables can be assigned to system time using sy-uzeit
- Arithmetic operations can be used to time fields

### 1. Declaration
```
DATA timevar TYPE t.
DATA timevar2 TYPE t VALUE '100000'.
DATA systime TYPE t.
DATA systime2 LIKE sy-uzeit.

systime = sy-uzeit.

WRITE : / timevar,
        timevar2,
        / systime,
        systime2.
```
### Output
```
000000 100000
043308 00:00:00
```

### 2. Find current system time (returns UTC time)
```
systime = sy-uzeit.
WRITE systime.
```
### Output
```
043308
```

### 3. Difference in seconds
```
DATA : diff_hours   TYPE p DECIMALS 2,
       diff_minutes TYPE p DECIMALS 2,
       diff_seconds TYPE p DECIMALS 2.

timevar2 = '040000'.
diff_seconds = sy-uzeit - timevar2.
SKIP 2.
WRITE diff_seconds.
```
### Output
```
3,437.00
```
### 4. Difference in minutes
```
diff_minutes = diff_seconds / 60.
WRITE / diff_minutes.
```
### Output
```
57.28
```

### 5. Difference in hours
```
diff_hours = diff_minutes / 60.
WRITE / diff_hours.
```
### Output
```
0.95
```

### 6. Adding seconds
```
DATA : adds TYPE t,
       addm TYPE t,
       addh TYPE t.

WRITE sy-uzeit.

adds = sy-uzeit + timevar2.
SKIP 2.
WRITE adds.
```
### Output
```
091246
```

### 7. Adding minutes
```
addm = adds / 60.
WRITE / addm.
```
### Output
```
000913
```

### 8. Adding hours
```
addh = addm / 60.
WRITE / addh.
```
### Output
```
000009
```
