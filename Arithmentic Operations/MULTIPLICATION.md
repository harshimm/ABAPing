# MULTIPLICATION  ✖️

### 1. Involving Only Integers
```
DATA num1 TYPE i VALUE 1.
DATA num2 TYPE i VALUE 2.
DATA result1 TYPE i.

result1 = num1 * num2.

WRITE result1. 
```
### Output
```
2
```
### 2. Involving 1 Integer and 1 decimal.
```
DATA num3 TYPE p DECIMALS 1 VALUE '2.0'.
DATA num4 TYPE i VALUE 1.
DATA result2 LIKE num3.

result2 = num3 * num4.

WRITE / result2.
```
### Output
```
2.0
```

### 3. Involving only decimal values
```
DATA num5 TYPE p DECIMALS 1 VALUE '2.0'.
DATA num6 TYPE p DECIMALS 2 VALUE '3.00'.
DATA result3 LIKE num6.

result3 = num5 * num6.

WRITE / result3.
```

### Output
```
6.00
```

### 4. Using the MULTIPLY statement
```
DATA num7 TYPE p DECIMALS 1 VALUE '2.0'.
DATA num8 TYPE p DECIMALS 2 VALUE '3.00'.
DATA result4 LIKE num8 VALUE 1.

MULTIPLY result4 BY num7.
MULTIPLY result4 BY num8.

WRITE / result4.
```

### Output
```
6.00
```

### 5. Difference in result based on positioning of variables in MULTIPLY statement
```
DATA num7 TYPE p DECIMALS 1 VALUE '2.0'.
DATA num8 TYPE p DECIMALS 2 VALUE '3.00'.
DATA result4 LIKE num8 VALUE 1.

MULTIPLY num7 BY result4.
MULTIPLY num8 BY result4.

WRITE / result4.
```

### Output
```
1.00
```

### Explanation

- num7 remains 2.0 as it is multiplied by 1.00
- num8 remains 3.00 as it is multiplied by 1.00
- the value of result4 is not changed anywhere so it prints the original value of result4
