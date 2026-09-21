# DIVISION ➗

### 1. Involving Only Integers
```
DATA num1 TYPE i VALUE 2.
DATA num2 TYPE i VALUE 1.
DATA result1 TYPE i.

result1 = num1 / num2.

WRITE result1.
uline. 
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

result2 = num3 / num4.

WRITE / result2.
uline.
```
### Output
```
2.0
```

### 3. Involving only decimal values
```
DATA num5 TYPE p DECIMALS 1 VALUE '3.00'.
DATA num6 TYPE p DECIMALS 2 VALUE '2.00'.
DATA result3 LIKE num6.

result3 = num5 / num6.

WRITE / result3.
```

### Output
```
1.50
```

### 4. Using the DIVIDE statement
```
DATA num7 TYPE p DECIMALS 1 VALUE '3.00'.
DATA num8 TYPE p DECIMALS 2 VALUE '2.00'.
DATA result4 LIKE num8 VALUE '1.00'.

MULTIPLY result4 BY num7.
DIVIDE result4 BY num8.

WRITE / result4.
```

### Output
```
2
```

### 5. Difference in result based on positioning of variables in MULTIPLY statement
```
DATA num9 TYPE p DECIMALS 1 VALUE '2.00'.
DATA num10 TYPE p DECIMALS 2 VALUE '3.00'.
DATA result5 LIKE num8 VALUE '1.00'.

DIVIDE num9 BY result5.
DIVIDE num10 BY result5.

WRITE / result5.
```

### Output
```
1.00
```

### Explanation

- num7 remains 2.0 as it is multiplied by 1.00
- num8 remains 3.00 as it is multiplied by 1.00
- the value of result4 is not changed anywhere so it prints the original value of result4

### 6. Using DIV Statement (Returns integer quotient)
```
DATA num11 TYPE p DECIMALS 1 VALUE '2.00'.
DATA num12 TYPE p DECIMALS 2 VALUE '5.00'.

num12 = num12 DIV num11.

WRITE / num12.
ULINE.
```

### Output
```
2.00
```

### 7. Using MOD Statement (Returns remainder)
```
DATA num13 TYPE p DECIMALS 1 VALUE '2.00'.
DATA num14 TYPE p DECIMALS 2 VALUE '3.00'.

num14 = num14 MOD num13.

WRITE / num14.
ULINE.
```

### Output
```
1.00
```
