# NUMC 1️⃣2️⃣3️⃣
- Special data type to store numbers as strings.
- It is right aligned unlike the remaining data types which are left aligned by default.

### Example 1 ✏️
- When a number is entered which has greater than 1 digit, it prints the first character from the right.
```
DATA numc TYPE n.
numc = 12.
WRITE / numc.
```
### Output
```
2
```

### Example 2 ✏️
- When a character string is provided, it outputs 0, as it stores only numeric characters.
```
DATA numc2 TYPE n.
numc2 = 'Hi'.
WRITE / numc2.
```
### Output
```
0
```

### Example 3 ✏️
- When a numeric string is provided, it fills out the leading spaces with 0, if length of the numeric string is less than the specified length.
- Else it prints the numeric string as it is.
```
DATA numc3 TYPE n LENGTH 6.
numc3 = '123'.
WRITE / numc3.
```
### Output
```
000123
```


