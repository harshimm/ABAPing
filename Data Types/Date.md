# Date Field 📅
- It is a string field
- Stores values in YYYYMMDD format
- The initial values are '00000000'
- Values can be specified explicitly using the VALUE statement
- Variables can be assigned to system time using sy-datum
- Arithmetic operations can be used to time fields

### 1. Declaration
```
DATA datevar TYPE d.
DATA datevar2 TYPE d VALUE '20261001'.
DATA sysdate TYPE d.
DATA sysdate2 LIKE sy-datum.

sysdate = sy-datum.

WRITE : / datevar,
          datevar2,
        / sysdate,
          sysdate2.
```
### Output
```
00000000 10012026
10012026 00/00/0000
```

### 2. Find current system date
```
sysdate = sy-datum.
WRITE sysdate.
```
### Output
```
10012026
```

### 3. Difference in days
```
DATA : diff_years  TYPE p DECIMALS 2,
       diff_months TYPE p DECIMALS 2,
       diff_days   TYPE p DECIMALS 2.

datevar2 = '20250928'.
diff_days = sy-datum - datevar2.
SKIP 2.
WRITE diff_days.
```
### Output
```
368.00
```
### 4. Difference in months
```
diff_months = diff_days / 12.
WRITE / diff_months.
```
### Output
```
30.67
```

### 5. Difference in years
```
diff_years = diff_months / 12.
WRITE / diff_years.
```
### Output
```
2.56
```

### 6. Adding days
```
DATA : addy TYPE d,
       addm TYPE d,
       addd TYPE d,
       add_num TYPE i.

WRITE / sy-datum.

add_num = 20.
addd = sy-datum + 20.
SKIP 2.
WRITE addd.
```
### Output
```
10212026
```

### 7. Adding months
```
addm = sy-datum.
addm+4(2) = 11.
WRITE / addm.
```
### Output
```
11012026
```

### 8. Adding years
```
addy = sy-datum.
addy(4) = '2030'.
WRITE / addy.
```
### Output
```
10012030
```
