# Subfields 🔠
Used to refer to particular characters / strings in a given string

### 1. Obtain the first 2 characters of string
```
DATA : main_string TYPE c LENGTH 40 VALUE 'harshini'.
WRITE main_string(2).
```
### Output
```
ha
```

### 2. Obtain last 5 characters of string
```
DATA : main_string TYPE c LENGTH 40 VALUE 'harshini'.
WRITE main_string+3(5).
```
### Output
```
shini
```

### 3. Replace character of string at specific position
```
DATA : main_string TYPE c LENGTH 40 VALUE 'harshini'.

main_string(1) = 'd'.
WRITE main_string.
```
### Output
```
darshini
```
