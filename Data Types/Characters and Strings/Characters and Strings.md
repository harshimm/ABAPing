# Characters 🅰️ 

- By default the length of character data type is 1.
- If length is not specified it truncates the remaining characters and returns only the first character of the string.
  
### Example 1 ✏️
```
DATA char_data TYPE c.
c = 'Hello World'.
WRITE / c.
```

### Output
```
H
```

- When length is specified (>= length of the string) then it prints the whole word.

### Example 2 ✏️
```
DATA char_data2 TYPE c LENGTH 40.
char_data2 = 'Hello World'.
WRITE / char_data2.
```

### Ouput
```
Hello World
```

# Strings 🔤
- An extensible character array that adjusts according to length of the string.
- No need to explicitly specify the length unlike character data type.

### Example ✏️
```
DATA char_data3 TYPE string.
char_data3 = 'Hello World'.
WRITE / char_data3.
```

### Ouput
```
Hello World
```
