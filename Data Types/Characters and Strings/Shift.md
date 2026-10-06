# ⏩ Shift
- Shifts the string left/right/circular based on input provided.
- Has multiple variations e.g: Shift by removing leading or trailing characters.

## Shift Left ⬅️ 
- Shift left reducing 1 character, leaving an extra space on the right.
```
DATA str TYPE string.
str = '0000462'.
```

### 1. Default shift left
```
SHIFT str.
WRITE str.
```
### Output
```
000462
```

### 2. Using the LEFT keyword
```
SHIFT str LEFT.
WRITE / str.
```
### Ouput
```
00462
```

### 3. Deleting leading zeroes
```
SHIFT str LEFT DELETING LEADING '0'.
WRITE / str.
```
### Output
```
462
```

## Shift Right ➡️
- Shift right reducing 1 character, leaving an extra space on the left.
```
DATA str TYPE string.
str = '4620000'.
```

### 1. Using the RIGHT keyword
```
SHIFT str RIGHT.
WRITE / str.
```
### Ouput
```
462000
```

### 2. Deleting trailing zeroes
```
SHIFT str LEFT DELETING LEADING '0'.
WRITE / str.
```
### Output
```
462
```

## Circular shift 🔁
- Will shift first character to last
```
DATA str TYPE string.
str = '0000462'.
```

### Using CIRCULAR keyword
```
SHIFT str CIRCULAR.
WRITE / str.
```
### Output
```
0004620
```

